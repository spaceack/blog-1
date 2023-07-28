在物联网时代，工业物联网（IIoT）已成为工业运作的变革力量。通过连接设备、机器和系统，工业物联网能够实时监测、分析和控制工业流程，提升效率、生产力和安全性。

然而，在传统的工业物联网系统中，分散、异构、复杂的边缘设备给互操作性、扩展性和安全性带来了巨大的挑战。统一命名空间(Unified Namespace, UNS)框架能够应对这些挑战，并为 IIoT 4.0 带来许多好处，例如简化数据集成、增强数据可用性和扩展性。

## 什么是统一命名空间？

统一命名空间目前还没有权威的定义。从自动化的角度来看，统一命名空间可以被理解为一种通用的命名规范，用于组织设备、数据点和服务。它基于它们的属性（如位置、功能和类型）对其进行组织。不过，[Walker Reynolds](https://www.youtube.com/watch?v=1h0DFwWz4uE) 则认为统一命名空间不仅仅是一个命名，而是定义为满足以下五个条件的架构：

- 统一命名空间是业务数据和事件的语义层次结构。
- 统一命名空间是连接所有智能设备和 IT 基础设施的枢纽。
- 统一命名空间是业务中所有数据和信息的唯一可靠来源。
- 统一命名空间是未来数字化转型的根基。
- 统一命名空间反映了业务的当前状态，能够提供业务的实时快照。

这两种观点共同认为，统一命名空间是一个本体通信层，连接了工业物联网中的各个部分。它提供了一个共享的数据交汇点，使不同的系统和相关方能够进行沟通和协作，不受他们使用的技术或供应商的限制。

这个共享的交汇点可以增强工业物联网系统的互操作性、扩展性和灵活性，从而降低集成成本并加快上市速度。

统一命名空间在 IIoT 4.0 中的另一个优点是优化了数据管理和分析。通过使用通用的命名规则，统一命名空间使得数据点可以在不同的系统和应用之间被方便地识别、访问和分析。有了统一命名空间架构，只要有安全授权，公司内部的任何人都可以获取任何工业物联网组件的全部数据。

## 统一命名空间架构的演变

第一个统一命名空间项目是由 Walker Reynolds（Industrial 4.0 Solutions 总裁，2015 年 Ignition by Inductive Automation Award 的得主）在 2005 年创建的。他也是推广统一命名空间的最重要的人物。该项目利用动态数据交换（DDE）和 Excel 电子表格为一个盐田建立了统一命名空间。次年，该项目改用了 MQTT 技术。

最初，Walker 打算开发一个连接所有工业物联网基础设施的数据高速公路。数据高速公路负责从所有冲压机（盐田中使用的开采机器）采集数据。维护人员无需驾车到控制室的屏幕前检查人机界面（HMI）或控制面板。通过将所有操作统一在一个命名空间中，用户无需来回奔波于相隔数英里的厂房和工厂之间，就能够监控生产环境。

在随后的几年中，统一命名空间不断发展，如今已经成为工业物联网中的一个基础概念。

## 统一命名空间与传统工业物联网数据模型的区别

在工业 3.0 时代，常常利用 ERP 或 CRM 系统来管理组织和制造厂的运营。这些系统与仓库管理系统（WMS）相互配合，从操作员那里接收生产订单并将调度计划、物料清单和工作订单发送到工厂。制造厂通过电子表格向中央办公室和操作员报告情况。然而，由于数据不是实时的，这种方式无法准确地反映当前的业务状态。

![Industry 3.0](https://assets.emqx.com/images/5cb2b8ded153af99510b2dc98fc21837.png)

此外还存在另一个问题，如果公司想要采用商业智能（BI）或人工智能和机器学习（AI/ML）等新技术，它们往往需要完整的数据集作为基础，而不能仅仅基于传统 IIoT 3.0 系统的部分数据。 但是，目前没有简单的方法来创建这样的统一的数据集。

另外，传统的 ERP 系统通常无法直接连接到工厂的机械设备，这就导致了一种复杂的基础设施，被戏称为“数据意大利面”。这正是统一命名空间的优势所在：在边缘设备和云上运行的多个命名空间，它们相互协作，形成一个统一的命名空间。

![UNS](https://assets.emqx.com/images/5e0a17bfeb781e0b7025254f79351029.png)

下图展示了统一命名空间的不同层级：

![The different layers of a UNS](https://assets.emqx.com/images/b294138a63506c8a3f18e1fb9dcd1895.png)

在架构的最底层是**物理设备，如 HMI/PLC**，这里也是数据产生的地方。每个 PLC/HMI，甚至一个含有信息的标签，都可以看作一个命名空间，它将读数和事件发送到**数据采集层**，进行监控和控制。在这一层，常见的做法是部署一个工业网关，如 Neuron，来收集数据。

数据采集层之上是**制造执行层（MES）**，它负责协调 ERP/CRM 和工厂之间的关系，把销售订单转化为生产安排。传统的 ERP 层负责处理客户销售、计划生产、管理库存、检查财务支付等。

最顶层是用于管理业务层的**商业智能云**。

## 统一命名空间的优势

在组织中采用统一命名空间有以下几个好处：

- **集成简单：**工业物联网环境中的数据生产者和消费者只要接入网络就能实现集成。无需专业技术或工程工作，就能在从厂房到业务层的各个层面，实现数据的集成。
- **提高敏捷性：**统一命名空间能够实时获取任意时刻的数据状态，从而加快并优化测试、计划和交付的过程。
- **可扩展性强：**由于数据生产者和消费者是通过一个中心节点集成的，而不是直接相连的，因此可以连接百万级的节点，并保证它们之间的顺畅通信。

## 统一命名空间的 4 种类型

统一命名空间有四种类型，分别适用于不同的用途和方法。

### 功能命名空间(Functional Namespaces) 和 OEE

功能命名空间是指按照设备和数据点在工业网络中的功能或目的来组织它们。这意味着设备和数据点是按照它们完成的具体任务来分组，而不是按照它们的物理位置或网络。

例如，在一个制造厂中，与生产过程有关的设备和数据点可能被归入一个功能命名空间，而与维护有关的设备和数据点可能被归入另一个功能命名空间。

通常，功能命名空间用于计算整体设备效率 (OEE)，这是一个衡量制造设备性能的指标。OEE 是精益制造和持续改进计划中的一个重要指标。它包括三个因素：

- **可用性：**设备能够用于生产的时间
- **性能：**设备运行的速度
- **质量：**产品达到预期规格的比例

通过将不同的数据源和相关信息整合到功能命名空间中，制造商可以计算 OEE，并发现设备性能不佳的地方，从而采取措施提高效率和生产力。

### 信息命名空间(Informative Namespace)

信息命名空间是根据设备和数据点在工业网络中的信息内容来组织它们。这意味着设备和数据点是根据它们提供的信息类型进行分组，而不是根据它们的物理位置或功能。

例如，在一个制造厂中，与温度有关的设备和数据点可能被归入一个信息命名空间，而与压力有关的设备和数据点可能被归入另一个信息命名空间。

信息命名空间的目的是为了便于访问和分析工业网络中的数据。通过按照信息内容来归类设备和数据点，可以更容易地识别数据中的规律和趋势，并根据数据做出明智的决策。总而言之，信息命名空间可以通过方便地访问和分析数据，以及根据数据做出明智的决策，来提升工业网络的效率和效果。

### 定义命名空间(Definitional Namespace)

在工业网络和计算机科学的语境下，定义命名空间是按照设备和数据点的定义或属性来组织它们。这意味着设备和数据点是按照它们的特性来归类，比如类型、大小或功能。

例如，在一个制造厂中，与电机有关的设备和数据点可能被归入一个定义命名空间，而与传感器有关的设备和数据点可能被归入另一个定义命名空间。

### 临时命名空间(Ad Hoc Namespace)

临时命名空间是一种暂时或非正式的组织设备和数据点的方式。它可能在还未建立更正式的命名空间时使用，或者在设备和数据点需要快速归类以满足特定目的时使用。

例如，如果一个制造厂发生了一个突发的设备故障，一个临时命名空间可能被建立用来将所有与那个设备相关的设备和数据点归类在一起，以便尽快地诊断和解决问题。

## 结语

统一命名空间简化了设备通信和数据管理，因为设备和数据点只需知道它们想要通信的设备或数据所发布或订阅的主题，而不用知道设备或数据的具体位置或网络。

除了简化设备通信和数据管理，统一命名空间还提供了一种在工业网络中集成不同系统和协议的方法。把设备和数据点按照一个层次化的主题结构来组织，可以让不同的系统和协议更容易地集成，因为它们都遵循相同的命名规范来通信。

总之，统一命名空间是工业物联网的一个重要特性，它简化了设备通信、数据管理和系统集成。它让工业网络更加高效和顺畅，从而提升生产力、减少停机时间和优化整体性能。



<section class="promotion">
    <div>
        联系 EMQ 工业领域解决方案专家
    </div>
    <a href="https://www.emqx.com/zh/contact?product=solutions" class="button is-gradient px-5">联系我们 →</a>
</section>