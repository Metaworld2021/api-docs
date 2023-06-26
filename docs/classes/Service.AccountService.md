[Social](../groups/Social.Social.md) / AccountService

# AccountService <Badge type="tip" text="Class" /> <Score text="AccountService" />

**`Instance`**

用户账号信息管理相关服务

::: warning Precautions

单例类，请使用getInstance获取对象

:::

## Table of contents

| Methods |
| :-----|
| **[addFriend](Service.AccountService.md#addfriend)**(`resp`: [`MGSResponse`](../modules/Service.Service.md#mgsresponse), `friendOpenId`: `string`, `reason`: `string`): `void` <br> 向233发起addFriend并获得回调|
| **[applySharedId](Service.AccountService.md#applysharedid)**(`character`: [`CharacterBase`](Gameplay.CharacterBase.md), `id`: `string`, `callback`: [`BoolResponse`](../modules/Service.Service.md#boolresponse)): `void` <br> 应用分享Id的角色数据|
| **[checkVIP](Service.AccountService.md#checkvip)**(`userId`: `string`, `gameId`: `string`, `callback`: (`result`: `string`) => `void`): `void` <br> 发起checkVIP并获得回调，查询玩家的vip信息|
| **[createSharedId](Service.AccountService.md#createsharedid)**(`character`: [`CharacterBase`](Gameplay.CharacterBase.md), `callback`: [`StringResponse`](../modules/Service.Service.md#stringresponse)): `void` <br> 生成分享Id|
| **[dataShowToOther](Service.AccountService.md#datashowtoother)**(`index`: `number`, `isOpen`: `boolean`, `callback?`: [`BoolResponse`](../modules/Service.Service.md#boolresponse)): `void` <br> 设置数据是否公开给其他用户|
| **[downloadData](Service.AccountService.md#downloaddata)**(`character`: [`CharacterBase`](Gameplay.CharacterBase.md), `callback?`: [`BoolResponse`](../modules/Service.Service.md#boolresponse) \, `index?`: `number`): `void` <br> 下载角色形象并应用到当前角色身上|
| **[fillAvatar](Service.AccountService.md#fillavatar)**(`img`: [`Image`](UI.Image.md)): `void` <br> 将头像赋值到Image变量上|
| **[getNickName](Service.AccountService.md#getnickname)**(): `string` <br> 获取玩家昵称|
| **[getOpenId](Service.AccountService.md#getopenid)**(): `string` <br> 获取OpenId|
| **[getUserData](Service.AccountService.md#getuserdata)**(`userId`: `string`, `index`: `number`, `callback`: [`StringResponse`](../modules/Service.Service.md#stringresponse)): `void` <br> 获取用户存储在服务器上的角色形象数据|
| **[getUserId](Service.AccountService.md#getuserid)**(): `string` <br> 获取平台的用户Id,可以用于getUserData接口|
| **[getUserInfo](Service.AccountService.md#getuserinfo)**(`userId`: `string`, `gameId`: `string`, `callback`: (`nickname`: `string`, `gender`: `number`) => `void`): `void` <br> 发起getUserInfo并获得回调，查询玩家的昵称、性别|
| **[isFriend](Service.AccountService.md#isfriend)**(`resp`: [`MGSResponse`](../modules/Service.Service.md#mgsresponse), `friendOpenId`: `string`): `void` <br> 若需要检测玩家是否好友关系，可通过调用isFriend接口进行查看|
| **[setUserData](Service.AccountService.md#setuserdata)**(`character`: [`CharacterBase`](Gameplay.CharacterBase.md), `dataString`: `string`, `callback?`: [`BoolResponse`](../modules/Service.Service.md#boolresponse)): `void` <br> 将角色形象数据应用至角色|
| **[uploadData](Service.AccountService.md#uploaddata)**(`character`: [`CharacterBase`](Gameplay.CharacterBase.md), `callback?`: [`BoolResponse`](../modules/Service.Service.md#boolresponse) \, `index?`: `number`, `openStatus?`: `number`): `void` <br> 上传角色形象资源到服务器  Character， Hair, UpperCloth, LowerCloth, Gloves, Shoe|
| **[getInstance](Service.AccountService.md#getinstance)**(): [`AccountService`](Service.AccountService.md) <br> 获取用户账号信息管理器全局实例|

## Methods

### addFriend <Score text="addFriend" /> 

• **addFriend**(`resp`, `friendOpenId`, `reason`): `void` 

向233发起addFriend并获得回调


::: warning Precautions

只在移动端由233拉起生效

:::

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `resp` | [`MGSResponse`](../modules/Service.Service.md#mgsresponse) | 233的回调 |
| `friendOpenId` | `string` | 要加的平台账号id |
| `reason` | `string` | 申请理由 |


___

### applySharedId <Score text="applySharedId" /> 

• **applySharedId**(`character`, `id`, `callback`): `void` <Badge type="tip" text="client" />

应用分享Id的角色数据


#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `character` | [`CharacterBase`](Gameplay.CharacterBase.md) | 分享换装数据的角色 |
| `id` | `string` | 分享Id |
| `callback` | [`BoolResponse`](../modules/Service.Service.md#boolresponse) |  回调参数，true:应用成功；false:应用失败 |


___

### checkVIP <Score text="checkVIP" /> 

• **checkVIP**(`userId`, `gameId`, `callback`): `void` 

发起checkVIP并获得回调，查询玩家的vip信息


#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `userId` | `string` | 平台账号id(openId) |
| `gameId` | `string` | GameId |
| `callback` | (`result`: `string`) => `void` | 返回 result，玩家的vip是否正常 |


___

### createSharedId <Score text="createSharedId" /> 

• **createSharedId**(`character`, `callback`): `void` <Badge type="tip" text="client" />

生成分享Id


#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `character` | [`CharacterBase`](Gameplay.CharacterBase.md) | 分享换装数据的角色 |
| `callback` | [`StringResponse`](../modules/Service.Service.md#stringresponse) |  回调参数，返回生成的Id |


___

### dataShowToOther <Score text="dataShowToOther" /> 

• **dataShowToOther**(`index`, `isOpen`, `callback?`): `void` <Badge type="tip" text="client" />

设置数据是否公开给其他用户


#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `index` | `number` | 资源位(0-5) default:0,主角资源位 |
| `isOpen` | `boolean` | 是否公开 |
| `callback?` | [`BoolResponse`](../modules/Service.Service.md#boolresponse) | 设置是否成功的回调 default:无回调 |


___

### downloadData <Score text="downloadData" /> 

• **downloadData**(`character`, `callback?`, `index?`): `void` <Badge type="tip" text="client" />

下载角色形象并应用到当前角色身上


#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `character` | [`CharacterBase`](Gameplay.CharacterBase.md) | 要应用换装数据的角色 |
| `callback?` | [`BoolResponse`](../modules/Service.Service.md#boolresponse) \| [`VoidResponse`](../modules/Service.Service.md#voidresponse) | 设置是否成功的回调 default:默认没有回调 |
| `index?` | `number` | 角色位(0-5) default:0,主角资源位 |


___

### fillAvatar <Score text="fillAvatar" /> 

• **fillAvatar**(`img`): `void` <Badge type="tip" text="client" />

将头像赋值到Image变量上


::: warning Precautions

只在由233拉起生效

:::

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `img` | [`Image`](UI.Image.md) | 需要赋值获得头像的Image变量 |


___

### getNickName <Score text="getNickName" /> 

• **getNickName**(): `string` <Badge type="tip" text="client" />

获取玩家昵称


::: warning Precautions

只在由233拉起生效

:::

#### Returns

`string`

昵称

___

### getOpenId <Score text="getOpenId" /> 

• **getOpenId**(): `string` <Badge type="tip" text="client" />

获取OpenId


::: warning Precautions

只在由233拉起生效

:::

#### Returns

`string`

OpenId

___

### getUserData <Score text="getUserData" /> 

• **getUserData**(`userId`, `index`, `callback`): `void` <Badge type="tip" text="client" />

获取用户存储在服务器上的角色形象数据


#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `userId` | `string` | 用户Id |
| `index` | `number` | 资源位(0-5) |
| `callback` | [`StringResponse`](../modules/Service.Service.md#stringresponse) | 返回获取的数据string. |


___

### getUserId <Score text="getUserId" /> 

• **getUserId**(): `string` <Badge type="tip" text="client" />

获取平台的用户Id,可以用于getUserData接口


#### Returns

`string`

用户Id

___

### getUserInfo <Score text="getUserInfo" /> 

• **getUserInfo**(`userId`, `gameId`, `callback`): `void` 

发起getUserInfo并获得回调，查询玩家的昵称、性别


#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `userId` | `string` | 平台账号id(openId) |
| `gameId` | `string` | GameId |
| `callback` | (`nickname`: `string`, `gender`: `number`) => `void` | 返回 nickname(string) 和 gender(number) |


___

### isFriend <Score text="isFriend" /> 

• **isFriend**(`resp`, `friendOpenId`): `void` 

若需要检测玩家是否好友关系，可通过调用isFriend接口进行查看


::: warning Precautions

只在移动端由233拉起生效

:::

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `resp` | [`MGSResponse`](../modules/Service.Service.md#mgsresponse) | 233的回调 |
| `friendOpenId` | `string` | 要确定的平台账号id |


___

### setUserData <Score text="setUserData" /> 

• **setUserData**(`character`, `dataString`, `callback?`): `void` <Badge type="tip" text="client" />

将角色形象数据应用至角色


#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `character` | [`CharacterBase`](Gameplay.CharacterBase.md) |  用于换装的角色 |
| `dataString` | `string` |  返回的数据 |
| `callback?` | [`BoolResponse`](../modules/Service.Service.md#boolresponse) | 设置是否成功的回调 default:无回调 |


___

### uploadData <Score text="uploadData" /> 

• **uploadData**(`character`, `callback?`, `index?`, `openStatus?`): `void` <Badge type="tip" text="client" />

上传角色形象资源到服务器  Character， Hair, UpperCloth, LowerCloth, Gloves, Shoe


#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `character` | [`CharacterBase`](Gameplay.CharacterBase.md) | 要上传换装数据的角色 |
| `callback?` | [`BoolResponse`](../modules/Service.Service.md#boolresponse) \| [`VoidResponse`](../modules/Service.Service.md#voidresponse) | 设置是否成功的回调 default:默认没有回调 |
| `index?` | `number` | 角色位(0-5) default:0,主角资源位 |
| `openStatus?` | `number` | 开发状态 default:1,默认是开放状态 |


___

### getInstance <Score text="getInstance" /> 

• `Static` **getInstance**(): [`AccountService`](Service.AccountService.md) 

获取用户账号信息管理器全局实例


#### Returns

[`AccountService`](Service.AccountService.md)

用户账号信息管理器全局实例
