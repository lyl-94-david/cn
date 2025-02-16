# 产品物模型介绍

在物联网引擎中，定义物模型即定义产品功能。物模型（Thing Model）是真实世界的物体在虚拟世界中的数字化表现。物模型定义了一类物是什么，有什么属性，能做什么，能对外提供什么功能服务。完成功能定义后，系统将自动生成该产品的物模型。物模型描述产品可以提供的服务。物模型将产品功能分为三类：属性、服务和事件。


| 物模型定义                  | 描述                 |
| :-------------------: | :------------------- |
|物模型信息  | 物模型的基本信息。 |
|物信息  | 物体的基本信息，为系统固定字段。 |
|标准状态  | 在物联网平台里数字化物体所具有的标准状态。仅包括在线状态和激活状态。|
|属性  | 描述物体的现实属性和状态，分为只读和读写两类属性，支持读取和设置（读写属性）。 |
|服务  | 可被外部（Hub/应用）调用的一系列的指令和方法。相比于设置属性，服务可以提供更复杂的业务逻辑。如：执行某一任务。 | 
|事件  | 是指物体自身主动上报的信息，包含多个需要外部及时感知和处理的消息，比如：报警信息，故障信息等。| 



## 术语解释

| 名称                  | 定义                 |
| :-------------------: | :------------------- |
|物  | 真实世界中存在的物体。更广义的说法是真实/虚拟世界中存在的实体 |
|物模型  | 是物在虚拟世界中的数字化表现。物模型定义了一类物是什么，有什么属性，能做什么，能对外提供什么功能服务。 |
|产品  | 指一组具有相同功能的设备集合。每个产品具有全局唯一的ProductKey。每个产品下可以创建海量设备。|
|物影子  | 物影子是一个Json文档，主要用于存储物当前上报的属性值和用户期望下发给设备的属性值。每一个物有且只有一个物影子。物影子对应物模型中定义的所有读写属性 |
|数据类型  | 目前物模型中支持定义的数据类型为：字符串（string）、布尔值（bool）、单精度浮点（float）、整型（int32）、双精度浮点（double）、枚举值（enum） | 
|读写性  | 面向用户的定义，指该字段值是否可被用户读写。| 
|物模型下唯一  | 指在该物模型内定义唯一，不能出现重名。| 
