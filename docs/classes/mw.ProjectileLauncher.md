[Gameplay](../groups/Core.Gameplay.md) / ProjectileLauncher

# ProjectileLauncher <Badge type="tip" text="Class" /> <Score text="ProjectileLauncher" />

投掷物发射器，作为发射终端，维护投掷物发射相关的参数，发射的投掷物只在客户端存在，且以主控端的事件为主

## Hierarchy

- [`GameObject`](mw.GameObject.md)

  ↳ **`ProjectileLauncher`**

## Table of contents

| Properties |
| :-----|
| **[onProjectileDestroy](mw.ProjectileLauncher.md#onprojectiledestroy)**: [`MulticastDelegate`](mw.MulticastDelegate.md)<() => `void`\> <br> 投掷物被销毁时触发绑定函数|
| **[onProjectileHit](mw.ProjectileLauncher.md#onprojectilehit)**: [`MulticastDelegate`](mw.MulticastDelegate.md)<(`hitActor`: [`GameObject`](mw.GameObject.md), `normalImpulse`: [`Vector`](mw.Vector.md), `hitResult`: [`HitResult`](mw.HitResult.md)) => `void`\> <br> 投掷物击中物体时触发绑定函数|
| **[onProjectileSpawned](mw.ProjectileLauncher.md#onprojectilespawned)**: [`MulticastDelegate`](mw.MulticastDelegate.md)<(`spawnedInstance`: [`GameObject`](mw.GameObject.md)) => `void`\> <br> 投掷物生成实例时触发绑定函数，此回调触发时实例还没有开始移动，建议将此函数作为临时附着网格体或特效时使用|


::: details 点击查看继承
| Properties |
| :-----|
| **[onDestroyDelegate](mw.GameObject.md#ondestroydelegate)**: [`MulticastDelegate`](mw.MulticastDelegate.md)<() => `void`\> <br> 物体Destroy事件回调|
| **[scriptNumberPropPathMap](mw.GameObject.md#scriptnumberproppathmap)**: `any` <br> |
| **[scriptPropPathNumberMap](mw.GameObject.md#scriptproppathnumbermap)**: `any` <br> |
:::


| Accessors |
| :-----|
| **[acceleration](mw.ProjectileLauncher.md#acceleration)**(): `number` <br> 加速度值，正值加速，负值减速|
| **[accelerationEnable](mw.ProjectileLauncher.md#accelerationenable)**(): `boolean` <br> 投掷物是否在发射后受加速度影响|
| **[accelerationEnableDistance](mw.ProjectileLauncher.md#accelerationenabledistance)**(): `number` <br> 发射后多长距离后启用加速度|
| **[accelerationEnableMode](mw.ProjectileLauncher.md#accelerationenablemode)**(): [`ProjectileAccelerationEnableMode`](../enums/mw.ProjectileAccelerationEnableMode.md) <br> 加速度按照 时间 / 距离 后生效|
| **[accelerationEnableTime](mw.ProjectileLauncher.md#accelerationenabletime)**(): `number` <br> 发射后多长时间后启用加速度|
| **[collisionLossCoefficient](mw.ProjectileLauncher.md#collisionlosscoefficient)**(): `number` <br> 投掷物每次执行穿透后速度衰减的系数，系数为正，每次穿透后速度减少，系数为负，每次穿透后速度增加。|
| **[collisionMode](mw.ProjectileLauncher.md#collisionmode)**(): [`ProjectileCollisionMode`](../enums/mw.ProjectileCollisionMode.md) <br> 投掷物碰撞后如何运动：穿透/反弹|
| **[detectionRadius](mw.ProjectileLauncher.md#detectionradius)**(): `number` <br> 投掷物检测碰撞的宽度|
| **[gravitationalAcceleration](mw.ProjectileLauncher.md#gravitationalacceleration)**(): `number` <br> 重力值，正值重力向下，负值重力向上|
| **[gravityEnable](mw.ProjectileLauncher.md#gravityenable)**(): `boolean` <br> 投掷物是否在发射后受重力影响|
| **[gravityEnableDistance](mw.ProjectileLauncher.md#gravityenabledistance)**(): `number` <br> 发射后多长距离后启用重力|
| **[gravityEnableMode](mw.ProjectileLauncher.md#gravityenablemode)**(): [`ProjectileAccelerationEnableMode`](../enums/mw.ProjectileAccelerationEnableMode.md) <br> 重力按照 时间 / 距离 后生效|
| **[gravityEnableTime](mw.ProjectileLauncher.md#gravityenabletime)**(): `number` <br> 发射后多长时间后启用重力|
| **[initialSpeed](mw.ProjectileLauncher.md#initialspeed)**(): `number` <br> 投掷物发射的初始速度|
| **[isAutoDestroy](mw.ProjectileLauncher.md#isautodestroy)**(): `boolean` <br> 投掷物超出有效射程距离或者运动持续时间后自动销毁|
| **[launchDirection](mw.ProjectileLauncher.md#launchdirection)**(): [`Rotation`](mw.Rotation.md) <br> 投掷物发射方向|
| **[lifeSpan](mw.ProjectileLauncher.md#lifespan)**(): `number` <br> 投掷物运动持续时间，超出后投掷物不再运动。|
| **[maxCollisionTimes](mw.ProjectileLauncher.md#maxcollisiontimes)**(): `number` <br> 允许投掷物执行穿透的次数，超出次数后，再次碰撞投掷物不再移动。|
| **[maxSpeed](mw.ProjectileLauncher.md#maxspeed)**(): `number` <br> 投掷物发射后的最大速度|
| **[range](mw.ProjectileLauncher.md#range)**(): `number` <br> 投掷物有效射程距离，超出后投掷物不再运动。|
| **[startLocation](mw.ProjectileLauncher.md#startlocation)**(): [`Vector`](mw.Vector.md) <br> 投掷物起始位置|
| **[traceLineStyle](mw.ProjectileLauncher.md#tracelinestyle)**(): [`ProjectileLineStyle`](../enums/mw.ProjectileLineStyle.md) <br> 轨迹风格|


::: details 点击查看继承
| Accessors |
| :-----|
| **[guid](mw.GameObject.md#guid)**(): `string` <br> 获取对象的GUID（唯一标识一个对象的字符串）。|
| **[isLocked](mw.GameObject.md#islocked)**(): `boolean` <br> 获取对象是否锁定|
| **[isReady](mw.GameObject.md#isready)**(): `boolean` <br> 当前物体状态|
| **[isStatic](mw.GameObject.md#isstatic)**(): `boolean` <br> 获取对象是否静态|
| **[localTransform](mw.GameObject.md#localtransform)**(): [`Transform`](mw.Transform.md) <br> 当前物体本地transform|
| **[name](mw.GameObject.md#name)**(): `string` <br> 返回当前物体名称|
| **[netStatus](mw.GameObject.md#netstatus)**(): [`NetStatus`](../enums/mw.NetStatus.md) <br> 获取当前物体同步状态|
| **[parent](mw.GameObject.md#parent)**(): [`GameObject`](mw.GameObject.md) <br> 获取当前父物体|
| **[sourceAssetGuid](mw.GameObject.md#sourceassetguid)**(): `string` <br> 获取当前物体使用资源的GUID|
| **[tag](mw.GameObject.md#tag)**(): `string` <br> 获取当前物体的Tag|
| **[useUpdate](mw.GameObject.md#useupdate)**(): `boolean` <br> 获取对象是否使用更新|
| **[worldTransform](mw.GameObject.md#worldtransform)**(): [`Transform`](mw.Transform.md) <br> 当前物体世界transform|
:::


| Methods |
| :-----|
| **[bindPlayer](mw.ProjectileLauncher.md#bindplayer)**(`player`: [`Player`](mw.Player.md)): `boolean` <br> 绑定玩家|
| **[drawPredictedTrajectory](mw.ProjectileLauncher.md#drawpredictedtrajectory)**(`density?`: `number`, `duration?`: `number`): `void` <br> 绘制路径预测的轨迹，调一次开启，掉第二次即关闭，如此循环|
| **[predictedTrajectory](mw.ProjectileLauncher.md#predictedtrajectory)**(`density`: `number`, `duration`: `number`): [`Vector`](mw.Vector.md)[] <br> 获取路径预测的轨迹|
| **[spawnProjectileInstanceLaunch](mw.ProjectileLauncher.md#spawnprojectileinstancelaunch)**(): [`ProjectileInst`](mw.ProjectileInst.md) <br> 发射子弹实例|
| **[spawnProjectileInstanceLaunchToTarget](mw.ProjectileLauncher.md#spawnprojectileinstancelaunchtotarget)**(`location`: [`Vector`](mw.Vector.md), `time?`: `number`, `speed?`: `number`): [`ProjectileInst`](mw.ProjectileInst.md) <br> 发射子弹实例|
| **[unbindPlayer](mw.ProjectileLauncher.md#unbindplayer)**(): `void` <br> 解绑玩家|


::: details 点击查看继承
| Methods |
| :-----|
| **[asyncReady](mw.GameObject.md#asyncready)**(): `Promise`<[`GameObject`](mw.GameObject.md)\> <br> GameObject准备好后返回|
| **[attachToGameObject](mw.GameObject.md#attachtogameobject)**(`obj`: [`GameObject`](mw.GameObject.md)): `void` <br> 将物体附着到指定物体上|
| **[clone](mw.GameObject.md#clone)**(`spawnInfo?`: `boolean` \): [`GameObject`](mw.GameObject.md) <br> 复制对象|
| **[destroy](mw.GameObject.md#destroy)**(): `void` <br> 删除对象|
| **[detachFromGameObject](mw.GameObject.md#detachfromgameobject)**(): `void` <br> 将此物体与当前附着的物体分离|
| **[follow](mw.GameObject.md#follow)**(`Target`: [`GameObject`](mw.GameObject.md), `Radius?`: `number`, `OnSuccess?`: () => `void`, `OnFail?`: () => `void`): `void` <br> 跟随目标|
| **[getBoundingBoxSize](mw.GameObject.md#getboundingboxsize)**(`nonColliding?`: `boolean`, `includeFromChildActors?`: `boolean`, `outer?`: [`Vector`](mw.Vector.md)): [`Vector`](mw.Vector.md) <br> 获取物体包围盒大小|
| **[getBounds](mw.GameObject.md#getbounds)**(`onlyCollidingComponents`: `boolean`, `OriginOuter`: [`Vector`](mw.Vector.md), `BoxExtentOuter`: [`Vector`](mw.Vector.md), `includeFromChildActors?`: `boolean`): `void` <br> 获取GameObject边界|
| **[getChildByGuid](mw.GameObject.md#getchildbyguid)**(`GUID`: `string`): `undefined` \| [`GameObject`](mw.GameObject.md) <br> 根据GUID查找子物体|
| **[getChildByName](mw.GameObject.md#getchildbyname)**(`name`: `string`): `undefined` \| [`GameObject`](mw.GameObject.md) <br> 根据名称查找子物体|
| **[getChildByPath](mw.GameObject.md#getchildbypath)**(`path`: `string`): [`GameObject`](mw.GameObject.md) <br> 根据路径查找子物体|
| **[getChildren](mw.GameObject.md#getchildren)**(): `undefined` \| [`GameObject`](mw.GameObject.md)[] <br> 获取Children|
| **[getChildrenBoxCenter](mw.GameObject.md#getchildrenboxcenter)**(`outer?`: [`Vector`](mw.Vector.md)): [`Vector`](mw.Vector.md) <br> 获取所有子对象包围盒中心点(不包含父对象,父对象不可用返回[0,0,0])|
| **[getChildrenByName](mw.GameObject.md#getchildrenbyname)**(`name`: `string`): [`GameObject`](mw.GameObject.md)[] <br> 通过名字查找所有的子物体|
| **[getScriptByGuid](mw.GameObject.md#getscriptbyguid)**(`GUID`: `string`): `undefined` \| `Script` <br> 获得当前物体下的指定脚本|
| **[getScriptByName](mw.GameObject.md#getscriptbyname)**(`name`: `string`): `undefined` \| `Script` <br> 获得当前物体下的指定脚本|
| **[getScripts](mw.GameObject.md#getscripts)**(): `undefined` \| `Script`[] <br> 获得当前物体下的所有脚本|
| **[getVisibility](mw.GameObject.md#getvisibility)**(): `boolean` <br> 获取GameObject是否被显示|
| **[isRunningClient](mw.GameObject.md#isrunningclient)**(): `boolean` <br> 是否为客户端|
| **[navigateTo](mw.GameObject.md#navigateto)**(`Location`: [`Vector`](mw.Vector.md), `Radius?`: `number`, `OnSuccess?`: () => `void`, `OnFail?`: () => `void`): `void` <br> 向目标点进行寻路移动|
| **[onDestroy](mw.GameObject.md#ondestroy)**(): `void` <br> 周期函数 被销毁时调用|
| **[onReplicated](mw.GameObject.md#onreplicated)**(`path`: `string`, `value`: `unknown`, `oldVal`: `unknown`): `void` <br> 属性被同步事件 ClientOnly|
| **[onStart](mw.GameObject.md#onstart)**(): `void` <br> 周期函数 脚本开始执行时调用|
| **[onUpdate](mw.GameObject.md#onupdate)**(`dt`: `number`): `void` <br> 周期函数 useUpdate 设置为 true 后,每帧被执行,设置为false,不会执行|
| **[setVisibility](mw.GameObject.md#setvisibility)**(`status`: [`PropertyStatus`](../enums/mw.PropertyStatus.md), `propagateToChildren?`: `boolean`): `void` <br> 设置GameObject是否被显示|
| **[stopFollow](mw.GameObject.md#stopfollow)**(): `void` <br> 停止跟随|
| **[stopNavigateTo](mw.GameObject.md#stopnavigateto)**(): `void` <br> 停止向目标点寻路移动|
| **[asyncFindGameObjectByGuid](mw.GameObject.md#asyncfindgameobjectbyguid)**(`guid`: `string`): `Promise`<[`GameObject`](mw.GameObject.md)\> <br> 通过guid异步查找GameObject,默认是五秒,可以通过 `core.setGlobalAsyncOverTime(5000);|
| **[asyncGetGameObjectByPath](mw.GameObject.md#asyncgetgameobjectbypath)**(`path`: `string`): `Promise`<[`GameObject`](mw.GameObject.md)\> <br> 通过路径异步查找物体|
| **[asyncSpawn](mw.GameObject.md#asyncspawn)**<`T`: extends [`GameObject`](mw.GameObject.md)<`T`\>\>(`spawnInfo`: [`GameObjectInfo`](../interfaces/mw.GameObjectInfo.md)): `Promise`<`T`: extends [`GameObject`](mw.GameObject.md)<`T`\>\> <br> 异步构造一个 GameObject 资源不存在会先去下载资源再去创建|
| **[findGameObjectByGuid](mw.GameObject.md#findgameobjectbyguid)**(`guid`: `string`): [`GameObject`](mw.GameObject.md) <br> 通过guid查找GameObject|
| **[findGameObjectByName](mw.GameObject.md#findgameobjectbyname)**(`name`: `string`): `undefined` \| [`GameObject`](mw.GameObject.md) <br> 通过名字查找物体|
| **[findGameObjectsByName](mw.GameObject.md#findgameobjectsbyname)**(`name`: `string`): [`GameObject`](mw.GameObject.md)[] <br> 通过名字查找物体|
| **[findGameObjectsByTag](mw.GameObject.md#findgameobjectsbytag)**(`tag`: `string`): [`GameObject`](mw.GameObject.md)[] <br> 通过自定义tag获取GameObject|
| **[getGameObjectByPath](mw.GameObject.md#getgameobjectbypath)**(`path`: `string`): [`GameObject`](mw.GameObject.md) <br> 通过路径查找物体|
| **[spawn](mw.GameObject.md#spawn)**<`T`: extends [`GameObject`](mw.GameObject.md)<`T`\>\>(`[spawn](mw.GameObject.md#spawn)Info`): `T`: extends [`GameObject`](mw.GameObject.md)<`T`\> <br> 构造一个 GameObject|
:::


### onProjectileDestroy <Score text="onProjectileDestroy" /> 

• **onProjectileDestroy**: [`MulticastDelegate`](mw.MulticastDelegate.md)<() => `void`\>

投掷物被销毁时触发绑定函数

::: warning Precautions

所有投掷物都是使用的同一个回调，请不要循环添加事件绑定函数

:::

___

### onProjectileHit <Score text="onProjectileHit" /> 

• **onProjectileHit**: [`MulticastDelegate`](mw.MulticastDelegate.md)<(`hitActor`: [`GameObject`](mw.GameObject.md), `normalImpulse`: [`Vector`](mw.Vector.md), `hitResult`: [`HitResult`](mw.HitResult.md)) => `void`\>

投掷物击中物体时触发绑定函数

::: warning Precautions

所有投掷物都是使用的同一个回调，请不要循环添加事件绑定函数

:::

使用示例: 如下示例展示此委托的参数的含义和使用方法
```ts
projectileLauncher.onProjectileHit.add((hitActor: GameObject, normalImpulse: Vector, hitResult: HitResult) => {
    // hitActor: 投掷物击中的物体
    // normalImpulse: 碰撞法线
    // hitResult: 碰撞详细信息
})
```

___

### onProjectileSpawned <Score text="onProjectileSpawned" /> 

• **onProjectileSpawned**: [`MulticastDelegate`](mw.MulticastDelegate.md)<(`spawnedInstance`: [`GameObject`](mw.GameObject.md)) => `void`\>

投掷物生成实例时触发绑定函数，此回调触发时实例还没有开始移动，建议将此函数作为临时附着网格体或特效时使用

::: warning Precautions

所有投掷物都是使用的同一个回调，请不要循环添加事件绑定函数。每个客户端执行的都是单端的，不会自动同步

:::

使用示例: 如下示例展示此委托的参数的含义和使用方法
```ts
projectile.onProjectileSpawned.add((spawnedInstance: GameObject) => {
    // spawnedInstance: 生成的示例，用户可以向这个实例上设置属性和附着对象

    // 向发射的投掷物上附着一个特效或静态物体
    const decorate = GameObject.spawnGameObject("<静态物体 / 特效的 GUID>");
    decorate.attachToGameObject(spawnedInstance);
})
```

## Accessors

### acceleration <Score text="acceleration" /> 

• `get` **acceleration**(): `number`

加速度值，正值加速，负值减速

#### Returns

`number`

• `set` **acceleration**(`value`): `void`

加速度值，正值加速，负值减速

#### Parameters

| Name | Type |
| :------ | :------ |
| `value` | `number` |


___

### accelerationEnable <Score text="accelerationEnable" /> 

• `get` **accelerationEnable**(): `boolean`

投掷物是否在发射后受加速度影响

#### Returns

`boolean`

• `set` **accelerationEnable**(`value`): `void`

投掷物是否在发射后受加速度影响

#### Parameters

| Name | Type |
| :------ | :------ |
| `value` | `boolean` |


___

### accelerationEnableDistance <Score text="accelerationEnableDistance" /> 

• `get` **accelerationEnableDistance**(): `number`

发射后多长距离后启用加速度

#### Returns

`number`

• `set` **accelerationEnableDistance**(`value`): `void`

发射后多长距离后启用加速度

#### Parameters

| Name | Type |
| :------ | :------ |
| `value` | `number` |


___

### accelerationEnableMode <Score text="accelerationEnableMode" /> 

• `get` **accelerationEnableMode**(): [`ProjectileAccelerationEnableMode`](../enums/mw.ProjectileAccelerationEnableMode.md)

加速度按照 时间 / 距离 后生效

#### Returns

[`ProjectileAccelerationEnableMode`](../enums/mw.ProjectileAccelerationEnableMode.md)

• `set` **accelerationEnableMode**(`value`): `void`

加速度按照 时间 / 距离 后生效

#### Parameters

| Name | Type |
| :------ | :------ |
| `value` | [`ProjectileAccelerationEnableMode`](../enums/mw.ProjectileAccelerationEnableMode.md) |


___

### accelerationEnableTime <Score text="accelerationEnableTime" /> 

• `get` **accelerationEnableTime**(): `number`

发射后多长时间后启用加速度

#### Returns

`number`

• `set` **accelerationEnableTime**(`value`): `void`

发射后多长时间后启用加速度

#### Parameters

| Name | Type |
| :------ | :------ |
| `value` | `number` |


___

### collisionLossCoefficient <Score text="collisionLossCoefficient" /> 

• `get` **collisionLossCoefficient**(): `number`

投掷物每次执行穿透后速度衰减的系数，系数为正，每次穿透后速度减少，系数为负，每次穿透后速度增加。

#### Returns

`number`

• `set` **collisionLossCoefficient**(`value`): `void`

投掷物每次执行穿透后速度衰减的系数，系数为正，每次穿透后速度减少，系数为负，每次穿透后速度增加。

#### Parameters

| Name | Type |
| :------ | :------ |
| `value` | `number` |


___

### collisionMode <Score text="collisionMode" /> 

• `get` **collisionMode**(): [`ProjectileCollisionMode`](../enums/mw.ProjectileCollisionMode.md)

投掷物碰撞后如何运动：穿透/反弹

#### Returns

[`ProjectileCollisionMode`](../enums/mw.ProjectileCollisionMode.md)

• `set` **collisionMode**(`value`): `void`

投掷物碰撞后如何运动：穿透/反弹

#### Parameters

| Name | Type |
| :------ | :------ |
| `value` | [`ProjectileCollisionMode`](../enums/mw.ProjectileCollisionMode.md) |


___

### detectionRadius <Score text="detectionRadius" /> 

• `get` **detectionRadius**(): `number`

投掷物检测碰撞的宽度

#### Returns

`number`

• `set` **detectionRadius**(`value`): `void`

投掷物检测碰撞的宽度

#### Parameters

| Name | Type |
| :------ | :------ |
| `value` | `number` |


___

### gravitationalAcceleration <Score text="gravitationalAcceleration" /> 

• `get` **gravitationalAcceleration**(): `number`

重力值，正值重力向下，负值重力向上

#### Returns

`number`

• `set` **gravitationalAcceleration**(`value`): `void`

重力值，正值重力向下，负值重力向上

#### Parameters

| Name | Type |
| :------ | :------ |
| `value` | `number` |


___

### gravityEnable <Score text="gravityEnable" /> 

• `get` **gravityEnable**(): `boolean`

投掷物是否在发射后受重力影响

#### Returns

`boolean`

• `set` **gravityEnable**(`value`): `void`

投掷物是否在发射后受重力影响

#### Parameters

| Name | Type |
| :------ | :------ |
| `value` | `boolean` |


___

### gravityEnableDistance <Score text="gravityEnableDistance" /> 

• `get` **gravityEnableDistance**(): `number`

发射后多长距离后启用重力

#### Returns

`number`

• `set` **gravityEnableDistance**(`value`): `void`

发射后多长距离后启用重力

#### Parameters

| Name | Type |
| :------ | :------ |
| `value` | `number` |


___

### gravityEnableMode <Score text="gravityEnableMode" /> 

• `get` **gravityEnableMode**(): [`ProjectileAccelerationEnableMode`](../enums/mw.ProjectileAccelerationEnableMode.md)

重力按照 时间 / 距离 后生效

#### Returns

[`ProjectileAccelerationEnableMode`](../enums/mw.ProjectileAccelerationEnableMode.md)

• `set` **gravityEnableMode**(`value`): `void`

重力按照 时间 / 距离 后生效

#### Parameters

| Name | Type |
| :------ | :------ |
| `value` | [`ProjectileAccelerationEnableMode`](../enums/mw.ProjectileAccelerationEnableMode.md) |


___

### gravityEnableTime <Score text="gravityEnableTime" /> 

• `get` **gravityEnableTime**(): `number`

发射后多长时间后启用重力

#### Returns

`number`

• `set` **gravityEnableTime**(`value`): `void`

发射后多长时间后启用重力

#### Parameters

| Name | Type |
| :------ | :------ |
| `value` | `number` |


___

### initialSpeed <Score text="initialSpeed" /> 

• `get` **initialSpeed**(): `number`

投掷物发射的初始速度

#### Returns

`number`

• `set` **initialSpeed**(`value`): `void`

投掷物发射的初始速度

#### Parameters

| Name | Type |
| :------ | :------ |
| `value` | `number` |


___

### isAutoDestroy <Score text="isAutoDestroy" /> 

• `get` **isAutoDestroy**(): `boolean`

投掷物超出有效射程距离或者运动持续时间后自动销毁

#### Returns

`boolean`

• `set` **isAutoDestroy**(`value`): `void`

投掷物超出有效射程距离或者运动持续时间后自动销毁

#### Parameters

| Name | Type |
| :------ | :------ |
| `value` | `boolean` |


___

### launchDirection <Score text="launchDirection" /> 

• `get` **launchDirection**(): [`Rotation`](mw.Rotation.md)

投掷物发射方向

#### Returns

[`Rotation`](mw.Rotation.md)

• `set` **launchDirection**(`value`): `void`

投掷物发射方向

#### Parameters

| Name | Type |
| :------ | :------ |
| `value` | [`Rotation`](mw.Rotation.md) |


___

### lifeSpan <Score text="lifeSpan" /> 

• `get` **lifeSpan**(): `number`

投掷物运动持续时间，超出后投掷物不再运动。

#### Returns

`number`

• `set` **lifeSpan**(`value`): `void`

投掷物运动持续时间，超出后投掷物不再运动。

#### Parameters

| Name | Type |
| :------ | :------ |
| `value` | `number` |


___

### maxCollisionTimes <Score text="maxCollisionTimes" /> 

• `get` **maxCollisionTimes**(): `number`

允许投掷物执行穿透的次数，超出次数后，再次碰撞投掷物不再移动。

#### Returns

`number`

• `set` **maxCollisionTimes**(`value`): `void`

允许投掷物执行穿透的次数，超出次数后，再次碰撞投掷物不再移动。

#### Parameters

| Name | Type |
| :------ | :------ |
| `value` | `number` |


___

### maxSpeed <Score text="maxSpeed" /> 

• `get` **maxSpeed**(): `number`

投掷物发射后的最大速度

#### Returns

`number`

• `set` **maxSpeed**(`value`): `void`

投掷物发射后的最大速度

#### Parameters

| Name | Type |
| :------ | :------ |
| `value` | `number` |


___

### range <Score text="range" /> 

• `get` **range**(): `number`

投掷物有效射程距离，超出后投掷物不再运动。

#### Returns

`number`

• `set` **range**(`value`): `void`

投掷物有效射程距离，超出后投掷物不再运动。

#### Parameters

| Name | Type |
| :------ | :------ |
| `value` | `number` |


___

### startLocation <Score text="startLocation" /> 

• `get` **startLocation**(): [`Vector`](mw.Vector.md)

投掷物起始位置

#### Returns

[`Vector`](mw.Vector.md)

• `set` **startLocation**(`value`): `void`

投掷物起始位置

#### Parameters

| Name | Type |
| :------ | :------ |
| `value` | [`Vector`](mw.Vector.md) |


___

### traceLineStyle <Score text="traceLineStyle" /> 

• `get` **traceLineStyle**(): [`ProjectileLineStyle`](../enums/mw.ProjectileLineStyle.md)

轨迹风格

#### Returns

[`ProjectileLineStyle`](../enums/mw.ProjectileLineStyle.md)

• `set` **traceLineStyle**(`value`): `void`

轨迹风格

#### Parameters

| Name | Type |
| :------ | :------ |
| `value` | [`ProjectileLineStyle`](../enums/mw.ProjectileLineStyle.md) |



## Methods
___

### bindPlayer <Score text="bindPlayer" /> 

• **bindPlayer**(`player`): `boolean` <Badge type="tip" text="other" />

绑定玩家

调用端自动广播

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `player` | [`Player`](mw.Player.md) |  玩家类 |

#### Returns

`boolean`

true：参数 player 有效，绑定成功

___

### drawPredictedTrajectory <Score text="drawPredictedTrajectory" /> 

• **drawPredictedTrajectory**(`density?`, `duration?`): `void` <Badge type="tip" text="client" />

绘制路径预测的轨迹，调一次开启，掉第二次即关闭，如此循环

::: warning Precautions

如果只绘制了一个点，可能投掷物被卡住了

:::


#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `density?` | `number` |  密度，值越大路径点越密，性能消耗越大 default: 15 |
| `duration?` | `number` |  预测的时长 default: 2 |


___

### predictedTrajectory <Score text="predictedTrajectory" /> 

• **predictedTrajectory**(`density`, `duration`): [`Vector`](mw.Vector.md)[] 

获取路径预测的轨迹


::: warning Precautions

如果返回的数组长度为1，可能投掷物被卡住了

:::

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `density` | `number` |  密度，值越大路径点越细，性能消耗越大 |
| `duration` | `number` |  预测的时长 |

#### Returns

[`Vector`](mw.Vector.md)[]

路径轨迹点

___

### spawnProjectileInstanceLaunch <Score text="spawnProjectileInstanceLaunch" /> 

• **spawnProjectileInstanceLaunch**(): [`ProjectileInst`](mw.ProjectileInst.md) 

发射子弹实例

::: warning Precautions

发射后再更新其他属性无法对本次发射的子弹产生影响；允许重复发射，注意服务端发射时，返回的值是无效的

:::


#### Returns

[`ProjectileInst`](mw.ProjectileInst.md)

投掷物v2实例

___

### spawnProjectileInstanceLaunchToTarget <Score text="spawnProjectileInstanceLaunchToTarget" /> 

• **spawnProjectileInstanceLaunchToTarget**(`location`, `time?`, `speed?`): [`ProjectileInst`](mw.ProjectileInst.md) 

发射子弹实例

::: warning Precautions

发射后再更新其他属性无法对本次发射的子弹产生影响；允许重复发送

:::


#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `location` | [`Vector`](mw.Vector.md) |  发射位置 |
| `time?` | `number` | 最大飞行时长 default:5 |
| `speed?` | `number` | 初始速度 default:1000 |

#### Returns

[`ProjectileInst`](mw.ProjectileInst.md)

投掷物v2实例

___

### unbindPlayer <Score text="unbindPlayer" /> 

• **unbindPlayer**(): `void` <Badge type="tip" text="other" />

解绑玩家

调用端自动广播

