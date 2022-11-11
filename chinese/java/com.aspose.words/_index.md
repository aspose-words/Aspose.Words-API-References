---
title: com.aspose.words
second_title: Aspose.Words for Java API Reference
description: com.aspose.words 包提供了在不使用 Microsoft Word 的情况下生成转换、修改渲染和打印 Microsoft Word 文档的类。
type: docs
weight: 10
url: /zh/java/com.aspose.words/
---


这**com.aspose.words**包提供了在不使用 Microsoft Word 的情况下生成、转换、修改、呈现和打印 Microsoft Word 文档的类。

Aspose.Words 完全用 Java 编写。使用 Aspose.Words 不需要 Microsoft Word。

课程中的**com.aspose.words**包借鉴了两个著名框架的最佳实践：Microsoft Word Automation 和 System.Xml。 Aspose.Words 中的文档由节点树表示，与 XML DOM 非常相似。在可能的情况下，类、方法和属性名称与 Microsoft Word Automation 中的名称相匹配。

此命名空间中的主要类是：

 *  **Document**是表示 Microsoft Word 文档的对象模型的主要类。
 *  **DocumentBuilder**提供了一种将内容和格式插入文档的简单方法。
 *  **Node**是文档中所有节点的基类。
 *  **CompositeNode**是可以包含其他节点的文档的所有节点的基类，例如**Paragraph**, **Section**和**Table**和 。

这**com.aspose.words**包还包含构成 Aspose.Words 报告引擎的类。报告引擎允许使用来自各种数据源的数据快速轻松地填充在 Microsoft Word 中设计的文档，例如**java.sql.ResultSet**, **array of ResultSets**, **com.aspose.words.net.System.Data.DataSet**或一个**array of values**.

这**MailMerge**提供对报告功能的访问的对象可通过**Document.MailMerge**财产。


## 课程

| 班级 | 描述 |
| --- | --- |
| [AbsolutePositionTab](../com.aspose.words/absolutepositiontab) | 绝对位置制表符是一个字符，用于在显示此 WordprocessingML 内容时在当前文本行上推进位置。 |
| [ArrowLength](../com.aspose.words/arrowlength) | 行尾箭头的长度。 |
| [Arrow类型](../com.aspose.words/arrowtype) | 指定线端的箭头类型。 |
| [ArrowWidth](../com.aspose.words/arrowwidth) | 行尾箭头的宽度。 |
| [AsposeWordsPrintDocument](../com.aspose.words/asposewordsprintdocument) | 提供打印的默认实现[Document](../com.aspose.words/document)在 Java 打印框架内。 |
| [AutoFitBehavior](../com.aspose.words/autofitbehavior) | 确定 Aspose.Words 在您调用**M:Aspose.Words.Tables.Table.AutoFit(Aspose.Words.Tables.AutoFitBehavior)**方法。 |
| [AxisBound](../com.aspose.words/axisbound) | 表示轴值的最小或最大界限。 |
| [AxisBuiltInUnit](../com.aspose.words/axisbuiltinunit) | 指定轴的显示单位。 |
| [AxisCategory类型](../com.aspose.words/axiscategorytype) | 指定类别轴的类型。 |
| [AxisCrosses](../com.aspose.words/axiscrosses) | 指定轴的可能交叉点。 |
| [AxisDisplayUnit](../com.aspose.words/axisdisplayunit) | 提供对数值轴显示单位的缩放选项的访问。 |
| [AxisScale类型](../com.aspose.words/axisscaletype) | 指定轴的可能比例类型。 |
| [AxisScaling](../com.aspose.words/axisscaling) | 表示轴的缩放选项。 |
| [AxisTickLabelPosition](../com.aspose.words/axisticklabelposition) | 指定刻度标签的可能位置。 |
| [AxisTickMark](../com.aspose.words/axistickmark) | 指定刻度线的可能位置。 |
| [AxisTimeUnit](../com.aspose.words/axistimeunit) | 指定轴的时间单位。 |
| [Barcode参数](../com.aspose.words/barcodeparameters) | 用于将条码参数传递给 BarcodeGenerator 的容器类。 |
| [BaseWebExtensionCollection](../com.aspose.words/basewebextensioncollection) | 基类[TaskPaneCollection](../com.aspose.words/taskpanecollection), [WebExtensionBindingCollection](../com.aspose.words/webextensionbindingcollection), [WebExtensionPropertyCollection](../com.aspose.words/webextensionpropertycollection)和[WebExtensionReferenceCollection](../com.aspose.words/webextensionreferencecollection)收藏品。 |
| [BasicTextShaperCache](../com.aspose.words/basictextshapercache) |  |
| [BlockImportMode](../com.aspose.words/blockimportmode) | 指定如何从基于 HTML 的文档中导入块级元素的属性。 |
| [Body](../com.aspose.words/body) | 表示部分正文的容器。 |
| [Bookmark](../com.aspose.words/bookmark) | 表示单个书签。 |
| [BookmarkCollection](../com.aspose.words/bookmarkcollection) | 一个集合[Bookmark](../com.aspose.words/bookmark)表示指定范围内的书签的对象。 |
| [BookmarkEnd](../com.aspose.words/bookmarkend) | 表示 Word 文档中书签的结尾。 |
| [BookmarkStart](../com.aspose.words/bookmarkstart) | 表示 Word 文档中书签的开始。 |
| [BookmarksOutlineLevelCollection](../com.aspose.words/bookmarksoutlinelevelcollection) | 单个书签大纲级别的集合。 |
| [Border](../com.aspose.words/border) | 表示对象的边框。 |
| [BorderCollection](../com.aspose.words/bordercollection) | 边框对象的集合。 |
| [Border类型](../com.aspose.words/bordertype) | 指定边框的边。 |
| [Break类型](../com.aspose.words/breaktype) | 指定文档中的中断类型。 |
| [BuildVersionInfo](../com.aspose.words/buildversioninfo) | 提供有关当前产品名称和版本的信息。 |
| [BuildingBlock](../com.aspose.words/buildingblock) | 表示词汇表文档条目，例如 Building Block、自动图文集或自动更正条目。 |
| [BuildingBlockBehavior](../com.aspose.words/buildingblockbehavior) | 指定在将构建块插入主文档时应应用于构建块内容的行为。 |
| [BuildingBlockCollection](../com.aspose.words/buildingblockcollection) | 一个集合[BuildingBlock](../com.aspose.words/buildingblock)文档中的对象。 |
| [BuildingBlockGallery](../com.aspose.words/buildingblockgallery) | 指定构建块分类到的预定义库。 |
| [BuildingBlock类型](../com.aspose.words/buildingblocktype) | 指定构建块类型。 |
| [BuiltInDocumentProperties](../com.aspose.words/builtindocumentproperties) | 内置文档属性的集合。 |
| [Calendar类型](../com.aspose.words/calendartype) | 指定日历的类型。 |
| [Cell](../com.aspose.words/cell) | 表示表格单元格。 |
| [CellCollection](../com.aspose.words/cellcollection) | 提供对集合的类型化访问[Cell](../com.aspose.words/cell)节点。 |
| [CellFormat](../com.aspose.words/cellformat) | 表示表格单元格的所有格式。 |
| [CellMerge](../com.aspose.words/cellmerge) | 指定表格中的单元格如何与其他单元格合并。 |
| [CellVerticalAlignment](../com.aspose.words/cellverticalalignment) | 指定表格单元格内文本的垂直对齐方式。 |
| [CertificateHolder](../com.aspose.words/certificateholder) | 代表持有人**X509Certificate2**实例。 |
| [ChapterPageSeparator](../com.aspose.words/chapterpageseparator) | 定义出现在章节和页码之间的分隔符。 |
| [Chart](../com.aspose.words/chart) | 提供对图表形状属性的访问。 |
| [ChartAxis](../com.aspose.words/chartaxis) | 表示图表的轴选项。 |
| [ChartAxis类型](../com.aspose.words/chartaxistype) | 指定图表轴的类型。 |
| [ChartDataLabel](../com.aspose.words/chartdatalabel) | 表示图表点或趋势线上的数据标签。 |
| [ChartDataLabelCollection](../com.aspose.words/chartdatalabelcollection) | 代表一个集合[ChartDataLabel](../com.aspose.words/chartdatalabel). |
| [ChartDataPoint](../com.aspose.words/chartdatapoint) | 允许指定图表上单个数据点的格式。 |
| [ChartDataPointCollection](../com.aspose.words/chartdatapointcollection) | 代表一个集合[ChartDataPoint](../com.aspose.words/chartdatapoint). |
| [ChartFormat](../com.aspose.words/chartformat) | 表示图表元素的格式。 |
| [ChartLegend](../com.aspose.words/chartlegend) | 表示图表图例属性。 |
| [ChartLegendEntry](../com.aspose.words/chartlegendentry) | 表示图表图例条目。 |
| [ChartLegendEntryCollection](../com.aspose.words/chartlegendentrycollection) | 表示图表图例条目的集合。 |
| [ChartMarker](../com.aspose.words/chartmarker) | 表示图表数据标记。 |
| [ChartNumberFormat](../com.aspose.words/chartnumberformat) | 表示父元素的数字格式。 |
| [ChartSeries](../com.aspose.words/chartseries) | 表示图表系列属性。 |
| [ChartSeriesCollection](../com.aspose.words/chartseriescollection) | 代表一个集合[ChartSeries](../com.aspose.words/chartseries). |
| [ChartTitle](../com.aspose.words/charttitle) | 提供对图表标题属性的访问。 |
| [Chart类型](../com.aspose.words/charttype) | 指定图表的类型。 |
| [ChmLoadOptions](../com.aspose.words/chmloadoptions) | 允许在将 CHM 文档加载到[Document](../com.aspose.words/document)目的。 |
| [CleanupOptions](../com.aspose.words/cleanupoptions) | 允许指定文档清理选项。 |
| [Cluster](../com.aspose.words/cluster) |  |
| [ColorMode](../com.aspose.words/colormode) | 指定如何呈现颜色。 |
| [Comment](../com.aspose.words/comment) | 表示注释文本的容器。 |
| [CommentCollection](../com.aspose.words/commentcollection) | 提供对集合的类型化访问[Comment](../com.aspose.words/comment)节点。 |
| [CommentDisplayMode](../com.aspose.words/commentdisplaymode) | 指定文档注释的呈现模式。 |
| [CommentRangeEnd](../com.aspose.words/commentrangeend) | 表示具有与之关联的注释的文本区域的结尾。 |
| [CommentRangeStart](../com.aspose.words/commentrangestart) | 表示具有关联注释的文本区域的开始。 |
| [CompareOptions](../com.aspose.words/compareoptions) | 允许选择文档比较操作的高级选项。 |
| [ComparisonEvaluationResult](../com.aspose.words/comparisonevaluationresult) | 比较评价结果。 |
| [ComparisonExpression](../com.aspose.words/comparisonexpression) | 比较表达式。 |
| [ComparisonTarget类型](../com.aspose.words/comparisontargettype) | 允许指定将在比较期间使用的基本文档。 |
| [Compatibility](../com.aspose.words/compatibility) | 指定兼容性选项的名称。 |
| [CompatibilityOptions](../com.aspose.words/compatibilityoptions) | 包含兼容性选项（即，在**Compatibility**的选项卡**Options**Microsoft Word 中的对话框）。 |
| [CompositeNode](../com.aspose.words/compositenode) | 可以包含其他节点的节点的基类。 |
| [CompressionLevel](../com.aspose.words/compressionlevel) | OOXML 文件的压缩级别。 |
| [ConditionalStyle](../com.aspose.words/conditionalstyle) | 表示应用于具有指定表格样式的表格的某些区域的特殊格式。 |
| [ConditionalStyleCollection](../com.aspose.words/conditionalstylecollection) | 代表一个集合[ConditionalStyle](../com.aspose.words/conditionalstyle)对象。 |
| [ConditionalStyle类型](../com.aspose.words/conditionalstyletype) | 表示可以在表格样式中定义条件格式的可能表格区域。 |
| [ContentDisposition](../com.aspose.words/contentdisposition) | 枚举在客户端浏览器上呈现文档的不同方式。 |
| [ContinuousSectionRestart](../com.aspose.words/continuoussectionrestart) | 表示在重新开始页码的连续部分中计算页码时的不同行为。 |
| [ControlChar](../com.aspose.words/controlchar) | 控制字符在文档中经常遇到。 |
| [ConvertUtil](../com.aspose.words/convertutil) | 提供帮助函数以在各种测量单位之间进行转换。 |
| [CssSavingArgs](../com.aspose.words/csssavingargs) | 提供数据为[ICssSavingCallback.\#cssSaving(com.aspose.words.CssSavingArgs)](../com.aspose.words/icsssavingcallback\#cssSaving-com.aspose.words.CssSavingArgs-)事件。 |
| [CssStyleSheet类型](../com.aspose.words/cssstylesheettype) | 指定如何将 CSS（层叠样式表）样式导出为 HTML。 |
| [CsvDataLoadOptions](../com.aspose.words/csvdataloadoptions) | 表示用于解析 CSV 数据的选项。 |
| [CsvDataSource](../com.aspose.words/csvdatasource) | 提供对要在报告中使用的 CSV 文件或流的数据的访问。 |
| [CurrentThreadSettings](../com.aspose.words/currentthreadsettings) | 此类有助于为 Aspose.Words 应用程序设置线程隔离的区域设置和时区。 |
| [CustomDocumentProperties](../com.aspose.words/customdocumentproperties) | 自定义文档属性的集合。 |
| [CustomPart](../com.aspose.words/custompart) | 表示 ISO/IEC 29500 标准未定义的自定义（任意内容）部分。 |
| [CustomPartCollection](../com.aspose.words/custompartcollection) | 代表一个集合[CustomPart](../com.aspose.words/custompart)对象。 |
| [CustomXmlPart](../com.aspose.words/customxmlpart) | 表示自定义 XML 数据存储部件（包中的自定义 XML 数据）。 |
| [CustomXmlPartCollection](../com.aspose.words/customxmlpartcollection) | 表示自定义 XML 部件的集合。 |
| [CustomXmlProperty](../com.aspose.words/customxmlproperty) | 表示单个自定义 XML 属性或智能标记属性。 |
| [CustomXmlPropertyCollection](../com.aspose.words/customxmlpropertycollection) | 表示自定义 XML 属性或智能标记属性的集合。 |
| [CustomXmlSchemaCollection](../com.aspose.words/customxmlschemacollection) | 表示与自定义 XML 部件关联的 XML 模式的字符串集合。 |
| [DashStyle](../com.aspose.words/dashstyle) | 虚线样式。 |
| [DefaultFontSubstitutionRule](../com.aspose.words/defaultfontsubstitutionrule) | 默认字体替换规则。 |
| [DigitalSignature](../com.aspose.words/digitalsignature) | 表示文档上的数字签名及其验证结果。 |
| [DigitalSignatureCollection](../com.aspose.words/digitalsignaturecollection) | 提供附加到文档的数字签名的只读集合。 |
| [DigitalSignature类型](../com.aspose.words/digitalsignaturetype) | 指定数字签名的类型。 |
| [DigitalSignatureUtil](../com.aspose.words/digitalsignatureutil) | 提供签署文件的方法。 |
| [Direction](../com.aspose.words/direction) |  |
| [Dml3DEffectsRenderingMode](../com.aspose.words/dml3deffectsrenderingmode) | 指定如何渲染 3D 形状效果。 |
| [DmlEffectsRenderingMode](../com.aspose.words/dmleffectsrenderingmode) | 指定如何将 DrawingML 效果呈现为固定页面格式。 |
| [DmlRenderingMode](../com.aspose.words/dmlrenderingmode) | 指定如何将 DrawingML 形状呈现为固定页面格式。 |
| [DocSaveOptions](../com.aspose.words/docsaveoptions) | 可用于在将文档保存到[SaveFormat.\#DOC](../com.aspose.words/saveformat\#DOC)或者[SaveFormat.\#DOT](../com.aspose.words/saveformat\#DOT)格式。 |
| [Document](../com.aspose.words/document) | 表示 Word 文档。 |
| [DocumentBase](../com.aspose.words/documentbase) | 为 Word 文档的主文档和词汇表文档提供抽象基类。 |
| [DocumentBuilder](../com.aspose.words/documentbuilder) | 提供插入文本、图像和其他内容、指定字体、段落和部分格式的方法。 |
| [DocumentDirection](../com.aspose.words/documentdirection) | 允许指定文档中文本的流动方向。 |
| [DocumentLoadingArgs](../com.aspose.words/documentloadingargs) | 传入的参数[IDocumentLoadingCallback.\#notify(com.aspose.words.DocumentLoadingArgs)](../com.aspose.words/idocumentloadingcallback\#notify-com.aspose.words.DocumentLoadingArgs-). |
| [DocumentPartSavingArgs](../com.aspose.words/documentpartsavingargs) | 提供数据为[IDocumentPartSavingCallback.\#documentPartSaving(com.aspose.words.DocumentPartSavingArgs)](../com.aspose.words/idocumentpartsavingcallback\#documentPartSaving-com.aspose.words.DocumentPartSavingArgs-)打回来。 |
| [DocumentProperty](../com.aspose.words/documentproperty) | 表示自定义或内置文档属性。 |
| [DocumentPropertyCollection](../com.aspose.words/documentpropertycollection) | 基类[BuiltInDocumentProperties](../com.aspose.words/builtindocumentproperties)和[CustomDocumentProperties](../com.aspose.words/customdocumentproperties)收藏品。 |
| [DocumentReaderPluginLoadException](../com.aspose.words/documentreaderpluginloadexception) | 在文档加载过程中，无法加载读取文档格式所需的插件时抛出。 |
| [DocumentSavingArgs](../com.aspose.words/documentsavingargs) | 传入的参数[IDocumentSavingCallback.\#notify(com.aspose.words.DocumentSavingArgs)](../com.aspose.words/idocumentsavingcallback\#notify-com.aspose.words.DocumentSavingArgs-). |
| [DocumentSecurity](../com.aspose.words/documentsecurity) | 用作[BuiltInDocumentProperties.\#getSecurity()](../com.aspose.words/builtindocumentproperties\#getSecurity--) / [BuiltInDocumentProperties.\#setSecurity(int)](../com.aspose.words/builtindocumentproperties\#setSecurity-int-)财产。 |
| [DocumentSplitCriteria](../com.aspose.words/documentsplitcriteria) | 指定保存到时如何将文档拆分为多个部分[SaveFormat.\#HTML](../com.aspose.words/saveformat\#HTML), [SaveFormat.\#EPUB](../com.aspose.words/saveformat\#EPUB)或者[SaveFormat.\#AZW\_3](../com.aspose.words/saveformat\#AZW-3)格式。 |
| [DocumentVisitor](../com.aspose.words/documentvisitor) | 自定义文档访问者的基类。 |
| [DownsampleOptions](../com.aspose.words/downsampleoptions) | 允许指定下采样选项。 |
| [DropCapPosition](../com.aspose.words/dropcapposition) | 指定首字下沉文本的位置。 |
| [DropDownItemCollection](../com.aspose.words/dropdownitemcollection) | 表示下拉表单字段中所有项目的字符串集合。 |
| [EditableRange](../com.aspose.words/editablerange) | 表示单个可编辑范围。 |
| [EditableRangeEnd](../com.aspose.words/editablerangeend) | 表示 Word 文档中可编辑范围的结束。 |
| [EditableRangeStart](../com.aspose.words/editablerangestart) | 表示 Word 文档中可编辑范围的开始。 |
| [EditingLanguage](../com.aspose.words/editinglanguage) | 指定编辑语言。 |
| [Editor类型](../com.aspose.words/editortype) | 指定一组可能的别名（或编辑组），可用作别名以确定是否允许当前用户编辑由文档内的可编辑范围定义的单个范围。 |
| [EmbeddedFontFormat](../com.aspose.words/embeddedfontformat) | 指定内部特定嵌入字体的格式[FontInfo](../com.aspose.words/fontinfo)目的。 |
| [EmbeddedFontStyle](../com.aspose.words/embeddedfontstyle) | 指定嵌入字体的样式[FontInfo](../com.aspose.words/fontinfo)目的。 |
| [EmfPlusDualRenderingMode](../com.aspose.words/emfplusdualrenderingmode) | 指定 Aspose.Words 应如何呈现 EMF+ Dual 元文件。 |
| [EmphasisMark](../com.aspose.words/emphasismark) | 指定可能的强调标记类型。 |
| [EndCap](../com.aspose.words/endcap) | 指定线帽样式。 |
| [EndnoteOptions](../com.aspose.words/endnoteoptions) | 表示文档或部分的尾注编号选项。 |
| [EndnotePosition](../com.aspose.words/endnoteposition) | 定义尾注位置。 |
| [ExportFontFormat](../com.aspose.words/exportfontformat) | 指示在呈现为 HTML 固定格式时用于导出字体的格式。 |
| [ExportHeadersFootersMode](../com.aspose.words/exportheadersfootersmode) | 指定页眉和页脚如何导出为 HTML、MHTML 或 EPUB。 |
| [ExportListLabels](../com.aspose.words/exportlistlabels) | 指定如何将列表标签导出为 HTML、MHTML 和 EPUB。 |
| [字段](../com.aspose.words/field) | 表示 Microsoft Word 文档字段。 |
| [字段AddIn](../com.aspose.words/fieldaddin) | 实现 ADDIN 字段。 |
| [字段AddressBlock](../com.aspose.words/fieldaddressblock) | 实现 ADDRESSBLOCK 字段。 |
| [字段Advance](../com.aspose.words/fieldadvance) | 实现 ADVANCE 字段。 |
| [字段ArgumentBuilder](../com.aspose.words/fieldargumentbuilder) | 构建由字段、节点和纯文本组成的复杂字段参数。 |
| [字段Ask](../com.aspose.words/fieldask) | 实现 ASK 字段。 |
| [字段Author](../com.aspose.words/fieldauthor) | 实现 AUTHOR 字段。 |
| [字段AutoNum](../com.aspose.words/fieldautonum) | 实现 AUTONUM 字段。 |
| [字段AutoNumLgl](../com.aspose.words/fieldautonumlgl) | 实现 AUTONUMLGL 字段。 |
| [字段AutoNumOut](../com.aspose.words/fieldautonumout) | 实现 AUTONUMOUT 字段。 |
| [字段AutoText](../com.aspose.words/fieldautotext) | 实现自动文本字段。 |
| [字段AutoTextList](../com.aspose.words/fieldautotextlist) | 实现 AUTOTEXTLIST 字段。 |
| [字段Barcode](../com.aspose.words/fieldbarcode) | 实现 BARCODE 字段。 |
| [字段Bibliography](../com.aspose.words/fieldbibliography) | 实现书目字段。 |
| [字段BidiOutline](../com.aspose.words/fieldbidioutline) | 实现 BIDIOUTLINE 字段。 |
| [字段Builder](../com.aspose.words/fieldbuilder) | 从域代码标记（参数和开关）构建一个域。 |
| [字段Char](../com.aspose.words/fieldchar) | 表示文档中字段字符的节点的基类。 |
| [字段Citation](../com.aspose.words/fieldcitation) | 实现 CITATION 字段。 |
| [字段Collection](../com.aspose.words/fieldcollection) | 一个集合[字段](../com.aspose.words/field)表示指定范围内的字段的对象。 |
| [字段Comments](../com.aspose.words/fieldcomments) | 实现 COMMENTS 字段。 |
| [字段Compare](../com.aspose.words/fieldcompare) | 实现 COMPARE 字段。 |
| [字段CreateDate](../com.aspose.words/fieldcreatedate) | 实现 CREATEDATE 字段。 |
| [字段Data](../com.aspose.words/fielddata) | 实现 DATA 字段。 |
| [字段Database](../com.aspose.words/fielddatabase) | 实现 DATABASE 字段。 |
| [字段DatabaseDataRow](../com.aspose.words/fielddatabasedatarow) | 提供数据为[字段Database](../com.aspose.words/fielddatabase)场结果。 |
| [字段DatabaseDataTable](../com.aspose.words/fielddatabasedatatable) | 提供数据为[字段Database](../com.aspose.words/fielddatabase)场结果。 |
| [字段Date](../com.aspose.words/fielddate) | 实现 DATE 字段。 |
| [字段Dde](../com.aspose.words/fielddde) | 实现 DDE 字段。 |
| [字段DdeAuto](../com.aspose.words/fieldddeauto) | 实现 DDEAUTO 字段。 |
| [字段DisplayBarcode](../com.aspose.words/fielddisplaybarcode) | 实现 DISPLAYBARCODE 字段。 |
| [字段DocProperty](../com.aspose.words/fielddocproperty) | 实现 DOCPROPERTY 字段。 |
| [字段DocVariable](../com.aspose.words/fielddocvariable) | 实现 DOCVARIABLE 字段。 |
| [字段EQ](../com.aspose.words/fieldeq) | 实现 EQ 字段。 |
| [字段EditTime](../com.aspose.words/fieldedittime) | 实现 EDITTIME 字段。 |
| [字段Embed](../com.aspose.words/fieldembed) | 实现 EMBED 字段。 |
| [字段End](../com.aspose.words/fieldend) | 表示文档中 Word 字段的结尾。 |
| [字段FileName](../com.aspose.words/fieldfilename) | 实现 FILENAME 字段。 |
| [字段FileSize](../com.aspose.words/fieldfilesize) | 实现 FILESIZE 字段。 |
| [字段FillIn](../com.aspose.words/fieldfillin) | 实现 FILLIN 字段。 |
| [字段FootnoteRef](../com.aspose.words/fieldfootnoteref) | 实现 FOOTNOTEREF 字段。 |
| [字段FormCheckBox](../com.aspose.words/fieldformcheckbox) | 实现 FORMCHECKBOX 字段。 |
| [字段FormDropDown](../com.aspose.words/fieldformdropdown) | 实现 FORMDROPDOWN 字段。 |
| [字段FormText](../com.aspose.words/fieldformtext) | 实现 FORMTEXT 字段。 |
| [字段Format](../com.aspose.words/fieldformat) | 提供对字段的数字、日期和时间以及一般格式的键入访问。 |
| [字段Formula](../com.aspose.words/fieldformula) | 实现 =（公式）字段。 |
| [字段Glossary](../com.aspose.words/fieldglossary) | 实现 GLOSSARY 字段。 |
| [字段GoToButton](../com.aspose.words/fieldgotobutton) | 实现 GOTOBUTTON 字段。 |
| [字段GreetingLine](../com.aspose.words/fieldgreetingline) | 实现 GREETINGLINE 字段。 |
| [字段Hyperlink](../com.aspose.words/fieldhyperlink) | 实现 HYPERLINK 字段 |
| [字段If](../com.aspose.words/fieldif) | 实现 IF 字段。 |
| [字段IfComparisonResult](../com.aspose.words/fieldifcomparisonresult) | 指定 IF 字段条件评估的结果。 |
| [字段Import](../com.aspose.words/fieldimport) | 实现 IMPORT 字段。 |
| [字段Include](../com.aspose.words/fieldinclude) | 实现 INCLUDE 字段。 |
| [字段IncludePicture](../com.aspose.words/fieldincludepicture) | 实现 INCLUDEPICTURE 字段。 |
| [字段IncludeText](../com.aspose.words/fieldincludetext) | 实现 INCLUDETEXT 字段。 |
| [字段Index](../com.aspose.words/fieldindex) | 实现 INDEX 字段。 |
| [字段IndexFormat](../com.aspose.words/fieldindexformat) | 指定格式[字段Index](../com.aspose.words/fieldindex)文档中的字段。 |
| [字段Info](../com.aspose.words/fieldinfo) | 实现 INFO 字段。 |
| [字段Keywords](../com.aspose.words/fieldkeywords) | 实现 KEYWORDS 字段。 |
| [字段LastSavedBy](../com.aspose.words/fieldlastsavedby) | 实现 LASTSAVEDBY 字段。 |
| [字段Link](../com.aspose.words/fieldlink) | 实现 LINK 字段。 |
| [字段ListNum](../com.aspose.words/fieldlistnum) | 实现 LISTNUM 字段。 |
| [字段MacroButton](../com.aspose.words/fieldmacrobutton) | 实现 MACROBUTTON 字段。 |
| [字段MergeBarcode](../com.aspose.words/fieldmergebarcode) | 实现 MERGEBARCODE 字段。 |
| [字段Merge字段](../com.aspose.words/fieldmergefield) | 实现 MERGEFIELD 字段。 |
| [字段MergeRec](../com.aspose.words/fieldmergerec) | 实现 MERGEREC 字段。 |
| [字段MergeSeq](../com.aspose.words/fieldmergeseq) | 实现 MERGESEQ 字段。 |
| [字段MergingArgs](../com.aspose.words/fieldmergingargs) | 提供数据为**Merge字段**事件。 |
| [字段MergingArgsBase](../com.aspose.words/fieldmergingargsbase) | 基类[字段MergingArgs](../com.aspose.words/fieldmergingargs)和[Image字段MergingArgs](../com.aspose.words/imagefieldmergingargs). |
| [字段Next](../com.aspose.words/fieldnext) | 实现 NEXT 字段。 |
| [字段NextIf](../com.aspose.words/fieldnextif) | 实现 NEXTIF 字段。 |
| [字段NoteRef](../com.aspose.words/fieldnoteref) | 实现 NOTEREF 字段。 |
| [字段NumChars](../com.aspose.words/fieldnumchars) | 实现 NUMCHARS 字段。 |
| [字段NumPages](../com.aspose.words/fieldnumpages) | 实现 NUMPAGES 字段。 |
| [字段NumWords](../com.aspose.words/fieldnumwords) | 实现 NUMWORDS 字段。 |
| [字段Ocx](../com.aspose.words/fieldocx) | 实现 OCX 字段。 |
| [字段Options](../com.aspose.words/fieldoptions) | 表示用于控制文档中的字段处理的选项。 |
| [字段Page](../com.aspose.words/fieldpage) | 实现 PAGE 字段。 |
| [字段PageRef](../com.aspose.words/fieldpageref) | 实现 PAGEREF 字段。 |
| [字段Print](../com.aspose.words/fieldprint) | 实现 PRINT 字段。 |
| [字段PrintDate](../com.aspose.words/fieldprintdate) | 实现 PRINTDATE 字段。 |
| [字段Private](../com.aspose.words/fieldprivate) | 实现 PRIVATE 字段。 |
| [字段Quote](../com.aspose.words/fieldquote) | 实现 QUOTE 字段。 |
| [字段RD](../com.aspose.words/fieldrd) | 实现 RD 字段。 |
| [字段Ref](../com.aspose.words/fieldref) | 实现 REF 字段。 |
| [字段RevNum](../com.aspose.words/fieldrevnum) | 实现 REVNUM 字段。 |
| [字段SaveDate](../com.aspose.words/fieldsavedate) | 实现 SAVEDATE 字段。 |
| [字段Section](../com.aspose.words/fieldsection) | 实现 SECTION 字段。 |
| [字段SectionPages](../com.aspose.words/fieldsectionpages) | 实现 SECTIONPAGES 字段。 |
| [字段Separator](../com.aspose.words/fieldseparator) | 表示将域代码与域结果分开的 Word 域分隔符。 |
| [字段Seq](../com.aspose.words/fieldseq) | 实现 SEQ 字段。 |
| [字段Set](../com.aspose.words/fieldset) | 实现 SET 字段。 |
| [字段Shape](../com.aspose.words/fieldshape) | 实现 SHAPE 字段。 |
| [字段SkipIf](../com.aspose.words/fieldskipif) | 实现 SKIPIF 字段。 |
| [字段Start](../com.aspose.words/fieldstart) | 表示文档中 Word 字段的开始。 |
| [字段StyleRef](../com.aspose.words/fieldstyleref) | 实现 STYLEREF 字段。 |
| [字段Subject](../com.aspose.words/fieldsubject) | 实现 SUBJECT 字段。 |
| [字段Symbol](../com.aspose.words/fieldsymbol) | 实现一个符号字段。 |
| [字段TA](../com.aspose.words/fieldta) | 实现 TA 字段。 |
| [字段TC](../com.aspose.words/fieldtc) | 实现 TC 字段。 |
| [字段Template](../com.aspose.words/fieldtemplate) | 实现 TEMPLATE 字段。 |
| [字段Time](../com.aspose.words/fieldtime) | 实现 TIME 字段。 |
| [字段Title](../com.aspose.words/fieldtitle) | 实现 TITLE 字段。 |
| [字段Toa](../com.aspose.words/fieldtoa) | 实现 TOA 字段。 |
| [字段Toc](../com.aspose.words/fieldtoc) | 实现 TOC 字段。 |
| [字段类型](../com.aspose.words/fieldtype) | 指定 Microsoft Word 字段类型。 |
| [字段Unknown](../com.aspose.words/fieldunknown) | 实现未知或无法识别的字段。 |
| [字段UpdateCultureSource](../com.aspose.words/fieldupdateculturesource) | 指示在字段更新期间要使用的区域性。 |
| [字段UserAddress](../com.aspose.words/fielduseraddress) | 实现 USERADDRESS 字段。 |
| [字段UserInitials](../com.aspose.words/fielduserinitials) | 实现 USERINITIALS 字段。 |
| [字段UserName](../com.aspose.words/fieldusername) | 实现 USERNAME 字段。 |
| [字段XE](../com.aspose.words/fieldxe) | 实现 XE 字段。 |
| [FileCorruptedException](../com.aspose.words/filecorruptedexception) | 在文档加载过程中，当文档似乎已损坏且无法加载时抛出。 |
| [FileFontSource](../com.aspose.words/filefontsource) | 表示存储在文件系统中的单个 True类型 字体文件。 |
| [FileFormatInfo](../com.aspose.words/fileformatinfo) | 包含由返回的数据[FileFormatUtil](../com.aspose.words/fileformatutil)文档格式检测方法。 |
| [FileFormatUtil](../com.aspose.words/fileformatutil) | 提供用于处理文件格式的实用方法，例如检测文件格式或将文件扩展名转换为/从文件格式枚举。 |
| [Fill](../com.aspose.words/fill) | 表示对象的填充格式。 |
| [Fill类型](../com.aspose.words/filltype) | 指定可填充对象的填充类型。 |
| [FindReplaceDirection](../com.aspose.words/findreplacedirection) | 指定替换操作的方向。 |
| [FindReplaceOptions](../com.aspose.words/findreplaceoptions) | 指定查找/替换操作的选项。 |
| [FipsUnapprovedOperationException](../com.aspose.words/fipsunapprovedoperationexception) |  |
| [FixedPageSaveOptions](../com.aspose.words/fixedpagesaveoptions) | 包含在将文档保存为固定页面格式（PDF、XPS、图像等）时可以指定的常用选项。 |
| [FlipOrientation](../com.aspose.words/fliporientation) | 形状方向的可能值。 |
| [FolderFontSource](../com.aspose.words/folderfontsource) | 表示包含 True类型 字体文件的文件夹。 |
| [Font](../com.aspose.words/font) | 包含对象的字体属性（字体名称、字体大小、颜色等）。 |
| [FontConfigSubstitutionRule](../com.aspose.words/fontconfigsubstitutionrule) | 字体配置替换规则。 |
| [FontFallbackSettings](../com.aspose.words/fontfallbacksettings) | 指定字体回退机制设置。 |
| [FontFamily](../com.aspose.words/fontfamily) | 表示字体系列。 |
| [FontFeature](../com.aspose.words/fontfeature) |  |
| [FontInfo](../com.aspose.words/fontinfo) | 指定有关文档中使用的字体的信息。 |
| [FontInfoCollection](../com.aspose.words/fontinfocollection) | 表示文档中使用的字体集合。 |
| [FontInfoSubstitutionRule](../com.aspose.words/fontinfosubstitutionrule) | 字体信息替换规则。 |
| [FontNameSubstitutionRule](../com.aspose.words/fontnamesubstitutionrule) | 处理字体名称的字体替换规则。 |
| [FontPitch](../com.aspose.words/fontpitch) | 表示字体间距。 |
| [FontSavingArgs](../com.aspose.words/fontsavingargs) | 提供数据为[IFontSavingCallback.\#fontSaving(com.aspose.words.FontSavingArgs)](../com.aspose.words/ifontsavingcallback\#fontSaving-com.aspose.words.FontSavingArgs-)事件。 |
| [FontSettings](../com.aspose.words/fontsettings) | 指定文档的字体设置。 |
| [FontSourceBase](../com.aspose.words/fontsourcebase) | 这是允许用户指定各种字体源的类的抽象基类。 |
| [FontSource类型](../com.aspose.words/fontsourcetype) | 指定字体源的类型。 |
| [FontSubstitutionRule](../com.aspose.words/fontsubstitutionrule) | 这是字体替换规则的抽象基类。 |
| [FontSubstitutionSettings](../com.aspose.words/fontsubstitutionsettings) | 指定字体替换机制设置。 |
| [Footnote](../com.aspose.words/footnote) | 表示脚注或尾注文本的容器。 |
| [FootnoteNumberingRule](../com.aspose.words/footnotenumberingrule) | 确定自动脚注或尾注编号何时重新开始。 |
| [FootnoteOptions](../com.aspose.words/footnoteoptions) | 表示文档或部分的脚注编号选项。 |
| [FootnotePosition](../com.aspose.words/footnoteposition) | 定义脚注位置。 |
| [Footnote类型](../com.aspose.words/footnotetype) | 指定这是脚注还是尾注。 |
| [Form字段](../com.aspose.words/formfield) | 表示单个表单域。 |
| [Form字段Collection](../com.aspose.words/formfieldcollection) | 一个集合**Form字段**表示范围内所有表单域的对象。 |
| [Forms2OleControl](../com.aspose.words/forms2olecontrol) | 表示 Microsoft Forms 2.0 OLE 控件。 |
| [Forms2OleControlCollection](../com.aspose.words/forms2olecontrolcollection) | 代表集合[Forms2OleControl](../com.aspose.words/forms2olecontrol)对象。 |
| [Forms2OleControl类型](../com.aspose.words/forms2olecontroltype) |  |
| [FrameFormat](../com.aspose.words/frameformat) | 表示段落的框架相关格式。 |
| [Frameset](../com.aspose.words/frameset) |  |
| [FramesetCollection](../com.aspose.words/framesetcollection) |  |
| [GeneralFormat](../com.aspose.words/generalformat) | 指定应用于数字、文本或任何字段结果的通用格式。 |
| [GeneralFormatCollection](../com.aspose.words/generalformatcollection) | 表示一般格式的类型化集合。 |
| [GlossaryDocument](../com.aspose.words/glossarydocument) | 表示 Word 文档中词汇表文档的根元素。 |
| [Glyph](../com.aspose.words/glyph) |  |
| [GradientStop](../com.aspose.words/gradientstop) | 代表一个梯度停止。 |
| [GradientStopCollection](../com.aspose.words/gradientstopcollection) | 包含一个集合[GradientStop](../com.aspose.words/gradientstop)对象。 |
| [GradientStyle](../com.aspose.words/gradientstyle) | 指定渐变填充的样式。 |
| [GradientVariant](../com.aspose.words/gradientvariant) | 指定渐变填充的变体。 |
| [Granularity](../com.aspose.words/granularity) | 指定比较两个文档时要跟踪的更改的粒度。 |
| [GraphicsQualityOptions](../com.aspose.words/graphicsqualityoptions) | 允许指定额外的 . |
| [GroupShape](../com.aspose.words/groupshape) | 表示文档中的一组形状。 |
| [HeaderFooter](../com.aspose.words/headerfooter) | 表示节的页眉或页脚文本的容器。 |
| [HeaderFooterBookmarksExportMode](../com.aspose.words/headerfooterbookmarksexportmode) | 指定如何导出页眉/页脚中的书签。 |
| [HeaderFooterCollection](../com.aspose.words/headerfootercollection) | 提供键入访问[HeaderFooter](../com.aspose.words/headerfooter)a的节点**Section**. |
| [HeaderFooter类型](../com.aspose.words/headerfootertype) | 标识在 Word 文件中找到的页眉或页脚的类型。 |
| [HeightRule](../com.aspose.words/heightrule) | 指定确定对象高度的规则。 |
| [HorizontalAlignment](../com.aspose.words/horizontalalignment) | 指定浮动形状、文本框或浮动表格的水平对齐方式。 |
| [HorizontalRuleAlignment](../com.aspose.words/horizontalrulealignment) | 表示指定水平线的对齐方式。 |
| [HorizontalRuleFormat](../com.aspose.words/horizontalruleformat) | 表示水平规则格式。 |
| [HtmlControl类型](../com.aspose.words/htmlcontroltype) | 表示从 HTML 导入的元素的文档节点类型。 |
| [HtmlElementSizeOutputMode](../com.aspose.words/htmlelementsizeoutputmode) | 指定 Aspose.Words 如何将元素宽度和高度导出到 HTML、MHTML 和 EPUB。 |
| [HtmlFixedPageHorizontalAlignment](../com.aspose.words/htmlfixedpagehorizontalalignment) | 指定输出 HTML 文档中页面的水平对齐方式。 |
| [HtmlFixedSaveOptions](../com.aspose.words/htmlfixedsaveoptions) | 可用于在将文档保存到[SaveFormat.\#HTML\_FIXED](../com.aspose.words/saveformat\#HTML-FIXED)格式。 |
| [HtmlInsertOptions](../com.aspose.words/htmlinsertoptions) | 指定选项**M:Aspose.Words.DocumentBuilder.InsertHtml(System.String,Aspose.Words.HtmlInsertOptions)**方法。 |
| [HtmlLoadOptions](../com.aspose.words/htmlloadoptions) | 允许在将 HTML 文档加载到[Document](../com.aspose.words/document)目的。 |
| [HtmlMetafileFormat](../com.aspose.words/htmlmetafileformat) | 指示元文件保存到 HTML 文档的格式。 |
| [HtmlOfficeMathOutputMode](../com.aspose.words/htmlofficemathoutputmode) | 指定 Aspose.Words 如何将 OfficeMath 导出为 HTML、MHTML 和 EPUB。 |
| [HtmlSaveOptions](../com.aspose.words/htmlsaveoptions) | 可用于在将文档保存到[SaveFormat.\#HTML](../com.aspose.words/saveformat\#HTML), [SaveFormat.\#MHTML](../com.aspose.words/saveformat\#MHTML), [SaveFormat.\#EPUB](../com.aspose.words/saveformat\#EPUB)或者[SaveFormat.\#AZW\_3](../com.aspose.words/saveformat\#AZW-3)格式。 |
| [HtmlVersion](../com.aspose.words/htmlversion) | 表示将文档保存到时使用的 HTML 版本[SaveFormat.\#HTML](../com.aspose.words/saveformat\#HTML)和[SaveFormat.\#MHTML](../com.aspose.words/saveformat\#MHTML)格式。 |
| [Hyphenation](../com.aspose.words/hyphenation) | 提供使用连字字典的方法。 |
| [HyphenationOptions](../com.aspose.words/hyphenationoptions) | 允许配置文档断字选项。 |
| [ImageBinarization方法](../com.aspose.words/imagebinarizationmethod) | 指定用于二值化图像的方法。 |
| [ImageColorMode](../com.aspose.words/imagecolormode) | 指定生成的文档页面图像的颜色模式。 |
| [ImageData](../com.aspose.words/imagedata) | 定义形状的图像。 |
| [Image字段MergingArgs](../com.aspose.words/imagefieldmergingargs) | 提供数据为[I字段MergingCallback.\#image字段Merging(com.aspose.words.Image字段MergingArgs)](../com.aspose.words/ifieldmergingcallback\#image字段Merging-com.aspose.words.Image字段MergingArgs-)事件。 |
| [ImagePixelFormat](../com.aspose.words/imagepixelformat) | 指定生成的文档页面图像的像素格式。 |
| [ImageSaveOptions](../com.aspose.words/imagesaveoptions) | 允许在将文档页面或形状渲染为图像时指定其他选项。 |
| [ImageSavingArgs](../com.aspose.words/imagesavingargs) | 提供数据为[IImageSavingCallback.\#imageSaving(com.aspose.words.ImageSavingArgs)](../com.aspose.words/iimagesavingcallback\#imageSaving-com.aspose.words.ImageSavingArgs-)事件。 |
| [ImageSize](../com.aspose.words/imagesize) | 包含有关图像大小和分辨率的信息。 |
| [Image类型](../com.aspose.words/imagetype) | 指定 Microsoft Word 文档中图像的类型（格式）。 |
| [ImageWatermarkOptions](../com.aspose.words/imagewatermarkoptions) | 包含在添加带有图像的水印时可以指定的选项。 |
| [ImlRenderingMode](../com.aspose.words/imlrenderingmode) | 指定如何将墨迹 (InkML) 对象呈现为固定页面格式。 |
| [ImportFormatMode](../com.aspose.words/importformatmode) | 指定从另一个文档导入内容时如何合并格式。 |
| [ImportFormatOptions](../com.aspose.words/importformatoptions) | 允许指定各种导入选项来格式化输出。 |
| [IncorrectPasswordException](../com.aspose.words/incorrectpasswordexception) | 如果文档使用密码加密并且打开文档时指定的密码不正确或丢失，则抛出此错误。 |
| [Inline](../com.aspose.words/inline) | 内联级节点的基类，可以有与之关联的字符格式，但不能有自己的子节点。 |
| [InlineStory](../com.aspose.words/inlinestory) | 可以包含段落和表格的内联级节点的基类。 |
| [InternableComplexAttr](../com.aspose.words/internablecomplexattr) | 可内部复杂属性的基类。 |
| [JoinStyle](../com.aspose.words/joinstyle) | 线连接样式。 |
| [JsonDataLoadOptions](../com.aspose.words/jsondataloadoptions) | 表示解析 JSON 数据的选项。 |
| [JsonDataSource](../com.aspose.words/jsondatasource) | 提供对要在报告中使用的 JSON 文件或流的数据的访问。 |
| [JsonSimpleValueParseMode](../com.aspose.words/jsonsimplevalueparsemode) | 指定在加载 JSON 时解析 JSON 简单值（null、布尔值、数字、整数和字符串）的模式。 |
| [Known类型Set](../com.aspose.words/knowntypeset) | 表示一个无序集（即 |
| [LanguagePreferences](../com.aspose.words/languagepreferences) | 允许设置语言首选项。 |
| [LayoutCollector](../com.aspose.words/layoutcollector) | 此类允许计算文档节点的页码。 |
| [LayoutEntity类型](../com.aspose.words/layoutentitytype) | 布局实体的类型。 |
| [LayoutEnumerator](../com.aspose.words/layoutenumerator) | 枚举文档的页面布局实体。 |
| [LayoutFlow](../com.aspose.words/layoutflow) | 确定文本框中文本布局的流向。 |
| [LayoutOptions](../com.aspose.words/layoutoptions) | 包含允许控制文档布局过程的选项。 |
| [LegendPosition](../com.aspose.words/legendposition) | 指定图表图例的可能位置。 |
| [License](../com.aspose.words/license) | 提供许可组件的方法。 |
| [LineNumberRestartMode](../com.aspose.words/linenumberrestartmode) | 确定何时重新开始自动行编号。 |
| [LineSpacingRule](../com.aspose.words/linespacingrule) | 指定段落的行距值。 |
| [LineStyle](../com.aspose.words/linestyle) | 指定 a 的线型[Border](../com.aspose.words/border). |
| [List](../com.aspose.words/list) | 表示列表的格式。 |
| [ListCollection](../com.aspose.words/listcollection) | 存储和管理文档中使用的项目符号和编号列表的格式。 |
| [ListFormat](../com.aspose.words/listformat) | 允许控制应用于段落的列表格式。 |
| [ListLabel](../com.aspose.words/listlabel) | 定义特定于列表标签的属性。 |
| [ListLevel](../com.aspose.words/listlevel) | 定义列表级别的格式。 |
| [ListLevelAlignment](../com.aspose.words/listlevelalignment) | 指定列表编号或项目符号的对齐方式。 |
| [ListLevelCollection](../com.aspose.words/listlevelcollection) | 列表中每个级别的列表格式集合。 |
| [ListTemplate](../com.aspose.words/listtemplate) | 指定 Microsoft Word 中可用的预定义列表格式之一。 |
| [ListTrailingCharacter](../com.aspose.words/listtrailingcharacter) | 指定将列表标签与段落文本分开的字符。 |
| [LoadFormat](../com.aspose.words/loadformat) | 指示要加载的文档的格式。 |
| [LoadOptions](../com.aspose.words/loadoptions) | 允许在将文档加载到[Document](../com.aspose.words/document)目的。 |
| [MailMerge](../com.aspose.words/mailmerge) | 表示邮件合并功能。 |
| [MailMergeCheckErrors](../com.aspose.words/mailmergecheckerrors) | 指定 Microsoft Word 如何报告在邮件合并期间检测到的错误。 |
| [MailMergeCleanupOptions](../com.aspose.words/mailmergecleanupoptions) | 指定确定在邮件合并期间删除哪些项目的选项。 |
| [MailMergeData类型](../com.aspose.words/mailmergedatatype) | 指定外部邮件合并数据源的类型。 |
| [MailMergeDestination](../com.aspose.words/mailmergedestination) | 指定对文档执行邮件合并时可能生成的结果。 |
| [MailMergeMainDocument类型](../com.aspose.words/mailmergemaindocumenttype) | 指定邮件合并源文档的可能类型。 |
| [MailMergeRegionInfo](../com.aspose.words/mailmergeregioninfo) | 包含有关邮件合并区域的信息。 |
| [MailMergeSettings](../com.aspose.words/mailmergesettings) | 指定文档的所有邮件合并信息。 |
| [MappedData字段Collection](../com.aspose.words/mappeddatafieldcollection) | 允许在数据源中的字段名称和文档中的邮件合并字段名称之间自动映射。 |
| [MarkdownSaveOptions](../com.aspose.words/markdownsaveoptions) | 将文档保存到[SaveFormat.\#MARKDOWN](../com.aspose.words/saveformat\#MARKDOWN)格式。 |
| [MarkerSymbol](../com.aspose.words/markersymbol) | 指定标记符号样式。 |
| [MarkupLevel](../com.aspose.words/markuplevel) | 指定文档树中的特定级别[StructuredDocumentTag](../com.aspose.words/structureddocumenttag)可以发生。 |
| [MathObject类型](../com.aspose.words/mathobjecttype) | 指定 Office Math 对象的类型。 |
| [MeasurementUnits](../com.aspose.words/measurementunits) | 指定测量单位。 |
| [MemoryFontSource](../com.aspose.words/memoryfontsource) | 表示存储在内存中的单个 True类型 字体文件。 |
| [Merge字段ImageDimension](../com.aspose.words/mergefieldimagedimension) | 表示图像尺寸（即 |
| [Merge字段ImageDimensionUnit](../com.aspose.words/mergefieldimagedimensionunit) | 指定图像尺寸的单位（即 |
| [MetafileRenderingMode](../com.aspose.words/metafilerenderingmode) | 指定 Aspose.Words 应如何呈现 WMF 和 EMF 元文件。 |
| [MetafileRenderingOptions](../com.aspose.words/metafilerenderingoptions) | 允许指定额外的元文件渲染选项。 |
| [Metered](../com.aspose.words/metered) | 提供设置计量键的方法。 |
| [MsWordVersion](../com.aspose.words/mswordversion) | 允许 Aspose.Wods 模仿特定于 MS Word 版本的应用程序行为。 |
| [MultiplePages类型](../com.aspose.words/multiplepagestype) | 指定如何打印文档。 |
| [Node](../com.aspose.words/node) | Word 文档的所有节点的基类。 |
| [NodeChangingAction](../com.aspose.words/nodechangingaction) | 指定节点更改的类型。 |
| [NodeChangingArgs](../com.aspose.words/nodechangingargs) | 为方法提供数据[INodeChangingCallback](../com.aspose.words/inodechangingcallback)界面。 |
| [NodeCollection](../com.aspose.words/nodecollection) | 表示特定类型的节点的集合。 |
| [NodeImporter](../com.aspose.words/nodeimporter) | 允许有效地将节点从一个文档重复导入到另一个文档。 |
| [NodeList](../com.aspose.words/nodelist) | 表示与使用执行的 XPath 查询匹配的节点集合[CompositeNode.\#selectNodes(java.lang.String)](../com.aspose.words/compositenode\#selectNodes-java.lang.String-)方法。 |
| [NodeRendererBase](../com.aspose.words/noderendererbase) | 基类[ShapeRenderer](../com.aspose.words/shaperenderer)和[OfficeMathRenderer](../com.aspose.words/officemathrenderer). |
| [Node类型](../com.aspose.words/nodetype) | 指定 Word 文档节点的类型。 |
| [NumberStyle](../com.aspose.words/numberstyle) | 指定列表、脚注和尾注、页码的编号样式。 |
| [NumeralFormat](../com.aspose.words/numeralformat) | 指示在呈现为固定页面格式时用于表示数字的符号集。 |
| [Odso](../com.aspose.words/odso) | 指定邮件合并数据源的 Office 数据源对象 (ODSO) 设置。 |
| [OdsoDataSource类型](../com.aspose.words/odsodatasourcetype) | 指定要连接到的外部数据源的类型，作为 ODSO 连接信息的一部分。 |
| [Odso字段MapData](../com.aspose.words/odsofieldmapdata) | 指定如何将外部数据源中的列映射到文档中的预定义合并字段。 |
| [Odso字段MapDataCollection](../com.aspose.words/odsofieldmapdatacollection) | 的类型化集合[Odso字段MapData](../com.aspose.words/odsofieldmapdata)对象。 |
| [Odso字段Mapping类型](../com.aspose.words/odsofieldmappingtype) | 指定用于指示给定邮件合并字段是否已映射到给定外部数据源中的列的可能类型。 |
| [OdsoRecipientData](../com.aspose.words/odsorecipientdata) | 表示有关要从邮件合并中排除的外部数据源中的单个记录的信息。 |
| [OdsoRecipientDataCollection](../com.aspose.words/odsorecipientdatacollection) | 类型化的集合[OdsoRecipientData](../com.aspose.words/odsorecipientdata) |
| [OdtSaveMeasureUnit](../com.aspose.words/odtsavemeasureunit) | 指定的度量单位，以在保存期间应用于可测量的文档内容，例如形状、宽度和其他。 |
| [OdtSaveOptions](../com.aspose.words/odtsaveoptions) | 可用于在将文档保存到[SaveFormat.\#ODT](../com.aspose.words/saveformat\#ODT)或者[SaveFormat.\#OTT](../com.aspose.words/saveformat\#OTT)格式。 |
| [OfficeMath](../com.aspose.words/officemath) | 表示 Office Math 对象，例如函数、方程、矩阵等。 |
| [OfficeMathDisplay类型](../com.aspose.words/officemathdisplaytype) | 指定方程的显示格式类型。 |
| [OfficeMathJustification](../com.aspose.words/officemathjustification) | 指定等式的对正。 |
| [OfficeMathRenderer](../com.aspose.words/officemathrenderer) | 提供渲染个体的方法[OfficeMath](../com.aspose.words/officemath)到光栅或矢量图像或到图形对象。 |
| [OleControl](../com.aspose.words/olecontrol) | 表示 OLE ActiveX 控件。 |
| [OleFormat](../com.aspose.words/oleformat) | 提供对 OLE 对象或 ActiveX 控件的数据的访问。 |
| [Ole包裹](../com.aspose.words/olepackage) | 允许访问 OLE 包属性。 |
| [OoxmlCompliance](../com.aspose.words/ooxmlcompliance) | 允许指定以 DOCX 格式保存时将使用的 OOXML 规范。 |
| [OoxmlSaveOptions](../com.aspose.words/ooxmlsaveoptions) | 可用于在将文档保存到[SaveFormat.\#DOCX](../com.aspose.words/saveformat\#DOCX), [SaveFormat.\#DOCM](../com.aspose.words/saveformat\#DOCM), [SaveFormat.\#DOTX](../com.aspose.words/saveformat\#DOTX), [SaveFormat.\#DOTM](../com.aspose.words/saveformat\#DOTM)或者[SaveFormat.\#FLAT\_OPC](../com.aspose.words/saveformat\#FLAT-OPC)格式。 |
| [Orientation](../com.aspose.words/orientation) | 指定页面方向。 |
| [OutlineLevel](../com.aspose.words/outlinelevel) | 指定文档中段落的大纲级别。 |
| [OutlineOptions](../com.aspose.words/outlineoptions) | 允许指定大纲选项。 |
| [PageBorderAppliesTo](../com.aspose.words/pageborderappliesto) | 指定打印页面边框的页面。 |
| [PageBorderDistanceFrom](../com.aspose.words/pageborderdistancefrom) | 指定页面边框相对于页边距的位置。 |
| [PageInfo](../com.aspose.words/pageinfo) | 表示有关特定文档页面的信息。 |
| [PageLayoutCallbackArgs](../com.aspose.words/pagelayoutcallbackargs) | 传入的参数[IPageLayoutCallback.\#notify(com.aspose.words.PageLayoutCallbackArgs)](../com.aspose.words/ipagelayoutcallback\#notify-com.aspose.words.PageLayoutCallbackArgs-) |
| [PageLayoutEvent](../com.aspose.words/pagelayoutevent) | 在页面布局模型构建和渲染期间引发的事件代码。 |
| [PageRange](../com.aspose.words/pagerange) | 表示连续范围的页面。 |
| [PageSavingArgs](../com.aspose.words/pagesavingargs) | 提供数据为[IPageSavingCallback.\#pageSaving(com.aspose.words.PageSavingArgs)](../com.aspose.words/ipagesavingcallback\#pageSaving-com.aspose.words.PageSavingArgs-)事件。 |
| [PageSet](../com.aspose.words/pageset) | 描述一组随机的页面。 |
| [PageSetup](../com.aspose.words/pagesetup) | 表示部分的页面设置属性。 |
| [PageVerticalAlignment](../com.aspose.words/pageverticalalignment) | 指定每页上文本的垂直对齐方式。 |
| [PaperSize](../com.aspose.words/papersize) | 指定纸张尺寸。 |
| [Paragraph](../com.aspose.words/paragraph) | 代表一段文字。 |
| [ParagraphAlignment](../com.aspose.words/paragraphalignment) | 指定段落中的文本对齐方式。 |
| [ParagraphCollection](../com.aspose.words/paragraphcollection) | 提供对集合的类型化访问[Paragraph](../com.aspose.words/paragraph)节点。 |
| [ParagraphFormat](../com.aspose.words/paragraphformat) | 表示段落的所有格式。 |
| [Pattern类型](../com.aspose.words/patterntype) | 指定用于填充形状的填充图案。 |
| [PclSaveOptions](../com.aspose.words/pclsaveoptions) | 可用于在将文档保存到[SaveFormat.\#PCL](../com.aspose.words/saveformat\#PCL)格式。 |
| [PdfCompliance](../com.aspose.words/pdfcompliance) | 指定 PDF 标准合规级别。 |
| [PdfCustomPropertiesExport](../com.aspose.words/pdfcustompropertiesexport) | 指定方式[Document.\#getCustomDocumentProperties()](../com.aspose.words/document\#getCustomDocumentProperties--)导出为 PDF 文件。 |
| [PdfDigitalSignatureDetails](../com.aspose.words/pdfdigitalsignaturedetails) | 包含使用数字签名签署 PDF 文档的详细信息。 |
| [PdfDigitalSignatureHashAlgorithm](../com.aspose.words/pdfdigitalsignaturehashalgorithm) | 指定数字签名使用的数字哈希算法。 |
| [PdfDigitalSignatureTimestampSettings](../com.aspose.words/pdfdigitalsignaturetimestampsettings) | 包含数字签名时间戳的设置。 |
| [PdfEncryptionDetails](../com.aspose.words/pdfencryptiondetails) | 包含 PDF 文档的加密和访问权限的详细信息。 |
| [PdfFontEmbeddingMode](../com.aspose.words/pdffontembeddingmode) | 指定 Aspose.Words 应该如何嵌入字体。 |
| [PdfImageColorSpaceExportMode](../com.aspose.words/pdfimagecolorspaceexportmode) | 指定如何为 PDF 文档中的图像选择色彩空间。 |
| [PdfImageCompression](../com.aspose.words/pdfimagecompression) | 指定应用于 PDF 文件中图像的压缩类型。 |
| [PdfLoadOptions](../com.aspose.words/pdfloadoptions) | 允许在将 Pdf 文档加载到[Document](../com.aspose.words/document)目的。 |
| [PdfPageMode](../com.aspose.words/pdfpagemode) | 指定 PDF 文档在 PDF 阅读器中打开时的显示方式。 |
| [PdfPermissions](../com.aspose.words/pdfpermissions) | 指定允许用户对加密的 PDF 文档进行的操作。 |
| [PdfSaveOptions](../com.aspose.words/pdfsaveoptions) | 可用于在将文档保存到[SaveFormat.\#PDF](../com.aspose.words/saveformat\#PDF)格式。 |
| [PdfTextCompression](../com.aspose.words/pdftextcompression) | 指定应用于 PDF 文件中除图像之外的所有内容的压缩类型。 |
| [PdfZoomBehavior](../com.aspose.words/pdfzoombehavior) | 指定在 PDF 查看器中打开 PDF 文档时应用到的缩放类型。 |
| [PhysicalFontInfo](../com.aspose.words/physicalfontinfo) | 指定有关 Aspose.Words 字体引擎可用的物理字体的信息。 |
| [PlainTextDocument](../com.aspose.words/plaintextdocument) | 允许提取文档内容的纯文本表示。 |
| [PreferredWidth](../com.aspose.words/preferredwidth) | 表示一个值及其度量单位，用于指定表格或单元格的首选宽度。 |
| [PreferredWidth类型](../com.aspose.words/preferredwidthtype) | 指定表格或单元格的首选宽度的测量单位。 |
| [PresetTexture](../com.aspose.words/presettexture) | 指定用于填充形状的纹理。 |
| [Property类型](../com.aspose.words/propertytype) | 指定文档属性的数据类型。 |
| [Protection类型](../com.aspose.words/protectiontype) | 文档的保护类型。 |
| [PsSaveOptions](../com.aspose.words/pssaveoptions) | 可用于在将文档保存到[SaveFormat.\#PS](../com.aspose.words/saveformat\#PS)格式。 |
| [Range](../com.aspose.words/range) | 表示文档中的一个连续区域。 |
| [RelativeHorizontalPosition](../com.aspose.words/relativehorizontalposition) | 指定形状或文本框的水平位置是相对的。 |
| [RelativeVerticalPosition](../com.aspose.words/relativeverticalposition) | 指定形状或文本框的垂直位置是相对的。 |
| [ReplaceAction](../com.aspose.words/replaceaction) | 允许用户指定在替换操作期间当前匹配发生的情况。 |
| [ReplacingArgs](../com.aspose.words/replacingargs) | 为自定义替换操作提供数据。 |
| [ReportBuildOptions](../com.aspose.words/reportbuildoptions) | 指定控制行为的选项[ReportingEngine](../com.aspose.words/reportingengine)在构建报告时。 |
| [ReportingEngine](../com.aspose.words/reportingengine) | 提供例程来使用数据填充模板文档和一组设置来控制这些例程。 |
| [ResourceLoadingAction](../com.aspose.words/resourceloadingaction) | 指定资源加载的模式。 |
| [ResourceLoadingArgs](../com.aspose.words/resourceloadingargs) | 提供数据为[IResourceLoadingCallback.\#resourceLoading(com.aspose.words.ResourceLoadingArgs)](../com.aspose.words/iresourceloadingcallback\#resourceLoading-com.aspose.words.ResourceLoadingArgs-)方法。 |
| [ResourceSavingArgs](../com.aspose.words/resourcesavingargs) | 提供数据为[IResourceSavingCallback.\#resourceSaving(com.aspose.words.ResourceSavingArgs)](../com.aspose.words/iresourcesavingcallback\#resourceSaving-com.aspose.words.ResourceSavingArgs-)事件。 |
| [Resource类型](../com.aspose.words/resourcetype) | 加载资源的类型。 |
| [Revision](../com.aspose.words/revision) | 表示文档节点或样式中的修订（跟踪更改）。 |
| [RevisionCollection](../com.aspose.words/revisioncollection) | 一个集合[Revision](../com.aspose.words/revision)表示文档中的修订的对象。 |
| [RevisionColor](../com.aspose.words/revisioncolor) | 允许指定文档修订的颜色。 |
| [RevisionGroup](../com.aspose.words/revisiongroup) | 代表一组顺序[Revision](../com.aspose.words/revision)对象。 |
| [RevisionGroupCollection](../com.aspose.words/revisiongroupcollection) | 一个集合[RevisionGroup](../com.aspose.words/revisiongroup)表示文档中修订组的对象。 |
| [RevisionOptions](../com.aspose.words/revisionoptions) | 允许控制在布局过程中如何处理文档修订。 |
| [RevisionTextEffect](../com.aspose.words/revisiontexteffect) | 允许为文档文本的修订指定装饰效果。 |
| [Revision类型](../com.aspose.words/revisiontype) | 指定跟踪的更改类型[Revision](../com.aspose.words/revision). |
| [RevisionsView](../com.aspose.words/revisionsview) | 允许指定是使用文档的原始版本还是修订版本。 |
| [Row](../com.aspose.words/row) | 表示表格行。 |
| [RowCollection](../com.aspose.words/rowcollection) | 提供对集合的类型化访问[Row](../com.aspose.words/row)节点。 |
| [RowFormat](../com.aspose.words/rowformat) | 表示表格行的所有格式。 |
| [RtfLoadOptions](../com.aspose.words/rtfloadoptions) | 允许在加载时指定其他选项[LoadFormat.\#RTF](../com.aspose.words/loadformat\#RTF)文档成一个[Document](../com.aspose.words/document)目的。 |
| [RtfSaveOptions](../com.aspose.words/rtfsaveoptions) | 可用于在将文档保存到[SaveFormat.\#RTF](../com.aspose.words/saveformat\#RTF)格式。 |
| [Run](../com.aspose.words/run) | 表示具有相同字体格式的一系列字符。 |
| [RunCollection](../com.aspose.words/runcollection) | 提供对集合的类型化访问[Run](../com.aspose.words/run)节点。 |
| [SaveFormat](../com.aspose.words/saveformat) | 指示文档的保存格式。 |
| [SaveOptions](../com.aspose.words/saveoptions) | 这是类的抽象基类，允许用户在将文档保存为特定格式时指定其他选项。 |
| [SaveOutput参数](../com.aspose.words/saveoutputparameters) | 此对象在保存文档后返回给调用者，并包含在保存操作期间生成或计算的附加信息。 |
| [ScriptShapingLevel](../com.aspose.words/scriptshapinglevel) |  |
| [SdtAppearance](../com.aspose.words/sdtappearance) | 指定结构化文档标签的外观。 |
| [SdtCalendar类型](../com.aspose.words/sdtcalendartype) | 指定可用于指定的可能的日历类型[StructuredDocumentTag.\#getCalendar类型()](../com.aspose.words/structureddocumenttag\#getCalendar类型--) / [StructuredDocumentTag.\#setCalendar类型(int)](../com.aspose.words/structureddocumenttag\#setCalendar类型-int-)在 Office Open XML 文档中。 |
| [SdtDateStorageFormat](../com.aspose.words/sdtdatestorageformat) | 指定当 SDT 绑定到文档数据存储中的 XML 节点时如何存储/检索日期 SDT 的日期。 |
| [SdtListItem](../com.aspose.words/sdtlistitem) | 此元素指定父项中的单个列表项[Sdt类型.\#COMBO\_BOX](../com.aspose.words/sdttype\#COMBO-BOX)或者[Sdt类型.\#DROP\_DOWN\_LIST](../com.aspose.words/sdttype\#DROP-DOWN-LIST)结构化文档标签。 |
| [SdtListItemCollection](../com.aspose.words/sdtlistitemcollection) | 提供访问[SdtListItem](../com.aspose.words/sdtlistitem)结构化文档标签的元素。 |
| [Sdt类型](../com.aspose.words/sdttype) | 指定结构化文档标签 (SDT) 节点的类型。 |
| [Section](../com.aspose.words/section) | 表示文档中的单个部分。 |
| [SectionCollection](../com.aspose.words/sectioncollection) | 一个集合**Section**文档中的对象。 |
| [SectionLayoutMode](../com.aspose.words/sectionlayoutmode) | 指定允许定义文档网格行为的部分的布局模式。 |
| [SectionStart](../com.aspose.words/sectionstart) | 节开头的中断类型。 |
| [Shading](../com.aspose.words/shading) | 包含对象的着色属性。 |
| [ShadowFormat](../com.aspose.words/shadowformat) | 表示对象的阴影格式。 |
| [Shadow类型](../com.aspose.words/shadowtype) | 指定形状阴影的类型。 |
| [Shape](../com.aspose.words/shape) | 表示绘图层中的对象，例如自选图形、文本框、自由格式、OLE 对象、ActiveX 控件或图片。 |
| [ShapeBase](../com.aspose.words/shapebase) | 绘图层中对象的基类，例如自选图形、自由格式、OLE 对象、ActiveX 控件或图片。 |
| [ShapeLineStyle](../com.aspose.words/shapelinestyle) | 指定 a 的复合线型[Shape](../com.aspose.words/shape). |
| [ShapeMarkupLanguage](../com.aspose.words/shapemarkuplanguage) | 指定用于形状的标记语言。 |
| [ShapeRenderer](../com.aspose.words/shaperenderer) | 提供渲染个体的方法[Shape](../com.aspose.words/shape)或者[GroupShape](../com.aspose.words/groupshape)到光栅或矢量图像或到图形对象。 |
| [Shape类型](../com.aspose.words/shapetype) | 指定 Microsoft Word 文档中的形状类型。 |
| [ShowInBalloons](../com.aspose.words/showinballoons) | 指定在气球中呈现哪些修订。 |
| [SignOptions](../com.aspose.words/signoptions) | 允许指定文档签名的选项。 |
| [SignatureLine](../com.aspose.words/signatureline) | 提供对签名行属性的访问。 |
| [SignatureLineOptions](../com.aspose.words/signaturelineoptions) | 允许为插入的签名行指定选项。 |
| [SmartTag](../com.aspose.words/smarttag) | 此元素指定段落中一个或多个内联结构（运行、图像、字段等）周围是否存在智能标记。 |
| [SpecialChar](../com.aspose.words/specialchar) | 文档中特殊字符的基类。 |
| [Story](../com.aspose.words/story) | 包含块级节点的元素的基类[Paragraph](../com.aspose.words/paragraph)和[Table](../com.aspose.words/table). |
| [Story类型](../com.aspose.words/storytype) | Word 文档的文本存储在故事中。 |
| [StreamFontSource](../com.aspose.words/streamfontsource) | 用户定义流字体源的基类。 |
| [Stroke](../com.aspose.words/stroke) | 定义形状的笔触。 |
| [StructuredDocumentTag](../com.aspose.words/structureddocumenttag) | 表示文档中的结构化文档标签（SDT 或内容控件）。 |
| [StructuredDocumentTagCollection](../com.aspose.words/structureddocumenttagcollection) | 一个集合[IStructuredDocumentTag](../com.aspose.words/istructureddocumenttag)表示指定范围内的结构化文档标签的实例。 |
| [StructuredDocumentTagRangeEnd](../com.aspose.words/structureddocumenttagrangeend) | 代表结束**ranged**接受多节内容的结构化文档标签。 |
| [StructuredDocumentTagRangeStart](../com.aspose.words/structureddocumenttagrangestart) | 代表一个开始**ranged**接受多节内容的结构化文档标签。 |
| [Style](../com.aspose.words/style) | 表示单个内置或用户定义的样式。 |
| [StyleCollection](../com.aspose.words/stylecollection) | Style 对象的集合，表示文档中的内置样式和用户定义的样式。 |
| [StyleIdentifier](../com.aspose.words/styleidentifier) | 独立于语言环境的样式标识符。 |
| [Style类型](../com.aspose.words/styletype) | 表示样式的类型。 |
| [SubDocument](../com.aspose.words/subdocument) | 代表一个**SubDocument** \这是对外部存储文档的引用。 |
| [SvgSaveOptions](../com.aspose.words/svgsaveoptions) | 可用于在将文档保存到[SaveFormat.\#SVG](../com.aspose.words/saveformat\#SVG)格式。 |
| [SvgTextOutputMode](../com.aspose.words/svgtextoutputmode) |  |
| [SystemFontSource](../com.aspose.words/systemfontsource) | 表示安装到系统的所有 True类型 字体。 |
| [TabAlignment](../com.aspose.words/tabalignment) | 指定制表位的对齐方式/类型。 |
| [TabLeader](../com.aspose.words/tableader) | 指定制表符下显示的引线的类型。 |
| [TabStop](../com.aspose.words/tabstop) | 表示单个自定义制表位。 |
| [TabStopCollection](../com.aspose.words/tabstopcollection) | 一个集合[TabStop](../com.aspose.words/tabstop)代表段落或样式的自定义选项卡的对象。 |
| [Table](../com.aspose.words/table) | 表示 Word 文档中的表格。 |
| [TableAlignment](../com.aspose.words/tablealignment) | 指定内联表的对齐方式。 |
| [TableCollection](../com.aspose.words/tablecollection) | 提供对集合的类型化访问[Table](../com.aspose.words/table)节点。 |
| [TableContentAlignment](../com.aspose.words/tablecontentalignment) | 允许指定导出为 Markdown 格式时要使用的表格内容的对齐方式。 |
| [TableStyle](../com.aspose.words/tablestyle) | 表示表格样式。 |
| [TableStyleOptions](../com.aspose.words/tablestyleoptions) | 指定如何将表格样式应用于表格。 |
| [TableSubstitutionRule](../com.aspose.words/tablesubstitutionrule) | 表格字体替换规则。 |
| [TaskPane](../com.aspose.words/taskpane) | 表示加载项任务窗格对象。 |
| [TaskPaneCollection](../com.aspose.words/taskpanecollection) | 指定持久任务窗格对象的列表。 |
| [TaskPaneDockState](../com.aspose.words/taskpanedockstate) | 枚举任务窗格对象的可用位置。 |
| [TextBox](../com.aspose.words/textbox) | 定义指定文本如何在形状内显示的属性。 |
| [TextBoxAnchor](../com.aspose.words/textboxanchor) | 指定用于形状文本垂直对齐的值。 |
| [TextBoxWrapMode](../com.aspose.words/textboxwrapmode) | 指定文本在形状内的换行方式。 |
| [TextColumn](../com.aspose.words/textcolumn) | 表示单个文本列。 |
| [TextColumnCollection](../com.aspose.words/textcolumncollection) | 一个集合[TextColumn](../com.aspose.words/textcolumn)表示文档部分中所有文本列的对象。 |
| [TextDmlEffect](../com.aspose.words/textdmleffect) | 文本运行的 Dml 文本效果。 |
| [TextEffect](../com.aspose.words/texteffect) | 文本运行的动画效果。 |
| [TextForm字段类型](../com.aspose.words/textformfieldtype) | 指定文本表单域的类型。 |
| [TextOrientation](../com.aspose.words/textorientation) | 指定页面、表格单元格或文本框架中文本的方向。 |
| [TextPath](../com.aspose.words/textpath) | 定义文本路径（艺术字对象）的文本和格式。 |
| [TextPathAlignment](../com.aspose.words/textpathalignment) | 艺术字对齐。 |
| [TextWatermarkOptions](../com.aspose.words/textwatermarkoptions) | 包含在添加带文本的水印时可以指定的选项。 |
| [TextWrapping](../com.aspose.words/textwrapping) | 指定文本如何环绕表格。 |
| [TextureAlignment](../com.aspose.words/texturealignment) | 指定纹理填充平铺的对齐方式。 |
| [TextureIndex](../com.aspose.words/textureindex) | 指定着色纹理。 |
| [Theme](../com.aspose.words/theme) | 代表文档主题，并提供对主要主题部分的访问，包括[Theme.\#getMajorFonts()](../com.aspose.words/theme\#getMajorFonts--), [Theme.\#getMinorFonts()](../com.aspose.words/theme\#getMinorFonts--)和[Theme.\#getColors()](../com.aspose.words/theme\#getColors--) |
| [ThemeColor](../com.aspose.words/themecolor) | 指定文档主题的主题颜色。 |
| [ThemeColors](../com.aspose.words/themecolors) | 表示包含十二种颜色的文档主题的配色方案。 |
| [ThemeFont](../com.aspose.words/themefont) | 指定文档主题的主题字体名称类型。 |
| [ThemeFonts](../com.aspose.words/themefonts) | 表示字体方案中的字体集合，允许为不同的语言指定不同的字体[ThemeFonts.\#getLatin()](../com.aspose.words/themefonts\#getLatin--) / [ThemeFonts.\#setLatin(java.lang.String)](../com.aspose.words/themefonts\#setLatin-java.lang.String-), [ThemeFonts.\#getEastAsian()](../com.aspose.words/themefonts\#getEastAsian--) / [ThemeFonts.\#setEastAsian(java.lang.String)](../com.aspose.words/themefonts\#setEastAsian-java.lang.String-)和[ThemeFonts.\#getComplexScript()](../com.aspose.words/themefonts\#getComplexScript--) / [ThemeFonts.\#setComplexScript(java.lang.String)](../com.aspose.words/themefonts\#setComplexScript-java.lang.String-). |
| [ThumbnailGeneratingOptions](../com.aspose.words/thumbnailgeneratingoptions) | 可用于在为文档生成缩略图时指定其他选项。 |
| [TiffCompression](../com.aspose.words/tiffcompression) | 指定将页面图像保存到 TIFF 文件时应用的压缩类型。 |
| [ToaCategories](../com.aspose.words/toacategories) | 表示权限类别表。 |
| [TxtExportHeadersFootersMode](../com.aspose.words/txtexportheadersfootersmode) | 指定将页眉和页脚导出为纯文本格式的方式。 |
| [TxtLeadingSpacesOptions](../com.aspose.words/txtleadingspacesoptions) | 指定导入期间前导空间处理的可用选项[LoadFormat.\#TEXT](../com.aspose.words/loadformat\#TEXT)文件。 |
| [TxtListIndentation](../com.aspose.words/txtlistindentation) | 指定文档导出到时如何缩进列表级别[SaveFormat.\#TEXT](../com.aspose.words/saveformat\#TEXT)格式。 |
| [TxtLoadOptions](../com.aspose.words/txtloadoptions) | 允许在加载时指定其他选项[LoadFormat.\#TEXT](../com.aspose.words/loadformat\#TEXT)文档成一个[Document](../com.aspose.words/document)目的。 |
| [TxtSaveOptions](../com.aspose.words/txtsaveoptions) | 可用于在将文档保存到[SaveFormat.\#TEXT](../com.aspose.words/saveformat\#TEXT)格式。 |
| [TxtSaveOptionsBase](../com.aspose.words/txtsaveoptionsbase) | 将文档保存为基于文本的格式时指定附加选项的基类。 |
| [TxtTrailingSpacesOptions](../com.aspose.words/txttrailingspacesoptions) | 指定在从导入期间处理尾随空格的可用选项[LoadFormat.\#TEXT](../com.aspose.words/loadformat\#TEXT)文件。 |
| [Underline](../com.aspose.words/underline) | 指示应用于字体的下划线类型。 |
| [UnicodeScript](../com.aspose.words/unicodescript) |  |
| [UnsupportedFileFormatException](../com.aspose.words/unsupportedfileformatexception) | 在文档加载期间，当 Aspose.Words 无法识别或不支持文档格式时抛出。 |
| [UserInformation](../com.aspose.words/userinformation) | 指定有关用户的信息。 |
| [VariableCollection](../com.aspose.words/variablecollection) | 文档变量的集合。 |
| [VbaModule](../com.aspose.words/vbamodule) | 提供对 VBA 项目模块的访问。 |
| [VbaModuleCollection](../com.aspose.words/vbamodulecollection) | 代表一个集合[VbaModule](../com.aspose.words/vbamodule)对象。 |
| [VbaModule类型](../com.aspose.words/vbamoduletype) | 指定 VBA 项目中模型的类型。 |
| [VbaProject](../com.aspose.words/vbaproject) | 提供对 VBA 项目信息的访问。 |
| [VbaReference](../com.aspose.words/vbareference) | 实现对自动化类型库或 VBA 项目的引用。 |
| [VbaReferenceCollection](../com.aspose.words/vbareferencecollection) | 代表一个集合[VbaReference](../com.aspose.words/vbareference)对象。 |
| [VbaReference类型](../com.aspose.words/vbareferencetype) | 允许指定类型[VbaReference](../com.aspose.words/vbareference)目的。 |
| [VerticalAlignment](../com.aspose.words/verticalalignment) | 指定浮动形状、文本框架或浮动表格的垂直对齐方式。 |
| [ViewOptions](../com.aspose.words/viewoptions) | 提供各种选项来控制文档在 Microsoft Word 中的显示方式。 |
| [View类型](../com.aspose.words/viewtype) | Microsoft Word 中视图模式的可能值。 |
| [VisitorAction](../com.aspose.words/visitoraction) | 允许访问者控制节点的枚举。 |
| [WarningInfo](../com.aspose.words/warninginfo) | 包含有关 Aspose.Words 在文档加载或保存期间发出的警告的信息。 |
| [WarningInfoCollection](../com.aspose.words/warninginfocollection) | 表示一个类型化的集合[WarningInfo](../com.aspose.words/warninginfo)对象。 |
| [WarningSource](../com.aspose.words/warningsource) | 指定在文档加载或保存期间产生警告的模块。 |
| [Warning类型](../com.aspose.words/warningtype) | 指定在文档加载或保存期间由 Aspose.Words 发出的警告的类型。 |
| [Watermark](../com.aspose.words/watermark) | 表示使用文档水印的类。 |
| [WatermarkLayout](../com.aspose.words/watermarklayout) | 定义相对于水印中心的水印布局。 |
| [Watermark类型](../com.aspose.words/watermarktype) | 指定水印类型。 |
| [WebExtension](../com.aspose.words/webextension) | 表示一个 Web 扩展对象。 |
| [WebExtensionBinding](../com.aspose.words/webextensionbinding) | 指定 Web 扩展和文档中的数据之间的绑定关系。 |
| [WebExtensionBindingCollection](../com.aspose.words/webextensionbindingcollection) | 指定 Web 扩展绑定列表。 |
| [WebExtensionBinding类型](../com.aspose.words/webextensionbindingtype) | 枚举 Web 扩展和文档中数据之间的可用绑定类型。 |
| [WebExtensionProperty](../com.aspose.words/webextensionproperty) | 指定 Web 扩展定制属性。 |
| [WebExtensionPropertyCollection](../com.aspose.words/webextensionpropertycollection) | 指定一组 Web 扩展定制属性。 |
| [WebExtensionReference](../com.aspose.words/webextensionreference) | 表示对 Web 扩展的引用。 |
| [WebExtensionReferenceCollection](../com.aspose.words/webextensionreferencecollection) | 指定 Web 扩展引用的列表。 |
| [WebExtensionStore类型](../com.aspose.words/webextensionstoretype) | 枚举 Web 扩展商店的可用类型。 |
| [WordML2003SaveOptions](../com.aspose.words/wordml2003saveoptions) | 可用于在将文档保存到[SaveFormat.\#WORD\_ML](../com.aspose.words/saveformat\#WORD-ML)格式。 |
| [WrapSide](../com.aspose.words/wrapside) | 指定文本环绕的形状或图片的哪一侧。 |
| [Wrap类型](../com.aspose.words/wraptype) | 指定文本如何环绕形状或图片。 |
| [WriteProtection](../com.aspose.words/writeprotection) | 指定文档的写保护设置。 |
| [X509Certificate2Wrapper](../com.aspose.words/x509certificate2wrapper) |  |
| [XamlFixedSaveOptions](../com.aspose.words/xamlfixedsaveoptions) | 可用于在将文档保存到[SaveFormat.\#XAML\_FIXED](../com.aspose.words/saveformat\#XAML-FIXED)格式。 |
| [XamlFlowSaveOptions](../com.aspose.words/xamlflowsaveoptions) | 可用于在将文档保存到[SaveFormat.\#XAML\_FLOW](../com.aspose.words/saveformat\#XAML-FLOW)或者[SaveFormat.\#XAML\_FLOW\_PACK](../com.aspose.words/saveformat\#XAML-FLOW-PACK)格式。 |
| [XmlDataLoadOptions](../com.aspose.words/xmldataloadoptions) | 表示 XML 数据加载的选项。 |
| [XmlDataSource](../com.aspose.words/xmldatasource) | 提供对要在报告中使用的 XML 文件或流的数据的访问。 |
| [XmlMapping](../com.aspose.words/xmlmapping) | 指定用于在父结构化文档标记和存储在文档的自定义 XML 数据部分中的 XML 元素之间建立映射的信息。 |
| [XpsSaveOptions](../com.aspose.words/xpssaveoptions) | 可用于在将文档保存到[SaveFormat.\#XPS](../com.aspose.words/saveformat\#XPS)格式。 |
| [Zoom类型](../com.aspose.words/zoomtype) | 文档在 Microsoft Word 屏幕上显示的大小的可能值。 |

## 接口

| 界面 | 描述 |
| --- | --- |
| [IBarcodeGenerator](../com.aspose.words/ibarcodegenerator) | 条形码自定义生成器的公共接口。 |
| [IChartDataPoint](../com.aspose.words/ichartdatapoint) | 包含图表上单个数据点的属性。 |
| [IComparisonExpressionEvaluator](../com.aspose.words/icomparisonexpressionevaluator) | 实施时，允许覆盖默认比较表达式评估[字段If](../com.aspose.words/fieldif)和[字段Compare](../com.aspose.words/fieldcompare)字段。 |
| [ICssSavingCallback](../com.aspose.words/icsssavingcallback) | 如果您想控制 Aspose.Words 在将文档保存为 HTML 时如何保存 CSS（层叠样式表），请实现此接口。 |
| [IDocumentLoadingCallback](../com.aspose.words/idocumentloadingcallback) | 如果您想在加载文档期间调用自己的自定义方法，请实现此接口。 |
| [IDocumentPartSavingCallback](../com.aspose.words/idocumentpartsavingcallback) | 如果您想接收通知并控制 Aspose.Words 在将文档导出到[SaveFormat.\#HTML](../com.aspose.words/saveformat\#HTML)或者[SaveFormat.\#EPUB](../com.aspose.words/saveformat\#EPUB)格式。 |
| [IDocumentReaderPlugin](../com.aspose.words/idocumentreaderplugin) | 为可以将文件读入文档的外部阅读器插件定义接口。 |
| [IDocumentSavingCallback](../com.aspose.words/idocumentsavingcallback) | 如果您希望在保存文档期间调用自己的自定义方法，请实现此接口。 |
| [I字段DatabaseProvider](../com.aspose.words/ifielddatabaseprovider) | 实现此接口以提供数据[字段Database](../com.aspose.words/fielddatabase)更新时的字段。 |
| [I字段MergingCallback](../com.aspose.words/ifieldmergingcallback) | 如果您想控制在邮件合并操作期间如何将数据插入到合并字段中，请实现此接口。 |
| [I字段ResultFormatter](../com.aspose.words/ifieldresultformatter) | 如果要控制字段结果的格式，请实现此接口。 |
| [I字段UpdateCultureProvider](../com.aspose.words/ifieldupdatecultureprovider) | 实施时，提供了一个[CultureInfo](../com.aspose.words.net.system.globalization/cultureinfo)在更新特定字段期间应使用的对象。 |
| [I字段UpdatingCallback](../com.aspose.words/ifieldupdatingcallback) | 如果您想在字段更新期间调用自己的自定义方法，请实现此接口。 |
| [I字段UserPromptRespondent](../com.aspose.words/ifielduserpromptrespondent) | 代表字段更新期间用户提示的响应者。 |
| [IFontSavingCallback](../com.aspose.words/ifontsavingcallback) | 如果您想接收通知并控制 Aspose.Words 在将文档导出为 HTML 格式时如何保存字体，请实现此接口。 |
| [IHyphenationCallback](../com.aspose.words/ihyphenationcallback) | 由可以注册连字符字典的类实现。 |
| [IImageSavingCallback](../com.aspose.words/iimagesavingcallback) | 如果您想控制 Aspose.Words 在将文档保存为 HTML 时如何保存图像，请实现此接口。 |
| [IMailMergeCallback](../com.aspose.words/imailmergecallback) | 如果您想在执行邮件合并时接收通知，请实现此接口。 |
| [IMailMergeDataSource](../com.aspose.words/imailmergedatasource) | 实现此接口以允许来自自定义数据源（例如对象列表）的邮件合并。 |
| [IMailMergeDataSourceRoot](../com.aspose.words/imailmergedatasourceroot) | 实现此接口以允许来自自定义数据源的邮件与主从数据合并。 |
| [INodeChangingCallback](../com.aspose.words/inodechangingcallback) | 如果您想在文档中插入或删除节点时接收通知，请实现此接口。 |
| [IPageLayoutCallback](../com.aspose.words/ipagelayoutcallback) | 如果您希望在构建和呈现页面布局模型期间调用自己的自定义方法，请实现此接口。 |
| [IPageSavingCallback](../com.aspose.words/ipagesavingcallback) | 如果您想控制 Aspose.Words 在将文档保存为固定页面格式时如何保存单独的页面，请实现此接口。 |
| [IReplacingCallback](../com.aspose.words/ireplacingcallback) | 如果您希望在查找和替换操作期间调用您自己的自定义方法，请实现此接口。 |
| [IResourceLoadingCallback](../com.aspose.words/iresourceloadingcallback) | 如果您想控制 Aspose.Words 在导入文档和插入图像时如何加载外部资源，请实现此接口[DocumentBuilder](../com.aspose.words/documentbuilder). |
| [IResourceSavingCallback](../com.aspose.words/iresourcesavingcallback) | 如果您想控制 Aspose.Words 在将文档保存到固定页面 HTML 或 SVG 时如何保存外部资源（图像、字体和 css），请实现此接口。 |
| [IStructuredDocumentTag](../com.aspose.words/istructureddocumenttag) | 定义通用数据的接口[StructuredDocumentTag](../com.aspose.words/structureddocumenttag)和[StructuredDocumentTagRangeStart](../com.aspose.words/structureddocumenttagrangestart). |
| [ITextShaper](../com.aspose.words/itextshaper) |  |
| [ITextShaperFactory](../com.aspose.words/itextshaperfactory) |  |
| [IWarningCallback](../com.aspose.words/iwarningcallback) | 如果您希望调用自己的自定义方法来捕获在文档加载或保存期间可能发生的保真度丢失警告，请实现此接口。 |