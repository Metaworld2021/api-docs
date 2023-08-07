LOCALIZATION

# LOCALIZATION <Badge type="tip" text="Groups" /> <Score text="LOCALIZATION" />

## Table of contents
| Modules Functions |
| :-----|
| **[getDefaultLocale](LOCALIZATION.LOCALIZATION.md#getdefaultlocale)**(): `string` <br> 获取默认的语言和地区|
| **[getLocTextValue](LOCALIZATION.LOCALIZATION.md#getloctextvalue)**(`textkey`: `string`): `string` <br> 根据key获取翻译内容|
| **[locText](LOCALIZATION.LOCALIZATION.md#loctext)**(`textkey`: `string`): `string` <br> 多语言标记|
| **[useLocalizedLanguage](LOCALIZATION.LOCALIZATION.md#uselocalizedlanguage)**(`type`: [`LanguageType`](../enums/Type.LanguageType.md)): `boolean` <br> 游戏语言设置|


## Modules Functions


___

### getDefaultLocale <Score text="getDefaultLocale" /> 

• **getDefaultLocale**(): `string` 

获取默认的语言和地区


使用示例:调用方法
```ts
const locale = LocaleUtil.getDefaultLocale();
console.log(`locale: ${locale}`);
// zh-CN
```

#### Returns

`string`

以IETF语言标签表示的字符串包含:ISO 639-1 两位字母语言码 (如, "zh");
可选ISO 15924 四位字母脚本码 (如, "Hans");
___

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
| `type` | [`LanguageType`](../enums/Type.LanguageType.md) | 切换游戏语言种类 |

#### Returns

`boolean`
