[UI](../groups/Core.UI.md) / ButtonTouchMethod

# ButtonTouchMethod <Badge type="tip" text="Enumeration" /> <Score text="ButtonTouchMethod" />

按钮触摸响应规则

## Table of contents

| Enumeration Members |
| :-----|
| **[Down](mw.ButtonTouchMethod.md#down)** = ``1`` <br> |
| **[DownAndUp](mw.ButtonTouchMethod.md#downandup)** = ``0`` <br> |
| **[PreciseTap](mw.ButtonTouchMethod.md#precisetap)** = ``2`` <br> |

## Enumeration Members

### Down <Score text="Down" /> 

• **Down** = ``1``

点击将在触碰时立即触发，触碰将不会被捕获。

___

### DownAndUp <Score text="DownAndUp" /> 

• **DownAndUp** = ``0``

大多数按钮都是这样的按下并且抬起才会触发

___

### PreciseTap <Score text="PreciseTap" /> 

• **PreciseTap** = ``2``

在列表中，只能通过精确点击按钮。
移动指针将滚动列表。
