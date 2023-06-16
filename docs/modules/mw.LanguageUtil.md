[mw](Core.mw.md) / LanguageUtil

# LanguageUtil <Badge type="tip" text="Namespace" /> <Score text="LanguageUtil" />

## Table of contents

| Functions |
| :-----|
| **[getLocTextValue](mw.LanguageUtil.md#getloctextvalue)**(`textkey`: `string`): `string` <br> 根据key获取翻译内容|
| **[locText](mw.LanguageUtil.md#loctext)**(`textkey`: `string`): `string` <br> 多语言标记|
| **[useLocalizedLanguage](mw.LanguageUtil.md#uselocalizedlanguage)**(`type`: [`LanguageType`](../enums/mw.LanguageType.md)): `boolean` <br> 游戏语言设置|

## Functions

### getLocTextValue <Score text="getLocTextValue" /> 

• **getLocTextValue**(`textkey`): `string` 

根据key获取翻译内容


#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `textkey` | `string` | 需要查找的翻译的key |

#### Returns

`string`

返回Key对应的当前语言环境的翻译内容

___

### locText <Score text="locText" /> 

• **locText**(`textkey`): `string` 

多语言标记


#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `textkey` | `string` | 用户多语言配置表收集的Key |

#### Returns

`string`

返回Key，此函数只用于做翻译文本收集标识。

___

### useLocalizedLanguage <Score text="useLocalizedLanguage" /> 

• **useLocalizedLanguage**(`type`): `boolean` 

游戏语言设置


#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `type` | [`LanguageType`](../enums/mw.LanguageType.md) | 切换游戏语言种类 |

#### Returns

`boolean`

true修改成功 false修改失败
