[基类](../groups/Extension.基类.md) / Subdata

# Subdata <Badge type="tip" text="Class" /> <Score text="Subdata" />

数据控制类的基类

1. 为什么需要数据控制中心？

- 数据控制中心可以帮助我们将数据进行永久存储。

- 数据控制中心实现了服务端和客户端的数据同步。

- 数据控制中心实现了数据缓存，降低与KV服务器的交互频率。

- 数据控制中心实现了模块数据的统一管理。

【定义数据方便】数据体只需要继承SubData，数据就能自动被DataCenter管理起来

【保存数据方便】保存数据只需要调用父类SubData的save方法，即可实现保存

【获取数据方便】获取数据只需要传入数据体的类名，即可获取到对应数据

2. 数据控制中心是如何工作的？

数据上方标注的 @Decorator.saveProperty 装饰器有两个作用：

- 让字段能够被永久存储（永久存储可以认为当退出游戏后，再次打开游戏，会存储上次游戏数据继续玩）

- 让字段能够被同步到客户端

- 没有标注 @Decorator.saveProperty 装饰器将丧失永久存储和同步至客户端的能力。

3. 通过改写 ModuleService 中的示例，数据控制中心如何使用：

<span style="font-size: 14px;">
使用示例: C&S 和数据模块组合。
</span>

```ts
@Component
export default class GameStart extends Script {

    protected onStart(): void {
        ModuleService.registerModule(AppleModS, AppleModC, AppleData);
    }

}
class AppleData extends Subdata {

    @Decorator.persistence()
    appleNum : number = 10;

    public removeApple() {
        this.appleNum -= 1;
        this.save(true);
    }
    public addApple() {
        this.appleNum += 1;
        this.save(true);
    }
}
class AppleModS extends ModuleS<AppleModC,AppleData> {

    public net_appleChange(player:Player) {
        let curPlayer = DataCenterS.getData(this.currentPlayer, AppleData);
        curPlayer.removeApple();
        const otherPlayer = DataCenterS.getData(player, AppleData);
        otherPlayer.addApple();
    }
}
class AppleModC extends ModuleC<AppleModS, AppleData> {

    public npc:Player;

    protected onStart(): void {
        InputUtil.onKeyDown(Keys.P, () => {
            Player.getAllPlayers().forEach( (element) => {
                if(element != this.localPlayer){
                    this.npc = element;
                }
            });
            ModuleService.getModule(AppleModC).sendApple(this.npc);
        });
        InputUtil.onKeyDown(Keys.O, async () => {
            await DataCenterC.ready();
            let apple = DataCenterC.getData(AppleData).appleNum;
            console.log("The current number of apples of the client player is:" + apple);
        });
    }
    public sendApple(player:Player) {
        this.server.net_appleChange(player);
    }
}
```

## Table of contents

### Properties <Score text="Properties" /> 
| **[onDataChange](mwext.Subdata.md#ondatachange)**: [`Action`](mw.Action.md)  |
| :-----|
| 数据变化的委托|

### Accessors <Score text="Accessors" /> 
| **[currentVersion](mwext.Subdata.md#currentversion)**(): `number`  |
| :-----|
| 当前数据版本号，和version配合使用，可实现数据升级|
| **[version](mwext.Subdata.md#version)**(): `number`  |
| 数据版本号，数据有变化需要重写，和currentVersion配合使用，可实现数据升级|

### Methods <Score text="Methods" /> 
| **[getSavedProperty](mwext.Subdata.md#getsavedproperty)**<`T`: \>(`propertyName`: `string`): `T`:    |
| :-----|
| 通过属性名获取存储的属性值(用作数据升级，读取之前已经存储的数据)|
| **[initDefaultData](mwext.Subdata.md#initdefaultdata)**(): `void`   |
| 初始化默认数据，需要请复写|
| **[onDataInit](mwext.Subdata.md#ondatainit)**(): `void`   |
| 数据初始化完成调用，需要请复写，可在这个方法中实现数据升级|
| **[save](mwext.Subdata.md#save)**(`syncToClient`: `boolean`): [`Subdata`](mwext.Subdata.md) <Badge type="tip" text="server" />  |
| 保存数据|
| **[syncToClient](mwext.Subdata.md#synctoclient)**(): [`Subdata`](mwext.Subdata.md) <Badge type="tip" text="server" />  |
| 向客户端同步数据|

## Properties

### onDataChange <Score text="onDataChange" /> 

• `Readonly` **onDataChange**: [`Action`](mw.Action.md)

数据变化的委托

## Accessors

### currentVersion <Score text="currentVersion" /> 

<table class="get-set-table">
<thead><tr>
<th style="text-align: left">

• `Protected` `get` **currentVersion**(): `number`

</th>
<th style="text-align: left">

• `Protected` `set` **currentVersion**(`value`): `void`

</th>
</tr></thead>
<tbody><tr>
<td style="text-align: left">


当前数据版本号，和version配合使用，可实现数据升级

#### Returns

| `number` |  |
| :------ | :------ |


</td>
<td style="text-align: left">


当前数据版本号，和version配合使用，可实现数据升级

#### Parameters

| `value` | `number` |
| :------ | :------ |



</td>
</tr></tbody>
</table>

___

### version <Score text="version" /> 

<table class="get-set-table">
<thead><tr>
<th style="text-align: left">

• `Protected` `get` **version**(): `number`

</th>
</tr></thead>
<tbody><tr>
<td style="text-align: left">


数据版本号，数据有变化需要重写，和currentVersion配合使用，可实现数据升级

#### Returns

</td>
</tr></tbody>
</table>

| `number` |  |
| :------ | :------ |

## Methods

### getSavedProperty <Score text="getSavedProperty" /> 

• `Protected` **getSavedProperty**<`T`\>(`propertyName`): `T` 

通过属性名获取存储的属性值(用作数据升级，读取之前已经存储的数据)

#### Parameters

| `propertyName` `string` |  属性名 range: |
| :------ | :------ |

#### Returns

| `T` | 属性值 |
| :------ | :------ |

#### Type parameters

| Name |
| :------ |
| `T` |

___

### initDefaultData <Score text="initDefaultData" /> 

• `Protected` **initDefaultData**(): `void` 

初始化默认数据，需要请复写


___

### onDataInit <Score text="onDataInit" /> 

• `Protected` **onDataInit**(): `void` 

数据初始化完成调用，需要请复写，可在这个方法中实现数据升级


::: warning Precautions

这个方法调用完成后，你需要保证currentVersion和version是相等的

:::

___

### save <Score text="save" /> 

• **save**(`syncToClient`): [`Subdata`](mwext.Subdata.md) <Badge type="tip" text="server" />

保存数据

#### Parameters

| `syncToClient` `boolean` |  是否同步给客户端 |
| :------ | :------ |

#### Returns

| [`Subdata`](mwext.Subdata.md) | 自身 |
| :------ | :------ |

修改数据时，只有调用了 save 并设置参数为 true 时，才会同步至对应客户端。

___

### syncToClient <Score text="syncToClient" /> 

• **syncToClient**(): [`Subdata`](mwext.Subdata.md) <Badge type="tip" text="server" />

向客户端同步数据

#### Returns

| [`Subdata`](mwext.Subdata.md) | 自身 |
| :------ | :------ |
