# Introduction

## MICROELECTRONICS

The economics of VLSl circuits relies on the principle that replicating a circuit  is straightforward and therefore the design and manufacturing costs can be recovered  over a large volume of sales. The trend toward higher integration is economically positive because it leads to a reduction in the number of components per system, and therefore to a reduced cost in packaging and interconnection, as well as to a higher reliability of the overall system. More importantly, higher integration correlates to faster circuits, because of the reduction of parasitic effects in the electronic devices themselves and in the interconnections. As a result, the higher the integration level is, the better and cheaper the final product results. 

VLSI 电路的经济性依赖于复制电路的原理简单明了，因此可以通过大量的销售量收回设计和制造成本。 经济一体化的趋势是积极的，因为它会导致每个系统的组件数量减少，并且因此，以降低封装和互连成本，以及更高整个系统的可靠性。 更重要的是，更高的集成度与更快的电路有关，因为减少了相互连接的电子设备中的寄生效应。 因此，集成度越高，最终产品效果更好、更便宜。

##  SEMICONDUCTOR TECHNOLOGIES  AND CIRCUIT TAXONOMY 

**Electronic circuits are generally classified as analog or digital**. In the former class, the information is related to the value of a continuous electrical parameter, such as a voltage or a current. A power amplifier for an audio stereo system employs analog circuits. In digital circuits, the inionnation is quantized. Most digital circuits we binary, and therefore the quantum of information is either a TRUE or a FALSE value. The information is related to ranges of voltages at circuit internal nodes. Digital circuits have shown to be superior to analog circuits in many classes of applications, primarily electronic computing. Recently, digital applications have pervaded also the signal processing and telecommunication fields. Examples are compact disc players and digital telephony. Today the number of digital circuits overwhelms that of analog circuits.

电子电路通常分为模拟电路或数字电路。 在前者类，信息与连续电气参数的值有关，例如电压或电流。 用于音频立体声系统的功率放大器采用模拟电路。 在数电路中，离子化是量化的。 大多数数字电路都是二进制的，因此信息量要么是 TRUE 要么是 FALSE 值。 这信息与电路内部节点的电压范围有关。 数字电路已证明在许多类别的应用中优于模拟电路，主要是电子计算。 最近，数字应用也遍及信号处理和电信领域。 例子是光盘播放器和数字电话。 今天，数字电路的数量超过了模拟电路的数量。



Digital circuits can be classified in terms of their mode of operations. **Synchronoits circuits** are characterized by having information storage and processing synchronized to one (or more) global signal, called clock. **Asynchronous circuits** do not require a global clock signal. Different styles have been proposed for asynchronous design methods. When considering large-scale integration circuits, synchronous operation is advantageous because it is conceptually simpler; there is a broader common knowledge of design and verification methods and therefore the likelihood of final correct operation is higher. Furthermore, testing techniques have been developed for synchronous digital circuits. Conversely, the advantage of using asynchronous circuits stems from the fact that global clock distribution becomes more difficult as circuits grow in size, therefore invalidating the premise that designing synchronous circuits is simpler. Despite the growing interest in asynchronous circuits, most commercial digital designs use synchronous operation. 

数字电路可以根据其操作模式进行分类。同步器电路的特点是信息存储和处理与一个（或多个）全局信号（称为时钟）同步。异步电路不需要一个全局时钟信号。已经为异步提出了不同的风格设计方法。在考虑大规模集成电路时，同步操作是有利的，因为它在概念上更简单；有一个更广泛的共同点设计和验证方法的知识，因此最终的可能性正确操作较高。此外，还开发了测试技术同步数字电路。相反，使用异步电路的优势源于这样一个事实，即全局时钟分配随着电路变得更加困难
尺寸增大，因此使设计同步电路的前提无效更简单。尽管人们对异步电路越来越感兴趣，但大多数商业数字设计使用同步操作。

It is obvious that the choice of a semiconductor technology and the circuit class affect the type of CAD tools that are required. The choice of a semiconductor technology affects mainly the physical design of a circuit, i.e., the determination of the geometric patterns. It affects only marginany functional design. Conversely. the circuit type (i.e., analog, synchronous digital or asynchronous digital) affects the overall design of the circuit. In this book we consider CAD techniques for synchronous digital circuits, because they represent the vast majority of circuits and because these CAD design techniques have reached a high level of maturity.

很明显，半导体技术和电路的选择类影响所需的 CAD 工具的类型。 半导体的选择技术主要影响电路的物理设计，即确定的几何图案。 它只影响任何功能设计。 反过来。电路类型（即模拟、同步数字或异步数字）会影响电路的整体设计。 在本书中，我们考虑了用于同步的 CAD 技术数字电路，因为它们代表了绝大多数电路，并且因为这些CAD 设计技术已经达到了很高的成熟度。

## MICROELECTRONIC DESIGN STYLES

**Different design styles, often called methodologies**, have been used for microelectronic circuits. They are usually classified as **custom** and **semicustom** design styles. In the former case, the functional and physical design are handcrafted, requiring an extensive effort of a design team to optimize each detailed feature of the circuit. In this case, the design and cost are high, often compensated by the achievement of high-quality circuits.It is obvious that the cost bas either to be amortized over a large volume production (as in the case of processor design) or borne in full (as in the case of special applications). Custom design was popular in the early years of microelectronics. Today, the design complexity bas confined custom design techniques to specific portions of a limited number of projects, such as execution and floating point units of some processors

不同的设计风格，通常称为方法论，已用于微电子电路。 它们通常分为定制和半定制设计风格。在前一种情况下，功能和物理设计是手工制作的，需要设计团队付出了巨大的努力来优化电路的每个细节特征。 在这种情况下，设计和成本都很高，通常通过实现高质量电路来弥补。很明显，成本要么摊销在一个大批量生产（如在处理器设计的情况下）或全部承担（如在特殊应用的情况）。 定制设计在微电子的早期很流行。 今天，设计复杂性将定制设计技术限制在有限数量项目的特定部分，例如执行和浮点一些处理器的单元。

Semicustom designs can be partitioned in two major classes: **cell-based design** and array-based design. These classes further subdivide into subclasses. Cell-based design leverages the use of library cells, that can be designed once and stored, or the use of cell generators that synthesize macro-cell layouts from their functional specifications. In cell-based design the manufacturing process is not simplified at all with respect to custom design. Instead, the design process is simplified, because of the use of ready-made building blocks. 

**半定制设计可以分为两大类： 基于单元的设计和基于阵列的设计。** 这些类进一步细分为子类。 基于单元的设计利用可以设计一次并存储的库单元，或根据功能规格使用单元生成器来合成宏单元布局。 在基于单元的设计中，和定制设计相比没有简化制造的过程。 相反，他简化了设计过程，因为使用了现成的库。

 The combination of custom design and cell-based design has been used often for microprocessor design,

## DESIGN OF MICROELECTRONIC  CIRCUITS 

An objective of design is to maximize some figures of merit  of the circuit tlial relale to its quality. Validation consists of verifying the consistency  of the models used during design, as well as some properties pf the original model. 

设计的一个目标是最大化一些与电路质量相关的品质因数。 验证包括验证一致性设计过程中使用的模型，以及原始模型的一些属性。

Circuit optimization is often combined with synthesis. It entails the selection of some particular choices in a given model, with the goal of raising one (or more) figures of merit of the design. The role of optimization is to enhance the overall quality of the circuit. We explain now in more detail what quality means. First of all, we mean circuit performance. **Performance relates to the time required to process some information**, as well as to the amount of information that can be processed in a given time period. Circuit performance is essential to competitive products in many application domains. Second, **circuit quality relates to the overall area.** An objective of circuit design is to minimize the area, for many reasons. Smaller circuits relate to more circuits per wafer, and therefore to lower manufacturing cost. The manufacturing yield decreases with an increase in chip area. Large chips are more expensive to package too. Third, the circuit quality relates to the testabilify, i.e., to the ease of testing the chip after manufacturing. For some applications, the faulr coverage is an important quality measure. It spells the percentage of faults of a given type that can be detected by a set of test vectors. It is obvious that testable chips are desirable, because earlier detection of malfunctions in electronic systems relates to lower overall cost. 

电路优化通常与综合相结合。它需要选择给定模型中的一些特定选择，目的是提高一个（或多个）数字设计的优点。优化的作用是提升整体质量电路。我们现在更详细地解释质量的含义。首先，我们指的是电路表现。性能与处理某些信息所需的时间有关，以及在给定时间段内可以处理的信息量。电路性能对于许多应用领域的竞争产品至关重要。其次，电路质量与整体面积有关。电路设计的一个目标是最小化面积，原因有很多。较小的电路与每个晶片更多的电路有关，从而降低制造成本。制造良率随着芯片面积增加。大芯片的封装成本也更高。三、电路质量与可测试性有关，即与制造后测试芯片的难易程度有关。对于某些应用程序，故障覆盖率是一项重要的质量度量。它拼写一组测试向量可以检测到的给定类型故障的百分比。它很明显，可测试的芯片是可取的，因为更早地检测到故障
在电子系统中涉及到较低的总体成本。

## COMPUTER-AIDED SYNTHESIS AND  OPTIMIZATION

### Circuit Models 

A model of a circuit is an abstraction, i.e., a representation that shows relevant features without associated details. Synthesis is the generation of a circuit model, starting from a less detailed one. Models can be classified in terms of levels of abstraction and views. We consider here three main abstractions, namely: **architectural, logic and geometrical**. The levels can he visualized as follows. At the architectural level a circuit performs a set of operations, such as data computation or transfer. At the logic level, a digital circuit evaluates a set of logic functions. At the geometrical level, a circuit is a set of geometrical entities. Examples of representations for architectural models are HDL models or flow diagrams; for logic models are state transition diagrams or schematics; for geometric models are floor plans or layouts.

电路模型是一种抽象，即显示相关特征的表示没有相关的细节。 综合是电路模型的生成，开始从一个不太详细的。 模型可以根据抽象级别进行分类和意见。 我们在这里考虑三个主要抽象，即：架构、逻辑和几何。 他可以将级别可视化如下。 在架构层面，电路执行一组操作，例如数据计算或传输。 在逻辑层面，数字电路评估一组逻辑功能。 在几何层次上，电路是一组几何实体。 架构模型的表示示例是 HDL 模型或流程图； 对于逻辑模型是状态转换图或示意图； 几何模型是平面图或布局。

**We consider now the views of a model. They are classified as: behavioral,  structural and physical.** Behavioral views debcribe the function of the circuit regardless  of its implementation. Structural views describe a model as an interconnection of  components. Physical views relate to the physical objects (e.g., transistors) of a design.

### Synthesis

**Architectural-level synthesis** consists of generating a structural view of an architectural-level model. This corresponds to determining an assignment of the circuit  functions to operators, called resources, as well as their interconnection and the  timing pf their execution. It has also been called **high-level synthesis or structural  synthesis**, because it determines the macroscopic (i.e., block-level) structure of  the circuit. To avoid ambiguity, and for the sake of uniformity, we shall call it  **architectural synthesis.** 

**Logic-level synthesis** is the task of generating a structural view of a logic-level  model. Logic synthesis is the manipulation of logic specifications to create logic  models as an interconnection of logic primitives. Thus logic synthesis determines  the microscopic (i.e., gate-level) structure of a circuit. The task of transforming a logic model into an interconnection of instances of library cells, i.e., the hack end  of logic synthesis, is often referred to as **library binding** or **technology mapping**. 

**Geometrical-level synrhesis** consists of creating a physical view at the geometric  level. It entails the specification of all geometric patterns defining the physical  layout of the chip, as well as their position. It is often called physical design, and  we shall call it so in the sequel. 

**The macroscopic figures of merit of the implementation, such as circuit area and  performance, depend heavily on this step. Indeed, architectural synthesis determines  the degree of parallelism of the operations. Optimization at this level is very important,** 

### Optimization

Optimization  is motivated not only by the desire of maximizing the circuit quality, but also by the  fact that synthesis without optimization would yield noncompetitive circuits at all, and  therefore its value would be marginal. In this book, we consider the optimization of  two quality measures, namely, **area and perfarmance.** 

**Circuit area is an extensive quantity.** It is measured by the sum of the areas of  the circuit components and therefore it can bc computed from a structural view of a  circuit, once the areas of the components are known. The area computation can be  performed hierarchically. Usually, the fundamental components of digital circuits are  logic gates and registers, whose area is known a priori. The wiring area often plays an  important role and should not be neglected. It can be derived from a complete physical  view, or estimated from a structural view using predictive or statistical models. 

**Circuit performance is an intensive quantity.** It is not additive, and therefore its  computation requires analyzing the structure and often the behavior of a circuit. To be  more specific, we need to consider now the meaning of performance in more detail,  according to the different classes of digital circuits。

**The performance of a combinational logic circuit is measured by the inputloutput  propagation delay.** Often a simplifying assumption is made. All inputs are available  at the same time and the performance relates to the **delay through the critical path of  the circuit.** 

**The performance of a synchronous sequential circuit can be measured by its  cycle-time**, i.e., the period of the fastest clock that can be applied to the circuit. Note  that the delay through the combinational component of a sequential circuit is a lower  bound on the cycle-time. 

**According to these definitions and models, performance optimization consists  in minimizing the delay (for combinational circuits), the cycle-time and the latency  (for synchronous circuits) and maximizing the throughput (for pipelined circuits).** 

根据这些定义和模型，性能优化包括最小化延迟（对于组合电路）、周期时间和延迟（对于同步电路）和最大化吞吐量（对于流水线电路）。

## ORGANIZATION OF THE BOOK

Example of abstract models that can be derived from HDL models by compilation,  are: **sequencing and data-flow graphs (representing operations and dependencies),  state transition diagrams (describing finite-state machine behavior) and logic networks**

## SYNTHESIS AND OPTIMIZATION:  AN HISTORIC PERSPECTIVE 

Early efforts on logic synthesis and optimization algorithms date to the 1950s and 1960s. While this work has much historical importance, it has had less practical impact on CAD tools for microelectronic circuit design. Indeed most of the classical approaches to solving logic design problems were developed before the advent of very large-scale integration. Therefore those methods suffer from being not practical for mediumllarge-scale problems.

逻辑综合和优化算法的早期努力可以追溯到 1950 年代和1960 年代。 虽然这项工作具有很大的历史意义，但它的实际应用较少对用于微电子电路设计的 CAD 工具的影响。 事实上，解决逻辑设计问题的大多数经典方法都是在超大规模集成出现之前开发的。 因此，这些方法对于中等规模的问题并不实用。

As soon as large-scale integration (LSI) became possible from a technological standpoint, and LSI circuit design became practical because of the support provided by physical design tools, the research interest shifted to the logic level of abstraction. One major motivation was avoiding the design entry at the physical level, which is a tedious and error-prone task. The use of logic synthesis techniques required also a change in attitude toward problem solving. In the early 1970s the computational intractability theory was introduced. Researchers realized that it was not useful to extend the classical methods of switching theory, which tried to solve problems exactly. Instead, "good engineering solutions, such as those constructed by heuristic algorithms, were the goal to pursue in order to cope with LSI.

一旦从技术角度来看大规模集成（LSI）成为可能，并且由于物理设计工具提供的支持，LSI电路设计变得实用，研究兴趣转移到抽象的逻辑级别。 一个主要的动机是避免在物理级别进行设计输入，这是一项乏味且容易出错的任务。 使用逻辑综合技术也需要改变解决问题的态度。 **在 1970 年代初期，引入了计算难处理性理论。 研究人员意识到，扩展试图准确解决问题的经典转换理论方法并没有用处。 相反，“良好的工程解决方案，例如由启发式算法构建的解决方案，是应对 LSI 所追求的目标。**

An early example of "modem" logic optimization was IBM's program MINI,  a heuristic minimizer for two-level logic forms implementable by PLAs. MINI could  compute solutions whose quality was near optimal and could run in reasonable time  on most circuits of interest. In the 1970s, logic synthesis teols targeted mainly twolevel logic representations, and they were coupled to macro-cell generators for PLAs.  Programs for PLA-based combinational and sequential logic design were then developed. The most prominent example was program ESPRESSO, developed at IBM jointly  with the University of California at Berkeley. 

“调制解调器”逻辑优化的一个早期例子是 IBM 的程序 MINI，这是一个启发式最小化器，用于 PLA 可实现的两级逻辑形式。 MINI 可以计算出质量接近最佳的解决方案，并且可以在大多数感兴趣的电路上在合理的时间内运行。 **在 1970 年代，逻辑综合工具主要针对两级逻辑表示，它们与 PLA 的宏单元生成器耦合。 然后开发了基于 PLA 的组合和顺序逻辑设计程序。 最突出的例子是 IBM 与加州大学伯克利分校联合开发的 ESPRESSO 程序。**

In the early 1980s. as VLSI circuit technology matured, two requirements became important: the possibility of configuring logic circuits into multiple-level forms appropriate for cell-based and array-based styles and the necessity of using a higher, architectural level of abstraction in modeling and as a starting point for synthesis. 

**在 1980 年代初期。 随着 VLSI 电路技术的成熟，两个要求变得重要：将逻辑电路配置为适合基于单元和基于阵列的样式的多级形式的可能性，以及在建模和作为综合开始点时使用更高的架构抽象级别的必要性。**

The former issue was related to the evdution of semicustom design. Technology  mapping became the primary tool for redesigning transistor-tmnsistor-logic (TTL)-  based boards into CMOS integrated circuits. **Technology mapping, also called library  binding**, was researched at AT&T Bell Laboratories, where the first algorithmic approach was implemented in program DAGON and at IBM, where the rule-based LOGIC  SYNTHESIS SYSTEM (LSS) was introduced and used for designing mainframe computers. Multiple-level logic optimization algorithms and programs were then developed,  such as the YORKTOWN LOGIC EDITOR (YLE) program at IBM and MULTIPLE-LEVEL  INTERACTIVE SYSTEM (MIS) at the University of California at Berkeley, that could  cope with the manipulation and reduction of large sets of logic equations. At the same  time, the transduction method was also introduced at the University of Illinois and  then used in the Fujitsu's logic design system.

前一个问题与半定制设计的发展有关。 技术映射成为将基于晶体管-晶体管逻辑 (TTL) 的电路板重新设计为 CMOS 集成电路的主要工具。 tech map，也称为库绑定，在 AT&T 贝尔实验室进行了研究，第一个算法方法在程序 DAGON 和 IBM 中实现，基于规则的逻辑合成系统 (LSS) 被引入并用于设计大型机计算机 . 随后开发了多级逻辑优化算法和程序，如 IBM 的 YORKTOWN LOGIC EDITOR (YLE) 程序和加州大学伯克利分校的 MULTIPLE-LEVEL INTERACTIVE SYSTEM (MIS) 大量的逻辑方程。 同时，在伊利诺伊大学也引入了换能方法，然后在富士通的逻辑设计系统中使用。

As logic synthesis tools matured and companies started commercializing them, it became apparent that VLSI design could not be started by conceptualizing systems in terms of logic-level primitives and entering large circuits by means of schematic 
capture systems. Architectural (or high-level) synthesis techniques that traced hack to the MIMOLA system at Honeywell and the ALERT systems at IBM became an important research subject, especially at Camegie-Mellon University, the University of Southern California and Carleton University. The early architectural synthesis systems targeted instruction-set processor design and were not coupled to logic synthesis tools. The first fully integrated synthesis systems were IBM's YORKTOWN SILICON COMPILER (YSC), GTFs SILC system and the CATHEDRAL systems developed at the Catholic University of Leuven, Belgium. 

随着逻辑综合工具的成熟和公司开始将它们商业化，很明显，VLSI设计不能通过逻辑级原语概念化系统和通过原理图进入大型电路来开始
捕获系统。 追溯到霍尼韦尔的 MIMOLA 系统和 IBM 的 ALERT 系统的架构（或高级）综合技术成为一个重要的研究课题，特别是在卡梅基梅隆大学、南加州大学和卡尔顿大学。 早期的架构综合系统以指令集处理器设计为目标，并未与逻辑综合工具耦合。 第一个完全集成的合成系统是 IBM 的 YORKTOWN SILICON COMPILER (YSC)、GTFs SILC 系统和比利时鲁汶天主教大学开发的 CATHEDRAL 系统。

As logic synthesis tools matured and companies started commercializing them, it became apparent that VLSI design could not be started by conceptualizing systems in terms of logic-level primitives and entering large circuits by means of schematic 
capture systems. Architectural (or high-level) synthesis techniques that traced hack to the MIMOLA system at Honeywell and the ALERT systems at IBM became an important research subject, especially at Camegie-Mellon University, the University of Southern California and Carleton University. **The early architectural synthesis systems targeted instruction-set processor design and were not coupled to logic synthesis tools.** The first fully integrated synthesis systems were IBM's YORKTOWN SILICON COMPILER (YSC), GTFs SILC system and the CATHEDRAL systems developed at the Catholic University of Leuven, Belgium. 

随着逻辑综合工具的成熟和公司开始将它们商业化，很明显，VLSI设计不能通过逻辑级原语概念化系统和通过原理图进入大型电路来开始
捕获系统。 追溯到霍尼韦尔的 MIMOLA 系统和 IBM 的 ALERT 系统的架构（或高级）综合技术成为一个重要的研究课题，特别是在卡梅基梅隆大学、南加州大学和卡尔顿大学。 **早期的架构综合系统以指令集处理器设计为目标，并未与逻辑综合工具耦合。** 第一个完全集成的合成系统是 IBM 的 YORKTOWN SILICON COMPILER (YSC)、GTFs SILC 系统和比利时鲁汶天主教大学开发的 CATHEDRAL 系统。

At present, synthesis systems are common for circuit design at all levels. Commercial systems are available from vendors and research systems from universities  and research centers. Some companies have developed their own internal synthesis  systems, such as IBM, Digital Equipment Corporation, NEC, etc. Some synthesis  systems are described in Chapter 11. 

目前，综合系统普遍用于各级电路设计。 商业系统可从供应商处获得，研究系统可从大学和研究中心获得。 一些公司已经开发了自己的内部合成系统，例如 IBM、Digital Equipment Corporation、NEC 等。一些合成系统在第 11 章中进行了描述。