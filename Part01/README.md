<h1 align="center">PS3.1 总览</h1>

## 目录

* [声明](#notice-and-disclaimer)
* [前言](#foreword)
* 1.[适用范围和作用领域](#scope-and-field-of-application)
    * 1.1.[DICOM适用范围](#scope-of-dicom)
    * 1.2.[作用领域](#field-of-application)
    * 1.3.[历史](#history)
    * 1.4.[原则](#principles)
        * 1.4.1.[国际化和本地化](#global-applicability-and-localization)
        * 1.4.2.[持续维护](#continuous-maintenance)
        * 1.4.3.[信息对象和唯一对象识别](#information-objects-and-unique-object-identification)
        * 1.4.4.[一致性](#conformance)
        * 1.4.5.[信息模型的一致性](#consistency-of-information-model)

### <a name="notice-and-disclaimer"></a> 声明

本出版物的内容在文件制定时在技术上的合理性已经由编写和批准文件的人达成共识。共识并不意味着参与编写文档的每个人的意见是完全一致的。

本出版物是NEMA<sup>[[1](#nema)]</sup>标准和指导性出版物中的一员，符合自愿共识标准制定流程。这个流程将志愿者聚集起来并且寻找对本出版物所涵盖的主题感兴趣的人进行评审。虽然NEMA管理这个流程并且制定规则以促进本出版物共识开发中的公平性，但是它不会编写这个出版物，也不会独立测试，评估和验证它标准和指导性出版物的准确性和完整性。

NEMA对因发布，使用，应用或依赖本文档而直接或间接导致的任何性质的任何人身，财产或其他损害不承担任何责任，无论这些是特殊的，简洁的，后果性的还是补偿性的。NEMA对本出版物发表任何信息的准确定或完整性不作任何明确或者暗示性的担保或保证，并且不保证本出版物中的信息能够满足你任何特定目的或要求。NEMA不承诺任何根据此标准或指南的制造商或销售商的产品或者服务的性能。

在发布和提供此出版物时，NEMA不承诺为任何个人或者企业的代表提供专业或者其他的服务。NEMA也不承诺对任何人、企业或者其他履行任何义务。使用问出版物的任何人都应该依靠自己的独立判断，在适当的情况下，寻找合格的专业人员的建议，以确保在任何特殊情况下都能得到合理的使用。本出版物所涵盖有关该主题的信息和标准可以从其他地方获得，从这些地方用户可以咨询本出版物所未涵盖的信息。

NEMA没有任何权利，也不会承担任何责任或强制遵守本出版物中的内容。NEMA不会因安全或者健康目的对基于本出版物的产品，设计或者设备进行认证，测试或者检查。本出版物中任何与健康或者安全相关信息的认证和其他声明均不属于NEMA，并且完全由声明的认证者或指定者负责。

### <a name="foreword"></a> 前言

DICOM标准委员会是一个独立的、国际性的标准制定组织，由生物医学专业协会中专门负责医学成像，医学成像设备以及相关信息系统使用的部门、政府机构、行业协会以及其他对医学成像信息和相关数据的标准化感兴趣的标准制定组织组成。成员资格对所有委员会中有重大利益的组织开放。该委员会与医疗信息和医疗实工程中电气设备领域的其他组织合作紧密。委员会秘书处是美国国家电气制造商协会和它的医学影像和技术联盟部门。

委员会的主要产品是本标准：医疗数字影像传输协议 (DICOM)

DICOM标准使用基于 [ISO/IEC Directives, Part 2](#iso-iec-directives-part-2) 的指南构建的多部分文档。

该标准作为NEMA标准PS3初版，其部分按照NEMA出版物的格式进行编号(PS3.1, PS3.2等)。

DICOM&reg; 是美国国家电气制造商协会的注册商标，用于其医疗信息数字通信相关的标准出版物上保留所有权利。

HL7&reg; 和 CDA&reg; 是 Health Level Seven International 的注册商标，其保留所有权利。

SNOMED&reg;, SNOMED Clinical Terms&reg;, SNOMED CT&reg; 是 International Health Terminology Standards Development Organisation (IHTSDO) 的注册商标，其保留所有权利。

LOINC&reg; 是 Regenstrief Institute, Inc, 的注册商标，其保留所有权利。

### 1 <a name="scope-and-field-of-application"></a> 适用范围和作用领域

PS3.1 提供了医疗数字影像传输协议 (DICOM)的概述，包括其历史，范围，目标和结构。特别是它包括了该标准各个部分内容的简要说明。

#### <a name="scope-of-dicom"></a>1.1 DICOM的范围

医疗数字影像传输协议 (DICOM)是有关医疗影像信息和相关数据通信和管理的标准。

DICOM标准通过指定以下内容来促进医疗影像设备之间的互通性：

* 对于网络通信，定义一组协议，符合标准的设备都应当遵循。
    
* 使用以上协议可以交换命令和相关信息的语法和语义。

* 对于媒体通信，定义一组媒体存储服务，符合标准的设备都应当遵循。同时定义一种文件格式和医疗目录结构以便于访问交换媒体上的影像和相关信息。

* 必须提供包括符合标准的实现方案的信息。

DICOM标准不包括以下内容：

* 标准中任何功能的实现细节。

* DICOM标准设备组成的系统预期的整体特征和功能。

* 标准评估相关的测试和验证流程。

### 2 <a name="normative-references"></a> 其他标准的参考文献

<a name="iso-iec-directives-part-2"></a>[ISO/IEC Directives, Part 2] ISO/IEC. 2016/05. 7.0. Rules for the structure and drafting of International Standards. [http://www.iec.ch/members_experts/refdocs/iec/isoiecdir-2%7Bed7.0%7Den.pdf](http://www.iec.ch/members_experts/refdocs/iec/isoiecdir-2%7Bed7.0%7Den.pdf).

## 译者注

[1] <a name="nema">NEMA</a>: 美国国家电气制造商协会
