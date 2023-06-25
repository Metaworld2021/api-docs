[Ui](../groups/Core.Ui.md) / PointerEvent

# PointerEvent <Badge type="tip" text="Class" /> <Score text="PointerEvent" />

点击或者滑动的时候传递mobile touch,鼠标,键盘信息的类

## Table of contents

| Accessors |
| :-----|
| **[effectingButton](mw.PointerEvent.md#effectingbutton)**(): [`KeyEvent`](mw.KeyEvent.md) <br> 获取响应的事件key|
| **[isTouchEvent](mw.PointerEvent.md#istouchevent)**(): `boolean` <br> 判断是不是触摸事件|
| **[lastScreenSpacePosition](mw.PointerEvent.md#lastscreenspaceposition)**(): [`Vector2`](mw.Vector2.md) <br> 获取该事件上一次的屏幕位置|
| **[mouseWheelDelta](mw.PointerEvent.md#mousewheeldelta)**(): `number` <br> 获取鼠标滚轮滑动的距离|
| **[pointerIndex](mw.PointerEvent.md#pointerindex)**(): `number` <br> 返回该事件的唯一标识index|
| **[screenSpacePosition](mw.PointerEvent.md#screenspaceposition)**(): [`Vector2`](mw.Vector2.md) <br> 获取触发的屏幕位置|
| **[touchPadIndex](mw.PointerEvent.md#touchpadindex)**(): `number` <br> 获取触摸事件index|
| **[userIndex](mw.PointerEvent.md#userindex)**(): `number` <br> 获取事件触发玩家的index|

| Methods |
| :-----|
| **[isMouseButtonDown](mw.PointerEvent.md#ismousebuttondown)**(`MouseButton`: [`Keys`](../enums/mw.Keys.md)): `boolean` <br> 判断是不是鼠标按键事件|
| **[toInputEvent](mw.PointerEvent.md#toinputevent)**(): [`InputEvent`](mw.InputEvent.md) <br> 转化为 InputEvent|

默认构造

## Accessors

### effectingButton <Score text="effectingButton" /> 

• `get` **effectingButton**(): [`KeyEvent`](mw.KeyEvent.md) <Badge type="tip" text="client" />

获取响应的事件key


#### Returns

[`KeyEvent`](mw.KeyEvent.md)

返回响应的事件key

___

### isTouchEvent <Score text="isTouchEvent" /> 

• `get` **isTouchEvent**(): `boolean` <Badge type="tip" text="client" />

判断是不是触摸事件


#### Returns

`boolean`

返回是否是触摸事件

___

### lastScreenSpacePosition <Score text="lastScreenSpacePosition" /> 

• `get` **lastScreenSpacePosition**(): [`Vector2`](mw.Vector2.md) <Badge type="tip" text="client" />

获取该事件上一次的屏幕位置


#### Returns

[`Vector2`](mw.Vector2.md)

返回该事件上一次的屏幕位置

___

### mouseWheelDelta <Score text="mouseWheelDelta" /> 

• `get` **mouseWheelDelta**(): `number` <Badge type="tip" text="client" />

获取鼠标滚轮滑动的距离


#### Returns

`number`

返回鼠标滚轮滑动距离

___

### pointerIndex <Score text="pointerIndex" /> 

• `get` **pointerIndex**(): `number` <Badge type="tip" text="client" />

返回该事件的唯一标识index


#### Returns

`number`

返回该事件的唯一标识index

___

### screenSpacePosition <Score text="screenSpacePosition" /> 

• `get` **screenSpacePosition**(): [`Vector2`](mw.Vector2.md) <Badge type="tip" text="client" />

获取触发的屏幕位置


#### Returns

[`Vector2`](mw.Vector2.md)

返回触发的屏幕位置

___

### touchPadIndex <Score text="touchPadIndex" /> 

• `get` **touchPadIndex**(): `number` <Badge type="tip" text="client" />

获取触摸事件index


#### Returns

`number`

返回触摸事件的index

___

### userIndex <Score text="userIndex" /> 

• `get` **userIndex**(): `number` <Badge type="tip" text="client" />

获取事件触发玩家的index


#### Returns

`number`

返回事件触发玩家的index

## Methods

### isMouseButtonDown <Score text="isMouseButtonDown" /> 

• **isMouseButtonDown**(`MouseButton`): `boolean` <Badge type="tip" text="client" />

判断是不是鼠标按键事件


#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `MouseButton` | [`Keys`](../enums/mw.Keys.md) | 按键事件 |

#### Returns

`boolean`

返回是不是鼠标按键事件

___

### toInputEvent <Score text="toInputEvent" /> 

• **toInputEvent**(): [`InputEvent`](mw.InputEvent.md) <Badge type="tip" text="client" />

转化为 InputEvent


#### Returns

[`InputEvent`](mw.InputEvent.md)

返回转化后 InputEvent
