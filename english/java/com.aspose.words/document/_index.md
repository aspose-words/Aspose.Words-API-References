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

这**Document**是 Aspose.Words 库中的中心对象。

将现有文档加载到任何[LoadFormat](../../com.aspose.words/loadformat)格式，将文件名或流传递到其中一个**Document**构造函数。要创建空白文档，请调用不带参数的构造函数。

使用 Save 方法重载之一将文档保存在任何[SaveFormat](../../com.aspose.words/saveformat)格式。

将文档页面直接绘制到**Graphics**对象使用[renderToScale(int, java.awt.Graphics2D, float, float, float)](../../com.aspose.words/document\#renderToScale-int--java.awt.Graphics2D--float--float--float-)或者[renderToSize(int, java.awt.Graphics2D, float, float, float, float)](../../com.aspose.words/document\#renderToSize-int--java.awt.Graphics2D--float--float--float--float-)方法。

要打印文档，请使用其中一种[print(java.lang.String)](../../com.aspose.words/document\#print-java.lang.String-)方法。

[getMailMerge()](../../com.aspose.words/document\#getMailMerge--)是 Aspose.Words 的报告引擎，允许使用来自各种数据源的数据快速轻松地填充在 Microsoft Word 中设计的报告。数据可以来自 java.sql.ResultSet 或值数组。**MailMerge**将检查在数据源中找到的记录，并根据需要将它们插入到文档中的邮件合并字段中。

**Document**存储文档范围的信息，例如[DocumentBase.getStyles()](../../com.aspose.words/documentbase\#getStyles--), [getBuiltInDocumentProperties()](../../com.aspose.words/document\#getBuiltInDocumentProperties--), [getCustomDocumentProperties()](../../com.aspose.words/document\#getCustomDocumentProperties--)、列表和宏。这些对象中的大多数都可以通过相应的属性访问**Document**.

这**Document**是包含文档所有其他节点的树的根节点。树是一种复合设计模式，在许多方面类似于 XmlDocument。可以通过编程方式自由操作文档的内容：

 *  可以通过类型化集合访问文档的节点，例如[getSections()](../../com.aspose.words/document\#getSections--), [ParagraphCollection](../../com.aspose.words/paragraphcollection)等等
 *  文档的节点可以使用它们的节点类型来选择**M:Aspose.Words.CompositeNode.GetChildNodes(Aspose.Words.Node类型,System.Boolean)**或使用 XPath 查询[CompositeNode.selectNodes(java.lang.String)](../../com.aspose.words/compositenode\#selectNodes-java.lang.String-)或者[CompositeNode.selectSingleNode(java.lang.String)](../../com.aspose.words/compositenode\#selectSingleNode-java.lang.String-).
 *  可以使用在文档中的任何位置添加或删除内容节点[CompositeNode.insertBefore(com.aspose.words.Node, com.aspose.words.Node)](../../com.aspose.words/compositenode\#insertBefore-com.aspose.words.Node--com.aspose.words.Node-), [CompositeNode.insertAfter(com.aspose.words.Node, com.aspose.words.Node)](../../com.aspose.words/compositenode\#insertAfter-com.aspose.words.Node--com.aspose.words.Node-), [CompositeNode.removeChild(com.aspose.words.Node)](../../com.aspose.words/compositenode\#removeChild-com.aspose.words.Node-)以及基类提供的其他方法[CompositeNode](../../com.aspose.words/compositenode).
 *  每个节点的格式属性可以通过该节点的属性进行更改。

考虑使用[DocumentBuilder](../../com.aspose.words/documentbuilder)这简化了以编程方式创建或填充文档树的任务。

这**Document**只能包含[Section](../../com.aspose.words/section)对象。

在 Microsoft Word 中，一个有效的文档至少需要有一个部分。
## 构造函数s

| 构造函数 | 描述 |
| --- | --- |
| [Document()](#Document--) | 创建或加载文档。 |
| [Document(String fileName)](#Document-java.lang.String-) | 从文件中打开现有文档。 |
| [Document(String fileName, LoadOptions loadOptions)](#Document-java.lang.String-com.aspose.words.LoadOptions-) | 从文件中打开现有文档。 |
| [Document(InputStream stream)](#Document-java.io.InputStream-) | 初始化此类的新实例。 |
| [Document(InputStream stream, LoadOptions loadOptions)](#Document-java.io.InputStream-com.aspose.words.LoadOptions-) | 初始化此类的新实例。 |
## 方法s

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
| [ensureMinimum()](#ensureMinimum--) | 如果文档不包含任何部分，则创建一个包含一个段落的部分。 |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [expandTableStylesToDirectFormatting()](#expandTableStylesToDirectFormatting--) | 将表格样式中指定的格式转换为文档中表格的直接格式。 |
| [extractPages(int index, int count)](#extractPages-int-int-) | 返回[Document](../../com.aspose.words/document)表示指定页面范围的对象。 |
| [fetchInheritedSectionAttr(int key)](#fetchInheritedSectionAttr-int-) |  |
| [fetchSectionAttr(int key)](#fetchSectionAttr-int-) |  |
| [get()](#get--) |  |
| [getAncestor(int ancestor类型)](#getAncestor-int-) |  |
| [getAncestor(班级 ancestor类型)](#getAncestor-java.lang.班级-) | 获取指定对象类型的第一个祖先。 |
| [getAttachedTemplate()](#getAttachedTemplate--) | 获取附加到文档的模板的完整路径。 |
| [getAutomaticallyUpdateStyles()](#getAutomaticallyUpdateStyles--) | 获取一个标志，指示每次在 MS Word 中打开文档时是否更新文档中的样式以匹配附加模板中的样式。 |
| [getBackgroundShape()](#getBackgroundShape--) | 获取文档的背景形状。 |
| [getBuiltInDocumentProperties()](#getBuiltInDocumentProperties--) | 返回一个集合，该集合表示文档的所有内置文档属性。 |
| [getChild(int node类型, int index, boolean isDeep)](#getChild-int-int-boolean-) |  |
| [getChildNodes()](#getChildNodes--) | 获取此节点的所有直接子节点。 |
| [getChildNodes(int node类型, boolean isDeep)](#getChildNodes-int-boolean-) |  |
| [get班级()](#get班级--) |  |
| [getCompatibilityOptions()](#getCompatibilityOptions--) | 提供对文档兼容性选项的访问（即，在**Compatibility**的选项卡**Options**Word 中的对话框）。 |
| [getCompliance()](#getCompliance--) | 获取根据加载的文档内容确定的 OOXML 合规性版本。 |
| [getContainer()](#getContainer--) |  |
| [getCount()](#getCount--) | 获取此节点的直接子节点数。 |
| [getCurrentNode()](#getCurrentNode--) |  |
| [getCustomDocumentProperties()](#getCustomDocumentProperties--) | 返回一个集合，该集合表示文档的所有自定义文档属性。 |
| [getCustomNodeId()](#getCustomNodeId--) | 指定自定义节点标识符。 |
| [getCustomXmlParts()](#getCustomXmlParts--) | 获取自定义 XML 数据存储部件的集合。 |
| [getDefaultTabStop()](#getDefaultTabStop--) | 获取默认制表位之间的间隔（以磅为单位）。 |
| [getDigitalSignatures()](#getDigitalSignatures--) | 获取此文档的数字签名集合及其验证结果。 |
| [getDirectSectionAttr(int key)](#getDirectSectionAttr-int-) |  |
| [getDocument()](#getDocument--) |  |
| [getEndnoteOptions()](#getEndnoteOptions--) | 提供控制本文档中尾注编号和位置的选项。 |
| [get字段Options()](#get字段Options--) | 得到一个**字段Options**表示用于控制文档中的字段处理的选项的对象。 |
| [getFirstChild()](#getFirstChild--) | 获取节点的第一个子节点。 |
| [getFirstSection()](#getFirstSection--) | 获取文档中的第一部分。 |
| [getFontInfos()](#getFontInfos--) | 提供对本文档中使用的字体属性的访问。 |
| [getFontSettings()](#getFontSettings--) | 获取文档字体设置。 |
| [getFootnoteOptions()](#getFootnoteOptions--) | 提供控制本文档中脚注的编号和位置的选项。 |
| [getFrameset()](#getFrameset--) | 返回一个[getFrameset()](../../com.aspose.words/document\#getFrameset--)例如，如果此文档表示一个框架页面。 |
| [getGlossaryDocument()](#getGlossaryDocument--) | 获取此文档或模板中的词汇表文档。 |
| [getGrammarChecked()](#getGrammarChecked--) | 退货**true**如果文档已经过语法检查。 |
| [getHyphenationOptions()](#getHyphenationOptions--) | 提供对文档断字选项的访问。 |
| [getLastChild()](#getLastChild--) | 获取节点的最后一个子节点。 |
| [getLastSection()](#getLastSection--) | 获取文档中的最后一部分。 |
| [getLayoutOptions()](#getLayoutOptions--) | 得到一个**LayoutOptions**表示用于控制此文档的布局过程的选项的对象。 |
| [getLists()](#getLists--) | 提供对文档中使用的列表格式的访问。 |
| [getMailMerge()](#getMailMerge--) | 返回一个**MailMerge**表示文档的邮件合并功能的对象。 |
| [getMailMergeSettings()](#getMailMergeSettings--) | 获取包含文档的所有邮件合并信息的对象。 |
| [getNextMatchingNode(Node curNode)](#getNextMatchingNode-com.aspose.words.Node-) |  |
| [getNextSibling()](#getNextSibling--) | 获取紧跟此节点的节点。 |
| [getNodeChangingCallback()](#getNodeChangingCallback--) | 在文档中插入或删除节点时调用。 |
| [getNode类型()](#getNode类型--) | 退货**Node类型.Document**. |
| [getOriginalFileName()](#getOriginalFileName--) | 获取文档的原始文件名。 |
| [getOriginalLoadFormat()](#getOriginalLoadFormat--) | 获取加载到此对象中的原始文档的格式。 |
| [get包裹CustomParts()](#get包裹CustomParts--) | 获取使用“未知关系”链接到 OOXML 包的自定义部件（任意内容）的集合。 |
| [getPageColor()](#getPageColor--) | 获取文档的页面颜色。 |
| [getPageCount()](#getPageCount--) | 获取由最近的页面布局操作计算的文档中的页数。 |
| [getPageInfo(int pageIndex)](#getPageInfo-int-) | 获取可能对打印或呈现有用的页面的页面大小、方向和其他信息。 |
| [getParentNode()](#getParentNode--) | 获取此节点的直接父节点。 |
| [getPreviousSibling()](#getPreviousSibling--) | 获取紧接在此节点之前的节点。 |
| [getProtection类型()](#getProtection类型--) | 获取当前活动的文档保护类型。 |
| [getRange()](#getRange--) | 返回一个**Range**表示包含在此节点中的文档部分的对象。 |
| [getRemovePersonalInformation()](#getRemovePersonalInformation--) | 获取一个标志，表明 Microsoft Word 将在保存文档时从注释、修订和文档属性中删除所有用户信息。 |
| [getResourceLoadingCallback()](#getResourceLoadingCallback--) | 允许控制如何加载外部资源。 |
| [getRevisions()](#getRevisions--) | 获取此文档中存在的修订（跟踪的更改）的集合。 |
| [getRevisionsView()](#getRevisionsView--) | 获取一个值，该值指示是使用文档的原始版本还是修订版本。 |
| [getSections()](#getSections--) | 返回代表文档中所有部分的集合。 |
| [getShadeFormData()](#getShadeFormData--) | 指定是否打开表单域的灰色阴影。 |
| [getShowGrammaticalErrors()](#getShowGrammaticalErrors--) | 指定是否在此文档中显示语法错误。 |
| [getShowSpellingErrors()](#getShowSpellingErrors--) | 指定是否在此文档中显示拼写错误。 |
| [getSpellingChecked()](#getSpellingChecked--) | 退货**true**如果文档已经过拼写检查。 |
| [getStyles()](#getStyles--) | 返回文档中定义的样式集合。 |
| [getText()](#getText--) | 获取此节点及其所有子节点的文本。 |
| [getTheme()](#getTheme--) | 获取[getTheme()](../../com.aspose.words/document\#getTheme--)本文档的对象。 |
| [getTrackRevisions()](#getTrackRevisions--) | **True**如果在 Microsoft Word 中编辑此文档时跟踪更改。 |
| [getVariables()](#getVariables--) | 返回添加到文档或模板的变量集合。 |
| [getVbaProject()](#getVbaProject--) | 得到一个[getVbaProject()](../../com.aspose.words/document\#getVbaProject--) / [setVbaProject(com.aspose.words.VbaProject)](../../com.aspose.words/document\#setVbaProject-com.aspose.words.VbaProject-). |
| [getVersionsCount()](#getVersionsCount--) | 获取存储在 DOC 文档中的文档版本数。 |
| [getViewOptions()](#getViewOptions--) | 提供用于控制文档在 Microsoft Word 中的显示方式的选项。 |
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
| [insertAfter(Node newChild, Node refChild)](#insertAfter-com.aspose.words.Node-com.aspose.words.Node-) | 在指定的参考节点之后立即插入指定的节点。 |
| [insertBefore(Node newChild, Node refChild)](#insertBefore-com.aspose.words.Node-com.aspose.words.Node-) | 在指定的参考节点之前插入指定的节点。 |
| [isComposite()](#isComposite--) | 返回 true，因为此节点可以有子节点。 |
| [iterator()](#iterator--) | 为在此节点的子节点上的每个样式迭代提供支持。 |
| [joinRunsWithSameFormatting()](#joinRunsWithSameFormatting--) | 连接在文档的所有段落中以相同的格式运行。 |
| [nextPreOrder(Node rootNode)](#nextPreOrder-com.aspose.words.Node-) | 根据前序树遍历算法获取下一个节点。 |
| [node类型ToString(int node类型)](#node类型ToString-int-) |  |
| [normalize字段类型s()](#normalize字段类型s--) | 更改字段类型值[字段Char.get字段类型()](../../com.aspose.words/fieldchar\#get字段类型--)的[字段Start](../../com.aspose.words/fieldstart), [字段Separator](../../com.aspose.words/fieldseparator), [字段End](../../com.aspose.words/fieldend)在整个文档中，以便它们对应于域代码中包含的域类型。 |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [prependChild(Node newChild)](#prependChild-com.aspose.words.Node-) | 将指定节点添加到此节点的子节点列表的开头。 |
| [previousPreOrder(Node rootNode)](#previousPreOrder-com.aspose.words.Node-) | 根据前序树遍历算法获取上一个节点。 |
| [print()](#print--) | 打印文档而不显示任何用户界面表单。 |
| [print(String printerName)](#print-java.lang.String-) | 使用标准（无用户界面）打印控制器将整个文档打印到指定的打印机。 |
| [print(AttributeSet printerSettings)](#print-javax.print.attribute.AttributeSet-) | 根据指定的打印机设置，使用标准（无用户界面）打印控制器打印文档。 |
| [print(AttributeSet printerSettings, String documentName)](#print-javax.print.attribute.AttributeSet-java.lang.String-) | 根据指定的打印机设置，使用标准（无用户界面）打印控制器和文档名称打印文档。 |
| [protect(int type)](#protect-int-) |  |
| [protect(int type, String password)](#protect-int-java.lang.String-) |  |
| [remove()](#remove--) |  |
| [removeAllChildren()](#removeAllChildren--) | 移除当前节点的所有子节点。 |
| [removeChild(Node oldChild)](#removeChild-com.aspose.words.Node-) | 移除指定的子节点。 |
| [removeExternalSchemaReferences()](#removeExternalSchemaReferences--) | 从此文档中删除外部 XML 模式引用。 |
| [removeMacros()](#removeMacros--) | 从文档中删除所有宏（VBA 项目）以及工具栏和命令自定义。 |
| [removeSmartTags()](#removeSmartTags--) | 删除所有[SmartTag](../../com.aspose.words/smarttag)当前节点的后代节点。 |
| [renderToScale(int pageIndex, Graphics2D graphics, float x, float y, float scale)](#renderToScale-int-java.awt.Graphics2D-float-float-float-) | 将文档页面渲染为指定比例的对象。 |
| [renderToSize(int pageIndex, Graphics2D graphics, float x, float y, float width, float height)](#renderToSize-int-java.awt.Graphics2D-float-float-float-float-) | 将文档页面呈现为指定大小的对象。 |
| [save(OutputStream stream, SaveOptions saveOptions)](#save-java.io.OutputStream-com.aspose.words.SaveOptions-) |  |
| [save(OutputStream stream, int saveFormat)](#save-java.io.OutputStream-int-) |  |
| [save(String fileName)](#save-java.lang.String-) | 保存文档。 |
| [save(String fileName, SaveOptions saveOptions)](#save-java.lang.String-com.aspose.words.SaveOptions-) | 使用指定的保存选项将文档保存到文件中。 |
| [save(String fileName, int saveFormat)](#save-java.lang.String-int-) |  |
| [selectNodes(String xpath)](#selectNodes-java.lang.String-) | 选择与 XPath 表达式匹配的节点列表。 |
| [selectSingleNode(String xpath)](#selectSingleNode-java.lang.String-) | 选择与 XPath 表达式匹配的第一个节点。 |
| [setAttachedTemplate(String value)](#setAttachedTemplate-java.lang.String-) | 设置附加到文档的模板的完整路径。 |
| [setAutomaticallyUpdateStyles(boolean value)](#setAutomaticallyUpdateStyles-boolean-) | 设置一个标志，指示每次在 MS Word 中打开文档时是否更新文档中的样式以匹配附加模板中的样式。 |
| [setBackgroundShape(Shape value)](#setBackgroundShape-com.aspose.words.Shape-) | 设置文档的背景形状。 |
| [setCustomNodeId(int value)](#setCustomNodeId-int-) | 指定自定义节点标识符。 |
| [setCustomXmlParts(CustomXmlPartCollection value)](#setCustomXmlParts-com.aspose.words.CustomXmlPartCollection-) | 设置自定义 XML 数据存储部件的集合。 |
| [setDefaultTabStop(double value)](#setDefaultTabStop-double-) | 设置默认制表位之间的间隔（以磅为单位）。 |
| [setFontSettings(FontSettings value)](#setFontSettings-com.aspose.words.FontSettings-) | 设置文档字体设置。 |
| [setGlossaryDocument(GlossaryDocument value)](#setGlossaryDocument-com.aspose.words.GlossaryDocument-) | 在此文档或模板中设置词汇表文档。 |
| [setGrammarChecked(boolean value)](#setGrammarChecked-boolean-) | 退货**true**如果文档已经过语法检查。 |
| [setMailMergeSettings(MailMergeSettings value)](#setMailMergeSettings-com.aspose.words.MailMergeSettings-) | 设置包含文档的所有邮件合并信息的对象。 |
| [setNodeChangingCallback(INodeChangingCallback value)](#setNodeChangingCallback-com.aspose.words.INodeChangingCallback-) | 在文档中插入或删除节点时调用。 |
| [set包裹CustomParts(CustomPartCollection value)](#set包裹CustomParts-com.aspose.words.CustomPartCollection-) | 设置使用“未知关系”链接到 OOXML 包的自定义部分（任意内容）的集合。 |
| [setPageColor(Color value)](#setPageColor-java.awt.Color-) | 设置文档的页面颜色。 |
| [setRemovePersonalInformation(boolean value)](#setRemovePersonalInformation-boolean-) | 设置一个标志，表明 Microsoft Word 将在保存文档时从注释、修订和文档属性中删除所有用户信息。 |
| [setResourceLoadingCallback(IResourceLoadingCallback value)](#setResourceLoadingCallback-com.aspose.words.IResourceLoadingCallback-) | 允许控制如何加载外部资源。 |
| [setRevisionsView(int value)](#setRevisionsView-int-) | 设置一个值，该值指示是使用文档的原始版本还是修订版本。 |
| [setSectionAttr(int key, Object value)](#setSectionAttr-int-java.lang.Object-) |  |
| [setShadeFormData(boolean value)](#setShadeFormData-boolean-) | 指定是否打开表单域的灰色阴影。 |
| [setShowGrammaticalErrors(boolean value)](#setShowGrammaticalErrors-boolean-) | 指定是否在此文档中显示语法错误。 |
| [setShowSpellingErrors(boolean value)](#setShowSpellingErrors-boolean-) | 指定是否在此文档中显示拼写错误。 |
| [setSpellingChecked(boolean value)](#setSpellingChecked-boolean-) | 退货**true**如果文档已经过拼写检查。 |
| [setTrackRevisions(boolean value)](#setTrackRevisions-boolean-) | **True**如果在 Microsoft Word 中编辑此文档时跟踪更改。 |
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
| fileName | java.lang.String | File name of the document to open. |

### Document(String fileName, LoadOptions loadOptions) {#Document-java.lang.String-com.aspose.words.LoadOptions-}
```
public Document(String fileName, LoadOptions loadOptions)
```


Opens an existing document from a file. Allows to specify additional options such as an encryption password.

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| fileName | java.lang.String | File name of the document to open. |
| loadOptions | [LoadOptions](../../com.aspose.words/loadoptions) | Additional options to use when loading a document. Can be null. |

### Document(InputStream stream) {#Document-java.io.InputStream-}
```
public Document(InputStream stream)
```


Initializes a new instance of this class.

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| stream | java.io.InputStream |  |

### Document(InputStream stream, LoadOptions loadOptions) {#Document-java.io.InputStream-com.aspose.words.LoadOptions-}
```
public Document(InputStream stream, LoadOptions loadOptions)
```


Initializes a new instance of this class.

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| stream | java.io.InputStream |  |
| loadOptions | [LoadOptions](../../com.aspose.words/loadoptions) |  |

### accept(DocumentVisitor visitor) {#accept-com.aspose.words.DocumentVisitor-}
```
public boolean accept(DocumentVisitor visitor)
```


Accepts a visitor.

Enumerates over this node and all of its children. Each node calls a corresponding method on DocumentVisitor.

For more info see the Visitor design pattern.

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| visitor | [DocumentVisitor](../../com.aspose.words/documentvisitor) | The visitor that will visit the nodes. |

**退货:**
boolean - True if all nodes were visited; false if DocumentVisitor stopped the operation before visiting all nodes. Calls DocumentVisitor.VisitDocumentStart, then calls Accept for all child nodes of the document and calls DocumentVisitor.VisitDocumentEnd at the end.
### acceptAllRevisions() {#acceptAllRevisions--}
```
public void acceptAllRevisions()
```


Accepts all tracked changes in the document. This method is a shortcut for [RevisionCollection.acceptAll()](../../com.aspose.words/revisioncollection\#acceptAll--).

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


Adds the specified node to the end of the list of child nodes for this node.

If the newChild is already in the tree, it is first removed.

If the node being inserted was created from another document, you should use **M:Aspose.Words.DocumentBase.ImportNode(Aspose.Words.Node,System.Boolean,Aspose.Words.ImportFormatMode)** to import the node to the current document. The imported node can then be inserted into the current document.

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| newChild | [Node](../../com.aspose.words/node) | The node to add. |

**退货:**
[Node](../../com.aspose.words/node) - The node added.
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


Cleans unused styles and lists from the document.

### cleanup(CleanupOptions options) {#cleanup-com.aspose.words.CleanupOptions-}
```
public void cleanup(CleanupOptions options)
```


Cleans unused styles and lists from the document depending on given [CleanupOptions](../../com.aspose.words/cleanupoptions).

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


Compares this document with another document producing changes as number of edit and format revisions [Revision](../../com.aspose.words/revision).

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| document | [Document](../../com.aspose.words/document) | Document to compare. |
| author | java.lang.String | Initials of the author to use for revisions. |
| dateTime | java.util.Date | The date and time to use for revisions. The following document nodes are not compared at the moment:

 *  [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag)
 *  Item3

Documents must not have revisions before comparison. |

### compare(Document document, String author, Date dateTime, CompareOptions options) {#compare-com.aspose.words.Document-java.lang.String-java.util.Date-com.aspose.words.CompareOptions-}
```
public void compare(Document document, String author, Date dateTime, CompareOptions options)
```


Compares this document with another document producing changes as a number of edit and format revisions [Revision](../../com.aspose.words/revision). Allows to specify comparison options using [CompareOptions](../../com.aspose.words/compareoptions).

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


Copies styles from the specified template to a document. When styles are copied from a template to a document, like-named styles in the document are redefined to match the style descriptions in the template. Unique styles from the template are copied to the document. Unique styles in the document remain intact.

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| template | [Document](../../com.aspose.words/document) |  |

### copyStylesFromTemplate(String template) {#copyStylesFromTemplate-java.lang.String-}
```
public void copyStylesFromTemplate(String template)
```


Copies styles from the specified template to a document. When styles are copied from a template to a document, like-named styles in the document are redefined to match the style descriptions in the template. Unique styles from the template are copied to the document. Unique styles in the document remain intact.

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


Performs a deep copy of the [Document](../../com.aspose.words/document).

**退货:**
[Document](../../com.aspose.words/document) - The cloned document.
### deepClone(boolean isCloneChildren) {#deepClone-boolean-}
```
public Node deepClone(boolean isCloneChildren)
```


Creates a duplicate of the node.

This method serves as a copy constructor for nodes. The cloned node has no parent, but belongs to the same document as the original node.

This method always performs a deep copy of the node. The *isCloneChildren* parameter specifies whether to perform copy all child nodes as well.

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| isCloneChildren | boolean | True to recursively clone the subtree under the specified node; false to clone only the node itself. |

**退货:**
[Node](../../com.aspose.words/node) - The cloned node.
### ensureMinimum() {#ensureMinimum--}
```
public void ensureMinimum()
```


If the document contains no sections, creates one section with one paragraph.

### equals(Object arg0) {#equals-java.lang.Object-}
```
public boolean equals(Object arg0)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**退货:**
boolean
### expandTableStylesToDirectFormatting() {#expandTableStylesToDirectFormatting--}
```
public void expandTableStylesToDirectFormatting()
```


Converts formatting specified in table styles into direct formatting on tables in the document.

This method exists because this version of Aspose.Words provides only limited support for table styles (see below). This method might be useful when you load a DOCX or WordprocessingML document that contains tables formatted with table styles and you need to query formatting of tables, cells, paragraphs or text.

This version of Aspose.Words provides limited support for table styles as follows:

 *  Table styles defined in DOCX or WordprocessingML documents are preserved as table styles when saving the document as DOCX or WordprocessingML.
 *  Table styles defined in DOCX or WordprocessingML documents are automatically converted to direct formatting on tables when saving the document into any other format, rendering or printing.
 *  Table styles defined in DOC documents are preserved as table styles when saving the document as DOC only.

### extractPages(int index, int count) {#extractPages-int-int-}
```
public Document extractPages(int index, int count)
```


退货 the [Document](../../com.aspose.words/document) object representing specified range of pages. The resulting document should look like the one in MS Word, as if we had performed 'Print specific pages' \\u2013 the numbering, headers/footers and cross tables layout will be preserved. But due to a large number of nuances, appearing while reducing the number of pages, full match of the layout is a quiet complicated task requiring a lot of effort. Depending on the document complexity there might be slight differences in the resulting document contents layout comparing to the source document. Any feedback would be greatly appreciated.

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| index | int | The zero-based index of the first page to extract. |
| count | int | Number of pages to be extracted. |

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
### getAncestor(int ancestor类型) {#getAncestor-int-}
```
public CompositeNode getAncestor(int ancestor类型)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| ancestor类型 | int |  |

**退货:**
[CompositeNode](../../com.aspose.words/compositenode)
### getAncestor(班级 ancestor类型) {#getAncestor-java.lang.班级-}
```
public CompositeNode getAncestor(班级 ancestor类型)
```


Gets the first ancestor of the specified object type.

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| ancestor类型 | java.lang.班级 | The object type of the ancestor to retrieve. |

**退货:**
[CompositeNode](../../com.aspose.words/compositenode) - The ancestor of the specified type or null if no ancestor of this type was found.

The ancestor type matches if it is equal to ancestor类型 or derived from ancestor类型.
### getAttachedTemplate() {#getAttachedTemplate--}
```
public String getAttachedTemplate()
```


Gets the full path of the template attached to the document.

Empty string means the document is attached to the Normal template.

**退货:**
java.lang.String - The full path of the template attached to the document.
### getAutomaticallyUpdateStyles() {#getAutomaticallyUpdateStyles--}
```
public boolean getAutomaticallyUpdateStyles()
```


Gets a flag indicating whether the styles in the document are updated to match the styles in the attached template each time the document is opened in MS Word.

**退货:**
boolean - A flag indicating whether the styles in the document are updated to match the styles in the attached template each time the document is opened in MS Word.
### getBackgroundShape() {#getBackgroundShape--}
```
public Shape getBackgroundShape()
```


Gets the background shape of the document. Can be null.

Microsoft Word allows only a shape that has its [ShapeBase.getShape类型()](../../com.aspose.words/shapebase\#getShape类型--) property equal to [Shape类型.RECTANGLE](../../com.aspose.words/shapetype\#RECTANGLE) to be used as a background shape for a document.

Microsoft Word supports only the fill properties of a background shape. All other properties are ignored.

Setting this property to a non-null value will also set the [ViewOptions.getDisplayBackgroundShape()](../../com.aspose.words/viewoptions\#getDisplayBackgroundShape--) / [ViewOptions.setDisplayBackgroundShape(boolean)](../../com.aspose.words/viewoptions\#setDisplayBackgroundShape-boolean-) to true.

**退货:**
[Shape](../../com.aspose.words/shape) - The background shape of the document.
### getBuiltInDocumentProperties() {#getBuiltInDocumentProperties--}
```
public BuiltInDocumentProperties getBuiltInDocumentProperties()
```


退货 a collection that represents all the built-in document properties of the document.

**退货:**
[BuiltInDocumentProperties](../../com.aspose.words/builtindocumentproperties) - A collection that represents all the built-in document properties of the document.
### getChild(int node类型, int index, boolean isDeep) {#getChild-int-int-boolean-}
```
public Node getChild(int node类型, int index, boolean isDeep)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| node类型 | int |  |
| index | int |  |
| isDeep | boolean |  |

**退货:**
[Node](../../com.aspose.words/node)
### getChildNodes() {#getChildNodes--}
```
public NodeCollection getChildNodes()
```


Gets all immediate child nodes of this node.

Note, [getChildNodes()](../../com.aspose.words/compositenode\#getChildNodes--) is equivalent to calling  GetChildNodes(Node类型.Any, false)  and creates and returns a new collection every time it is accessed.

If there are no child nodes, this property returns an empty collection.

**退货:**
[NodeCollection](../../com.aspose.words/nodecollection) - All immediate child nodes of this node.
### getChildNodes(int node类型, boolean isDeep) {#getChildNodes-int-boolean-}
```
public NodeCollection getChildNodes(int node类型, boolean isDeep)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| node类型 | int |  |
| isDeep | boolean |  |

**退货:**
[NodeCollection](../../com.aspose.words/nodecollection)
### get班级() {#get班级--}
```
public final native 班级<?> get班级()
```




**退货:**
java.lang.班级<?>
### getCompatibilityOptions() {#getCompatibilityOptions--}
```
public CompatibilityOptions getCompatibilityOptions()
```


Provides access to document compatibility options (that is, the user preferences entered on the **Compatibility** tab of the **Options** dialog in Word).

**退货:**
[CompatibilityOptions](../../com.aspose.words/compatibilityoptions) - The corresponding [CompatibilityOptions](../../com.aspose.words/compatibilityoptions) value.
### getCompliance() {#getCompliance--}
```
public int getCompliance()
```


Gets the OOXML compliance version determined from the loaded document content. Makes sense only for OOXML documents.

If you created a new blank document or load non OOXML document returns the [OoxmlCompliance.ECMA\_376\_2006](../../com.aspose.words/ooxmlcompliance\#ECMA-376-2006) value.

**退货:**
int - The OOXML compliance version determined from the loaded document content. The returned value is one of [OoxmlCompliance](../../com.aspose.words/ooxmlcompliance) constants.
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


Gets the number of immediate children of this node.

**退货:**
int - The number of immediate children of this node.
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


退货 a collection that represents all the custom document properties of the document.

**退货:**
[CustomDocumentProperties](../../com.aspose.words/customdocumentproperties) - A collection that represents all the custom document properties of the document.
### getCustomNodeId() {#getCustomNodeId--}
```
public int getCustomNodeId()
```


Specifies custom node identifier.

Default is zero.

This identifier can be set and used arbitrarily. For example, as a key to get external data.

Important note, specified value is not saved to an output file and exists only during the node lifetime.

**退货:**
int - The corresponding  int  value.
### getCustomXmlParts() {#getCustomXmlParts--}
```
public CustomXmlPartCollection getCustomXmlParts()
```


Gets the collection of Custom XML Data Storage Parts.

Aspose.Words loads and saves Custom XML Parts into OOXML and DOC documents only.

This property cannot be  null .

**退货:**
[CustomXmlPartCollection](../../com.aspose.words/customxmlpartcollection) - The collection of Custom XML Data Storage Parts.
### getDefaultTabStop() {#getDefaultTabStop--}
```
public double getDefaultTabStop()
```


Gets the interval (in points) between the default tab stops.

**退货:**
double - The interval (in points) between the default tab stops.
### getDigitalSignatures() {#getDigitalSignatures--}
```
public DigitalSignatureCollection getDigitalSignatures()
```


Gets the collection of digital signatures for this document and their validation results.

This collection contains digital signatures that were loaded from the original document. These digital signatures will not be saved when you save this [Document](../../com.aspose.words/document) object into a file or stream because saving or converting will produce a document that is different from the original and the original digital signatures will no longer be valid.

This collection is never null. If the document is not signed, it will contain zero elements.

**退货:**
[DigitalSignatureCollection](../../com.aspose.words/digitalsignaturecollection) - The collection of digital signatures for this document and their validation results.
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


Gets the document to which this node belongs.

The node always belongs to a document even if it has just been created and not yet added to the tree, or if it has been removed from the tree.

**退货:**
[DocumentBase](../../com.aspose.words/documentbase)
### getEndnoteOptions() {#getEndnoteOptions--}
```
public EndnoteOptions getEndnoteOptions()
```


Provides options that control numbering and positioning of endnotes in this document.

**退货:**
[EndnoteOptions](../../com.aspose.words/endnoteoptions) - The corresponding [EndnoteOptions](../../com.aspose.words/endnoteoptions) value.
### get字段Options() {#get字段Options--}
```
public 字段Options get字段Options()
```


Gets a **字段Options** object that represents options to control field handling in the document.

**退货:**
[字段Options](../../com.aspose.words/fieldoptions) - A **字段Options** object that represents options to control field handling in the document.
### getFirstChild() {#getFirstChild--}
```
public Node getFirstChild()
```


Gets the first child of the node. If there is no first child node, a null is returned.

**退货:**
[Node](../../com.aspose.words/node) - The first child of the node.
### getFirstSection() {#getFirstSection--}
```
public Section getFirstSection()
```


Gets the first section in the document. 退货  null  if there are no sections.

**退货:**
[Section](../../com.aspose.words/section) - The first section in the document.
### getFontInfos() {#getFontInfos--}
```
public FontInfoCollection getFontInfos()
```


Provides access to properties of fonts used in this document.

This collection of font definitions is loaded as is from the document. Font definitions might be optional, missing or incomplete in some documents.

Do not rely on this collection to ascertain that a particular font is used in the document. You should only use this collection to get information about fonts that might be used in the document.

**退货:**
[FontInfoCollection](../../com.aspose.words/fontinfocollection) - The corresponding [FontInfoCollection](../../com.aspose.words/fontinfocollection) value.
### getFontSettings() {#getFontSettings--}
```
public FontSettings getFontSettings()
```


Gets document font settings.

This property allows to specify font settings per document. If set to null, default static font settings [FontSettings.getDefaultInstance()](../../com.aspose.words/fontsettings\#getDefaultInstance--) will be used.

The default value is null.

**退货:**
[FontSettings](../../com.aspose.words/fontsettings) - Document font settings.
### getFootnoteOptions() {#getFootnoteOptions--}
```
public FootnoteOptions getFootnoteOptions()
```


Provides options that control numbering and positioning of footnotes in this document.

**退货:**
[FootnoteOptions](../../com.aspose.words/footnoteoptions) - The corresponding [FootnoteOptions](../../com.aspose.words/footnoteoptions) value.
### getFrameset() {#getFrameset--}
```
public Frameset getFrameset()
```


退货 a [getFrameset()](../../com.aspose.words/document\#getFrameset--) instance if this document represents a frames page. If the document is not framed, the property has the **null** value.

**退货:**
[Frameset](../../com.aspose.words/frameset) - A [getFrameset()](../../com.aspose.words/document\#getFrameset--) instance if this document represents a frames page.
### getGlossaryDocument() {#getGlossaryDocument--}
```
public GlossaryDocument getGlossaryDocument()
```


Gets the glossary document within this document or template. A glossary document is a storage for AutoText, AutoCorrect and Building Block entries defined in a document.

This property returns  null  if the document does not have a glossary document.

You can add a glossary document to a document by creating a [GlossaryDocument](../../com.aspose.words/glossarydocument) object and assigning to this property.

**退货:**
[GlossaryDocument](../../com.aspose.words/glossarydocument) - The glossary document within this document or template.
### getGrammarChecked() {#getGrammarChecked--}
```
public boolean getGrammarChecked()
```


退货 **true** if the document has been checked for grammar. To recheck the grammar in the document, set this property to **false**.

**退货:**
boolean - **true** if the document has been checked for grammar.
### getHyphenationOptions() {#getHyphenationOptions--}
```
public HyphenationOptions getHyphenationOptions()
```


Provides access to document hyphenation options.

**退货:**
[HyphenationOptions](../../com.aspose.words/hyphenationoptions) - The corresponding [HyphenationOptions](../../com.aspose.words/hyphenationoptions) value.
### getLastChild() {#getLastChild--}
```
public Node getLastChild()
```


Gets the last child of the node. If there is no last child node, a null is returned.

**退货:**
[Node](../../com.aspose.words/node) - The last child of the node.
### getLastSection() {#getLastSection--}
```
public Section getLastSection()
```


Gets the last section in the document. 退货  null  if there are no sections.

**退货:**
[Section](../../com.aspose.words/section) - The last section in the document.
### getLayoutOptions() {#getLayoutOptions--}
```
public LayoutOptions getLayoutOptions()
```


Gets a **LayoutOptions** object that represents options to control the layout process of this document.

**退货:**
[LayoutOptions](../../com.aspose.words/layoutoptions) - A **LayoutOptions** object that represents options to control the layout process of this document.
### getLists() {#getLists--}
```
public ListCollection getLists()
```


Provides access to the list formatting used in the document.

For more information see the description of the [ListCollection](../../com.aspose.words/listcollection) class.

**退货:**
[ListCollection](../../com.aspose.words/listcollection) - The corresponding [ListCollection](../../com.aspose.words/listcollection) value.
### getMailMerge() {#getMailMerge--}
```
public MailMerge getMailMerge()
```


退货 a **MailMerge** object that represents the mail merge functionality for the document.

**退货:**
[MailMerge](../../com.aspose.words/mailmerge) - A **MailMerge** object that represents the mail merge functionality for the document.
### getMailMergeSettings() {#getMailMergeSettings--}
```
public MailMergeSettings getMailMergeSettings()
```


Gets the object that contains all of the mail merge information for a document.

You can use this object to specify a mail merge data source for a document and this information (along with the available data fields) will appear in Microsoft Word when the user opens this document. Or you can use this object to query mail merge settings that the user has specified in Microsoft Word for this document.

This object is never null.

**退货:**
[MailMergeSettings](../../com.aspose.words/mailmergesettings) - The object that contains all of the mail merge information for a document.
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


Gets the node immediately following this node. If there is no next node, a null is returned.

**退货:**
[Node](../../com.aspose.words/node) - The node immediately following this node.
### getNodeChangingCallback() {#getNodeChangingCallback--}
```
public INodeChangingCallback getNodeChangingCallback()
```


Called when a node is inserted or removed in the document.

**退货:**
[INodeChangingCallback](../../com.aspose.words/inodechangingcallback) - The corresponding [INodeChangingCallback](../../com.aspose.words/inodechangingcallback) value.
### getNode类型() {#getNode类型--}
```
public int getNode类型()
```


退货 **Node类型.Document**.

**退货:**
int - **Node类型.Document**. The returned value is one of [Node类型](../../com.aspose.words/nodetype) constants.
### getOriginalFileName() {#getOriginalFileName--}
```
public String getOriginalFileName()
```


Gets the original file name of the document.

退货 null if the document was loaded from a stream or created blank.

**退货:**
java.lang.String - The original file name of the document.
### getOriginalLoadFormat() {#getOriginalLoadFormat--}
```
public int getOriginalLoadFormat()
```


Gets the format of the original document that was loaded into this object.

If you created a new blank document, returns the [LoadFormat.DOC](../../com.aspose.words/loadformat\#DOC) value.

**退货:**
int - The format of the original document that was loaded into this object. The returned value is one of [LoadFormat](../../com.aspose.words/loadformat) constants.
### get包裹CustomParts() {#get包裹CustomParts--}
```
public CustomPartCollection get包裹CustomParts()
```


Gets the collection of custom parts (arbitrary content) that are linked to the OOXML package using "unknown relationships".

Do not confuse these custom parts with Custom XML Data. If you need to access Custom XML parts, use the [getCustomXmlParts()](../../com.aspose.words/document\#getCustomXmlParts--) / [setCustomXmlParts(com.aspose.words.CustomXmlPartCollection)](../../com.aspose.words/document\#setCustomXmlParts-com.aspose.words.CustomXmlPartCollection-) property.

This collection contains OOXML parts whose parent is the OOXML package and they targets are of an "unknown relationship". For more information see [CustomPart](../../com.aspose.words/custompart).

Aspose.Words loads and saves custom parts into OOXML documents only.

This property cannot be  null .

**退货:**
[CustomPartCollection](../../com.aspose.words/custompartcollection) - The collection of custom parts (arbitrary content) that are linked to the OOXML package using "unknown relationships".
### getPageColor() {#getPageColor--}
```
public Color getPageColor()
```


Gets the page color of the document. This property is a simpler version of [getBackgroundShape()](../../com.aspose.words/documentbase\#getBackgroundShape--) / [setBackgroundShape(com.aspose.words.Shape)](../../com.aspose.words/documentbase\#setBackgroundShape-com.aspose.words.Shape-).

This property provides a simple way to specify a solid page color for the document. Setting this property creates and sets an appropriate [getBackgroundShape()](../../com.aspose.words/documentbase\#getBackgroundShape--) / [setBackgroundShape(com.aspose.words.Shape)](../../com.aspose.words/documentbase\#setBackgroundShape-com.aspose.words.Shape-).

If the page color is not set (e.g. there is no background shape in the document) returns a zero color.

**退货:**
java.awt.Color - The page color of the document.
### getPageCount() {#getPageCount--}
```
public int getPageCount()
```


Gets the number of pages in the document as calculated by the most recent page layout operation.

**退货:**
int - The number of pages in the document as calculated by the most recent page layout operation.
### getPageInfo(int pageIndex) {#getPageInfo-int-}
```
public PageInfo getPageInfo(int pageIndex)
```


Gets the page size, orientation and other information about a page that might be useful for printing or rendering.

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| pageIndex | int | The 0-based page index. |

**退货:**
[PageInfo](../../com.aspose.words/pageinfo)
### getParentNode() {#getParentNode--}
```
public CompositeNode getParentNode()
```


Gets the immediate parent of this node.

If a node has just been created and not yet added to the tree, or if it has been removed from the tree, the parent is null.

**退货:**
[CompositeNode](../../com.aspose.words/compositenode) - The immediate parent of this node.
### getPreviousSibling() {#getPreviousSibling--}
```
public Node getPreviousSibling()
```


Gets the node immediately preceding this node. If there is no preceding node, a null is returned.

**退货:**
[Node](../../com.aspose.words/node) - The node immediately preceding this node.
### getProtection类型() {#getProtection类型--}
```
public int getProtection类型()
```


Gets the currently active document protection type.

This property allows to retrieve the currently set document protection type. To change the document protection type use the **M:Aspose.Words.Document.Protect(Aspose.Words.Protection类型,System.String)** and [unprotect()](../../com.aspose.words/document\#unprotect--) methods.

When a document is protected, the user can make only limited changes, such as adding annotations, making revisions, or completing a form.

Note that document protection is different from write protection. Write protection is specified using the [getWriteProtection()](../../com.aspose.words/document\#getWriteProtection--)

**M:Aspose.Words.Document.Protect(Aspose.Words.Protection类型,System.String)**

**退货:**
int - The currently active document protection type. The returned value is one of [Protection类型](../../com.aspose.words/protectiontype) constants.
### getRange() {#getRange--}
```
public Range getRange()
```


退货 a **Range** object that represents the portion of a document that is contained in this node.

**退货:**
[Range](../../com.aspose.words/range) - A **Range** object that represents the portion of a document that is contained in this node.
### getRemovePersonalInformation() {#getRemovePersonalInformation--}
```
public boolean getRemovePersonalInformation()
```


Gets a flag indicating that Microsoft Word will remove all user information from comments, revisions and document properties upon saving the document.

**退货:**
boolean - A flag indicating that Microsoft Word will remove all user information from comments, revisions and document properties upon saving the document.
### getResourceLoadingCallback() {#getResourceLoadingCallback--}
```
public IResourceLoadingCallback getResourceLoadingCallback()
```


Allows to control how external resources are loaded.

**退货:**
[IResourceLoadingCallback](../../com.aspose.words/iresourceloadingcallback) - The corresponding [IResourceLoadingCallback](../../com.aspose.words/iresourceloadingcallback) value.
### getRevisions() {#getRevisions--}
```
public RevisionCollection getRevisions()
```


Gets a collection of revisions (tracked changes) that exist in this document.

The returned collection is a "live" collection, which means if you remove parts of a document that contain revisions, the deleted revisions will automatically disappear from this collection.

**退货:**
[RevisionCollection](../../com.aspose.words/revisioncollection) - A collection of revisions (tracked changes) that exist in this document.
### getRevisionsView() {#getRevisionsView--}
```
public int getRevisionsView()
```


Gets a value indicating whether to work with the original or revised version of a document. The default value is  **[RevisionsView.ORIGINAL](../../com.aspose.words/revisionsview\#ORIGINAL)** .

**退货:**
int - A value indicating whether to work with the original or revised version of a document. The returned value is one of [RevisionsView](../../com.aspose.words/revisionsview) constants.
### getSections() {#getSections--}
```
public SectionCollection getSections()
```


退货 a collection that represents all sections in the document.

**退货:**
[SectionCollection](../../com.aspose.words/sectioncollection) - A collection that represents all sections in the document.
### getShadeFormData() {#getShadeFormData--}
```
public boolean getShadeFormData()
```


Specifies whether to turn on the gray shading on form fields.

**退货:**
boolean - The corresponding  boolean  value.
### getShowGrammaticalErrors() {#getShowGrammaticalErrors--}
```
public boolean getShowGrammaticalErrors()
```


Specifies whether to display grammar errors in this document.

**退货:**
boolean - The corresponding  boolean  value.
### getShowSpellingErrors() {#getShowSpellingErrors--}
```
public boolean getShowSpellingErrors()
```


Specifies whether to display spelling errors in this document.

**退货:**
boolean - The corresponding  boolean  value.
### getSpellingChecked() {#getSpellingChecked--}
```
public boolean getSpellingChecked()
```


退货 **true** if the document has been checked for spelling. To recheck the spelling in the document, set this property to **false**.

**退货:**
boolean - **true** if the document has been checked for spelling.
### getStyles() {#getStyles--}
```
public StyleCollection getStyles()
```


退货 a collection of styles defined in the document.

For more information see the description of the [StyleCollection](../../com.aspose.words/stylecollection) class.

**退货:**
[StyleCollection](../../com.aspose.words/stylecollection) - A collection of styles defined in the document.
### getText() {#getText--}
```
public String getText()
```


Gets the text of this node and of all its children.

The returned string includes all control and special characters as described in [ControlChar](../../com.aspose.words/controlchar).

**退货:**
java.lang.String
### getTheme() {#getTheme--}
```
public Theme getTheme()
```


Gets the [getTheme()](../../com.aspose.words/document\#getTheme--) object for this document.

**退货:**
[Theme](../../com.aspose.words/theme) - The [getTheme()](../../com.aspose.words/document\#getTheme--) object for this document.
### getTrackRevisions() {#getTrackRevisions--}
```
public boolean getTrackRevisions()
```


**True** if changes are tracked when this document is edited in Microsoft Word.

Setting this option only instructs Microsoft Word whether the track changes is turned on or off. This property has no effect on changes to the document that you make programmatically via Aspose.Words.

If you want to automatically track changes as they are made programmatically by Aspose.Words to this document use the [startTrackRevisions(java.lang.String, java.util.Date)](../../com.aspose.words/document\#startTrackRevisions-java.lang.String--java.util.Date-) method.

**退货:**
boolean - The corresponding  boolean  value.
### getVariables() {#getVariables--}
```
public VariableCollection getVariables()
```


退货 the collection of variables added to a document or template.

**退货:**
[VariableCollection](../../com.aspose.words/variablecollection) - The collection of variables added to a document or template.
### getVbaProject() {#getVbaProject--}
```
public VbaProject getVbaProject()
```


Gets a [getVbaProject()](../../com.aspose.words/document\#getVbaProject--) / [setVbaProject(com.aspose.words.VbaProject)](../../com.aspose.words/document\#setVbaProject-com.aspose.words.VbaProject-).

**退货:**
[VbaProject](../../com.aspose.words/vbaproject) - A [getVbaProject()](../../com.aspose.words/document\#getVbaProject--) / [setVbaProject(com.aspose.words.VbaProject)](../../com.aspose.words/document\#setVbaProject-com.aspose.words.VbaProject-).
### getVersionsCount() {#getVersionsCount--}
```
public int getVersionsCount()
```


Gets the number of document versions that was stored in the DOC document.

Versions in Microsoft Word are accessed via the File/Versions menu. Microsoft Word supports versions only for DOC files.

This property allows to detect if there were document versions stored in this document before it was opened in Aspose.Words. Aspose.Words provides no other support for document versions. If you save this document using Aspose.Words, the document will be saved without versions.

**退货:**
int - The number of document versions that was stored in the DOC document.
### getViewOptions() {#getViewOptions--}
```
public ViewOptions getViewOptions()
```


Provides options to control how the document is displayed in Microsoft Word.

**退货:**
[ViewOptions](../../com.aspose.words/viewoptions) - The corresponding [ViewOptions](../../com.aspose.words/viewoptions) value.
### getWarningCallback() {#getWarningCallback--}
```
public IWarningCallback getWarningCallback()
```


Called during various document processing procedures when an issue is detected that might result in data or formatting fidelity loss. Document may generate warnings at any stage of its existence, so it's important to setup warning callback as early as possible to avoid the warnings loss. E.g. such properties as [Document.getPageCount()](../../com.aspose.words/document\#getPageCount--) actually build the document layout which is used later for rendering, and the layout warnings may be lost if warning callback is specified just for the rendering calls later.

**退货:**
[IWarningCallback](../../com.aspose.words/iwarningcallback) - The corresponding [IWarningCallback](../../com.aspose.words/iwarningcallback) value.
### getWatermark() {#getWatermark--}
```
public Watermark getWatermark()
```


Provides access to the document watermark.

**退货:**
[Watermark](../../com.aspose.words/watermark) - The corresponding [Watermark](../../com.aspose.words/watermark) value.
### getWebExtensionTaskPanes() {#getWebExtensionTaskPanes--}
```
public TaskPaneCollection getWebExtensionTaskPanes()
```


退货 a collection that represents a list of task pane add-ins.

**退货:**
[TaskPaneCollection](../../com.aspose.words/taskpanecollection) - A collection that represents a list of task pane add-ins.
### getWriteProtection() {#getWriteProtection--}
```
public WriteProtection getWriteProtection()
```


Provides access to the document write protection options.

**退货:**
[WriteProtection](../../com.aspose.words/writeprotection) - The corresponding [WriteProtection](../../com.aspose.words/writeprotection) value.
### hasChildNodes() {#hasChildNodes--}
```
public boolean hasChildNodes()
```


退货 true if this node has any child nodes.

**退货:**
boolean - True if this node has any child nodes.
### hasMacros() {#hasMacros--}
```
public boolean hasMacros()
```


退货 **true** if the document has a VBA project (macros).

**退货:**
boolean - **true** if the document has a VBA project (macros).
### hasRevisions() {#hasRevisions--}
```
public boolean hasRevisions()
```


退货 **true** if the document has any tracked changes. This property is a shortcut for comparing [RevisionCollection.getCount()](../../com.aspose.words/revisioncollection\#getCount--) to zero.

**退货:**
boolean - **true** if the document has any tracked changes.
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**退货:**
int
### importNode(Node srcNode, boolean isImportChildren) {#importNode-com.aspose.words.Node-boolean-}
```
public Node importNode(Node srcNode, boolean isImportChildren)
```


Imports a node from another document to the current document.

Imports a node from another document to the current document.

This method uses the [ImportFormatMode.USE\_DESTINATION\_STYLES](../../com.aspose.words/importformatmode\#USE-DESTINATION-STYLES) option to resolve formatting.

Importing a node creates a copy of the source node belonging to the importing document. The returned node has no parent. The source node is not altered or removed from the original document.

Before a node from another document can be inserted into this document, it must be imported. During import, document-specific properties such as references to styles and lists are translated from the original to the importing document. After the node was imported, it can be inserted into the appropriate place in the document using [CompositeNode.insertBefore(com.aspose.words.Node, com.aspose.words.Node)](../../com.aspose.words/compositenode\#insertBefore-com.aspose.words.Node--com.aspose.words.Node-) or [CompositeNode.insertAfter(com.aspose.words.Node, com.aspose.words.Node)](../../com.aspose.words/compositenode\#insertAfter-com.aspose.words.Node--com.aspose.words.Node-).

If the source node already belongs to the destination document, then simply a deep clone of the source node is created.

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| srcNode | [Node](../../com.aspose.words/node) | The node being imported. |
| isImportChildren | boolean | True to import all child nodes recursively; otherwise, false. |

**退货:**
[Node](../../com.aspose.words/node) - The cloned node that belongs to the current document.
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


退货 the index of the specified child node in the child node array. 退货 -1 if the node is not found in the child nodes.

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| child | [Node](../../com.aspose.words/node) |  |

**退货:**
int
### insertAfter(Node newChild, Node refChild) {#insertAfter-com.aspose.words.Node-com.aspose.words.Node-}
```
public Node insertAfter(Node newChild, Node refChild)
```


Inserts the specified node immediately after the specified reference node.

If refChild is null, inserts newChild at the beginning of the list of child nodes.

If the newChild is already in the tree, it is first removed.

If the node being inserted was created from another document, you should use **M:Aspose.Words.DocumentBase.ImportNode(Aspose.Words.Node,System.Boolean,Aspose.Words.ImportFormatMode)** to import the node to the current document. The imported node can then be inserted into the current document.

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| newChild | [Node](../../com.aspose.words/node) | The Node to insert. |
| refChild | [Node](../../com.aspose.words/node) | The Node that is the reference node. The newNode is placed after the refNode. |

**退货:**
[Node](../../com.aspose.words/node) - The inserted node.
### insertBefore(Node newChild, Node refChild) {#insertBefore-com.aspose.words.Node-com.aspose.words.Node-}
```
public Node insertBefore(Node newChild, Node refChild)
```


Inserts the specified node immediately before the specified reference node.

If refChild is null, inserts newChild at the end of the list of child nodes.

If the newChild is already in the tree, it is first removed.

If the node being inserted was created from another document, you should use **M:Aspose.Words.DocumentBase.ImportNode(Aspose.Words.Node,System.Boolean,Aspose.Words.ImportFormatMode)** to import the node to the current document. The imported node can then be inserted into the current document.

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| newChild | [Node](../../com.aspose.words/node) | The Node to insert. |
| refChild | [Node](../../com.aspose.words/node) | The Node that is the reference node. The newChild is placed before this node. |

**退货:**
[Node](../../com.aspose.words/node) - The inserted node.
### isComposite() {#isComposite--}
```
public boolean isComposite()
```


退货 true as this node can have child nodes.

**退货:**
boolean - True as this node can have child nodes.
### iterator() {#iterator--}
```
public Iterator iterator()
```


Provides support for the for each style iteration over the child nodes of this node.

**退货:**
java.util.Iterator
### joinRunsWithSameFormatting() {#joinRunsWithSameFormatting--}
```
public int joinRunsWithSameFormatting()
```


Joins runs with same formatting in all paragraphs of the document.

This is an optimization method. Some documents contain adjacent runs with same formatting. Usually this occurs if a document was intensively edited manually. You can reduce the document size and speed up further processing by joining these runs.

The operation checks every [Paragraph](../../com.aspose.words/paragraph) node in the document for adjacent [Run](../../com.aspose.words/run) nodes having identical properties. It ignores unique identifiers used to track editing sessions of run creation and modification. First run in every joining sequence accumulates all text. Remaining runs are deleted from the document.

**退货:**
int - Number of joins performed. When **N** adjacent runs are being joined they count as **N - 1** joins.
### nextPreOrder(Node rootNode) {#nextPreOrder-com.aspose.words.Node-}
```
public Node nextPreOrder(Node rootNode)
```


Gets next node according to the pre-order tree traversal algorithm.

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| rootNode | [Node](../../com.aspose.words/node) | The top node (limit) of traversal. |

**退货:**
[Node](../../com.aspose.words/node) - Next node in pre-order order. Null if reached the rootNode.
### node类型ToString(int node类型) {#node类型ToString-int-}
```
public static String node类型ToString(int node类型)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| node类型 | int |  |

**退货:**
java.lang.String
### normalize字段类型s() {#normalize字段类型s--}
```
public void normalize字段类型s()
```


Changes field type values [字段Char.get字段类型()](../../com.aspose.words/fieldchar\#get字段类型--) of [字段Start](../../com.aspose.words/fieldstart), [字段Separator](../../com.aspose.words/fieldseparator), [字段End](../../com.aspose.words/fieldend) in the whole document so that they correspond to the field types contained in the field codes.

Use this method after document changes that affect field types.

To change field type values in a specific part of the document use [Range.normalize字段类型s()](../../com.aspose.words/range\#normalize字段类型s--).

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


Adds the specified node to the beginning of the list of child nodes for this node.

If the newChild is already in the tree, it is first removed.

If the node being inserted was created from another document, you should use **M:Aspose.Words.DocumentBase.ImportNode(Aspose.Words.Node,System.Boolean,Aspose.Words.ImportFormatMode)** to import the node to the current document. The imported node can then be inserted into the current document.

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| newChild | [Node](../../com.aspose.words/node) | The node to add. |

**退货:**
[Node](../../com.aspose.words/node) - The node added.
### previousPreOrder(Node rootNode) {#previousPreOrder-com.aspose.words.Node-}
```
public Node previousPreOrder(Node rootNode)
```


Gets the previous node according to the pre-order tree traversal algorithm.

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| rootNode | [Node](../../com.aspose.words/node) | The top node (limit) of traversal. |

**退货:**
[Node](../../com.aspose.words/node) - Previous node in pre-order order. Null if reached the rootNode.
### print() {#print--}
```
public void print()
```


Prints the document without bringing up any user interface forms.  Prints the whole document to the default printer.

### print(String printerName) {#print-java.lang.String-}
```
public void print(String printerName)
```


Print the whole document to the specified printer, using the standard (no User 界面) print controller.

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| printerName | java.lang.String | The name of the printer. |

### print(AttributeSet printerSettings) {#print-javax.print.attribute.AttributeSet-}
```
public void print(AttributeSet printerSettings)
```


Prints the document according to the specified printer settings, using the standard (no User 界面) print controller.

The  object allows you to specify the printer to print on, the range of pages of to print and other options.

The  can contain both  to configure PrintJob request and  to configure PrintService lookup.

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| printerSettings | javax.print.attribute.AttributeSet | The printer settings to use. |

### print(AttributeSet printerSettings, String documentName) {#print-javax.print.attribute.AttributeSet-java.lang.String-}
```
public void print(AttributeSet printerSettings, String documentName)
```


Prints the document according to the specified printer settings, using the standard (no User 界面) print controller and a document name.

The  object allows you to specify the printer to print on, the range of pages of to print and other options.

The  can contain both  to configure PrintJob request and  to configure PrintService lookup.

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| printerSettings | javax.print.attribute.AttributeSet | The printer settings to use. |
| documentName | java.lang.String | The document name to display (for example, in a print status dialog box or printer queue) while printing the document. |

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


Removes itself from the parent.

### removeAllChildren() {#removeAllChildren--}
```
public void removeAllChildren()
```


Removes all the child nodes of the current node.

### removeChild(Node oldChild) {#removeChild-com.aspose.words.Node-}
```
public Node removeChild(Node oldChild)
```


Removes the specified child node.

The parent of oldChild is set to null after the node is removed.

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| oldChild | [Node](../../com.aspose.words/node) | The node to remove. |

**退货:**
[Node](../../com.aspose.words/node) - The removed node.
### removeExternalSchemaReferences() {#removeExternalSchemaReferences--}
```
public void removeExternalSchemaReferences()
```


Removes external XML schema references from this document.

### removeMacros() {#removeMacros--}
```
public void removeMacros()
```


Removes all macros (the VBA project) as well as toolbars and command customizations from the document.

By removing all macros from a document you can ensure the document contains no macro viruses.

### removeSmartTags() {#removeSmartTags--}
```
public void removeSmartTags()
```


Removes all [SmartTag](../../com.aspose.words/smarttag) descendant nodes of the current node. This method does not remove the content of the smart tags.

### renderToScale(int pageIndex, Graphics2D graphics, float x, float y, float scale) {#renderToScale-int-java.awt.Graphics2D-float-float-float-}
```
public Point2D.Float renderToScale(int pageIndex, Graphics2D graphics, float x, float y, float scale)
```


Renders a document page into a  object to a specified scale.

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| pageIndex | int | The 0-based page index. |
| graphics | java.awt.Graphics2D | The object where to render to. |
| x | float | The X coordinate (in world units) of the top left corner of the rendered page. |
| y | float | The Y coordinate (in world units) of the top left corner of the rendered page. |
| scale | float | The scale for rendering the page (1.0 is 100%). |

**退货:**
java.awt.geom.Point2D.Float - The width and height (in world units) of the rendered page.
### renderToSize(int pageIndex, Graphics2D graphics, float x, float y, float width, float height) {#renderToSize-int-java.awt.Graphics2D-float-float-float-float-}
```
public float renderToSize(int pageIndex, Graphics2D graphics, float x, float y, float width, float height)
```


Renders a document page into a  object to a specified size.

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| pageIndex | int | The 0-based page index. |
| graphics | java.awt.Graphics2D | The object where to render to. |
| x | float | The X coordinate (in world units) of the top left corner of the rendered page. |
| y | float | The Y coordinate (in world units) of the top left corner of the rendered page. |
| width | float | The maximum width (in world units) that can be occupied by the rendered page. |
| height | float | The maximum height (in world units) that can be occupied by the rendered page. |

**退货:**
float - The scale that was automatically calculated for the rendered page to fit the specified size.
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


Saves the document.  Saves the document to a file. Automatically determines the save format from the extension.

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| fileName | java.lang.String | The name for the document. If a document with the specified file name already exists, the existing document is overwritten. |

**退货:**
[SaveOutput参数](../../com.aspose.words/saveoutputparameters) - Additional information that you can optionally use.
### save(String fileName, SaveOptions saveOptions) {#save-java.lang.String-com.aspose.words.SaveOptions-}
```
public SaveOutput参数 save(String fileName, SaveOptions saveOptions)
```


Saves the document to a file using the specified save options.

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| fileName | java.lang.String | The name for the document. If a document with the specified file name already exists, the existing document is overwritten. |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions) | Specifies the options that control how the document is saved. Can be null. |

**退货:**
[SaveOutput参数](../../com.aspose.words/saveoutputparameters) - Additional information that you can optionally use.
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


Selects a list of nodes matching the XPath expression.

Only expressions with element names are supported at the moment. Expressions that use attribute names are not supported.

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| xpath | java.lang.String | The XPath expression. |

**退货:**
[NodeList](../../com.aspose.words/nodelist) - A list of nodes matching the XPath query.
### selectSingleNode(String xpath) {#selectSingleNode-java.lang.String-}
```
public Node selectSingleNode(String xpath)
```


Selects the first Node that matches the XPath expression.

Only expressions with element names are supported at the moment. Expressions that use attribute names are not supported.

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| xpath | java.lang.String | The XPath expression. |

**退货:**
[Node](../../com.aspose.words/node) - The first Node that matches the XPath query or null if no matching node is found.
### setAttachedTemplate(String value) {#setAttachedTemplate-java.lang.String-}
```
public void setAttachedTemplate(String value)
```


Sets the full path of the template attached to the document.

Empty string means the document is attached to the Normal template.

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | The full path of the template attached to the document. |

### setAutomaticallyUpdateStyles(boolean value) {#setAutomaticallyUpdateStyles-boolean-}
```
public void setAutomaticallyUpdateStyles(boolean value)
```


Sets a flag indicating whether the styles in the document are updated to match the styles in the attached template each time the document is opened in MS Word.

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | A flag indicating whether the styles in the document are updated to match the styles in the attached template each time the document is opened in MS Word. |

### setBackgroundShape(Shape value) {#setBackgroundShape-com.aspose.words.Shape-}
```
public void setBackgroundShape(Shape value)
```


Sets the background shape of the document. Can be null.

Microsoft Word allows only a shape that has its [ShapeBase.getShape类型()](../../com.aspose.words/shapebase\#getShape类型--) property equal to [Shape类型.RECTANGLE](../../com.aspose.words/shapetype\#RECTANGLE) to be used as a background shape for a document.

Microsoft Word supports only the fill properties of a background shape. All other properties are ignored.

Setting this property to a non-null value will also set the [ViewOptions.getDisplayBackgroundShape()](../../com.aspose.words/viewoptions\#getDisplayBackgroundShape--) / [ViewOptions.setDisplayBackgroundShape(boolean)](../../com.aspose.words/viewoptions\#setDisplayBackgroundShape-boolean-) to true.

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | [Shape](../../com.aspose.words/shape) | The background shape of the document. |

### setCustomNodeId(int value) {#setCustomNodeId-int-}
```
public void setCustomNodeId(int value)
```


Specifies custom node identifier.

Default is zero.

This identifier can be set and used arbitrarily. For example, as a key to get external data.

Important note, specified value is not saved to an output file and exists only during the node lifetime.

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | The corresponding  int  value. |

### setCustomXmlParts(CustomXmlPartCollection value) {#setCustomXmlParts-com.aspose.words.CustomXmlPartCollection-}
```
public void setCustomXmlParts(CustomXmlPartCollection value)
```


Sets the collection of Custom XML Data Storage Parts.

Aspose.Words loads and saves Custom XML Parts into OOXML and DOC documents only.

This property cannot be  null .

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | [CustomXmlPartCollection](../../com.aspose.words/customxmlpartcollection) | The collection of Custom XML Data Storage Parts. |

### setDefaultTabStop(double value) {#setDefaultTabStop-double-}
```
public void setDefaultTabStop(double value)
```


Sets the interval (in points) between the default tab stops.

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | double | The interval (in points) between the default tab stops. |

### setFontSettings(FontSettings value) {#setFontSettings-com.aspose.words.FontSettings-}
```
public void setFontSettings(FontSettings value)
```


Sets document font settings.

This property allows to specify font settings per document. If set to null, default static font settings [FontSettings.getDefaultInstance()](../../com.aspose.words/fontsettings\#getDefaultInstance--) will be used.

The default value is null.

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | [FontSettings](../../com.aspose.words/fontsettings) | Document font settings. |

### setGlossaryDocument(GlossaryDocument value) {#setGlossaryDocument-com.aspose.words.GlossaryDocument-}
```
public void setGlossaryDocument(GlossaryDocument value)
```


Sets the glossary document within this document or template. A glossary document is a storage for AutoText, AutoCorrect and Building Block entries defined in a document.

This property returns  null  if the document does not have a glossary document.

You can add a glossary document to a document by creating a [GlossaryDocument](../../com.aspose.words/glossarydocument) object and assigning to this property.

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | [GlossaryDocument](../../com.aspose.words/glossarydocument) | The glossary document within this document or template. |

### setGrammarChecked(boolean value) {#setGrammarChecked-boolean-}
```
public void setGrammarChecked(boolean value)
```


退货 **true** if the document has been checked for grammar. To recheck the grammar in the document, set this property to **false**.

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | **true** if the document has been checked for grammar. |

### setMailMergeSettings(MailMergeSettings value) {#setMailMergeSettings-com.aspose.words.MailMergeSettings-}
```
public void setMailMergeSettings(MailMergeSettings value)
```


Sets the object that contains all of the mail merge information for a document.

You can use this object to specify a mail merge data source for a document and this information (along with the available data fields) will appear in Microsoft Word when the user opens this document. Or you can use this object to query mail merge settings that the user has specified in Microsoft Word for this document.

This object is never null.

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | [MailMergeSettings](../../com.aspose.words/mailmergesettings) | The object that contains all of the mail merge information for a document. |

### setNodeChangingCallback(INodeChangingCallback value) {#setNodeChangingCallback-com.aspose.words.INodeChangingCallback-}
```
public void setNodeChangingCallback(INodeChangingCallback value)
```


Called when a node is inserted or removed in the document.

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | [INodeChangingCallback](../../com.aspose.words/inodechangingcallback) | The corresponding [INodeChangingCallback](../../com.aspose.words/inodechangingcallback) value. |

### set包裹CustomParts(CustomPartCollection value) {#set包裹CustomParts-com.aspose.words.CustomPartCollection-}
```
public void set包裹CustomParts(CustomPartCollection value)
```


Sets the collection of custom parts (arbitrary content) that are linked to the OOXML package using "unknown relationships".

Do not confuse these custom parts with Custom XML Data. If you need to access Custom XML parts, use the [getCustomXmlParts()](../../com.aspose.words/document\#getCustomXmlParts--) / [setCustomXmlParts(com.aspose.words.CustomXmlPartCollection)](../../com.aspose.words/document\#setCustomXmlParts-com.aspose.words.CustomXmlPartCollection-) property.

This collection contains OOXML parts whose parent is the OOXML package and they targets are of an "unknown relationship". For more information see [CustomPart](../../com.aspose.words/custompart).

Aspose.Words loads and saves custom parts into OOXML documents only.

This property cannot be  null .

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | [CustomPartCollection](../../com.aspose.words/custompartcollection) | The collection of custom parts (arbitrary content) that are linked to the OOXML package using "unknown relationships". |

### setPageColor(Color value) {#setPageColor-java.awt.Color-}
```
public void setPageColor(Color value)
```


Sets the page color of the document. This property is a simpler version of [getBackgroundShape()](../../com.aspose.words/documentbase\#getBackgroundShape--) / [setBackgroundShape(com.aspose.words.Shape)](../../com.aspose.words/documentbase\#setBackgroundShape-com.aspose.words.Shape-).

This property provides a simple way to specify a solid page color for the document. Setting this property creates and sets an appropriate [getBackgroundShape()](../../com.aspose.words/documentbase\#getBackgroundShape--) / [setBackgroundShape(com.aspose.words.Shape)](../../com.aspose.words/documentbase\#setBackgroundShape-com.aspose.words.Shape-).

If the page color is not set (e.g. there is no background shape in the document) returns a zero color.

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.awt.Color | The page color of the document. |

### setRemovePersonalInformation(boolean value) {#setRemovePersonalInformation-boolean-}
```
public void setRemovePersonalInformation(boolean value)
```


Sets a flag indicating that Microsoft Word will remove all user information from comments, revisions and document properties upon saving the document.

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | A flag indicating that Microsoft Word will remove all user information from comments, revisions and document properties upon saving the document. |

### setResourceLoadingCallback(IResourceLoadingCallback value) {#setResourceLoadingCallback-com.aspose.words.IResourceLoadingCallback-}
```
public void setResourceLoadingCallback(IResourceLoadingCallback value)
```


Allows to control how external resources are loaded.

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | [IResourceLoadingCallback](../../com.aspose.words/iresourceloadingcallback) | The corresponding [IResourceLoadingCallback](../../com.aspose.words/iresourceloadingcallback) value. |

### setRevisionsView(int value) {#setRevisionsView-int-}
```
public void setRevisionsView(int value)
```


Sets a value indicating whether to work with the original or revised version of a document. The default value is  **[RevisionsView.ORIGINAL](../../com.aspose.words/revisionsview\#ORIGINAL)** .

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | A value indicating whether to work with the original or revised version of a document. The value must be one of [RevisionsView](../../com.aspose.words/revisionsview) constants. |

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


Specifies whether to turn on the gray shading on form fields.

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setShowGrammaticalErrors(boolean value) {#setShowGrammaticalErrors-boolean-}
```
public void setShowGrammaticalErrors(boolean value)
```


Specifies whether to display grammar errors in this document.

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setShowSpellingErrors(boolean value) {#setShowSpellingErrors-boolean-}
```
public void setShowSpellingErrors(boolean value)
```


Specifies whether to display spelling errors in this document.

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setSpellingChecked(boolean value) {#setSpellingChecked-boolean-}
```
public void setSpellingChecked(boolean value)
```


退货 **true** if the document has been checked for spelling. To recheck the spelling in the document, set this property to **false**.

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | **true** if the document has been checked for spelling. |

### setTrackRevisions(boolean value) {#setTrackRevisions-boolean-}
```
public void setTrackRevisions(boolean value)
```


**True** if changes are tracked when this document is edited in Microsoft Word.

Setting this option only instructs Microsoft Word whether the track changes is turned on or off. This property has no effect on changes to the document that you make programmatically via Aspose.Words.

If you want to automatically track changes as they are made programmatically by Aspose.Words to this document use the [startTrackRevisions(java.lang.String, java.util.Date)](../../com.aspose.words/document\#startTrackRevisions-java.lang.String--java.util.Date-) method.

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setVbaProject(VbaProject value) {#setVbaProject-com.aspose.words.VbaProject-}
```
public void setVbaProject(VbaProject value)
```


Sets a [getVbaProject()](../../com.aspose.words/document\#getVbaProject--) / [setVbaProject(com.aspose.words.VbaProject)](../../com.aspose.words/document\#setVbaProject-com.aspose.words.VbaProject-).

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | [VbaProject](../../com.aspose.words/vbaproject) | A [getVbaProject()](../../com.aspose.words/document\#getVbaProject--) / [setVbaProject(com.aspose.words.VbaProject)](../../com.aspose.words/document\#setVbaProject-com.aspose.words.VbaProject-). |

### setWarningCallback(IWarningCallback value) {#setWarningCallback-com.aspose.words.IWarningCallback-}
```
public void setWarningCallback(IWarningCallback value)
```


Called during various document processing procedures when an issue is detected that might result in data or formatting fidelity loss. Document may generate warnings at any stage of its existence, so it's important to setup warning callback as early as possible to avoid the warnings loss. E.g. such properties as [Document.getPageCount()](../../com.aspose.words/document\#getPageCount--) actually build the document layout which is used later for rendering, and the layout warnings may be lost if warning callback is specified just for the rendering calls later.

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | [IWarningCallback](../../com.aspose.words/iwarningcallback) | The corresponding [IWarningCallback](../../com.aspose.words/iwarningcallback) value. |

### startTrackRevisions(String author) {#startTrackRevisions-java.lang.String-}
```
public void startTrackRevisions(String author)
```


Starts automatically marking all further changes you make to the document programmatically as revision changes.

If you call this method and then make some changes to the document programmatically, save the document and later open the document in MS Word you will see these changes as revisions.

Currently Aspose.Words supports tracking of node insertions and deletions only. Formatting changes are not recorded as revisions.

Automatic tracking of changes is supported both when modifying this document through node manipulations as well as when using [DocumentBuilder](../../com.aspose.words/documentbuilder)

This method does not change the [getTrackRevisions()](../../com.aspose.words/document\#getTrackRevisions--) / [setTrackRevisions(boolean)](../../com.aspose.words/document\#setTrackRevisions-boolean-) option and does not use its value for the purposes of revision tracking.

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| author | java.lang.String | Initials of the author to use for revisions. |

### startTrackRevisions(String author, Date dateTime) {#startTrackRevisions-java.lang.String-java.util.Date-}
```
public void startTrackRevisions(String author, Date dateTime)
```


Starts automatically marking all further changes you make to the document programmatically as revision changes.

If you call this method and then make some changes to the document programmatically, save the document and later open the document in MS Word you will see these changes as revisions.

Currently Aspose.Words supports tracking of node insertions and deletions only. Formatting changes are not recorded as revisions.

Automatic tracking of changes is supported both when modifying this document through node manipulations as well as when using [DocumentBuilder](../../com.aspose.words/documentbuilder)

This method does not change the [getTrackRevisions()](../../com.aspose.words/document\#getTrackRevisions--) / [setTrackRevisions(boolean)](../../com.aspose.words/document\#setTrackRevisions-boolean-) option and does not use its value for the purposes of revision tracking.

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| author | java.lang.String | Initials of the author to use for revisions. |
| dateTime | java.util.Date | The date and time to use for revisions. |

### stopTrackRevisions() {#stopTrackRevisions--}
```
public void stopTrackRevisions()
```


Stops automatic marking of document changes as revisions.

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


Exports the content of the node into a string using the specified save options.

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions) | Specifies the options that control how the node is saved. |

**退货:**
java.lang.String - The content of the node in the specified format.
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


Unlinks fields in the whole document.

Replaces all the fields in the whole document with their most recent results.

To unlink fields in a specific part of the document use [Range.unlink字段()](../../com.aspose.words/range\#unlink字段--).

### unprotect() {#unprotect--}
```
public void unprotect()
```


Removes protection from the document.  Removes protection from the document regardless of the password.

This method unprotects the document even if it has a protection password.

Note that document protection is different from write protection. Write protection is specified using the [getWriteProtection()](../../com.aspose.words/document\#getWriteProtection--).

### unprotect(String password) {#unprotect-java.lang.String-}
```
public boolean unprotect(String password)
```


Removes protection from the document if a correct password is specified.

This method unprotects the document only if a correct password is specified.

Note that document protection is different from write protection. Write protection is specified using the [getWriteProtection()](../../com.aspose.words/document\#getWriteProtection--).

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| password | java.lang.String | The password to unprotect the document with. |

**退货:**
boolean - True if a correct password was specified and the document was unprotected.
### update字段() {#update字段--}
```
public void update字段()
```


Updates the values of fields in the whole document.

When you open, modify and then save a document, Aspose.Words does not update fields automatically, it keeps them intact. Therefore, you would usually want to call this method before saving if you have modified the document programmatically and want to make sure the proper (calculated) field values appear in the saved document.

There is no need to update fields after executing a mail merge because mail merge is a kind of field update and automatically updates all fields in the document.

This method does not update all field types. For the detailed list of supported field types, see the Programmers Guide.

This method does not update fields that are related to the page layout algorithms (e.g. PAGE, PAGES, PAGEREF). The page layout-related fields are updated when you render a document or call [updatePageLayout()](../../com.aspose.words/document\#updatePageLayout--).

Use the [normalize字段类型s()](../../com.aspose.words/document\#normalize字段类型s--) method before fields updating if there were document changes that affected field types.

To update fields in a specific part of the document use [Range.update字段()](../../com.aspose.words/range\#update字段--).

### updateListLabels() {#updateListLabels--}
```
public void updateListLabels()
```


Updates list labels for all list items in the document.

This method updates list label properties such as [ListLabel.getLabelValue()](../../com.aspose.words/listlabel\#getLabelValue--) and [ListLabel.getLabelString()](../../com.aspose.words/listlabel\#getLabelString--) for each [Paragraph.getListLabel()](../../com.aspose.words/paragraph\#getListLabel--) object in the document.

Also, this method is sometimes implicitly called when updating fields in the document. This is required because some fields that may reference list numbers (such as TOC or REF) need them be up-to-date.

### updatePageLayout() {#updatePageLayout--}
```
public void updatePageLayout()
```


Rebuilds the page layout of the document.

This method formats a document into pages and updates the page number related fields in the document such as PAGE, PAGES, PAGEREF and REF. The up-to-date page layout information is required for a correct rendering of the document to fixed-page formats.

This method is automatically invoked when you first convert a document to PDF, XPS, image or print it. However, if you modify the document after rendering and then attempt to render it again - Aspose.Words will not update the page layout automatically. In this case you should call [updatePageLayout()](../../com.aspose.words/document\#updatePageLayout--) before rendering again.

### updateTableLayout() {#updateTableLayout--}
```
public void updateTableLayout()
```


Implements an earlier approach to table column widths re-calculation that has known issues. The method is deprecated and it will be removed in a few releases.

### updateThumbnail() {#updateThumbnail--}
```
public void updateThumbnail()
```


Updates [BuiltInDocumentProperties.getThumbnail()](../../com.aspose.words/builtindocumentproperties\#getThumbnail--) / [BuiltInDocumentProperties.setThumbnail(byte[])](../../com.aspose.words/builtindocumentproperties\#setThumbnail-byte---) of the document using default options.

### updateThumbnail(ThumbnailGeneratingOptions options) {#updateThumbnail-com.aspose.words.ThumbnailGeneratingOptions-}
```
public void updateThumbnail(ThumbnailGeneratingOptions options)
```


Updates [BuiltInDocumentProperties.getThumbnail()](../../com.aspose.words/builtindocumentproperties\#getThumbnail--) / [BuiltInDocumentProperties.setThumbnail(byte[])](../../com.aspose.words/builtindocumentproperties\#setThumbnail-byte---) of the document according to the specified options. The [ThumbnailGeneratingOptions](../../com.aspose.words/thumbnailgeneratingoptions) allows you to specify the source of thumbnail, size and other options. If attempt to generate thumbnail fails, doesn't change one.

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| options | [ThumbnailGeneratingOptions](../../com.aspose.words/thumbnailgeneratingoptions) | The generating options to use. |

### updateWordCount() {#updateWordCount--}
```
public void updateWordCount()
```


Updates word count properties of the document.

**UpdateWordCount** recalculates and updates Characters, Words and Paragraphs properties in the [getBuiltInDocumentProperties()](../../com.aspose.words/document\#getBuiltInDocumentProperties--) collection of the **Document**.

Note that **UpdateWordCount** does not update number of lines and pages properties. Use the [updateWordCount()](../../com.aspose.words/document\#updateWordCount--) overload and pass True value as a parameter to do that.

When you use an evaluation version, the evaluation watermark will also be included in the word count.

### updateWordCount(boolean updateLinesCount) {#updateWordCount-boolean-}
```
public void updateWordCount(boolean updateLinesCount)
```


Updates word count properties of the document, optionally updates [BuiltInDocumentProperties.getLines()](../../com.aspose.words/builtindocumentproperties\#getLines--) / [BuiltInDocumentProperties.setLines(int)](../../com.aspose.words/builtindocumentproperties\#setLines-int-) property. This method will rebuild page layout of the document.

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| updateLinesCount | boolean | True if number of lines in the document shall be calculated. |

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
