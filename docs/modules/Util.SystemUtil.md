[Util](Util.Util.md) / SystemUtil

# SystemUtil <Badge type="tip" text="Namespace" /> <Score text="SystemUtil" />

## Table of contents

| Variables |
| :-----|
| **[currentPlatform](Util.SystemUtil.md#currentplatform)**: `string` <br> 判定当前程序的运行平台,返回值参考Type.RuntimePlatform|
| **[isPIE](Util.SystemUtil.md#ispie)**: `boolean` <br> 判定当前程序的运行环境是否为PIE|

| Functions |
| :-----|
| **[getCurrentEnv](Util.SystemUtil.md#getcurrentenv)**(): `string` <br> 获取当前环境|
| **[getDefaultGraphicsCPULevel](Util.SystemUtil.md#getdefaultgraphicscpulevel)**(): [`GraphicsLevel`](../enums/Type.GraphicsLevel.md) <br> 获取默认CPU画质等级|
| **[getDefaultGraphicsGPULevel](Util.SystemUtil.md#getdefaultgraphicsgpulevel)**(): [`GraphicsLevel`](../enums/Type.GraphicsLevel.md) <br> 获取默认GPU画质等级|
| **[getEditorVersion](Util.SystemUtil.md#geteditorversion)**(): `string` <br> 获取编辑器版本号|
| **[getFullEditorVersion](Util.SystemUtil.md#getfulleditorversion)**(): `string` <br> 获取完整编辑器版本号|
| **[getGameId](Util.SystemUtil.md#getgameid)**(): `string` <br> 获取当前游戏GameId|
| **[getGraphicsCPULevel](Util.SystemUtil.md#getgraphicscpulevel)**(): [`GraphicsLevel`](../enums/Type.GraphicsLevel.md) <br> 获取当前CPU画质等级|
| **[getGraphicsGPULevel](Util.SystemUtil.md#getgraphicsgpulevel)**(): [`GraphicsLevel`](../enums/Type.GraphicsLevel.md) <br> 获取当前GPU画质等级|
| **[getVersion](Util.SystemUtil.md#getversion)**(): `string` <br> 获取当前游戏版本|
| **[isClient](Util.SystemUtil.md#isclient)**(): `boolean` <br> 是否客户端运行|
| **[isMobile](Util.SystemUtil.md#ismobile)**(): `boolean` <br> 判断当前是否是移动端|
| **[isServer](Util.SystemUtil.md#isserver)**(): `boolean` <br> 是否服务器运行|
| **[setGraphicsCPULevel](Util.SystemUtil.md#setgraphicscpulevel)**(`CPULevel`: [`GraphicsLevel`](../enums/Type.GraphicsLevel.md)): `void` <br> 设置当前CPU画质等级|
| **[setGraphicsGPULevel](Util.SystemUtil.md#setgraphicsgpulevel)**(`GPULevel`: [`GraphicsLevel`](../enums/Type.GraphicsLevel.md)): `void` <br> 设置当前GPU画质等级|

## Variables

### currentPlatform <Score text="currentPlatform" /> 

• `Const` **currentPlatform**: `string` 

判定当前程序的运行平台,返回值参考Type.RuntimePlatform


使用示例:创建一个名为SystemExample的脚本，放置在对象栏中，打开脚本，将原本内容修改为如下内容，保存并运行游戏，会将当前运行环境打印到控制台
```ts
@Core.Class
export default class SystemExample extends Core.Script {

    protected onStart(): void {
        this.test();
    }

    private async test(): Promise<void> {
        console.log("当前程序的运行平台", SystemUtil.currentPlatform)
    }

}
```

___

### isPIE <Score text="isPIE" /> 

• `Const` **isPIE**: `boolean` 

判定当前程序的运行环境是否为PIE


## Functions

### getCurrentEnv <Score text="getCurrentEnv" /> 

• **getCurrentEnv**(): `string` 

获取当前环境


使用示例:创建一个名为SystemExample的脚本，放置在对象栏中，打开脚本，将原本内容修改为如下内容，保存并运行游戏，会将当前环境打印到控制台
```ts
@Core.Class
export default class SystemExample extends Core.Script {

    protected onStart(): void {
        this.test();
    }

    private async test(): Promise<void> {
        console.log("当前环境", SystemUtil.getCurrentEnv())
    }

}
```

#### Returns

`string`

当前环境,返回值包含(Dev/Test/Meta/Pre/Online/dev-oversea/test-oversea/pre-oversea/online-oversea/tc-sa-saopaulo-playza)

___

### getDefaultGraphicsCPULevel <Score text="getDefaultGraphicsCPULevel" /> 

• **getDefaultGraphicsCPULevel**(): [`GraphicsLevel`](../enums/Type.GraphicsLevel.md) <Badge type="tip" text="client" />

获取默认CPU画质等级


使用示例:创建一个名为SystemExample的脚本，放置在对象栏中，打开脚本，将原本内容修改为如下内容，保存并运行游戏，会将默认CPU画质等级打印到控制台
```ts
@Core.Class
export default class SystemExample extends Core.Script {

    protected onStart(): void {
        this.test();
    }

    private async test(): Promise<void> {
        let level = SystemUtil.getDefaultGraphicsCPULevel();
        console.log("默认画质等级", level);
//0-9 0为最低 9为最高
    }

}
```

#### Returns

[`GraphicsLevel`](../enums/Type.GraphicsLevel.md)

默认画质等级

___

### getDefaultGraphicsGPULevel <Score text="getDefaultGraphicsGPULevel" /> 

• **getDefaultGraphicsGPULevel**(): [`GraphicsLevel`](../enums/Type.GraphicsLevel.md) <Badge type="tip" text="client" />

获取默认GPU画质等级


使用示例:创建一个名为SystemExample的脚本，放置在对象栏中，打开脚本，将原本内容修改为如下内容，保存并运行游戏，会将默认GPU画质等级打印到控制台
```ts
@Core.Class
export default class SystemExample extends Core.Script {

    protected onStart(): void {
        this.test();
    }

    private async test(): Promise<void> {
        let level = SystemUtil.getDefaultGraphicsGPULevel();
        console.log("默认GPU画质等级", level);
//0-9 0为最低 9为最高
    }

}
```

#### Returns

[`GraphicsLevel`](../enums/Type.GraphicsLevel.md)

默认画质等级

___

### getEditorVersion <Score text="getEditorVersion" /> 

• **getEditorVersion**(): `string` 

获取编辑器版本号


使用示例:创建一个名为SystemExample的脚本，放置在对象栏中，打开脚本，将原本内容修改为如下内容，保存并运行游戏，会将当前编辑器版本号打印到控制台
```ts
@Core.Class
export default class SystemExample extends Core.Script {

    protected onStart(): void {
        this.test();
    }

    private async test(): Promise<void> {
        console.log("当前编辑器版本号", SystemUtil.getEditorVersion())
    }

}
```

#### Returns

`string`

当前编辑器版本号

___

### getFullEditorVersion <Score text="getFullEditorVersion" /> 

• **getFullEditorVersion**(): `string` 

获取完整编辑器版本号


使用示例:创建一个名为SystemExample的脚本，放置在对象栏中，打开脚本，将原本内容修改为如下内容，保存并运行游戏，会将当前完整编辑器版本号打印到控制台
```ts
@Core.Class
export default class SystemExample extends Core.Script {

    protected onStart(): void {
        this.test();
    }

    private async test(): Promise<void> {
        console.log("当前完整编辑器版本号", SystemUtil.getFullEditorVersion())
    }

}
```

#### Returns

`string`

当前完整编辑器版本号

___

### getGameId <Score text="getGameId" /> 

• **getGameId**(): `string` 

获取当前游戏GameId


使用示例:创建一个名为SystemExample的脚本，放置在对象栏中，打开脚本，将原本内容修改为如下内容，保存并运行游戏，输出当前游戏GameId pc端输出为空，移动端输出为游戏GameId
```ts
@Core.Class
export default class SystemExample extends Core.Script {

    protected onStart(): void {
        this.test();
    }

    private async test(): Promise<void> {
        if (!SystemUtil.isClient()) return;
        const gameId = SystemUtil.getGameId();
        console.log(`gameId: ${gameId}`);
    }

}
```

#### Returns

`string`

当前游戏GameId

___

### getGraphicsCPULevel <Score text="getGraphicsCPULevel" /> 

• **getGraphicsCPULevel**(): [`GraphicsLevel`](../enums/Type.GraphicsLevel.md) <Badge type="tip" text="client" />

获取当前CPU画质等级


使用示例:创建一个名为SystemExample的脚本，放置在对象栏中，打开脚本，将原本内容修改为如下内容，保存并运行游戏，会将当前CPU画质等级打印到控制台
```ts
@Core.Class
export default class SystemExample extends Core.Script {

    protected onStart(): void {
        this.test();
    }

    private async test(): Promise<void> {
        let level = SystemUtil.getGraphicsCPULevel();
        console.log("当前CPU画质等级", level);
//0-9 0为最低 9为最高
    }

}
```

#### Returns

[`GraphicsLevel`](../enums/Type.GraphicsLevel.md)

画质等级

___

### getGraphicsGPULevel <Score text="getGraphicsGPULevel" /> 

• **getGraphicsGPULevel**(): [`GraphicsLevel`](../enums/Type.GraphicsLevel.md) <Badge type="tip" text="client" />

获取当前GPU画质等级


使用示例:创建一个名为SystemExample的脚本，放置在对象栏中，打开脚本，将原本内容修改为如下内容，保存并运行游戏，会将当前GPU画质等级打印到控制台
```ts
@Core.Class
export default class SystemExample extends Core.Script {

    protected onStart(): void {
        this.test();
    }

    private async test(): Promise<void> {
        let level = SystemUtil.getGraphicsGPULevel();
        console.log("当前GPU画质等级", level);
//0-9 0为最低 9为最高
    }

}
```

#### Returns

[`GraphicsLevel`](../enums/Type.GraphicsLevel.md)

画质等级

___

### getVersion <Score text="getVersion" /> 

• **getVersion**(): `string` 

获取当前游戏版本


使用示例:创建一个名为SystemExample的脚本，放置在对象栏中，打开脚本，将原本内容修改为如下内容，保存并运行游戏，输出当前游戏版本 pc端输出为空，移动端输出为游戏版本
```ts
@Core.Class
export default class SystemExample extends Core.Script {

    protected onStart(): void {
        this.test();
    }

    private async test(): Promise<void> {
        if (!SystemUtil.isClient()) return;
        const version = SystemUtil.getVersion();
        console.log(`version: ${version}`);
    }

}
```

#### Returns

`string`

当前游戏版本

___

### isClient <Score text="isClient" /> 

• **isClient**(): `boolean` 

是否客户端运行


使用示例:创建一个名为SystemExample的脚本，放置在对象栏中，打开脚本，将原本内容修改为如下内容，保存并运行游戏，会将当前运行环境打印到控制台
```ts
@Core.Class
export default class SystemExample extends Core.Script {

    protected onStart(): void {
        this.test();
    }

    private async test(): Promise<void> {
        if (SystemUtil.isClient()) {
            console.log("当前是客户端");
        } else if (SystemUtil.isServer()) {
            console.log("当前是服务端");
        }
    }

}
```

#### Returns

`boolean`

是否客户端运行

___

### isMobile <Score text="isMobile" /> 

• **isMobile**(): `boolean` 

判断当前是否是移动端


使用示例:创建一个名为SystemExample的脚本，放置在对象栏中，打开脚本，将原本内容修改为如下内容，保存并运行游戏，会将当前是否是移动端打印到控制台
```ts
@Core.Class
export default class SystemExample extends Core.Script {

    protected onStart(): void {
        this.test();
    }

    private async test(): Promise<void> {
        console.log("当前是否是移动端", SystemUtil.isMobile())
    }

}
```

#### Returns

`boolean`

是否是移动端

___

### isServer <Score text="isServer" /> 

• **isServer**(): `boolean` 

是否服务器运行


使用示例:创建一个名为SystemExample的脚本，放置在对象栏中，打开脚本，将原本内容修改为如下内容，保存并运行游戏，会将当前运行环境打印到控制台
```ts
@Core.Class
export default class SystemExample extends Core.Script {

    protected onStart(): void {
        this.test();
    }

    private async test(): Promise<void> {
        if (SystemUtil.isClient()) {
            console.log("当前是客户端");
        } else if (SystemUtil.isServer()) {
            console.log("当前是服务端");
        }
    }

}
```

#### Returns

`boolean`

是否服务器运行

___

### setGraphicsCPULevel <Score text="setGraphicsCPULevel" /> 

• **setGraphicsCPULevel**(`CPULevel`): `void` <Badge type="tip" text="client" />

设置当前CPU画质等级


使用示例:创建一个名为SystemExample的脚本，放置在对象栏中，打开脚本，将原本内容修改为如下内容，保存并运行游戏，按F键将CPU画质等级设置为最低，按G键将CPU画质等级设置为最高
```ts
@Core.Class
export default class SystemExample extends Core.Script {

    protected onStart(): void {
        this.test();
    }

    private async test(): Promise<void> {
        if (!SystemUtil.isClient()) return;
        InputUtil.onKeyDown(Keys.F, () => {
            SystemUtil.setGraphicsCPULevel(Type.GraphicsLevel.Low1);
        })
        InputUtil.onKeyDown(Keys.G, () => {
            SystemUtil.setGraphicsCPULevel(Type.GraphicsLevel.Cinematic3);
        })
    }

}
```

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `CPULevel` | [`GraphicsLevel`](../enums/Type.GraphicsLevel.md) | CPU画质等级 |


___

### setGraphicsGPULevel <Score text="setGraphicsGPULevel" /> 

• **setGraphicsGPULevel**(`GPULevel`): `void` <Badge type="tip" text="client" />

设置当前GPU画质等级


使用示例:创建一个名为SystemExample的脚本，放置在对象栏中，打开脚本，将原本内容修改为如下内容，保存并运行游戏，按F键将GPU画质等级设置为最低，按G键将GPU画质等级设置为最高
```ts
@Core.Class
export default class SystemExample extends Core.Script {

    protected onStart(): void {
        this.test();
    }

    private async test(): Promise<void> {
        if (!SystemUtil.isClient()) return;
        InputUtil.onKeyDown(Keys.F, () => {
            SystemUtil.setGraphicsGPULevel(Type.GraphicsLevel.Low1);
        })
        InputUtil.onKeyDown(Keys.G, () => {
            SystemUtil.setGraphicsGPULevel(Type.GraphicsLevel.Cinematic3);
        })
    }

}
```

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `GPULevel` | [`GraphicsLevel`](../enums/Type.GraphicsLevel.md) | GPU画质等级 |

