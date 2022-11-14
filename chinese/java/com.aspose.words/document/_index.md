---
title: Document
second_title: Aspose.Words for Java API 参考
description: 表示 Word 文档。
type: docs
weight: 120
url: /zh/java/com.aspose.words/document/
---

**遗产:**
java.lang.Object, [com.aspose.words.Node](../../com.aspose.words/node), [com.aspose.words.CompositeNode](../../com.aspose.words/compositenode), [com.aspose.words.DocumentBase](../../com.aspose.words/documentbase)
```
public class Document extends DocumentBase
```

表示 Word 文档。

要了解更多信息，请访问**Working with Document**文档文章。

这**Document**是 Aspose.Words 库中的核心对象。

以任何方式加载现有文档[LoadFormat](../../com.aspose.words/loadformat)格式，将文件名或流传递到其中一个**Document**构造函数。要创建空白文档，请调用不带参数的构造函数。

使用 Save 方法重载之一将文档保存在任何[SaveFormat](../../com.aspose.words/saveformat)格式。

将文档页面直接绘制到**Graphics**对象使用[renderToScale(int, java.awt.Graphics2D, float, float, float)](../../com.aspose.words/document\#renderToScale-int--java.awt.Graphics2D--float--float--float-)或者[renderToSize(int, java.awt.Graphics2D, float, float, float, float)](../../com.aspose.words/document\#renderToSize-int--java.awt.Graphics2D--float--float--float--float-)方法。

要打印文档，请使用其中一种[print(java.lang.String)](../../com.aspose.words/document\#print-java.lang.String-)方法。

[getMailMerge()](../../com.aspose.words/document\#getMailMerge--)是 Aspose.Words 的报告引擎，允许使用来自各种数据源的数据快速轻松地填充在 Microsoft Word 中设计的报告。数据可以来自 java.sql.ResultSet 或值数组。**MailMerge**将检查在数据源中找到的记录，并根据需要将它们插入到文档中的邮件合并字段中。

**Document**存储文档范围的信息，例如[DocumentBase.getStyles()](../../com.aspose.words/documentbase\#getStyles--), [getBuiltInDocumentProperties()](../../com.aspose.words/document\#getBuiltInDocumentProperties--), [getCustomDocumentProperties()](../../com.aspose.words/document\#getCustomDocumentProperties--)、列表和宏。这些对象中的大多数都可以通过相应的属性访问**Document**.

这**Document**是包含文档所有其他节点的树的根节点。树是一种复合设计模式，在许多方面类似于 XmlDocument。可以通过编程方式自由操作文档的内容：

 *  可以通过类型化集合访问文档的节点，例如[getSections()](../../com.aspose.words/document\#getSections--), [ParagraphCollection](../../com.aspose.words/paragraphcollection)等等
 *  文档的节点可以使用它们的节点类型来选择**M:Aspose.Words.CompositeNode.GetChildNodes(Aspose.Words.NodeType,System.Boolean)**或使用 XPath 查询[CompositeNode.selectNodes(java.lang.String)](../../com.aspose.words/compositenode\#selectNodes-java.lang.String-)或者[CompositeNode.selectSingleNode(java.lang.String)](../../com.aspose.words/compositenode\#selectSingleNode-java.lang.String-).
 *  可以使用在文档中的任何位置添加或删除内容节点[CompositeNode.insertBefore(com.aspose.words.Node, com.aspose.words.Node)](../../com.aspose.words/compositenode\#insertBefore-com.aspose.words.Node--com.aspose.words.Node-), [CompositeNode.insertAfter(com.aspose.words.Node, com.aspose.words.Node)](../../com.aspose.words/compositenode\#insertAfter-com.aspose.words.Node--com.aspose.words.Node-), [CompositeNode.removeChild(com.aspose.words.Node)](../../com.aspose.words/compositenode\#removeChild-com.aspose.words.Node-)以及基类提供的其他方法[CompositeNode](../../com.aspose.words/compositenode).
 *  每个节点的格式属性可以通过该节点的属性进行更改。

考虑使用[DocumentBuilder](../../com.aspose.words/documentbuilder)这简化了以编程方式创建或填充文档树的任务。

这**Document**只能包含[Section](../../com.aspose.words/section)对象。

在 Microsoft Word 中，一个有效的文档至少需要有一个部分。
## 构造函数

| 构造函数 | 描述 |
| --- | --- |
| [Document()](#Document--) | 创建或加载文档。 |
| [Document(String fileName)](#Document-java.lang.String-) | 从文件中打开现有文档。 |
| [Document(String fileName, LoadOptions loadOptions)](#Document-java.lang.String-com.aspose.words.LoadOptions-) | 从文件中打开现有文档。 |
| [Document(InputStream stream)](#Document-java.io.InputStream-) | 初始化此类的新实例。 |
| [Document(InputStream stream, LoadOptions loadOptions)](#Document-java.io.InputStream-com.aspose.words.LoadOptions-) | 初始化此类的新实例。 |
## 方法

| 方法 | 描述 |
| --- | --- |
| [accept(DocumentVisitor visitor)](#accept-com.aspose.words.DocumentVisitor-) | 接受访客。 |
| [acceptAllRevisions()](#acceptAllRevisions--) | 接受文档中的所有修订。 |
| [add(Shape watermark)](#add-com.aspose.words.Shape-) |  |
| [appendChild(Node newChild)](#appendChild-com.aspose.words.Node-) | 将指定节点添加到此节点的子节点列表的末尾。 |
| [appendDocument(Document srcDoc, int importFormatMode)](#appendDocument-com.aspose.words.Document-int-) |  |
| [appendDocument(Document srcDoc, int importFormatMode, ImportFormatOptions importFormatOptions)](#appendDocument-com.aspose.words.Document-int-com.aspose.words.ImportFormatOptions-) |  |
| [cleanup()](#cleanup--) | 从文档中清除未使用的样式和列表。 |
| [cleanup(CleanupOptions options)](#cleanup-com.aspose.words.CleanupOptions-) | 根据给定的内容从文档中清除未使用的样式和列表[CleanupOptions](../../com.aspose.words/cleanupoptions). |
| [clearSectionAttrs()](#clearSectionAttrs--) |  |
| [compare(Document document, String author, Date dateTime)](#compare-com.aspose.words.Document-java.lang.String-java.util.Date-) | 将此文档与另一个文档进行比较，以产生编辑和格式修订的数量[Revision](../../com.aspose.words/revision). |
| [compare(Document document, String author, Date dateTime, CompareOptions options)](#compare-com.aspose.words.Document-java.lang.String-java.util.Date-com.aspose.words.CompareOptions-) | 将此文档与另一个文档进行比较，从而产生一些编辑和格式修订[Revision](../../com.aspose.words/revision). |
| [copyStylesFromTemplate(Document template)](#copyStylesFromTemplate-com.aspose.words.Document-) | 将样式从指定模板复制到文档。 |
| [copyStylesFromTemplate(String template)](#copyStylesFromTemplate-java.lang.String-) | 将样式从指定模板复制到文档。 |
| [dd()](#dd--) |  |
| [deepClone()](#deepClone--) | 执行深拷贝[Document](../../com.aspose.words/document). |
| [deepClone(boolean isCloneChildren)](#deepClone-boolean-) | 创建节点的副本。 |
| [ensureMinimum()](#ensureMinimum--) | 如果文档不包含节，则创建一个节和一个段落。 |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [expandTableStylesToDirectFormatting()](#expandTableStylesToDirectFormatting--) | 将表格样式中指定的格式转换为文档中表格的直接格式。 |
| [extractPages(int index, int count)](#extractPages-int-int-) | 返回[Document](../../com.aspose.words/document)表示指定页面范围的对象。 |
| [fetchInheritedSectionAttr(int key)](#fetchInheritedSectionAttr-int-) |  |
| [fetchSectionAttr(int key)](#fetchSectionAttr-int-) |  |
| [get()](#get--) |  |
| [getAncestor(int ancestorType)](#getAncestor-int-) |  |
| [getAncestor(Class ancestorType)](#getAncestor-java.lang.Class-) | 获取指定对象类型的第一个祖先。 |
| [getAttachedTemplate()](#getAttachedTemplate--) | 获取附加到文档的模板的完整路径。 |
| [getAutomaticallyUpdateStyles()](#getAutomaticallyUpdateStyles--) | 获取一个标志，指示每次在 MS Word 中打开文档时，文档中的样式是否更新以匹配附加模板中的样式。 |
| [getBackgroundShape()](#getBackgroundShape--) | 获取文档的背景形状。 |
| [getBuiltInDocumentProperties()](#getBuiltInDocumentProperties--) | 返回一个集合，该集合表示文档的所有内置文档属性。 |
| [getChild(int nodeType, int index, boolean isDeep)](#getChild-int-int-boolean-) |  |
| [getChildNodes()](#getChildNodes--) | 获取此节点的所有直接子节点。 |
| [getChildNodes(int nodeType, boolean isDeep)](#getChildNodes-int-boolean-) |  |
| [getClass()](#getClass--) |  |
| [getCompatibilityOptions()](#getCompatibilityOptions--) | 提供对文档兼容性选项的访问（即，在**Compatibility**的选项卡**Options**Word 中的对话框）。 |
| [getCompliance()](#getCompliance--) | 获取根据加载的文档内容确定的 OOXML 合规性版本。 |
| [getContainer()](#getContainer--) |  |
| [getCount()](#getCount--) | 获取此节点的直接子节点数。 |
| [getCurrentNode()](#getCurrentNode--) |  |
| [getCustomDocumentProperties()](#getCustomDocumentProperties--) | 返回表示文档的所有自定义文档属性的集合。 |
| [getCustomNodeId()](#getCustomNodeId--) | 指定自定义节点标识符。 |
| [getCustomXmlParts()](#getCustomXmlParts--) | 获取自定义 XML 数据存储部件的集合。 |
| [getDefaultTabStop()](#getDefaultTabStop--) | 获取默认制表位之间的间隔（以磅为单位）。 |
| [getDigitalSignatures()](#getDigitalSignatures--) | 获取此文档的数字签名集合及其验证结果。 |
| [getDirectSectionAttr(int key)](#getDirectSectionAttr-int-) |  |
| [getDocument()](#getDocument--) |  |
| [getEndnoteOptions()](#getEndnoteOptions--) | 提供控制本文档中尾注编号和位置的选项。 |
| [getFieldOptions()](#getFieldOptions--) | 得到一个**FieldOptions**表示控制文档中字段处理的选项的对象。 |
| [getFirstChild()](#getFirstChild--) | 获取节点的第一个子节点。 |
| [getFirstSection()](#getFirstSection--) | 获取文档中的第一部分。 |
| [getFontInfos()](#getFontInfos--) | 提供对本文档中使用的字体属性的访问。 |
| [getFontSettings()](#getFontSettings--) | 获取文档字体设置。 |
| [getFootnoteOptions()](#getFootnoteOptions--) | 提供控制本文档中脚注编号和位置的选项。 |
| [getFrameset()](#getFrameset--) | 返回一个[getFrameset()](../../com.aspose.words/document\#getFrameset--)例如，如果此文档代表一个框架页面。 |
| [getGlossaryDocument()](#getGlossaryDocument--) | 获取此文档或模板中的词汇表文档。 |
| [getGrammarChecked()](#getGrammarChecked--) | 退货**true**如果文档已经过语法检查。 |
| [getHyphenationOptions()](#getHyphenationOptions--) | 提供对文档断字选项的访问。 |
| [getLastChild()](#getLastChild--) | 获取节点的最后一个子节点。 |
| [getLastSection()](#getLastSection--) | 获取文档中的最后一节。 |
| [getLayoutOptions()](#getLayoutOptions--) | 得到一个**LayoutOptions**表示控制此文档布局过程的选项的对象。 |
| [getLists()](#getLists--) | 提供对文档中使用的列表格式的访问。 |
| [getMailMerge()](#getMailMerge--) | 返回一个**MailMerge**表示文档的邮件合并功能的对象。 |
| [getMailMergeSettings()](#getMailMergeSettings--) | 获取包含文档的所有邮件合并信息的对象。 |
| [getNextMatchingNode(Node curNode)](#getNextMatchingNode-com.aspose.words.Node-) |  |
| [getNextSibling()](#getNextSibling--) | 获取紧跟此节点的节点。 |
| [getNodeChangingCallback()](#getNodeChangingCallback--) | 在文档中插入或删除节点时调用。 |
| [getNodeType()](#getNodeType--) | 退货**NodeType.Document**. |
| [getOriginalFileName()](#getOriginalFileName--) | 获取文档的原始文件名。 |
| [getOriginalLoadFormat()](#getOriginalLoadFormat--) | 获取加载到此对象中的原始文档的格式。 |
| [getPackageCustomParts()](#getPackageCustomParts--) | 获取使用“未知关系”链接到 OOXML 包的自定义部件（任意内容）的集合。 |
| [getPageColor()](#getPageColor--) | 获取文档的页面颜色。 |
| [getPageCount()](#getPageCount--) | 获取由最近的页面布局操作计算的文档中的页数。 |
| [getPageInfo(int pageIndex)](#getPageInfo-int-) | 获取可能对打印或呈现有用的页面的页面大小、方向和其他信息。 |
| [getParentNode()](#getParentNode--) | 获取此节点的直接父节点。 |
| [getPreviousSibling()](#getPreviousSibling--) | 获取紧接在此节点之前的节点。 |
| [getProtectionType()](#getProtectionType--) | 获取当前活动的文档保护类型。 |
| [getRange()](#getRange--) | 返回一个**Range**表示包含在此节点中的文档部分的对象。 |
| [getRemovePersonalInformation()](#getRemovePersonalInformation--) | 获取一个标志，表明 Microsoft Word 将在保存文档时从注释、修订和文档属性中删除所有用户信息。 |
| [getResourceLoadingCallback()](#getResourceLoadingCallback--) | 允许控制外部资源的加载方式。 |
| [getRevisions()](#getRevisions--) | 获取此文档中存在的修订（跟踪更改）的集合。 |
| [getRevisionsView()](#getRevisionsView--) | 获取一个值，该值指示是使用文档的原始版本还是修订版本。 |
| [getSections()](#getSections--) | 返回代表文档中所有部分的集合。 |
| [getShadeFormData()](#getShadeFormData--) | 指定是否打开表单域的灰色底纹。 |
| [getShowGrammaticalErrors()](#getShowGrammaticalErrors--) | 指定是否在此文档中显示语法错误。 |
| [getShowSpellingErrors()](#getShowSpellingErrors--) | 指定是否在此文档中显示拼写错误。 |
| [getSpellingChecked()](#getSpellingChecked--) | 退货**true**如果文档已经过拼写检查。 |
| [getStyles()](#getStyles--) | 返回文档中定义的样式集合。 |
| [getText()](#getText--) | 获取此节点及其所有子节点的文本。 |
| [getTheme()](#getTheme--) | 获取[getTheme()](../../com.aspose.words/document\#getTheme--)本文档的对象。 |
| [getTrackRevisions()](#getTrackRevisions--) | **True**在 Microsoft Word 中编辑此文档时是否跟踪更改。 |
| [getVariables()](#getVariables--) | 返回添加到文档或模板的变量集合。 |
| [getVbaProject()](#getVbaProject--) | 得到一个[getVbaProject()](../../com.aspose.words/document\#getVbaProject--) / [setVbaProject(com.aspose.words.VbaProject)](../../com.aspose.words/document\#setVbaProject-com.aspose.words.VbaProject-). |
| [getVersionsCount()](#getVersionsCount--) | 获取存储在 DOC 文档中的文档版本数。 |
| [getViewOptions()](#getViewOptions--) | 提供选项以控制文档在 Microsoft Word 中的显示方式。 |
| [getWarningCallback()](#getWarningCallback--) | 当检测到可能导致数据或格式保真度丢失的问题时，在各种文档处理过程中调用。 |
| [getWatermark()](#getWatermark--) | 提供对文档水印的访问。 |
| [getWebExtensionTaskPanes()](#getWebExtensionTaskPanes--) | 返回表示任务窗格加载项列表的集合。 |
| [getWriteProtection()](#getWriteProtection--) | 提供对文档写保护选项的访问。 |
| [hasChildNodes()](#hasChildNodes--) | 如果此节点有任何子节点，则返回 true。 |
| [hasMacros()](#hasMacros--) | 退货**true**如果文档有 VBA 项目（宏）。 |
| [hasRevisions()](#hasRevisions--) | 退货**true**如果文档有任何跟踪更改。 |
| [hashCode()](#hashCode--) |  |
| [importNode(Node srcNode, boolean isImportChildren)](#importNode-com.aspose.words.Node-boolean-) | 将节点从另一个文档导入到当前文档。 |
| [importNode(Node srcNode, boolean isImportChildren, int importFormatMode)](#importNode-com.aspose.words.Node-boolean-int-) |  |
| [indexOf(Node child)](#indexOf-com.aspose.words.Node-) | 返回子节点数组中指定子节点的索引。 |
| [insertAfter(Node newChild, Node refChild)](#insertAfter-com.aspose.words.Node-com.aspose.words.Node-) | 在指定的引用节点之后立即插入指定的节点。 |
| [insertBefore(Node newChild, Node refChild)](#insertBefore-com.aspose.words.Node-com.aspose.words.Node-) | 将指定节点插入到紧靠指定引用节点之前。 |
| [isComposite()](#isComposite--) | 返回 true，因为此节点可以有子节点。 |
| [iterator()](#iterator--) | 为该节点的子节点上的每个样式迭代提供支持。 |
| [joinRunsWithSameFormatting()](#joinRunsWithSameFormatting--) | 连接在文档的所有段落中以相同的格式运行。 |
| [nextPreOrder(Node rootNode)](#nextPreOrder-com.aspose.words.Node-) | 根据前序树遍历算法获取下一个节点。 |
| [nodeTypeToString(int nodeType)](#nodeTypeToString-int-) |  |
| [normalizeFieldTypes()](#normalizeFieldTypes--) | 更改字段类型值[FieldChar.getFieldType()](../../com.aspose.words/fieldchar\#getFieldType--)的[FieldStart](../../com.aspose.words/fieldstart), [FieldSeparator](../../com.aspose.words/fieldseparator), [FieldEnd](../../com.aspose.words/fieldend)在整个文档中，以便它们对应于域代码中包含的域类型。 |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [prependChild(Node newChild)](#prependChild-com.aspose.words.Node-) | 将指定节点添加到此节点的子节点列表的开头。 |
| [previousPreOrder(Node rootNode)](#previousPreOrder-com.aspose.words.Node-) | 根据前序树遍历算法获取上一个节点。 |
| [print()](#print--) | 打印文档而不显示任何用户界面表单。 |
| [print(String printerName)](#print-java.lang.String-) | 使用标准（无用户界面）打印控制器将整个文档打印到指定的打印机。 |
| [print(AttributeSet printerSettings)](#print-javax.print.attribute.AttributeSet-) | 根据指定的打印机设置，使用标准（无用户界面）打印控制器打印文档。 |
| [print(AttributeSet printerSettings, String documentName)](#print-javax.print.attribute.AttributeSet-java.lang.String-) | 根据指定的打印机设置打印文档，使用标准（无用户界面）打印控制器和文档名称。 |
| [protect(int type)](#protect-int-) |  |
| [protect(int type, String password)](#protect-int-java.lang.String-) |  |
| [remove()](#remove--) |  |
| [removeAllChildren()](#removeAllChildren--) | 移除当前节点的所有子节点。 |
| [removeChild(Node oldChild)](#removeChild-com.aspose.words.Node-) | 删除指定的子节点。 |
| [removeExternalSchemaReferences()](#removeExternalSchemaReferences--) | 从此文档中删除外部 XML 架构引用。 |
| [removeMacros()](#removeMacros--) | 从文档中删除所有宏（VBA 项目）以及工具栏和命令自定义项。 |
| [removeSmartTags()](#removeSmartTags--) | 删除所有[SmartTag](../../com.aspose.words/smarttag)当前节点的后代节点。 |
| [renderToScale(int pageIndex, Graphics2D graphics, float x, float y, float scale)](#renderToScale-int-java.awt.Graphics2D-float-float-float-) | 将文档页面呈现为指定比例的对象。 |
| [renderToSize(int pageIndex, Graphics2D graphics, float x, float y, float width, float height)](#renderToSize-int-java.awt.Graphics2D-float-float-float-float-) | 将文档页面呈现为指定大小的对象。 |
| [save(OutputStream stream, SaveOptions saveOptions)](#save-java.io.OutputStream-com.aspose.words.SaveOptions-) |  |
| [save(OutputStream stream, int saveFormat)](#save-java.io.OutputStream-int-) |  |
| [save(String fileName)](#save-java.lang.String-) | 保存文档。 |
| [save(String fileName, SaveOptions saveOptions)](#save-java.lang.String-com.aspose.words.SaveOptions-) | 使用指定的保存选项将文档保存到文件。 |
| [save(String fileName, int saveFormat)](#save-java.lang.String-int-) |  |
| [selectNodes(String xpath)](#selectNodes-java.lang.String-) | 选择与 XPath 表达式匹配的节点列表。 |
| [selectSingleNode(String xpath)](#selectSingleNode-java.lang.String-) | 选择与 XPath 表达式匹配的第一个节点。 |
| [setAttachedTemplate(String value)](#setAttachedTemplate-java.lang.String-) | 设置附加到文档的模板的完整路径。 |
| [setAutomaticallyUpdateStyles(boolean value)](#setAutomaticallyUpdateStyles-boolean-) | 设置一个标志，指示每次在 MS Word 中打开文档时，文档中的样式是否更新以匹配附加模板中的样式。 |
| [setBackgroundShape(Shape value)](#setBackgroundShape-com.aspose.words.Shape-) | 设置文档的背景形状。 |
| [setCustomNodeId(int value)](#setCustomNodeId-int-) | 指定自定义节点标识符。 |
| [setCustomXmlParts(CustomXmlPartCollection value)](#setCustomXmlParts-com.aspose.words.CustomXmlPartCollection-) | 设置自定义 XML 数据存储部件的集合。 |
| [setDefaultTabStop(double value)](#setDefaultTabStop-double-) | 设置默认制表位之间的间隔（以磅为单位）。 |
| [setFontSettings(FontSettings value)](#setFontSettings-com.aspose.words.FontSettings-) | 设置文档字体设置。 |
| [setGlossaryDocument(GlossaryDocument value)](#setGlossaryDocument-com.aspose.words.GlossaryDocument-) | 在此文档或模板中设置词汇表文档。 |
| [setGrammarChecked(boolean value)](#setGrammarChecked-boolean-) | 退货**true**如果文档已经过语法检查。 |
| [setMailMergeSettings(MailMergeSettings value)](#setMailMergeSettings-com.aspose.words.MailMergeSettings-) | 设置包含文档的所有邮件合并信息的对象。 |
| [setNodeChangingCallback(INodeChangingCallback value)](#setNodeChangingCallback-com.aspose.words.INodeChangingCallback-) | 在文档中插入或删除节点时调用。 |
| [setPackageCustomParts(CustomPartCollection value)](#setPackageCustomParts-com.aspose.words.CustomPartCollection-) | 设置使用“未知关系”链接到 OOXML 包的自定义部分（任意内容）的集合。 |
| [setPageColor(Color value)](#setPageColor-java.awt.Color-) | 设置文档的页面颜色。 |
| [setRemovePersonalInformation(boolean value)](#setRemovePersonalInformation-boolean-) | 设置一个标志，表明 Microsoft Word 将在保存文档时从注释、修订和文档属性中删除所有用户信息。 |
| [setResourceLoadingCallback(IResourceLoadingCallback value)](#setResourceLoadingCallback-com.aspose.words.IResourceLoadingCallback-) | 允许控制外部资源的加载方式。 |
| [setRevisionsView(int value)](#setRevisionsView-int-) | 设置一个值，该值指示是使用文档的原始版本还是修订版本。 |
| [setSectionAttr(int key, Object value)](#setSectionAttr-int-java.lang.Object-) |  |
| [setShadeFormData(boolean value)](#setShadeFormData-boolean-) | 指定是否打开表单域的灰色底纹。 |
| [setShowGrammaticalErrors(boolean value)](#setShowGrammaticalErrors-boolean-) | 指定是否在此文档中显示语法错误。 |
| [setShowSpellingErrors(boolean value)](#setShowSpellingErrors-boolean-) | 指定是否在此文档中显示拼写错误。 |
| [setSpellingChecked(boolean value)](#setSpellingChecked-boolean-) | 退货**true**如果文档已经过拼写检查。 |
| [setTrackRevisions(boolean value)](#setTrackRevisions-boolean-) | **True**在 Microsoft Word 中编辑此文档时是否跟踪更改。 |
| [setVbaProject(VbaProject value)](#setVbaProject-com.aspose.words.VbaProject-) | 设置一个[getVbaProject()](../../com.aspose.words/document\#getVbaProject--) / [setVbaProject(com.aspose.words.VbaProject)](../../com.aspose.words/document\#setVbaProject-com.aspose.words.VbaProject-). |
| [setWarningCallback(IWarningCallback value)](#setWarningCallback-com.aspose.words.IWarningCallback-) | 当检测到可能导致数据或格式保真度丢失的问题时，在各种文档处理过程中调用。 |
| [startTrackRevisions(String author)](#startTrackRevisions-java.lang.String-) | 开始自动将您以编程方式对文档所做的所有进一步更改标记为修订更改。 |
| [startTrackRevisions(String author, Date dateTime)](#startTrackRevisions-java.lang.String-java.util.Date-) | 开始自动将您以编程方式对文档所做的所有进一步更改标记为修订更改。 |
| [stopTrackRevisions()](#stopTrackRevisions--) | 停止将文档更改自动标记为修订。 |
| [toString()](#toString--) |  |
| [toString(SaveOptions saveOptions)](#toString-com.aspose.words.SaveOptions-) | 使用指定的保存选项将节点的内容导出为字符串。 |
| [toString(int saveFormat)](#toString-int-) |  |
| [unlink字段()](#unlink字段--) | 取消链接整个文档中的字段。 |
| [unprotect()](#unprotect--) | 取消对文档的保护。 |
| [unprotect(String password)](#unprotect-java.lang.String-) | 如果指定了正确的密码，则从文档中删除保护。 |
| [update字段()](#update字段--) | 更新整个文档中的字段值。 |
| [updateListLabels()](#updateListLabels--) | 更新文档中所有列表项的列表标签。 |
| [updatePageLayout()](#updatePageLayout--) | 重建文档的页面布局。 |
| [updateTableLayout()](#updateTableLayout--) | 实施一种较早的方法来重新计算具有已知问题的表列宽度。 |
| [updateThumbnail()](#updateThumbnail--) | 更新[BuiltInDocumentProperties.getThumbnail()](../../com.aspose.words/builtindocumentproperties\#getThumbnail--) / [BuiltInDocumentProperties.setThumbnail(byte[])](../../com.aspose.words/builtindocumentproperties\#setThumbnail-byte---)使用默认选项的文档。 |
| [updateThumbnail(ThumbnailGeneratingOptions options)](#updateThumbnail-com.aspose.words.ThumbnailGeneratingOptions-) | 更新[BuiltInDocumentProperties.getThumbnail()](../../com.aspose.words/builtindocumentproperties\#getThumbnail--) / [BuiltInDocumentProperties.setThumbnail(byte[])](../../com.aspose.words/builtindocumentproperties\#setThumbnail-byte---)根据指定的选项的文档。 |
| [updateWordCount()](#updateWordCount--) | 更新文档的字数统计属性。 |
| [updateWordCount(boolean updateLinesCount)](#updateWordCount-boolean-) | 更新文档的字数统计属性，可选择更新[BuiltInDocumentProperties.getLines()](../../com.aspose.words/builtindocumentproperties\#getLines--) / [BuiltInDocumentProperties.setLines(int)](../../com.aspose.words/builtindocumentproperties\#setLines-int-)财产。 |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### Document() {#Document--}
```
public Document()
```


创建或加载文档。创建一个空白 Word 文档。

文档纸张尺寸默认为 Letter。如果要更改页面设置，请使用[Section.getPageSetup()](../../com.aspose.words/section\#getPageSetup--).

创建后，您可以使用[DocumentBuilder](../../com.aspose.words/documentbuilder)轻松添加文档内容。

### Document(String fileName) {#Document-java.lang.String-}
```
public Document(String fileName)
```


从文件中打开现有文档。自动检测文件格式。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| fileName | java.lang.String | 要打开的文档的文件名。 |

### Document(String fileName, LoadOptions loadOptions) {#Document-java.lang.String-com.aspose.words.LoadOptions-}
```
public Document(String fileName, LoadOptions loadOptions)
```


从文件中打开现有文档。允许指定其他选项，例如加密密码。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| fileName | java.lang.String | 要打开的文档的文件名。 |
| loadOptions | [LoadOptions](../../com.aspose.words/loadoptions) | 加载文档时使用的其他选项。可以为空。 |

### Document(InputStream stream) {#Document-java.io.InputStream-}
```
public Document(InputStream stream)
```


初始化此类的新实例。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| stream | java.io.InputStream |  |

### Document(InputStream stream, LoadOptions loadOptions) {#Document-java.io.InputStream-com.aspose.words.LoadOptions-}
```
public Document(InputStream stream, LoadOptions loadOptions)
```


初始化此类的新实例。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| stream | java.io.InputStream |  |
| loadOptions | [LoadOptions](../../com.aspose.words/loadoptions) |  |

### accept(DocumentVisitor visitor) {#accept-com.aspose.words.DocumentVisitor-}
```
public boolean accept(DocumentVisitor visitor)
```


接受访客。

枚举此节点及其所有子节点。每个节点调用 DocumentVisitor 上的相应方法。

有关更多信息，请参阅访问者设计模式。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| visitor | [DocumentVisitor](../../com.aspose.words/documentvisitor) | 将访问节点的访问者。 |

**退货:**
boolean - 如果访问了所有节点则为真；如果 DocumentVisitor 在访问所有节点之前停止操作，则为 false。调用 DocumentVisitor.VisitDocumentStart，然后为文档的所有子节点调用 Accept，最后调用 DocumentVisitor.VisitDocumentEnd。
### acceptAllRevisions() {#acceptAllRevisions--}
```
public void acceptAllRevisions()
```


接受文档中的所有修订。这个方法是一个捷径[RevisionCollection.acceptAll()](../../com.aspose.words/revisioncollection\#acceptAll--).

### add(Shape watermark) {#add-com.aspose.words.Shape-}
```
public void add(Shape watermark)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| watermark | [Shape](../../com.aspose.words/shape) |  |

### appendChild(Node newChild) {#appendChild-com.aspose.words.Node-}
```
public Node appendChild(Node newChild)
```


将指定节点添加到此节点的子节点列表的末尾。

如果 newChild 已经在树中，则首先将其移除。

如果要插入的节点是从另一个文档创建的，您应该使用**M:Aspose.Words.DocumentBase.ImportNode(Aspose.Words.Node,System.Boolean,Aspose.Words.ImportFormatMode)**将节点导入当前文档。然后可以将导入的节点插入到当前文档中。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| newChild | [Node](../../com.aspose.words/node) | 要添加的节点。 |

**退货:**
[Node](../../com.aspose.words/node) - 添加的节点。
### appendDocument(Document srcDoc, int importFormatMode) {#appendDocument-com.aspose.words.Document-int-}
```
public void appendDocument(Document srcDoc, int importFormatMode)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| srcDoc | [Document](../../com.aspose.words/document) |  |
| importFormatMode | int |  |

### appendDocument(Document srcDoc, int importFormatMode, ImportFormatOptions importFormatOptions) {#appendDocument-com.aspose.words.Document-int-com.aspose.words.ImportFormatOptions-}
```
public void appendDocument(Document srcDoc, int importFormatMode, ImportFormatOptions importFormatOptions)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| srcDoc | [Document](../../com.aspose.words/document) |  |
| importFormatMode | int |  |
| importFormatOptions | [ImportFormatOptions](../../com.aspose.words/importformatoptions) |  |

### cleanup() {#cleanup--}
```
public void cleanup()
```


从文档中清除未使用的样式和列表。

### cleanup(CleanupOptions options) {#cleanup-com.aspose.words.CleanupOptions-}
```
public void cleanup(CleanupOptions options)
```


根据给定的内容从文档中清除未使用的样式和列表[CleanupOptions](../../com.aspose.words/cleanupoptions).

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| options | [CleanupOptions](../../com.aspose.words/cleanupoptions) |  |

### clearSectionAttrs() {#clearSectionAttrs--}
```
public void clearSectionAttrs()
```




### compare(Document document, String author, Date dateTime) {#compare-com.aspose.words.Document-java.lang.String-java.util.Date-}
```
public void compare(Document document, String author, Date dateTime)
```


将此文档与另一个文档进行比较，以产生编辑和格式修订的数量[Revision](../../com.aspose.words/revision).

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| document | [Document](../../com.aspose.words/document) | 要比较的文档。 |
| author | java.lang.String | 用于修订的作者姓名缩写。 |
| dateTime | java.util.Date | 用于修订的日期和时间。目前不比较以下文档节点：

 *  [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag)
 *  第 3 项

文件在比较前不得有修改。|

### compare(Document document, String author, Date dateTime, CompareOptions options) {#compare-com.aspose.words.Document-java.lang.String-java.util.Date-com.aspose.words.CompareOptions-}
```
public void compare(Document document, String author, Date dateTime, CompareOptions options)
```


将此文档与另一个文档进行比较，从而产生一些编辑和格式修订[Revision](../../com.aspose.words/revision) .允许使用指定比较选项[CompareOptions](../../com.aspose.words/compareoptions).

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| document | [Document](../../com.aspose.words/document) |  |
| author | java.lang.String |  |
| dateTime | java.util.Date |  |
| options | [CompareOptions](../../com.aspose.words/compareoptions) |  |

### copyStylesFromTemplate(Document template) {#copyStylesFromTemplate-com.aspose.words.Document-}
```
public void copyStylesFromTemplate(Document template)
```


将样式从指定模板复制到文档。当样式从模板复制到文档时，文档中的同名样式会重新定义以匹配模板中的样式描述。模板中的独特样式被复制到文档中。文档中的独特样式保持不变。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| template | [Document](../../com.aspose.words/document) |  |

### copyStylesFromTemplate(String template) {#copyStylesFromTemplate-java.lang.String-}
```
public void copyStylesFromTemplate(String template)
```


将样式从指定模板复制到文档。当样式从模板复制到文档时，文档中的同名样式会重新定义以匹配模板中的样式描述。模板中的独特样式被复制到文档中。文档中的独特样式保持不变。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| template | java.lang.String |  |

### dd() {#dd--}
```
public void dd()
```




### deepClone() {#deepClone--}
```
public Document deepClone()
```


执行深拷贝[Document](../../com.aspose.words/document).

**退货:**
[Document](../../com.aspose.words/document) - 克隆的文档。
### deepClone(boolean isCloneChildren) {#deepClone-boolean-}
```
public Node deepClone(boolean isCloneChildren)
```


创建节点的副本。

此方法用作节点的复制构造函数。克隆的节点没有父节点，但与原始节点属于同一个文档。

此方法始终执行节点的深层复制。这*isCloneChildren*参数指定是否也执行复制所有子节点。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| isCloneChildren | boolean | True 递归克隆指定节点下的子树； false 仅克隆节点本身。 |

**退货:**
[Node](../../com.aspose.words/node) - 克隆的节点。
### ensureMinimum() {#ensureMinimum--}
```
public void ensureMinimum()
```


如果文档不包含节，则创建一个节和一个段落。

### equals(Object arg0) {#equals-java.lang.Object-}
```
public boolean equals(Object arg0)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**退货:**
布尔值
### expandTableStylesToDirectFormatting() {#expandTableStylesToDirectFormatting--}
```
public void expandTableStylesToDirectFormatting()
```


将表格样式中指定的格式转换为文档中表格的直接格式。

这个方法存在是因为这个版本的 Aspose.Words 只提供对表格样式的有限支持（见下文）。当您加载包含使用表格样式格式化的表格的 DOCX 或 WordprocessingML 文档并且您需要查询表格、单元格、段落或文本的格式时，此方法可能很有用。

此版本的 Aspose.Words 对表格样式提供有限支持，如下所示：

 *  在将文档另存为 DOCX 或 WordprocessingML 时，在 DOCX 或 WordprocessingML 文档中定义的表格样式将保留为表格样式。
 *  在将文档保存为任何其他格式、渲染或打印时，DOCX 或 WordprocessingML 文档中定义的表格样式会自动转换为表格的直接格式。
 *  当仅将文档另存为 DOC 时，DOC 文档中定义的表格样式将保留为表格样式。

### extractPages(int index, int count) {#extractPages-int-int-}
```
public Document extractPages(int index, int count)
```


返回[Document](../../com.aspose.words/document)表示指定页面范围的对象。生成的文档应该看起来像 MS Word 中的文档，就像我们执行了“打印特定页面”一样\\u2013 编号、页眉/页脚和交叉表布局将被保留。但是由于大量的细微差别，在减少页数的同时出现，完全匹配版面是一项安静复杂的工作，需要付出很多努力。根据文档的复杂性，与源文档相比，生成的文档内容布局可能会略有不同。任何反馈将不胜感激。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| index | int | 要提取的第一页的从零开始的索引。 |
| count | int | 要提取的页数。 |

**退货:**
[Document](../../com.aspose.words/document)
### fetchInheritedSectionAttr(int key) {#fetchInheritedSectionAttr-int-}
```
public Object fetchInheritedSectionAttr(int key)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| key | int |  |

**退货:**
java.lang.Object
### fetchSectionAttr(int key) {#fetchSectionAttr-int-}
```
public Object fetchSectionAttr(int key)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| key | int |  |

**退货:**
java.lang.Object
### get() {#get--}
```
public Shape get()
```




**退货:**
[Shape](../../com.aspose.words/shape)
### getAncestor(int ancestorType) {#getAncestor-int-}
```
public CompositeNode getAncestor(int ancestorType)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| ancestorType | int |  |

**退货:**
[CompositeNode](../../com.aspose.words/compositenode)
### getAncestor(Class ancestorType) {#getAncestor-java.lang.Class-}
```
public CompositeNode getAncestor(Class ancestorType)
```


获取指定对象类型的第一个祖先。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| ancestorType | java.lang.Class | 要检索的祖先的对象类型。 |

**退货:**
[CompositeNode](../../com.aspose.words/compositenode) - 指定类型的祖先，如果没有找到该类型的祖先，则返回 null。

如果祖先类型等于祖先类型或从祖先类型派生，则祖先类型匹配。
### getAttachedTemplate() {#getAttachedTemplate--}
```
public String getAttachedTemplate()
```


获取附加到文档的模板的完整路径。

空字符串表示文档附加到 Normal 模板。

**退货:**
java.lang.String - 附加到文档的模板的完整路径。
### getAutomaticallyUpdateStyles() {#getAutomaticallyUpdateStyles--}
```
public boolean getAutomaticallyUpdateStyles()
```


获取一个标志，指示每次在 MS Word 中打开文档时，文档中的样式是否更新以匹配附加模板中的样式。

**退货:**
布尔值 - 指示每次在 MS Word 中打开文档时文档中的样式是否更新以匹配附加模板中的样式的标志。
### getBackgroundShape() {#getBackgroundShape--}
```
public Shape getBackgroundShape()
```


获取文档的背景形状。可以为空。

Microsoft Word 只允许具有其[ShapeBase.getShapeType()](../../com.aspose.words/shapebase\#getShapeType--)属性等于[ShapeType.RECTANGLE](../../com.aspose.words/shapetype\#RECTANGLE)用作文档的背景形状。

Microsoft Word 仅支持背景形状的填充属性。所有其他属性都被忽略。

将此属性设置为非空值也将设置[ViewOptions.getDisplayBackgroundShape()](../../com.aspose.words/viewoptions\#getDisplayBackgroundShape--) / [ViewOptions.setDisplayBackgroundShape(boolean)](../../com.aspose.words/viewoptions\#setDisplayBackgroundShape-boolean-)为真。

**退货:**
[Shape](../../com.aspose.words/shape) - 文档的背景形状。
### getBuiltInDocumentProperties() {#getBuiltInDocumentProperties--}
```
public BuiltInDocumentProperties getBuiltInDocumentProperties()
```


返回一个集合，该集合表示文档的所有内置文档属性。

**退货:**
[BuiltInDocumentProperties](../../com.aspose.words/builtindocumentproperties) - 表示文档的所有内置文档属性的集合。
### getChild(int nodeType, int index, boolean isDeep) {#getChild-int-int-boolean-}
```
public Node getChild(int nodeType, int index, boolean isDeep)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| nodeType | int |  |
| index | int |  |
| isDeep | boolean |  |

**退货:**
[Node](../../com.aspose.words/node)
### getChildNodes() {#getChildNodes--}
```
public NodeCollection getChildNodes()
```


获取此节点的所有直接子节点。

笔记，[getChildNodes()](../../com.aspose.words/compositenode\#getChildNodes--)相当于调用 GetChildNodes(NodeType.Any, false) 并在每次访问时创建并返回一个新集合。

如果没有子节点，则此属性返回一个空集合。

**退货:**
[NodeCollection](../../com.aspose.words/nodecollection) - 该节点的所有直接子节点。
### getChildNodes(int nodeType, boolean isDeep) {#getChildNodes-int-boolean-}
```
public NodeCollection getChildNodes(int nodeType, boolean isDeep)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| nodeType | int |  |
| isDeep | boolean |  |

**退货:**
[NodeCollection](../../com.aspose.words/nodecollection)
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**退货:**
java.lang.Class<?>
### getCompatibilityOptions() {#getCompatibilityOptions--}
```
public CompatibilityOptions getCompatibilityOptions()
```


提供对文档兼容性选项的访问（即，在**Compatibility**的选项卡**Options**Word 中的对话框）。

**退货:**
[CompatibilityOptions](../../com.aspose.words/compatibilityoptions) - 相应的[CompatibilityOptions](../../com.aspose.words/compatibilityoptions)价值。
### getCompliance() {#getCompliance--}
```
public int getCompliance()
```


获取根据加载的文档内容确定的 OOXML 合规性版本。仅对 OOXML 文档有意义。

如果您创建了一个新的空白文档或加载非 OOXML 文档，则返回[OoxmlCompliance.ECMA\_376\_2006](../../com.aspose.words/ooxmlcompliance\#ECMA-376-2006)价值。

**退货:**
int - 根据加载的文档内容确定的 OOXML 合规版本。返回值是以下之一[OoxmlCompliance](../../com.aspose.words/ooxmlcompliance)常数。
### getContainer() {#getContainer--}
```
public CompositeNode getContainer()
```




**退货:**
[CompositeNode](../../com.aspose.words/compositenode)
### getCount() {#getCount--}
```
public int getCount()
```


获取此节点的直接子节点数。

**退货:**
int - 此节点的直接子节点数。
### getCurrentNode() {#getCurrentNode--}
```
public Node getCurrentNode()
```




**退货:**
[Node](../../com.aspose.words/node)
### getCustomDocumentProperties() {#getCustomDocumentProperties--}
```
public CustomDocumentProperties getCustomDocumentProperties()
```


返回表示文档的所有自定义文档属性的集合。

**退货:**
[CustomDocumentProperties](../../com.aspose.words/customdocumentproperties) 表示文档的所有自定义文档属性的集合。
### getCustomNodeId() {#getCustomNodeId--}
```
public int getCustomNodeId()
```


指定自定义节点标识符。

默认为零。

这个标识符可以任意设置和使用。例如，作为获取外部数据的键。

重要说明，指定的值不会保存到输出文件中，并且仅在节点生命周期内存在。

**退货:**
int - 对应的 int 值。
### getCustomXmlParts() {#getCustomXmlParts--}
```
public CustomXmlPartCollection getCustomXmlParts()
```


获取自定义 XML 数据存储部件的集合。

Aspose.Words 仅将自定义 XML 部件加载和保存到 OOXML 和 DOC 文档中。

此属性不能为 null 。

**退货:**
[CustomXmlPartCollection](../../com.aspose.words/customxmlpartcollection) 自定义 XML 数据存储部件的集合。
### getDefaultTabStop() {#getDefaultTabStop--}
```
public double getDefaultTabStop()
```


获取默认制表位之间的间隔（以磅为单位）。

**退货:**
double - 默认制表位之间的间隔（以磅为单位）。
### getDigitalSignatures() {#getDigitalSignatures--}
```
public DigitalSignatureCollection getDigitalSignatures()
```


获取此文档的数字签名集合及其验证结果。

此集合包含从原始文档加载的数字签名。保存时不会保存这些数字签名[Document](../../com.aspose.words/document)对象到文件或流中，因为保存或转换将生成与原始文件不同的文档，并且原始数字签名将不再有效。

此集合永远不会为空。如果文档未签名，它将包含零个元素。

**退货:**
[DigitalSignatureCollection](../../com.aspose.words/digitalsignaturecollection) - 本文档的数字签名集合及其验证结果。
### getDirectSectionAttr(int key) {#getDirectSectionAttr-int-}
```
public Object getDirectSectionAttr(int key)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| key | int |  |

**退货:**
java.lang.Object
### getDocument() {#getDocument--}
```
public DocumentBase getDocument()
```


获取该节点所属的文档。

该节点始终属于一个文档，即使它刚刚创建但尚未添加到树中，或者已从树中删除。

**退货:**
[DocumentBase](../../com.aspose.words/documentbase)
### getEndnoteOptions() {#getEndnoteOptions--}
```
public EndnoteOptions getEndnoteOptions()
```


提供控制本文档中尾注编号和位置的选项。

**退货:**
[EndnoteOptions](../../com.aspose.words/endnoteoptions) - 相应的[EndnoteOptions](../../com.aspose.words/endnoteoptions)价值。
### getFieldOptions() {#getFieldOptions--}
```
public FieldOptions getFieldOptions()
```


得到一个**FieldOptions**表示控制文档中字段处理的选项的对象。

**退货:**
[FieldOptions](../../com.aspose.words/fieldoptions) - 一个**FieldOptions**表示控制文档中字段处理的选项的对象。
### getFirstChild() {#getFirstChild--}
```
public Node getFirstChild()
```


获取节点的第一个子节点。如果没有第一个子节点，则返回 null。

**退货:**
[Node](../../com.aspose.words/node) - 节点的第一个子节点。
### getFirstSection() {#getFirstSection--}
```
public Section getFirstSection()
```


获取文档中的第一部分。如果没有节，则返回 null。

**退货:**
[Section](../../com.aspose.words/section) - 文档的第一部分。
### getFontInfos() {#getFontInfos--}
```
public FontInfoCollection getFontInfos()
```


提供对本文档中使用的字体属性的访问。

此字体定义集合按原样从文档中加载。在某些文档中，字体定义可能是可选的、缺失的或不完整的。

不要依赖此集合来确定文档中使用了特定字体。您应该只使用此集合来获取有关文档中可能使用的字体的信息。

**退货:**
[FontInfoCollection](../../com.aspose.words/fontinfocollection) - 相应的[FontInfoCollection](../../com.aspose.words/fontinfocollection)价值。
### getFontSettings() {#getFontSettings--}
```
public FontSettings getFontSettings()
```


获取文档字体设置。

此属性允许为每个文档指定字体设置。如果设置为空，默认静态字体设置[FontSettings.getDefaultInstance()](../../com.aspose.words/fontsettings\#getDefaultInstance--)将会被使用。

默认值为空。

**退货:**
[FontSettings](../../com.aspose.words/fontsettings) 文档字体设置。
### getFootnoteOptions() {#getFootnoteOptions--}
```
public FootnoteOptions getFootnoteOptions()
```


提供控制本文档中脚注编号和位置的选项。

**退货:**
[FootnoteOptions](../../com.aspose.words/footnoteoptions) - 相应的[FootnoteOptions](../../com.aspose.words/footnoteoptions)价值。
### getFrameset() {#getFrameset--}
```
public Frameset getFrameset()
```


返回一个[getFrameset()](../../com.aspose.words/document\#getFrameset--)例如，如果此文档代表一个框架页面。如果文档未加框，则该属性具有**null**价值。

**退货:**
[Frameset](../../com.aspose.words/frameset) - 一个[getFrameset()](../../com.aspose.words/document\#getFrameset--)例如，如果此文档代表一个框架页面。
### getGlossaryDocument() {#getGlossaryDocument--}
```
public GlossaryDocument getGlossaryDocument()
```


获取此文档或模板中的词汇表文档。词汇表文档是文档中定义的自动图文集、自动更正和构建块条目的存储。

如果文档没有词汇表文档，则此属性返回 null。

您可以通过创建[GlossaryDocument](../../com.aspose.words/glossarydocument)对象并分配给该属性。

**退货:**
[GlossaryDocument](../../com.aspose.words/glossarydocument) - 本文档或模板中的词汇表文档。
### getGrammarChecked() {#getGrammarChecked--}
```
public boolean getGrammarChecked()
```


退货**true**如果文档已经过语法检查。要重新检查文档中的语法，请将此属性设置为**false**.

**退货:**
布尔值 -**true**如果文档已经过语法检查。
### getHyphenationOptions() {#getHyphenationOptions--}
```
public HyphenationOptions getHyphenationOptions()
```


提供对文档断字选项的访问。

**退货:**
[HyphenationOptions](../../com.aspose.words/hyphenationoptions) - 相应的[HyphenationOptions](../../com.aspose.words/hyphenationoptions)价值。
### getLastChild() {#getLastChild--}
```
public Node getLastChild()
```


获取节点的最后一个子节点。如果没有最后一个子节点，则返回 null。

**退货:**
[Node](../../com.aspose.words/node) - 节点的最后一个子节点。
### getLastSection() {#getLastSection--}
```
public Section getLastSection()
```


获取文档中的最后一部分。如果没有节，则返回 null。

**退货:**
[Section](../../com.aspose.words/section) - 文档的最后一部分。
### getLayoutOptions() {#getLayoutOptions--}
```
public LayoutOptions getLayoutOptions()
```


得到一个**LayoutOptions**表示控制此文档布局过程的选项的对象。

**退货:**
[LayoutOptions](../../com.aspose.words/layoutoptions) - 一个**LayoutOptions**表示控制此文档布局过程的选项的对象。
### getLists() {#getLists--}
```
public ListCollection getLists()
```


提供对文档中使用的列表格式的访问。

有关更多信息，请参阅[ListCollection](../../com.aspose.words/listcollection)班级。

**退货:**
[ListCollection](../../com.aspose.words/listcollection) - 相应的[ListCollection](../../com.aspose.words/listcollection)价值。
### getMailMerge() {#getMailMerge--}
```
public MailMerge getMailMerge()
```


返回一个**MailMerge**表示文档的邮件合并功能的对象。

**退货:**
[MailMerge](../../com.aspose.words/mailmerge) - 一个**MailMerge**表示文档的邮件合并功能的对象。
### getMailMergeSettings() {#getMailMergeSettings--}
```
public MailMergeSettings getMailMergeSettings()
```


获取包含文档的所有邮件合并信息的对象。

您可以使用此对象为文档指定邮件合并数据源，当用户打开此文档时，此信息（连同可用的数据字段）将出现在 Microsoft Word 中。或者，您可以使用此对象查询用户在 Microsoft Word 中为此文档指定的邮件合并设置。

该对象永远不会为空。

**退货:**
[MailMergeSettings](../../com.aspose.words/mailmergesettings) - 包含文档的所有邮件合并信息的对象。
### getNextMatchingNode(Node curNode) {#getNextMatchingNode-com.aspose.words.Node-}
```
public Node getNextMatchingNode(Node curNode)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| curNode | [Node](../../com.aspose.words/node) |  |

**退货:**
[Node](../../com.aspose.words/node)
### getNextSibling() {#getNextSibling--}
```
public Node getNextSibling()
```


获取紧跟在该节点之后的节点。如果没有下一个节点，则返回 null。

**退货:**
[Node](../../com.aspose.words/node) - 紧接此节点之后的节点。
### getNodeChangingCallback() {#getNodeChangingCallback--}
```
public INodeChangingCallback getNodeChangingCallback()
```


在文档中插入或删除节点时调用。

**退货:**
[INodeChangingCallback](../../com.aspose.words/inodechangingcallback) - 相应的[INodeChangingCallback](../../com.aspose.words/inodechangingcallback)价值。
### getNodeType() {#getNodeType--}
```
public int getNodeType()
```


退货**NodeType.Document**.

**退货:**
整数 -**NodeType.Document** .返回值是其中之一[NodeType](../../com.aspose.words/nodetype)常数。
### getOriginalFileName() {#getOriginalFileName--}
```
public String getOriginalFileName()
```


获取文档的原始文件名。

如果文档是从流中加载或创建为空白，则返回 null。

**退货:**
java.lang.String - 文档的原始文件名。
### getOriginalLoadFormat() {#getOriginalLoadFormat--}
```
public int getOriginalLoadFormat()
```


获取加载到此对象中的原始文档的格式。

如果您创建了一个新的空白文档，则返回[LoadFormat.DOC](../../com.aspose.words/loadformat\#DOC)价值。

**退货:**
int - 加载到此对象中的原始文档的格式。返回值是以下之一[LoadFormat](../../com.aspose.words/loadformat)常数。
### getPackageCustomParts() {#getPackageCustomParts--}
```
public CustomPartCollection getPackageCustomParts()
```


获取使用“未知关系”链接到 OOXML 包的自定义部件（任意内容）的集合。

不要将这些自定义部分与自定义 XML 数据混淆。如果您需要访问自定义 XML 部件，请使用[getCustomXmlParts()](../../com.aspose.words/document\#getCustomXmlParts--) / [setCustomXmlParts(com.aspose.words.CustomXmlPartCollection)](../../com.aspose.words/document\#setCustomXmlParts-com.aspose.words.CustomXmlPartCollection-)财产。

此集合包含 OOXML 部分，其父项是 OOXML 包，并且它们的目标是“未知关系”。有关更多信息，请参阅[CustomPart](../../com.aspose.words/custompart).

Aspose.Words 仅将自定义部件加载和保存到 OOXML 文档中。

此属性不能为 null 。

**退货:**
[CustomPartCollection](../../com.aspose.words/custompartcollection) - 使用“未知关系”链接到 OOXML 包的自定义部分（任意内容）的集合。
### getPageColor() {#getPageColor--}
```
public Color getPageColor()
```


获取文档的页面颜色。这个属性是一个更简单的版本[getBackgroundShape()](../../com.aspose.words/documentbase\#getBackgroundShape--) / [setBackgroundShape(com.aspose.words.Shape)](../../com.aspose.words/documentbase\#setBackgroundShape-com.aspose.words.Shape-).

此属性提供了一种为文档指定纯色页面颜色的简单方法。设置此属性会创建并设置一个适当的[getBackgroundShape()](../../com.aspose.words/documentbase\#getBackgroundShape--) / [setBackgroundShape(com.aspose.words.Shape)](../../com.aspose.words/documentbase\#setBackgroundShape-com.aspose.words.Shape-).

如果未设置页面颜色（例如文档中没有背景形状），则返回零颜色。

**退货:**
java.awt.Color - 文档的页面颜色。
### getPageCount() {#getPageCount--}
```
public int getPageCount()
```


获取由最近的页面布局操作计算的文档中的页数。

**退货:**
int - 由最近的页面布局操作计算的文档中的页数。
### getPageInfo(int pageIndex) {#getPageInfo-int-}
```
public PageInfo getPageInfo(int pageIndex)
```


获取可能对打印或呈现有用的页面的页面大小、方向和其他信息。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| pageIndex | int | 基于 0 的页面索引。 |

**退货:**
[PageInfo](../../com.aspose.words/pageinfo)
### getParentNode() {#getParentNode--}
```
public CompositeNode getParentNode()
```


获取此节点的直接父节点。

如果一个节点刚刚被创建并且还没有被添加到树中，或者如果它已经被从树中移除，则父节点为空。

**退货:**
[CompositeNode](../../com.aspose.words/compositenode) - 此节点的直接父节点。
### getPreviousSibling() {#getPreviousSibling--}
```
public Node getPreviousSibling()
```


获取紧接在该节点之前的节点。如果前面没有节点，则返回 null。

**退货:**
[Node](../../com.aspose.words/node) - 紧接在该节点之前的节点。
### getProtectionType() {#getProtectionType--}
```
public int getProtectionType()
```


获取当前活动的文档保护类型。

此属性允许检索当前设置的文档保护类型。要更改文档保护类型，请使用**M:Aspose.Words.Document.Protect(Aspose.Words.ProtectionType,System.String)**和[unprotect()](../../com.aspose.words/document\#unprotect--)方法。

当文档受到保护时，用户只能进行有限的更改，例如添加注释、进行修订或填写表格。

请注意，文档保护不同于写保护。写保护是使用指定[getWriteProtection()](../../com.aspose.words/document\#getWriteProtection--)

**M:Aspose.Words.Document.Protect(Aspose.Words.ProtectionType,System.String)**

**退货:**
int - 当前活动的文档保护类型。返回值是以下之一[ProtectionType](../../com.aspose.words/protectiontype)常数。
### getRange() {#getRange--}
```
public Range getRange()
```


返回一个**Range**表示包含在此节点中的文档部分的对象。

**退货:**
[Range](../../com.aspose.words/range) - 一个**Range**表示包含在此节点中的文档部分的对象。
### getRemovePersonalInformation() {#getRemovePersonalInformation--}
```
public boolean getRemovePersonalInformation()
```


获取一个标志，表明 Microsoft Word 将在保存文档时从注释、修订和文档属性中删除所有用户信息。

**退货:**
boolean - 一个标志，表明 Microsoft Word 将在保存文档时从注释、修订和文档属性中删除所有用户信息。
### getResourceLoadingCallback() {#getResourceLoadingCallback--}
```
public IResourceLoadingCallback getResourceLoadingCallback()
```


允许控制外部资源的加载方式。

**退货:**
[IResourceLoadingCallback](../../com.aspose.words/iresourceloadingcallback) - 相应的[IResourceLoadingCallback](../../com.aspose.words/iresourceloadingcallback)价值。
### getRevisions() {#getRevisions--}
```
public RevisionCollection getRevisions()
```


获取此文档中存在的修订（跟踪更改）的集合。

返回的集合是一个“实时”集合，这意味着如果您删除包含修订的文档部分，删除的修订将自动从该集合中消失。

**退货:**
[RevisionCollection](../../com.aspose.words/revisioncollection) - 本文档中存在的修订（跟踪更改）的集合。
### getRevisionsView() {#getRevisionsView--}
```
public int getRevisionsView()
```


获取一个值，该值指示是使用文档的原始版本还是修订版本。默认值为**[RevisionsView.ORIGINAL](../../com.aspose.words/revisionsview\#ORIGINAL)** .

**退货:**
int - 一个值，指示是使用文档的原始版本还是修订版本。返回值是以下之一[RevisionsView](../../com.aspose.words/revisionsview)常数。
### getSections() {#getSections--}
```
public SectionCollection getSections()
```


返回代表文档中所有部分的集合。

**退货:**
[SectionCollection](../../com.aspose.words/sectioncollection) 代表文档中所有部分的集合。
### getShadeFormData() {#getShadeFormData--}
```
public boolean getShadeFormData()
```


指定是否打开表单域的灰色底纹。

**退货:**
boolean - 对应的布尔值。
### getShowGrammaticalErrors() {#getShowGrammaticalErrors--}
```
public boolean getShowGrammaticalErrors()
```


指定是否在此文档中显示语法错误。

**退货:**
boolean - 对应的布尔值。
### getShowSpellingErrors() {#getShowSpellingErrors--}
```
public boolean getShowSpellingErrors()
```


指定是否在此文档中显示拼写错误。

**退货:**
boolean - 对应的布尔值。
### getSpellingChecked() {#getSpellingChecked--}
```
public boolean getSpellingChecked()
```


退货**true**如果文档已经过拼写检查。要重新检查文档中的拼写，请将此属性设置为**false**.

**退货:**
布尔值 -**true**如果文档已经过拼写检查。
### getStyles() {#getStyles--}
```
public StyleCollection getStyles()
```


返回文档中定义的样式集合。

有关更多信息，请参阅[StyleCollection](../../com.aspose.words/stylecollection)班级。

**退货:**
[StyleCollection](../../com.aspose.words/stylecollection) 文档中定义的样式集合。
### getText() {#getText--}
```
public String getText()
```


获取此节点及其所有子节点的文本。

返回的字符串包括所有控制和特殊字符，如[ControlChar](../../com.aspose.words/controlchar).

**退货:**
java.lang.String
### getTheme() {#getTheme--}
```
public Theme getTheme()
```


获取[getTheme()](../../com.aspose.words/document\#getTheme--)本文档的对象。

**退货:**
[Theme](../../com.aspose.words/theme) - 这[getTheme()](../../com.aspose.words/document\#getTheme--)本文档的对象。
### getTrackRevisions() {#getTrackRevisions--}
```
public boolean getTrackRevisions()
```


**True**在 Microsoft Word 中编辑此文档时是否跟踪更改。

设置此选项仅指示 Microsoft Word 是否打开或关闭修订。此属性对您通过 Aspose.Words 以编程方式对文档所做的更改没有影响。

如果您想自动跟踪 Aspose.Words 以编程方式对本文档所做的更改，请使用[startTrackRevisions(java.lang.String, java.util.Date)](../../com.aspose.words/document\#startTrackRevisions-java.lang.String--java.util.Date-)方法。

**退货:**
boolean - 对应的布尔值。
### getVariables() {#getVariables--}
```
public VariableCollection getVariables()
```


返回添加到文档或模板的变量集合。

**退货:**
[VariableCollection](../../com.aspose.words/variablecollection) 添加到文档或模板的变量集合。
### getVbaProject() {#getVbaProject--}
```
public VbaProject getVbaProject()
```


得到一个[getVbaProject()](../../com.aspose.words/document\#getVbaProject--) / [setVbaProject(com.aspose.words.VbaProject)](../../com.aspose.words/document\#setVbaProject-com.aspose.words.VbaProject-).

**退货:**
[VbaProject](../../com.aspose.words/vbaproject) - 一个[getVbaProject()](../../com.aspose.words/document\#getVbaProject--) / [setVbaProject(com.aspose.words.VbaProject)](../../com.aspose.words/document\#setVbaProject-com.aspose.words.VbaProject-).
### getVersionsCount() {#getVersionsCount--}
```
public int getVersionsCount()
```


获取存储在 DOC 文档中的文档版本数。

Microsoft Word 中的版本可通过文件/版本菜单访问。 Microsoft Word 仅支持 DOC 文件的版本。

此属性允许检测在 Aspose.Words 中打开此文档之前是否有文档版本存储在此文档中。 Aspose.Words 不为文档版本提供其他支持。如果您使用 Aspose.Words 保存该文档，则该文档将被保存而没有版本。

**退货:**
int - 存储在 DOC 文档中的文档版本数。
### getViewOptions() {#getViewOptions--}
```
public ViewOptions getViewOptions()
```


提供选项以控制文档在 Microsoft Word 中的显示方式。

**退货:**
[ViewOptions](../../com.aspose.words/viewoptions) - 相应的[ViewOptions](../../com.aspose.words/viewoptions)价值。
### getWarningCallback() {#getWarningCallback--}
```
public IWarningCallback getWarningCallback()
```


当检测到可能导致数据或格式保真度丢失的问题时，在各种文档处理过程中调用。文档可能会在其存在的任何阶段产生警告，因此尽早设置警告回调以避免警告丢失非常重要。例如这样的属性[Document.getPageCount()](../../com.aspose.words/document\#getPageCount--)实际构建稍后用于渲染的文档布局，如果为稍后的渲染调用指定警告回调，则布局警告可能会丢失。

**退货:**
[IWarningCallback](../../com.aspose.words/iwarningcallback) - 相应的[IWarningCallback](../../com.aspose.words/iwarningcallback)价值。
### getWatermark() {#getWatermark--}
```
public Watermark getWatermark()
```


提供对文档水印的访问。

**退货:**
[Watermark](../../com.aspose.words/watermark) - 相应的[Watermark](../../com.aspose.words/watermark)价值。
### getWebExtensionTaskPanes() {#getWebExtensionTaskPanes--}
```
public TaskPaneCollection getWebExtensionTaskPanes()
```


返回表示任务窗格加载项列表的集合。

**退货:**
[TaskPaneCollection](../../com.aspose.words/taskpanecollection) 表示任务窗格加载项列表的集合。
### getWriteProtection() {#getWriteProtection--}
```
public WriteProtection getWriteProtection()
```


提供对文档写保护选项的访问。

**退货:**
[WriteProtection](../../com.aspose.words/writeprotection) - 相应的[WriteProtection](../../com.aspose.words/writeprotection)价值。
### hasChildNodes() {#hasChildNodes--}
```
public boolean hasChildNodes()
```


如果此节点有任何子节点，则返回 true。

**退货:**
boolean - 如果此节点有任何子节点，则为真。
### hasMacros() {#hasMacros--}
```
public boolean hasMacros()
```


退货**true**如果文档有 VBA 项目（宏）。

**退货:**
布尔值 -**true**如果文档有 VBA 项目（宏）。
### hasRevisions() {#hasRevisions--}
```
public boolean hasRevisions()
```


退货**true**如果文档有任何跟踪更改。此属性是比较的快捷方式[RevisionCollection.getCount()](../../com.aspose.words/revisioncollection\#getCount--)为零。

**退货:**
布尔值 -**true**如果文档有任何跟踪更改。
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**退货:**
整数
### importNode(Node srcNode, boolean isImportChildren) {#importNode-com.aspose.words.Node-boolean-}
```
public Node importNode(Node srcNode, boolean isImportChildren)
```


将节点从另一个文档导入到当前文档。

将节点从另一个文档导入到当前文档。

该方法使用[ImportFormatMode.USE\_DESTINATION\_STYLES](../../com.aspose.words/importformatmode\#USE-DESTINATION-STYLES)解决格式的选项。

导入节点会创建属于导入文档的源节点的副本。返回的节点没有父节点。源节点不会从原始文档中更改或删除。

在将另一个文档中的节点插入此文档之前，必须先导入它。在导入期间，文档特定的属性（例如对样式和列表的引用）会从原始文档转换为导入文档。导入节点后，可以使用将其插入到文档中的适当位置[CompositeNode.insertBefore(com.aspose.words.Node, com.aspose.words.Node)](../../com.aspose.words/compositenode\#insertBefore-com.aspose.words.Node--com.aspose.words.Node-)或者[CompositeNode.insertAfter(com.aspose.words.Node, com.aspose.words.Node)](../../com.aspose.words/compositenode\#insertAfter-com.aspose.words.Node--com.aspose.words.Node-).

如果源节点已经属于目标文档，则只需创建源节点的深层克隆。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| srcNode | [Node](../../com.aspose.words/node) | 正在导入的节点。 |
| isImportChildren | boolean | True 递归导入所有子节点；否则为假。 |

**退货:**
[Node](../../com.aspose.words/node) 属于当前文档的克隆节点。
### importNode(Node srcNode, boolean isImportChildren, int importFormatMode) {#importNode-com.aspose.words.Node-boolean-int-}
```
public Node importNode(Node srcNode, boolean isImportChildren, int importFormatMode)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| srcNode | [Node](../../com.aspose.words/node) |  |
| isImportChildren | boolean |  |
| importFormatMode | int |  |

**退货:**
[Node](../../com.aspose.words/node)
### indexOf(Node child) {#indexOf-com.aspose.words.Node-}
```
public int indexOf(Node child)
```


返回子节点数组中指定子节点的索引。如果在子节点中未找到该节点，则返回 -1。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| child | [Node](../../com.aspose.words/node) |  |

**退货:**
整数
### insertAfter(Node newChild, Node refChild) {#insertAfter-com.aspose.words.Node-com.aspose.words.Node-}
```
public Node insertAfter(Node newChild, Node refChild)
```


在指定的引用节点之后立即插入指定的节点。

如果 refChild 为 null，则在子节点列表的开头插入 newChild。

如果 newChild 已经在树中，则首先将其移除。

如果要插入的节点是从另一个文档创建的，您应该使用**M:Aspose.Words.DocumentBase.ImportNode(Aspose.Words.Node,System.Boolean,Aspose.Words.ImportFormatMode)**将节点导入当前文档。然后可以将导入的节点插入到当前文档中。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| newChild | [Node](../../com.aspose.words/node) | 要插入的节点。 |
| refChild | [Node](../../com.aspose.words/node) | 作为参考节点的节点。 newNode 放在 refNode 之后。 |

**退货:**
[Node](../../com.aspose.words/node) - 插入的节点。
### insertBefore(Node newChild, Node refChild) {#insertBefore-com.aspose.words.Node-com.aspose.words.Node-}
```
public Node insertBefore(Node newChild, Node refChild)
```


将指定节点插入到紧靠指定引用节点之前。

如果 refChild 为 null，则在子节点列表的末尾插入 newChild。

如果 newChild 已经在树中，则首先将其移除。

如果要插入的节点是从另一个文档创建的，您应该使用**M:Aspose.Words.DocumentBase.ImportNode(Aspose.Words.Node,System.Boolean,Aspose.Words.ImportFormatMode)**将节点导入当前文档。然后可以将导入的节点插入到当前文档中。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| newChild | [Node](../../com.aspose.words/node) | 要插入的节点。 |
| refChild | [Node](../../com.aspose.words/node) | 作为参考节点的节点。 newChild 放置在此节点之前。 |

**退货:**
[Node](../../com.aspose.words/node) - 插入的节点。
### isComposite() {#isComposite--}
```
public boolean isComposite()
```


返回 true，因为此节点可以有子节点。

**退货:**
boolean - True 因为这个节点可以有子节点。
### iterator() {#iterator--}
```
public Iterator iterator()
```


为该节点的子节点上的每个样式迭代提供支持。

**退货:**
java.util.Iterator
### joinRunsWithSameFormatting() {#joinRunsWithSameFormatting--}
```
public int joinRunsWithSameFormatting()
```


连接在文档的所有段落中以相同的格式运行。

这是一种优化方法。一些文档包含具有相同格式的相邻运行。如果手动对文档进行大量编辑，通常会发生这种情况。您可以通过加入这些运行来减小文档大小并加快进一步处理。

该操作检查每个[Paragraph](../../com.aspose.words/paragraph)相邻文档中的节点[Run](../../com.aspose.words/run)具有相同属性的节点。它忽略了用于跟踪运行创建和修改的编辑会话的唯一标识符。在每个连接序列中首次运行会累积所有文本。剩余的运行将从文档中删除。

**退货:**
 int - 执行的连接数。什么时候**N**相邻的跑步被加入他们算作**N - 1**加入。
### nextPreOrder(Node rootNode) {#nextPreOrder-com.aspose.words.Node-}
```
public Node nextPreOrder(Node rootNode)
```


根据前序树遍历算法获取下一个节点。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| rootNode | [Node](../../com.aspose.words/node) | 遍历的顶部节点（极限）。 |

**退货:**
[Node](../../com.aspose.words/node) - 预购订单中的下一个节点。如果到达 rootNode，则为 Null。
### nodeTypeToString(int nodeType) {#nodeTypeToString-int-}
```
public static String nodeTypeToString(int nodeType)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| nodeType | int |  |

**退货:**
java.lang.String
### normalizeFieldTypes() {#normalizeFieldTypes--}
```
public void normalizeFieldTypes()
```


更改字段类型值[FieldChar.getFieldType()](../../com.aspose.words/fieldchar\#getFieldType--)的[FieldStart](../../com.aspose.words/fieldstart), [FieldSeparator](../../com.aspose.words/fieldseparator), [FieldEnd](../../com.aspose.words/fieldend)在整个文档中，以便它们对应于域代码中包含的域类型。

在影响字段类型的文档更改后使用此方法。

要更改文档特定部分中的字段类型值，请使用[Range.normalizeFieldTypes()](../../com.aspose.words/range\#normalizeFieldTypes--).

### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### prependChild(Node newChild) {#prependChild-com.aspose.words.Node-}
```
public Node prependChild(Node newChild)
```


将指定节点添加到此节点的子节点列表的开头。

如果 newChild 已经在树中，则首先将其移除。

如果要插入的节点是从另一个文档创建的，您应该使用**M:Aspose.Words.DocumentBase.ImportNode(Aspose.Words.Node,System.Boolean,Aspose.Words.ImportFormatMode)**将节点导入当前文档。然后可以将导入的节点插入到当前文档中。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| newChild | [Node](../../com.aspose.words/node) | 要添加的节点。 |

**退货:**
[Node](../../com.aspose.words/node) - 添加的节点。
### previousPreOrder(Node rootNode) {#previousPreOrder-com.aspose.words.Node-}
```
public Node previousPreOrder(Node rootNode)
```


根据前序树遍历算法获取上一个节点。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| rootNode | [Node](../../com.aspose.words/node) | 遍历的顶部节点（极限）。 |

**退货:**
[Node](../../com.aspose.words/node) - 预购订单中的上一个节点。如果到达 rootNode，则为 Null。
### print() {#print--}
```
public void print()
```


打印文档而不显示任何用户界面表单。将整个文档打印到默认打印机。

### print(String printerName) {#print-java.lang.String-}
```
public void print(String printerName)
```


使用标准（无用户界面）打印控制器将整个文档打印到指定的打印机。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| printerName | java.lang.String | 打印机的名称。 |

### print(AttributeSet printerSettings) {#print-javax.print.attribute.AttributeSet-}
```
public void print(AttributeSet printerSettings)
```


根据指定的打印机设置，使用标准（无用户界面）打印控制器打印文档。

该对象允许您指定要打印的打印机、要打印的页面范围和其他选项。

可以同时包含配置 PrintJob 请求和配置 PrintService 查找。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| printerSettings | javax.print.attribute.AttributeSet | 要使用的打印机设置。 |

### print(AttributeSet printerSettings, String documentName) {#print-javax.print.attribute.AttributeSet-java.lang.String-}
```
public void print(AttributeSet printerSettings, String documentName)
```


根据指定的打印机设置打印文档，使用标准（无用户界面）打印控制器和文档名称。

该对象允许您指定要打印的打印机、要打印的页面范围和其他选项。

可以同时包含配置 PrintJob 请求和配置 PrintService 查找。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| printerSettings | javax.print.attribute.AttributeSet | 要使用的打印机设置。 |
| documentName | java.lang.String | 打印文档时要显示的文档名称（例如，在打印状态对话框或打印机队列中）。 |

### protect(int type) {#protect-int-}
```
public void protect(int type)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| type | int |  |

### protect(int type, String password) {#protect-int-java.lang.String-}
```
public void protect(int type, String password)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| type | int |  |
| password | java.lang.String |  |

### remove() {#remove--}
```
public void remove()
```


从父级中移除自身。

### removeAllChildren() {#removeAllChildren--}
```
public void removeAllChildren()
```


移除当前节点的所有子节点。

### removeChild(Node oldChild) {#removeChild-com.aspose.words.Node-}
```
public Node removeChild(Node oldChild)
```


删除指定的子节点。

删除节点后，oldChild 的父级设置为 null。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| oldChild | [Node](../../com.aspose.words/node) | 要移除的节点。 |

**退货:**
[Node](../../com.aspose.words/node) - 删除的节点。
### removeExternalSchemaReferences() {#removeExternalSchemaReferences--}
```
public void removeExternalSchemaReferences()
```


从此文档中删除外部 XML 架构引用。

### removeMacros() {#removeMacros--}
```
public void removeMacros()
```


从文档中删除所有宏（VBA 项目）以及工具栏和命令自定义项。

通过从文档中删除所有宏，您可以确保文档不包含宏病毒。

### removeSmartTags() {#removeSmartTags--}
```
public void removeSmartTags()
```


删除所有[SmartTag](../../com.aspose.words/smarttag)当前节点的后代节点。此方法不会删除智能标记的内容。

### renderToScale(int pageIndex, Graphics2D graphics, float x, float y, float scale) {#renderToScale-int-java.awt.Graphics2D-float-float-float-}
```
public Point2D.Float renderToScale(int pageIndex, Graphics2D graphics, float x, float y, float scale)
```


将文档页面呈现为指定比例的对象。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| pageIndex | int | 基于 0 的页面索引。 |
| graphics | java.awt.Graphics2D | 渲染到的对象。 |
| x | float | 渲染页面左上角的 X 坐标（以世界单位为单位）。 |
| y | float | 渲染页面左上角的 Y 坐标（以世界单位为单位）。 |
| scale | float | 渲染页面的比例（1.0 为 100%）。 |

**退货:**
java.awt.geom.Point2D.Float - 渲染页面的宽度和高度（以世界单位为单位）。
### renderToSize(int pageIndex, Graphics2D graphics, float x, float y, float width, float height) {#renderToSize-int-java.awt.Graphics2D-float-float-float-float-}
```
public float renderToSize(int pageIndex, Graphics2D graphics, float x, float y, float width, float height)
```


将文档页面呈现为指定大小的对象。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| pageIndex | int | 基于 0 的页面索引。 |
| graphics | java.awt.Graphics2D | 渲染到的对象。 |
| x | float | 渲染页面左上角的 X 坐标（以世界单位为单位）。 |
| y | float | 渲染页面左上角的 Y 坐标（以世界单位为单位）。 |
| width | float | 渲染页面可以占据的最大宽度（以世界单位为单位）。 |
| height | float | 渲染页面可以占据的最大高度（以世界单位为单位）。 |

**退货:**
float - 为呈现的页面自动计算以适合指定大小的比例。
### save(OutputStream stream, SaveOptions saveOptions) {#save-java.io.OutputStream-com.aspose.words.SaveOptions-}
```
public SaveOutput参数 save(OutputStream stream, SaveOptions saveOptions)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| stream | java.io.OutputStream |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions) |  |

**退货:**
[SaveOutput参数](../../com.aspose.words/saveoutputparameters)
### save(OutputStream stream, int saveFormat) {#save-java.io.OutputStream-int-}
```
public SaveOutput参数 save(OutputStream stream, int saveFormat)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| stream | java.io.OutputStream |  |
| saveFormat | int |  |

**退货:**
[SaveOutput参数](../../com.aspose.words/saveoutputparameters)
### save(String fileName) {#save-java.lang.String-}
```
public SaveOutput参数 save(String fileName)
```


保存文档。将文档保存到文件中。自动确定扩展的保存格式。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| fileName | java.lang.String | 文档的名称。如果具有指定文件名的文档已存在，则覆盖现有文档。 |

**退货:**
[SaveOutput参数](../../com.aspose.words/saveoutputparameters) - 您可以选择使用的附加信息。
### save(String fileName, SaveOptions saveOptions) {#save-java.lang.String-com.aspose.words.SaveOptions-}
```
public SaveOutput参数 save(String fileName, SaveOptions saveOptions)
```


使用指定的保存选项将文档保存到文件。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| fileName | java.lang.String | 文档的名称。如果具有指定文件名的文档已存在，则覆盖现有文档。 |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions) | 指定控制文档保存方式的选项。可以为空。 |

**退货:**
[SaveOutput参数](../../com.aspose.words/saveoutputparameters) - 您可以选择使用的附加信息。
### save(String fileName, int saveFormat) {#save-java.lang.String-int-}
```
public SaveOutput参数 save(String fileName, int saveFormat)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| fileName | java.lang.String |  |
| saveFormat | int |  |

**退货:**
[SaveOutput参数](../../com.aspose.words/saveoutputparameters)
### selectNodes(String xpath) {#selectNodes-java.lang.String-}
```
public NodeList selectNodes(String xpath)
```


选择与 XPath 表达式匹配的节点列表。

目前仅支持带有元素名称的表达式。不支持使用属性名称的表达式。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| xpath | java.lang.String | XPath 表达式。 |

**退货:**
[NodeList](../../com.aspose.words/nodelist) - 与 XPath 查询匹配的节点列表。
### selectSingleNode(String xpath) {#selectSingleNode-java.lang.String-}
```
public Node selectSingleNode(String xpath)
```


选择与 XPath 表达式匹配的第一个节点。

目前仅支持带有元素名称的表达式。不支持使用属性名称的表达式。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| xpath | java.lang.String | XPath 表达式。 |

**退货:**
[Node](../../com.aspose.words/node) - 与 XPath 查询匹配的第一个节点，如果未找到匹配节点，则为 null。
### setAttachedTemplate(String value) {#setAttachedTemplate-java.lang.String-}
```
public void setAttachedTemplate(String value)
```


设置附加到文档的模板的完整路径。

空字符串表示文档附加到 Normal 模板。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 附加到文档的模板的完整路径。 |

### setAutomaticallyUpdateStyles(boolean value) {#setAutomaticallyUpdateStyles-boolean-}
```
public void setAutomaticallyUpdateStyles(boolean value)
```


设置一个标志，指示每次在 MS Word 中打开文档时，文档中的样式是否更新以匹配附加模板中的样式。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 指示每次在 MS Word 中打开文档时是否更新文档中的样式以匹配附加模板中的样式的标志。 |

### setBackgroundShape(Shape value) {#setBackgroundShape-com.aspose.words.Shape-}
```
public void setBackgroundShape(Shape value)
```


设置文档的背景形状。可以为空。

Microsoft Word 只允许具有其[ShapeBase.getShapeType()](../../com.aspose.words/shapebase\#getShapeType--)属性等于[ShapeType.RECTANGLE](../../com.aspose.words/shapetype\#RECTANGLE)用作文档的背景形状。

Microsoft Word 仅支持背景形状的填充属性。所有其他属性都被忽略。

将此属性设置为非空值也将设置[ViewOptions.getDisplayBackgroundShape()](../../com.aspose.words/viewoptions\#getDisplayBackgroundShape--) / [ViewOptions.setDisplayBackgroundShape(boolean)](../../com.aspose.words/viewoptions\#setDisplayBackgroundShape-boolean-)为真。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | [Shape](../../com.aspose.words/shape) | 文档的背景形状。 |

### setCustomNodeId(int value) {#setCustomNodeId-int-}
```
public void setCustomNodeId(int value)
```


指定自定义节点标识符。

默认为零。

这个标识符可以任意设置和使用。例如，作为获取外部数据的键。

重要说明，指定的值不会保存到输出文件中，并且仅在节点生命周期内存在。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 对应的 int 值。 |

### setCustomXmlParts(CustomXmlPartCollection value) {#setCustomXmlParts-com.aspose.words.CustomXmlPartCollection-}
```
public void setCustomXmlParts(CustomXmlPartCollection value)
```


设置自定义 XML 数据存储部件的集合。

Aspose.Words 仅将自定义 XML 部件加载和保存到 OOXML 和 DOC 文档中。

此属性不能为 null 。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | [CustomXmlPartCollection](../../com.aspose.words/customxmlpartcollection) | 自定义 XML 数据存储部件的集合。 |

### setDefaultTabStop(double value) {#setDefaultTabStop-double-}
```
public void setDefaultTabStop(double value)
```


设置默认制表位之间的间隔（以磅为单位）。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | double | 默认制表位之间的间隔（以磅为单位）。 |

### setFontSettings(FontSettings value) {#setFontSettings-com.aspose.words.FontSettings-}
```
public void setFontSettings(FontSettings value)
```


设置文档字体设置。

此属性允许为每个文档指定字体设置。如果设置为空，默认静态字体设置[FontSettings.getDefaultInstance()](../../com.aspose.words/fontsettings\#getDefaultInstance--)将会被使用。

默认值为空。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | [FontSettings](../../com.aspose.words/fontsettings) | 文档字体设置。 |

### setGlossaryDocument(GlossaryDocument value) {#setGlossaryDocument-com.aspose.words.GlossaryDocument-}
```
public void setGlossaryDocument(GlossaryDocument value)
```


在此文档或模板中设置词汇表文档。词汇表文档是文档中定义的自动图文集、自动更正和构建块条目的存储。

如果文档没有词汇表文档，则此属性返回 null。

您可以通过创建[GlossaryDocument](../../com.aspose.words/glossarydocument)对象并分配给该属性。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | [GlossaryDocument](../../com.aspose.words/glossarydocument) | 此文档或模板中的词汇表文档。 |

### setGrammarChecked(boolean value) {#setGrammarChecked-boolean-}
```
public void setGrammarChecked(boolean value)
```


退货**true**如果文档已经过语法检查。要重新检查文档中的语法，请将此属性设置为**false**.

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | **true**如果文档已经过语法检查。 |

### setMailMergeSettings(MailMergeSettings value) {#setMailMergeSettings-com.aspose.words.MailMergeSettings-}
```
public void setMailMergeSettings(MailMergeSettings value)
```


设置包含文档的所有邮件合并信息的对象。

您可以使用此对象为文档指定邮件合并数据源，当用户打开此文档时，此信息（连同可用的数据字段）将出现在 Microsoft Word 中。或者，您可以使用此对象查询用户在 Microsoft Word 中为此文档指定的邮件合并设置。

该对象永远不会为空。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | [MailMergeSettings](../../com.aspose.words/mailmergesettings) | 包含文档的所有邮件合并信息的对象。 |

### setNodeChangingCallback(INodeChangingCallback value) {#setNodeChangingCallback-com.aspose.words.INodeChangingCallback-}
```
public void setNodeChangingCallback(INodeChangingCallback value)
```


在文档中插入或删除节点时调用。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | [INodeChangingCallback](../../com.aspose.words/inodechangingcallback) | 相应的[INodeChangingCallback](../../com.aspose.words/inodechangingcallback)价值。 |

### setPackageCustomParts(CustomPartCollection value) {#setPackageCustomParts-com.aspose.words.CustomPartCollection-}
```
public void setPackageCustomParts(CustomPartCollection value)
```


设置使用“未知关系”链接到 OOXML 包的自定义部分（任意内容）的集合。

不要将这些自定义部分与自定义 XML 数据混淆。如果您需要访问自定义 XML 部件，请使用[getCustomXmlParts()](../../com.aspose.words/document\#getCustomXmlParts--) / [setCustomXmlParts(com.aspose.words.CustomXmlPartCollection)](../../com.aspose.words/document\#setCustomXmlParts-com.aspose.words.CustomXmlPartCollection-)财产。

此集合包含 OOXML 部分，其父项是 OOXML 包，并且它们的目标是“未知关系”。有关更多信息，请参阅[CustomPart](../../com.aspose.words/custompart).

Aspose.Words 仅将自定义部件加载和保存到 OOXML 文档中。

此属性不能为 null 。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | [CustomPartCollection](../../com.aspose.words/custompartcollection) | 使用“未知关系”链接到 OOXML 包的自定义部分（任意内容）的集合。 |

### setPageColor(Color value) {#setPageColor-java.awt.Color-}
```
public void setPageColor(Color value)
```


设置文档的页面颜色。这个属性是一个更简单的版本[getBackgroundShape()](../../com.aspose.words/documentbase\#getBackgroundShape--) / [setBackgroundShape(com.aspose.words.Shape)](../../com.aspose.words/documentbase\#setBackgroundShape-com.aspose.words.Shape-).

此属性提供了一种为文档指定纯色页面颜色的简单方法。设置此属性会创建并设置一个适当的[getBackgroundShape()](../../com.aspose.words/documentbase\#getBackgroundShape--) / [setBackgroundShape(com.aspose.words.Shape)](../../com.aspose.words/documentbase\#setBackgroundShape-com.aspose.words.Shape-).

如果未设置页面颜色（例如文档中没有背景形状），则返回零颜色。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.awt.Color | 文档的页面颜色。 |

### setRemovePersonalInformation(boolean value) {#setRemovePersonalInformation-boolean-}
```
public void setRemovePersonalInformation(boolean value)
```


设置一个标志，表明 Microsoft Word 将在保存文档时从注释、修订和文档属性中删除所有用户信息。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 一个标志，表明 Microsoft Word 将在保存文档时从注释、修订和文档属性中删除所有用户信息。 |

### setResourceLoadingCallback(IResourceLoadingCallback value) {#setResourceLoadingCallback-com.aspose.words.IResourceLoadingCallback-}
```
public void setResourceLoadingCallback(IResourceLoadingCallback value)
```


允许控制外部资源的加载方式。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | [IResourceLoadingCallback](../../com.aspose.words/iresourceloadingcallback) | 相应的[IResourceLoadingCallback](../../com.aspose.words/iresourceloadingcallback)价值。 |

### setRevisionsView(int value) {#setRevisionsView-int-}
```
public void setRevisionsView(int value)
```


设置一个值，该值指示是使用文档的原始版本还是修订版本。默认值为**[RevisionsView.ORIGINAL](../../com.aspose.words/revisionsview\#ORIGINAL)** .

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 一个值，指示是使用文档的原始版本还是修订版本。该值必须是以下之一[RevisionsView](../../com.aspose.words/revisionsview)常数。 |

### setSectionAttr(int key, Object value) {#setSectionAttr-int-java.lang.Object-}
```
public void setSectionAttr(int key, Object value)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| key | int |  |
| value | java.lang.Object |  |

### setShadeFormData(boolean value) {#setShadeFormData-boolean-}
```
public void setShadeFormData(boolean value)
```


指定是否打开表单域的灰色底纹。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setShowGrammaticalErrors(boolean value) {#setShowGrammaticalErrors-boolean-}
```
public void setShowGrammaticalErrors(boolean value)
```


指定是否在此文档中显示语法错误。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setShowSpellingErrors(boolean value) {#setShowSpellingErrors-boolean-}
```
public void setShowSpellingErrors(boolean value)
```


指定是否在此文档中显示拼写错误。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setSpellingChecked(boolean value) {#setSpellingChecked-boolean-}
```
public void setSpellingChecked(boolean value)
```


退货**true**如果文档已经过拼写检查。要重新检查文档中的拼写，请将此属性设置为**false**.

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | **true**如果文档已经过拼写检查。 |

### setTrackRevisions(boolean value) {#setTrackRevisions-boolean-}
```
public void setTrackRevisions(boolean value)
```


**True**在 Microsoft Word 中编辑此文档时是否跟踪更改。

设置此选项仅指示 Microsoft Word 是否打开或关闭修订。此属性对您通过 Aspose.Words 以编程方式对文档所做的更改没有影响。

如果您想自动跟踪 Aspose.Words 以编程方式对本文档所做的更改，请使用[startTrackRevisions(java.lang.String, java.util.Date)](../../com.aspose.words/document\#startTrackRevisions-java.lang.String--java.util.Date-)方法。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setVbaProject(VbaProject value) {#setVbaProject-com.aspose.words.VbaProject-}
```
public void setVbaProject(VbaProject value)
```


设置一个[getVbaProject()](../../com.aspose.words/document\#getVbaProject--) / [setVbaProject(com.aspose.words.VbaProject)](../../com.aspose.words/document\#setVbaProject-com.aspose.words.VbaProject-).

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | [VbaProject](../../com.aspose.words/vbaproject) | 一个[getVbaProject()](../../com.aspose.words/document\#getVbaProject--) / [setVbaProject(com.aspose.words.VbaProject)](../../com.aspose.words/document\#setVbaProject-com.aspose.words.VbaProject-). |

### setWarningCallback(IWarningCallback value) {#setWarningCallback-com.aspose.words.IWarningCallback-}
```
public void setWarningCallback(IWarningCallback value)
```


当检测到可能导致数据或格式保真度丢失的问题时，在各种文档处理过程中调用。文档可能会在其存在的任何阶段产生警告，因此尽早设置警告回调以避免警告丢失非常重要。例如这样的属性[Document.getPageCount()](../../com.aspose.words/document\#getPageCount--)实际构建稍后用于渲染的文档布局，如果为稍后的渲染调用指定警告回调，则布局警告可能会丢失。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | [IWarningCallback](../../com.aspose.words/iwarningcallback) | 相应的[IWarningCallback](../../com.aspose.words/iwarningcallback)价值。 |

### startTrackRevisions(String author) {#startTrackRevisions-java.lang.String-}
```
public void startTrackRevisions(String author)
```


开始自动将您以编程方式对文档所做的所有进一步更改标记为修订更改。

如果您调用此方法，然后以编程方式对文档进行一些更改，保存文档并稍后在 MS Word 中打开文档，您将看到这些更改作为修订。

目前 Aspose.Words 仅支持跟踪节点插入和删除。格式更改不会记录为修订。

通过节点操作修改此文档以及使用[DocumentBuilder](../../com.aspose.words/documentbuilder)

这种方法不会改变[getTrackRevisions()](../../com.aspose.words/document\#getTrackRevisions--) / [setTrackRevisions(boolean)](../../com.aspose.words/document\#setTrackRevisions-boolean-)选项并且不将其值用于修订跟踪的目的。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| author | java.lang.String | 用于修订的作者姓名缩写。 |

### startTrackRevisions(String author, Date dateTime) {#startTrackRevisions-java.lang.String-java.util.Date-}
```
public void startTrackRevisions(String author, Date dateTime)
```


开始自动将您以编程方式对文档所做的所有进一步更改标记为修订更改。

如果您调用此方法，然后以编程方式对文档进行一些更改，保存文档并稍后在 MS Word 中打开文档，您将看到这些更改作为修订。

目前 Aspose.Words 仅支持跟踪节点插入和删除。格式更改不会记录为修订。

通过节点操作修改此文档以及使用[DocumentBuilder](../../com.aspose.words/documentbuilder)

这种方法不会改变[getTrackRevisions()](../../com.aspose.words/document\#getTrackRevisions--) / [setTrackRevisions(boolean)](../../com.aspose.words/document\#setTrackRevisions-boolean-)选项并且不将其值用于修订跟踪的目的。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| author | java.lang.String | 用于修订的作者姓名缩写。 |
| dateTime | java.util.Date | 用于修订的日期和时间。 |

### stopTrackRevisions() {#stopTrackRevisions--}
```
public void stopTrackRevisions()
```


停止将文档更改自动标记为修订。

### toString() {#toString--}
```
public String toString()
```




**退货:**
java.lang.String
### toString(SaveOptions saveOptions) {#toString-com.aspose.words.SaveOptions-}
```
public String toString(SaveOptions saveOptions)
```


使用指定的保存选项将节点的内容导出为字符串。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions) | 指定控制节点保存方式的选项。 |

**退货:**
java.lang.String - 指定格式的节点内容。
### toString(int saveFormat) {#toString-int-}
```
public String toString(int saveFormat)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| saveFormat | int |  |

**退货:**
java.lang.String
### unlink字段() {#unlink字段--}
```
public void unlink字段()
```


取消链接整个文档中的字段。

将整个文档中的所有字段替换为其最新结果。

要取消链接文档特定部分中的字段，请使用[Range.unlink字段()](../../com.aspose.words/range\#unlink字段--).

### unprotect() {#unprotect--}
```
public void unprotect()
```


取消对文档的保护。无论密码如何，都会从文档中删除保护。

即使文档有保护密码，此方法也会取消对文档的保护。

请注意，文档保护不同于写保护。写保护是使用指定[getWriteProtection()](../../com.aspose.words/document\#getWriteProtection--).

### unprotect(String password) {#unprotect-java.lang.String-}
```
public boolean unprotect(String password)
```


如果指定了正确的密码，则从文档中删除保护。

仅当指定了正确的密码时，此方法才会取消对文档的保护。

请注意，文档保护不同于写保护。写保护是使用指定[getWriteProtection()](../../com.aspose.words/document\#getWriteProtection--).

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| password | java.lang.String | 用于取消保护文档的密码。 |

**退货:**
boolean - 如果指定了正确的密码并且文档未受保护，则为真。
### update字段() {#update字段--}
```
public void update字段()
```


更新整个文档中的字段值。

当您打开、修改并保存文档时，Aspose.Words 不会自动更新字段，它会保持它们完好无损。因此，如果您以编程方式修改了文档并希望确保正确的（计算的）字段值出现在保存的文档中，则通常需要在保存之前调用此方法。

执行邮件合并后不需要更新字段，因为邮件合并是一种字段更新，会自动更新文档中的所有字段。

此方法不会更新所有字段类型。有关支持的字段类型的详细列表，请参阅程序员指南。

此方法不会更新与页面布局算法相关的字段（例如 PAGE、PAGES、PAGEREF）。渲染文档或调用时更新页面布局相关字段[updatePageLayout()](../../com.aspose.words/document\#updatePageLayout--).

使用[normalizeFieldTypes()](../../com.aspose.words/document\#normalizeFieldTypes--)如果存在影响字段类型的文档更改，则字段更新之前的方法。

要更新文档特定部分中的字段，请使用[Range.update字段()](../../com.aspose.words/range\#update字段--).

### updateListLabels() {#updateListLabels--}
```
public void updateListLabels()
```


更新文档中所有列表项的列表标签。

此方法更新列表标签属性，例如[ListLabel.getLabelValue()](../../com.aspose.words/listlabel\#getLabelValue--)和[ListLabel.getLabelString()](../../com.aspose.words/listlabel\#getLabelString--)对于每个[Paragraph.getListLabel()](../../com.aspose.words/paragraph\#getListLabel--)文档中的对象。

此外，在更新文档中的字段时，有时会隐式调用此方法。这是必需的，因为某些可能引用列表编号的字段（例如 TOC 或 REF）需要它们是最新的。

### updatePageLayout() {#updatePageLayout--}
```
public void updatePageLayout()
```


重建文档的页面布局。

此方法将文档格式化为页面，并更新文档中的页码相关字段，例如 PAGE、PAGES、PAGEREF 和 REF。将文档正确呈现为固定页面格式需要最新的页面布局信息。

当您第一次将文档转换为 PDF、XPS、图像或打印时，会自动调用此方法。但是，如果您在渲染后修改文档然后尝试再次渲染它 - Aspose.Words 不会自动更新页面布局。在这种情况下，您应该致电[updatePageLayout()](../../com.aspose.words/document\#updatePageLayout--)在再次渲染之前。

### updateTableLayout() {#updateTableLayout--}
```
public void updateTableLayout()
```


实施一种较早的方法来重新计算具有已知问题的表列宽度。该方法已弃用，将在几个版本中删除。

### updateThumbnail() {#updateThumbnail--}
```
public void updateThumbnail()
```


更新[BuiltInDocumentProperties.getThumbnail()](../../com.aspose.words/builtindocumentproperties\#getThumbnail--) / [BuiltInDocumentProperties.setThumbnail(byte[])](../../com.aspose.words/builtindocumentproperties\#setThumbnail-byte---)使用默认选项的文档。

### updateThumbnail(ThumbnailGeneratingOptions options) {#updateThumbnail-com.aspose.words.ThumbnailGeneratingOptions-}
```
public void updateThumbnail(ThumbnailGeneratingOptions options)
```


更新[BuiltInDocumentProperties.getThumbnail()](../../com.aspose.words/builtindocumentproperties\#getThumbnail--) / [BuiltInDocumentProperties.setThumbnail(byte[])](../../com.aspose.words/builtindocumentproperties\#setThumbnail-byte---)根据指定的选项的文档。这[ThumbnailGeneratingOptions](../../com.aspose.words/thumbnailgeneratingoptions)允许您指定缩略图的来源、大小和其他选项。如果尝试生成缩略图失败，则不更改。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| options | [ThumbnailGeneratingOptions](../../com.aspose.words/thumbnailgeneratingoptions) | 要使用的生成选项。 |

### updateWordCount() {#updateWordCount--}
```
public void updateWordCount()
```


更新文档的字数统计属性。

**UpdateWordCount**重新计算和更新字符、单词和段落属性[getBuiltInDocumentProperties()](../../com.aspose.words/document\#getBuiltInDocumentProperties--)的集合**Document**.

注意**UpdateWordCount**不更新行数和页数属性。使用[updateWordCount()](../../com.aspose.words/document\#updateWordCount--)重载并将 True 值作为参数传递来执行此操作。

当您使用评估版时，评估水印也将包含在字数中。

### updateWordCount(boolean updateLinesCount) {#updateWordCount-boolean-}
```
public void updateWordCount(boolean updateLinesCount)
```


更新文档的字数统计属性，可选择更新[BuiltInDocumentProperties.getLines()](../../com.aspose.words/builtindocumentproperties\#getLines--) / [BuiltInDocumentProperties.setLines(int)](../../com.aspose.words/builtindocumentproperties\#setLines-int-)财产。此方法将重建文档的页面布局。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| updateLinesCount | boolean | 如果应计算文档中的行数，则为真。 |

### wait() {#wait--}
```
public final void wait()
```




### wait(long arg0) {#wait-long-}
```
public final native void wait(long arg0)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int-}
```
public final void wait(long arg0, int arg1)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |
