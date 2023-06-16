[Gui](../groups/Core.Gui.md) / UIBehavior

# UIBehavior <Badge type="tip" text="Class" /> <Score text="UIBehavior" />

UI的驱动脚本基类

## Hierarchy

- **`UIBehavior`**

  ↳ [`IItemView`](../interfaces/mw.IItemView.md)

  ↳ [`IPanelView`](../interfaces/mw.IPanelView.md)

  ↳ [`BaseView`](mw.BaseView.md)

## Table of contents

| Accessors |
| :-----|
| **[canUpdate](mw.UIBehavior.md#canupdate)**(): `boolean` <br> 是否能触发onUpdate函数|
| **[fullScreen](mw.UIBehavior.md#fullscreen)**(`inFull`: `boolean`): `void` <br> 设置随父节点全屏适配,会验证父节点大小以保证跟随父节点的大小|
| **[layer](mw.UIBehavior.md#layer)**(): `number` <br> 获取UI的Layer层级,显示可能会影响到zOrder,使用UIManager显示UI时，|
| **[rootCanvas](mw.UIBehavior.md#rootcanvas)**(): [`Canvas`](mw.Canvas.md) <br> 获取UI的根Canvas节点|
| **[uiObject](mw.UIBehavior.md#uiobject)**(): [`Widget`](mw.Widget.md) <br> 获取脚本挂载的UI对象|
| **[uiWidgetBase](mw.UIBehavior.md#uiwidgetbase)**(): [`UserWidget`](mw.UserWidget.md) <br> 转化UIObject 为指定UserWidget对象|
| **[visible](mw.UIBehavior.md#visible)**(): `boolean` <br> 获取UI是否显示|

| Methods |
| :-----|
| **[destroy](mw.UIBehavior.md#destroy)**(): `void` <br> 销毁UI对象|
| **[detectDrag](mw.UIBehavior.md#detectdrag)**(`dragKey`: [`Keys`](../enums/mw.Keys.md)): [`EventReply`](mw.EventReply.md) <br> 触发DragDrop事件的检测|
| **[detectDragIfPressed](mw.UIBehavior.md#detectdragifpressed)**(`inPointEvent`: [`PointerEvent`](mw.PointerEvent.md), `dragKey`: [`Keys`](../enums/mw.Keys.md)): [`EventReply`](mw.EventReply.md) <br> 如果事件检测通过就触发DragDrop事件的回复|
| **[newDragDrop](mw.UIBehavior.md#newdragdrop)**(`inVisualWidget`: [`Widget`](mw.Widget.md), `inTag?`: `string`, `inPayLoad?`: `any`, `inPivot?`: [`DragPivot`](../enums/mw.DragPivot.md), `inOffset?`: [`Vector2`](mw.Vector2.md)): [`DragDropOperation`](mw.DragDropOperation.md) <br> 创建DragDrop事件|
| **[remove](mw.UIBehavior.md#remove)**(): `void` <br> 移除UI对象|
| **[setVisible](mw.UIBehavior.md#setvisible)**(`inVisible`: `boolean` \, `...params`: `any`[]): `void` <br> 设置UI是否显示,会触发绑定的脚本的OnShow/OnHide事件，可以传递参数|
| **[addBehavior](mw.UIBehavior.md#addbehavior)**(`key`: `string`, `value`: `any`): `void` <br> 添加一个全局的行为记录|
| **[clearBehavior](mw.UIBehavior.md#clearbehavior)**(): `void` <br> 清空全局的行为记录|
| **[getBehavior](mw.UIBehavior.md#getbehavior)**(`key`: `string`): `any` <br> 获取一个全局的行为记录|
| **[removeBehavior](mw.UIBehavior.md#removebehavior)**(`key`: `string`): `void` <br> 移除一个全局的行为记录|

## Accessors

### canUpdate <Score text="canUpdate" /> 

• `get` **canUpdate**(): `boolean` <Badge type="tip" text="client" />

是否能触发onUpdate函数


#### Returns

`boolean`

返回能否触发的标志

• `set` **canUpdate**(`bCanUpdate`): `void` <Badge type="tip" text="client" />

设置是否能触发onUpdate函数


#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `bCanUpdate` | `boolean` | 能否触发的标志 |


___

### fullScreen <Score text="fullScreen" /> 

• `set` **fullScreen**(`inFull`): `void` <Badge type="tip" text="client" />

设置随父节点全屏适配,会验证父节点大小以保证跟随父节点的大小


#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `inFull` | `boolean` |  设置为随父节点大小全屏适配 |


___

### layer <Score text="layer" /> 

• `get` **layer**(): `number` <Badge type="tip" text="client" />

获取UI的Layer层级,显示可能会影响到zOrder,使用UIManager显示UI时，
会根据Layer层级动态设置zOrder，每一次调用都会重新计算当前layer的新zOrder，确保UI位于当前层级的顶端


使用示例: 一般来说，可以使用内置定义好的，也可以是自定义拓展层级
```ts
UIManager.Instance.show(UIBehavior,UIBehavior.layer)
// 内置定义好的层级
[
UILayerScene,  //场景层 zOrder开始于0
UILayerBottom, //底层 zOrder开始于100000
UILayerMiddle, //中层 zOrder开始于200000
UILayerOwn     //独享层(调用此层会自动隐藏Bottom和Middle层) zOrder开始于300000
UILayerTop     //顶层 zOrder开始于400000
UILayerDialog  //对话层 zOrder开始于500000
UILayerSystem  //系统层 zOrder开始于600000
UILayerError   //错误层 这个层级不可以使用，需要增加层级可以使用UI.UIManager.Instance.addUILayerMap zOrder开始于700000
]
```

#### Returns

`number`

Layer层级

• `set` **layer**(`inLayer`): `void` <Badge type="tip" text="client" />

设置UI的所在的Layer层级,显示可能会影响到zOrder,使用UIManager显示UI时，
会根据Layer层级动态设置zOrder，每一次调用都会重新计算当前layer的新zOrder，确保UI位于当前层级的顶端


使用示例: 一般来说，可以使用内置定义好的，也可以自定义拓展层级
```ts
this.layer = UILayerScene;
// 内置定义好的层级
[
UILayerScene,  //场景层 zOrder开始于0
UILayerBottom, //底层 zOrder开始于100000
UILayerMiddle, //中层 zOrder开始于200000
UILayerOwn     //独享层(调用此层会自动隐藏Bottom和Middle层) zOrder开始于300000
UILayerTop     //顶层 zOrder开始于400000
UILayerDialog  //对话层 zOrder开始于500000
UILayerSystem  //系统层 zOrder开始于600000
UILayerError   //错误层 这个层级不可以使用，需要增加层级可以使用UI.UIManager.Instance.addUILayerMap zOrder开始于700000
]
```

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `inLayer` | `number` |  设置Layer层级 |


___

### rootCanvas <Score text="rootCanvas" /> 

• `get` **rootCanvas**(): [`Canvas`](mw.Canvas.md) <Badge type="tip" text="client" />

获取UI的根Canvas节点


#### Returns

[`Canvas`](mw.Canvas.md)

返回canvas节点

___

### uiObject <Score text="uiObject" /> 

• `get` **uiObject**(): [`Widget`](mw.Widget.md)

获取脚本挂载的UI对象

#### Returns

[`Widget`](mw.Widget.md)

脚本挂载的UI对象

___

### uiWidgetBase <Score text="uiWidgetBase" /> 

• `get` **uiWidgetBase**(): [`UserWidget`](mw.UserWidget.md) <Badge type="tip" text="client" />

转化UIObject 为指定UserWidget对象


#### Returns

[`UserWidget`](mw.UserWidget.md)

返回转化指定UserWidget对象

___

### visible <Score text="visible" /> 

• `get` **visible**(): `boolean` <Badge type="tip" text="client" />

获取UI是否显示


#### Returns

`boolean`

返回是否可见

• `set` **visible**(`inVisible`): `void` <Badge type="tip" text="client" />

设置UI是否显示,会触发绑定的脚本的OnShow/OnHide事件，需要传递参数的可以使用setVisible方法


#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `inVisible` | `boolean` |  设置是否可见 可见设置为SelfHitTestInvisible,不可见设置为Collapsed |


## Methods

### destroy <Score text="destroy" /> 

• **destroy**(): `void` <Badge type="tip" text="client" />

销毁UI对象



___

### detectDrag <Score text="detectDrag" /> 

• **detectDrag**(`dragKey`): [`EventReply`](mw.EventReply.md) <Badge type="tip" text="client" />

触发DragDrop事件的检测


#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `dragKey` | [`Keys`](../enums/mw.Keys.md) | 触发按键 default:Keys |

#### Returns

[`EventReply`](mw.EventReply.md)

返回触发的事件回复

___

### detectDragIfPressed <Score text="detectDragIfPressed" /> 

• **detectDragIfPressed**(`inPointEvent`, `dragKey`): [`EventReply`](mw.EventReply.md) <Badge type="tip" text="client" />

如果事件检测通过就触发DragDrop事件的回复


#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `inPointEvent` | [`PointerEvent`](mw.PointerEvent.md) | 传递触发的事件信息 |
| `dragKey` | [`Keys`](../enums/mw.Keys.md) | 触发按键 |

#### Returns

[`EventReply`](mw.EventReply.md)

返回触发的事件回复

___

### newDragDrop <Score text="newDragDrop" /> 

• **newDragDrop**(`inVisualWidget`, `inTag?`, `inPayLoad?`, `inPivot?`, `inOffset?`): [`DragDropOperation`](mw.DragDropOperation.md) <Badge type="tip" text="client" />

创建DragDrop事件


#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `inVisualWidget` | [`Widget`](mw.Widget.md) | 拖拽显示的UI控件 |
| `inTag?` | `string` | 标签文本 default:"" |
| `inPayLoad?` | `any` | 拖拽事件数据信息 default:null |
| `inPivot?` | [`DragPivot`](../enums/mw.DragPivot.md) | 拖拽显示UI的锚点 default:UIType.DragPivot.TopLeft |
| `inOffset?` | [`Vector2`](mw.Vector2.md) | 拖拽显示UI相对于锚点的偏移的百分比 default:vector2(0,0) |

#### Returns

[`DragDropOperation`](mw.DragDropOperation.md)

返回触发的事件回复

___

### remove <Score text="remove" /> 

• **remove**(): `void` <Badge type="tip" text="client" />

移除UI对象



___

### setVisible <Score text="setVisible" /> 

• **setVisible**(`inVisible`, `...params`): `void` <Badge type="tip" text="client" />

设置UI是否显示,会触发绑定的脚本的OnShow/OnHide事件，可以传递参数


#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `inVisible` | `boolean` \| [`SlateVisibility`](../enums/mw.SlateVisibility.md) |  设置是否可见,如果是boolean类型设置为SelfHitTestInvisible,不可见设置为Collapsed， 否则的话就是按照枚举拉设置具体的显示类型 |
| `...params` | `any`[] |  传递给onShow的参数 |


___

### addBehavior <Score text="addBehavior" /> 

• `Static` **addBehavior**(`key`, `value`): `void` <Badge type="tip" text="client" />

添加一个全局的行为记录


#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `key` | `string` |  行为标记 |
| `value` | `any` |  行为值 |


___

### clearBehavior <Score text="clearBehavior" /> 

• `Static` **clearBehavior**(): `void` <Badge type="tip" text="client" />

清空全局的行为记录



___

### getBehavior <Score text="getBehavior" /> 

• `Static` **getBehavior**(`key`): `any` <Badge type="tip" text="client" />

获取一个全局的行为记录


#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `key` | `string` |  行为标记 |

#### Returns

`any`

返回一个行为

___

### removeBehavior <Score text="removeBehavior" /> 

• `Static` **removeBehavior**(`key`): `void` <Badge type="tip" text="client" />

移除一个全局的行为记录


#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `key` | `string` |  行为标记 |

