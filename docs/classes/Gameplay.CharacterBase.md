[AVATAR](../groups/AVATAR.AVATAR.md) / CharacterBase

# CharacterBase <Badge type="tip" text="Class" /> <Score text="CharacterBase" />

角色基类,派生自GameObject,在GameObject的基础上提供对角色的高级封装,是玩家角色跟非玩家角色的基类,该对象是基类,无法使用构造函数创建此对象.主要功能分三大块:形象设置,动画,移动.
             形象设置上,角色目前可以选择 V1人形,V2人形,四足,自定义形象等.
             动画上,可以使用高度封装的姿态对象和直接播放动画.
             移动功能上,支持对角色的基础移动属性进行查询和更改,比如移动速度,转向速度,移动控制模式等,还提供了地面移动,空中移动,水中移动的模式切换.

## Hierarchy

- [`GameObject`](Gameplay.GameObject.md)

  ↳ **`CharacterBase`**

  ↳↳ [`AICharacter`](Gameplay.Gameplay.AICharacter.md)

  ↳↳ [`Character`](Gameplay.Character.md)

  ↳↳ [`Humanoid`](Gameplay.Gameplay.Humanoid.md)

  ↳↳ [`NPC`](Gameplay.NPC.md)

## Table of contents

| Properties |
| :-----|
| **[onLoadAppearanceDataAllCompleted](Gameplay.CharacterBase.md#onloadappearancedataallcompleted)**: [`MulticastDelegate`](Type.MulticastDelegate.md)<[`LoadAppearanceDataAllCompletedCallback`](../modules/Gameplay.Gameplay.md#loadappearancedataallcompletedcallback)\> <br> 加载完角色形象数据后的回调|
| **[onLoadDecorationsAllCompleted](Gameplay.CharacterBase.md#onloaddecorationsallcompleted)**: [`MulticastDelegate`](Type.MulticastDelegate.md)<[`LoadDecorationsAllCompletedCallback`](../modules/Gameplay.Gameplay.md#loaddecorationsallcompletedcallback)\> <br> 加载完角色形象数据后的回调|
| **[onMeshChanged](Gameplay.CharacterBase.md#onmeshchanged)**: [`MulticastDelegate`](Type.MulticastDelegate.md)<[`onAppearanceDataChanged`](../modules/Gameplay.Gameplay.md#onappearancedatachanged)\> <br> 角色模型切换成功广播|
| **[onMovementStateChanged](Gameplay.CharacterBase.md#onmovementstatechanged)**: [`OnMovementStateChanged`](../modules/Gameplay.Gameplay.md#onmovementstatechanged) <br> 移动状态切换时的回调|
| **[onSetAppearanceDataCompleted](Gameplay.CharacterBase.md#onsetappearancedatacompleted)**: [`MulticastDelegate`](Type.MulticastDelegate.md)<[`SetAppearanceDataCallback`](../modules/Gameplay.Gameplay.md#setappearancedatacallback)\> <br> 设置一个角色编辑API成功后的回调|
| **[onTextureChanged](Gameplay.CharacterBase.md#ontexturechanged)**: [`MulticastDelegate`](Type.MulticastDelegate.md)<[`onAppearanceDataChanged`](../modules/Gameplay.Gameplay.md#onappearancedatachanged)\> <br> 角色贴图切换成功广播|
| **[player](Gameplay.CharacterBase.md#player)**: [`Player`](Gameplay.Player.md) <br> 玩家对象|

| Accessors |
| :-----|
| **[airControl](Gameplay.CharacterBase.md#aircontrol)**(): `number` <br> 角色在空中时, 控制水平方向移动的灵活度|
| **[airControlBoostMultiplier](Gameplay.CharacterBase.md#aircontrolboostmultiplier)**(): `number` <br> 当角色空中水平移动速率比airControlBoostVelocityThreshold小时, 对airControl效果加倍的倍数|
| **[airControlBoostVelocityThreshold](Gameplay.CharacterBase.md#aircontrolboostvelocitythreshold)**(): `number` <br> 下落控制提升速率阈值, 当角色在空中时水平移动速率小于此值, 就会依照airControlBoostMultiplier的值对airControl效果进行加倍|
| **[animationMode](Gameplay.CharacterBase.md#animationmode)**(): [`AnimationMode`](../enums/Gameplay.AnimationMode.md) <br> 动画播放模式|
| **[appearanceType](Gameplay.CharacterBase.md#appearancetype)**(): [`AppearanceType`](../enums/Gameplay.AppearanceType.md) <br> 形象类型|
| **[baseShadowLocationOffset](Gameplay.CharacterBase.md#baseshadowlocationoffset)**(): [`Vector2`](Type.Vector2.md) <br> 模拟阴影相对于角色脚底中心的位置偏移|
| **[baseShadowMaxVisibleHeight](Gameplay.CharacterBase.md#baseshadowmaxvisibleheight)**(): `number` <br> 模拟阴影可见的最大离地高度|
| **[baseShadowScale](Gameplay.CharacterBase.md#baseshadowscale)**(): [`Vector2`](Type.Vector2.md) <br> 模拟阴影的缩放|
| **[basicStance](Gameplay.CharacterBase.md#basicstance)**(): `string` <br> 基础姿态|
| **[basicStanceAimOffsetEnable](Gameplay.CharacterBase.md#basicstanceaimoffsetenable)**(): `boolean` <br> 是否基础姿态的开启瞄准偏移|
| **[brakingDecelerationFalling](Gameplay.CharacterBase.md#brakingdecelerationfalling)**(): `number` <br> 下落制动速率|
| **[brakingDecelerationFlying](Gameplay.CharacterBase.md#brakingdecelerationflying)**(): `number` <br> 飞行制动速率|
| **[brakingDecelerationSwimming](Gameplay.CharacterBase.md#brakingdecelerationswimming)**(): `number` <br> 游泳制动速率|
| **[brakingDecelerationWalking](Gameplay.CharacterBase.md#brakingdecelerationwalking)**(): `number` <br> 行走制动速率|
| **[canSetAppearanceData](Gameplay.CharacterBase.md#cansetappearancedata)**(): `boolean` <br> 是否可以设置角色形象数据|
| **[canStepUpOn](Gameplay.CharacterBase.md#canstepupon)**(): `boolean` <br> 获取组件是否可以被玩家站立|
| **[capsuleHalfHeight](Gameplay.CharacterBase.md#capsulehalfheight)**(): `number` <br> 胶囊体半高|
| **[capsuleRadius](Gameplay.CharacterBase.md#capsuleradius)**(): `number` <br> 胶囊体半径|
| **[characterName](Gameplay.CharacterBase.md#charactername)**(): `string` <br> 角色名称|
| **[collisionEnable](Gameplay.CharacterBase.md#collisionenable)**(): `boolean` <br> 是否开启碰撞|
| **[collisionExtent](Gameplay.CharacterBase.md#collisionextent)**(): [`Vector`](Type.Vector.md) <br> 碰撞形状的大小|
| **[collisionShape](Gameplay.CharacterBase.md#collisionshape)**(): [`CustomShapeType`](../enums/Gameplay.CustomShapeType.md) <br> 碰撞形状|
| **[collisionWithOtherCharacterEnable](Gameplay.CharacterBase.md#collisionwithothercharacterenable)**(): `boolean` <br> 能否与其他角色发生碰撞|
| **[crouchEnable](Gameplay.CharacterBase.md#crouchenable)**(): `boolean` <br> 启用/禁用下蹲能力|
| **[crouchedHeight](Gameplay.CharacterBase.md#crouchedheight)**(): `number` <br> 下蹲时胶囊体的高度|
| **[forceUpdateMovement](Gameplay.CharacterBase.md#forceupdatemovement)**(`value`: `boolean`): `void` <br> 启用/禁用强制更新移动|
| **[gravityScale](Gameplay.CharacterBase.md#gravityscale)**(): `number` <br> 重力倍率|
| **[groundFriction](Gameplay.CharacterBase.md#groundfriction)**(): `number` <br> 地面摩檫力|
| **[headUIVisible](Gameplay.CharacterBase.md#headuivisible)**(): `boolean` <br> 头顶UI是否可见|
| **[headUIVisibleRange](Gameplay.CharacterBase.md#headuivisiblerange)**(): `number` <br> 头顶UI可见距离|
| **[isCrouching](Gameplay.CharacterBase.md#iscrouching)**(): `boolean` <br> 是否处于下蹲状态|
| **[isJumping](Gameplay.CharacterBase.md#isjumping)**(): `boolean` <br> 是否正在跳跃|
| **[isMoving](Gameplay.CharacterBase.md#ismoving)**(): `boolean` <br> 是否正在移动|
| **[jumpEnable](Gameplay.CharacterBase.md#jumpenable)**(): `boolean` <br> 启用/禁用跳跃能力|
| **[jumpMaxCount](Gameplay.CharacterBase.md#jumpmaxcount)**(): `number` <br> 最大可跳跃次数|
| **[jumpingOutOfWaterEnable](Gameplay.CharacterBase.md#jumpingoutofwaterenable)**(): `boolean` <br> 是否可以跳出水面|
| **[maxAcceleration](Gameplay.CharacterBase.md#maxacceleration)**(): `number` <br> 最大加速度|
| **[maxFallingSpeed](Gameplay.CharacterBase.md#maxfallingspeed)**(): `number` <br> 最大下落速度|
| **[maxFlySpeed](Gameplay.CharacterBase.md#maxflyspeed)**(): `number` <br> 最大飞行速度|
| **[maxJumpHeight](Gameplay.CharacterBase.md#maxjumpheight)**(): `number` <br> 最大跳跃高度|
| **[maxStepHeight](Gameplay.CharacterBase.md#maxstepheight)**(): `number` <br> 获取角色最大可跨越高度|
| **[maxSwimSpeed](Gameplay.CharacterBase.md#maxswimspeed)**(): `number` <br> 最大游泳速度|
| **[maxWalkSpeed](Gameplay.CharacterBase.md#maxwalkspeed)**(): `number` <br> 地面最大速度|
| **[maxWalkSpeedCrouched](Gameplay.CharacterBase.md#maxwalkspeedcrouched)**(): `number` <br> 地面蹲伏行走时的最大移动速度|
| **[meshOffset](Gameplay.CharacterBase.md#meshoffset)**(): [`Vector`](Type.Vector.md) <br> 获取mesh相对角色坐标点的偏移|
| **[moveEnable](Gameplay.CharacterBase.md#moveenable)**(): `boolean` <br> 启用/禁用移动能力|
| **[moveFacingDirection](Gameplay.CharacterBase.md#movefacingdirection)**(): [`MoveFacingDirection`](../enums/Gameplay.MoveFacingDirection.md) <br> 运动面朝方向|
| **[movementAxisDirection](Gameplay.CharacterBase.md#movementaxisdirection)**(): [`Vector`](Type.Vector.md) <br> 运动时依据的轴方向, 只有当前的MovementDirection为AxisDirection时有效|
| **[movementDirection](Gameplay.CharacterBase.md#movementdirection)**(): [`MovementDirection`](../enums/Gameplay.MovementDirection.md) <br> 运动时依据的正方向|
| **[movementState](Gameplay.CharacterBase.md#movementstate)**(): [`MovementMode`](../enums/Gameplay.MovementMode.md) <br> 当前角色运动状态|
| **[outOfWaterZ](Gameplay.CharacterBase.md#outofwaterz)**(): `number` <br> 出水时Z轴方向上的速度|
| **[physicsEnabled](Gameplay.CharacterBase.md#physicsenabled)**(): `boolean` <br> 获取角色物理状态|
| **[ragdollEnable](Gameplay.CharacterBase.md#ragdollenable)**(): `boolean` <br> 启用/禁用布娃娃状态|
| **[rotateRate](Gameplay.CharacterBase.md#rotaterate)**(): `number` <br> 最大转向速度|
| **[separateBrakingFrictionEnable](Gameplay.CharacterBase.md#separatebrakingfrictionenable)**(): `boolean` <br> 使用单独制动摩擦|
| **[usedCapsuleCorrection](Gameplay.CharacterBase.md#usedcapsulecorrection)**(): `boolean` <br> 使用胶囊体修正 true代表应用角色编辑中的数据自动计算胶囊体大小。false代表应用"capsuleHalfHeight"和"capsuleRadius"设置胶囊体的大小。|
| **[velocity](Gameplay.CharacterBase.md#velocity)**(): [`Vector`](Type.Vector.md) <br> 当前移动速度|
| **[walkableFloorAngle](Gameplay.CharacterBase.md#walkablefloorangle)**(): `number` <br> 可行走的最大角度|


::: details 点击查看继承
| Accessors |
| :-----|
| **[forwardVector](Gameplay.GameObject.md#forwardvector)**(): [`Vector`](Type.Vector.md) <br> 获取当前物体的向前向量|
| **[guid](Gameplay.GameObject.md#guid)**(): `string` <br> 获取对象的GUID（唯一标识一个对象的字符串）。|
| **[lockStatus](Gameplay.GameObject.md#lockstatus)**(): `boolean` <br> 获取对象是否锁定|
| **[name](Gameplay.GameObject.md#name)**(): `string` <br> 返回当前物体名称|
| **[netStatus](Gameplay.GameObject.md#netstatus)**(): [`NetStatus`](../enums/Type.NetStatus.md) <br> 获取当前物体同步状态|
| **[parent](Gameplay.GameObject.md#parent)**(): `GameObject` <br> 获取当前父物体|
| **[relativeLocation](Gameplay.GameObject.md#relativelocation)**(): [`Vector`](Type.Vector.md) <br> 获取相对位置|
| **[relativeRotation](Gameplay.GameObject.md#relativerotation)**(): [`Rotation`](Type.Rotation.md) <br> 获取相对旋转|
| **[relativeScale](Gameplay.GameObject.md#relativescale)**(): [`Vector`](Type.Vector.md) <br> 获取相对缩放|
| **[rightVector](Gameplay.GameObject.md#rightvector)**(): [`Vector`](Type.Vector.md) <br> 获取当前物体的向右向量|
| **[staticStatus](Gameplay.GameObject.md#staticstatus)**(): `boolean` <br> 获取对象是否静态|
| **[tag](Gameplay.GameObject.md#tag)**(): `string` <br> 获取当前物体的Tag|
| **[transform](Gameplay.GameObject.md#transform)**(): [`Transform`](Type.Transform.md) <br> 返回当前物体transform|
| **[upVector](Gameplay.GameObject.md#upvector)**(): [`Vector`](Type.Vector.md) <br> 获取当前物体的向上向量|
| **[useUpdate](Gameplay.GameObject.md#useupdate)**(): `boolean` <br> 获取对象是否使用更新|
| **[worldLocation](Gameplay.GameObject.md#worldlocation)**(): [`Vector`](Type.Vector.md) <br> 获取物体的世界坐标|
| **[worldRotation](Gameplay.GameObject.md#worldrotation)**(): [`Rotation`](Type.Rotation.md) <br> 获取物体的世界旋转|
| **[worldScale](Gameplay.GameObject.md#worldscale)**(): [`Vector`](Type.Vector.md) <br> 获取物体的世界缩放|
:::


| Methods |
| :-----|
| **[addImpulse](Gameplay.CharacterBase.md#addimpulse)**(`Vector`: [`Vector`](Type.Vector.md), `ignoreMass?`: `boolean`): `void` <br> 添加冲量|
| **[addMoveInput](Gameplay.CharacterBase.md#addmoveinput)**(`direction`: [`Vector`](Type.Vector.md)): `void` <br> 沿着给定的方向向量添加移动输入|
| **[appearanceReady](Gameplay.CharacterBase.md#appearanceready)**(): `Promise`<`void`\> <br> 在外观数据准备好后返回并执行已绑定的函数，保证当前角色换装表现和数据是正确的。在设置角色外观形象之前，可以用做这个判断|
| **[attach](Gameplay.CharacterBase.md#attach)**(`gameObject`: `GameObject`, `slotName`: [`SlotType`](../enums/Gameplay.SlotType.md)): `void` <br> 将物体附着到人物角色的指定插槽|
| **[clearAppearance](Gameplay.CharacterBase.md#clearappearance)**(): `void` <br> 清空角色形象数据|
| **[clearDecorations](Gameplay.CharacterBase.md#cleardecorations)**(): `void` <br> 清空所有挂件数据|
| **[clearOneDecoration](Gameplay.CharacterBase.md#clearonedecoration)**(`GUID`: `string`): `void` <br> 删除一个挂件|
| **[crouch](Gameplay.CharacterBase.md#crouch)**(`isCrouch`: `boolean`): `void` <br> 下蹲|
| **[getAppearance](Gameplay.CharacterBase.md#getappearance)**<`T`: extends [`HumanoidV1`](Gameplay.HumanoidV1.md) \\>(): `T`: extends [`HumanoidV1`](Gameplay.HumanoidV1.md) \ <br> 设置外观修改功能|
| **[getControlRotator](Gameplay.CharacterBase.md#getcontrolrotator)**(`Out?`: [`Rotation`](Type.Rotation.md)): [`Rotation`](Type.Rotation.md) <br> 获取控制器的旋转|
| **[getDecorations](Gameplay.CharacterBase.md#getdecorations)**(): [`DecorationTuple`](../modules/Gameplay.Gameplay.md#decorationtuple)[] <br> 获取当前挂件实例化对象的GUID|
| **[getHeadUIWidget](Gameplay.CharacterBase.md#getheaduiwidget)**(): [`UIWidget`](Gameplay.UIWidget.md) <br> 获取头顶UIWidget|
| **[getSlotName](Gameplay.CharacterBase.md#getslotname)**(`slotType`: [`SlotType`](../enums/Gameplay.SlotType.md)): `string` <br> 获取对应插槽名称|
| **[isPlayingAnimation](Gameplay.CharacterBase.md#isplayinganimation)**(): `boolean` <br> 是否正在播放动画|
| **[jump](Gameplay.CharacterBase.md#jump)**(): `void` <br> 跳跃|
| **[loadAnimation](Gameplay.CharacterBase.md#loadanimation)**(`GUID`: `string`, `sync?`: `boolean`): [`Animation`](Gameplay.Animation.md) <br> 加载动画,获取到动画对象，playAnimation是个快速实现功能的接口,可配置参数有限。loadAnimation可以返回动画,以进行更加精细的动画控制，获取到对象后需用户自己配置参数，手动调用play接口动画才会播放。|
| **[loadDecoration](Gameplay.CharacterBase.md#loaddecoration)**(`decorationString`: `string`, `callback`: [`StringCallback`](../modules/Gameplay.Gameplay.md#stringcallback)): `void` <br> 加载挂件,给移动角色编辑器提供的能力|
| **[loadStance](Gameplay.CharacterBase.md#loadstance)**(`GUID`: `string`, `sync?`: `boolean`): [`SubStance`](Gameplay.SubStance.md) <br> 创建一个二级姿态对象并返回|
| **[lookAt](Gameplay.CharacterBase.md#lookat)**(`TargetPoint`: [`Vector`](Type.Vector.md)): `void` <br> 角色面朝目标点|
| **[playAnimation](Gameplay.CharacterBase.md#playanimation)**(`GUID`: `string`, `loopCount?`: `number`, `rate?`: `number`): [`Animation`](Gameplay.Animation.md) <br> 播放动画,同时获取到动画对象,Animation对象接口默认是同步的，playanimation是个快速实现功能的接口,可配置参数有限，loadanimation 可以返回动画,以进行更加精细的动画控制。|
| **[setAppearance](Gameplay.CharacterBase.md#setappearance)**<`T`: extends [`SomatotypeBase`](Gameplay.SomatotypeBase.md)<`T`\>\>(`clz`: [`Constructor`](../modules/Gameplay.Gameplay.md#constructor)<`T`\>): `T`: extends [`SomatotypeBase`](Gameplay.SomatotypeBase.md)<`T`\> <br> 设置外观修改功能|
| **[setCollisionShapeAndExtent](Gameplay.CharacterBase.md#setcollisionshapeandextent)**(`ShapeType`: [`CustomShapeType`](../enums/Gameplay.CustomShapeType.md), `CollisionExtent`: [`Vector`](Type.Vector.md)): `void` <br> 设置不同形状不同大小的碰撞体|
| **[setLocallyVisibility](Gameplay.CharacterBase.md#setlocallyvisibility)**(`status`: [`PropertyStatus`](../enums/Type.PropertyStatus.md), `propagateToChildren?`: `boolean`): `void` <br> 设置是否被显示(本地生效)|
| **[stopStance](Gameplay.CharacterBase.md#stopstance)**(`sync?`: `boolean`): `void` <br> 停止任何正在播放的姿态|
| **[swimmingDown](Gameplay.CharacterBase.md#swimmingdown)**(`speed`: `number`): `void` <br> 水中下潜|
| **[swimmingUp](Gameplay.CharacterBase.md#swimmingup)**(`speed`: `number`): `void` <br> 水中上浮|
| **[switchToFlying](Gameplay.CharacterBase.md#switchtoflying)**(): `void` <br> 切换为飞行状态|
| **[switchToSwimming](Gameplay.CharacterBase.md#switchtoswimming)**(): `void` <br> 切换为游泳状态|
| **[switchToWalking](Gameplay.CharacterBase.md#switchtowalking)**(): `void` <br> 切换为行走状态|


::: details 点击查看继承
| Methods |
| :-----|
| **[addDestroyCallback](Gameplay.GameObject.md#adddestroycallback)**(`callback`: (...`arg`: `unknown`[]) => `void`): `void` <br> 添加物体Destroy事件回调|
| **[asyncGetScriptByName](Gameplay.GameObject.md#asyncgetscriptbyname)**(`name`: `string`): `Promise`<`Script`\> <br> 异步获得当前物体下的指定脚本 客户端不维系父子关系|
| **[attachComponent](Gameplay.GameObject.md#attachcomponent)**(`component`: `Component`, `isStatic?`: `boolean`): `boolean` <br> 附加组件|
| **[attachToGameObject](Gameplay.GameObject.md#attachtogameobject)**(`obj`: `GameObject`): `void` <br> 将物体附着到指定物体上|
| **[clone](Gameplay.GameObject.md#clone)**(`spawnInfo?`: `boolean` \): `GameObject` <br> 复制对象|
| **[deleteDestroyCallback](Gameplay.GameObject.md#deletedestroycallback)**(`callback`: (...`arg`: `unknown`[]) => `void`): `void` <br> 移除物体Destroy事件回调|
| **[destroy](Gameplay.GameObject.md#destroy)**(): `void` <br> 删除对象|
| **[detachComponent](Gameplay.GameObject.md#detachcomponent)**(`component`: `string` \): `void` <br> 移除组件|
| **[detachFromGameObject](Gameplay.GameObject.md#detachfromgameobject)**(): `void` <br> 将此物体与当前附着的物体分离|
| **[getBoundingBoxSize](Gameplay.GameObject.md#getboundingboxsize)**(`nonColliding?`: `boolean`, `includeFromChildActors?`: `boolean`, `outer?`: [`Vector`](Type.Vector.md)): [`Vector`](Type.Vector.md) <br> 获取物体包围盒大小|
| **[getBounds](Gameplay.GameObject.md#getbounds)**(`onlyCollidingComponents`: `boolean`, `OriginOuter`: [`Vector`](Type.Vector.md), `BoxExtentOuter`: [`Vector`](Type.Vector.md), `includeFromChildActors?`: `boolean`): `void` <br> 获取GameObject边界|
| **[getChildByGuid](Gameplay.GameObject.md#getchildbyguid)**(`GUID`: `string`): `undefined` \| `GameObject` <br> 根据GUID查找子物体|
| **[getChildByName](Gameplay.GameObject.md#getchildbyname)**(`name`: `string`): `undefined` \| `GameObject` <br> 根据名称查找子物体|
| **[getChildren](Gameplay.GameObject.md#getchildren)**(): `undefined` \| `GameObject`[] <br> 获取Children，客户端不维系父子关系。推荐使用Find替代|
| **[getChildrenBoxCenter](Gameplay.GameObject.md#getchildrenboxcenter)**(`outer?`: [`Vector`](Type.Vector.md)): [`Vector`](Type.Vector.md) <br> 获取所有子对象包围盒中心点(不包含父对象,父对象不可用返回[0,0,0])|
| **[getForwardVector](Gameplay.GameObject.md#getforwardvector)**(`outer?`: [`Vector`](Type.Vector.md)): [`Vector`](Type.Vector.md) <br> 获取当前物体的向前向量|
| **[getRelativeLocation](Gameplay.GameObject.md#getrelativelocation)**(`outer?`: [`Vector`](Type.Vector.md)): [`Vector`](Type.Vector.md) <br> 获取相对位置|
| **[getRelativeRotation](Gameplay.GameObject.md#getrelativerotation)**(`outer?`: [`Rotation`](Type.Rotation.md)): [`Rotation`](Type.Rotation.md) <br> 获取相对旋转|
| **[getRelativeScale](Gameplay.GameObject.md#getrelativescale)**(`outer?`: [`Vector`](Type.Vector.md)): [`Vector`](Type.Vector.md) <br> 获取相对缩放|
| **[getRightVector](Gameplay.GameObject.md#getrightvector)**(`outer?`: [`Vector`](Type.Vector.md)): [`Vector`](Type.Vector.md) <br> 获取当前物体的向右向量|
| **[getScriptByGuid](Gameplay.GameObject.md#getscriptbyguid)**(`GUID`: `string`): `undefined` \| `Script` <br> 获得当前物体下的指定脚本|
| **[getScriptByName](Gameplay.GameObject.md#getscriptbyname)**(`name`: `string`): `undefined` \| `Script` <br> 获得当前物体下的指定脚本|
| **[getScripts](Gameplay.GameObject.md#getscripts)**(): `undefined` \| `Script`[] <br> 获得当前物体下的所有脚本|
| **[getSourceAssetGuid](Gameplay.GameObject.md#getsourceassetguid)**(): `string` <br> 获取当前物体使用资源的GUID|
| **[getTransform](Gameplay.GameObject.md#gettransform)**(`outer?`: [`Transform`](Type.Transform.md)): [`Transform`](Type.Transform.md) <br> 返回当前物体Transform|
| **[getUpVector](Gameplay.GameObject.md#getupvector)**(`outer?`: [`Vector`](Type.Vector.md)): [`Vector`](Type.Vector.md) <br> 获取当前物体的向上向量|
| **[getVisibility](Gameplay.GameObject.md#getvisibility)**(): `boolean` <br> 获取GameObject是否被显示|
| **[getWorldLocation](Gameplay.GameObject.md#getworldlocation)**(`outer?`: [`Vector`](Type.Vector.md)): [`Vector`](Type.Vector.md) <br> 获取物体的世界坐标|
| **[getWorldRotation](Gameplay.GameObject.md#getworldrotation)**(`outer?`: [`Rotation`](Type.Rotation.md)): [`Rotation`](Type.Rotation.md) <br> 获取物体的世界旋转|
| **[getWorldScale](Gameplay.GameObject.md#getworldscale)**(`outer?`: [`Vector`](Type.Vector.md)): [`Vector`](Type.Vector.md) <br> 获取物体的世界缩放|
| **[isRunningClient](Gameplay.GameObject.md#isrunningclient)**(): `boolean` <br> 是否为客户端|
| **[onDestroy](Gameplay.GameObject.md#ondestroy)**(): `void` <br> 周期函数 被销毁时调用|
| **[onReplicated](Gameplay.GameObject.md#onreplicated)**(`path`: `string`, `value`: `unknown`, `oldVal`: `unknown`): `void` <br> 属性被同步事件 ClientOnly|
| **[onStart](Gameplay.GameObject.md#onstart)**(): `void` <br> 周期函数 脚本开始执行时调用|
| **[onUpdate](Gameplay.GameObject.md#onupdate)**(`dt`: `number`): `void` <br> 周期函数 useUpdate 设置为 true 后,每帧被执行,设置为false,不会执行|
| **[ready](Gameplay.GameObject.md#ready)**(): `Promise`<[`GameObject`](Gameplay.GameObject.md)\> <br> GameObject准备好后返回|
| **[setLocationAndRotation](Gameplay.GameObject.md#setlocationandrotation)**(`location`: [`Vector`](Type.Vector.md), `rotation`: [`Rotation`](Type.Rotation.md)): `void` <br> 同时设置物体的世界位置与旋转|
| **[setRelativeLocation](Gameplay.GameObject.md#setrelativelocation)**(`location`: [`Vector`](Type.Vector.md)): `void` <br> 设置相对位置|
| **[setRelativeRotation](Gameplay.GameObject.md#setrelativerotation)**(`rotation`: [`Rotation`](Type.Rotation.md)): `void` <br> 设置相对旋转|
| **[setRelativeScale](Gameplay.GameObject.md#setrelativescale)**(`scale`: [`Vector`](Type.Vector.md)): `void` <br> 设置相对缩放|
| **[setTransform](Gameplay.GameObject.md#settransform)**(`transform`: [`Transform`](Type.Transform.md)): `void` <br> 设置当前物体transform|
| **[setVisibility](Gameplay.GameObject.md#setvisibility)**(`status`: [`PropertyStatus`](../enums/Type.PropertyStatus.md), `propagateToChildren?`: `boolean`): `void` <br> 设置GameObject是否被显示|
| **[setWorldLocation](Gameplay.GameObject.md#setworldlocation)**(`v`: [`Vector`](Type.Vector.md)): `void` <br> 设置物体的世界坐标|
| **[setWorldRotation](Gameplay.GameObject.md#setworldrotation)**(`rotation`: [`Rotation`](Type.Rotation.md)): `void` <br> 设置物体的世界旋转|
| **[setWorldScale](Gameplay.GameObject.md#setworldscale)**(`v`: [`Vector`](Type.Vector.md)): `void` <br> 设置物体的世界缩放|
| **[asyncFind](Gameplay.GameObject.md#asyncfind)**(`GUID`: `string`): `Promise`<`GameObject`\> <br> 通过GUID异步查找GameObject,默认是五秒,可以通过 `core.setGlobalAsyncOverTime(5000);|
| **[asyncSpawn](Gameplay.GameObject.md#asyncspawn)**<`T`: extends `GameObject`<`T`\>\>(`spawnInfo`: [`SpawnInfo`](../interfaces/Type.SpawnInfo.md)): `Promise`<`T`: extends `GameObject`<`T`\>\> <br> 异步构造一个 GameObject 资源不存在会先去下载资源再去创建|
| **[find](Gameplay.GameObject.md#find)**(`GUID`: `string`): `GameObject` <br> 通过GUID查找GameObject|
| **[findGameObjectByTag](Gameplay.GameObject.md#findgameobjectbytag)**(`InTag`: `string`): `GameObject`[] <br> 通过自定义Tag获取GameObject|
| **[getGameObjectByName](Gameplay.GameObject.md#getgameobjectbyname)**(`name`: `string`): `undefined` \| `GameObject` <br> 通过名字查找物体|
| **[getGameObjectsByName](Gameplay.GameObject.md#getgameobjectsbyname)**(`name`: `string`): `GameObject`[] <br> 通过名字查找物体|
| **[spawn](Gameplay.GameObject.md#spawn)**<`T`: extends `GameObject`<`T`\>\>(`[spawn](Gameplay.GameObject.md#spawn)Info`): `T`: extends `GameObject`<`T`\> <br> 构造一个 GameObject|
:::


### onLoadAppearanceDataAllCompleted <Score text="onLoadAppearanceDataAllCompleted" /> 

• **onLoadAppearanceDataAllCompleted**: [`MulticastDelegate`](Type.MulticastDelegate.md)<[`LoadAppearanceDataAllCompletedCallback`](../modules/Gameplay.Gameplay.md#loadappearancedataallcompletedcallback)\>

加载完角色形象数据后的回调

___

### onLoadDecorationsAllCompleted <Score text="onLoadDecorationsAllCompleted" /> 

• **onLoadDecorationsAllCompleted**: [`MulticastDelegate`](Type.MulticastDelegate.md)<[`LoadDecorationsAllCompletedCallback`](../modules/Gameplay.Gameplay.md#loaddecorationsallcompletedcallback)\>

加载完角色形象数据后的回调

___

### onMeshChanged <Score text="onMeshChanged" /> 

• **onMeshChanged**: [`MulticastDelegate`](Type.MulticastDelegate.md)<[`onAppearanceDataChanged`](../modules/Gameplay.Gameplay.md#onappearancedatachanged)\>

角色模型切换成功广播

___

### onMovementStateChanged <Score text="onMovementStateChanged" /> 

• **onMovementStateChanged**: [`OnMovementStateChanged`](../modules/Gameplay.Gameplay.md#onmovementstatechanged)

移动状态切换时的回调

___

### onSetAppearanceDataCompleted <Score text="onSetAppearanceDataCompleted" /> 

• **onSetAppearanceDataCompleted**: [`MulticastDelegate`](Type.MulticastDelegate.md)<[`SetAppearanceDataCallback`](../modules/Gameplay.Gameplay.md#setappearancedatacallback)\>

设置一个角色编辑API成功后的回调

___

### onTextureChanged <Score text="onTextureChanged" /> 

• **onTextureChanged**: [`MulticastDelegate`](Type.MulticastDelegate.md)<[`onAppearanceDataChanged`](../modules/Gameplay.Gameplay.md#onappearancedatachanged)\>

角色贴图切换成功广播

___

### player <Score text="player" /> 

• **player**: [`Player`](Gameplay.Player.md)

玩家对象

## Accessors

### airControl <Score text="airControl" /> 

• `get` **airControl**(): `number`

角色在空中时, 控制水平方向移动的灵活度

::: warning Precautions

范围:0~1, 0表示不能控制, 1表示能按地面最大移动速率完全控制

:::

#### Returns

`number`

• `set` **airControl**(`InAirControl`): `void`

角色在空中时, 控制水平方向移动的灵活度

::: warning Precautions

范围:0~1, 0表示不能控制, 1表示能按地面最大移动速率完全控制

:::

#### Parameters

| Name | Type |
| :------ | :------ |
| `InAirControl` | `number` |


___

### airControlBoostMultiplier <Score text="airControlBoostMultiplier" /> 

• `get` **airControlBoostMultiplier**(): `number`

当角色空中水平移动速率比airControlBoostVelocityThreshold小时, 对airControl效果加倍的倍数

::: warning Precautions

范围:大于等于0的数字, 取0时, 不会对airControl效果加倍, 无论取值多大, airControl最大值都被限制为1

:::

#### Returns

`number`

• `set` **airControlBoostMultiplier**(`InAirControlBoostMultiplier`): `void`

当角色空中水平移动速率比airControlBoostVelocityThreshold小时, 对airControl效果加倍的倍数

::: warning Precautions

范围:大于等于0的数字, 取0时, 不会对airControl效果加倍, 无论取值多大, airControl最大值都被限制为1

:::

#### Parameters

| Name | Type |
| :------ | :------ |
| `InAirControlBoostMultiplier` | `number` |


___

### airControlBoostVelocityThreshold <Score text="airControlBoostVelocityThreshold" /> 

• `get` **airControlBoostVelocityThreshold**(): `number`

下落控制提升速率阈值, 当角色在空中时水平移动速率小于此值, 就会依照airControlBoostMultiplier的值对airControl效果进行加倍

::: warning Precautions

范围: 大于等于0

:::

#### Returns

`number`

• `set` **airControlBoostVelocityThreshold**(`InAirControlBoostVelocityThreshold`): `void`

下落控制提升速率阈值, 当角色在空中时水平移动速率小于此值, 就会依照airControlBoostMultiplier的值对airControl效果进行加倍

::: warning Precautions

范围: 大于等于0

:::

#### Parameters

| Name | Type |
| :------ | :------ |
| `InAirControlBoostVelocityThreshold` | `number` |


___

### animationMode <Score text="animationMode" /> 

• `get` **animationMode**(): [`AnimationMode`](../enums/Gameplay.AnimationMode.md)

动画播放模式

#### Returns

[`AnimationMode`](../enums/Gameplay.AnimationMode.md)

• `set` **animationMode**(`mode`): `void`

动画播放模式

::: warning Precautions

Auto 提供基础姿态，表现为边走边播动画，Custom自定义模式，不提供姿态,默认下没有任何动作，需要自行编写状态控制动画播放。

:::

使用示例: 应用
```ts
// Auto
 Gameplay.asyncGetCurrentPlayer().then((player) => {
  let Anim = player.character.playAnimation(animGUID);
  Anim = player.character.loadAnimation(animGUID);
});

//Custom 动画状态机
export class EasyAnimState{

 public stateTag:string;

 private anim:Gameplay.Animation;

 public stateCheckCallback:(anim:Gameplay.Animation,stateTag:string)=>string;

 constructor(tag:string,anim:Gameplay.Animation,stateChange:(anim:Gameplay.Animation,stateTag:string)=>string) {
    this.stateTag = tag;
    this.anim = anim;
    this.stateCheckCallback = stateChange;
 }

 public enter(){
   this.anim.play();
 }

 public exit(){
  this.anim.stop();
 }

 public check():string{
   return this.stateCheckCallback(this.anim,this.stateTag);
 }
}

export class EasyAnimStateMachine{
private statesMap:Map<string,EasyAnimState>;

private currentState:EasyAnimState;

public startTag:string;

private timerId:number = undefined;

private updateRate:number;

public load(states:EasyAnimState[],startTag:string,updateRate = 33){
 if(this.timerId != undefined){
      console.warn("State Machine is Running");
      this.stop();
 }

 this.statesMap = new Map<string,EasyAnimState>();
 this.startTag = startTag;
 this.updateRate = updateRate;
 states.forEach((state)=>{
     this.statesMap.set(state.stateTag ,state);
 });

 this.timerId = undefined;
}

public start(){
  if(this.timerId != undefined){
      console.warn("State Machine is Running");
  }
  if(this.statesMap){
      if(this.statesMap.has(this.startTag)){
         this.currentState = this.statesMap.get(this.startTag);
         this.currentState.enter();
          this.timerId = setInterval(()=>{
             this.update();
         },this.updateRate);
     }else{
         console.log("error start tag " + this.startTag);
     }
 }
}

private update(){
 if(this.currentState && this.currentState.check){
     let nextState =  this.currentState.check();
     if(this.statesMap.has(nextState)){
         this.currentState.exit();
         this.currentState = this.statesMap.get(nextState);
         this.currentState.enter();
         console.log("change State: " + nextState);
     }
 }
}

public stop(){
   if(this.timerId == undefined){
      return;
  }

  clearInterval(this.timerId);
  this.currentState.exit();
  this.currentState = undefined;
  console.log("stop State Machine");
 }
}

@Core.Class
export default class Test extends Core.Script {
    stateMachine:EasyAnimStateMachine
    character:Gameplay.CharacterBase
    pressT = false;
    protected onStart(): void {
        if(Util.SystemUtil.isClient()) {
            Gameplay.asyncGetCurrentPlayer().then((player)=>{
                InputUtil.onKeyDown(Type.Keys.T,()=>{
                    this.pressT = true;
                });

                this.pressT = false;
                this.character = player.character;
                this.character.animationMode = Gameplay.AnimationMode.Custom;
                setTimeout(() => {
                    const animIdle = this.character.loadAnimation("47769");
                    animIdle.loop = 0
                    const stateIdle = new EasyAnimState("Idle",animIdle,
                    (anim:Gameplay.Animation,stateTag:string)=>{
                        if(this.pressT){
                            this.pressT = false;
                            return "Hello";
                        }

                        if(this.character.velocity.length > 0.1 && (this.character.velocity.x!=0 || this.character.velocity.y!=0)){
                            return "Walk";
                        }
                        return "";
                    });

                    const animAWalk = this.character.loadAnimation("33567");
                    animAWalk.loop = 0;
                    const stateWalk = new EasyAnimState("Walk",animAWalk,
                    (anim:Gameplay.Animation,stateTag:string)=>{
                        if(this.pressT){
                            this.pressT = false;
                            return "Hello";
                        }

                        if(this.character.velocity.length < 0.1){
                            return "Idle";
                        }
                        return "";
                    });

                    const animHello = this.character.loadAnimation("29755");
                    const stateHello = new EasyAnimState("Hello",animHello,
                     (anim:Gameplay.Animation,stateTag:string)=>{

                        if(this.pressT){
                            this.pressT = false;
                            anim.play();
                            return "";
                        }

                        if(this.character.velocity.length > 0.1 &&  (this.character.velocity.x!=0 || this.character.velocity.y!=0)){
                            return "Walk";
                        }

                        if(anim.isPlaying == false){
                            if( this.character.velocity.length < 0.1){
                                return "Idle";
                            }else{
                                return "Walk";
                            }
                        }
                        return "";
                    });

                    this.stateMachine = new EasyAnimStateMachine();
                    this.stateMachine.load([stateIdle,stateWalk,stateHello],"Idle");
                    Events.addLocalListener("start",()=>{
                        this.pressT = false;
                        this.stateMachine.start();
                    })
                    Events.addLocalListener("stop",()=>{
                        this.stateMachine.stop();
                    })
                }, 500);
            })
        }
    }
}
```

#### Parameters

| Name | Type |
| :------ | :------ |
| `mode` | [`AnimationMode`](../enums/Gameplay.AnimationMode.md) |


___

### appearanceType <Score text="appearanceType" /> 

• `get` **appearanceType**(): [`AppearanceType`](../enums/Gameplay.AppearanceType.md)

形象类型

::: warning Precautions

自动同步

:::

#### Returns

[`AppearanceType`](../enums/Gameplay.AppearanceType.md)

• `set` **appearanceType**(`type`): `void`

形象类型

#### Parameters

| Name | Type |
| :------ | :------ |
| `type` | [`AppearanceType`](../enums/Gameplay.AppearanceType.md) |


___

### baseShadowLocationOffset <Score text="baseShadowLocationOffset" /> 

• `get` **baseShadowLocationOffset**(): [`Vector2`](Type.Vector2.md)

模拟阴影相对于角色脚底中心的位置偏移

#### Returns

[`Vector2`](Type.Vector2.md)

• `set` **baseShadowLocationOffset**(`InLocationOffset`): `void`

模拟阴影相对于角色脚底中心的位置偏移

#### Parameters

| Name | Type |
| :------ | :------ |
| `InLocationOffset` | [`Vector2`](Type.Vector2.md) |


___

### baseShadowMaxVisibleHeight <Score text="baseShadowMaxVisibleHeight" /> 

• `get` **baseShadowMaxVisibleHeight**(): `number`

模拟阴影可见的最大离地高度

#### Returns

`number`

• `set` **baseShadowMaxVisibleHeight**(`InHeight`): `void`

模拟阴影可见的最大离地高度

#### Parameters

| Name | Type |
| :------ | :------ |
| `InHeight` | `number` |


___

### baseShadowScale <Score text="baseShadowScale" /> 

• `get` **baseShadowScale**(): [`Vector2`](Type.Vector2.md)

模拟阴影的缩放

#### Returns

[`Vector2`](Type.Vector2.md)

• `set` **baseShadowScale**(`InScale`): `void`

模拟阴影的缩放

#### Parameters

| Name | Type |
| :------ | :------ |
| `InScale` | [`Vector2`](Type.Vector2.md) |


___

### basicStance <Score text="basicStance" /> 

• `get` **basicStance**(): `string`

基础姿态

::: warning Precautions

基础姿态是一个预制的基本动画状态机, 包含行走, 跳跃, 飞行等基本动画, 传入基础姿态资源的GUID进行基础姿态的切换

:::

#### Returns

`string`

• `set` **basicStance**(`InBasicStance`): `void`

基础姿态

::: warning Precautions

基础姿态是一个预制的基本动画状态机, 包含行走, 跳跃, 飞行等基本动画, 传入基础姿态资源的GUID进行基础姿态的切换

:::

#### Parameters

| Name | Type |
| :------ | :------ |
| `InBasicStance` | `string` |


___

### basicStanceAimOffsetEnable <Score text="basicStanceAimOffsetEnable" /> 

• `get` **basicStanceAimOffsetEnable**(): `boolean`

是否基础姿态的开启瞄准偏移

#### Returns

`boolean`

• `set` **basicStanceAimOffsetEnable**(`InbEnableAimOffset`): `void`

是否基础姿态的开启瞄准偏移

#### Parameters

| Name | Type |
| :------ | :------ |
| `InbEnableAimOffset` | `boolean` |


___

### brakingDecelerationFalling <Score text="brakingDecelerationFalling" /> 

• `get` **brakingDecelerationFalling**(): `number`

下落制动速率

#### Returns

`number`

• `set` **brakingDecelerationFalling**(`InBrakingDecelerationFalling`): `void`

下落制动速率

#### Parameters

| Name | Type |
| :------ | :------ |
| `InBrakingDecelerationFalling` | `number` |


___

### brakingDecelerationFlying <Score text="brakingDecelerationFlying" /> 

• `get` **brakingDecelerationFlying**(): `number`

飞行制动速率

#### Returns

`number`

• `set` **brakingDecelerationFlying**(`InBrakingDecelerationFlying`): `void`

飞行制动速率

#### Parameters

| Name | Type |
| :------ | :------ |
| `InBrakingDecelerationFlying` | `number` |


___

### brakingDecelerationSwimming <Score text="brakingDecelerationSwimming" /> 

• `get` **brakingDecelerationSwimming**(): `number`

游泳制动速率

#### Returns

`number`

• `set` **brakingDecelerationSwimming**(`InBrakingDecelerationSwimming`): `void`

游泳制动速率

#### Parameters

| Name | Type |
| :------ | :------ |
| `InBrakingDecelerationSwimming` | `number` |


___

### brakingDecelerationWalking <Score text="brakingDecelerationWalking" /> 

• `get` **brakingDecelerationWalking**(): `number`

行走制动速率

#### Returns

`number`

• `set` **brakingDecelerationWalking**(`InBrakingDecelerationWalking`): `void`

行走制动速率

#### Parameters

| Name | Type |
| :------ | :------ |
| `InBrakingDecelerationWalking` | `number` |


___

### canSetAppearanceData <Score text="canSetAppearanceData" /> 

• `get` **canSetAppearanceData**(): `boolean`

是否可以设置角色形象数据

#### Returns

`boolean`

___

### canStepUpOn <Score text="canStepUpOn" /> 

• `get` **canStepUpOn**(): `boolean` 

获取组件是否可以被玩家站立


#### Returns

`boolean`

true 其他角色可以站到玩家头上  false 其他角色不可以站到玩家头上

• `set` **canStepUpOn**(`CanStepUpOn`): `void` <Badge type="tip" text="server" />

设置组件是否可以被玩家站立


#### Parameters

| Name | Type |
| :------ | :------ |
| `CanStepUpOn` | `boolean` |


___

### capsuleHalfHeight <Score text="capsuleHalfHeight" /> 

• `get` **capsuleHalfHeight**(): `number`

胶囊体半高

#### Returns

`number`

• `set` **capsuleHalfHeight**(`InCapsuleHalfHeight`): `void`

胶囊体半高

#### Parameters

| Name | Type |
| :------ | :------ |
| `InCapsuleHalfHeight` | `number` |


___

### capsuleRadius <Score text="capsuleRadius" /> 

• `get` **capsuleRadius**(): `number`

胶囊体半径

#### Returns

`number`

• `set` **capsuleRadius**(`InCapsuleRadius`): `void`

胶囊体半径

#### Parameters

| Name | Type |
| :------ | :------ |
| `InCapsuleRadius` | `number` |


___

### characterName <Score text="characterName" /> 

• `get` **characterName**(): `string`

角色名称

::: warning Precautions

会显示在角色头顶UI上

:::

#### Returns

`string`

• `set` **characterName**(`inCharacterName`): `void`

角色名称

::: warning Precautions

会显示在角色头顶UI上

:::

#### Parameters

| Name | Type |
| :------ | :------ |
| `inCharacterName` | `string` |


___

### collisionEnable <Score text="collisionEnable" /> 

• `get` **collisionEnable**(): `boolean`

是否开启碰撞

::: warning Precautions

如果关闭碰撞, 角色将无法执行移动相关逻辑

:::

#### Returns

`boolean`

• `set` **collisionEnable**(`InbEnableCollision`): `void`

是否开启碰撞

#### Parameters

| Name | Type |
| :------ | :------ |
| `InbEnableCollision` | `boolean` |


___

### collisionExtent <Score text="collisionExtent" /> 

• `get` **collisionExtent**(): [`Vector`](Type.Vector.md)

碰撞形状的大小

#### Returns

[`Vector`](Type.Vector.md)

___

### collisionShape <Score text="collisionShape" /> 

• `get` **collisionShape**(): [`CustomShapeType`](../enums/Gameplay.CustomShapeType.md)

碰撞形状

#### Returns

[`CustomShapeType`](../enums/Gameplay.CustomShapeType.md)

___

### collisionWithOtherCharacterEnable <Score text="collisionWithOtherCharacterEnable" /> 

• `get` **collisionWithOtherCharacterEnable**(): `boolean`

能否与其他角色发生碰撞

#### Returns

`boolean`

• `set` **collisionWithOtherCharacterEnable**(`value`): `void`

能否与其他角色发生碰撞

#### Parameters

| Name | Type |
| :------ | :------ |
| `value` | `boolean` |


___

### crouchEnable <Score text="crouchEnable" /> 

• `get` **crouchEnable**(): `boolean`

启用/禁用下蹲能力

#### Returns

`boolean`

• `set` **crouchEnable**(`canCrouch`): `void`

启用/禁用下蹲能力

#### Parameters

| Name | Type |
| :------ | :------ |
| `canCrouch` | `boolean` |


___

### crouchedHeight <Score text="crouchedHeight" /> 

• `get` **crouchedHeight**(): `number`

下蹲时胶囊体的高度

#### Returns

`number`

• `set` **crouchedHeight**(`InCrouchedHeight`): `void`

下蹲时胶囊体的高度

#### Parameters

| Name | Type |
| :------ | :------ |
| `InCrouchedHeight` | `number` |


___

### forceUpdateMovement <Score text="forceUpdateMovement" /> 

• `set` **forceUpdateMovement**(`value`): `void` 

启用/禁用强制更新移动


#### Parameters

| Name | Type |
| :------ | :------ |
| `value` | `boolean` |


___

### gravityScale <Score text="gravityScale" /> 

• `get` **gravityScale**(): `number`

重力倍率

::: warning Precautions

范围0~10, 过大和过小的值都会被限制

:::

#### Returns

`number`

• `set` **gravityScale**(`newGravityScale`): `void`

重力倍率

#### Parameters

| Name | Type |
| :------ | :------ |
| `newGravityScale` | `number` |


___

### groundFriction <Score text="groundFriction" /> 

• `get` **groundFriction**(): `number`

地面摩檫力

#### Returns

`number`

• `set` **groundFriction**(`inGroundFriction`): `void`

地面摩檫力

#### Parameters

| Name | Type |
| :------ | :------ |
| `inGroundFriction` | `number` |


___

### headUIVisible <Score text="headUIVisible" /> 

• `get` **headUIVisible**(): `boolean`

头顶UI是否可见

#### Returns

`boolean`

• `set` **headUIVisible**(`isVisible`): `void`

头顶UI是否可见

#### Parameters

| Name | Type |
| :------ | :------ |
| `isVisible` | `boolean` |


___

### headUIVisibleRange <Score text="headUIVisibleRange" /> 

• `get` **headUIVisibleRange**(): `number`

头顶UI可见距离

#### Returns

`number`

• `set` **headUIVisibleRange**(`VisibleDistance`): `void`

头顶UI可见距离

#### Parameters

| Name | Type |
| :------ | :------ |
| `VisibleDistance` | `number` |


___

### isCrouching <Score text="isCrouching" /> 

• `get` **isCrouching**(): `boolean`

是否处于下蹲状态

#### Returns

`boolean`

___

### isJumping <Score text="isJumping" /> 

• `get` **isJumping**(): `boolean`

是否正在跳跃

#### Returns

`boolean`

___

### isMoving <Score text="isMoving" /> 

• `get` **isMoving**(): `boolean`

是否正在移动

#### Returns

`boolean`

___

### jumpEnable <Score text="jumpEnable" /> 

• `get` **jumpEnable**(): `boolean`

启用/禁用跳跃能力

#### Returns

`boolean`

• `set` **jumpEnable**(`value`): `void`

启用/禁用跳跃能力

#### Parameters

| Name | Type |
| :------ | :------ |
| `value` | `boolean` |


___

### jumpMaxCount <Score text="jumpMaxCount" /> 

• `get` **jumpMaxCount**(): `number`

最大可跳跃次数

#### Returns

`number`

• `set` **jumpMaxCount**(`InJumpMaxCount`): `void`

最大可跳跃次数

#### Parameters

| Name | Type |
| :------ | :------ |
| `InJumpMaxCount` | `number` |


___

### jumpingOutOfWaterEnable <Score text="jumpingOutOfWaterEnable" /> 

• `get` **jumpingOutOfWaterEnable**(): `boolean`

是否可以跳出水面

#### Returns

`boolean`

• `set` **jumpingOutOfWaterEnable**(`value`): `void`

是否可以跳出水面

#### Parameters

| Name | Type |
| :------ | :------ |
| `value` | `boolean` |


___

### maxAcceleration <Score text="maxAcceleration" /> 

• `get` **maxAcceleration**(): `number`

最大加速度

#### Returns

`number`

• `set` **maxAcceleration**(`InMaxAcceleration`): `void`

最大加速度

#### Parameters

| Name | Type |
| :------ | :------ |
| `InMaxAcceleration` | `number` |


___

### maxFallingSpeed <Score text="maxFallingSpeed" /> 

• `get` **maxFallingSpeed**(): `number`

最大下落速度

#### Returns

`number`

• `set` **maxFallingSpeed**(`speed`): `void`

最大下落速度

#### Parameters

| Name | Type |
| :------ | :------ |
| `speed` | `number` |


___

### maxFlySpeed <Score text="maxFlySpeed" /> 

• `get` **maxFlySpeed**(): `number`

最大飞行速度

#### Returns

`number`

• `set` **maxFlySpeed**(`InMaxFlySpeed`): `void`

最大飞行速度

#### Parameters

| Name | Type |
| :------ | :------ |
| `InMaxFlySpeed` | `number` |


___

### maxJumpHeight <Score text="maxJumpHeight" /> 

• `get` **maxJumpHeight**(): `number`

最大跳跃高度

#### Returns

`number`

• `set` **maxJumpHeight**(`InMaxJumpHeight`): `void`

最大跳跃高度

#### Parameters

| Name | Type |
| :------ | :------ |
| `InMaxJumpHeight` | `number` |


___

### maxStepHeight <Score text="maxStepHeight" /> 

• `get` **maxStepHeight**(): `number`

获取角色最大可跨越高度

#### Returns

`number`

• `set` **maxStepHeight**(`InMaxStepHeight`): `void`

设置角色最大可跨越高度

#### Parameters

| Name | Type |
| :------ | :------ |
| `InMaxStepHeight` | `number` |


___

### maxSwimSpeed <Score text="maxSwimSpeed" /> 

• `get` **maxSwimSpeed**(): `number`

最大游泳速度

#### Returns

`number`

• `set` **maxSwimSpeed**(`InMaxSwimSpeed`): `void`

最大游泳速度

#### Parameters

| Name | Type |
| :------ | :------ |
| `InMaxSwimSpeed` | `number` |


___

### maxWalkSpeed <Score text="maxWalkSpeed" /> 

• `get` **maxWalkSpeed**(): `number`

地面最大速度

#### Returns

`number`

• `set` **maxWalkSpeed**(`InMaxWalkSpeed`): `void`

地面最大速度

#### Parameters

| Name | Type |
| :------ | :------ |
| `InMaxWalkSpeed` | `number` |


___

### maxWalkSpeedCrouched <Score text="maxWalkSpeedCrouched" /> 

• `get` **maxWalkSpeedCrouched**(): `number`

地面蹲伏行走时的最大移动速度

#### Returns

`number`

• `set` **maxWalkSpeedCrouched**(`maxSpeed`): `void`

地面蹲伏行走时的最大移动速度

#### Parameters

| Name | Type |
| :------ | :------ |
| `maxSpeed` | `number` |


___

### meshOffset <Score text="meshOffset" /> 

• `get` **meshOffset**(): [`Vector`](Type.Vector.md) 

获取mesh相对角色坐标点的偏移


#### Returns

[`Vector`](Type.Vector.md)

• `set` **meshOffset**(`offset`): `void` 

设置mesh相对角色坐标点的偏移


#### Parameters

| Name | Type |
| :------ | :------ |
| `offset` | [`Vector`](Type.Vector.md) |


___

### moveEnable <Score text="moveEnable" /> 

• `get` **moveEnable**(): `boolean`

启用/禁用移动能力

#### Returns

`boolean`

• `set` **moveEnable**(`value`): `void`

启用/禁用移动能力

#### Parameters

| Name | Type |
| :------ | :------ |
| `value` | `boolean` |


___

### moveFacingDirection <Score text="moveFacingDirection" /> 

• `get` **moveFacingDirection**(): [`MoveFacingDirection`](../enums/Gameplay.MoveFacingDirection.md)

运动面朝方向

#### Returns

[`MoveFacingDirection`](../enums/Gameplay.MoveFacingDirection.md)

• `set` **moveFacingDirection**(`InMoveFacingDirection`): `void`

运动面朝方向

#### Parameters

| Name | Type |
| :------ | :------ |
| `InMoveFacingDirection` | [`MoveFacingDirection`](../enums/Gameplay.MoveFacingDirection.md) |


___

### movementAxisDirection <Score text="movementAxisDirection" /> 

• `get` **movementAxisDirection**(): [`Vector`](Type.Vector.md)

运动时依据的轴方向, 只有当前的MovementDirection为AxisDirection时有效

#### Returns

[`Vector`](Type.Vector.md)

• `set` **movementAxisDirection**(`InMovementAxisDirection`): `void`

运动时依据的轴方向, 只有当前的MovementDirection为AxisDirection时有效

#### Parameters

| Name | Type |
| :------ | :------ |
| `InMovementAxisDirection` | [`Vector`](Type.Vector.md) |


___

### movementDirection <Score text="movementDirection" /> 

• `get` **movementDirection**(): [`MovementDirection`](../enums/Gameplay.MovementDirection.md)

运动时依据的正方向

::: warning Precautions

如果是控制器方向, 就以控制器坐标系为轴;
如果是定轴方向，就以世界坐标系为轴;
如果是视线方向, 就以相机坐标系为轴. 在玩家相机不存在Z轴旋转时, 控制器方向和视线方向效果一致, 人形对象的控制器方向和视线方向效果永远一致.

:::

#### Returns

[`MovementDirection`](../enums/Gameplay.MovementDirection.md)

• `set` **movementDirection**(`InMovementDirection`): `void`

运动时依据的正方向

#### Parameters

| Name | Type |
| :------ | :------ |
| `InMovementDirection` | [`MovementDirection`](../enums/Gameplay.MovementDirection.md) |


___

### movementState <Score text="movementState" /> 

• `get` **movementState**(): [`MovementMode`](../enums/Gameplay.MovementMode.md)

当前角色运动状态

#### Returns

[`MovementMode`](../enums/Gameplay.MovementMode.md)

___

### outOfWaterZ <Score text="outOfWaterZ" /> 

• `get` **outOfWaterZ**(): `number`

出水时Z轴方向上的速度

#### Returns

`number`

• `set` **outOfWaterZ**(`value`): `void`

出水时Z轴方向上的速度

#### Parameters

| Name | Type |
| :------ | :------ |
| `value` | `number` |


___

### physicsEnabled <Score text="physicsEnabled" /> 

• `get` **physicsEnabled**(): `boolean`

获取角色物理状态

#### Returns

`boolean`

• `set` **physicsEnabled**(`value`): `void`

设置角色物理状态

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `value` | `boolean` | 是否开启角色物理,默认关闭以节省性能.该属性对角色射线检测功能有影响,如果需要射线检测打到具体的骨骼部位,可将physicsEnabled设置true |


___

### ragdollEnable <Score text="ragdollEnable" /> 

• `get` **ragdollEnable**(): `boolean`

启用/禁用布娃娃状态

#### Returns

`boolean`

• `set` **ragdollEnable**(`value`): `void`

启用/禁用布娃娃状态

#### Parameters

| Name | Type |
| :------ | :------ |
| `value` | `boolean` |


___

### rotateRate <Score text="rotateRate" /> 

• `get` **rotateRate**(): `number`

最大转向速度

::: warning Precautions

设置为负值时, 转向速度被视为无限大, 可以瞬间转向

:::

#### Returns

`number`

• `set` **rotateRate**(`InRotateRate`): `void`

最大转向速度

::: warning Precautions

设置为负值时, 转向速度被视为无限大, 可以瞬间转向

:::

#### Parameters

| Name | Type |
| :------ | :------ |
| `InRotateRate` | `number` |


___

### separateBrakingFrictionEnable <Score text="separateBrakingFrictionEnable" /> 

• `get` **separateBrakingFrictionEnable**(): `boolean`

使用单独制动摩擦

#### Returns

`boolean`

• `set` **separateBrakingFrictionEnable**(`used`): `void`

使用单独制动摩擦

#### Parameters

| Name | Type |
| :------ | :------ |
| `used` | `boolean` |


___

### usedCapsuleCorrection <Score text="usedCapsuleCorrection" /> 

• `get` **usedCapsuleCorrection**(): `boolean`

使用胶囊体修正 true代表应用角色编辑中的数据自动计算胶囊体大小。false代表应用"capsuleHalfHeight"和"capsuleRadius"设置胶囊体的大小。

#### Returns

`boolean`

• `set` **usedCapsuleCorrection**(`usedCapsuleCorrection`): `void`

使用胶囊体修正 true代表应用角色编辑中的数据自动计算胶囊体大小。false代表应用"capsuleHalfHeight"和"capsuleRadius"设置胶囊体的大小。

#### Parameters

| Name | Type |
| :------ | :------ |
| `usedCapsuleCorrection` | `boolean` |


___

### velocity <Score text="velocity" /> 

• `get` **velocity**(): [`Vector`](Type.Vector.md)

当前移动速度

#### Returns

[`Vector`](Type.Vector.md)

___

### walkableFloorAngle <Score text="walkableFloorAngle" /> 

• `get` **walkableFloorAngle**(): `number`

可行走的最大角度

#### Returns

`number`

• `set` **walkableFloorAngle**(`InWalkableFloorAngle`): `void`

可行走的最大角度

#### Parameters

| Name | Type |
| :------ | :------ |
| `InWalkableFloorAngle` | `number` |



## Methods
___

### addImpulse <Score text="addImpulse" /> 

• **addImpulse**(`Vector`, `ignoreMass?`): `void` <Badge type="tip" text="server" />

添加冲量


::: warning Precautions

质量固定为100, 受质量影响的算法为: 冲量按位除以质量

:::

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `Vector` | [`Vector`](Type.Vector.md) | 应用的冲量 |
| `ignoreMass?` | `boolean` | 是否忽略质量对冲量的影响 default:false |


___

### addMoveInput <Score text="addMoveInput" /> 

• **addMoveInput**(`direction`): `void` 

沿着给定的方向向量添加移动输入


::: warning Precautions

效果受movementDirection属性影响

:::

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `direction` | [`Vector`](Type.Vector.md) | 输入的方向 |


___

### appearanceReady <Score text="appearanceReady" /> 

• **appearanceReady**(): `Promise`<`void`\> <Badge type="tip" text="client" />

在外观数据准备好后返回并执行已绑定的函数，保证当前角色换装表现和数据是正确的。在设置角色外观形象之前，可以用做这个判断


#### Returns

`Promise`<`void`\>

异步回调

___

### attach <Score text="attach" /> 

• **attach**(`gameObject`, `slotName`): `void` 

将物体附着到人物角色的指定插槽


#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `gameObject` | `GameObject` | 物体 |
| `slotName` | [`SlotType`](../enums/Gameplay.SlotType.md) | 插槽类型 |


___

### clearAppearance <Score text="clearAppearance" /> 

• **clearAppearance**(): `void` 

清空角色形象数据



___

### clearDecorations <Score text="clearDecorations" /> 

• **clearDecorations**(): `void` <Badge type="tip" text="client" />

清空所有挂件数据



___

### clearOneDecoration <Score text="clearOneDecoration" /> 

• **clearOneDecoration**(`GUID`): `void` <Badge type="tip" text="client" />

删除一个挂件


#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `GUID` | `string` |  实例化后的挂件对象GUID |


___

### crouch <Score text="crouch" /> 

• **crouch**(`isCrouch`): `void` 

下蹲


#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `isCrouch` | `boolean` | 是否下蹲 |


___

### getAppearance <Score text="getAppearance" /> 

• **getAppearance**<`T`\>(): `T` 

设置外观修改功能


#### Type parameters

| Name | Type |
| :------ | :------ |
| `T` | extends [`HumanoidV1`](Gameplay.HumanoidV1.md) \| [`HumanoidV2`](Gameplay.HumanoidV2.md) \| [`FourFootStandard`](Gameplay.FourFootStandard.md) |

#### Returns

`T`

外观修改对象

___

### getControlRotator <Score text="getControlRotator" /> 

• **getControlRotator**(`Out?`): [`Rotation`](Type.Rotation.md) 

获取控制器的旋转


#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `Out?` | [`Rotation`](Type.Rotation.md) | 获取控制器旋转 default:出参，可选参数 |

#### Returns

[`Rotation`](Type.Rotation.md)

控制器的旋转

___

### getDecorations <Score text="getDecorations" /> 

• **getDecorations**(): [`DecorationTuple`](../modules/Gameplay.Gameplay.md#decorationtuple)[] <Badge type="tip" text="client" />

获取当前挂件实例化对象的GUID


#### Returns

[`DecorationTuple`](../modules/Gameplay.Gameplay.md#decorationtuple)[]

GUID数组

___

### getHeadUIWidget <Score text="getHeadUIWidget" /> 

• **getHeadUIWidget**(): [`UIWidget`](Gameplay.UIWidget.md) 

获取头顶UIWidget


#### Returns

[`UIWidget`](Gameplay.UIWidget.md)

头顶UIWidget对象

___

### getSlotName <Score text="getSlotName" /> 

• **getSlotName**(`slotType`): `string` 

获取对应插槽名称


#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `slotType` | [`SlotType`](../enums/Gameplay.SlotType.md) | 插槽类型 |

#### Returns

`string`

插槽名称(string)

___

### isPlayingAnimation <Score text="isPlayingAnimation" /> 

• **isPlayingAnimation**(): `boolean` <Badge type="tip" text="client" />

是否正在播放动画


#### Returns

`boolean`

是否正在播放动画

___

### jump <Score text="jump" /> 

• **jump**(): `void` 

跳跃



___

### loadAnimation <Score text="loadAnimation" /> 

• **loadAnimation**(`GUID`, `sync?`): [`Animation`](Gameplay.Animation.md) 

加载动画,获取到动画对象，playAnimation是个快速实现功能的接口,可配置参数有限。loadAnimation可以返回动画,以进行更加精细的动画控制，获取到对象后需用户自己配置参数，手动调用play接口动画才会播放。


使用示例:加载并播放动画
```ts
let anim = player.character.loadAnimation(animGUID);
anim.play();
anim.rate = 0.5;
anim.loop = 1;
anim.onAnimFinished.add(()=>{
      ..........
})
anim.play()
```

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `GUID` | `string` | 动画GUID |
| `sync?` | `boolean` | Animation对象是否同步 default:true |

#### Returns

[`Animation`](Gameplay.Animation.md)

Animation 对象

___

### loadDecoration <Score text="loadDecoration" /> 

• **loadDecoration**(`decorationString`, `callback`): `void` <Badge type="tip" text="client" />

加载挂件,给移动角色编辑器提供的能力

::: warning Precautions

数据格式为："骨架名字#112801#Glasses#0,0,0|0,-90,0|1,1,1"

:::


#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `decorationString` | `string` |  一个挂件数据 |
| `callback` | [`StringCallback`](../modules/Gameplay.Gameplay.md#stringcallback) |  挂件对象的GUID |


___

### loadStance <Score text="loadStance" /> 

• **loadStance**(`GUID`, `sync?`): [`SubStance`](Gameplay.SubStance.md) 

创建一个二级姿态对象并返回


::: warning Precautions

即使在服务器上调用loadStance(), 如果sync参数置为false, 也不会同步操作到客户端.

:::

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `GUID` | `string` |  预制姿态资源GUID或动画资源GUID |
| `sync?` | `boolean` |  对姿态对象的操作是否自动同步 default:true |

#### Returns

[`SubStance`](Gameplay.SubStance.md)

二级姿态对象

___

### lookAt <Score text="lookAt" /> 

• **lookAt**(`TargetPoint`): `void` 

角色面朝目标点


#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `TargetPoint` | [`Vector`](Type.Vector.md) | 目标点 |


___

### playAnimation <Score text="playAnimation" /> 

• **playAnimation**(`GUID`, `loopCount?`, `rate?`): [`Animation`](Gameplay.Animation.md) 

播放动画,同时获取到动画对象,Animation对象接口默认是同步的，playanimation是个快速实现功能的接口,可配置参数有限，loadanimation 可以返回动画,以进行更加精细的动画控制。


使用示例:播放动画
```ts
player.character.playAnimation(animGUID);
....... or ......
player.character.playAnimation(animGUID，100，2);
```

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `GUID` | `string` | 动画GUID |
| `loopCount?` | `number` | 循环播放次数, 范围0~2147483647, 设置为0时无限循环 default:1 |
| `rate?` | `number` | 播放速率，1表示正常速率 default:1 |

#### Returns

[`Animation`](Gameplay.Animation.md)

Animation 对象

___

### setAppearance <Score text="setAppearance" /> 

• **setAppearance**<`T`\>(`clz`): `T` 

设置外观修改功能


#### Type parameters

| Name | Type |
| :------ | :------ |
| `T` | extends [`SomatotypeBase`](Gameplay.SomatotypeBase.md)<`T`\> |

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `clz` | [`Constructor`](../modules/Gameplay.Gameplay.md#constructor)<`T`\> | 外观修改接口类类型 |

#### Returns

`T`

外观修改对象

___

### setCollisionShapeAndExtent <Score text="setCollisionShapeAndExtent" /> 

• **setCollisionShapeAndExtent**(`ShapeType`, `CollisionExtent`): `void` 

设置不同形状不同大小的碰撞体


使用示例:创建一个名为"NewScript"的脚本，放置在对象栏中，打开脚本，输入一下代码保存，运行游戏，你将看到日志窗口输出对应的数值,代码如下:
```ts
@Core.Class
export default class NewScript extends Core.Script {
 protected onStart(): void {
    Gameplay.asyncGetCurrentPlayer().then((player) => {
    player.character.usedCapsuleCorrection = false;
    player.character.setCollisionShapeAndExtent(Gameplay.CustomShapeType.VerticalCapsule, new Type.Vector(100, 100, 100));
    console.log(player.character.collisionExtent);
 });
}
}
```

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `ShapeType` | [`CustomShapeType`](../enums/Gameplay.CustomShapeType.md) | 启用的碰撞形状 |
| `CollisionExtent` | [`Vector`](Type.Vector.md) | 启用的碰撞形状 |


___

### setLocallyVisibility <Score text="setLocallyVisibility" /> 

• **setLocallyVisibility**(`status`, `propagateToChildren?`): `void` <Badge type="tip" text="client" />

设置是否被显示(本地生效)


#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `status` | [`PropertyStatus`](../enums/Type.PropertyStatus.md) | 状态 |
| `propagateToChildren?` | `boolean` |  是否设置子物体 default:true |


___

### stopStance <Score text="stopStance" /> 

• **stopStance**(`sync?`): `void` 

停止任何正在播放的姿态


::: warning Precautions

当你不想保存执行play()后的姿态对象时, 可以直接调用这个方法停止姿态. 对单端对象操作时需要把sync参数置为false.

:::

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `sync?` | `boolean` |  是否自动同步 default:true |


___

### swimmingDown <Score text="swimmingDown" /> 

• **swimmingDown**(`speed`): `void` 

水中下潜


#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `speed` | `number` | 下潜速度不能超过MaxSwimSpeed(游泳最大速度) |


___

### swimmingUp <Score text="swimmingUp" /> 

• **swimmingUp**(`speed`): `void` 

水中上浮


#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `speed` | `number` | 上浮速度不能超过MaxSwimSpeed(游泳最大速度) |


___

### switchToFlying <Score text="switchToFlying" /> 

• **switchToFlying**(): `void` 

切换为飞行状态



___

### switchToSwimming <Score text="switchToSwimming" /> 

• **switchToSwimming**(): `void` 

切换为游泳状态


::: warning Precautions

仅在游泳区域中生效

:::


___

### switchToWalking <Score text="switchToWalking" /> 

• **switchToWalking**(): `void` 

切换为行走状态


