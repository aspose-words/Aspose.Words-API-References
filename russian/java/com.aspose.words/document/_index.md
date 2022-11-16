---
title: Document
second_title: Справочник по API Aspose.Words для Java
description: Представляет документ Word.
type: docs
weight: 120
url: /ru/java/com.aspose.words/document/
---

**Наследование:**
java.lang.Object, [com.aspose.words.Node](../../com.aspose.words/node), [com.aspose.words.CompositeNode](../../com.aspose.words/compositenode), [com.aspose.words.DocumentBase](../../com.aspose.words/documentbase)
```
public class Document extends DocumentBase
```

Представляет документ Word.

 Чтобы узнать больше, посетите**Working with Document** документальная статья.

**Document** является центральным объектом в библиотеке Aspose.Words.

 Чтобы загрузить существующий документ в любой из[LoadFormat](../../com.aspose.words/loadformat) форматы, передать имя файла или поток в один из**Document** конструкторы. Чтобы создать пустой документ, вызовите конструктор без параметров.

 Используйте одну из перегруженных версий метода Save, чтобы сохранить документ в любом из[SaveFormat](../../com.aspose.words/saveformat) форматы.

 Чтобы рисовать страницы документа непосредственно на**Graphics**использование объекта[renderToScale(int, java.awt.Graphics2D, float, float, float)](../../com.aspose.words/document\#renderToScale-int--java.awt.Graphics2D--float--float--float-) или же[renderToSize(int, java.awt.Graphics2D, float, float, float, float)](../../com.aspose.words/document\#renderToSize-int--java.awt.Graphics2D--float--float--float--float-) метод.

 Для печати документа используйте один из[print(java.lang.String)](../../com.aspose.words/document\#print-java.lang.String-) методы.

[getMailMerge()](../../com.aspose.words/document\#getMailMerge--) — это механизм отчетов Aspose.Words, который позволяет быстро и легко заполнять отчеты, разработанные в Microsoft Word, данными из различных источников данных. Данные могут быть из java.sql.ResultSet или массива значений.**MailMerge** будет просматривать записи, найденные в источнике данных, и вставлять их в поля слияния в документе, расширяя его по мере необходимости.

**Document** хранит информацию по всему документу, такую как[DocumentBase.getStyles()](../../com.aspose.words/documentbase\#getStyles--), [getBuiltInDocumentProperties()](../../com.aspose.words/document\#getBuiltInDocumentProperties--), [getCustomDocumentProperties()](../../com.aspose.words/document\#getCustomDocumentProperties--) , списки и макросы. Доступ к большинству этих объектов осуществляется через соответствующие свойства**Document**.

**Document** является корневым узлом дерева, содержащего все остальные узлы документа. Дерево — это составной шаблон проектирования, во многом похожий на XmlDocument. Содержимым документа можно свободно управлять программно:

 *   Доступ к узлам документа можно получить через типизированные коллекции, например[getSections()](../../com.aspose.words/document\#getSections--), [ParagraphCollection](../../com.aspose.words/paragraphcollection) и т.п.
 *   Узлы документа могут быть выбраны по их типу узла с помощью**M:Aspose.Words.CompositeNode.GetChildNodes(Aspose.Words.NodeType,System.Boolean)** или используя запрос XPath с[CompositeNode.selectNodes(java.lang.String)](../../com.aspose.words/compositenode\#selectNodes-java.lang.String-) или же[CompositeNode.selectSingleNode(java.lang.String)](../../com.aspose.words/compositenode\#selectSingleNode-java.lang.String-).
 *  Узлы содержимого могут быть добавлены или удалены из любого места документа с помощью[CompositeNode.insertBefore(com.aspose.words.Node, com.aspose.words.Node)](../../com.aspose.words/compositenode\#insertBefore-com.aspose.words.Node--com.aspose.words.Node-), [CompositeNode.insertAfter(com.aspose.words.Node, com.aspose.words.Node)](../../com.aspose.words/compositenode\#insertAfter-com.aspose.words.Node--com.aspose.words.Node-), [CompositeNode.removeChild(com.aspose.words.Node)](../../com.aspose.words/compositenode\#removeChild-com.aspose.words.Node-) и другие методы, предоставляемые базовым классом[CompositeNode](../../com.aspose.words/compositenode).
 *  Атрибуты форматирования каждого узла можно изменить с помощью свойств этого узла.

 Рассмотрите возможность использования[DocumentBuilder](../../com.aspose.words/documentbuilder) это упрощает задачу программного создания или заполнения дерева документов.

**Document** может содержать только[Section](../../com.aspose.words/section) объекты.

В Microsoft Word действительный документ должен иметь хотя бы один раздел.
## Конструкторы

| Конструктор | Описание |
| --- | --- |
| [Document()](#Document--) | Создает или загружает документ. |
| [Document(String fileName)](#Document-java.lang.String-) | Открывает существующий документ из файла. |
| [Document(String fileName, LoadOptions loadOptions)](#Document-java.lang.String-com.aspose.words.LoadOptions-) | Открывает существующий документ из файла. |
| [Document(InputStream stream)](#Document-java.io.InputStream-) | Инициализирует новый экземпляр этого класса. |
| [Document(InputStream stream, LoadOptions loadOptions)](#Document-java.io.InputStream-com.aspose.words.LoadOptions-) | Инициализирует новый экземпляр этого класса. |
## Методы

| Метод | Описание |
| --- | --- |
| [accept(DocumentVisitor visitor)](#accept-com.aspose.words.DocumentVisitor-) | Принимает посетителя. |
| [acceptAllRevisions()](#acceptAllRevisions--) | Принимает все отслеживаемые изменения в документе. |
| [add(Shape watermark)](#add-com.aspose.words.Shape-) |  |
| [appendChild(Node newChild)](#appendChild-com.aspose.words.Node-) | Добавляет указанный узел в конец списка дочерних узлов для этого узла. |
| [appendDocument(Document srcDoc, int importFormatMode)](#appendDocument-com.aspose.words.Document-int-) |  |
| [appendDocument(Document srcDoc, int importFormatMode, ImportFormatOptions importFormatOptions)](#appendDocument-com.aspose.words.Document-int-com.aspose.words.ImportFormatOptions-) |  |
| [cleanup()](#cleanup--) | Удаляет неиспользуемые стили и списки из документа. |
| [cleanup(CleanupOptions options)](#cleanup-com.aspose.words.CleanupOptions-) |  Удаляет из документа неиспользуемые стили и списки в зависимости от[CleanupOptions](../../com.aspose.words/cleanupoptions). |
| [clearSectionAttrs()](#clearSectionAttrs--) |  |
| [compare(Document document, String author, Date dateTime)](#compare-com.aspose.words.Document-java.lang.String-java.util.Date-) |  Сравнивает этот документ с другим документом, производящим изменения в виде количества редакций редактирования и форматирования.[Revision](../../com.aspose.words/revision). |
| [compare(Document document, String author, Date dateTime, CompareOptions options)](#compare-com.aspose.words.Document-java.lang.String-java.util.Date-com.aspose.words.CompareOptions-) |  Сравнивает этот документ с другим документом, производящим изменения в виде ряда редакций редактирования и форматирования.[Revision](../../com.aspose.words/revision). |
| [copyStylesFromTemplate(Document template)](#copyStylesFromTemplate-com.aspose.words.Document-) | Копирует стили из указанного шаблона в документ. |
| [copyStylesFromTemplate(String template)](#copyStylesFromTemplate-java.lang.String-) | Копирует стили из указанного шаблона в документ. |
| [dd()](#dd--) |  |
| [deepClone()](#deepClone--) |  Выполняет глубокую копию[Document](../../com.aspose.words/document). |
| [deepClone(boolean isCloneChildren)](#deepClone-boolean-) | Создает дубликат узла. |
| [ensureMinimum()](#ensureMinimum--) | Если документ не содержит разделов, создается один раздел с одним абзацем. |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [expandTableStylesToDirectFormatting()](#expandTableStylesToDirectFormatting--) | Преобразует форматирование, указанное в стилях таблиц, в прямое форматирование таблиц в документе. |
| [extractPages(int index, int count)](#extractPages-int-int-) |  Возвращает[Document](../../com.aspose.words/document) объект, представляющий указанный диапазон страниц. |
| [fetchInheritedSectionAttr(int key)](#fetchInheritedSectionAttr-int-) |  |
| [fetchSectionAttr(int key)](#fetchSectionAttr-int-) |  |
| [get()](#get--) |  |
| [getAncestor(int ancestorType)](#getAncestor-int-) |  |
| [getAncestor(Class ancestorType)](#getAncestor-java.lang.Class-) | Получает первого предка указанного типа объекта. |
| [getAttachedTemplate()](#getAttachedTemplate--) | Получает полный путь к шаблону, прикрепленному к документу. |
| [getAutomaticallyUpdateStyles()](#getAutomaticallyUpdateStyles--) | Получает флаг, указывающий, обновляются ли стили в документе в соответствии со стилями в прикрепленном шаблоне каждый раз, когда документ открывается в MS Word. |
| [getBackgroundShape()](#getBackgroundShape--) | Получает форму фона документа. |
| [getBuiltInDocumentProperties()](#getBuiltInDocumentProperties--) | Возвращает коллекцию, которая представляет все встроенные свойства документа. |
| [getChild(int nodeType, int index, boolean isDeep)](#getChild-int-int-boolean-) |  |
| [getChildNodes()](#getChildNodes--) | Получает все непосредственные дочерние узлы этого узла. |
| [getChildNodes(int nodeType, boolean isDeep)](#getChildNodes-int-boolean-) |  |
| [getClass()](#getClass--) |  |
| [getCompatibilityOptions()](#getCompatibilityOptions--) |  Предоставляет доступ к параметрам совместимости документов (то есть к настройкам пользователя, введенным в**Compatibility** вкладка**Options** диалоговое окно в Word). |
| [getCompliance()](#getCompliance--) | Получает версию соответствия OOXML, определенную из загруженного содержимого документа. |
| [getContainer()](#getContainer--) |  |
| [getCount()](#getCount--) | Получает количество непосредственных дочерних элементов этого узла. |
| [getCurrentNode()](#getCurrentNode--) |  |
| [getCustomDocumentProperties()](#getCustomDocumentProperties--) | Возвращает коллекцию, которая представляет все настраиваемые свойства документа. |
| [getCustomNodeId()](#getCustomNodeId--) | Задает идентификатор пользовательского узла. |
| [getCustomXmlParts()](#getCustomXmlParts--) | Получает коллекцию пользовательских частей хранилища данных XML. |
| [getDefaultTabStop()](#getDefaultTabStop--) | Получает интервал (в пунктах) между позициями табуляции по умолчанию. |
| [getDigitalSignatures()](#getDigitalSignatures--) | Получает коллекцию цифровых подписей для этого документа и результаты их проверки. |
| [getDirectSectionAttr(int key)](#getDirectSectionAttr-int-) |  |
| [getDocument()](#getDocument--) |  |
| [getEndnoteOptions()](#getEndnoteOptions--) | Предоставляет параметры, управляющие нумерацией и расположением концевых сносок в этом документе. |
| [getFieldOptions()](#getFieldOptions--) | Получает**FieldOptions** объект, представляющий параметры для управления обработкой полей в документе. |
| [getFirstChild()](#getFirstChild--) | Получает первый дочерний элемент узла. |
| [getFirstSection()](#getFirstSection--) | Получает первый раздел в документе. |
| [getFontInfos()](#getFontInfos--) | Предоставляет доступ к свойствам шрифтов, используемых в этом документе. |
| [getFontSettings()](#getFontSettings--) | Получает настройки шрифта документа. |
| [getFootnoteOptions()](#getFootnoteOptions--) | Предоставляет параметры, управляющие нумерацией и расположением сносок в этом документе. |
| [getFrameset()](#getFrameset--) |  Возвращает[getFrameset()](../../com.aspose.words/document\#getFrameset--) instance, если этот документ представляет страницу фреймов. |
| [getGlossaryDocument()](#getGlossaryDocument--) | Получает документ глоссария в этом документе или шаблоне. |
| [getGrammarChecked()](#getGrammarChecked--) |  Возвращает**true** если документ был проверен на грамматику. |
| [getHyphenationOptions()](#getHyphenationOptions--) | Предоставляет доступ к параметрам переноса документа. |
| [getLastChild()](#getLastChild--) | Получает последний дочерний элемент узла. |
| [getLastSection()](#getLastSection--) | Получает последний раздел в документе. |
| [getLayoutOptions()](#getLayoutOptions--) | Получает**LayoutOptions** объект, который представляет параметры для управления процессом компоновки этого документа. |
| [getLists()](#getLists--) | Предоставляет доступ к форматированию списка, используемому в документе. |
| [getMailMerge()](#getMailMerge--) |  Возвращает**MailMerge**объект, представляющий функциональность слияния для документа. |
| [getMailMergeSettings()](#getMailMergeSettings--) | Получает объект, содержащий всю информацию о слиянии для документа. |
| [getNextMatchingNode(Node curNode)](#getNextMatchingNode-com.aspose.words.Node-) |  |
| [getNextSibling()](#getNextSibling--) | Получает узел, следующий сразу за этим узлом. |
| [getNodeChangingCallback()](#getNodeChangingCallback--) | Вызывается при вставке или удалении узла в документе. |
| [getNodeType()](#getNodeType--) |  Возвращает**NodeType.Document**. |
| [getOriginalFileName()](#getOriginalFileName--) | Получает исходное имя файла документа. |
| [getOriginalLoadFormat()](#getOriginalLoadFormat--) | Получает формат исходного документа, который был загружен в этот объект. |
| [getPackageCustomParts()](#getPackageCustomParts--) | Получает набор настраиваемых частей (произвольное содержимое), которые связаны с пакетом OOXML с помощью «неизвестных связей». |
| [getPageColor()](#getPageColor--) | Получает цвет страницы документа. |
| [getPageCount()](#getPageCount--) | Получает количество страниц в документе, рассчитанное самой последней операцией макета страницы. |
| [getPageInfo(int pageIndex)](#getPageInfo-int-) | Получает размер страницы, ориентацию и другую информацию о странице, которая может быть полезна для печати или визуализации. |
| [getParentNode()](#getParentNode--) | Получает непосредственного родителя этого узла. |
| [getPreviousSibling()](#getPreviousSibling--) | Получает узел, непосредственно предшествующий этому узлу. |
| [getProtectionType()](#getProtectionType--) | Получает текущий активный тип защиты документа. |
| [getRange()](#getRange--) |  Возвращает**Range** объект, который представляет часть документа, содержащегося в этом узле. |
| [getRemovePersonalInformation()](#getRemovePersonalInformation--) | Получает флаг, указывающий, что Microsoft Word удалит всю информацию о пользователе из комментариев, редакций и свойств документа при сохранении документа. |
| [getResourceLoadingCallback()](#getResourceLoadingCallback--) | Позволяет контролировать загрузку внешних ресурсов. |
| [getRevisions()](#getRevisions--) | Получает коллекцию редакций (отслеживаемых изменений), существующих в этом документе. |
| [getRevisionsView()](#getRevisionsView--) | Получает значение, указывающее, следует ли работать с исходной или исправленной версией документа. |
| [getSections()](#getSections--) | Возвращает коллекцию, представляющую все разделы документа. |
| [getShadeFormData()](#getShadeFormData--) | Указывает, следует ли включать серое затенение полей формы. |
| [getShowGrammaticalErrors()](#getShowGrammaticalErrors--) | Указывает, отображать ли грамматические ошибки в этом документе. |
| [getShowSpellingErrors()](#getShowSpellingErrors--) | Указывает, отображать ли орфографические ошибки в этом документе. |
| [getSpellingChecked()](#getSpellingChecked--) |  Возвращает**true** если документ был проверен на орфографию. |
| [getStyles()](#getStyles--) | Возвращает набор стилей, определенных в документе. |
| [getText()](#getText--) | Получает текст этого узла и всех его дочерних элементов. |
| [getTheme()](#getTheme--) |  Получает[getTheme()](../../com.aspose.words/document\#getTheme--) объект для этого документа. |
| [getTrackRevisions()](#getTrackRevisions--) | **True** отслеживаются ли изменения при редактировании этого документа в Microsoft Word. |
| [getVariables()](#getVariables--) | Возвращает набор переменных, добавленных в документ или шаблон. |
| [getVbaProject()](#getVbaProject--) | Получает[getVbaProject()](../../com.aspose.words/document\#getVbaProject--) / [setVbaProject(com.aspose.words.VbaProject)](../../com.aspose.words/document\#setVbaProject-com.aspose.words.VbaProject-). |
| [getVersionsCount()](#getVersionsCount--) | Получает количество версий документа, сохраненных в документе DOC. |
| [getViewOptions()](#getViewOptions--) | Предоставляет параметры для управления отображением документа в Microsoft Word. |
| [getWarningCallback()](#getWarningCallback--) | Вызывается во время различных процедур обработки документов при обнаружении проблемы, которая может привести к потере точности данных или форматирования. |
| [getWatermark()](#getWatermark--) | Предоставляет доступ к водяному знаку документа. |
| [getWebExtensionTaskPanes()](#getWebExtensionTaskPanes--) | Возвращает коллекцию, представляющую список надстроек области задач. |
| [getWriteProtection()](#getWriteProtection--) | Предоставляет доступ к параметрам защиты документа от записи. |
| [hasChildNodes()](#hasChildNodes--) | Возвращает true, если у этого узла есть дочерние узлы. |
| [hasMacros()](#hasMacros--) |  Возвращает**true** если документ имеет проект VBA (макросы). |
| [hasRevisions()](#hasRevisions--) |  Возвращает**true** если документ имеет какие-либо отслеживаемые изменения. |
| [hashCode()](#hashCode--) |  |
| [importNode(Node srcNode, boolean isImportChildren)](#importNode-com.aspose.words.Node-boolean-) | Импортирует узел из другого документа в текущий документ. |
| [importNode(Node srcNode, boolean isImportChildren, int importFormatMode)](#importNode-com.aspose.words.Node-boolean-int-) |  |
| [indexOf(Node child)](#indexOf-com.aspose.words.Node-) | Возвращает индекс указанного дочернего узла в массиве дочерних узлов. |
| [insertAfter(Node newChild, Node refChild)](#insertAfter-com.aspose.words.Node-com.aspose.words.Node-) | Вставляет указанный узел сразу после указанного ссылочного узла. |
| [insertBefore(Node newChild, Node refChild)](#insertBefore-com.aspose.words.Node-com.aspose.words.Node-) | Вставляет указанный узел непосредственно перед указанным ссылочным узлом. |
| [isComposite()](#isComposite--) | Возвращает true, так как этот узел может иметь дочерние узлы. |
| [iterator()](#iterator--) | Обеспечивает поддержку для каждой итерации стиля над дочерними узлами этого узла. |
| [joinRunsWithSameFormatting()](#joinRunsWithSameFormatting--) | Соединения выполняются с одинаковым форматированием во всех абзацах документа. |
| [nextPreOrder(Node rootNode)](#nextPreOrder-com.aspose.words.Node-) | Получает следующий узел в соответствии с алгоритмом обхода дерева предварительного порядка. |
| [nodeTypeToString(int nodeType)](#nodeTypeToString-int-) |  |
| [normalizeFieldTypes()](#normalizeFieldTypes--) |  Изменяет значения типа поля[FieldChar.getFieldType()](../../com.aspose.words/fieldchar\#getFieldType--) из[FieldStart](../../com.aspose.words/fieldstart), [FieldSeparator](../../com.aspose.words/fieldseparator), [FieldEnd](../../com.aspose.words/fieldend) во всем документе, чтобы они соответствовали типам полей, содержащимся в кодах полей. |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [prependChild(Node newChild)](#prependChild-com.aspose.words.Node-) | Добавляет указанный узел в начало списка дочерних узлов для этого узла. |
| [previousPreOrder(Node rootNode)](#previousPreOrder-com.aspose.words.Node-) | Получает предыдущий узел в соответствии с алгоритмом обхода дерева предварительного порядка. |
| [print()](#print--) | Печатает документ без вызова каких-либо форм пользовательского интерфейса. |
| [print(String printerName)](#print-java.lang.String-) | Распечатайте весь документ на указанном принтере, используя стандартный (без пользовательского интерфейса) контроллер печати. |
| [print(AttributeSet printerSettings)](#print-javax.print.attribute.AttributeSet-) | Печать документа в соответствии с заданными параметрами принтера с использованием стандартного (без пользовательского интерфейса) контроллера печати. |
| [print(AttributeSet printerSettings, String documentName)](#print-javax.print.attribute.AttributeSet-java.lang.String-) | Печать документа в соответствии с указанными настройками принтера с использованием стандартного (без пользовательского интерфейса) контроллера печати и имени документа. |
| [protect(int type)](#protect-int-) |  |
| [protect(int type, String password)](#protect-int-java.lang.String-) |  |
| [remove()](#remove--) |  |
| [removeAllChildren()](#removeAllChildren--) | Удаляет все дочерние узлы текущего узла. |
| [removeChild(Node oldChild)](#removeChild-com.aspose.words.Node-) | Удаляет указанный дочерний узел. |
| [removeExternalSchemaReferences()](#removeExternalSchemaReferences--) | Удаляет ссылки на внешние XML-схемы из этого документа. |
| [removeMacros()](#removeMacros--) | Удаляет все макросы (проект VBA), а также панели инструментов и настройки команд из документа. |
| [removeSmartTags()](#removeSmartTags--) |  Удаляет все[SmartTag](../../com.aspose.words/smarttag) узлы-потомки текущего узла. |
| [renderToScale(int pageIndex, Graphics2D graphics, float x, float y, float scale)](#renderToScale-int-java.awt.Graphics2D-float-float-float-) | Преобразует страницу документа в объект в указанном масштабе. |
| [renderToSize(int pageIndex, Graphics2D graphics, float x, float y, float width, float height)](#renderToSize-int-java.awt.Graphics2D-float-float-float-float-) | Преобразует страницу документа в объект заданного размера. |
| [save(OutputStream stream, SaveOptions saveOptions)](#save-java.io.OutputStream-com.aspose.words.SaveOptions-) |  |
| [save(OutputStream stream, int saveFormat)](#save-java.io.OutputStream-int-) |  |
| [save(String fileName)](#save-java.lang.String-) | Сохраняет документ. |
| [save(String fileName, SaveOptions saveOptions)](#save-java.lang.String-com.aspose.words.SaveOptions-) | Сохраняет документ в файл, используя указанные параметры сохранения. |
| [save(String fileName, int saveFormat)](#save-java.lang.String-int-) |  |
| [selectNodes(String xpath)](#selectNodes-java.lang.String-) | Выбирает список узлов, соответствующих выражению XPath. |
| [selectSingleNode(String xpath)](#selectSingleNode-java.lang.String-) | Выбирает первый узел, соответствующий выражению XPath. |
| [setAttachedTemplate(String value)](#setAttachedTemplate-java.lang.String-) | Задает полный путь к шаблону, прикрепленному к документу. |
| [setAutomaticallyUpdateStyles(boolean value)](#setAutomaticallyUpdateStyles-boolean-) | Устанавливает флаг, указывающий, обновляются ли стили в документе в соответствии со стилями в прикрепленном шаблоне каждый раз, когда документ открывается в MS Word. |
| [setBackgroundShape(Shape value)](#setBackgroundShape-com.aspose.words.Shape-) | Устанавливает форму фона документа. |
| [setCustomNodeId(int value)](#setCustomNodeId-int-) | Задает идентификатор пользовательского узла. |
| [setCustomXmlParts(CustomXmlPartCollection value)](#setCustomXmlParts-com.aspose.words.CustomXmlPartCollection-) | Задает коллекцию пользовательских частей хранилища данных XML. |
| [setDefaultTabStop(double value)](#setDefaultTabStop-double-) | Устанавливает интервал (в пунктах) между позициями табуляции по умолчанию. |
| [setFontSettings(FontSettings value)](#setFontSettings-com.aspose.words.FontSettings-) | Задает настройки шрифта документа. |
| [setGlossaryDocument(GlossaryDocument value)](#setGlossaryDocument-com.aspose.words.GlossaryDocument-) | Задает глоссарий в этом документе или шаблоне. |
| [setGrammarChecked(boolean value)](#setGrammarChecked-boolean-) |  Возвращает**true** если документ был проверен на грамматику. |
| [setMailMergeSettings(MailMergeSettings value)](#setMailMergeSettings-com.aspose.words.MailMergeSettings-) | Задает объект, содержащий всю информацию о слиянии для документа. |
| [setNodeChangingCallback(INodeChangingCallback value)](#setNodeChangingCallback-com.aspose.words.INodeChangingCallback-) | Вызывается при вставке или удалении узла в документе. |
| [setPackageCustomParts(CustomPartCollection value)](#setPackageCustomParts-com.aspose.words.CustomPartCollection-) | Задает набор настраиваемых частей (произвольное содержимое), которые связаны с пакетом OOXML с помощью «неизвестных связей». |
| [setPageColor(Color value)](#setPageColor-java.awt.Color-) | Устанавливает цвет страницы документа. |
| [setRemovePersonalInformation(boolean value)](#setRemovePersonalInformation-boolean-) | Устанавливает флаг, указывающий, что Microsoft Word удалит всю информацию о пользователе из комментариев, редакций и свойств документа при сохранении документа. |
| [setResourceLoadingCallback(IResourceLoadingCallback value)](#setResourceLoadingCallback-com.aspose.words.IResourceLoadingCallback-) | Позволяет контролировать загрузку внешних ресурсов. |
| [setRevisionsView(int value)](#setRevisionsView-int-) | Задает значение, указывающее, следует ли работать с исходной или исправленной версией документа. |
| [setSectionAttr(int key, Object value)](#setSectionAttr-int-java.lang.Object-) |  |
| [setShadeFormData(boolean value)](#setShadeFormData-boolean-) | Указывает, следует ли включать серое затенение полей формы. |
| [setShowGrammaticalErrors(boolean value)](#setShowGrammaticalErrors-boolean-) | Указывает, отображать ли грамматические ошибки в этом документе. |
| [setShowSpellingErrors(boolean value)](#setShowSpellingErrors-boolean-) | Указывает, отображать ли орфографические ошибки в этом документе. |
| [setSpellingChecked(boolean value)](#setSpellingChecked-boolean-) |  Возвращает**true** если документ был проверен на орфографию. |
| [setTrackRevisions(boolean value)](#setTrackRevisions-boolean-) | **True** отслеживаются ли изменения при редактировании этого документа в Microsoft Word. |
| [setVbaProject(VbaProject value)](#setVbaProject-com.aspose.words.VbaProject-) |  Устанавливает[getVbaProject()](../../com.aspose.words/document\#getVbaProject--) / [setVbaProject(com.aspose.words.VbaProject)](../../com.aspose.words/document\#setVbaProject-com.aspose.words.VbaProject-). |
| [setWarningCallback(IWarningCallback value)](#setWarningCallback-com.aspose.words.IWarningCallback-) | Вызывается во время различных процедур обработки документов при обнаружении проблемы, которая может привести к потере точности данных или форматирования. |
| [startTrackRevisions(String author)](#startTrackRevisions-java.lang.String-) | Начинает автоматически отмечать все дальнейшие изменения, которые вы вносите в документ программно, как изменения версии. |
| [startTrackRevisions(String author, Date dateTime)](#startTrackRevisions-java.lang.String-java.util.Date-) | Начинает автоматически отмечать все дальнейшие изменения, которые вы вносите в документ программно, как изменения версии. |
| [stopTrackRevisions()](#stopTrackRevisions--) | Останавливает автоматическую маркировку изменений документа как редакций. |
| [toString()](#toString--) |  |
| [toString(SaveOptions saveOptions)](#toString-com.aspose.words.SaveOptions-) | Экспортирует содержимое узла в строку, используя указанные параметры сохранения. |
| [toString(int saveFormat)](#toString-int-) |  |
| [unlinkFields()](#unlinkFields--) | Разъединяет поля во всем документе. |
| [unprotect()](#unprotect--) | Снимает защиту с документа. |
| [unprotect(String password)](#unprotect-java.lang.String-) | Снимает защиту с документа, если указан правильный пароль. |
| [updateFields()](#updateFields--) | Обновляет значения полей во всем документе. |
| [updateListLabels()](#updateListLabels--) | Обновляет метки списка для всех элементов списка в документе. |
| [updatePageLayout()](#updatePageLayout--) | Восстанавливает макет страницы документа. |
| [updateTableLayout()](#updateTableLayout--) | Реализует более ранний подход к пересчету ширины столбцов таблицы, который имеет известные проблемы. |
| [updateThumbnail()](#updateThumbnail--) |  Обновления[BuiltInDocumentProperties.getThumbnail()](../../com.aspose.words/builtindocumentproperties\#getThumbnail--) / [BuiltInDocumentProperties.setThumbnail(byte[])](../../com.aspose.words/builtindocumentproperties\#setThumbnail-byte---) документа с использованием параметров по умолчанию. |
| [updateThumbnail(ThumbnailGeneratingOptions options)](#updateThumbnail-com.aspose.words.ThumbnailGeneratingOptions-) |  Обновления[BuiltInDocumentProperties.getThumbnail()](../../com.aspose.words/builtindocumentproperties\#getThumbnail--) / [BuiltInDocumentProperties.setThumbnail(byte[])](../../com.aspose.words/builtindocumentproperties\#setThumbnail-byte---) документа в соответствии с указанными параметрами. |
| [updateWordCount()](#updateWordCount--) | Обновляет свойства количества слов в документе. |
| [updateWordCount(boolean updateLinesCount)](#updateWordCount-boolean-) |  Обновляет свойства количества слов в документе, опционально обновляет[BuiltInDocumentProperties.getLines()](../../com.aspose.words/builtindocumentproperties\#getLines--) / [BuiltInDocumentProperties.setLines(int)](../../com.aspose.words/builtindocumentproperties\#setLines-int-) имущество. |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### Document() {#Document--}
```
public Document()
```


Создает или загружает документ. Создает пустой документ Word.

 Размер бумаги документа по умолчанию — Letter. Если вы хотите изменить настройки страницы, используйте[Section.getPageSetup()](../../com.aspose.words/section\#getPageSetup--).

 После создания вы можете использовать[DocumentBuilder](../../com.aspose.words/documentbuilder) легко добавлять содержимое документа.

### Document(String fileName) {#Document-java.lang.String-}
```
public Document(String fileName)
```


Открывает существующий документ из файла. Автоматически определяет формат файла.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| fileName | java.lang.String | Имя файла открываемого документа. |

### Document(String fileName, LoadOptions loadOptions) {#Document-java.lang.String-com.aspose.words.LoadOptions-}
```
public Document(String fileName, LoadOptions loadOptions)
```


Открывает существующий документ из файла. Позволяет указать дополнительные параметры, такие как пароль шифрования.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| fileName | java.lang.String | Имя файла открываемого документа. |
| loadOptions | [LoadOptions](../../com.aspose.words/loadoptions) | Дополнительные параметры для использования при загрузке документа. Может быть нулевым. |

### Document(InputStream stream) {#Document-java.io.InputStream-}
```
public Document(InputStream stream)
```


Инициализирует новый экземпляр этого класса.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| stream | java.io.InputStream |  |

### Document(InputStream stream, LoadOptions loadOptions) {#Document-java.io.InputStream-com.aspose.words.LoadOptions-}
```
public Document(InputStream stream, LoadOptions loadOptions)
```


Инициализирует новый экземпляр этого класса.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| stream | java.io.InputStream |  |
| loadOptions | [LoadOptions](../../com.aspose.words/loadoptions) |  |

### accept(DocumentVisitor visitor) {#accept-com.aspose.words.DocumentVisitor-}
```
public boolean accept(DocumentVisitor visitor)
```


Принимает посетителя.

Перечисляет этот узел и все его дочерние элементы. Каждый узел вызывает соответствующий метод в DocumentVisitor.

Дополнительные сведения см. в шаблоне проектирования «Посетитель».

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| visitor | [DocumentVisitor](../../com.aspose.words/documentvisitor) | Посетитель, который будет посещать узлы. |

**Возвращает:**
boolean - Истинно, если были посещены все узлы; false, если DocumentVisitor остановил операцию перед посещением всех узлов. Вызывает DocumentVisitor.VisitDocumentStart, затем вызывает Accept для всех дочерних узлов документа и в конце вызывает DocumentVisitor.VisitDocumentEnd.
### acceptAllRevisions() {#acceptAllRevisions--}
```
public void acceptAllRevisions()
```


 Принимает все отслеживаемые изменения в документе. Этот метод является кратчайшим путем[RevisionCollection.acceptAll()](../../com.aspose.words/revisioncollection\#acceptAll--).

### add(Shape watermark) {#add-com.aspose.words.Shape-}
```
public void add(Shape watermark)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| watermark | [Shape](../../com.aspose.words/shape) |  |

### appendChild(Node newChild) {#appendChild-com.aspose.words.Node-}
```
public Node appendChild(Node newChild)
```


Добавляет указанный узел в конец списка дочерних узлов для этого узла.

Если новый дочерний элемент уже находится в дереве, он сначала удаляется.

 Если вставляемый узел был создан из другого документа, следует использовать**M:Aspose.Words.DocumentBase.ImportNode(Aspose.Words.Node,System.Boolean,Aspose.Words.ImportFormatMode)** чтобы импортировать узел в текущий документ. Затем импортированный узел можно вставить в текущий документ.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| newChild | [Node](../../com.aspose.words/node) | Добавляемый узел. |

**Возвращает:**
[Node](../../com.aspose.words/node) - Добавлен узел.
### appendDocument(Document srcDoc, int importFormatMode) {#appendDocument-com.aspose.words.Document-int-}
```
public void appendDocument(Document srcDoc, int importFormatMode)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| srcDoc | [Document](../../com.aspose.words/document) |  |
| importFormatMode | int |  |

### appendDocument(Document srcDoc, int importFormatMode, ImportFormatOptions importFormatOptions) {#appendDocument-com.aspose.words.Document-int-com.aspose.words.ImportFormatOptions-}
```
public void appendDocument(Document srcDoc, int importFormatMode, ImportFormatOptions importFormatOptions)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| srcDoc | [Document](../../com.aspose.words/document) |  |
| importFormatMode | int |  |
| importFormatOptions | [ImportFormatOptions](../../com.aspose.words/importformatoptions) |  |

### cleanup() {#cleanup--}
```
public void cleanup()
```


Удаляет неиспользуемые стили и списки из документа.

### cleanup(CleanupOptions options) {#cleanup-com.aspose.words.CleanupOptions-}
```
public void cleanup(CleanupOptions options)
```


 Удаляет из документа неиспользуемые стили и списки в зависимости от[CleanupOptions](../../com.aspose.words/cleanupoptions).

**Параметры:**

| Параметр | Тип | Описание |
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


 Сравнивает этот документ с другим документом, производящим изменения в виде количества редакций редактирования и форматирования.[Revision](../../com.aspose.words/revision).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| document | [Document](../../com.aspose.words/document) | Документ для сравнения. |
| author | java.lang.String | Инициалы автора использовать для редакций. |
| dateTime | java.util.Date | Дата и время для использования для изменений. На данный момент не сравниваются следующие узлы документа:

 *  [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag)
 *  Пункт 3

 Документы не должны иметь редакций перед сравнением.|

### compare(Document document, String author, Date dateTime, CompareOptions options) {#compare-com.aspose.words.Document-java.lang.String-java.util.Date-com.aspose.words.CompareOptions-}
```
public void compare(Document document, String author, Date dateTime, CompareOptions options)
```


 Сравнивает этот документ с другим документом, производящим изменения в виде ряда редакций редактирования и форматирования.[Revision](../../com.aspose.words/revision) . Позволяет указать параметры сравнения с помощью[CompareOptions](../../com.aspose.words/compareoptions).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| document | [Document](../../com.aspose.words/document) |  |
| author | java.lang.String |  |
| dateTime | java.util.Date |  |
| options | [CompareOptions](../../com.aspose.words/compareoptions) |  |

### copyStylesFromTemplate(Document template) {#copyStylesFromTemplate-com.aspose.words.Document-}
```
public void copyStylesFromTemplate(Document template)
```


Копирует стили из указанного шаблона в документ. Когда стили копируются из шаблона в документ, стили с одинаковыми именами в документе переопределяются, чтобы соответствовать описаниям стилей в шаблоне. Уникальные стили из шаблона копируются в документ. Уникальные стили в документе остаются неизменными.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| template | [Document](../../com.aspose.words/document) |  |

### copyStylesFromTemplate(String template) {#copyStylesFromTemplate-java.lang.String-}
```
public void copyStylesFromTemplate(String template)
```


Копирует стили из указанного шаблона в документ. Когда стили копируются из шаблона в документ, стили с одинаковыми именами в документе переопределяются, чтобы соответствовать описаниям стилей в шаблоне. Уникальные стили из шаблона копируются в документ. Уникальные стили в документе остаются неизменными.

**Параметры:**

| Параметр | Тип | Описание |
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


 Выполняет глубокую копию[Document](../../com.aspose.words/document).

**Возвращает:**
[Document](../../com.aspose.words/document) - Клонированный документ.
### deepClone(boolean isCloneChildren) {#deepClone-boolean-}
```
public Node deepClone(boolean isCloneChildren)
```


Создает дубликат узла.

Этот метод служит конструктором копирования для узлов. Клонированный узел не имеет родителя, но принадлежит к тому же документу, что и исходный узел.

 Этот метод всегда выполняет глубокую копию узла.*isCloneChildren* Параметр указывает, следует ли также выполнять копирование всех дочерних узлов.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| isCloneChildren | boolean | Значение true, чтобы рекурсивно клонировать поддерево в указанном узле; false, чтобы клонировать только сам узел. |

**Возвращает:**
[Node](../../com.aspose.words/node) - Клонированный узел.
### ensureMinimum() {#ensureMinimum--}
```
public void ensureMinimum()
```


Если документ не содержит разделов, создается один раздел с одним абзацем.

### equals(Object arg0) {#equals-java.lang.Object-}
```
public boolean equals(Object arg0)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**Возвращает:**
логический
### expandTableStylesToDirectFormatting() {#expandTableStylesToDirectFormatting--}
```
public void expandTableStylesToDirectFormatting()
```


Преобразует форматирование, указанное в стилях таблиц, в прямое форматирование таблиц в документе.

Этот метод существует, потому что эта версия Aspose.Words обеспечивает лишь ограниченную поддержку стилей таблиц (см. ниже). Этот метод может быть полезен, когда вы загружаете документ DOCX или WordprocessingML, содержащий таблицы, отформатированные с помощью стилей таблиц, и вам нужно запросить форматирование таблиц, ячеек, абзацев или текста.

Эта версия Aspose.Words обеспечивает ограниченную поддержку следующих стилей таблиц:

 *  Стили таблиц, определенные в документах DOCX или WordprocessingML, сохраняются как стили таблиц при сохранении документа в формате DOCX или WordprocessingML.
 *  Стили таблиц, определенные в документах DOCX или WordprocessingML, автоматически преобразуются в прямое форматирование таблиц при сохранении документа в любом другом формате, визуализации или печати.
 *  Стили таблиц, определенные в документах DOC, сохраняются как стили таблиц при сохранении документа только как DOC.

### extractPages(int index, int count) {#extractPages-int-int-}
```
public Document extractPages(int index, int count)
```


 Возвращает[Document](../../com.aspose.words/document)объект, представляющий указанный диапазон страниц. Полученный документ должен выглядеть так же, как в MS Word, как если бы мы выполнили «Печать определенных страниц».\\u2013 нумерация, верхние/нижние колонтитулы и компоновка перекрестных таблиц будут сохранены. Но из-за большого количества нюансов, возникающих при уменьшении количества страниц, полное соответствие верстки представляет собой довольно сложную задачу, требующую больших усилий. В зависимости от сложности документа могут быть небольшие отличия в итоговом макете содержимого документа по сравнению с исходным документом. Любая обратная связь будет принята с благодарностью.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| index | int | Отсчитываемый от нуля индекс первой извлекаемой страницы. |
| count | int | Количество страниц, которые необходимо извлечь. |

**Возвращает:**
[Document](../../com.aspose.words/document)
### fetchInheritedSectionAttr(int key) {#fetchInheritedSectionAttr-int-}
```
public Object fetchInheritedSectionAttr(int key)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| key | int |  |

**Возвращает:**
java.lang.Объект
### fetchSectionAttr(int key) {#fetchSectionAttr-int-}
```
public Object fetchSectionAttr(int key)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| key | int |  |

**Возвращает:**
java.lang.Объект
### get() {#get--}
```
public Shape get()
```




**Возвращает:**
[Shape](../../com.aspose.words/shape)
### getAncestor(int ancestorType) {#getAncestor-int-}
```
public CompositeNode getAncestor(int ancestorType)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| ancestorType | int |  |

**Возвращает:**
[CompositeNode](../../com.aspose.words/compositenode)
### getAncestor(Class ancestorType) {#getAncestor-java.lang.Class-}
```
public CompositeNode getAncestor(Class ancestorType)
```


Получает первого предка указанного типа объекта.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| ancestorType | java.lang.Class | Тип объекта-предка для извлечения. |

**Возвращает:**
[CompositeNode](../../com.aspose.words/compositenode) - предок указанного типа или ноль, если предок этого типа не найден.

Тип предка совпадает, если он равен ancestorType или является производным от ancestorType.
### getAttachedTemplate() {#getAttachedTemplate--}
```
public String getAttachedTemplate()
```


Получает полный путь к шаблону, прикрепленному к документу.

Пустая строка означает, что документ прикреплен к шаблону Normal.

**Возвращает:**
java.lang.String — Полный путь к шаблону, прикрепленному к документу.
### getAutomaticallyUpdateStyles() {#getAutomaticallyUpdateStyles--}
```
public boolean getAutomaticallyUpdateStyles()
```


Получает флаг, указывающий, обновляются ли стили в документе в соответствии со стилями в прикрепленном шаблоне каждый раз, когда документ открывается в MS Word.

**Возвращает:**
boolean — флаг, указывающий, обновляются ли стили в документе в соответствии со стилями в прикрепленном шаблоне каждый раз, когда документ открывается в MS Word.
### getBackgroundShape() {#getBackgroundShape--}
```
public Shape getBackgroundShape()
```


Получает форму фона документа. Может быть нулевым.

Microsoft Word допускает только ту форму, которая имеет свою[ShapeBase.getShapeType()](../../com.aspose.words/shapebase\#getShapeType--) свойство, равное[ShapeType.RECTANGLE](../../com.aspose.words/shapetype\#RECTANGLE) для использования в качестве фоновой формы для документа.

Microsoft Word поддерживает только свойства заливки фоновой фигуры. Все остальные свойства игнорируются.

 Установка для этого свойства ненулевого значения также установит[ViewOptions.getDisplayBackgroundShape()](../../com.aspose.words/viewoptions\#getDisplayBackgroundShape--) / [ViewOptions.setDisplayBackgroundShape(boolean)](../../com.aspose.words/viewoptions\#setDisplayBackgroundShape-boolean-) к истине.

**Возвращает:**
[Shape](../../com.aspose.words/shape) - Форма фона документа.
### getBuiltInDocumentProperties() {#getBuiltInDocumentProperties--}
```
public BuiltInDocumentProperties getBuiltInDocumentProperties()
```


Возвращает коллекцию, которая представляет все встроенные свойства документа.

**Возвращает:**
[BuiltInDocumentProperties](../../com.aspose.words/builtindocumentproperties) - Коллекция, представляющая все встроенные свойства документа.
### getChild(int nodeType, int index, boolean isDeep) {#getChild-int-int-boolean-}
```
public Node getChild(int nodeType, int index, boolean isDeep)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| nodeType | int |  |
| index | int |  |
| isDeep | boolean |  |

**Возвращает:**
[Node](../../com.aspose.words/node)
### getChildNodes() {#getChildNodes--}
```
public NodeCollection getChildNodes()
```


Получает все непосредственные дочерние узлы этого узла.

 Примечание,[getChildNodes()](../../com.aspose.words/compositenode\#getChildNodes--) эквивалентно вызову GetChildNodes(NodeType.Any, false) и создает и возвращает новую коллекцию при каждом доступе к ней.

Если дочерних узлов нет, это свойство возвращает пустую коллекцию.

**Возвращает:**
[NodeCollection](../../com.aspose.words/nodecollection) - Все непосредственные дочерние узлы этого узла.
### getChildNodes(int nodeType, boolean isDeep) {#getChildNodes-int-boolean-}
```
public NodeCollection getChildNodes(int nodeType, boolean isDeep)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| nodeType | int |  |
| isDeep | boolean |  |

**Возвращает:**
[NodeCollection](../../com.aspose.words/nodecollection)
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getCompatibilityOptions() {#getCompatibilityOptions--}
```
public CompatibilityOptions getCompatibilityOptions()
```


 Предоставляет доступ к параметрам совместимости документов (то есть к настройкам пользователя, введенным в**Compatibility** вкладка**Options** диалоговое окно в Word).

**Возвращает:**
[CompatibilityOptions](../../com.aspose.words/compatibilityoptions) - соответствующий[CompatibilityOptions](../../com.aspose.words/compatibilityoptions) ценность.
### getCompliance() {#getCompliance--}
```
public int getCompliance()
```


Получает версию соответствия OOXML, определенную из загруженного содержимого документа. Имеет смысл только для документов OOXML.

 Если вы создали новый пустой документ или загрузили документ, отличный от OOXML,[OoxmlCompliance.ECMA\_376\_2006](../../com.aspose.words/ooxmlcompliance\#ECMA-376-2006) ценность.

**Возвращает:**
 int — версия соответствия OOXML, определенная из загруженного содержимого документа. Возвращаемое значение является одним из[OoxmlCompliance](../../com.aspose.words/ooxmlcompliance) константы.
### getContainer() {#getContainer--}
```
public CompositeNode getContainer()
```




**Возвращает:**
[CompositeNode](../../com.aspose.words/compositenode)
### getCount() {#getCount--}
```
public int getCount()
```


Получает количество непосредственных дочерних элементов этого узла.

**Возвращает:**
int - количество непосредственных дочерних элементов этого узла.
### getCurrentNode() {#getCurrentNode--}
```
public Node getCurrentNode()
```




**Возвращает:**
[Node](../../com.aspose.words/node)
### getCustomDocumentProperties() {#getCustomDocumentProperties--}
```
public CustomDocumentProperties getCustomDocumentProperties()
```


Возвращает коллекцию, которая представляет все настраиваемые свойства документа.

**Возвращает:**
[CustomDocumentProperties](../../com.aspose.words/customdocumentproperties) - Коллекция, представляющая все настраиваемые свойства документа.
### getCustomNodeId() {#getCustomNodeId--}
```
public int getCustomNodeId()
```


Задает идентификатор пользовательского узла.

По умолчанию ноль.

Этот идентификатор можно установить и использовать произвольно. Например, как ключ для получения внешних данных.

Важное примечание: указанное значение не сохраняется в выходной файл и существует только в течение срока службы узла.

**Возвращает:**
int - соответствующее значение int.
### getCustomXmlParts() {#getCustomXmlParts--}
```
public CustomXmlPartCollection getCustomXmlParts()
```


Получает коллекцию пользовательских частей хранилища данных XML.

Aspose.Words загружает и сохраняет пользовательские XML-части только в документах OOXML и DOC.

Это свойство не может быть нулевым.

**Возвращает:**
[CustomXmlPartCollection](../../com.aspose.words/customxmlpartcollection) Коллекция пользовательских частей хранилища данных XML.
### getDefaultTabStop() {#getDefaultTabStop--}
```
public double getDefaultTabStop()
```


Получает интервал (в пунктах) между позициями табуляции по умолчанию.

**Возвращает:**
double — интервал (в пунктах) между позициями табуляции по умолчанию.
### getDigitalSignatures() {#getDigitalSignatures--}
```
public DigitalSignatureCollection getDigitalSignatures()
```


Получает коллекцию цифровых подписей для этого документа и результаты их проверки.

 Эта коллекция содержит цифровые подписи, загруженные из исходного документа. Эти цифровые подписи не будут сохранены, когда вы сохраните это[Document](../../com.aspose.words/document) объект в файл или поток, потому что при сохранении или преобразовании будет создан документ, отличный от оригинала, и исходные цифровые подписи больше не будут действительными.

Эта коллекция никогда не бывает нулевой. Если документ не подписан, он будет содержать нулевые элементы.

**Возвращает:**
[DigitalSignatureCollection](../../com.aspose.words/digitalsignaturecollection) - Сбор ЭЦП для данного документа и результаты их проверки.
### getDirectSectionAttr(int key) {#getDirectSectionAttr-int-}
```
public Object getDirectSectionAttr(int key)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| key | int |  |

**Возвращает:**
java.lang.Объект
### getDocument() {#getDocument--}
```
public DocumentBase getDocument()
```


Получает документ, которому принадлежит этот узел.

Узел всегда принадлежит документу, даже если он только что создан и еще не добавлен в дерево или удален из дерева.

**Возвращает:**
[DocumentBase](../../com.aspose.words/documentbase)
### getEndnoteOptions() {#getEndnoteOptions--}
```
public EndnoteOptions getEndnoteOptions()
```


Предоставляет параметры, управляющие нумерацией и расположением концевых сносок в этом документе.

**Возвращает:**
[EndnoteOptions](../../com.aspose.words/endnoteoptions) - соответствующий[EndnoteOptions](../../com.aspose.words/endnoteoptions) ценность.
### getFieldOptions() {#getFieldOptions--}
```
public FieldOptions getFieldOptions()
```


Получает**FieldOptions** объект, представляющий параметры для управления обработкой полей в документе.

**Возвращает:**
[FieldOptions](../../com.aspose.words/fieldoptions) - А**FieldOptions** объект, представляющий параметры для управления обработкой полей в документе.
### getFirstChild() {#getFirstChild--}
```
public Node getFirstChild()
```


Получает первый дочерний элемент узла. Если нет первого дочернего узла, возвращается нуль.

**Возвращает:**
[Node](../../com.aspose.words/node) - Первый дочерний узел.
### getFirstSection() {#getFirstSection--}
```
public Section getFirstSection()
```


Получает первый раздел в документе. Возвращает null, если разделов нет.

**Возвращает:**
[Section](../../com.aspose.words/section) - Первый раздел в документе.
### getFontInfos() {#getFontInfos--}
```
public FontInfoCollection getFontInfos()
```


Предоставляет доступ к свойствам шрифтов, используемых в этом документе.

Эта коллекция определений шрифтов загружается как есть из документа. Определения шрифтов могут быть необязательными, отсутствовать или быть неполными в некоторых документах.

Не полагайтесь на эту коллекцию, чтобы убедиться, что в документе используется определенный шрифт. Вы должны использовать эту коллекцию только для получения информации о шрифтах, которые могут использоваться в документе.

**Возвращает:**
[FontInfoCollection](../../com.aspose.words/fontinfocollection) - соответствующий[FontInfoCollection](../../com.aspose.words/fontinfocollection) ценность.
### getFontSettings() {#getFontSettings--}
```
public FontSettings getFontSettings()
```


Получает настройки шрифта документа.

 Это свойство позволяет указать настройки шрифта для каждого документа. Если установлено значение null, настройки статического шрифта по умолчанию[FontSettings.getDefaultInstance()](../../com.aspose.words/fontsettings\#getDefaultInstance--) будет использован.

Значение по умолчанию равно нулю.

**Возвращает:**
[FontSettings](../../com.aspose.words/fontsettings) - Настройки шрифта документа.
### getFootnoteOptions() {#getFootnoteOptions--}
```
public FootnoteOptions getFootnoteOptions()
```


Предоставляет параметры, управляющие нумерацией и расположением сносок в этом документе.

**Возвращает:**
[FootnoteOptions](../../com.aspose.words/footnoteoptions) - соответствующий[FootnoteOptions](../../com.aspose.words/footnoteoptions) ценность.
### getFrameset() {#getFrameset--}
```
public Frameset getFrameset()
```


 Возвращает[getFrameset()](../../com.aspose.words/document\#getFrameset--) instance, если этот документ представляет страницу фреймов. Если документ не оформлен, свойство имеет**null** ценность.

**Возвращает:**
[Frameset](../../com.aspose.words/frameset) - А[getFrameset()](../../com.aspose.words/document\#getFrameset--) instance, если этот документ представляет страницу фреймов.
### getGlossaryDocument() {#getGlossaryDocument--}
```
public GlossaryDocument getGlossaryDocument()
```


Получает документ глоссария в этом документе или шаблоне. Глоссарий — это хранилище для записей автотекста, автозамены и стандартных блоков, определенных в документе.

Это свойство возвращает значение null, если в документе нет глоссария.

 Вы можете добавить глоссарий в документ, создав[GlossaryDocument](../../com.aspose.words/glossarydocument) объект и присвоение этому свойству.

**Возвращает:**
[GlossaryDocument](../../com.aspose.words/glossarydocument) - Глоссарий в этом документе или шаблоне.
### getGrammarChecked() {#getGrammarChecked--}
```
public boolean getGrammarChecked()
```


 Возвращает**true** если документ был проверен на грамматику. Чтобы перепроверить грамматику в документе, установите для этого свойства значение**false**.

**Возвращает:**
 логический -**true** если документ был проверен на грамматику.
### getHyphenationOptions() {#getHyphenationOptions--}
```
public HyphenationOptions getHyphenationOptions()
```


Предоставляет доступ к параметрам переноса документа.

**Возвращает:**
[HyphenationOptions](../../com.aspose.words/hyphenationoptions) - соответствующий[HyphenationOptions](../../com.aspose.words/hyphenationoptions) ценность.
### getLastChild() {#getLastChild--}
```
public Node getLastChild()
```


Получает последний дочерний элемент узла. Если последнего дочернего узла нет, возвращается нуль.

**Возвращает:**
[Node](../../com.aspose.words/node) - Последний дочерний узел.
### getLastSection() {#getLastSection--}
```
public Section getLastSection()
```


Получает последний раздел в документе. Возвращает null, если разделов нет.

**Возвращает:**
[Section](../../com.aspose.words/section) - Последний раздел в документе.
### getLayoutOptions() {#getLayoutOptions--}
```
public LayoutOptions getLayoutOptions()
```


Получает**LayoutOptions** объект, который представляет параметры для управления процессом компоновки этого документа.

**Возвращает:**
[LayoutOptions](../../com.aspose.words/layoutoptions) - А**LayoutOptions** объект, который представляет параметры для управления процессом компоновки этого документа.
### getLists() {#getLists--}
```
public ListCollection getLists()
```


Предоставляет доступ к форматированию списка, используемому в документе.

 Для получения дополнительной информации см. описание[ListCollection](../../com.aspose.words/listcollection) учебный класс.

**Возвращает:**
[ListCollection](../../com.aspose.words/listcollection) - соответствующий[ListCollection](../../com.aspose.words/listcollection) ценность.
### getMailMerge() {#getMailMerge--}
```
public MailMerge getMailMerge()
```


 Возвращает**MailMerge**объект, представляющий функциональность слияния для документа.

**Возвращает:**
[MailMerge](../../com.aspose.words/mailmerge) - А**MailMerge**объект, представляющий функциональность слияния для документа.
### getMailMergeSettings() {#getMailMergeSettings--}
```
public MailMergeSettings getMailMergeSettings()
```


Получает объект, содержащий всю информацию о слиянии для документа.

Вы можете использовать этот объект, чтобы указать источник данных слияния для документа, и эта информация (вместе с доступными полями данных) появится в Microsoft Word, когда пользователь откроет этот документ. Или вы можете использовать этот объект для запроса настроек слияния, которые пользователь указал в Microsoft Word для этого документа.

Этот объект никогда не бывает нулевым.

**Возвращает:**
[MailMergeSettings](../../com.aspose.words/mailmergesettings) - Объект, содержащий всю информацию о слиянии для документа.
### getNextMatchingNode(Node curNode) {#getNextMatchingNode-com.aspose.words.Node-}
```
public Node getNextMatchingNode(Node curNode)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| curNode | [Node](../../com.aspose.words/node) |  |

**Возвращает:**
[Node](../../com.aspose.words/node)
### getNextSibling() {#getNextSibling--}
```
public Node getNextSibling()
```


Получает узел, следующий сразу за этим узлом. Если следующего узла нет, возвращается нуль.

**Возвращает:**
[Node](../../com.aspose.words/node) - Узел, непосредственно следующий за этим узлом.
### getNodeChangingCallback() {#getNodeChangingCallback--}
```
public INodeChangingCallback getNodeChangingCallback()
```


Вызывается при вставке или удалении узла в документе.

**Возвращает:**
[INodeChangingCallback](../../com.aspose.words/inodechangingcallback) - соответствующий[INodeChangingCallback](../../com.aspose.words/inodechangingcallback) ценность.
### getNodeType() {#getNodeType--}
```
public int getNodeType()
```


 Возвращает**NodeType.Document**.

**Возвращает:**
 инт -**NodeType.Document** . Возвращаемое значение является одним из[NodeType](../../com.aspose.words/nodetype) константы.
### getOriginalFileName() {#getOriginalFileName--}
```
public String getOriginalFileName()
```


Получает исходное имя файла документа.

Возвращает null, если документ был загружен из потока или создан пустым.

**Возвращает:**
java.lang.String — Исходное имя файла документа.
### getOriginalLoadFormat() {#getOriginalLoadFormat--}
```
public int getOriginalLoadFormat()
```


Получает формат исходного документа, который был загружен в этот объект.

 Если вы создали новый пустой документ, возвращает[LoadFormat.DOC](../../com.aspose.words/loadformat\#DOC) ценность.

**Возвращает:**
 int — формат исходного документа, который был загружен в этот объект. Возвращаемое значение является одним из[LoadFormat](../../com.aspose.words/loadformat) константы.
### getPackageCustomParts() {#getPackageCustomParts--}
```
public CustomPartCollection getPackageCustomParts()
```


Получает набор настраиваемых частей (произвольное содержимое), которые связаны с пакетом OOXML с помощью «неизвестных связей».

Не путайте эти настраиваемые части с пользовательскими XML-данными. Если вам нужен доступ к частям Custom XML, используйте[getCustomXmlParts()](../../com.aspose.words/document\#getCustomXmlParts--) / [setCustomXmlParts(com.aspose.words.CustomXmlPartCollection)](../../com.aspose.words/document\#setCustomXmlParts-com.aspose.words.CustomXmlPartCollection-) имущество.

 Эта коллекция содержит части OOXML, родительским элементом которых является пакет OOXML, а их цели имеют "неизвестную связь". Для получения дополнительной информации см.[CustomPart](../../com.aspose.words/custompart).

Aspose.Words загружает и сохраняет пользовательские части только в документах OOXML.

Это свойство не может быть нулевым.

**Возвращает:**
[CustomPartCollection](../../com.aspose.words/custompartcollection) - Набор пользовательских частей (произвольный контент), которые связаны с пакетом OOXML с помощью «неизвестных отношений».
### getPageColor() {#getPageColor--}
```
public Color getPageColor()
```


 Получает цвет страницы документа. Это свойство является упрощенной версией[getBackgroundShape()](../../com.aspose.words/documentbase\#getBackgroundShape--) / [setBackgroundShape(com.aspose.words.Shape)](../../com.aspose.words/documentbase\#setBackgroundShape-com.aspose.words.Shape-).

 Это свойство предоставляет простой способ указать сплошной цвет страницы для документа. Установка этого свойства создает и устанавливает соответствующий[getBackgroundShape()](../../com.aspose.words/documentbase\#getBackgroundShape--) / [setBackgroundShape(com.aspose.words.Shape)](../../com.aspose.words/documentbase\#setBackgroundShape-com.aspose.words.Shape-).

Если цвет страницы не задан (например, в документе нет формы фона), возвращает нулевой цвет.

**Возвращает:**
java.awt.Color — цвет страницы документа.
### getPageCount() {#getPageCount--}
```
public int getPageCount()
```


Получает количество страниц в документе, рассчитанное самой последней операцией макета страницы.

**Возвращает:**
int — количество страниц в документе, рассчитанное самой последней операцией макета страницы.
### getPageInfo(int pageIndex) {#getPageInfo-int-}
```
public PageInfo getPageInfo(int pageIndex)
```


Получает размер страницы, ориентацию и другую информацию о странице, которая может быть полезна для печати или визуализации.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| pageIndex | int | Индекс страницы, начинающийся с 0. |

**Возвращает:**
[PageInfo](../../com.aspose.words/pageinfo)
### getParentNode() {#getParentNode--}
```
public CompositeNode getParentNode()
```


Получает непосредственного родителя этого узла.

Если узел был только что создан и еще не добавлен в дерево, или если он был удален из дерева, родитель имеет значение null.

**Возвращает:**
[CompositeNode](../../com.aspose.words/compositenode) - Непосредственный родитель этого узла.
### getPreviousSibling() {#getPreviousSibling--}
```
public Node getPreviousSibling()
```


Получает узел, непосредственно предшествующий этому узлу. Если предыдущего узла нет, возвращается нуль.

**Возвращает:**
[Node](../../com.aspose.words/node) - Узел, непосредственно предшествующий этому узлу.
### getProtectionType() {#getProtectionType--}
```
public int getProtectionType()
```


Получает текущий активный тип защиты документа.

Это свойство позволяет получить текущий установленный тип защиты документа. Для изменения типа защиты документа используйте кнопку**M:Aspose.Words.Document.Protect(Aspose.Words.ProtectionType,System.String)** а также[unprotect()](../../com.aspose.words/document\#unprotect--) методы.

Когда документ защищен, пользователь может вносить только ограниченные изменения, такие как добавление аннотаций, внесение изменений или заполнение формы.

 Обратите внимание, что защита документа отличается от защиты от записи. Защита от записи указывается с помощью[getWriteProtection()](../../com.aspose.words/document\#getWriteProtection--)

**M:Aspose.Words.Document.Protect(Aspose.Words.ProtectionType,System.String)**

**Возвращает:**
 int — Текущий активный тип защиты документа. Возвращаемое значение является одним из[ProtectionType](../../com.aspose.words/protectiontype) константы.
### getRange() {#getRange--}
```
public Range getRange()
```


 Возвращает**Range** объект, который представляет часть документа, содержащегося в этом узле.

**Возвращает:**
[Range](../../com.aspose.words/range) - А**Range** объект, который представляет часть документа, содержащегося в этом узле.
### getRemovePersonalInformation() {#getRemovePersonalInformation--}
```
public boolean getRemovePersonalInformation()
```


Получает флаг, указывающий, что Microsoft Word удалит всю информацию о пользователе из комментариев, редакций и свойств документа при сохранении документа.

**Возвращает:**
boolean — флаг, указывающий, что Microsoft Word удалит всю пользовательскую информацию из комментариев, редакций и свойств документа при сохранении документа.
### getResourceLoadingCallback() {#getResourceLoadingCallback--}
```
public IResourceLoadingCallback getResourceLoadingCallback()
```


Позволяет контролировать загрузку внешних ресурсов.

**Возвращает:**
[IResourceLoadingCallback](../../com.aspose.words/iresourceloadingcallback) - соответствующий[IResourceLoadingCallback](../../com.aspose.words/iresourceloadingcallback) ценность.
### getRevisions() {#getRevisions--}
```
public RevisionCollection getRevisions()
```


Получает коллекцию редакций (отслеживаемых изменений), существующих в этом документе.

Возвращаемая коллекция является «живой» коллекцией, что означает, что если вы удалите части документа, содержащие ревизии, удаленные ревизии автоматически исчезнут из этой коллекции.

**Возвращает:**
[RevisionCollection](../../com.aspose.words/revisioncollection) - Коллекция ревизий (отслеживаемых изменений), существующих в этом документе.
### getRevisionsView() {#getRevisionsView--}
```
public int getRevisionsView()
```


Получает значение, указывающее, следует ли работать с исходной или исправленной версией документа. Значение по умолчанию**[RevisionsView.ORIGINAL](../../com.aspose.words/revisionsview\#ORIGINAL)** .

**Возвращает:**
 int — значение, указывающее, следует ли работать с исходной или исправленной версией документа. Возвращаемое значение является одним из[RevisionsView](../../com.aspose.words/revisionsview) константы.
### getSections() {#getSections--}
```
public SectionCollection getSections()
```


Возвращает коллекцию, представляющую все разделы документа.

**Возвращает:**
[SectionCollection](../../com.aspose.words/sectioncollection) - Коллекция, представляющая все разделы документа.
### getShadeFormData() {#getShadeFormData--}
```
public boolean getShadeFormData()
```


Указывает, следует ли включать серое затенение полей формы.

**Возвращает:**
boolean - соответствующее логическое значение.
### getShowGrammaticalErrors() {#getShowGrammaticalErrors--}
```
public boolean getShowGrammaticalErrors()
```


Указывает, отображать ли грамматические ошибки в этом документе.

**Возвращает:**
boolean - соответствующее логическое значение.
### getShowSpellingErrors() {#getShowSpellingErrors--}
```
public boolean getShowSpellingErrors()
```


Указывает, отображать ли орфографические ошибки в этом документе.

**Возвращает:**
boolean - соответствующее логическое значение.
### getSpellingChecked() {#getSpellingChecked--}
```
public boolean getSpellingChecked()
```


 Возвращает**true** если документ был проверен на орфографию. Чтобы перепроверить орфографию в документе, установите для этого свойства значение**false**.

**Возвращает:**
 логический -**true** если документ был проверен на орфографию.
### getStyles() {#getStyles--}
```
public StyleCollection getStyles()
```


Возвращает набор стилей, определенных в документе.

 Для получения дополнительной информации см. описание[StyleCollection](../../com.aspose.words/stylecollection) учебный класс.

**Возвращает:**
[StyleCollection](../../com.aspose.words/stylecollection) - Набор стилей, определенных в документе.
### getText() {#getText--}
```
public String getText()
```


Получает текст этого узла и всех его дочерних элементов.

 Возвращаемая строка включает все управляющие и специальные символы, как описано в[ControlChar](../../com.aspose.words/controlchar).

**Возвращает:**
java.lang.String
### getTheme() {#getTheme--}
```
public Theme getTheme()
```


 Получает[getTheme()](../../com.aspose.words/document\#getTheme--) объект для этого документа.

**Возвращает:**
[Theme](../../com.aspose.words/theme) -[getTheme()](../../com.aspose.words/document\#getTheme--) объект для этого документа.
### getTrackRevisions() {#getTrackRevisions--}
```
public boolean getTrackRevisions()
```


**True** отслеживаются ли изменения при редактировании этого документа в Microsoft Word.

Установка этого параметра только указывает Microsoft Word, включено или выключено отслеживание изменений. Это свойство не влияет на изменения в документе, которые вы вносите программно через Aspose.Words.

 Если вы хотите автоматически отслеживать изменения, вносимые Aspose.Words программно в этот документ, используйте[startTrackRevisions(java.lang.String, java.util.Date)](../../com.aspose.words/document\#startTrackRevisions-java.lang.String--java.util.Date-) метод.

**Возвращает:**
boolean - соответствующее логическое значение.
### getVariables() {#getVariables--}
```
public VariableCollection getVariables()
```


Возвращает набор переменных, добавленных в документ или шаблон.

**Возвращает:**
[VariableCollection](../../com.aspose.words/variablecollection) - Набор переменных, добавленных в документ или шаблон.
### getVbaProject() {#getVbaProject--}
```
public VbaProject getVbaProject()
```


Получает[getVbaProject()](../../com.aspose.words/document\#getVbaProject--) / [setVbaProject(com.aspose.words.VbaProject)](../../com.aspose.words/document\#setVbaProject-com.aspose.words.VbaProject-).

**Возвращает:**
[VbaProject](../../com.aspose.words/vbaproject) - А[getVbaProject()](../../com.aspose.words/document\#getVbaProject--) / [setVbaProject(com.aspose.words.VbaProject)](../../com.aspose.words/document\#setVbaProject-com.aspose.words.VbaProject-).
### getVersionsCount() {#getVersionsCount--}
```
public int getVersionsCount()
```


Получает количество версий документа, сохраненных в документе DOC.

Доступ к версиям в Microsoft Word осуществляется через меню «Файл/Версии». Microsoft Word поддерживает версии только для файлов DOC.

Это свойство позволяет определить, были ли в этом документе сохранены версии документа до того, как он был открыт в Aspose.Words. Aspose.Words не предоставляет никакой другой поддержки версий документа. Если вы сохраните этот документ с помощью Aspose.Words, документ будет сохранен без версий.

**Возвращает:**
int — количество версий документа, хранившихся в документе DOC.
### getViewOptions() {#getViewOptions--}
```
public ViewOptions getViewOptions()
```


Предоставляет параметры для управления отображением документа в Microsoft Word.

**Возвращает:**
[ViewOptions](../../com.aspose.words/viewoptions) - соответствующий[ViewOptions](../../com.aspose.words/viewoptions) ценность.
### getWarningCallback() {#getWarningCallback--}
```
public IWarningCallback getWarningCallback()
```


 Вызывается во время различных процедур обработки документов при обнаружении проблемы, которая может привести к потере точности данных или форматирования. Документ может генерировать предупреждения на любом этапе своего существования, поэтому важно настроить обратный вызов предупреждения как можно раньше, чтобы избежать потери предупреждений. Например, такие свойства, как[Document.getPageCount()](../../com.aspose.words/document\#getPageCount--) на самом деле создать макет документа, который позже используется для рендеринга, и предупреждения макета могут быть потеряны, если обратный вызов предупреждения указан только для вызовов рендеринга позже.

**Возвращает:**
[IWarningCallback](../../com.aspose.words/iwarningcallback) - соответствующий[IWarningCallback](../../com.aspose.words/iwarningcallback) ценность.
### getWatermark() {#getWatermark--}
```
public Watermark getWatermark()
```


Предоставляет доступ к водяному знаку документа.

**Возвращает:**
[Watermark](../../com.aspose.words/watermark) - соответствующий[Watermark](../../com.aspose.words/watermark) ценность.
### getWebExtensionTaskPanes() {#getWebExtensionTaskPanes--}
```
public TaskPaneCollection getWebExtensionTaskPanes()
```


Возвращает коллекцию, представляющую список надстроек области задач.

**Возвращает:**
[TaskPaneCollection](../../com.aspose.words/taskpanecollection) Коллекция, представляющая список надстроек области задач.
### getWriteProtection() {#getWriteProtection--}
```
public WriteProtection getWriteProtection()
```


Предоставляет доступ к параметрам защиты документа от записи.

**Возвращает:**
[WriteProtection](../../com.aspose.words/writeprotection) - соответствующий[WriteProtection](../../com.aspose.words/writeprotection) ценность.
### hasChildNodes() {#hasChildNodes--}
```
public boolean hasChildNodes()
```


Возвращает true, если у этого узла есть дочерние узлы.

**Возвращает:**
boolean — Истинно, если у этого узла есть дочерние узлы.
### hasMacros() {#hasMacros--}
```
public boolean hasMacros()
```


 Возвращает**true** если документ имеет проект VBA (макросы).

**Возвращает:**
 логический -**true** если документ имеет проект VBA (макросы).
### hasRevisions() {#hasRevisions--}
```
public boolean hasRevisions()
```


 Возвращает**true** если документ имеет какие-либо отслеживаемые изменения. Это свойство является ярлыком для сравнения[RevisionCollection.getCount()](../../com.aspose.words/revisioncollection\#getCount--) до нуля.

**Возвращает:**
 логический -**true** если документ имеет какие-либо отслеживаемые изменения.
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**Возвращает:**
инт
### importNode(Node srcNode, boolean isImportChildren) {#importNode-com.aspose.words.Node-boolean-}
```
public Node importNode(Node srcNode, boolean isImportChildren)
```


Импортирует узел из другого документа в текущий документ.

Импортирует узел из другого документа в текущий документ.

 Этот метод использует[ImportFormatMode.USE\_DESTINATION\_STYLES](../../com.aspose.words/importformatmode\#USE-DESTINATION-STYLES) возможность разрешить форматирование.

При импорте узла создается копия исходного узла, принадлежащего импортируемому документу. Возвращенный узел не имеет родителя. Исходный узел не изменяется и не удаляется из исходного документа.

 Прежде чем узел из другого документа можно будет вставить в этот документ, его необходимо импортировать. Во время импорта свойства документа, такие как ссылки на стили и списки, переводятся из оригинала в импортируемый документ. После того, как узел был импортирован, его можно вставить в соответствующее место документа с помощью[CompositeNode.insertBefore(com.aspose.words.Node, com.aspose.words.Node)](../../com.aspose.words/compositenode\#insertBefore-com.aspose.words.Node--com.aspose.words.Node-) или же[CompositeNode.insertAfter(com.aspose.words.Node, com.aspose.words.Node)](../../com.aspose.words/compositenode\#insertAfter-com.aspose.words.Node--com.aspose.words.Node-).

Если исходный узел уже принадлежит целевому документу, то создается просто глубокий клон исходного узла.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| srcNode | [Node](../../com.aspose.words/node) | Импортируемый узел. |
| isImportChildren | boolean | Значение true для рекурсивного импорта всех дочерних узлов; в противном случае ложно. |

**Возвращает:**
[Node](../../com.aspose.words/node) Клонированный узел, принадлежащий текущему документу.
### importNode(Node srcNode, boolean isImportChildren, int importFormatMode) {#importNode-com.aspose.words.Node-boolean-int-}
```
public Node importNode(Node srcNode, boolean isImportChildren, int importFormatMode)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| srcNode | [Node](../../com.aspose.words/node) |  |
| isImportChildren | boolean |  |
| importFormatMode | int |  |

**Возвращает:**
[Node](../../com.aspose.words/node)
### indexOf(Node child) {#indexOf-com.aspose.words.Node-}
```
public int indexOf(Node child)
```


Возвращает индекс указанного дочернего узла в массиве дочерних узлов. Возвращает -1, если узел не найден среди дочерних узлов.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| child | [Node](../../com.aspose.words/node) |  |

**Возвращает:**
инт
### insertAfter(Node newChild, Node refChild) {#insertAfter-com.aspose.words.Node-com.aspose.words.Node-}
```
public Node insertAfter(Node newChild, Node refChild)
```


Вставляет указанный узел сразу после указанного ссылочного узла.

Если refChild имеет значение null, вставляет newChild в начало списка дочерних узлов.

Если новый дочерний элемент уже находится в дереве, он сначала удаляется.

 Если вставляемый узел был создан из другого документа, следует использовать**M:Aspose.Words.DocumentBase.ImportNode(Aspose.Words.Node,System.Boolean,Aspose.Words.ImportFormatMode)** чтобы импортировать узел в текущий документ. Затем импортированный узел можно вставить в текущий документ.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| newChild | [Node](../../com.aspose.words/node) | Узел для вставки. |
| refChild | [Node](../../com.aspose.words/node) | Узел, который является эталонным узлом. newNode размещается после refNode. |

**Возвращает:**
[Node](../../com.aspose.words/node) - Вставленный узел.
### insertBefore(Node newChild, Node refChild) {#insertBefore-com.aspose.words.Node-com.aspose.words.Node-}
```
public Node insertBefore(Node newChild, Node refChild)
```


Вставляет указанный узел непосредственно перед указанным ссылочным узлом.

Если refChild имеет значение null, вставляет newChild в конец списка дочерних узлов.

Если новый дочерний элемент уже находится в дереве, он сначала удаляется.

 Если вставляемый узел был создан из другого документа, следует использовать**M:Aspose.Words.DocumentBase.ImportNode(Aspose.Words.Node,System.Boolean,Aspose.Words.ImportFormatMode)** чтобы импортировать узел в текущий документ. Затем импортированный узел можно вставить в текущий документ.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| newChild | [Node](../../com.aspose.words/node) | Узел для вставки. |
| refChild | [Node](../../com.aspose.words/node) | Узел, который является эталонным узлом. Новый дочерний элемент помещается перед этим узлом. |

**Возвращает:**
[Node](../../com.aspose.words/node) - Вставленный узел.
### isComposite() {#isComposite--}
```
public boolean isComposite()
```


Возвращает true, так как этот узел может иметь дочерние узлы.

**Возвращает:**
boolean — True, так как этот узел может иметь дочерние узлы.
### iterator() {#iterator--}
```
public Iterator iterator()
```


Обеспечивает поддержку для каждой итерации стиля над дочерними узлами этого узла.

**Возвращает:**
java.util.Iterator
### joinRunsWithSameFormatting() {#joinRunsWithSameFormatting--}
```
public int joinRunsWithSameFormatting()
```


Соединения выполняются с одинаковым форматированием во всех абзацах документа.

Это метод оптимизации. Некоторые документы содержат смежные прогоны с одинаковым форматированием. Обычно это происходит, если документ интенсивно редактировался вручную. Вы можете уменьшить размер документа и ускорить дальнейшую обработку, объединив эти прогоны.

 Операция проверяет каждый[Paragraph](../../com.aspose.words/paragraph) узел в документе для смежных[Run](../../com.aspose.words/run) узлы с одинаковыми свойствами. Он игнорирует уникальные идентификаторы, используемые для отслеживания сеансов редактирования создания и модификации прогонов. При первом запуске в каждой последовательности соединения накапливается весь текст. Оставшиеся прогоны удаляются из документа.

**Возвращает:**
 int — количество выполненных объединений. Когда**N** соединяются соседние прогоны, они считаются**N - 1** присоединяется.
### nextPreOrder(Node rootNode) {#nextPreOrder-com.aspose.words.Node-}
```
public Node nextPreOrder(Node rootNode)
```


Получает следующий узел в соответствии с алгоритмом обхода дерева предварительного порядка.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| rootNode | [Node](../../com.aspose.words/node) | Верхний узел (предел) обхода. |

**Возвращает:**
[Node](../../com.aspose.words/node) - Следующий узел в порядке предварительного заказа. Null, если достигнут rootNode.
### nodeTypeToString(int nodeType) {#nodeTypeToString-int-}
```
public static String nodeTypeToString(int nodeType)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| nodeType | int |  |

**Возвращает:**
java.lang.String
### normalizeFieldTypes() {#normalizeFieldTypes--}
```
public void normalizeFieldTypes()
```


 Изменяет значения типа поля[FieldChar.getFieldType()](../../com.aspose.words/fieldchar\#getFieldType--) из[FieldStart](../../com.aspose.words/fieldstart), [FieldSeparator](../../com.aspose.words/fieldseparator), [FieldEnd](../../com.aspose.words/fieldend) во всем документе, чтобы они соответствовали типам полей, содержащимся в кодах полей.

Используйте этот метод после изменений документа, влияющих на типы полей.

 Чтобы изменить значения типа поля в определенной части документа, используйте[Range.normalizeFieldTypes()](../../com.aspose.words/range\#normalizeFieldTypes--).

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


Добавляет указанный узел в начало списка дочерних узлов для этого узла.

Если новый дочерний элемент уже находится в дереве, он сначала удаляется.

 Если вставляемый узел был создан из другого документа, следует использовать**M:Aspose.Words.DocumentBase.ImportNode(Aspose.Words.Node,System.Boolean,Aspose.Words.ImportFormatMode)** чтобы импортировать узел в текущий документ. Затем импортированный узел можно вставить в текущий документ.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| newChild | [Node](../../com.aspose.words/node) | Добавляемый узел. |

**Возвращает:**
[Node](../../com.aspose.words/node) - Добавлен узел.
### previousPreOrder(Node rootNode) {#previousPreOrder-com.aspose.words.Node-}
```
public Node previousPreOrder(Node rootNode)
```


Получает предыдущий узел в соответствии с алгоритмом обхода дерева предварительного порядка.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| rootNode | [Node](../../com.aspose.words/node) | Верхний узел (предел) обхода. |

**Возвращает:**
[Node](../../com.aspose.words/node) - Предыдущий узел в порядке предварительного заказа. Null, если достигнут rootNode.
### print() {#print--}
```
public void print()
```


Печатает документ без вызова каких-либо форм пользовательского интерфейса. Печать всего документа на принтере по умолчанию.

### print(String printerName) {#print-java.lang.String-}
```
public void print(String printerName)
```


Распечатайте весь документ на указанном принтере, используя стандартный (без пользовательского интерфейса) контроллер печати.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| printerName | java.lang.String | Имя принтера. |

### print(AttributeSet printerSettings) {#print-javax.print.attribute.AttributeSet-}
```
public void print(AttributeSet printerSettings)
```


Печать документа в соответствии с заданными параметрами принтера с использованием стандартного (без пользовательского интерфейса) контроллера печати.

Объект позволяет указать принтер для печати, диапазон страниц для печати и другие параметры.

Может содержать как настройку запроса PrintJob, так и настройку поиска PrintService.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| printerSettings | javax.print.attribute.AttributeSet | Используемые настройки принтера. |

### print(AttributeSet printerSettings, String documentName) {#print-javax.print.attribute.AttributeSet-java.lang.String-}
```
public void print(AttributeSet printerSettings, String documentName)
```


Печать документа в соответствии с указанными настройками принтера с использованием стандартного (без пользовательского интерфейса) контроллера печати и имени документа.

Объект позволяет указать принтер для печати, диапазон страниц для печати и другие параметры.

Может содержать как настройку запроса PrintJob, так и настройку поиска PrintService.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| printerSettings | javax.print.attribute.AttributeSet | Используемые настройки принтера. |
| documentName | java.lang.String | Имя документа, которое будет отображаться (например, в диалоговом окне состояния печати или в очереди печати) при печати документа. |

### protect(int type) {#protect-int-}
```
public void protect(int type)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| type | int |  |

### protect(int type, String password) {#protect-int-java.lang.String-}
```
public void protect(int type, String password)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| type | int |  |
| password | java.lang.String |  |

### remove() {#remove--}
```
public void remove()
```


Удаляет себя из родителя.

### removeAllChildren() {#removeAllChildren--}
```
public void removeAllChildren()
```


Удаляет все дочерние узлы текущего узла.

### removeChild(Node oldChild) {#removeChild-com.aspose.words.Node-}
```
public Node removeChild(Node oldChild)
```


Удаляет указанный дочерний узел.

Родительский элемент oldChild устанавливается равным нулю после удаления узла.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| oldChild | [Node](../../com.aspose.words/node) | Узел для удаления. |

**Возвращает:**
[Node](../../com.aspose.words/node) - Удаленный узел.
### removeExternalSchemaReferences() {#removeExternalSchemaReferences--}
```
public void removeExternalSchemaReferences()
```


Удаляет ссылки на внешние XML-схемы из этого документа.

### removeMacros() {#removeMacros--}
```
public void removeMacros()
```


Удаляет все макросы (проект VBA), а также панели инструментов и настройки команд из документа.

Удаляя все макросы из документа, вы гарантируете, что документ не содержит макровирусов.

### removeSmartTags() {#removeSmartTags--}
```
public void removeSmartTags()
```


 Удаляет все[SmartTag](../../com.aspose.words/smarttag) узлы-потомки текущего узла. Этот метод не удаляет содержимое смарт-тегов.

### renderToScale(int pageIndex, Graphics2D graphics, float x, float y, float scale) {#renderToScale-int-java.awt.Graphics2D-float-float-float-}
```
public Point2D.Float renderToScale(int pageIndex, Graphics2D graphics, float x, float y, float scale)
```


Преобразует страницу документа в объект в указанном масштабе.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| pageIndex | int | Индекс страницы, начинающийся с 0. |
| graphics | java.awt.Graphics2D | Объект, на который выполняется рендеринг. |
| x | float | Координата X (в мировых единицах) левого верхнего угла отображаемой страницы. |
| y | float | Координата Y (в мировых единицах) левого верхнего угла отображаемой страницы. |
| scale | float | Масштаб рендеринга страницы (1.0 это 100%). |

**Возвращает:**
java.awt.geom.Point2D.Float — ширина и высота (в мировых единицах) отображаемой страницы.
### renderToSize(int pageIndex, Graphics2D graphics, float x, float y, float width, float height) {#renderToSize-int-java.awt.Graphics2D-float-float-float-float-}
```
public float renderToSize(int pageIndex, Graphics2D graphics, float x, float y, float width, float height)
```


Преобразует страницу документа в объект заданного размера.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| pageIndex | int | Индекс страницы, начинающийся с 0. |
| graphics | java.awt.Graphics2D | Объект, на который выполняется рендеринг. |
| x | float | Координата X (в мировых единицах) левого верхнего угла отображаемой страницы. |
| y | float | Координата Y (в мировых единицах) левого верхнего угла отображаемой страницы. |
| width | float | Максимальная ширина (в мировых единицах), которую может занимать отображаемая страница. |
| height | float | Максимальная высота (в мировых единицах), которую может занимать отображаемая страница. |

**Возвращает:**
float - Масштаб, который автоматически рассчитывается для отображаемой страницы, чтобы соответствовать указанному размеру.
### save(OutputStream stream, SaveOptions saveOptions) {#save-java.io.OutputStream-com.aspose.words.SaveOptions-}
```
public SaveOutputParameters save(OutputStream stream, SaveOptions saveOptions)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| stream | java.io.OutputStream |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions) |  |

**Возвращает:**
[SaveOutputParameters](../../com.aspose.words/saveoutputparameters)
### save(OutputStream stream, int saveFormat) {#save-java.io.OutputStream-int-}
```
public SaveOutputParameters save(OutputStream stream, int saveFormat)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| stream | java.io.OutputStream |  |
| saveFormat | int |  |

**Возвращает:**
[SaveOutputParameters](../../com.aspose.words/saveoutputparameters)
### save(String fileName) {#save-java.lang.String-}
```
public SaveOutputParameters save(String fileName)
```


Сохраняет документ. Сохраняет документ в файл. Автоматически определяет формат сохранения из расширения.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| fileName | java.lang.String | Имя для документа. Если документ с указанным именем файла уже существует, существующий документ перезаписывается. |

**Возвращает:**
[SaveOutputParameters](../../com.aspose.words/saveoutputparameters) - Дополнительная информация, которую вы можете использовать по желанию.
### save(String fileName, SaveOptions saveOptions) {#save-java.lang.String-com.aspose.words.SaveOptions-}
```
public SaveOutputParameters save(String fileName, SaveOptions saveOptions)
```


Сохраняет документ в файл, используя указанные параметры сохранения.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| fileName | java.lang.String | Имя для документа. Если документ с указанным именем файла уже существует, существующий документ перезаписывается. |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions) | Указывает параметры, управляющие способом сохранения документа. Может быть нулевым. |

**Возвращает:**
[SaveOutputParameters](../../com.aspose.words/saveoutputparameters) - Дополнительная информация, которую вы можете использовать по желанию.
### save(String fileName, int saveFormat) {#save-java.lang.String-int-}
```
public SaveOutputParameters save(String fileName, int saveFormat)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| fileName | java.lang.String |  |
| saveFormat | int |  |

**Возвращает:**
[SaveOutputParameters](../../com.aspose.words/saveoutputparameters)
### selectNodes(String xpath) {#selectNodes-java.lang.String-}
```
public NodeList selectNodes(String xpath)
```


Выбирает список узлов, соответствующих выражению XPath.

На данный момент поддерживаются только выражения с именами элементов. Выражения, использующие имена атрибутов, не поддерживаются.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| xpath | java.lang.String | Выражение XPath. |

**Возвращает:**
[NodeList](../../com.aspose.words/nodelist) - Список узлов, соответствующих запросу XPath.
### selectSingleNode(String xpath) {#selectSingleNode-java.lang.String-}
```
public Node selectSingleNode(String xpath)
```


Выбирает первый узел, соответствующий выражению XPath.

На данный момент поддерживаются только выражения с именами элементов. Выражения, использующие имена атрибутов, не поддерживаются.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| xpath | java.lang.String | Выражение XPath. |

**Возвращает:**
[Node](../../com.aspose.words/node) - Первый узел, соответствующий запросу XPath, или нуль, если соответствующий узел не найден.
### setAttachedTemplate(String value) {#setAttachedTemplate-java.lang.String-}
```
public void setAttachedTemplate(String value)
```


Задает полный путь к шаблону, прикрепленному к документу.

Пустая строка означает, что документ прикреплен к шаблону Normal.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Полный путь к шаблону, прикрепленному к документу. |

### setAutomaticallyUpdateStyles(boolean value) {#setAutomaticallyUpdateStyles-boolean-}
```
public void setAutomaticallyUpdateStyles(boolean value)
```


Устанавливает флаг, указывающий, обновляются ли стили в документе в соответствии со стилями в прикрепленном шаблоне каждый раз, когда документ открывается в MS Word.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Флаг, указывающий, обновляются ли стили в документе в соответствии со стилями в прикрепленном шаблоне каждый раз, когда документ открывается в MS Word. |

### setBackgroundShape(Shape value) {#setBackgroundShape-com.aspose.words.Shape-}
```
public void setBackgroundShape(Shape value)
```


Устанавливает форму фона документа. Может быть нулевым.

Microsoft Word допускает только ту форму, которая имеет свою[ShapeBase.getShapeType()](../../com.aspose.words/shapebase\#getShapeType--) свойство, равное[ShapeType.RECTANGLE](../../com.aspose.words/shapetype\#RECTANGLE) для использования в качестве фоновой формы для документа.

Microsoft Word поддерживает только свойства заливки фоновой фигуры. Все остальные свойства игнорируются.

 Установка для этого свойства ненулевого значения также установит[ViewOptions.getDisplayBackgroundShape()](../../com.aspose.words/viewoptions\#getDisplayBackgroundShape--) / [ViewOptions.setDisplayBackgroundShape(boolean)](../../com.aspose.words/viewoptions\#setDisplayBackgroundShape-boolean-) к истине.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | [Shape](../../com.aspose.words/shape) | Форма фона документа. |

### setCustomNodeId(int value) {#setCustomNodeId-int-}
```
public void setCustomNodeId(int value)
```


Задает идентификатор пользовательского узла.

По умолчанию ноль.

Этот идентификатор можно установить и использовать произвольно. Например, как ключ для получения внешних данных.

Важное примечание: указанное значение не сохраняется в выходной файл и существует только в течение срока службы узла.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int | Соответствующее целочисленное значение. |

### setCustomXmlParts(CustomXmlPartCollection value) {#setCustomXmlParts-com.aspose.words.CustomXmlPartCollection-}
```
public void setCustomXmlParts(CustomXmlPartCollection value)
```


Задает коллекцию пользовательских частей хранилища данных XML.

Aspose.Words загружает и сохраняет пользовательские XML-части только в документах OOXML и DOC.

Это свойство не может быть нулевым.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | [CustomXmlPartCollection](../../com.aspose.words/customxmlpartcollection) | Коллекция пользовательских частей хранилища данных XML. |

### setDefaultTabStop(double value) {#setDefaultTabStop-double-}
```
public void setDefaultTabStop(double value)
```


Устанавливает интервал (в пунктах) между позициями табуляции по умолчанию.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | double | Интервал (в пунктах) между позициями табуляции по умолчанию. |

### setFontSettings(FontSettings value) {#setFontSettings-com.aspose.words.FontSettings-}
```
public void setFontSettings(FontSettings value)
```


Задает настройки шрифта документа.

 Это свойство позволяет указать настройки шрифта для каждого документа. Если установлено значение null, настройки статического шрифта по умолчанию[FontSettings.getDefaultInstance()](../../com.aspose.words/fontsettings\#getDefaultInstance--) будет использован.

Значение по умолчанию равно нулю.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | [FontSettings](../../com.aspose.words/fontsettings) | Настройки шрифта документа. |

### setGlossaryDocument(GlossaryDocument value) {#setGlossaryDocument-com.aspose.words.GlossaryDocument-}
```
public void setGlossaryDocument(GlossaryDocument value)
```


Задает глоссарий в этом документе или шаблоне. Глоссарий — это хранилище для записей автотекста, автозамены и стандартных блоков, определенных в документе.

Это свойство возвращает значение null, если в документе нет глоссария.

 Вы можете добавить глоссарий в документ, создав[GlossaryDocument](../../com.aspose.words/glossarydocument) объект и присвоение этому свойству.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | [GlossaryDocument](../../com.aspose.words/glossarydocument) | Глоссарий в этом документе или шаблоне. |

### setGrammarChecked(boolean value) {#setGrammarChecked-boolean-}
```
public void setGrammarChecked(boolean value)
```


 Возвращает**true** если документ был проверен на грамматику. Чтобы перепроверить грамматику в документе, установите для этого свойства значение**false**.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | **true** если документ был проверен на грамматику. |

### setMailMergeSettings(MailMergeSettings value) {#setMailMergeSettings-com.aspose.words.MailMergeSettings-}
```
public void setMailMergeSettings(MailMergeSettings value)
```


Задает объект, содержащий всю информацию о слиянии для документа.

Вы можете использовать этот объект, чтобы указать источник данных слияния для документа, и эта информация (вместе с доступными полями данных) появится в Microsoft Word, когда пользователь откроет этот документ. Или вы можете использовать этот объект для запроса настроек слияния, которые пользователь указал в Microsoft Word для этого документа.

Этот объект никогда не бывает нулевым.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | [MailMergeSettings](../../com.aspose.words/mailmergesettings) | Объект, содержащий всю информацию о слиянии для документа. |

### setNodeChangingCallback(INodeChangingCallback value) {#setNodeChangingCallback-com.aspose.words.INodeChangingCallback-}
```
public void setNodeChangingCallback(INodeChangingCallback value)
```


Вызывается при вставке или удалении узла в документе.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | [INodeChangingCallback](../../com.aspose.words/inodechangingcallback) |  Соответствующий[INodeChangingCallback](../../com.aspose.words/inodechangingcallback) ценность. |

### setPackageCustomParts(CustomPartCollection value) {#setPackageCustomParts-com.aspose.words.CustomPartCollection-}
```
public void setPackageCustomParts(CustomPartCollection value)
```


Задает набор настраиваемых частей (произвольное содержимое), которые связаны с пакетом OOXML с помощью «неизвестных связей».

Не путайте эти настраиваемые части с пользовательскими XML-данными. Если вам нужен доступ к частям Custom XML, используйте[getCustomXmlParts()](../../com.aspose.words/document\#getCustomXmlParts--) / [setCustomXmlParts(com.aspose.words.CustomXmlPartCollection)](../../com.aspose.words/document\#setCustomXmlParts-com.aspose.words.CustomXmlPartCollection-) имущество.

 Эта коллекция содержит части OOXML, родительским элементом которых является пакет OOXML, а их цели имеют "неизвестную связь". Для получения дополнительной информации см.[CustomPart](../../com.aspose.words/custompart).

Aspose.Words загружает и сохраняет пользовательские части только в документах OOXML.

Это свойство не может быть нулевым.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | [CustomPartCollection](../../com.aspose.words/custompartcollection) | Набор пользовательских частей (произвольное содержимое), которые связаны с пакетом OOXML с помощью «неизвестных связей». |

### setPageColor(Color value) {#setPageColor-java.awt.Color-}
```
public void setPageColor(Color value)
```


 Устанавливает цвет страницы документа. Это свойство является упрощенной версией[getBackgroundShape()](../../com.aspose.words/documentbase\#getBackgroundShape--) / [setBackgroundShape(com.aspose.words.Shape)](../../com.aspose.words/documentbase\#setBackgroundShape-com.aspose.words.Shape-).

 Это свойство предоставляет простой способ указать сплошной цвет страницы для документа. Установка этого свойства создает и устанавливает соответствующий[getBackgroundShape()](../../com.aspose.words/documentbase\#getBackgroundShape--) / [setBackgroundShape(com.aspose.words.Shape)](../../com.aspose.words/documentbase\#setBackgroundShape-com.aspose.words.Shape-).

Если цвет страницы не задан (например, в документе нет формы фона), возвращает нулевой цвет.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.awt.Color | Цвет страницы документа. |

### setRemovePersonalInformation(boolean value) {#setRemovePersonalInformation-boolean-}
```
public void setRemovePersonalInformation(boolean value)
```


Устанавливает флаг, указывающий, что Microsoft Word удалит всю информацию о пользователе из комментариев, редакций и свойств документа при сохранении документа.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Флаг, указывающий, что Microsoft Word удалит всю пользовательскую информацию из комментариев, редакций и свойств документа при сохранении документа. |

### setResourceLoadingCallback(IResourceLoadingCallback value) {#setResourceLoadingCallback-com.aspose.words.IResourceLoadingCallback-}
```
public void setResourceLoadingCallback(IResourceLoadingCallback value)
```


Позволяет контролировать загрузку внешних ресурсов.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | [IResourceLoadingCallback](../../com.aspose.words/iresourceloadingcallback) |  Соответствующий[IResourceLoadingCallback](../../com.aspose.words/iresourceloadingcallback) ценность. |

### setRevisionsView(int value) {#setRevisionsView-int-}
```
public void setRevisionsView(int value)
```


 Задает значение, указывающее, следует ли работать с исходной или исправленной версией документа. Значение по умолчанию**[RevisionsView.ORIGINAL](../../com.aspose.words/revisionsview\#ORIGINAL)** .

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Значение, указывающее, следует ли работать с исходной или исправленной версией документа. Значение должно быть одним из[RevisionsView](../../com.aspose.words/revisionsview) константы. |

### setSectionAttr(int key, Object value) {#setSectionAttr-int-java.lang.Object-}
```
public void setSectionAttr(int key, Object value)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| key | int |  |
| value | java.lang.Object |  |

### setShadeFormData(boolean value) {#setShadeFormData-boolean-}
```
public void setShadeFormData(boolean value)
```


Указывает, следует ли включать серое затенение полей формы.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setShowGrammaticalErrors(boolean value) {#setShowGrammaticalErrors-boolean-}
```
public void setShowGrammaticalErrors(boolean value)
```


Указывает, отображать ли грамматические ошибки в этом документе.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setShowSpellingErrors(boolean value) {#setShowSpellingErrors-boolean-}
```
public void setShowSpellingErrors(boolean value)
```


Указывает, отображать ли орфографические ошибки в этом документе.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setSpellingChecked(boolean value) {#setSpellingChecked-boolean-}
```
public void setSpellingChecked(boolean value)
```


 Возвращает**true** если документ был проверен на орфографию. Чтобы перепроверить орфографию в документе, установите для этого свойства значение**false**.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | **true** если документ был проверен на орфографию. |

### setTrackRevisions(boolean value) {#setTrackRevisions-boolean-}
```
public void setTrackRevisions(boolean value)
```


**True** отслеживаются ли изменения при редактировании этого документа в Microsoft Word.

Установка этого параметра только указывает Microsoft Word, включено или выключено отслеживание изменений. Это свойство не влияет на изменения в документе, которые вы вносите программно через Aspose.Words.

 Если вы хотите автоматически отслеживать изменения, вносимые Aspose.Words программно в этот документ, используйте[startTrackRevisions(java.lang.String, java.util.Date)](../../com.aspose.words/document\#startTrackRevisions-java.lang.String--java.util.Date-) метод.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setVbaProject(VbaProject value) {#setVbaProject-com.aspose.words.VbaProject-}
```
public void setVbaProject(VbaProject value)
```


 Устанавливает[getVbaProject()](../../com.aspose.words/document\#getVbaProject--) / [setVbaProject(com.aspose.words.VbaProject)](../../com.aspose.words/document\#setVbaProject-com.aspose.words.VbaProject-).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | [VbaProject](../../com.aspose.words/vbaproject) |  А[getVbaProject()](../../com.aspose.words/document\#getVbaProject--) / [setVbaProject(com.aspose.words.VbaProject)](../../com.aspose.words/document\#setVbaProject-com.aspose.words.VbaProject-). |

### setWarningCallback(IWarningCallback value) {#setWarningCallback-com.aspose.words.IWarningCallback-}
```
public void setWarningCallback(IWarningCallback value)
```


 Вызывается во время различных процедур обработки документов при обнаружении проблемы, которая может привести к потере точности данных или форматирования. Документ может генерировать предупреждения на любом этапе своего существования, поэтому важно настроить обратный вызов предупреждения как можно раньше, чтобы избежать потери предупреждений. Например, такие свойства, как[Document.getPageCount()](../../com.aspose.words/document\#getPageCount--) на самом деле создать макет документа, который позже используется для рендеринга, и предупреждения макета могут быть потеряны, если обратный вызов предупреждения указан только для вызовов рендеринга позже.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | [IWarningCallback](../../com.aspose.words/iwarningcallback) |  Соответствующий[IWarningCallback](../../com.aspose.words/iwarningcallback) ценность. |

### startTrackRevisions(String author) {#startTrackRevisions-java.lang.String-}
```
public void startTrackRevisions(String author)
```


Начинает автоматически отмечать все дальнейшие изменения, которые вы вносите в документ программно, как изменения версии.

Если вы вызовете этот метод, а затем внесете некоторые изменения в документ программно, сохраните документ, а затем откроете документ в MS Word, вы увидите эти изменения как ревизии.

В настоящее время Aspose.Words поддерживает только отслеживание вставок и удалений узлов. Изменения форматирования не записываются как ревизии.

 Автоматическое отслеживание изменений поддерживается как при модификации этого документа посредством манипуляций с узлами, так и при использовании[DocumentBuilder](../../com.aspose.words/documentbuilder)

 Этот метод не изменяет[getTrackRevisions()](../../com.aspose.words/document\#getTrackRevisions--) / [setTrackRevisions(boolean)](../../com.aspose.words/document\#setTrackRevisions-boolean-) option и не использует его значение для целей отслеживания изменений.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| author | java.lang.String | Инициалы автора использовать для редакций. |

### startTrackRevisions(String author, Date dateTime) {#startTrackRevisions-java.lang.String-java.util.Date-}
```
public void startTrackRevisions(String author, Date dateTime)
```


Начинает автоматически отмечать все дальнейшие изменения, которые вы вносите в документ программно, как изменения версии.

Если вы вызовете этот метод, а затем внесете некоторые изменения в документ программно, сохраните документ, а затем откроете документ в MS Word, вы увидите эти изменения как ревизии.

В настоящее время Aspose.Words поддерживает только отслеживание вставок и удалений узлов. Изменения форматирования не записываются как ревизии.

 Автоматическое отслеживание изменений поддерживается как при модификации этого документа посредством манипуляций с узлами, так и при использовании[DocumentBuilder](../../com.aspose.words/documentbuilder)

 Этот метод не изменяет[getTrackRevisions()](../../com.aspose.words/document\#getTrackRevisions--) / [setTrackRevisions(boolean)](../../com.aspose.words/document\#setTrackRevisions-boolean-) option и не использует его значение для целей отслеживания изменений.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| author | java.lang.String | Инициалы автора использовать для редакций. |
| dateTime | java.util.Date | Дата и время для использования для изменений. |

### stopTrackRevisions() {#stopTrackRevisions--}
```
public void stopTrackRevisions()
```


Останавливает автоматическую маркировку изменений документа как редакций.

### toString() {#toString--}
```
public String toString()
```




**Возвращает:**
java.lang.String
### toString(SaveOptions saveOptions) {#toString-com.aspose.words.SaveOptions-}
```
public String toString(SaveOptions saveOptions)
```


Экспортирует содержимое узла в строку, используя указанные параметры сохранения.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions) | Указывает параметры, управляющие способом сохранения узла. |

**Возвращает:**
java.lang.String — содержимое узла в указанном формате.
### toString(int saveFormat) {#toString-int-}
```
public String toString(int saveFormat)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| saveFormat | int |  |

**Возвращает:**
java.lang.String
### unlinkFields() {#unlinkFields--}
```
public void unlinkFields()
```


Разъединяет поля во всем документе.

Заменяет все поля во всем документе их самыми последними результатами.

 Чтобы отменить связь полей в определенной части документа, используйте[Range.unlinkFields()](../../com.aspose.words/range\#unlinkFields--).

### unprotect() {#unprotect--}
```
public void unprotect()
```


Снимает защиту с документа. Снимает защиту с документа независимо от пароля.

Этот метод снимает защиту с документа, даже если он имеет пароль защиты.

 Обратите внимание, что защита документа отличается от защиты от записи. Защита от записи указывается с помощью[getWriteProtection()](../../com.aspose.words/document\#getWriteProtection--).

### unprotect(String password) {#unprotect-java.lang.String-}
```
public boolean unprotect(String password)
```


Снимает защиту с документа, если указан правильный пароль.

Этот метод снимает защиту с документа, только если указан правильный пароль.

 Обратите внимание, что защита документа отличается от защиты от записи. Защита от записи указывается с помощью[getWriteProtection()](../../com.aspose.words/document\#getWriteProtection--).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| password | java.lang.String | Пароль для снятия защиты с документа. |

**Возвращает:**
boolean - True, если был указан правильный пароль и документ не был защищен.
### updateFields() {#updateFields--}
```
public void updateFields()
```


Обновляет значения полей во всем документе.

Когда вы открываете, изменяете и затем сохраняете документ, Aspose.Words не обновляет поля автоматически, а сохраняет их нетронутыми. Таким образом, вы обычно хотите вызвать этот метод перед сохранением, если вы программно изменили документ и хотите убедиться, что в сохраненном документе отображаются правильные (вычисленные) значения полей.

Нет необходимости обновлять поля после выполнения слияния, потому что слияние — это своего рода обновление полей, которое автоматически обновляет все поля в документе.

Этот метод не обновляет все типы полей. Подробный список поддерживаемых типов полей см. в Руководстве программиста.

Этот метод не обновляет поля, связанные с алгоритмами макета страницы (например, PAGE, PAGES, PAGEREF). Поля, связанные с макетом страницы, обновляются при отображении документа или вызове[updatePageLayout()](../../com.aspose.words/document\#updatePageLayout--).

 Использовать[normalizeFieldTypes()](../../com.aspose.words/document\#normalizeFieldTypes--) перед обновлением полей, если в документе были изменения, влияющие на типы полей.

 Для обновления полей в определенной части документа используйте[Range.updateFields()](../../com.aspose.words/range\#updateFields--).

### updateListLabels() {#updateListLabels--}
```
public void updateListLabels()
```


Обновляет метки списка для всех элементов списка в документе.

 Этот метод обновляет свойства метки списка, такие как[ListLabel.getLabelValue()](../../com.aspose.words/listlabel\#getLabelValue--) а также[ListLabel.getLabelString()](../../com.aspose.words/listlabel\#getLabelString--) для каждого[Paragraph.getListLabel()](../../com.aspose.words/paragraph\#getListLabel--) объект в документе.

Также этот метод иногда неявно вызывается при обновлении полей в документе. Это необходимо, потому что некоторые поля, которые могут ссылаться на номера списка (такие как TOC или REF), требуют актуальности.

### updatePageLayout() {#updatePageLayout--}
```
public void updatePageLayout()
```


Восстанавливает макет страницы документа.

Этот метод форматирует документ в страницы и обновляет поля, связанные с номерами страниц в документе, такие как PAGE, PAGES, PAGEREF и REF. Актуальная информация о макете страницы требуется для правильного отображения документа в форматах с фиксированной страницей.

Этот метод вызывается автоматически, когда вы впервые конвертируете документ в PDF, XPS, изображение или печатаете его. Однако, если вы измените документ после рендеринга, а затем попытаетесь отобразить его снова, Aspose.Words не будет автоматически обновлять макет страницы. В этом случае следует позвонить[updatePageLayout()](../../com.aspose.words/document\#updatePageLayout--) перед повторным рендерингом.

### updateTableLayout() {#updateTableLayout--}
```
public void updateTableLayout()
```


Реализует более ранний подход к пересчету ширины столбцов таблицы, который имеет известные проблемы. Этот метод устарел и будет удален через несколько выпусков.

### updateThumbnail() {#updateThumbnail--}
```
public void updateThumbnail()
```


 Обновления[BuiltInDocumentProperties.getThumbnail()](../../com.aspose.words/builtindocumentproperties\#getThumbnail--) / [BuiltInDocumentProperties.setThumbnail(byte[])](../../com.aspose.words/builtindocumentproperties\#setThumbnail-byte---) документа с использованием параметров по умолчанию.

### updateThumbnail(ThumbnailGeneratingOptions options) {#updateThumbnail-com.aspose.words.ThumbnailGeneratingOptions-}
```
public void updateThumbnail(ThumbnailGeneratingOptions options)
```


 Обновления[BuiltInDocumentProperties.getThumbnail()](../../com.aspose.words/builtindocumentproperties\#getThumbnail--) / [BuiltInDocumentProperties.setThumbnail(byte[])](../../com.aspose.words/builtindocumentproperties\#setThumbnail-byte---) документа в соответствии с указанными параметрами.[ThumbnailGeneratingOptions](../../com.aspose.words/thumbnailgeneratingoptions) позволяет указать источник эскиза, размер и другие параметры. Если попытка создать миниатюру не удалась, не изменяет ее.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| options | [ThumbnailGeneratingOptions](../../com.aspose.words/thumbnailgeneratingoptions) | Используемые параметры генерации. |

### updateWordCount() {#updateWordCount--}
```
public void updateWordCount()
```


Обновляет свойства количества слов в документе.

**UpdateWordCount** пересчитывает и обновляет свойства символов, слов и абзацев в[getBuiltInDocumentProperties()](../../com.aspose.words/document\#getBuiltInDocumentProperties--) коллекция**Document**.

 Обратите внимание, что**UpdateWordCount** не обновляет количество строк и свойства страниц. Использовать[updateWordCount()](../../com.aspose.words/document\#updateWordCount--) перегрузите и передайте значение True в качестве параметра для этого.

При использовании ознакомительной версии водяной знак ознакомительной версии также будет включен в количество слов.

### updateWordCount(boolean updateLinesCount) {#updateWordCount-boolean-}
```
public void updateWordCount(boolean updateLinesCount)
```


 Обновляет свойства количества слов в документе, опционально обновляет[BuiltInDocumentProperties.getLines()](../../com.aspose.words/builtindocumentproperties\#getLines--) / [BuiltInDocumentProperties.setLines(int)](../../com.aspose.words/builtindocumentproperties\#setLines-int-) имущество. Этот метод перестроит макет страницы документа.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| updateLinesCount | boolean | Истинно, если количество строк в документе должно быть рассчитано. |

### wait() {#wait--}
```
public final void wait()
```




### wait(long arg0) {#wait-long-}
```
public final native void wait(long arg0)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int-}
```
public final void wait(long arg0, int arg1)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |
