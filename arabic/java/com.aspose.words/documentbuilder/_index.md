---
title: "DocumentBuilder"
linktitle: "DocumentBuilder"
second_title: "Aspose.Words لـ Java"
description: "يوفر طرقًا لإدراج النصوص والصور ومحتويات أخرى وتحديد تنسيق الخط والفقرات والأقسام في Java."
type: docs
weight: 163
url: /ar/java/com.aspose.words/documentbuilder/
---

**Inheritance:**
java.lang.Object
```
public class DocumentBuilder
```

يوفر طرقًا لإدراج النصوص والصور والمحتوى الآخر، وتحديد تنسيق الخط والفقرة والقسم.

للتعرف على المزيد، زر مقالة الوثائق [ Document Builder Overview ][Document Builder Overview].

 **Remarks:** 

[DocumentBuilder](../../com.aspose.words/documentbuilder/) makes the process of building a [Document](../../com.aspose.words/document/) easier. [Document](../../com.aspose.words/document/) is a composite object consisting of a tree of nodes and while inserting content nodes directly into the tree is possible, it requires good understanding of the tree structure. [DocumentBuilder](../../com.aspose.words/documentbuilder/) is a "facade" for the complex structure of [Document](../../com.aspose.words/document/) and allows to insert content and formatting quickly and easily.

أنشئ [DocumentBuilder](../../com.aspose.words/documentbuilder/) واربطه بـ [Document](../../com.aspose.words/document/).

يحتوي [DocumentBuilder](../../com.aspose.words/documentbuilder/) على مؤشر داخلي حيث سيتم إدراج النص عندما تستدعي [write(java.lang.String)](../../com.aspose.words/documentbuilder/\#write-java.lang.String)، [writeln(java.lang.String)](../../com.aspose.words/documentbuilder/\#writeln-java.lang.String)، **M:Aspose.Words.DocumentBuilder.InsertBreak(Aspose.Words.BreakType)** وغيرها من الطرق. يمكنك تحريك مؤشر [DocumentBuilder](../../com.aspose.words/documentbuilder/) إلى موقع مختلف في المستند باستخدام طرق MoveToXXX المختلفة.

استخدم الخاصية [getFont()](../../com.aspose.words/documentbuilder/\#getFont) لتحديد تنسيق الأحرف الذي سيُطبق على جميع النصوص المُدخلة من الموضع الحالي في المستند فصاعدًا.

استخدم الخاصية [getParagraphFormat()](../../com.aspose.words/documentbuilder/\#getParagraphFormat) لتحديد تنسيق الفقرات للفقرة الحالية وجميع الفقرات التي سيتم إدراجها.

استخدم الخاصية [getPageSetup()](../../com.aspose.words/documentbuilder/\#getPageSetup) لتحديد خصائص الصفحة والقسم للقسم الحالي وجميع الأقسام التي سيتم إدراجها.

استخدم الخصائص [getCellFormat()](../../com.aspose.words/documentbuilder/\#getCellFormat) و [getRowFormat()](../../com.aspose.words/documentbuilder/\#getRowFormat) لتحديد خصائص التنسيق لخلايا الجدول والصفوف. استخدم الطرق [insertCell()](../../com.aspose.words/documentbuilder/\#insertCell) و [endRow()](../../com.aspose.words/documentbuilder/\#endRow) لإنشاء جدول.

لاحظ أن الخصائص [getFont()](../../com.aspose.words/documentbuilder/\#getFont)، [getParagraphFormat()](../../com.aspose.words/documentbuilder/\#getParagraphFormat) و [getPageSetup()](../../com.aspose.words/documentbuilder/\#getPageSetup) يتم تحديثها كلما انتقلت إلى موقع مختلف في المستند لتعكس خصائص التنسيق المتاحة في الموقع الجديد.

 **Examples:** 

يوضح كيفية إنشاء رؤوس وتذييلات في المستند باستخدام DocumentBuilder.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Specify that we want different headers and footers for first, even and odd pages.
 builder.getPageSetup().setDifferentFirstPageHeaderFooter(true);
 builder.getPageSetup().setOddAndEvenPagesHeaderFooter(true);

 // Create the headers, then add three pages to the document to display each header type.
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_FIRST);
 builder.write("Header for the first page");
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_EVEN);
 builder.write("Header for even pages");
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 builder.write("Header for all other pages");

 builder.moveToSection(0);
 builder.writeln("Page1");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Page2");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Page3");

 doc.save(getArtifactsDir() + "DocumentBuilder.HeadersAndFooters.docx");
 
```

يوضح كيفية إنشاء جدول بحدود مخصصة.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.startTable();

 // Setting table formatting options for a document builder
 // will apply them to every row and cell that we add with it.
 builder.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);

 builder.getCellFormat().clearFormatting();
 builder.getCellFormat().setWidth(150.0);
 builder.getCellFormat().setVerticalAlignment(CellVerticalAlignment.CENTER);
 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.GREEN);
 builder.getCellFormat().setWrapText(false);
 builder.getCellFormat().setFitText(true);

 builder.getRowFormat().clearFormatting();
 builder.getRowFormat().setHeightRule(HeightRule.EXACTLY);
 builder.getRowFormat().setHeight(50.0);
 builder.getRowFormat().getBorders().setLineStyle(LineStyle.ENGRAVE_3_D);
 builder.getRowFormat().getBorders().setColor(Color.ORANGE);

 builder.insertCell();
 builder.write("Row 1, Col 1");

 builder.insertCell();
 builder.write("Row 1, Col 2");
 builder.endRow();

 // Changing the formatting will apply it to the current cell,
 // and any new cells that we create with the builder afterward.
 // This will not affect the cells that we have added previously.
 builder.getCellFormat().getShading().clearFormatting();

 builder.insertCell();
 builder.write("Row 2, Col 1");

 builder.insertCell();
 builder.write("Row 2, Col 2");

 builder.endRow();

 // Increase row height to fit the vertical text.
 builder.insertCell();
 builder.getRowFormat().setHeight(150.0);
 builder.getCellFormat().setOrientation(TextOrientation.UPWARD);
 builder.write("Row 3, Col 1");

 builder.insertCell();
 builder.getCellFormat().setOrientation(TextOrientation.DOWNWARD);
 builder.write("Row 3, Col 2");

 builder.endRow();
 builder.endTable();

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertTable.docx");
 
```

يوضح كيفية استخدام DocumentBuilder لإنشاء جدول.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Start the table, then populate the first row with two cells.
 builder.startTable();
 builder.insertCell();
 builder.write("Row 1, Cell 1.");
 builder.insertCell();
 builder.write("Row 1, Cell 2.");

 // Call the builder's "EndRow" method to start a new row.
 builder.endRow();
 builder.insertCell();
 builder.write("Row 2, Cell 1.");
 builder.insertCell();
 builder.write("Row 2, Cell 2.");
 builder.endTable();

 doc.save(getArtifactsDir() + "DocumentBuilder.CreateTable.docx");
 
```


[Document Builder Overview]: https://docs.aspose.com/words/java/document-builder-overview/
## المنشئات

| المنشئ | الوصف |
| --- | --- |
| [DocumentBuilder()](#DocumentBuilder) | يقوم بتهيئة نسخة جديدة من هذه الفئة. |
| [DocumentBuilder(DocumentBuilderOptions options)](#DocumentBuilder-com.aspose.words.DocumentBuilderOptions) | يقوم بتهيئة نسخة جديدة من هذه الفئة. |
| [DocumentBuilder(Document doc)](#DocumentBuilder-com.aspose.words.Document) | يقوم بتهيئة نسخة جديدة من هذه الفئة. |
| [DocumentBuilder(Document doc, DocumentBuilderOptions options)](#DocumentBuilder-com.aspose.words.Document-com.aspose.words.DocumentBuilderOptions) | يقوم بتهيئة نسخة جديدة من هذه الفئة. |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [clearCellAttrs()](#clearCellAttrs) |  |
| [clearParaAttrs()](#clearParaAttrs) |  |
| [clearRowAttrs()](#clearRowAttrs) |  |
| [clearRunAttrs()](#clearRunAttrs) |  |
| [deleteRow(int tableIndex, int rowIndex)](#deleteRow-int-int) | يحذف صفًا من جدول. |
| [endBookmark(String bookmarkName)](#endBookmark-java.lang.String) | يحدد الموضع الحالي في المستند كنهاية إشارة مرجعية. |
| [endColumnBookmark(String bookmarkName)](#endColumnBookmark-java.lang.String) | يحدد الموضع الحالي في المستند كنهاية إشارة مرجعية للعمود. |
| [endEditableRange()](#endEditableRange) | يحدد الموضع الحالي في المستند كنهاية نطاق قابل للتحرير. |
| [endEditableRange(EditableRangeStart start)](#endEditableRange-com.aspose.words.EditableRangeStart) | يحدد الموضع الحالي في المستند كنهاية نطاق قابل للتحرير. |
| [endRow()](#endRow) | ينهي صف جدول في المستند. |
| [endTable()](#endTable) | ينهي جدولًا في المستند. |
| [fetchCellAttr(int key)](#fetchCellAttr-int) |  |
| [fetchInheritedCellAttr(int key)](#fetchInheritedCellAttr-int) |  |
| [fetchInheritedParaAttr(int key)](#fetchInheritedParaAttr-int) |  |
| [fetchInheritedRowAttr(int key)](#fetchInheritedRowAttr-int) |  |
| [fetchInheritedRunAttr(int fontAttr)](#fetchInheritedRunAttr-int) |  |
| [fetchParaAttr(int key)](#fetchParaAttr-int) |  |
| [fetchRowAttr(int key)](#fetchRowAttr-int) |  |
| [getBold()](#getBold) | صحيح إذا كان الخط مُنسقًا كغامق. |
| [getCellFormat()](#getCellFormat) | يرجع كائنًا يمثل خصائص تنسيق خلية الجدول الحالية. |
| [getCurrentNode()](#getCurrentNode) | يحصل على العقدة المحددة حاليًا في هذا DocumentBuilder. |
| [getCurrentParagraph()](#getCurrentParagraph) | يحصل على الفقرة المحددة حاليًا في هذا [DocumentBuilder](../../com.aspose.words/documentbuilder/). |
| [getCurrentSection()](#getCurrentSection) | يحصل على القسم المحدد حاليًا في هذا [DocumentBuilder](../../com.aspose.words/documentbuilder/). |
| [getCurrentStory()](#getCurrentStory) | يحصل على القصة المحددة حاليًا في هذا [DocumentBuilder](../../com.aspose.words/documentbuilder/). |
| [getCurrentStructuredDocumentTag()](#getCurrentStructuredDocumentTag) | يحصل على علامة المستند المهيكلة المحددة حاليًا في هذا [DocumentBuilder](../../com.aspose.words/documentbuilder/). |
| [getDirectCellAttr(int key)](#getDirectCellAttr-int) |  |
| [getDirectParaAttr(int key)](#getDirectParaAttr-int) |  |
| [getDirectParaAttr(int key, int revisionsView)](#getDirectParaAttr-int-int) |  |
| [getDirectRowAttr(int key)](#getDirectRowAttr-int) |  |
| [getDirectRunAttr(int fontAttr)](#getDirectRunAttr-int) |  |
| [getDirectRunAttr(int key, int revisionsView)](#getDirectRunAttr-int-int) |  |
| [getDocument()](#getDocument) | يحصل على الكائن [getDocument()](../../com.aspose.words/documentbuilder/\#getDocument) / [setDocument(com.aspose.words.Document)](../../com.aspose.words/documentbuilder/\#setDocument-com.aspose.words.Document) الذي يرتبط به هذا الكائن. |
| [getFont()](#getFont) | يرجع كائنًا يمثل خصائص تنسيق الخط الحالية. |
| [getItalic()](#getItalic) | صحيح إذا كان الخط مُنسقًا كخط مائل. |
| [getListFormat()](#getListFormat) | إرجاع كائن يمثل خصائص تنسيق القائمة الحالية. |
| [getPageSetup()](#getPageSetup) | إرجاع كائن يمثل إعداد الصفحة الحالي وخصائص القسم. |
| [getParagraphFormat()](#getParagraphFormat) | إرجاع كائن يمثل خصائص تنسيق الفقرة الحالية. |
| [getRowFormat()](#getRowFormat) | إرجاع كائن يمثل خصائص تنسيق صف الجدول الحالي. |
| [getUnderline()](#getUnderline) | الحصول/تعيين نوع التسطير للخط الحالي. |
| [insertBreak(int breakType)](#insertBreak-int) |  |
| [insertCell()](#insertCell) | إدراج خلية جدول في المستند. |
| [insertChart(int chartType, double width, double height)](#insertChart-int-double-double) |  |
| [insertChart(int chartType, double width, double height, int chartStyle)](#insertChart-int-double-double-int) |  |
| [insertChart(int chartType, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType)](#insertChart-int-int-double-int-double-double-double-int) |  |
| [insertChart(int chartType, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType, int chartStyle)](#insertChart-int-int-double-int-double-double-double-int-int) |  |
| [insertCheckBox(String name, boolean defaultValue, boolean checkedValue, int size)](#insertCheckBox-java.lang.String-boolean-boolean-int) | إدراج حقل نموذج مربع اختيار في الموضع الحالي. |
| [insertCheckBox(String name, boolean checkedValue, int size)](#insertCheckBox-java.lang.String-boolean-int) | إدراج حقل نموذج مربع اختيار في الموضع الحالي. |
| [insertComboBox(String name, String[] items, int selectedIndex)](#insertComboBox-java.lang.String-java.lang.String---int) | إدراج حقل نموذج صندوق مركب في الموضع الحالي. |
| [insertDocument(Document srcDoc, int importFormatMode)](#insertDocument-com.aspose.words.Document-int) |  |
| [insertDocument(Document srcDoc, int importFormatMode, ImportFormatOptions importFormatOptions)](#insertDocument-com.aspose.words.Document-int-com.aspose.words.ImportFormatOptions) |  |
| [insertDocumentInline(Document srcDoc, int importFormatMode, ImportFormatOptions importFormatOptions)](#insertDocumentInline-com.aspose.words.Document-int-com.aspose.words.ImportFormatOptions) |  |
| [insertField(int fieldType, boolean updateField)](#insertField-int-boolean) |  |
| [insertField(String fieldCode)](#insertField-java.lang.String) | إدراج حقل Word في مستند وتحديث نتيجة الحقل. |
| [insertField(String fieldCode, String fieldValue)](#insertField-java.lang.String-java.lang.String) | إدراج حقل Word في مستند دون تحديث نتيجة الحقل. |
| [insertFootnote(int footnoteType, String footnoteText)](#insertFootnote-int-java.lang.String) |  |
| [insertFootnote(int footnoteType, String footnoteText, String referenceMark)](#insertFootnote-int-java.lang.String-java.lang.String) |  |
| [insertForms2OleControl(Forms2OleControl forms2OleControl)](#insertForms2OleControl-com.aspose.words.Forms2OleControl) | إدراج كائن [Forms2OleControl](../../com.aspose.words/forms2olecontrol/) في الموضع الحالي.. |
| [insertGroupShape(ShapeBase[] shapes)](#insertGroupShape-com.aspose.words.ShapeBase...) | تجميع الأشكال الممررة كمعامل في عقدة GroupShape جديدة يتم إدراجها في الموضع الحالي. |
| [insertGroupShape(double left, double top, double width, double height, ShapeBase[] shapes)](#insertGroupShape-double-double-double-double-com.aspose.words.ShapeBase...) | تجميع الأشكال الممررة كمعامل في عقدة GroupShape جديدة بالحجم المحدد يتم إدراجها في الموضع المحدد. |
| [insertHorizontalRule()](#insertHorizontalRule) | إدراج شكل قاعدة أفقية في المستند. |
| [insertHtml(String html)](#insertHtml-java.lang.String) | إدراج سلسلة HTML في المستند. |
| [insertHtml(String html, boolean useBuilderFormatting)](#insertHtml-java.lang.String-boolean) | إدراج سلسلة HTML في المستند. |
| [insertHtml(String html, int options)](#insertHtml-java.lang.String-int) |  |
| [insertHyperlink(String displayText, String urlOrBookmark, boolean isBookmark)](#insertHyperlink-java.lang.String-java.lang.String-boolean) | إدراج ارتباط تشعبي في المستند. |
| [insertImage(byte[] imageBytes)](#insertImage-byte) | إدراج صورة من مصفوفة بايت في المستند. |
| [insertImage(byte[] imageBytes, double width, double height)](#insertImage-byte---double-double) | إدراج صورة مدمجة من مصفوفة بايت في المستند وتغيير حجمها إلى الحجم المحدد. |
| [insertImage(byte[] imageBytes, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType)](#insertImage-byte---int-double-int-double-double-double-int) |  |
| [insertImage(BufferedImage image)](#insertImage-java.awt.image.BufferedImage) | إدراج صورة في المستند. |
| [insertImage(BufferedImage image, double width, double height)](#insertImage-java.awt.image.BufferedImage-double-double) | إدراج صورة مدمجة من كائن java.awt.image.BufferedImage في المستند وتغيير حجمها إلى الحجم المحدد. |
| [insertImage(BufferedImage image, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType)](#insertImage-java.awt.image.BufferedImage-int-double-int-double-double-double-int) |  |
| [insertImage(InputStream stream)](#insertImage-java.io.InputStream) |  |
| [insertImage(InputStream stream, double width, double height)](#insertImage-java.io.InputStream-double-double) |  |
| [insertImage(InputStream stream, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType)](#insertImage-java.io.InputStream-int-double-int-double-double-double-int) |  |
| [insertImage(String fileName)](#insertImage-java.lang.String) | إدراج صورة من ملف أو عنوان URL في المستند. |
| [insertImage(String fileName, double width, double height)](#insertImage-java.lang.String-double-double) | إدراج صورة مدمجة من ملف أو عنوان URL في المستند وتغيير حجمها إلى الحجم المحدد. |
| [insertImage(String fileName, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType)](#insertImage-java.lang.String-int-double-int-double-double-double-int) |  |
| [insertNode(Node node)](#insertNode-com.aspose.words.Node) | إدراج عقدة قبل المؤشر. |
| [insertOleObject(InputStream stream, String progId, boolean asIcon, InputStream presentation)](#insertOleObject-java.io.InputStream-java.lang.String-boolean-java.io.InputStream) |  |
| [insertOleObject(String fileName, boolean isLinked, boolean asIcon, InputStream presentation)](#insertOleObject-java.lang.String-boolean-boolean-java.io.InputStream) |  |
| [insertOleObject(String fileName, String progId, boolean isLinked, boolean asIcon, InputStream presentation)](#insertOleObject-java.lang.String-java.lang.String-boolean-boolean-java.io.InputStream) |  |
| [insertOleObjectAsIcon(InputStream stream, String progId, String iconFile, String iconCaption)](#insertOleObjectAsIcon-java.io.InputStream-java.lang.String-java.lang.String-java.lang.String) |  |
| [insertOleObjectAsIcon(String fileName, boolean isLinked, String iconFile, String iconCaption)](#insertOleObjectAsIcon-java.lang.String-boolean-java.lang.String-java.lang.String) | إدراج كائن OLE مدمج أو مرتبط كأيقونة في المستند. |
| [insertOleObjectAsIcon(String fileName, String progId, boolean isLinked, String iconFile, String iconCaption)](#insertOleObjectAsIcon-java.lang.String-java.lang.String-boolean-java.lang.String-java.lang.String) | إدراج كائن OLE مدمج أو مرتبط كأيقونة في المستند. |
| [insertOnlineVideo(String videoUrl, double width, double height)](#insertOnlineVideo-java.lang.String-double-double) | إدراج كائن فيديو عبر الإنترنت في المستند وتغيير حجمها إلى الحجم المحدد. |
| [insertOnlineVideo(String videoUrl, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType)](#insertOnlineVideo-java.lang.String-int-double-int-double-double-double-int) |  |
| [insertOnlineVideo(String videoUrl, String videoEmbedCode, byte[] thumbnailImageBytes, double width, double height)](#insertOnlineVideo-java.lang.String-java.lang.String-byte---double-double) | إدراج كائن فيديو عبر الإنترنت في المستند وتغيير حجمها إلى الحجم المحدد. |
| [insertOnlineVideo(String videoUrl, String videoEmbedCode, byte[] thumbnailImageBytes, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType)](#insertOnlineVideo-java.lang.String-java.lang.String-byte---int-double-int-double-double-double-int) |  |
| [insertParagraph()](#insertParagraph) | يدرج فاصل فقرة في المستند. |
| [insertShape(int shapeType, double width, double height)](#insertShape-int-double-double) |  |
| [insertShape(int shapeType, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType)](#insertShape-int-int-double-int-double-double-double-int) |  |
| [insertSignatureLine(SignatureLineOptions signatureLineOptions)](#insertSignatureLine-com.aspose.words.SignatureLineOptions) | يدرج سطر توقيع في الموضع الحالي. |
| [insertSignatureLine(SignatureLineOptions signatureLineOptions, int horzPos, double left, int vertPos, double top, int wrapType)](#insertSignatureLine-com.aspose.words.SignatureLineOptions-int-double-int-double-int) |  |
| [insertStructuredDocumentTag(int type)](#insertStructuredDocumentTag-int) |  |
| [insertStyleSeparator()](#insertStyleSeparator) | يدرج فاصل نمط في المستند. |
| [insertTableOfContents(String switches)](#insertTableOfContents-java.lang.String) | يدرج حقل فهرس (جدول المحتويات) في المستند. |
| [insertTextInput(String name, int type, String format, String fieldValue, int maxLength)](#insertTextInput-java.lang.String-int-java.lang.String-java.lang.String-int) |  |
| [isAtEndOfParagraph()](#isAtEndOfParagraph) | يرجع  true  إذا كان المؤشر في نهاية الفقرة الحالية. |
| [isAtEndOfStructuredDocumentTag()](#isAtEndOfStructuredDocumentTag) | يرجع **true** إذا كان المؤشر في نهاية علامة مستند منسقة. |
| [isAtStartOfParagraph()](#isAtStartOfParagraph) | يرجع  true  إذا كان المؤشر في بداية الفقرة الحالية (لا يوجد نص قبل المؤشر). |
| [moveTo(Node node)](#moveTo-com.aspose.words.Node) | ينقل المؤشر إلى عقدة مضمنة أو إلى نهاية الفقرة. |
| [moveToBookmark(String bookmarkName)](#moveToBookmark-java.lang.String) | ينقل المؤشر إلى إشارة مرجعية. |
| [moveToBookmark(String bookmarkName, boolean isStart, boolean isAfter)](#moveToBookmark-java.lang.String-boolean-boolean) | ينقل المؤشر إلى إشارة مرجعية بدقة أكبر. |
| [moveToCell(int tableIndex, int rowIndex, int columnIndex, int characterIndex)](#moveToCell-int-int-int-int) | ينقل المؤشر إلى خلية جدول في القسم الحالي. |
| [moveToDocumentEnd()](#moveToDocumentEnd) | ينقل المؤشر إلى نهاية المستند. |
| [moveToDocumentStart()](#moveToDocumentStart) | ينقل المؤشر إلى بداية المستند. |
| [moveToField(Field field, boolean isAfter)](#moveToField-com.aspose.words.Field-boolean) | ينقل المؤشر إلى حقل في المستند. |
| [moveToHeaderFooter(int headerFooterType)](#moveToHeaderFooter-int) |  |
| [moveToMergeField(String fieldName)](#moveToMergeField-java.lang.String) | ينقل المؤشر إلى حقل الدمج المحدد. |
| [moveToMergeField(String fieldName, boolean isAfter, boolean isDeleteField)](#moveToMergeField-java.lang.String-boolean-boolean) | ينقل حقل الدمج إلى حقل الدمج المحدد. |
| [moveToParagraph(int paragraphIndex, int characterIndex)](#moveToParagraph-int-int) | ينقل المؤشر إلى فقرة في القسم الحالي. |
| [moveToSection(int sectionIndex)](#moveToSection-int) | ينقل المؤشر إلى بداية الجسم في قسم محدد. |
| [moveToStructuredDocumentTag(StructuredDocumentTag structuredDocumentTag, int characterIndex)](#moveToStructuredDocumentTag-com.aspose.words.StructuredDocumentTag-int) | ينقل المؤشر إلى علامة المستند المنسقة. |
| [moveToStructuredDocumentTag(int structuredDocumentTagIndex, int characterIndex)](#moveToStructuredDocumentTag-int-int) | ينقل المؤشر إلى علامة مستند منسقة في القسم الحالي. |
| [popFont()](#popFont) | يسترجع تنسيق الأحرف الذي تم حفظه مسبقًا على المكدس. |
| [pushFont()](#pushFont) | يحفظ تنسيق الأحرف الحالي على المكدس. |
| [removeParaAttr(int key)](#removeParaAttr-int) |  |
| [removeRunAttr(int key)](#removeRunAttr-int) |  |
| [resetToDefaultAttrs()](#resetToDefaultAttrs) |  |
| [setBold(boolean value)](#setBold-boolean) | صحيح إذا كان الخط مُنسقًا كغامق. |
| [setCellAttr(int key, Object value)](#setCellAttr-int-java.lang.Object) |  |
| [setDocument(Document value)](#setDocument-com.aspose.words.Document) | يضبط الكائن [getDocument()](../../com.aspose.words/documentbuilder/\#getDocument) / [setDocument(com.aspose.words.Document)](../../com.aspose.words/documentbuilder/\#setDocument-com.aspose.words.Document) الذي يتم إرفاق هذا الكائن به. |
| [setItalic(boolean value)](#setItalic-boolean) | صحيح إذا كان الخط مُنسقًا كخط مائل. |
| [setParaAttr(int key, Object value)](#setParaAttr-int-java.lang.Object) |  |
| [setRowAttr(int key, Object value)](#setRowAttr-int-java.lang.Object) |  |
| [setRunAttr(int fontAttr, Object value)](#setRunAttr-int-java.lang.Object) |  |
| [setUnderline(int value)](#setUnderline-int) | الحصول/تعيين نوع التسطير للخط الحالي. |
| [startBookmark(String bookmarkName)](#startBookmark-java.lang.String) | يحدد الموضع الحالي في المستند كبداية إشارة مرجعية. |
| [startColumnBookmark(String bookmarkName)](#startColumnBookmark-java.lang.String) | يحدد الموضع الحالي في المستند كبداية إشارة مرجعية عمودية. |
| [startEditableRange()](#startEditableRange) | يحدد الموضع الحالي في المستند كبداية نطاق قابل للتحرير. |
| [startTable()](#startTable) | يبدأ جدولًا في المستند. |
| [write(String text)](#write-java.lang.String) | يدرج سلسلة نصية في المستند عند موضع الإدراج الحالي. |
| [writeln()](#writeln) | يدرج فاصل فقرة في المستند. |
| [writeln(String text)](#writeln-java.lang.String) | يدرج سلسلة نصية وفاصل فقرة في المستند. |
### DocumentBuilder() {#DocumentBuilder}
```
public DocumentBuilder()
```


يقوم بتهيئة نسخة جديدة من هذه الفئة.

 **Remarks:** 

ينشئ كائنًا جديدًا من [DocumentBuilder](../../com.aspose.words/documentbuilder/) ويربطه بكائن جديد من [Document](../../com.aspose.words/document/).

 **Examples:** 

يوضح كيفية إدراج نص منسق باستخدام DocumentBuilder.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Specify font formatting, then add text.
 Font font = builder.getFont();
 font.setSize(16.0);
 font.setBold(true);
 font.setColor(Color.BLUE);
 font.setName("Courier New");
 font.setUnderline(Underline.DASH);

 builder.write("Hello world!");
 
```

### DocumentBuilder(DocumentBuilderOptions options) {#DocumentBuilder-com.aspose.words.DocumentBuilderOptions}
```
public DocumentBuilder(DocumentBuilderOptions options)
```


يقوم بتهيئة نسخة جديدة من هذه الفئة.

 **Remarks:** 

ينشئ كائنًا جديدًا من [DocumentBuilder](../../com.aspose.words/documentbuilder/) ويربطه بكائن جديد من [Document](../../com.aspose.words/document/). يمكن تحديد خيارات إضافية لبناء المستند.

 **Examples:** 

يوضح كيفية تجاهل تنسيق الجدول للمحتوى بعد ذلك.

```

 Document doc = new Document();
 DocumentBuilderOptions builderOptions = new DocumentBuilderOptions();
 builderOptions.setContextTableFormatting(true);
 DocumentBuilder builder = new DocumentBuilder(doc, builderOptions);

 // Adds content before the table.
 // Default font size is 12.
 builder.writeln("Font size 12 here.");
 builder.startTable();
 builder.insertCell();
 // Changes the font size inside the table.
 builder.getFont().setSize(5.0);
 builder.write("Font size 5 here");
 builder.insertCell();
 builder.write("Font size 5 here");
 builder.endRow();
 builder.endTable();

 // If ContextTableFormatting is true, then table formatting isn't applied to the content after.
 // If ContextTableFormatting is false, then table formatting is applied to the content after.
 builder.writeln("Font size 12 here.");

 doc.save(getArtifactsDir() + "Table.ContextTableFormatting.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| options | [DocumentBuilderOptions](../../com.aspose.words/documentbuilderoptions/) |  |

### DocumentBuilder(Document doc) {#DocumentBuilder-com.aspose.words.Document}
```
public DocumentBuilder(Document doc)
```


يقوم بتهيئة نسخة جديدة من هذه الفئة.

 **Remarks:** 

ينشئ كائنًا جديدًا من [DocumentBuilder](../../com.aspose.words/documentbuilder/)، ويربطه بكائن [Document](../../com.aspose.words/document/) المحدد. يتم وضع المؤشر في بداية المستند.

 **Examples:** 

يوضح كيفية إنشاء رؤوس وتذييلات في المستند باستخدام DocumentBuilder.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Specify that we want different headers and footers for first, even and odd pages.
 builder.getPageSetup().setDifferentFirstPageHeaderFooter(true);
 builder.getPageSetup().setOddAndEvenPagesHeaderFooter(true);

 // Create the headers, then add three pages to the document to display each header type.
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_FIRST);
 builder.write("Header for the first page");
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_EVEN);
 builder.write("Header for even pages");
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 builder.write("Header for all other pages");

 builder.moveToSection(0);
 builder.writeln("Page1");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Page2");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Page3");

 doc.save(getArtifactsDir() + "DocumentBuilder.HeadersAndFooters.docx");
 
```

يوضح كيفية إدراج جدول محتويات (TOC) في المستند باستخدام أنماط العناوين كعناصر.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a table of contents for the first page of the document.
 // Configure the table to pick up paragraphs with headings of levels 1 to 3.
 // Also, set its entries to be hyperlinks that will take us
 // to the location of the heading when left-clicked in Microsoft Word.
 builder.insertTableOfContents("\\o \"1-3\" \\h \\z \\u");
 builder.insertBreak(BreakType.PAGE_BREAK);

 // Populate the table of contents by adding paragraphs with heading styles.
 // Each such heading with a level between 1 and 3 will create an entry in the table.
 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_1);
 builder.writeln("Heading 1");

 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_2);
 builder.writeln("Heading 1.1");
 builder.writeln("Heading 1.2");

 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_1);
 builder.writeln("Heading 2");
 builder.writeln("Heading 3");

 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_2);
 builder.writeln("Heading 3.1");

 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_3);
 builder.writeln("Heading 3.1.1");
 builder.writeln("Heading 3.1.2");
 builder.writeln("Heading 3.1.3");

 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_4);
 builder.writeln("Heading 3.1.3.1");
 builder.writeln("Heading 3.1.3.2");

 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_2);
 builder.writeln("Heading 3.2");
 builder.writeln("Heading 3.3");

 // A table of contents is a field of a type that needs to be updated to show an up-to-date result.
 doc.updateFields();
 doc.save(getArtifactsDir() + "DocumentBuilder.InsertToc.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| doc | [Document](../../com.aspose.words/document/) | كائن [Document](../../com.aspose.words/document/) المراد الارتباط به. |

### DocumentBuilder(Document doc, DocumentBuilderOptions options) {#DocumentBuilder-com.aspose.words.Document-com.aspose.words.DocumentBuilderOptions}
```
public DocumentBuilder(Document doc, DocumentBuilderOptions options)
```


يقوم بتهيئة نسخة جديدة من هذه الفئة.

 **Remarks:** 

ينشئ كائنًا جديدًا من [DocumentBuilder](../../com.aspose.words/documentbuilder/)، ويربطه بكائن [Document](../../com.aspose.words/document/) المحدد. يتم وضع المؤشر في بداية المستند.

 **Examples:** 

يوضح كيفية تجاهل تنسيق الجدول للمحتوى بعد ذلك.

```

 Document doc = new Document();
 DocumentBuilderOptions builderOptions = new DocumentBuilderOptions();
 builderOptions.setContextTableFormatting(true);
 DocumentBuilder builder = new DocumentBuilder(doc, builderOptions);

 // Adds content before the table.
 // Default font size is 12.
 builder.writeln("Font size 12 here.");
 builder.startTable();
 builder.insertCell();
 // Changes the font size inside the table.
 builder.getFont().setSize(5.0);
 builder.write("Font size 5 here");
 builder.insertCell();
 builder.write("Font size 5 here");
 builder.endRow();
 builder.endTable();

 // If ContextTableFormatting is true, then table formatting isn't applied to the content after.
 // If ContextTableFormatting is false, then table formatting is applied to the content after.
 builder.writeln("Font size 12 here.");

 doc.save(getArtifactsDir() + "Table.ContextTableFormatting.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| doc | [Document](../../com.aspose.words/document/) | كائن [Document](../../com.aspose.words/document/) المراد الارتباط به. |
| options | [DocumentBuilderOptions](../../com.aspose.words/documentbuilderoptions/) | خيارات إضافية لعملية بناء المستند. |

### clearCellAttrs() {#clearCellAttrs}
```
public void clearCellAttrs()
```




### clearParaAttrs() {#clearParaAttrs}
```
public void clearParaAttrs()
```




### clearRowAttrs() {#clearRowAttrs}
```
public void clearRowAttrs()
```




### clearRunAttrs() {#clearRunAttrs}
```
public void clearRunAttrs()
```




### deleteRow(int tableIndex, int rowIndex) {#deleteRow-int-int}
```
public Row deleteRow(int tableIndex, int rowIndex)
```


يحذف صفًا من جدول.

 **Remarks:** 

إذا كان المؤشر داخل الصف الذي يتم حذفه، يتم نقل المؤشر إلى الصف التالي أو إلى الفقرة التالية بعد الجدول.

إذا قمت بحذف صف من جدول يحتوي على صف واحد فقط، يتم حذف الجدول بالكامل.

بالنسبة لمعلمات الفهرس، عندما يكون الفهرس أكبر من أو يساوي 0، فإنه يحدد فهرسًا من البداية حيث 0 هو العنصر الأول. عندما يكون الفهرس أقل من 0، فإنه يحدد فهرسًا من النهاية حيث -1 هو العنصر الأخير.

 **Examples:** 

يوضح كيفية حذف صف من جدول.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Row 1, cell 1.");
 builder.insertCell();
 builder.write("Row 1, cell 2.");
 builder.endRow();
 builder.insertCell();
 builder.write("Row 2, cell 1.");
 builder.insertCell();
 builder.write("Row 2, cell 2.");
 builder.endTable();

 Assert.assertEquals(2, table.getRows().getCount());

 // Delete the first row of the first table in the document.
 builder.deleteRow(0, 0);

 Assert.assertEquals(1, table.getRows().getCount());
 Assert.assertEquals("Row 2, cell 1.Row 2, cell 2.", table.getText().trim());
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| tableIndex | int | فهرس الجدول. |
| rowIndex | int | فهرس الصف في الجدول. |

**Returns:**
[Row](../../com.aspose.words/row/) - The row node that was just removed.
### endBookmark(String bookmarkName) {#endBookmark-java.lang.String}
```
public BookmarkEnd endBookmark(String bookmarkName)
```


يحدد الموضع الحالي في المستند كنهاية إشارة مرجعية.

 **Remarks:** 

يمكن للعلامات المرجعية في المستند أن تتداخل وتغطي أي نطاق. لإنشاء علامة مرجعية صالحة تحتاج إلى استدعاء كل من [startBookmark(java.lang.String)](../../com.aspose.words/documentbuilder/\#startBookmark-java.lang.String) و [endBookmark(java.lang.String)](../../com.aspose.words/documentbuilder/\#endBookmark-java.lang.String) باستخدام نفس معامل  bookmarkName.

سيتم تجاهل العلامات المرجعية المشوهة أو العلامات المرجعية ذات الأسماء المكررة عند حفظ المستند.

 **Examples:** 

يوضح كيفية إنشاء علامة مرجعية.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // A valid bookmark needs to have document body text enclosed by
 // BookmarkStart and BookmarkEnd nodes created with a matching bookmark name.
 builder.startBookmark("MyBookmark");
 builder.writeln("Hello world!");
 builder.endBookmark("MyBookmark");

 Assert.assertEquals(1, doc.getRange().getBookmarks().getCount());
 Assert.assertEquals("MyBookmark", doc.getRange().getBookmarks().get(0).getName());
 Assert.assertEquals("Hello world!", doc.getRange().getBookmarks().get(0).getText().trim());
 
```

يوضح كيفية إدراج ارتباط تشعبي يشير إلى علامة مرجعية محلية.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.startBookmark("Bookmark1");
 builder.write("Bookmarked text. ");
 builder.endBookmark("Bookmark1");
 builder.writeln("Text outside of the bookmark.");

 // Insert a HYPERLINK field that links to the bookmark. We can pass field switches
 // to the "InsertHyperlink" method as part of the argument containing the referenced bookmark's name.
 builder.getFont().setColor(Color.BLUE);
 builder.getFont().setUnderline(Underline.SINGLE);
 FieldHyperlink hyperlink = (FieldHyperlink)builder.insertHyperlink("Link to Bookmark1", "Bookmark1", true);
 hyperlink.setScreenTip("Hyperlink Tip");

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertHyperlinkToLocalBookmark.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| bookmarkName | java.lang.String | اسم العلامة المرجعية. |

**Returns:**
[BookmarkEnd](../../com.aspose.words/bookmarkend/) - The bookmark end node that was just created.
### endColumnBookmark(String bookmarkName) {#endColumnBookmark-java.lang.String}
```
public BookmarkEnd endColumnBookmark(String bookmarkName)
```


يحدد الموضع الحالي في المستند كنهاية علامة مرجعية عمودية. يجب أن يكون الموضع داخل خلية جدول.

 **Remarks:** 

تغطي علامة مرجعية عمودية عمودًا أو أكثر في نطاق من الصفوف. لإنشاء علامة مرجعية صالحة تحتاج إلى استدعاء كل من [startColumnBookmark(java.lang.String)](../../com.aspose.words/documentbuilder/\#startColumnBookmark-java.lang.String) و [endColumnBookmark(java.lang.String)](../../com.aspose.words/documentbuilder/\#endColumnBookmark-java.lang.String) باستخدام نفس معامل  bookmarkName.

سيتم تجاهل العلامات المرجعية المشوهة أو العلامات المرجعية ذات الأسماء المكررة عند حفظ المستند.

الموقع الفعلي للعقدة [BookmarkEnd](../../com.aspose.words/bookmarkend/) التي تم إدراجها قد يختلف عن موقع منشئ المستند الحالي.

 **Examples:** 

يعرض كيفية إنشاء إشارة مرجعية للعمود.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.startTable();

 builder.insertCell();
 // Cells 1,2,4,5 will be bookmarked.
 builder.startColumnBookmark("MyBookmark_1");
 // Badly formed bookmarks or bookmarks with duplicate names will be ignored when the document is saved.
 builder.startColumnBookmark("MyBookmark_1");
 builder.startColumnBookmark("BadStartBookmark");
 builder.write("Cell 1");

 builder.insertCell();
 builder.write("Cell 2");

 builder.insertCell();
 builder.write("Cell 3");

 builder.endRow();

 builder.insertCell();
 builder.write("Cell 4");

 builder.insertCell();
 builder.write("Cell 5");
 builder.endColumnBookmark("MyBookmark_1");
 builder.endColumnBookmark("MyBookmark_1");

 builder.insertCell();
 builder.write("Cell 6");

 builder.endRow();
 builder.endTable();

 doc.save(getArtifactsDir() + "Bookmarks.CreateColumnBookmark.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| bookmarkName | java.lang.String | اسم العلامة المرجعية. |

**Returns:**
[BookmarkEnd](../../com.aspose.words/bookmarkend/) - The bookmark end node that was just created.
### endEditableRange() {#endEditableRange}
```
public EditableRangeEnd endEditableRange()
```


يحدد الموضع الحالي في المستند كنهاية نطاق قابل للتحرير.

 **Remarks:** 

يمكن أن يتداخل النطاق القابل للتحرير في المستند ويمتد عبر أي نطاق. لإنشاء نطاق قابل للتحرير صالح تحتاج إلى استدعاء كل من [startEditableRange()](../../com.aspose.words/documentbuilder/\#startEditableRange) و [endEditableRange()](../../com.aspose.words/documentbuilder/\#endEditableRange) أو طريقة [endEditableRange(com.aspose.words.EditableRangeStart)](../../com.aspose.words/documentbuilder/\#endEditableRange-com.aspose.words.EditableRangeStart).

سيتم تجاهل النطاق القابل للتحرير غير المشكل بشكل صحيح عند حفظ المستند.

 **Examples:** 

يوضح كيفية العمل مع نطاق قابل للتحرير.

```

 Document doc = new Document();
 doc.protect(ProtectionType.READ_ONLY, "MyPassword");

 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world! Since we have set the document's protection level to read-only," +
         " we cannot edit this paragraph without the password.");

 // Editable ranges allow us to leave parts of protected documents open for editing.
 EditableRangeStart editableRangeStart = builder.startEditableRange();
 builder.writeln("This paragraph is inside an editable range, and can be edited.");
 EditableRangeEnd editableRangeEnd = builder.endEditableRange();

 // A well-formed editable range has a start node, and end node.
 // These nodes have matching IDs and encompass editable nodes.
 EditableRange editableRange = editableRangeStart.getEditableRange();

 Assert.assertEquals(editableRangeStart.getId(), editableRange.getId());
 Assert.assertEquals(editableRangeEnd.getId(), editableRange.getId());

 // Different parts of the editable range link to each other.
 Assert.assertEquals(editableRangeStart.getId(), editableRange.getEditableRangeStart().getId());
 Assert.assertEquals(editableRangeStart.getId(), editableRangeEnd.getEditableRangeStart().getId());
 Assert.assertEquals(editableRange.getId(), editableRangeStart.getEditableRange().getId());
 Assert.assertEquals(editableRangeEnd.getId(), editableRange.getEditableRangeEnd().getId());

 // We can access the node types of each part like this. The editable range itself is not a node,
 // but an entity which consists of a start, an end, and their enclosed contents.
 Assert.assertEquals(NodeType.EDITABLE_RANGE_START, editableRangeStart.getNodeType());
 Assert.assertEquals(NodeType.EDITABLE_RANGE_END, editableRangeEnd.getNodeType());

 builder.writeln("This paragraph is outside the editable range, and cannot be edited.");

 doc.save(getArtifactsDir() + "EditableRange.CreateAndRemove.docx");

 // Remove an editable range. All the nodes that were inside the range will remain intact.
 editableRange.remove();
 
```

**Returns:**
[EditableRangeEnd](../../com.aspose.words/editablerangeend/) - The editable range end node that was just created.
### endEditableRange(EditableRangeStart start) {#endEditableRange-com.aspose.words.EditableRangeStart}
```
public EditableRangeEnd endEditableRange(EditableRangeStart start)
```


يحدد الموضع الحالي في المستند كنهاية نطاق قابل للتحرير.

 **Remarks:** 

استخدم هذا التحميل الزائد أثناء إنشاء نطاقات تحرير متداخلة.

يمكن أن يتداخل النطاق القابل للتحرير في المستند ويمتد عبر أي نطاق. لإنشاء نطاق قابل للتحرير صالح تحتاج إلى استدعاء كل من [startEditableRange()](../../com.aspose.words/documentbuilder/\#startEditableRange) و [endEditableRange()](../../com.aspose.words/documentbuilder/\#endEditableRange) أو طريقة [endEditableRange(com.aspose.words.EditableRangeStart)](../../com.aspose.words/documentbuilder/\#endEditableRange-com.aspose.words.EditableRangeStart).

سيتم تجاهل النطاق القابل للتحرير غير المشكل بشكل صحيح عند حفظ المستند.

 **Examples:** 

يوضح كيفية إنشاء نطاقات قابلة للتحرير متداخلة.

```

 Document doc = new Document();
 doc.protect(ProtectionType.READ_ONLY, "MyPassword");

 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world! Since we have set the document's protection level to read-only, " +
         "we cannot edit this paragraph without the password.");

 // Create two nested editable ranges.
 EditableRangeStart outerEditableRangeStart = builder.startEditableRange();
 builder.writeln("This paragraph inside the outer editable range and can be edited.");

 EditableRangeStart innerEditableRangeStart = builder.startEditableRange();
 builder.writeln("This paragraph inside both the outer and inner editable ranges and can be edited.");

 // Currently, the document builder's node insertion cursor is in more than one ongoing editable range.
 // When we want to end an editable range in this situation,
 // we need to specify which of the ranges we wish to end by passing its EditableRangeStart node.
 builder.endEditableRange(innerEditableRangeStart);

 builder.writeln("This paragraph inside the outer editable range and can be edited.");

 builder.endEditableRange(outerEditableRangeStart);

 builder.writeln("This paragraph is outside any editable ranges, and cannot be edited.");

 // If a region of text has two overlapping editable ranges with specified groups,
 // the combined group of users excluded by both groups are prevented from editing it.
 outerEditableRangeStart.getEditableRange().setEditorGroup(EditorType.EVERYONE);
 innerEditableRangeStart.getEditableRange().setEditorGroup(EditorType.CONTRIBUTORS);

 doc.save(getArtifactsDir() + "EditableRange.Nested.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| start | [EditableRangeStart](../../com.aspose.words/editablerangestart/) | بداية هذا النطاق القابل للتحرير. |

**Returns:**
[EditableRangeEnd](../../com.aspose.words/editablerangeend/) - The editable range end node that was just created.
### endRow() {#endRow}
```
public Row endRow()
```


ينهي صف جدول في المستند.

 **Remarks:** 

استدعِ [endRow()](../../com.aspose.words/documentbuilder/\#endRow) لإنهاء صف جدول. إذا استدعيت [insertCell()](../../com.aspose.words/documentbuilder/\#insertCell) مباشرةً بعد ذلك، فإن الجدول سيستمر في صف جديد.

استخدم الخاصية [getRowFormat()](../../com.aspose.words/documentbuilder/\#getRowFormat) لتحديد تنسيق الصف.

 **Examples:** 

يعرض كيفية دمج خلايا الجدول عموديًا.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a cell into the first column of the first row.
 // This cell will be the first in a range of vertically merged cells.
 builder.insertCell();
 builder.getCellFormat().setVerticalMerge(CellMerge.FIRST);
 builder.write("Text in merged cells.");

 // Insert a cell into the second column of the first row, then end the row.
 // Also, configure the builder to disable vertical merging in created cells.
 builder.insertCell();
 builder.getCellFormat().setVerticalMerge(CellMerge.NONE);
 builder.write("Text in unmerged cell.");
 builder.endRow();

 // Insert a cell into the first column of the second row.
 // Instead of adding text contents, we will merge this cell with the first cell that we added directly above.
 builder.insertCell();
 builder.getCellFormat().setVerticalMerge(CellMerge.PREVIOUS);

 // Insert another independent cell in the second column of the second row.
 builder.insertCell();
 builder.getCellFormat().setVerticalMerge(CellMerge.NONE);
 builder.write("Text in unmerged cell.");
 builder.endRow();
 builder.endTable();

 doc.save(getArtifactsDir() + "CellFormat.VerticalMerge.docx");
 
```

يوضح كيفية إنشاء جدول بحدود مخصصة.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.startTable();

 // Setting table formatting options for a document builder
 // will apply them to every row and cell that we add with it.
 builder.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);

 builder.getCellFormat().clearFormatting();
 builder.getCellFormat().setWidth(150.0);
 builder.getCellFormat().setVerticalAlignment(CellVerticalAlignment.CENTER);
 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.GREEN);
 builder.getCellFormat().setWrapText(false);
 builder.getCellFormat().setFitText(true);

 builder.getRowFormat().clearFormatting();
 builder.getRowFormat().setHeightRule(HeightRule.EXACTLY);
 builder.getRowFormat().setHeight(50.0);
 builder.getRowFormat().getBorders().setLineStyle(LineStyle.ENGRAVE_3_D);
 builder.getRowFormat().getBorders().setColor(Color.ORANGE);

 builder.insertCell();
 builder.write("Row 1, Col 1");

 builder.insertCell();
 builder.write("Row 1, Col 2");
 builder.endRow();

 // Changing the formatting will apply it to the current cell,
 // and any new cells that we create with the builder afterward.
 // This will not affect the cells that we have added previously.
 builder.getCellFormat().getShading().clearFormatting();

 builder.insertCell();
 builder.write("Row 2, Col 1");

 builder.insertCell();
 builder.write("Row 2, Col 2");

 builder.endRow();

 // Increase row height to fit the vertical text.
 builder.insertCell();
 builder.getRowFormat().setHeight(150.0);
 builder.getCellFormat().setOrientation(TextOrientation.UPWARD);
 builder.write("Row 3, Col 1");

 builder.insertCell();
 builder.getCellFormat().setOrientation(TextOrientation.DOWNWARD);
 builder.write("Row 3, Col 2");

 builder.endRow();
 builder.endTable();

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertTable.docx");
 
```

يعرض كيفية إنشاء جدول 2x2 منسق.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.getCellFormat().setVerticalAlignment(CellVerticalAlignment.CENTER);
 builder.write("Row 1, cell 1.");
 builder.insertCell();
 builder.write("Row 1, cell 2.");
 builder.endRow();

 // While building the table, the document builder will apply its current RowFormat/CellFormat property values
 // to the current row/cell that its cursor is in and any new rows/cells as it creates them.
 Assert.assertEquals(CellVerticalAlignment.CENTER, table.getRows().get(0).getCells().get(0).getCellFormat().getVerticalAlignment());
 Assert.assertEquals(CellVerticalAlignment.CENTER, table.getRows().get(0).getCells().get(1).getCellFormat().getVerticalAlignment());

 builder.insertCell();
 builder.getRowFormat().setHeight(100.0);
 builder.getRowFormat().setHeightRule(HeightRule.EXACTLY);
 builder.getCellFormat().setOrientation(TextOrientation.UPWARD);
 builder.write("Row 2, cell 1.");
 builder.insertCell();
 builder.getCellFormat().setOrientation(TextOrientation.DOWNWARD);
 builder.write("Row 2, cell 2.");
 builder.endRow();
 builder.endTable();

 // Previously added rows and cells are not retroactively affected by changes to the builder's formatting.
 Assert.assertEquals(0.0, table.getRows().get(0).getRowFormat().getHeight());
 Assert.assertEquals(HeightRule.AUTO, table.getRows().get(0).getRowFormat().getHeightRule());
 Assert.assertEquals(100.0, table.getRows().get(1).getRowFormat().getHeight());
 Assert.assertEquals(HeightRule.EXACTLY, table.getRows().get(1).getRowFormat().getHeightRule());
 Assert.assertEquals(TextOrientation.UPWARD, table.getRows().get(1).getCells().get(0).getCellFormat().getOrientation());
 Assert.assertEquals(TextOrientation.DOWNWARD, table.getRows().get(1).getCells().get(1).getCellFormat().getOrientation());

 doc.save(getArtifactsDir() + "DocumentBuilder.BuildTable.docx");
 
```

**Returns:**
[Row](../../com.aspose.words/row/) - The row node that was just finished.
### endTable() {#endTable}
```
public Table endTable()
```


ينهي جدولًا في المستند.

 **Remarks:** 

يجب استدعاء هذه الطريقة مرة واحدة فقط بعد استدعاء [endRow()](../../com.aspose.words/documentbuilder/\#endRow). عند الاستدعاء، تقوم [endTable()](../../com.aspose.words/documentbuilder/\#endTable) بنقل المؤشر خارج الخلية الحالية لتشير مباشرةً بعد الجدول.

 **Examples:** 

يوضح كيفية إنشاء جدول بحدود مخصصة.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.startTable();

 // Setting table formatting options for a document builder
 // will apply them to every row and cell that we add with it.
 builder.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);

 builder.getCellFormat().clearFormatting();
 builder.getCellFormat().setWidth(150.0);
 builder.getCellFormat().setVerticalAlignment(CellVerticalAlignment.CENTER);
 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.GREEN);
 builder.getCellFormat().setWrapText(false);
 builder.getCellFormat().setFitText(true);

 builder.getRowFormat().clearFormatting();
 builder.getRowFormat().setHeightRule(HeightRule.EXACTLY);
 builder.getRowFormat().setHeight(50.0);
 builder.getRowFormat().getBorders().setLineStyle(LineStyle.ENGRAVE_3_D);
 builder.getRowFormat().getBorders().setColor(Color.ORANGE);

 builder.insertCell();
 builder.write("Row 1, Col 1");

 builder.insertCell();
 builder.write("Row 1, Col 2");
 builder.endRow();

 // Changing the formatting will apply it to the current cell,
 // and any new cells that we create with the builder afterward.
 // This will not affect the cells that we have added previously.
 builder.getCellFormat().getShading().clearFormatting();

 builder.insertCell();
 builder.write("Row 2, Col 1");

 builder.insertCell();
 builder.write("Row 2, Col 2");

 builder.endRow();

 // Increase row height to fit the vertical text.
 builder.insertCell();
 builder.getRowFormat().setHeight(150.0);
 builder.getCellFormat().setOrientation(TextOrientation.UPWARD);
 builder.write("Row 3, Col 1");

 builder.insertCell();
 builder.getCellFormat().setOrientation(TextOrientation.DOWNWARD);
 builder.write("Row 3, Col 2");

 builder.endRow();
 builder.endTable();

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertTable.docx");
 
```

يعرض كيفية إنشاء جدول 2x2 منسق.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.getCellFormat().setVerticalAlignment(CellVerticalAlignment.CENTER);
 builder.write("Row 1, cell 1.");
 builder.insertCell();
 builder.write("Row 1, cell 2.");
 builder.endRow();

 // While building the table, the document builder will apply its current RowFormat/CellFormat property values
 // to the current row/cell that its cursor is in and any new rows/cells as it creates them.
 Assert.assertEquals(CellVerticalAlignment.CENTER, table.getRows().get(0).getCells().get(0).getCellFormat().getVerticalAlignment());
 Assert.assertEquals(CellVerticalAlignment.CENTER, table.getRows().get(0).getCells().get(1).getCellFormat().getVerticalAlignment());

 builder.insertCell();
 builder.getRowFormat().setHeight(100.0);
 builder.getRowFormat().setHeightRule(HeightRule.EXACTLY);
 builder.getCellFormat().setOrientation(TextOrientation.UPWARD);
 builder.write("Row 2, cell 1.");
 builder.insertCell();
 builder.getCellFormat().setOrientation(TextOrientation.DOWNWARD);
 builder.write("Row 2, cell 2.");
 builder.endRow();
 builder.endTable();

 // Previously added rows and cells are not retroactively affected by changes to the builder's formatting.
 Assert.assertEquals(0.0, table.getRows().get(0).getRowFormat().getHeight());
 Assert.assertEquals(HeightRule.AUTO, table.getRows().get(0).getRowFormat().getHeightRule());
 Assert.assertEquals(100.0, table.getRows().get(1).getRowFormat().getHeight());
 Assert.assertEquals(HeightRule.EXACTLY, table.getRows().get(1).getRowFormat().getHeightRule());
 Assert.assertEquals(TextOrientation.UPWARD, table.getRows().get(1).getCells().get(0).getCellFormat().getOrientation());
 Assert.assertEquals(TextOrientation.DOWNWARD, table.getRows().get(1).getCells().get(1).getCellFormat().getOrientation());

 doc.save(getArtifactsDir() + "DocumentBuilder.BuildTable.docx");
 
```

يعرض كيفية تنسيق الخلايا باستخدام منشئ المستند.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Row 1, cell 1.");

 // Insert a second cell, and then configure cell text padding options.
 // The builder will apply these settings at its current cell, and any new cells creates afterwards.
 builder.insertCell();

 CellFormat cellFormat = builder.getCellFormat();
 cellFormat.setWidth(250.0);
 cellFormat.setLeftPadding(30.0);
 cellFormat.setRightPadding(30.0);
 cellFormat.setTopPadding(30.0);
 cellFormat.setBottomPadding(30.0);

 builder.write("Row 1, cell 2.");
 builder.endRow();
 builder.endTable();

 // The first cell was unaffected by the padding reconfiguration, and still holds the default values.
 Assert.assertEquals(0.0d, table.getFirstRow().getCells().get(0).getCellFormat().getWidth());
 Assert.assertEquals(5.4d, table.getFirstRow().getCells().get(0).getCellFormat().getLeftPadding());
 Assert.assertEquals(5.4d, table.getFirstRow().getCells().get(0).getCellFormat().getRightPadding());
 Assert.assertEquals(0.0d, table.getFirstRow().getCells().get(0).getCellFormat().getTopPadding());
 Assert.assertEquals(0.0d, table.getFirstRow().getCells().get(0).getCellFormat().getBottomPadding());

 Assert.assertEquals(250.0d, table.getFirstRow().getCells().get(1).getCellFormat().getWidth());
 Assert.assertEquals(30.0d, table.getFirstRow().getCells().get(1).getCellFormat().getLeftPadding());
 Assert.assertEquals(30.0d, table.getFirstRow().getCells().get(1).getCellFormat().getRightPadding());
 Assert.assertEquals(30.0d, table.getFirstRow().getCells().get(1).getCellFormat().getTopPadding());
 Assert.assertEquals(30.0d, table.getFirstRow().getCells().get(1).getCellFormat().getBottomPadding());

 // The first cell will still grow in the output document to match the size of its neighboring cell.
 doc.save(getArtifactsDir() + "DocumentBuilder.SetCellFormatting.docx");
 
```

**Returns:**
[Table](../../com.aspose.words/table/) - The table node that was just finished.
### fetchCellAttr(int key) {#fetchCellAttr-int}
```
public Object fetchCellAttr(int key)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### fetchInheritedCellAttr(int key) {#fetchInheritedCellAttr-int}
```
public Object fetchInheritedCellAttr(int key)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### fetchInheritedParaAttr(int key) {#fetchInheritedParaAttr-int}
```
public Object fetchInheritedParaAttr(int key)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### fetchInheritedRowAttr(int key) {#fetchInheritedRowAttr-int}
```
public Object fetchInheritedRowAttr(int key)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### fetchInheritedRunAttr(int fontAttr) {#fetchInheritedRunAttr-int}
```
public Object fetchInheritedRunAttr(int fontAttr)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| fontAttr | int |  |

**Returns:**
java.lang.Object
### fetchParaAttr(int key) {#fetchParaAttr-int}
```
public Object fetchParaAttr(int key)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### fetchRowAttr(int key) {#fetchRowAttr-int}
```
public Object fetchRowAttr(int key)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### getBold() {#getBold}
```
public boolean getBold()
```


صحيح إذا كان الخط مُنسقًا كغامق.

 **Examples:** 

يعرض كيفية ملء حقول MERGEFIELD بالبيانات باستخدام منشئ المستند بدلاً من دمج البريد.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert some MERGEFIELDS, which accept data from columns of the same name in a data source during a mail merge,
 // and then fill them manually.
 builder.insertField(" MERGEFIELD Chairman ");
 builder.insertField(" MERGEFIELD ChiefFinancialOfficer ");
 builder.insertField(" MERGEFIELD ChiefTechnologyOfficer ");

 builder.moveToMergeField("Chairman");
 builder.setBold(true);
 builder.writeln("John Doe");

 builder.moveToMergeField("ChiefFinancialOfficer");
 builder.setItalic(true);
 builder.writeln("Jane Doe");

 builder.moveToMergeField("ChiefTechnologyOfficer");
 builder.setItalic(true);
 builder.writeln("John Bloggs");

 doc.save(getArtifactsDir() + "DocumentBuilder.FillMergeFields.docx");
 
```

**Returns:**
boolean - القيمة المنطقية المقابلة.
### getCellFormat() {#getCellFormat}
```
public CellFormat getCellFormat()
```


يرجع كائنًا يمثل خصائص تنسيق خلية الجدول الحالية.

 **Examples:** 

يوضح كيفية إنشاء جدول بحدود مخصصة.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.startTable();

 // Setting table formatting options for a document builder
 // will apply them to every row and cell that we add with it.
 builder.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);

 builder.getCellFormat().clearFormatting();
 builder.getCellFormat().setWidth(150.0);
 builder.getCellFormat().setVerticalAlignment(CellVerticalAlignment.CENTER);
 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.GREEN);
 builder.getCellFormat().setWrapText(false);
 builder.getCellFormat().setFitText(true);

 builder.getRowFormat().clearFormatting();
 builder.getRowFormat().setHeightRule(HeightRule.EXACTLY);
 builder.getRowFormat().setHeight(50.0);
 builder.getRowFormat().getBorders().setLineStyle(LineStyle.ENGRAVE_3_D);
 builder.getRowFormat().getBorders().setColor(Color.ORANGE);

 builder.insertCell();
 builder.write("Row 1, Col 1");

 builder.insertCell();
 builder.write("Row 1, Col 2");
 builder.endRow();

 // Changing the formatting will apply it to the current cell,
 // and any new cells that we create with the builder afterward.
 // This will not affect the cells that we have added previously.
 builder.getCellFormat().getShading().clearFormatting();

 builder.insertCell();
 builder.write("Row 2, Col 1");

 builder.insertCell();
 builder.write("Row 2, Col 2");

 builder.endRow();

 // Increase row height to fit the vertical text.
 builder.insertCell();
 builder.getRowFormat().setHeight(150.0);
 builder.getCellFormat().setOrientation(TextOrientation.UPWARD);
 builder.write("Row 3, Col 1");

 builder.insertCell();
 builder.getCellFormat().setOrientation(TextOrientation.DOWNWARD);
 builder.write("Row 3, Col 2");

 builder.endRow();
 builder.endTable();

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertTable.docx");
 
```

يعرض كيفية إنشاء جدول 2x2 منسق.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.getCellFormat().setVerticalAlignment(CellVerticalAlignment.CENTER);
 builder.write("Row 1, cell 1.");
 builder.insertCell();
 builder.write("Row 1, cell 2.");
 builder.endRow();

 // While building the table, the document builder will apply its current RowFormat/CellFormat property values
 // to the current row/cell that its cursor is in and any new rows/cells as it creates them.
 Assert.assertEquals(CellVerticalAlignment.CENTER, table.getRows().get(0).getCells().get(0).getCellFormat().getVerticalAlignment());
 Assert.assertEquals(CellVerticalAlignment.CENTER, table.getRows().get(0).getCells().get(1).getCellFormat().getVerticalAlignment());

 builder.insertCell();
 builder.getRowFormat().setHeight(100.0);
 builder.getRowFormat().setHeightRule(HeightRule.EXACTLY);
 builder.getCellFormat().setOrientation(TextOrientation.UPWARD);
 builder.write("Row 2, cell 1.");
 builder.insertCell();
 builder.getCellFormat().setOrientation(TextOrientation.DOWNWARD);
 builder.write("Row 2, cell 2.");
 builder.endRow();
 builder.endTable();

 // Previously added rows and cells are not retroactively affected by changes to the builder's formatting.
 Assert.assertEquals(0.0, table.getRows().get(0).getRowFormat().getHeight());
 Assert.assertEquals(HeightRule.AUTO, table.getRows().get(0).getRowFormat().getHeightRule());
 Assert.assertEquals(100.0, table.getRows().get(1).getRowFormat().getHeight());
 Assert.assertEquals(HeightRule.EXACTLY, table.getRows().get(1).getRowFormat().getHeightRule());
 Assert.assertEquals(TextOrientation.UPWARD, table.getRows().get(1).getCells().get(0).getCellFormat().getOrientation());
 Assert.assertEquals(TextOrientation.DOWNWARD, table.getRows().get(1).getCells().get(1).getCellFormat().getOrientation());

 doc.save(getArtifactsDir() + "DocumentBuilder.BuildTable.docx");
 
```

يعرض كيفية تنسيق الخلايا باستخدام منشئ المستند.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Row 1, cell 1.");

 // Insert a second cell, and then configure cell text padding options.
 // The builder will apply these settings at its current cell, and any new cells creates afterwards.
 builder.insertCell();

 CellFormat cellFormat = builder.getCellFormat();
 cellFormat.setWidth(250.0);
 cellFormat.setLeftPadding(30.0);
 cellFormat.setRightPadding(30.0);
 cellFormat.setTopPadding(30.0);
 cellFormat.setBottomPadding(30.0);

 builder.write("Row 1, cell 2.");
 builder.endRow();
 builder.endTable();

 // The first cell was unaffected by the padding reconfiguration, and still holds the default values.
 Assert.assertEquals(0.0d, table.getFirstRow().getCells().get(0).getCellFormat().getWidth());
 Assert.assertEquals(5.4d, table.getFirstRow().getCells().get(0).getCellFormat().getLeftPadding());
 Assert.assertEquals(5.4d, table.getFirstRow().getCells().get(0).getCellFormat().getRightPadding());
 Assert.assertEquals(0.0d, table.getFirstRow().getCells().get(0).getCellFormat().getTopPadding());
 Assert.assertEquals(0.0d, table.getFirstRow().getCells().get(0).getCellFormat().getBottomPadding());

 Assert.assertEquals(250.0d, table.getFirstRow().getCells().get(1).getCellFormat().getWidth());
 Assert.assertEquals(30.0d, table.getFirstRow().getCells().get(1).getCellFormat().getLeftPadding());
 Assert.assertEquals(30.0d, table.getFirstRow().getCells().get(1).getCellFormat().getRightPadding());
 Assert.assertEquals(30.0d, table.getFirstRow().getCells().get(1).getCellFormat().getTopPadding());
 Assert.assertEquals(30.0d, table.getFirstRow().getCells().get(1).getCellFormat().getBottomPadding());

 // The first cell will still grow in the output document to match the size of its neighboring cell.
 doc.save(getArtifactsDir() + "DocumentBuilder.SetCellFormatting.docx");
 
```

**Returns:**
[CellFormat](../../com.aspose.words/cellformat/) - An object that represents current table cell formatting properties.
### getCurrentNode() {#getCurrentNode}
```
public Node getCurrentNode()
```


يحصل على العقدة المحددة حاليًا في هذا DocumentBuilder.

 **Remarks:** 

[getCurrentNode()](../../com.aspose.words/documentbuilder/\#getCurrentNode) is a cursor of [DocumentBuilder](../../com.aspose.words/documentbuilder/) and points to a [Node](../../com.aspose.words/node/) that is a direct child of a [Paragraph](../../com.aspose.words/paragraph/). Any insert operations you perform using [DocumentBuilder](../../com.aspose.words/documentbuilder/) will insert before the [getCurrentNode()](../../com.aspose.words/documentbuilder/\#getCurrentNode).

عندما يكون الفقرة الحالية فارغة أو يكون المؤشر موضعًا مباشرةً قبل نهاية فقرة أو علامة مستند منسقة، تُعيد [getCurrentNode()](../../com.aspose.words/documentbuilder/\#getCurrentNode) القيمة null.

 **Examples:** 

يعرض كيفية نقل مؤشر منشئ المستند إلى عقد مختلفة في المستند.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create a valid bookmark, an entity that consists of nodes enclosed by a bookmark start node,
 // and a bookmark end node.
 builder.startBookmark("MyBookmark");
 builder.write("Bookmark contents.");
 builder.endBookmark("MyBookmark");

 NodeCollection firstParagraphNodes = doc.getFirstSection().getBody().getFirstParagraph().getChildNodes(NodeType.ANY, false);

 Assert.assertEquals(NodeType.BOOKMARK_START, firstParagraphNodes.get(0).getNodeType());
 Assert.assertEquals(NodeType.RUN, firstParagraphNodes.get(1).getNodeType());
 Assert.assertEquals("Bookmark contents.", firstParagraphNodes.get(1).getText().trim());
 Assert.assertEquals(NodeType.BOOKMARK_END, firstParagraphNodes.get(2).getNodeType());

 // The document builder's cursor is always ahead of the node that we last added with it.
 // If the builder's cursor is at the end of the document, its current node will be null.
 // The previous node is the bookmark end node that we last added.
 // Adding new nodes with the builder will append them to the last node.
 Assert.assertNull(builder.getCurrentNode());

 // If we wish to edit a different part of the document with the builder,
 // we will need to bring its cursor to the node we wish to edit.
 builder.moveToBookmark("MyBookmark");

 // Moving it to a bookmark will move it to the first node within the bookmark start and end nodes, the enclosed run.
 Assert.assertEquals(firstParagraphNodes.get(1), builder.getCurrentNode());

 // We can also move the cursor to an individual node like this.
 builder.moveTo(doc.getFirstSection().getBody().getFirstParagraph().getChildNodes(NodeType.ANY, false).get(0));

 Assert.assertEquals(NodeType.BOOKMARK_START, builder.getCurrentNode().getNodeType());
 Assert.assertEquals(doc.getFirstSection().getBody().getFirstParagraph(), builder.getCurrentParagraph());
 Assert.assertTrue(builder.isAtStartOfParagraph());

 // We can use specific methods to move to the start/end of a document.
 builder.moveToDocumentEnd();

 Assert.assertTrue(builder.isAtEndOfParagraph());

 builder.moveToDocumentStart();

 Assert.assertTrue(builder.isAtStartOfParagraph());
 
```

**Returns:**
[Node](../../com.aspose.words/node/) - The node that is currently selected in this DocumentBuilder.
### getCurrentParagraph() {#getCurrentParagraph}
```
public Paragraph getCurrentParagraph()
```


يحصل على الفقرة المحددة حاليًا في هذا [DocumentBuilder](../../com.aspose.words/documentbuilder/).

 **Remarks:** 

[getCurrentNode()](../../com.aspose.words/documentbuilder/\#getCurrentNode)

 **Examples:** 

يعرض كيفية نقل مؤشر منشئ المستند إلى عقد مختلفة في المستند.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create a valid bookmark, an entity that consists of nodes enclosed by a bookmark start node,
 // and a bookmark end node.
 builder.startBookmark("MyBookmark");
 builder.write("Bookmark contents.");
 builder.endBookmark("MyBookmark");

 NodeCollection firstParagraphNodes = doc.getFirstSection().getBody().getFirstParagraph().getChildNodes(NodeType.ANY, false);

 Assert.assertEquals(NodeType.BOOKMARK_START, firstParagraphNodes.get(0).getNodeType());
 Assert.assertEquals(NodeType.RUN, firstParagraphNodes.get(1).getNodeType());
 Assert.assertEquals("Bookmark contents.", firstParagraphNodes.get(1).getText().trim());
 Assert.assertEquals(NodeType.BOOKMARK_END, firstParagraphNodes.get(2).getNodeType());

 // The document builder's cursor is always ahead of the node that we last added with it.
 // If the builder's cursor is at the end of the document, its current node will be null.
 // The previous node is the bookmark end node that we last added.
 // Adding new nodes with the builder will append them to the last node.
 Assert.assertNull(builder.getCurrentNode());

 // If we wish to edit a different part of the document with the builder,
 // we will need to bring its cursor to the node we wish to edit.
 builder.moveToBookmark("MyBookmark");

 // Moving it to a bookmark will move it to the first node within the bookmark start and end nodes, the enclosed run.
 Assert.assertEquals(firstParagraphNodes.get(1), builder.getCurrentNode());

 // We can also move the cursor to an individual node like this.
 builder.moveTo(doc.getFirstSection().getBody().getFirstParagraph().getChildNodes(NodeType.ANY, false).get(0));

 Assert.assertEquals(NodeType.BOOKMARK_START, builder.getCurrentNode().getNodeType());
 Assert.assertEquals(doc.getFirstSection().getBody().getFirstParagraph(), builder.getCurrentParagraph());
 Assert.assertTrue(builder.isAtStartOfParagraph());

 // We can use specific methods to move to the start/end of a document.
 builder.moveToDocumentEnd();

 Assert.assertTrue(builder.isAtEndOfParagraph());

 builder.moveToDocumentStart();

 Assert.assertTrue(builder.isAtStartOfParagraph());
 
```

**Returns:**
[Paragraph](../../com.aspose.words/paragraph/) - The paragraph that is currently selected in this [DocumentBuilder](../../com.aspose.words/documentbuilder/).
### getCurrentSection() {#getCurrentSection}
```
public Section getCurrentSection()
```


يحصل على القسم المحدد حاليًا في هذا [DocumentBuilder](../../com.aspose.words/documentbuilder/).

 **Examples:** 

يظهر كيفية إدراج صورة عائمة وتحديد موضعها وحجمها.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertImage(getImageDir() + "Logo.jpg");
 shape.setWrapType(WrapType.NONE);

 // Configure the shape's "RelativeHorizontalPosition" property to treat the value of the "Left" property
 // as the shape's horizontal distance, in points, from the left side of the page.
 shape.setRelativeHorizontalPosition(RelativeHorizontalPosition.PAGE);

 // Set the shape's horizontal distance from the left side of the page to 100.
 shape.setLeft(100.0);

 // Use the "RelativeVerticalPosition" property in a similar way to position the shape 80pt below the top of the page.
 shape.setRelativeVerticalPosition(RelativeVerticalPosition.PAGE);
 shape.setTop(80.0);

 // Set the shape's height, which will automatically scale the width to preserve dimensions.
 shape.setHeight(125.0);

 Assert.assertEquals(125.0d, shape.getWidth());

 // The "Bottom" and "Right" properties contain the bottom and right edges of the image.
 Assert.assertEquals(shape.getTop() + shape.getHeight(), shape.getBottom());
 Assert.assertEquals(shape.getLeft() + shape.getWidth(), shape.getRight());

 doc.save(getArtifactsDir() + "Image.CreateFloatingPositionSize.docx");
 
```

**Returns:**
[Section](../../com.aspose.words/section/) - The section that is currently selected in this [DocumentBuilder](../../com.aspose.words/documentbuilder/).
### getCurrentStory() {#getCurrentStory}
```
public Story getCurrentStory()
```


يحصل على القصة المحددة حاليًا في هذا [DocumentBuilder](../../com.aspose.words/documentbuilder/).

 **Examples:** 

يعرض كيفية العمل مع القصة الحالية لمنشئ المستند.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // A Story is a type of node that has child Paragraph nodes, such as a Body.
 Assert.assertEquals(builder.getCurrentStory(), doc.getFirstSection().getBody());
 Assert.assertEquals(builder.getCurrentStory(), builder.getCurrentParagraph().getParentNode());
 Assert.assertEquals(StoryType.MAIN_TEXT, builder.getCurrentStory().getStoryType());

 builder.getCurrentStory().appendParagraph("Text added to current Story.");

 // A Story can also contain tables.
 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Row 1, cell 1");
 builder.insertCell();
 builder.write("Row 1, cell 2");
 builder.endTable();

 Assert.assertTrue(builder.getCurrentStory().getTables().contains(table));
 
```

**Returns:**
[Story](../../com.aspose.words/story/) - The story that is currently selected in this [DocumentBuilder](../../com.aspose.words/documentbuilder/).
### getCurrentStructuredDocumentTag() {#getCurrentStructuredDocumentTag}
```
public StructuredDocumentTag getCurrentStructuredDocumentTag()
```


يحصل على علامة المستند المهيكلة المحددة حاليًا في هذا [DocumentBuilder](../../com.aspose.words/documentbuilder/).

 **Examples:** 

يعرض كيفية نقل مؤشر DocumentBuilder داخل علامة مستند منسقة.

```

 Document doc = new Document(getMyDir() + "Structured document tags.docx");
 DocumentBuilder builder = new DocumentBuilder(doc);

 // There is a several ways to move the cursor:
 // 1 -  Move to the first character of structured document tag by index.
 builder.moveToStructuredDocumentTag(1, 1);

 // 2 -  Move to the first character of structured document tag by object.
 StructuredDocumentTag tag = (StructuredDocumentTag)doc.getChild(NodeType.STRUCTURED_DOCUMENT_TAG, 2, true);
 builder.moveToStructuredDocumentTag(tag, 1);
 builder.write(" New text.");

 Assert.assertEquals("R New text.ichText", tag.getText().trim());

 // 3 -  Move to the end of the second structured document tag.
 builder.moveToStructuredDocumentTag(1, -1);
 Assert.assertTrue(builder.isAtEndOfStructuredDocumentTag());

 // Get currently selected structured document tag.
 builder.getCurrentStructuredDocumentTag().setColor(Color.GREEN);

 doc.save(getArtifactsDir() + "Document.MoveToStructuredDocumentTag.docx");
 
```

**Returns:**
[StructuredDocumentTag](../../com.aspose.words/structureddocumenttag/) - The structured document tag that is currently selected in this [DocumentBuilder](../../com.aspose.words/documentbuilder/).
### getDirectCellAttr(int key) {#getDirectCellAttr-int}
```
public Object getDirectCellAttr(int key)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### getDirectParaAttr(int key) {#getDirectParaAttr-int}
```
public Object getDirectParaAttr(int key)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### getDirectParaAttr(int key, int revisionsView) {#getDirectParaAttr-int-int}
```
public Object getDirectParaAttr(int key, int revisionsView)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| key | int |  |
| revisionsView | int |  |

**Returns:**
java.lang.Object
### getDirectRowAttr(int key) {#getDirectRowAttr-int}
```
public Object getDirectRowAttr(int key)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### getDirectRunAttr(int fontAttr) {#getDirectRunAttr-int}
```
public Object getDirectRunAttr(int fontAttr)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| fontAttr | int |  |

**Returns:**
java.lang.Object
### getDirectRunAttr(int key, int revisionsView) {#getDirectRunAttr-int-int}
```
public Object getDirectRunAttr(int key, int revisionsView)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| key | int |  |
| revisionsView | int |  |

**Returns:**
java.lang.Object
### getDocument() {#getDocument}
```
public Document getDocument()
```


يحصل على الكائن [getDocument()](../../com.aspose.words/documentbuilder/\#getDocument) / [setDocument(com.aspose.words.Document)](../../com.aspose.words/documentbuilder/\#setDocument-com.aspose.words.Document) الذي يرتبط به هذا الكائن.

 **Examples:** 

يوضح كيفية تطبيق وإرجاع إعدادات إعداد الصفحة للأقسام في المستند.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Modify the page setup properties for the builder's current section and add text.
 builder.getPageSetup().setOrientation(Orientation.LANDSCAPE);
 builder.getPageSetup().setVerticalAlignment(PageVerticalAlignment.CENTER);
 builder.writeln("This is the first section, which landscape oriented with vertically centered text.");

 // If we start a new section using a document builder,
 // it will inherit the builder's current page setup properties.
 builder.insertBreak(BreakType.SECTION_BREAK_NEW_PAGE);

 Assert.assertEquals(Orientation.LANDSCAPE, doc.getSections().get(1).getPageSetup().getOrientation());
 Assert.assertEquals(PageVerticalAlignment.CENTER, doc.getSections().get(1).getPageSetup().getVerticalAlignment());

 // We can revert its page setup properties to their default values using the "ClearFormatting" method.
 builder.getPageSetup().clearFormatting();

 Assert.assertEquals(Orientation.PORTRAIT, doc.getSections().get(1).getPageSetup().getOrientation());
 Assert.assertEquals(PageVerticalAlignment.TOP, doc.getSections().get(1).getPageSetup().getVerticalAlignment());

 builder.writeln("This is the second section, which is in default Letter paper size, portrait orientation and top alignment.");

 doc.save(getArtifactsDir() + "PageSetup.ClearFormatting.docx");
 
```

**Returns:**
[Document](../../com.aspose.words/document/) - The [getDocument()](../../com.aspose.words/documentbuilder/\#getDocument) / [setDocument(com.aspose.words.Document)](../../com.aspose.words/documentbuilder/\#setDocument-com.aspose.words.Document) object that this object is attached to.
### getFont() {#getFont}
```
public Font getFont()
```


يرجع كائنًا يمثل خصائص تنسيق الخط الحالية.

 **Remarks:** 

استخدم [getFont()](../../com.aspose.words/documentbuilder/\#getFont) للوصول إلى خصائص تنسيق الخط وتعديلها.

حدد تنسيق الخط قبل إدراج النص.

 **Examples:** 

يوضح كيفية إدراج سلسلة محاطة بحد داخل مستند.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().getBorder().setColor(Color.GREEN);
 builder.getFont().getBorder().setLineWidth(2.5);
 builder.getFont().getBorder().setLineStyle(LineStyle.DASH_DOT_STROKER);

 builder.write("Text surrounded by green border.");

 doc.save(getArtifactsDir() + "Border.FontBorder.docx");
 
```

يوضح كيفية إنشاء جدول منسق باستخدام DocumentBuilder.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 table.setLeftIndent(20.0);

 // Set some formatting options for text and table appearance.
 builder.getRowFormat().setHeight(40.0);
 builder.getRowFormat().setHeightRule(HeightRule.AT_LEAST);
 builder.getCellFormat().getShading().setBackgroundPatternColor(new Color((198), (217), (241)));

 builder.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);
 builder.getFont().setSize(16.0);
 builder.getFont().setName("Arial");
 builder.getFont().setBold(true);

 // Configuring the formatting options in a document builder will apply them
 // to the current cell/row its cursor is in,
 // as well as any new cells and rows created using that builder.
 builder.write("Header Row,\n Cell 1");
 builder.insertCell();
 builder.write("Header Row,\n Cell 2");
 builder.insertCell();
 builder.write("Header Row,\n Cell 3");
 builder.endRow();

 // Reconfigure the builder's formatting objects for new rows and cells that we are about to make.
 // The builder will not apply these to the first row already created so that it will stand out as a header row.
 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.WHITE);
 builder.getCellFormat().setVerticalAlignment(CellVerticalAlignment.CENTER);
 builder.getRowFormat().setHeight(30.0);
 builder.getRowFormat().setHeightRule(HeightRule.AUTO);
 builder.insertCell();
 builder.getFont().setSize(12.0);
 builder.getFont().setBold(false);

 builder.write("Row 1, Cell 1.");
 builder.insertCell();
 builder.write("Row 1, Cell 2.");
 builder.insertCell();
 builder.write("Row 1, Cell 3.");
 builder.endRow();
 builder.insertCell();
 builder.write("Row 2, Cell 1.");
 builder.insertCell();
 builder.write("Row 2, Cell 2.");
 builder.insertCell();
 builder.write("Row 2, Cell 3.");
 builder.endRow();
 builder.endTable();

 doc.save(getArtifactsDir() + "DocumentBuilder.CreateFormattedTable.docx");
 
```

**Returns:**
[Font](../../com.aspose.words/font/) - An object that represents current font formatting properties.
### getItalic() {#getItalic}
```
public boolean getItalic()
```


صحيح إذا كان الخط مُنسقًا كخط مائل.

 **Examples:** 

يعرض كيفية ملء حقول MERGEFIELD بالبيانات باستخدام منشئ المستند بدلاً من دمج البريد.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert some MERGEFIELDS, which accept data from columns of the same name in a data source during a mail merge,
 // and then fill them manually.
 builder.insertField(" MERGEFIELD Chairman ");
 builder.insertField(" MERGEFIELD ChiefFinancialOfficer ");
 builder.insertField(" MERGEFIELD ChiefTechnologyOfficer ");

 builder.moveToMergeField("Chairman");
 builder.setBold(true);
 builder.writeln("John Doe");

 builder.moveToMergeField("ChiefFinancialOfficer");
 builder.setItalic(true);
 builder.writeln("Jane Doe");

 builder.moveToMergeField("ChiefTechnologyOfficer");
 builder.setItalic(true);
 builder.writeln("John Bloggs");

 doc.save(getArtifactsDir() + "DocumentBuilder.FillMergeFields.docx");
 
```

**Returns:**
boolean - القيمة المنطقية المقابلة.
### getListFormat() {#getListFormat}
```
public ListFormat getListFormat()
```


إرجاع كائن يمثل خصائص تنسيق القائمة الحالية.

 **Examples:** 

يعرض كيفية إنشاء قوائم نقطية ومرقمة.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Aspose.Words main advantages are:");

 // A list allows us to organize and decorate sets of paragraphs with prefix symbols and indents.
 // We can create nested lists by increasing the indent level.
 // We can begin and end a list by using a document builder's "ListFormat" property.
 // Each paragraph that we add between a list's start and the end will become an item in the list.
 // Below are two types of lists that we can create with a document builder.
 // 1 -  A bulleted list:
 // This list will apply an indent and a bullet symbol ("\u2022") before each paragraph.
 builder.getListFormat().applyBulletDefault();
 builder.writeln("Great performance");
 builder.writeln("High reliability");
 builder.writeln("Quality code and working");
 builder.writeln("Wide variety of features");
 builder.writeln("Easy to understand API");

 // End the bulleted list.
 builder.getListFormat().removeNumbers();

 builder.insertBreak(BreakType.PARAGRAPH_BREAK);
 builder.writeln("Aspose.Words allows:");

 // 2 -  A numbered list:
 // Numbered lists create a logical order for their paragraphs by numbering each item.
 builder.getListFormat().applyNumberDefault();

 // This paragraph is the first item. The first item of a numbered list will have a "1." as its list item symbol.
 builder.writeln("Opening documents from different formats:");

 Assert.assertEquals(0, builder.getListFormat().getListLevelNumber());

 // Call the "ListIndent" method to increase the current list level,
 // which will start a new self-contained list, with a deeper indent, at the current item of the first list level.
 builder.getListFormat().listIndent();

 Assert.assertEquals(1, builder.getListFormat().getListLevelNumber());

 // These are the first three list items of the second list level, which will maintain a count
 // independent of the count of the first list level. According to the current list format,
 // they will have symbols of "a.", "b.", and "c.".
 builder.writeln("DOC");
 builder.writeln("PDF");
 builder.writeln("HTML");

 // Call the "ListOutdent" method to return to the previous list level.
 builder.getListFormat().listOutdent();

 Assert.assertEquals(0, builder.getListFormat().getListLevelNumber());

 // These two paragraphs will continue the count of the first list level.
 // These items will have symbols of "2.", and "3."
 builder.writeln("Processing documents");
 builder.writeln("Saving documents in different formats:");

 // If we increase the list level to a level that we have added items to previously,
 // the nested list will be separate from the previous, and its numbering will start from the beginning.
 // These list items will have symbols of "a.", "b.", "c.", "d.", and "e".
 builder.getListFormat().listIndent();
 builder.writeln("DOC");
 builder.writeln("PDF");
 builder.writeln("HTML");
 builder.writeln("MHTML");
 builder.writeln("Plain text");

 // Outdent the list level again.
 builder.getListFormat().listOutdent();
 builder.writeln("Doing many other things!");

 // End the numbered list.
 builder.getListFormat().removeNumbers();

 doc.save(getArtifactsDir() + "Lists.ApplyDefaultBulletsAndNumbers.docx");
 
```

**Returns:**
[ListFormat](../../com.aspose.words/listformat/) - An object that represents current list formatting properties.
### getPageSetup() {#getPageSetup}
```
public PageSetup getPageSetup()
```


إرجاع كائن يمثل إعداد الصفحة الحالي وخصائص القسم.

 **Examples:** 

يوضح كيفية تطبيق وإرجاع إعدادات إعداد الصفحة للأقسام في المستند.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Modify the page setup properties for the builder's current section and add text.
 builder.getPageSetup().setOrientation(Orientation.LANDSCAPE);
 builder.getPageSetup().setVerticalAlignment(PageVerticalAlignment.CENTER);
 builder.writeln("This is the first section, which landscape oriented with vertically centered text.");

 // If we start a new section using a document builder,
 // it will inherit the builder's current page setup properties.
 builder.insertBreak(BreakType.SECTION_BREAK_NEW_PAGE);

 Assert.assertEquals(Orientation.LANDSCAPE, doc.getSections().get(1).getPageSetup().getOrientation());
 Assert.assertEquals(PageVerticalAlignment.CENTER, doc.getSections().get(1).getPageSetup().getVerticalAlignment());

 // We can revert its page setup properties to their default values using the "ClearFormatting" method.
 builder.getPageSetup().clearFormatting();

 Assert.assertEquals(Orientation.PORTRAIT, doc.getSections().get(1).getPageSetup().getOrientation());
 Assert.assertEquals(PageVerticalAlignment.TOP, doc.getSections().get(1).getPageSetup().getVerticalAlignment());

 builder.writeln("This is the second section, which is in default Letter paper size, portrait orientation and top alignment.");

 doc.save(getArtifactsDir() + "PageSetup.ClearFormatting.docx");
 
```

**Returns:**
[PageSetup](../../com.aspose.words/pagesetup/) - An object that represents current page setup and section properties.
### getParagraphFormat() {#getParagraphFormat}
```
public ParagraphFormat getParagraphFormat()
```


إرجاع كائن يمثل خصائص تنسيق الفقرة الحالية.

 **Examples:** 

يوضح كيفية إنشاء جدول منسق باستخدام DocumentBuilder.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 table.setLeftIndent(20.0);

 // Set some formatting options for text and table appearance.
 builder.getRowFormat().setHeight(40.0);
 builder.getRowFormat().setHeightRule(HeightRule.AT_LEAST);
 builder.getCellFormat().getShading().setBackgroundPatternColor(new Color((198), (217), (241)));

 builder.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);
 builder.getFont().setSize(16.0);
 builder.getFont().setName("Arial");
 builder.getFont().setBold(true);

 // Configuring the formatting options in a document builder will apply them
 // to the current cell/row its cursor is in,
 // as well as any new cells and rows created using that builder.
 builder.write("Header Row,\n Cell 1");
 builder.insertCell();
 builder.write("Header Row,\n Cell 2");
 builder.insertCell();
 builder.write("Header Row,\n Cell 3");
 builder.endRow();

 // Reconfigure the builder's formatting objects for new rows and cells that we are about to make.
 // The builder will not apply these to the first row already created so that it will stand out as a header row.
 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.WHITE);
 builder.getCellFormat().setVerticalAlignment(CellVerticalAlignment.CENTER);
 builder.getRowFormat().setHeight(30.0);
 builder.getRowFormat().setHeightRule(HeightRule.AUTO);
 builder.insertCell();
 builder.getFont().setSize(12.0);
 builder.getFont().setBold(false);

 builder.write("Row 1, Cell 1.");
 builder.insertCell();
 builder.write("Row 1, Cell 2.");
 builder.insertCell();
 builder.write("Row 1, Cell 3.");
 builder.endRow();
 builder.insertCell();
 builder.write("Row 2, Cell 1.");
 builder.insertCell();
 builder.write("Row 2, Cell 2.");
 builder.insertCell();
 builder.write("Row 2, Cell 3.");
 builder.endRow();
 builder.endTable();

 doc.save(getArtifactsDir() + "DocumentBuilder.CreateFormattedTable.docx");
 
```

**Returns:**
[ParagraphFormat](../../com.aspose.words/paragraphformat/) - An object that represents current paragraph formatting properties.
### getRowFormat() {#getRowFormat}
```
public RowFormat getRowFormat()
```


إرجاع كائن يمثل خصائص تنسيق صف الجدول الحالي.

 **Examples:** 

يوضح كيفية إنشاء جدول بحدود مخصصة.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.startTable();

 // Setting table formatting options for a document builder
 // will apply them to every row and cell that we add with it.
 builder.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);

 builder.getCellFormat().clearFormatting();
 builder.getCellFormat().setWidth(150.0);
 builder.getCellFormat().setVerticalAlignment(CellVerticalAlignment.CENTER);
 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.GREEN);
 builder.getCellFormat().setWrapText(false);
 builder.getCellFormat().setFitText(true);

 builder.getRowFormat().clearFormatting();
 builder.getRowFormat().setHeightRule(HeightRule.EXACTLY);
 builder.getRowFormat().setHeight(50.0);
 builder.getRowFormat().getBorders().setLineStyle(LineStyle.ENGRAVE_3_D);
 builder.getRowFormat().getBorders().setColor(Color.ORANGE);

 builder.insertCell();
 builder.write("Row 1, Col 1");

 builder.insertCell();
 builder.write("Row 1, Col 2");
 builder.endRow();

 // Changing the formatting will apply it to the current cell,
 // and any new cells that we create with the builder afterward.
 // This will not affect the cells that we have added previously.
 builder.getCellFormat().getShading().clearFormatting();

 builder.insertCell();
 builder.write("Row 2, Col 1");

 builder.insertCell();
 builder.write("Row 2, Col 2");

 builder.endRow();

 // Increase row height to fit the vertical text.
 builder.insertCell();
 builder.getRowFormat().setHeight(150.0);
 builder.getCellFormat().setOrientation(TextOrientation.UPWARD);
 builder.write("Row 3, Col 1");

 builder.insertCell();
 builder.getCellFormat().setOrientation(TextOrientation.DOWNWARD);
 builder.write("Row 3, Col 2");

 builder.endRow();
 builder.endTable();

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertTable.docx");
 
```

يعرض كيفية إنشاء جدول 2x2 منسق.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.getCellFormat().setVerticalAlignment(CellVerticalAlignment.CENTER);
 builder.write("Row 1, cell 1.");
 builder.insertCell();
 builder.write("Row 1, cell 2.");
 builder.endRow();

 // While building the table, the document builder will apply its current RowFormat/CellFormat property values
 // to the current row/cell that its cursor is in and any new rows/cells as it creates them.
 Assert.assertEquals(CellVerticalAlignment.CENTER, table.getRows().get(0).getCells().get(0).getCellFormat().getVerticalAlignment());
 Assert.assertEquals(CellVerticalAlignment.CENTER, table.getRows().get(0).getCells().get(1).getCellFormat().getVerticalAlignment());

 builder.insertCell();
 builder.getRowFormat().setHeight(100.0);
 builder.getRowFormat().setHeightRule(HeightRule.EXACTLY);
 builder.getCellFormat().setOrientation(TextOrientation.UPWARD);
 builder.write("Row 2, cell 1.");
 builder.insertCell();
 builder.getCellFormat().setOrientation(TextOrientation.DOWNWARD);
 builder.write("Row 2, cell 2.");
 builder.endRow();
 builder.endTable();

 // Previously added rows and cells are not retroactively affected by changes to the builder's formatting.
 Assert.assertEquals(0.0, table.getRows().get(0).getRowFormat().getHeight());
 Assert.assertEquals(HeightRule.AUTO, table.getRows().get(0).getRowFormat().getHeightRule());
 Assert.assertEquals(100.0, table.getRows().get(1).getRowFormat().getHeight());
 Assert.assertEquals(HeightRule.EXACTLY, table.getRows().get(1).getRowFormat().getHeightRule());
 Assert.assertEquals(TextOrientation.UPWARD, table.getRows().get(1).getCells().get(0).getCellFormat().getOrientation());
 Assert.assertEquals(TextOrientation.DOWNWARD, table.getRows().get(1).getCells().get(1).getCellFormat().getOrientation());

 doc.save(getArtifactsDir() + "DocumentBuilder.BuildTable.docx");
 
```

يوضح كيفية تنسيق الصفوف باستخدام DocumentBuilder.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Row 1, cell 1.");

 // Start a second row, and then configure its height. The builder will apply these settings to
 // its current row, as well as any new rows it creates afterwards.
 builder.endRow();

 RowFormat rowFormat = builder.getRowFormat();
 rowFormat.setHeight(100.0);
 rowFormat.setHeightRule(HeightRule.EXACTLY);

 builder.insertCell();
 builder.write("Row 2, cell 1.");
 builder.endTable();

 // The first row was unaffected by the padding reconfiguration and still holds the default values.
 Assert.assertEquals(0.0d, table.getRows().get(0).getRowFormat().getHeight());
 Assert.assertEquals(HeightRule.AUTO, table.getRows().get(0).getRowFormat().getHeightRule());

 Assert.assertEquals(100.0d, table.getRows().get(1).getRowFormat().getHeight());
 Assert.assertEquals(HeightRule.EXACTLY, table.getRows().get(1).getRowFormat().getHeightRule());

 doc.save(getArtifactsDir() + "DocumentBuilder.SetRowFormatting.docx");
 
```

**Returns:**
[RowFormat](../../com.aspose.words/rowformat/) - An object that represents current table row formatting properties.
### getUnderline() {#getUnderline}
```
public int getUnderline()
```


الحصول/تعيين نوع التسطير للخط الحالي.

 **Examples:** 

يعرض كيفية تنسيق النص الذي يُدرجه منشئ المستند.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.setUnderline(Underline.DASH);
 builder.getFont().setColor(Color.BLUE);
 builder.getFont().setSize(32.0);

 // The builder applies formatting to its current paragraph and any new text added by it afterward.
 builder.writeln("Large, blue, and underlined text.");

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertUnderline.docx");
 
```

**Returns:**
int - القيمة المقابلة من نوع  int . القيمة المرجعة هي واحدة من ثوابت [Underline](../../com.aspose.words/underline/).
### insertBreak(int breakType) {#insertBreak-int}
```
public void insertBreak(int breakType)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| breakType | int |  |

### insertCell() {#insertCell}
```
public Cell insertCell()
```


إدراج خلية جدول في المستند.

 **Remarks:** 

لبدء جدول، ما عليك سوى استدعاء [insertCell()](../../com.aspose.words/documentbuilder/\#insertCell). بعد ذلك، سيتم إضافة أي محتوى تضيفه باستخدام طرق أخرى من فئة [DocumentBuilder](../../com.aspose.words/documentbuilder/) إلى الخلية الحالية.

لبدء خلية جديدة في نفس الصف، استدعِ [insertCell()](../../com.aspose.words/documentbuilder/\#insertCell) مرة أخرى.

لإنهاء صف جدول استدعِ [endRow()](../../com.aspose.words/documentbuilder/\#endRow).

استخدم الخاصية [getCellFormat()](../../com.aspose.words/documentbuilder/\#getCellFormat) لتحديد تنسيق الخلية.

 **Examples:** 

يوضح كيفية إنشاء جدول بحدود مخصصة.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.startTable();

 // Setting table formatting options for a document builder
 // will apply them to every row and cell that we add with it.
 builder.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);

 builder.getCellFormat().clearFormatting();
 builder.getCellFormat().setWidth(150.0);
 builder.getCellFormat().setVerticalAlignment(CellVerticalAlignment.CENTER);
 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.GREEN);
 builder.getCellFormat().setWrapText(false);
 builder.getCellFormat().setFitText(true);

 builder.getRowFormat().clearFormatting();
 builder.getRowFormat().setHeightRule(HeightRule.EXACTLY);
 builder.getRowFormat().setHeight(50.0);
 builder.getRowFormat().getBorders().setLineStyle(LineStyle.ENGRAVE_3_D);
 builder.getRowFormat().getBorders().setColor(Color.ORANGE);

 builder.insertCell();
 builder.write("Row 1, Col 1");

 builder.insertCell();
 builder.write("Row 1, Col 2");
 builder.endRow();

 // Changing the formatting will apply it to the current cell,
 // and any new cells that we create with the builder afterward.
 // This will not affect the cells that we have added previously.
 builder.getCellFormat().getShading().clearFormatting();

 builder.insertCell();
 builder.write("Row 2, Col 1");

 builder.insertCell();
 builder.write("Row 2, Col 2");

 builder.endRow();

 // Increase row height to fit the vertical text.
 builder.insertCell();
 builder.getRowFormat().setHeight(150.0);
 builder.getCellFormat().setOrientation(TextOrientation.UPWARD);
 builder.write("Row 3, Col 1");

 builder.insertCell();
 builder.getCellFormat().setOrientation(TextOrientation.DOWNWARD);
 builder.write("Row 3, Col 2");

 builder.endRow();
 builder.endTable();

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertTable.docx");
 
```

يوضح كيفية استخدام DocumentBuilder لإنشاء جدول.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Start the table, then populate the first row with two cells.
 builder.startTable();
 builder.insertCell();
 builder.write("Row 1, Cell 1.");
 builder.insertCell();
 builder.write("Row 1, Cell 2.");

 // Call the builder's "EndRow" method to start a new row.
 builder.endRow();
 builder.insertCell();
 builder.write("Row 2, Cell 1.");
 builder.insertCell();
 builder.write("Row 2, Cell 2.");
 builder.endTable();

 doc.save(getArtifactsDir() + "DocumentBuilder.CreateTable.docx");
 
```

**Returns:**
[Cell](../../com.aspose.words/cell/) - The cell node that was just inserted.
### insertChart(int chartType, double width, double height) {#insertChart-int-double-double}
```
public Shape insertChart(int chartType, double width, double height)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| chartType | int |  |
| العرض | double |  |
| الارتفاع | double |  |

**Returns:**
[Shape](../../com.aspose.words/shape/)
### insertChart(int chartType, double width, double height, int chartStyle) {#insertChart-int-double-double-int}
```
public Shape insertChart(int chartType, double width, double height, int chartStyle)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| chartType | int |  |
| العرض | double |  |
| الارتفاع | double |  |
| chartStyle | int |  |

**Returns:**
[Shape](../../com.aspose.words/shape/)
### insertChart(int chartType, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType) {#insertChart-int-int-double-int-double-double-double-int}
```
public Shape insertChart(int chartType, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| chartType | int |  |
| horzPos | int |  |
| left | double |  |
| vertPos | int |  |
| top | double |  |
| العرض | double |  |
| الارتفاع | double |  |
| wrapType | int |  |

**Returns:**
[Shape](../../com.aspose.words/shape/)
### insertChart(int chartType, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType, int chartStyle) {#insertChart-int-int-double-int-double-double-double-int-int}
```
public Shape insertChart(int chartType, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType, int chartStyle)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| chartType | int |  |
| horzPos | int |  |
| left | double |  |
| vertPos | int |  |
| top | double |  |
| العرض | double |  |
| الارتفاع | double |  |
| wrapType | int |  |
| chartStyle | int |  |

**Returns:**
[Shape](../../com.aspose.words/shape/)
### insertCheckBox(String name, boolean defaultValue, boolean checkedValue, int size) {#insertCheckBox-java.lang.String-boolean-boolean-int}
```
public FormField insertCheckBox(String name, boolean defaultValue, boolean checkedValue, int size)
```


إدراج حقل نموذج مربع اختيار في الموضع الحالي.

 **Remarks:** 

إذا قمت بتحديد اسم لحقل النموذج، فسيتم إنشاء إشارة مرجعية تلقائيًا بنفس الاسم.

 **Examples:** 

يظهر كيفية إدراج مربعات اختيار في المستند.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert checkboxes of varying sizes and default checked statuses.
 builder.write("Unchecked check box of a default size: ");
 builder.insertCheckBox("", false, false, 0);
 builder.insertParagraph();

 builder.write("Large checked check box: ");
 builder.insertCheckBox("CheckBox_Default", true, true, 50);
 builder.insertParagraph();

 // Form fields have a name length limit of 20 characters.
 builder.write("Very large checked check box: ");
 builder.insertCheckBox("CheckBox_OnlyCheckedValue", true, 100);

 Assert.assertEquals("CheckBox_OnlyChecked", doc.getRange().getFormFields().get(2).getName());

 // We can interact with these check boxes in Microsoft Word by double clicking them.
 doc.save(getArtifactsDir() + "DocumentBuilder.InsertCheckBox.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| الاسم | java.lang.String | اسم حقل النموذج. يمكن أن يكون سلسلة فارغة. سيتم قطع القيمة التي تزيد عن 20 حرفًا. |
| defaultValue | boolean | القيمة الافتراضية لحقل مربع الاختيار. |
| checkedValue | boolean | الحالة الحالية للعلامة في حقل مربع الاختيار. |
| size | int | يحدد حجم مربع الاختيار بالنقاط. حدد 0 لبرنامج MS Word لحساب حجم مربع الاختيار تلقائيًا. |

**Returns:**
[FormField](../../com.aspose.words/formfield/) - The form field node that was just inserted.
### insertCheckBox(String name, boolean checkedValue, int size) {#insertCheckBox-java.lang.String-boolean-int}
```
public FormField insertCheckBox(String name, boolean checkedValue, int size)
```


إدراج حقل نموذج مربع اختيار في الموضع الحالي.

 **Remarks:** 

إذا قمت بتحديد اسم لحقل النموذج، فسيتم إنشاء إشارة مرجعية تلقائيًا بنفس الاسم.

 **Examples:** 

يظهر كيفية إدراج مربعات اختيار في المستند.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert checkboxes of varying sizes and default checked statuses.
 builder.write("Unchecked check box of a default size: ");
 builder.insertCheckBox("", false, false, 0);
 builder.insertParagraph();

 builder.write("Large checked check box: ");
 builder.insertCheckBox("CheckBox_Default", true, true, 50);
 builder.insertParagraph();

 // Form fields have a name length limit of 20 characters.
 builder.write("Very large checked check box: ");
 builder.insertCheckBox("CheckBox_OnlyCheckedValue", true, 100);

 Assert.assertEquals("CheckBox_OnlyChecked", doc.getRange().getFormFields().get(2).getName());

 // We can interact with these check boxes in Microsoft Word by double clicking them.
 doc.save(getArtifactsDir() + "DocumentBuilder.InsertCheckBox.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| الاسم | java.lang.String | اسم حقل النموذج. يمكن أن يكون سلسلة فارغة. سيتم قطع القيمة التي تزيد عن 20 حرفًا. |
| checkedValue | boolean | حالة العلامة في حقل مربع الاختيار. |
| size | int | يحدد حجم مربع الاختيار بالنقاط. حدد 0 لبرنامج MS Word لحساب حجم مربع الاختيار تلقائيًا. |

**Returns:**
[FormField](../../com.aspose.words/formfield/) - The form field node that was just inserted.
### insertComboBox(String name, String[] items, int selectedIndex) {#insertComboBox-java.lang.String-java.lang.String---int}
```
public FormField insertComboBox(String name, String[] items, int selectedIndex)
```


إدراج حقل نموذج صندوق مركب في الموضع الحالي.

 **Remarks:** 

إذا قمت بتحديد اسم لحقل النموذج، فسيتم إنشاء إشارة مرجعية تلقائيًا بنفس الاسم.

 **Examples:** 

يظهر كيفية إنشاء حقول النموذج.

```

 DocumentBuilder builder = new DocumentBuilder();

 // Form fields are objects in the document that the user can interact with by being prompted to enter values.
 // We can create them using a document builder, and below are two ways of doing so.
 // 1 -  Basic text input:
 builder.insertTextInput("My text input", TextFormFieldType.REGULAR,
         "", "Enter your name here", 30);

 // 2 -  Combo box with prompt text, and a range of possible values:
 String[] items =
         {
                 "-- Select your favorite footwear --", "Sneakers", "Oxfords", "Flip-flops", "Other"
         };

 builder.insertParagraph();
 builder.insertComboBox("My combo box", items, 0);

 builder.getDocument().save(getArtifactsDir() + "DocumentBuilder.CreateForm.docx");
 
```

يظهر كيفية إدراج حقل نموذج صندوق مركب في مستند.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a form that prompts the user to pick one of the items from the menu.
 builder.write("Pick a fruit: ");
 String[] items = {"Apple", "Banana", "Cherry"};
 builder.insertComboBox("DropDown", items, 0);

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertComboBox.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| الاسم | java.lang.String | اسم حقل النموذج. يمكن أن يكون سلسلة فارغة. سيتم قطع القيمة التي تزيد عن 20 حرفًا. |
| items | java.lang.String[] | عناصر صندوق القائمة المركبة. الحد الأقصى هو 25 عنصرًا. |
| selectedIndex | int | فهرس العنصر المحدد في صندوق القائمة المركبة. |

**Returns:**
[FormField](../../com.aspose.words/formfield/) - The form field node that was just inserted.
### insertDocument(Document srcDoc, int importFormatMode) {#insertDocument-com.aspose.words.Document-int}
```
public Node insertDocument(Document srcDoc, int importFormatMode)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| srcDoc | [Document](../../com.aspose.words/document/) |  |
| importFormatMode | int |  |

**Returns:**
[Node](../../com.aspose.words/node/)
### insertDocument(Document srcDoc, int importFormatMode, ImportFormatOptions importFormatOptions) {#insertDocument-com.aspose.words.Document-int-com.aspose.words.ImportFormatOptions}
```
public Node insertDocument(Document srcDoc, int importFormatMode, ImportFormatOptions importFormatOptions)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| srcDoc | [Document](../../com.aspose.words/document/) |  |
| importFormatMode | int |  |
| importFormatOptions | [ImportFormatOptions](../../com.aspose.words/importformatoptions/) |  |

**Returns:**
[Node](../../com.aspose.words/node/)
### insertDocumentInline(Document srcDoc, int importFormatMode, ImportFormatOptions importFormatOptions) {#insertDocumentInline-com.aspose.words.Document-int-com.aspose.words.ImportFormatOptions}
```
public Node insertDocumentInline(Document srcDoc, int importFormatMode, ImportFormatOptions importFormatOptions)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| srcDoc | [Document](../../com.aspose.words/document/) |  |
| importFormatMode | int |  |
| importFormatOptions | [ImportFormatOptions](../../com.aspose.words/importformatoptions/) |  |

**Returns:**
[Node](../../com.aspose.words/node/)
### insertField(int fieldType, boolean updateField) {#insertField-int-boolean}
```
public Field insertField(int fieldType, boolean updateField)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| fieldType | int |  |
| updateField | boolean |  |

**Returns:**
[Field](../../com.aspose.words/field/)
### insertField(String fieldCode) {#insertField-java.lang.String}
```
public Field insertField(String fieldCode)
```


إدراج حقل Word في مستند وتحديث نتيجة الحقل.

 **Remarks:** 

تقوم هذه الطريقة بإدراج حقل في مستند وتحديث نتيجة الحقل فورًا. يمكن لـ Aspose.Words تحديث الحقول من معظم الأنواع، ولكن ليس جميعها. لمزيد من التفاصيل راجع التحميل الزائد [insertField(java.lang.String, java.lang.String)](../../com.aspose.words/documentbuilder/\#insertField-java.lang.String--java.lang.String).

 **Examples:** 

يظهر كيفية إدراج الحقول وتحريك مؤشر منشئ المستند إليها.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.insertField("MERGEFIELD MyMergeField1 \\* MERGEFORMAT");
 builder.insertField("MERGEFIELD MyMergeField2 \\* MERGEFORMAT");

 // Move the cursor to the first MERGEFIELD.
 builder.moveToMergeField("MyMergeField1", true, false);

 // Note that the cursor is placed immediately after the first MERGEFIELD, and before the second.
 Assert.assertEquals(doc.getRange().getFields().get(1).getStart(), builder.getCurrentNode());
 Assert.assertEquals(doc.getRange().getFields().get(0).getEnd(), builder.getCurrentNode().getPreviousSibling());

 // If we wish to edit the field's field code or contents using the builder,
 // its cursor would need to be inside a field.
 // To place it inside a field, we would need to call the document builder's MoveTo method
 // and pass the field's start or separator node as an argument.
 builder.write(" Text between our merge fields. ");

 doc.save(getArtifactsDir() + "DocumentBuilder.MergeFields.docx");
 
```

يوضح كيفية إدراج حقل في مستند باستخدام شفرة الحقل.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Field dateField = builder.insertField("DATE \\* MERGEFORMAT");

 Assert.assertEquals(FieldType.FIELD_DATE, dateField.getType());
 Assert.assertEquals("DATE \\* MERGEFORMAT", dateField.getFieldCode());
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| fieldCode | java.lang.String | رمز الحقل لإدراجه (بدون الأقواس المعقوفة). |

**Returns:**
[Field](../../com.aspose.words/field/) - A [Field](../../com.aspose.words/field/) object that represents the inserted field.
### insertField(String fieldCode, String fieldValue) {#insertField-java.lang.String-java.lang.String}
```
public Field insertField(String fieldCode, String fieldValue)
```


إدراج حقل Word في مستند دون تحديث نتيجة الحقل.

 **Remarks:** 

تتكون الحقول في مستندات Microsoft Word من رمز الحقل ونتيجة الحقل. رمز الحقل يشبه الصيغة ونتيجة الحقل تشبه القيمة التي تنتجها الصيغة. قد يحتوي رمز الحقل أيضًا على مفاتيح الحقل التي تشبه التعليمات الإضافية لتنفيذ إجراء محدد.

يمكنك التبديل بين عرض رموز الحقول والنتائج في مستندك في Microsoft Word باستخدام اختصار لوحة المفاتيح Alt+F9. تظهر رموز الحقول بين الأقواس المعقوفة ( \{ \} ).

لإنشاء حقل، تحتاج إلى تحديد نوع الحقل، رمز الحقل و"قيمة العنصر النائب". إذا لم تكن متأكدًا من صياغة رمز حقل معين، أنشئ الحقل في Microsoft Word أولاً ثم قم بالتبديل لرؤية رمزه.

يمكن لـ Aspose.Words حساب نتائج الحقول لمعظم أنواع الحقول، لكن هذه الطريقة لا تقوم بتحديث نتيجة الحقل تلقائيًا. نظرًا لأن نتيجة الحقل لا تُحسب تلقائيًا، من المتوقع أن تمرّر قيمة نصية (أو حتى سلسلة فارغة) سيتم إدراجها في نتيجة الحقل. ستظل هذه القيمة في نتيجة الحقل كعنصر نائب حتى يتم تحديث الحقل. لتحديث نتيجة الحقل يمكنك استدعاء [Field.update()](../../com.aspose.words/field/\#update) على كائن الحقل الذي تم إرجاعه لك أو [Document.updateFields()](../../com.aspose.words/document/\#updateFields) لتحديث الحقول في المستند بأكمله.

 **Examples:** 

يظهر كيفية إعداد ترقيم الصفحات في قسم.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Section 1, page 1.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Section 1, page 2.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Section 1, page 3.");
 builder.insertBreak(BreakType.SECTION_BREAK_NEW_PAGE);
 builder.writeln("Section 2, page 1.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Section 2, page 2.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Section 2, page 3.");

 // Move the document builder to the first section's primary header,
 // which every page in that section will display.
 builder.moveToSection(0);
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);

 // Insert a PAGE field, which will display the number of the current page.
 builder.write("Page ");
 builder.insertField("PAGE", "");

 // Configure the section to have the page count that PAGE fields display start from 5.
 // Also, configure all PAGE fields to display their page numbers using uppercase Roman numerals.
 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();
 pageSetup.setRestartPageNumbering(true);
 pageSetup.setPageStartingNumber(5);
 pageSetup.setPageNumberStyle(NumberStyle.UPPERCASE_ROMAN);

 // Create another primary header for the second section, with another PAGE field.
 builder.moveToSection(1);
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 builder.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);
 builder.write(" - ");
 builder.insertField("PAGE", "");
 builder.write(" - ");

 // Configure the section to have the page count that PAGE fields display start from 10.
 // Also, configure all PAGE fields to display their page numbers using Arabic numbers.
 pageSetup = doc.getSections().get(1).getPageSetup();
 pageSetup.setPageStartingNumber(10);
 pageSetup.setRestartPageNumbering(true);
 pageSetup.setPageNumberStyle(NumberStyle.ARABIC);

 doc.save(getArtifactsDir() + "PageSetup.PageNumbering.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| fieldCode | java.lang.String | رمز الحقل لإدراجه (بدون الأقواس المعقوفة). |
| fieldValue | java.lang.String | قيمة الحقل لإدراجها. مرّر null للحقول التي لا تحتوي على قيمة. |

**Returns:**
[Field](../../com.aspose.words/field/) - A [Field](../../com.aspose.words/field/) object that represents the inserted field.
### insertFootnote(int footnoteType, String footnoteText) {#insertFootnote-int-java.lang.String}
```
public Footnote insertFootnote(int footnoteType, String footnoteText)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| footnoteType | int |  |
| footnoteText | java.lang.String |  |

**Returns:**
[Footnote](../../com.aspose.words/footnote/)
### insertFootnote(int footnoteType, String footnoteText, String referenceMark) {#insertFootnote-int-java.lang.String-java.lang.String}
```
public Footnote insertFootnote(int footnoteType, String footnoteText, String referenceMark)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| footnoteType | int |  |
| footnoteText | java.lang.String |  |
| referenceMark | java.lang.String |  |

**Returns:**
[Footnote](../../com.aspose.words/footnote/)
### insertForms2OleControl(Forms2OleControl forms2OleControl) {#insertForms2OleControl-com.aspose.words.Forms2OleControl}
```
public Shape insertForms2OleControl(Forms2OleControl forms2OleControl)
```


إدراج كائن [Forms2OleControl](../../com.aspose.words/forms2olecontrol/) في الموضع الحالي..

 **Examples:** 

يوضح كيفية إدراج عنصر التحكم ActiveX.

```

 DocumentBuilder builder = new DocumentBuilder();

 CommandButtonControl button1 = new CommandButtonControl();
 Shape shape = builder.insertForms2OleControl(button1);
 Assert.assertEquals(Forms2OleControlType.COMMAND_BUTTON, button1.getType());
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| forms2OleControl | [Forms2OleControl](../../com.aspose.words/forms2olecontrol/) |  |

**Returns:**
[Shape](../../com.aspose.words/shape/) - [Shape](../../com.aspose.words/shape/) object that contains passed [Forms2OleControl](../../com.aspose.words/forms2olecontrol/)
### insertGroupShape(ShapeBase[] shapes) {#insertGroupShape-com.aspose.words.ShapeBase...}
```
public GroupShape insertGroupShape(ShapeBase[] shapes)
```


تجميع الأشكال الممررة كمعامل في عقدة GroupShape جديدة يتم إدراجها في الموضع الحالي.

 **Remarks:** 

سيتم حساب موضع وأبعاد GroupShape الجديد تلقائيًا.

لا يمكن تجميع أشكال VML و DML معًا.

 **Examples:** 

يعرض كيفية إدراج شكل مجموعة DML.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape1 = builder.insertShape(ShapeType.RECTANGLE, 200.0, 250.0);
 shape1.setLeft(20.0);
 shape1.setTop(20.0);
 shape1.getStroke().setColor(Color.RED);

 Shape shape2 = builder.insertShape(ShapeType.ELLIPSE, 150.0, 200.0);
 shape2.setLeft(40.0);
 shape2.setTop(50.0);
 shape2.getStroke().setColor(Color.GREEN);

 // Dimensions for the new GroupShape node.
 double left = 10.0;
 double top = 10.0;
 double width = 200.0;
 double height = 300.0;
 // Insert GroupShape node for the specified size which is inserted into the specified position.
 GroupShape groupShape1 = builder.insertGroupShape(left, top, width, height, new Shape[] { shape1, shape2 });

 // Insert GroupShape node which position and dimension will be calculated automatically.
 Shape shape3 = (Shape)shape1.deepClone(true);
 GroupShape groupShape2 = builder.insertGroupShape(shape3);

 doc.save(getArtifactsDir() + "Shape.InsertGroupShape.docx");
 
```

يعرض كيفية دمج شكل المجموعة مع الشكل.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape1 = builder.insertShape(ShapeType.RECTANGLE, 200.0, 250.0);
 shape1.setLeft(20.0);
 shape1.setTop(20.0);
 shape1.getStroke().setColor(Color.RED);

 Shape shape2 = builder.insertShape(ShapeType.ELLIPSE, 150.0, 200.0);
 shape2.setLeft(40.0);
 shape2.setTop(50.0);
 shape2.getStroke().setColor(Color.GREEN);

 // Combine shapes into a GroupShape node which is inserted into the specified position.
 GroupShape groupShape1 = builder.insertGroupShape(shape1, shape2);

 // Combine Shape and GroupShape nodes.
 Shape shape3 = (Shape)shape1.deepClone(true);
 GroupShape groupShape2 = builder.insertGroupShape(groupShape1, shape3);

 doc.save(getArtifactsDir() + "Shape.CombineGroupShape.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| shapes | [ShapeBase\[\]](../../com.aspose.words/shapebase/) | قائمة الأشكال التي سيتم تجميعها. |

**Returns:**
[GroupShape](../../com.aspose.words/groupshape/)
### insertGroupShape(double left, double top, double width, double height, ShapeBase[] shapes) {#insertGroupShape-double-double-double-double-com.aspose.words.ShapeBase...}
```
public GroupShape insertGroupShape(double left, double top, double width, double height, ShapeBase[] shapes)
```


تجميع الأشكال الممررة كمعامل في عقدة GroupShape جديدة بالحجم المحدد يتم إدراجها في الموضع المحدد.

 **Remarks:** 

لا يمكن تجميع أشكال VML و DML معًا.

 **Examples:** 

يعرض كيفية إدراج شكل مجموعة DML.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape1 = builder.insertShape(ShapeType.RECTANGLE, 200.0, 250.0);
 shape1.setLeft(20.0);
 shape1.setTop(20.0);
 shape1.getStroke().setColor(Color.RED);

 Shape shape2 = builder.insertShape(ShapeType.ELLIPSE, 150.0, 200.0);
 shape2.setLeft(40.0);
 shape2.setTop(50.0);
 shape2.getStroke().setColor(Color.GREEN);

 // Dimensions for the new GroupShape node.
 double left = 10.0;
 double top = 10.0;
 double width = 200.0;
 double height = 300.0;
 // Insert GroupShape node for the specified size which is inserted into the specified position.
 GroupShape groupShape1 = builder.insertGroupShape(left, top, width, height, new Shape[] { shape1, shape2 });

 // Insert GroupShape node which position and dimension will be calculated automatically.
 Shape shape3 = (Shape)shape1.deepClone(true);
 GroupShape groupShape2 = builder.insertGroupShape(shape3);

 doc.save(getArtifactsDir() + "Shape.InsertGroupShape.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| left | double | المسافة بالنقاط من الأصل إلى الجانب الأيسر من شكل المجموعة. |
| top | double | المسافة بالنقاط من الأصل إلى الجانب العلوي من شكل المجموعة. |
| العرض | double | عرض شكل المجموعة بالنقاط. لا يُسمح بالقيمة السلبية. |
| الارتفاع | double | ارتفاع شكل المجموعة بالنقاط. لا يُسمح بالقيمة السلبية. |
| shapes | [ShapeBase\[\]](../../com.aspose.words/shapebase/) | قائمة الأشكال التي سيتم تجميعها. |

**Returns:**
[GroupShape](../../com.aspose.words/groupshape/)
### insertHorizontalRule() {#insertHorizontalRule}
```
public Shape insertHorizontalRule()
```


إدراج شكل قاعدة أفقية في المستند.

 **Examples:** 

يظهر كيفية إدراج شكل خط أفقي، وتخصيص تنسيقه.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 Shape shape = builder.insertHorizontalRule();

 HorizontalRuleFormat horizontalRuleFormat = shape.getHorizontalRuleFormat();
 horizontalRuleFormat.setAlignment(HorizontalRuleAlignment.CENTER);
 horizontalRuleFormat.setWidthPercent(70.0);
 horizontalRuleFormat.setHeight(3.0);
 horizontalRuleFormat.setColor(Color.BLUE);
 horizontalRuleFormat.setNoShade(true);

 Assert.assertTrue(shape.isHorizontalRule());
 Assert.assertTrue(shape.getHorizontalRuleFormat().getNoShade());
 
```

**Returns:**
[Shape](../../com.aspose.words/shape/) - The shape that is a horizontal rule.
### insertHtml(String html) {#insertHtml-java.lang.String}
```
public void insertHtml(String html)
```


إدراج سلسلة HTML في المستند.

 **Remarks:** 

يمكنك استخدام هذه الطريقة لإدراج جزء HTML أو مستند HTML كامل.

 **Examples:** 

يعرض كيفية استخدام منشئ المستند لإدراج محتوى HTML في مستند.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 final String HTML = " Paragraph right" +
         "Implicit paragraph left" +
         " Div center" +
         " Heading 1 left.";

 builder.insertHtml(HTML);

 // Inserting HTML code parses the formatting of each element into equivalent document text formatting.
 ParagraphCollection paragraphs = doc.getFirstSection().getBody().getParagraphs();

 Assert.assertEquals("Paragraph right", paragraphs.get(0).getText().trim());
 Assert.assertEquals(ParagraphAlignment.RIGHT, paragraphs.get(0).getParagraphFormat().getAlignment());

 Assert.assertEquals("Implicit paragraph left", paragraphs.get(1).getText().trim());
 Assert.assertEquals(ParagraphAlignment.LEFT, paragraphs.get(1).getParagraphFormat().getAlignment());
 Assert.assertTrue(paragraphs.get(1).getRuns().get(0).getFont().getBold());

 Assert.assertEquals("Div center", paragraphs.get(2).getText().trim());
 Assert.assertEquals(ParagraphAlignment.CENTER, paragraphs.get(2).getParagraphFormat().getAlignment());

 Assert.assertEquals("Heading 1 left.", paragraphs.get(3).getText().trim());
 Assert.assertEquals("Heading 1", paragraphs.get(3).getParagraphFormat().getStyle().getName());

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertHtml.docx");
 
```

يوضح كيفية تنفيذ دمج بريد مع رد اتصال مخصص يتعامل مع بيانات الدمج على شكل مستندات HTML.

```

 public void insertHtml() throws Exception {
     Document doc = new Document(getMyDir() + "Field sample - MERGEFIELD.docx");

     // Add a handler for the MergeField event
     doc.getMailMerge().setFieldMergingCallback(new HandleMergeFieldInsertHtml());

     final String htmlText = "\r\n Hello world!\r\n";

     // Execute mail merge
     doc.getMailMerge().execute(new String[]{"htmlField1"}, new String[]{htmlText});

     // Save resulting document with a new name
     doc.save(getArtifactsDir() + "MailMergeEvent.InsertHtml.docx");
 }

 private class HandleMergeFieldInsertHtml implements IFieldMergingCallback {
     // This is called when merge field is actually merged with data in the document.
     public void fieldMerging(final FieldMergingArgs args) throws Exception {
         // All merge fields that expect HTML data should be marked with some prefix, e.g. 'html'
         if (args.getDocumentFieldName().startsWith("html") && args.getField().getFieldCode().contains("\\b")) {
             FieldMergeField field = args.getField();

             // Insert the text for this merge field as HTML data, using DocumentBuilder
             DocumentBuilder builder = new DocumentBuilder(args.getDocument());
             builder.moveToMergeField(args.getDocumentFieldName());
             builder.write(field.getTextBefore());
             builder.insertHtml((String) args.getFieldValue());

             // The HTML text itself should not be inserted
             // We have already inserted it as an HTML
             args.setText("");
         }
     }

     public void imageFieldMerging(ImageFieldMergingArgs args) {
         // Do nothing
     }
 }
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| html | java.lang.String | سلسلة HTML لإدراجها في المستند. |

### insertHtml(String html, boolean useBuilderFormatting) {#insertHtml-java.lang.String-boolean}
```
public void insertHtml(String html, boolean useBuilderFormatting)
```


إدراج سلسلة HTML في المستند.

 **Remarks:** 

يمكنك استخدام هذه الطريقة لإدراج جزء HTML أو مستند HTML كامل.

عندما يكون useBuilderFormatting مساويًا لـ false، يتم تجاهل تنسيق [DocumentBuilder](../../com.aspose.words/documentbuilder/) ويستند تنسيق النص المُدرج إلى تنسيق HTML الافتراضي. نتيجة لذلك، يبدو النص كما يُعرض في المتصفحات.

عند كون useBuilderFormatting صحيحًا، يتم تنسيق النص المُدرج بناءً على تنسيق [DocumentBuilder](../../com.aspose.words/documentbuilder/)، ويظهر النص كما لو أنه تم إدخاله باستخدام [write(java.lang.String)](../../com.aspose.words/documentbuilder/\#write-java.lang.String).

 **Examples:** 

يوضح كيفية تطبيق تنسيق مُنشئ المستند أثناء إدراج محتوى HTML.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Set a text alignment for the builder, insert an HTML paragraph with a specified alignment, and one without.
 builder.getParagraphFormat().setAlignment(ParagraphAlignment.DISTRIBUTED);
 builder.insertHtml(
         " Paragraph 1." +
                 " Paragraph 2.", useBuilderFormatting);

 ParagraphCollection paragraphs = doc.getFirstSection().getBody().getParagraphs();

 // The first paragraph has an alignment specified. When InsertHtml parses the HTML code,
 // the paragraph alignment value found in the HTML code always supersedes the document builder's value.
 Assert.assertEquals("Paragraph 1.", paragraphs.get(0).getText().trim());
 Assert.assertEquals(ParagraphAlignment.RIGHT, paragraphs.get(0).getParagraphFormat().getAlignment());

 // The second paragraph has no alignment specified. It can have its alignment value filled in
 // by the builder's value depending on the flag we passed to the InsertHtml method.
 Assert.assertEquals("Paragraph 2.", paragraphs.get(1).getText().trim());
 Assert.assertEquals(useBuilderFormatting ? ParagraphAlignment.DISTRIBUTED : ParagraphAlignment.LEFT,
         paragraphs.get(1).getParagraphFormat().getAlignment());

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertHtmlWithFormatting.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| html | java.lang.String | سلسلة HTML لإدراجها في المستند. |
| useBuilderFormatting | boolean | قيمة تشير إلى ما إذا كان التنسيق المحدد في [DocumentBuilder](../../com.aspose.words/documentbuilder/) يُستخدم كتنسيق أساسي للنص المستورد من HTML. |

### insertHtml(String html, int options) {#insertHtml-java.lang.String-int}
```
public void insertHtml(String html, int options)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| html | java.lang.String |  |
| الخيارات | int |  |

### insertHyperlink(String displayText, String urlOrBookmark, boolean isBookmark) {#insertHyperlink-java.lang.String-java.lang.String-boolean}
```
public Field insertHyperlink(String displayText, String urlOrBookmark, boolean isBookmark)
```


إدراج ارتباط تشعبي في المستند.

 **Remarks:** 

لاحظ أنه يجب عليك تحديد تنسيق الخط لنص عرض الارتباط التشعبي صراحةً باستخدام الخاصية [getFont()](../../com.aspose.words/documentbuilder/\#getFont).

تستدعي هذه الطريقة داخليًا [insertField(java.lang.String)](../../com.aspose.words/documentbuilder/\#insertField-java.lang.String) لإدراج حقل HYPERLINK في مستند MS Word.

 **Examples:** 

يوضح كيفية إدراج حقل ارتباط تشعبي.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.write("For more information, please visit the ");

 // Insert a hyperlink and emphasize it with custom formatting.
 // The hyperlink will be a clickable piece of text which will take us to the location specified in the URL.
 builder.getFont().setColor(Color.BLUE);
 builder.getFont().setUnderline(Underline.SINGLE);
 builder.insertHyperlink("Google website", "https://www.google.com", false);
 builder.getFont().clearFormatting();
 builder.writeln(".");

 // Ctrl + left clicking the link in the text in Microsoft Word will take us to the URL via a new web browser window.
 doc.save(getArtifactsDir() + "DocumentBuilder.InsertHyperlink.docx");
 
```

يوضح كيفية استخدام مكدس تنسيق مُنشئ المستند.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Set up font formatting, then write the text that goes before the hyperlink.
 builder.getFont().setName("Arial");
 builder.getFont().setSize(24.0);
 builder.write("To visit Google, hold Ctrl and click ");

 // Preserve our current formatting configuration on the stack.
 builder.pushFont();

 // Alter the builder's current formatting by applying a new style.
 builder.getFont().setStyleIdentifier(StyleIdentifier.HYPERLINK);
 builder.insertHyperlink("here", "http://www.google.com", false);

 Assert.assertEquals(Color.BLUE.getRGB(), builder.getFont().getColor().getRGB());
 Assert.assertEquals(Underline.SINGLE, builder.getFont().getUnderline());

 // Restore the font formatting that we saved earlier and remove the element from the stack.
 builder.popFont();

 Assert.assertEquals(0, builder.getFont().getColor().getRGB());
 Assert.assertEquals(Underline.NONE, builder.getFont().getUnderline());

 builder.write(". We hope you enjoyed the example.");

 doc.save(getArtifactsDir() + "DocumentBuilder.PushPopFont.docx");
 
```

يوضح كيفية إدراج ارتباط تشعبي يشير إلى علامة مرجعية محلية.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.startBookmark("Bookmark1");
 builder.write("Bookmarked text. ");
 builder.endBookmark("Bookmark1");
 builder.writeln("Text outside of the bookmark.");

 // Insert a HYPERLINK field that links to the bookmark. We can pass field switches
 // to the "InsertHyperlink" method as part of the argument containing the referenced bookmark's name.
 builder.getFont().setColor(Color.BLUE);
 builder.getFont().setUnderline(Underline.SINGLE);
 FieldHyperlink hyperlink = (FieldHyperlink)builder.insertHyperlink("Link to Bookmark1", "Bookmark1", true);
 hyperlink.setScreenTip("Hyperlink Tip");

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertHyperlinkToLocalBookmark.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| displayText | java.lang.String | نص الرابط الذي سيُعرض في المستند. |
| urlOrBookmark | java.lang.String | وجهة الرابط. يمكن أن تكون عنوان URL أو اسم إشارة مرجعية داخل المستند. هذه الطريقة دائمًا تضيف علامات اقتباس في بداية ونهاية عنوان URL. |
| isBookmark | boolean | صحيح إذا كان المعامل السابق اسم إشارة مرجعية داخل المستند؛ خطأ إذا كان المعامل السابق عنوان URL. |

**Returns:**
[Field](../../com.aspose.words/field/) - A [Field](../../com.aspose.words/field/) object that represents the inserted field.
### insertImage(byte[] imageBytes) {#insertImage-byte}
```
public Shape insertImage(byte[] imageBytes)
```


يدرج صورة من مصفوفة بايت في المستند. تُدرج الصورة داخل النص وبمقياس 100٪.

 **Remarks:** 

يمكنك تغيير حجم الصورة وموقعها وطريقة التموضع وإعدادات أخرى باستخدام كائن [Shape](../../com.aspose.words/shape/) الذي تُعيده هذه الطريقة.

 **Examples:** 

يوضح كيفية إدراج صورة من مصفوفة بايت في مستند.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 byte[] imageByteArray = DocumentHelper.getBytesFromStream(new FileInputStream(getImageDir() + "Logo.jpg"));

 // Below are three ways of inserting an image from a byte array.
 // 1 -  Inline shape with a default size based on the image's original dimensions:
 builder.insertImage(imageByteArray);

 builder.insertBreak(BreakType.PAGE_BREAK);

 // 2 -  Inline shape with custom dimensions:
 builder.insertImage(imageByteArray, ConvertUtil.pixelToPoint(250.0), ConvertUtil.pixelToPoint(144.0));

 builder.insertBreak(BreakType.PAGE_BREAK);

 // 3 -  Floating shape with custom dimensions:
 builder.insertImage(imageByteArray, RelativeHorizontalPosition.MARGIN, 100.0, RelativeVerticalPosition.MARGIN,
         100.0, 200.0, 100.0, WrapType.SQUARE);

 doc.save(getArtifactsDir() + "DocumentBuilderImages.InsertImageFromByteArray.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| imageBytes | byte[] | مصفوفة البايت التي تحتوي على الصورة. |

**Returns:**
[Shape](../../com.aspose.words/shape/) - The image node that was just inserted.
### insertImage(byte[] imageBytes, double width, double height) {#insertImage-byte---double-double}
```
public Shape insertImage(byte[] imageBytes, double width, double height)
```


إدراج صورة مدمجة من مصفوفة بايت في المستند وتغيير حجمها إلى الحجم المحدد.

 **Remarks:** 

يمكنك تغيير حجم الصورة وموقعها وطريقة التموضع وإعدادات أخرى باستخدام كائن [Shape](../../com.aspose.words/shape/) الذي تُعيده هذه الطريقة.

 **Examples:** 

يوضح كيفية إدراج صورة من مصفوفة بايت في مستند.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 byte[] imageByteArray = DocumentHelper.getBytesFromStream(new FileInputStream(getImageDir() + "Logo.jpg"));

 // Below are three ways of inserting an image from a byte array.
 // 1 -  Inline shape with a default size based on the image's original dimensions:
 builder.insertImage(imageByteArray);

 builder.insertBreak(BreakType.PAGE_BREAK);

 // 2 -  Inline shape with custom dimensions:
 builder.insertImage(imageByteArray, ConvertUtil.pixelToPoint(250.0), ConvertUtil.pixelToPoint(144.0));

 builder.insertBreak(BreakType.PAGE_BREAK);

 // 3 -  Floating shape with custom dimensions:
 builder.insertImage(imageByteArray, RelativeHorizontalPosition.MARGIN, 100.0, RelativeVerticalPosition.MARGIN,
         100.0, 200.0, 100.0, WrapType.SQUARE);

 doc.save(getArtifactsDir() + "DocumentBuilderImages.InsertImageFromByteArray.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| imageBytes | byte[] | مصفوفة البايت التي تحتوي على الصورة. |
| العرض | double | عرض الصورة بالنقاط. يمكن أن يكون قيمة سالبة أو صفر لطلب مقياس 100٪. |
| الارتفاع | double | ارتفاع الصورة بالنقاط. يمكن أن يكون قيمة سالبة أو صفر لطلب مقياس 100٪. |

**Returns:**
[Shape](../../com.aspose.words/shape/) - The image node that was just inserted.
### insertImage(byte[] imageBytes, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType) {#insertImage-byte---int-double-int-double-double-double-int}
```
public Shape insertImage(byte[] imageBytes, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| imageBytes | byte[] |  |
| horzPos | int |  |
| left | double |  |
| vertPos | int |  |
| top | double |  |
| العرض | double |  |
| الارتفاع | double |  |
| wrapType | int |  |

**Returns:**
[Shape](../../com.aspose.words/shape/)
### insertImage(BufferedImage image) {#insertImage-java.awt.image.BufferedImage}
```
public Shape insertImage(BufferedImage image)
```


يدرج صورة في المستند. يدرج صورة من كائن java.awt.image.BufferedImage في المستند. تُدرج الصورة داخل النص وبمقياس 100٪.

 **Remarks:** 

يمكنك تغيير حجم الصورة وموقعها وطريقة التموضع وإعدادات أخرى باستخدام كائن [Shape](../../com.aspose.words/shape/) الذي تُعيده هذه الطريقة.

ستقوم Aspose.Words بإدراج الصورة بتنسيق PNG وبالإعدادات الافتراضية. إذا أردت إدراج BufferedImage بتنسيق آخر أو بإعدادات مختلفة، تحتاج إلى حفظ الصورة في مصفوفة بايت واستخدام [insertImage(byte[])](../../com.aspose.words/documentbuilder/\#insertImage-byte).

 **Examples:** 

يوضح كيفية إدراج صورة من كائن في مستند.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 String imageFile = getImageDir() + "Logo.jpg";

 // Below are three ways of inserting an image from an Image object instance.
 // 1 -  Inline shape with a default size based on the image's original dimensions:
 builder.insertImage(imageFile);

 builder.insertBreak(BreakType.PAGE_BREAK);

 // 2 -  Inline shape with custom dimensions:
 builder.insertImage(imageFile, ConvertUtil.pixelToPoint(250.0), ConvertUtil.pixelToPoint(144.0));

 builder.insertBreak(BreakType.PAGE_BREAK);

 // 3 -  Floating shape with custom dimensions:
 builder.insertImage(imageFile, RelativeHorizontalPosition.MARGIN, 100.0, RelativeVerticalPosition.MARGIN,
         100.0, 200.0, 100.0, WrapType.SQUARE);

 doc.save(getArtifactsDir() + "DocumentBuilderImages.InsertImageFromImageObject.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| صورة | java.awt.image.BufferedImage | الصورة التي سيتم إدراجها في المستند. |

**Returns:**
[Shape](../../com.aspose.words/shape/) - The image node that was just inserted.
### insertImage(BufferedImage image, double width, double height) {#insertImage-java.awt.image.BufferedImage-double-double}
```
public Shape insertImage(BufferedImage image, double width, double height)
```


إدراج صورة مدمجة من كائن java.awt.image.BufferedImage في المستند وتغيير حجمها إلى الحجم المحدد.

 **Remarks:** 

يمكنك تغيير حجم الصورة وموقعها وطريقة التموضع وإعدادات أخرى باستخدام كائن [Shape](../../com.aspose.words/shape/) الذي تُعيده هذه الطريقة.

ستقوم Aspose.Words بإدراج الصورة بتنسيق PNG وبالإعدادات الافتراضية. إذا أردت إدراج BufferedImage بتنسيق آخر أو بإعدادات مختلفة، تحتاج إلى حفظ الصورة في مصفوفة بايت واستخدام [insertImage(byte[])](../../com.aspose.words/documentbuilder/\#insertImage-byte).

 **Examples:** 

يوضح كيفية إدراج صورة من كائن في مستند.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 String imageFile = getImageDir() + "Logo.jpg";

 // Below are three ways of inserting an image from an Image object instance.
 // 1 -  Inline shape with a default size based on the image's original dimensions:
 builder.insertImage(imageFile);

 builder.insertBreak(BreakType.PAGE_BREAK);

 // 2 -  Inline shape with custom dimensions:
 builder.insertImage(imageFile, ConvertUtil.pixelToPoint(250.0), ConvertUtil.pixelToPoint(144.0));

 builder.insertBreak(BreakType.PAGE_BREAK);

 // 3 -  Floating shape with custom dimensions:
 builder.insertImage(imageFile, RelativeHorizontalPosition.MARGIN, 100.0, RelativeVerticalPosition.MARGIN,
         100.0, 200.0, 100.0, WrapType.SQUARE);

 doc.save(getArtifactsDir() + "DocumentBuilderImages.InsertImageFromImageObject.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| صورة | java.awt.image.BufferedImage | الصورة التي سيتم إدراجها في المستند. |
| العرض | double | عرض الصورة بالنقاط. يمكن أن يكون قيمة سالبة أو صفر لطلب مقياس 100٪. |
| الارتفاع | double | ارتفاع الصورة بالنقاط. يمكن أن يكون قيمة سالبة أو صفر لطلب مقياس 100٪. |

**Returns:**
[Shape](../../com.aspose.words/shape/) - The image node that was just inserted.
### insertImage(BufferedImage image, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType) {#insertImage-java.awt.image.BufferedImage-int-double-int-double-double-double-int}
```
public Shape insertImage(BufferedImage image, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| صورة | java.awt.image.BufferedImage |  |
| horzPos | int |  |
| left | double |  |
| vertPos | int |  |
| top | double |  |
| العرض | double |  |
| الارتفاع | double |  |
| wrapType | int |  |

**Returns:**
[Shape](../../com.aspose.words/shape/)
### insertImage(InputStream stream) {#insertImage-java.io.InputStream}
```
public Shape insertImage(InputStream stream)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| stream | java.io.InputStream |  |

**Returns:**
[Shape](../../com.aspose.words/shape/)
### insertImage(InputStream stream, double width, double height) {#insertImage-java.io.InputStream-double-double}
```
public Shape insertImage(InputStream stream, double width, double height)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| stream | java.io.InputStream |  |
| العرض | double |  |
| الارتفاع | double |  |

**Returns:**
[Shape](../../com.aspose.words/shape/)
### insertImage(InputStream stream, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType) {#insertImage-java.io.InputStream-int-double-int-double-double-double-int}
```
public Shape insertImage(InputStream stream, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| stream | java.io.InputStream |  |
| horzPos | int |  |
| left | double |  |
| vertPos | int |  |
| top | double |  |
| العرض | double |  |
| الارتفاع | double |  |
| wrapType | int |  |

**Returns:**
[Shape](../../com.aspose.words/shape/)
### insertImage(String fileName) {#insertImage-java.lang.String}
```
public Shape insertImage(String fileName)
```


يدرج صورة من ملف أو عنوان URL في المستند. تُدرج الصورة داخل النص وبمقياس 100٪.

 **Remarks:** 

سيقوم هذا التحميل الزائد تلقائيًا بتنزيل الصورة قبل إدراجها في المستند إذا قمت بتحديد URI بعيد.

يمكنك تغيير حجم الصورة وموقعها وطريقة التموضع وإعدادات أخرى باستخدام كائن [Shape](../../com.aspose.words/shape/) الذي تُعيده هذه الطريقة.

 **Examples:** 

يعرض كيفية إدراج صورة من نظام الملفات المحلي في مستند.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Below are three ways of inserting an image from a local system filename.
 // 1 -  Inline shape with a default size based on the image's original dimensions:
 builder.insertImage(getImageDir() + "Logo.jpg");

 builder.insertBreak(BreakType.PAGE_BREAK);

 // 2 -  Inline shape with custom dimensions:
 builder.insertImage(getImageDir() + "Transparent background logo.png", ConvertUtil.pixelToPoint(250.0),
         ConvertUtil.pixelToPoint(144.0));

 builder.insertBreak(BreakType.PAGE_BREAK);

 // 3 -  Floating shape with custom dimensions:
 builder.insertImage(getImageDir() + "Windows MetaFile.wmf", RelativeHorizontalPosition.MARGIN, 100.0,
         RelativeVerticalPosition.MARGIN, 100.0, 200.0, 100.0, WrapType.SQUARE);

 doc.save(getArtifactsDir() + "DocumentBuilderImages.InsertImageFromFilename.docx");
 
```

يعرض كيفية تحديد الصورة التي سيتم إدراجها.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.insertImage(getImageDir() + "Scalable Vector Graphics.svg");

 // Aspose.Words insert SVG image to the document as PNG with svgBlip extension
 // that contains the original vector SVG image representation.
 doc.save(getArtifactsDir() + "DocumentBuilderImages.InsertSvgImage.SvgWithSvgBlip.docx");

 // Aspose.Words insert SVG image to the document as PNG, just like Microsoft Word does for old format.
 doc.save(getArtifactsDir() + "DocumentBuilderImages.InsertSvgImage.Svg.doc");

 doc.getCompatibilityOptions().optimizeFor(MsWordVersion.WORD_2003);

 // Aspose.Words insert SVG image to the document as EMF metafile to keep the image in vector representation.
 doc.save(getArtifactsDir() + "DocumentBuilderImages.InsertSvgImage.Emf.docx");
 
```

يعرض كيفية إدراج صورة GIF في المستند.

```

 DocumentBuilder builder = new DocumentBuilder();

 // We can insert gif image using path or bytes array.
 // It works only if DocumentBuilder optimized to Word version 2010 or higher.
 // Note, that access to the image bytes causes conversion Gif to Png.
 Shape gifImage = builder.insertImage(getImageDir() + "Graphics Interchange Format.gif");

 gifImage = builder.insertImage(DocumentHelper.getBytesFromStream(new FileInputStream(getImageDir() + "Graphics Interchange Format.gif")));

 builder.getDocument().save(getArtifactsDir() + "InsertGif.docx");
 
```

يعرض كيفية إدراج شكل مع صورة في مستند.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Below are two locations where the document builder's "InsertShape" method
 // can source the image that the shape will display.
 // 1 -  Pass a local file system filename of an image file:
 builder.write("Image from local file: ");
 builder.insertImage(getImageDir() + "Logo.jpg");
 builder.writeln();

 // 2 -  Pass a URL which points to an image.
 builder.write("Image from a URL: ");
 builder.insertImage(getImageUri().toURL().openStream());
 builder.writeln();

 doc.save(getArtifactsDir() + "Image.FromUrl.docx");
 
```

يوضح كيفية إدراج صورة عائمة في مركز الصفحة.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a floating image that will appear behind the overlapping text and align it to the page's center.
 Shape shape = builder.insertImage(getImageDir() + "Logo.jpg");
 shape.setWrapType(WrapType.NONE);
 shape.setBehindText(true);
 shape.setRelativeHorizontalPosition(RelativeHorizontalPosition.PAGE);
 shape.setRelativeVerticalPosition(RelativeVerticalPosition.PAGE);
 shape.setHorizontalAlignment(HorizontalAlignment.CENTER);
 shape.setVerticalAlignment(VerticalAlignment.CENTER);

 doc.save(getArtifactsDir() + "Image.CreateFloatingPageCenter.docx");
 
```

يعرض كيفية إدراج صورة WebP.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.insertImage(getImageDir() + "WebP image.webp");

 doc.save(getArtifactsDir() + "Image.InsertWebpImage.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| fileName | java.lang.String | الملف الذي يحتوي على الصورة. يمكن أن يكون أي URI محلي أو بعيد صالح. |

**Returns:**
[Shape](../../com.aspose.words/shape/) - The image node that was just inserted.
### insertImage(String fileName, double width, double height) {#insertImage-java.lang.String-double-double}
```
public Shape insertImage(String fileName, double width, double height)
```


إدراج صورة مدمجة من ملف أو عنوان URL في المستند وتغيير حجمها إلى الحجم المحدد.

 **Remarks:** 

يمكنك تغيير حجم الصورة وموقعها وطريقة التموضع وإعدادات أخرى باستخدام كائن [Shape](../../com.aspose.words/shape/) الذي تُعيده هذه الطريقة.

 **Examples:** 

يعرض كيفية إدراج صورة من نظام الملفات المحلي في مستند.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Below are three ways of inserting an image from a local system filename.
 // 1 -  Inline shape with a default size based on the image's original dimensions:
 builder.insertImage(getImageDir() + "Logo.jpg");

 builder.insertBreak(BreakType.PAGE_BREAK);

 // 2 -  Inline shape with custom dimensions:
 builder.insertImage(getImageDir() + "Transparent background logo.png", ConvertUtil.pixelToPoint(250.0),
         ConvertUtil.pixelToPoint(144.0));

 builder.insertBreak(BreakType.PAGE_BREAK);

 // 3 -  Floating shape with custom dimensions:
 builder.insertImage(getImageDir() + "Windows MetaFile.wmf", RelativeHorizontalPosition.MARGIN, 100.0,
         RelativeVerticalPosition.MARGIN, 100.0, 200.0, 100.0, WrapType.SQUARE);

 doc.save(getArtifactsDir() + "DocumentBuilderImages.InsertImageFromFilename.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| fileName | java.lang.String | الملف الذي يحتوي على الصورة. |
| العرض | double | عرض الصورة بالنقاط. يمكن أن يكون قيمة سالبة أو صفر لطلب مقياس 100٪. |
| الارتفاع | double | ارتفاع الصورة بالنقاط. يمكن أن يكون قيمة سالبة أو صفر لطلب مقياس 100٪. |

**Returns:**
[Shape](../../com.aspose.words/shape/) - The image node that was just inserted.
### insertImage(String fileName, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType) {#insertImage-java.lang.String-int-double-int-double-double-double-int}
```
public Shape insertImage(String fileName, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| fileName | java.lang.String |  |
| horzPos | int |  |
| left | double |  |
| vertPos | int |  |
| top | double |  |
| العرض | double |  |
| الارتفاع | double |  |
| wrapType | int |  |

**Returns:**
[Shape](../../com.aspose.words/shape/)
### insertNode(Node node) {#insertNode-com.aspose.words.Node}
```
public void insertNode(Node node)
```


إدراج عقدة قبل المؤشر.

 **Examples:** 

يوضح كيفية إدراج صورة مربوطة في مستند.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 String imageFileName = getImageDir() + "Windows MetaFile.wmf";

 // Below are two ways of applying an image to a shape so that it can display it.
 // 1 -  Set the shape to contain the image.
 Shape shape = new Shape(builder.getDocument(), ShapeType.IMAGE);
 shape.setWrapType(WrapType.INLINE);
 shape.getImageData().setImage(imageFileName);

 builder.insertNode(shape);

 doc.save(getArtifactsDir() + "Image.CreateLinkedImage.Embedded.docx");

 // Every image that we store in shape will increase the size of our document.
 Assert.assertTrue(new File(getArtifactsDir() + "Image.CreateLinkedImage.Embedded.docx").length() > 70000);

 doc.getFirstSection().getBody().getFirstParagraph().removeAllChildren();

 // 2 -  Set the shape to link to an image file in the local file system.
 shape = new Shape(builder.getDocument(), ShapeType.IMAGE);
 shape.setWrapType(WrapType.INLINE);
 shape.getImageData().setSourceFullName(imageFileName);

 builder.insertNode(shape);
 doc.save(getArtifactsDir() + "Image.CreateLinkedImage.Linked.docx");

 // Linking to images will save space and result in a smaller document.
 // However, the document can only display the image correctly while
 // the image file is present at the location that the shape's "SourceFullName" property points to.
 Assert.assertTrue(new File(getArtifactsDir() + "Image.CreateLinkedImage.Linked.docx").length() < 10000);
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| node | [Node](../../com.aspose.words/node/) |  |

### insertOleObject(InputStream stream, String progId, boolean asIcon, InputStream presentation) {#insertOleObject-java.io.InputStream-java.lang.String-boolean-java.io.InputStream}
```
public Shape insertOleObject(InputStream stream, String progId, boolean asIcon, InputStream presentation)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| stream | java.io.InputStream |  |
| progId | java.lang.String |  |
| asIcon | boolean |  |
| presentation | java.io.InputStream |  |

**Returns:**
[Shape](../../com.aspose.words/shape/)
### insertOleObject(String fileName, boolean isLinked, boolean asIcon, InputStream presentation) {#insertOleObject-java.lang.String-boolean-boolean-java.io.InputStream}
```
public Shape insertOleObject(String fileName, boolean isLinked, boolean asIcon, InputStream presentation)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| fileName | java.lang.String |  |
| isLinked | boolean |  |
| asIcon | boolean |  |
| presentation | java.io.InputStream |  |

**Returns:**
[Shape](../../com.aspose.words/shape/)
### insertOleObject(String fileName, String progId, boolean isLinked, boolean asIcon, InputStream presentation) {#insertOleObject-java.lang.String-java.lang.String-boolean-boolean-java.io.InputStream}
```
public Shape insertOleObject(String fileName, String progId, boolean isLinked, boolean asIcon, InputStream presentation)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| fileName | java.lang.String |  |
| progId | java.lang.String |  |
| isLinked | boolean |  |
| asIcon | boolean |  |
| presentation | java.io.InputStream |  |

**Returns:**
[Shape](../../com.aspose.words/shape/)
### insertOleObjectAsIcon(InputStream stream, String progId, String iconFile, String iconCaption) {#insertOleObjectAsIcon-java.io.InputStream-java.lang.String-java.lang.String-java.lang.String}
```
public Shape insertOleObjectAsIcon(InputStream stream, String progId, String iconFile, String iconCaption)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| stream | java.io.InputStream |  |
| progId | java.lang.String |  |
| iconFile | java.lang.String |  |
| iconCaption | java.lang.String |  |

**Returns:**
[Shape](../../com.aspose.words/shape/)
### insertOleObjectAsIcon(String fileName, boolean isLinked, String iconFile, String iconCaption) {#insertOleObjectAsIcon-java.lang.String-boolean-java.lang.String-java.lang.String}
```
public Shape insertOleObjectAsIcon(String fileName, boolean isLinked, String iconFile, String iconCaption)
```


يدرج كائن OLE مضمّن أو مرتبط كأيقونة في المستند. يسمح بتحديد ملف الأيقونة والتسمية التوضيحية. يكتشف نوع كائن OLE باستخدام امتداد الملف.

 **Examples:** 

يعرض كيفية إدراج كائن OLE في مستند.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // OLE objects are links to files in our local file system that can be opened by other installed applications.
 // Double clicking these shapes will launch the application, and then use it to open the linked object.
 // There are three ways of using the InsertOleObject method to insert these shapes and configure their appearance.
 // If 'presentation' is omitted and 'asIcon' is set, this overloaded method selects
 // the icon according to the file extension and uses the filename for the icon caption.
 // 1 -  Image taken from the local file system:
 builder.insertOleObject(getMyDir() + "Spreadsheet.xlsx", false, false, new FileInputStream(getImageDir() + "Logo.jpg"));

 // If 'presentation' is omitted and 'asIcon' is set, this overloaded method selects
 // the icon according to 'progId' and uses the filename for the icon caption.
 // 2 -  Icon based on the application that will open the object:
 builder.insertOleObject(getMyDir() + "Spreadsheet.xlsx", "Excel.Sheet", false, true, new FileInputStream(getImageDir() + "Logo.jpg"));

 // If 'iconFile' and 'iconCaption' are omitted, this overloaded method selects
 // the icon according to 'progId' and uses the predefined icon caption.
 // 3 -  Image icon that's 32 x 32 pixels or smaller from the local file system, with a custom caption:
 builder.insertOleObjectAsIcon(getMyDir() + "Presentation.pptx", false, getImageDir() + "Logo icon.ico",
         "Double click to view presentation!");

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertOleObject.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| fileName | java.lang.String | المسار الكامل إلى الملف. |
| isLinked | boolean | إذا  true  فسيتم إدراج كائن OLE مرتبط وإلا سيتم إدراج كائن OLE مضمّن. |
| iconFile | java.lang.String | المسار الكامل إلى ملف ICO. إذا كانت القيمة  null , ستستخدم Aspose.Words صورة معرفة مسبقًا. |
| iconCaption | java.lang.String | تسمية الأيقونة. إذا كانت القيمة  null , ستستخدم Aspose.Words اسم الملف. |

**Returns:**
[Shape](../../com.aspose.words/shape/) - Shape node containing Ole object and inserted at the current Builder position.
### insertOleObjectAsIcon(String fileName, String progId, boolean isLinked, String iconFile, String iconCaption) {#insertOleObjectAsIcon-java.lang.String-java.lang.String-boolean-java.lang.String-java.lang.String}
```
public Shape insertOleObjectAsIcon(String fileName, String progId, boolean isLinked, String iconFile, String iconCaption)
```


يدرج كائن OLE مضمّن أو مرتبط كأيقونة في المستند. يسمح بتحديد ملف الأيقونة والتسمية التوضيحية. يكتشف نوع كائن OLE باستخدام معلمة progID المعطاة.

 **Examples:** 

يعرض كيفية إدراج كائن OLE مضمّن أو مرتبط كأيقونة في المستند.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // If 'iconFile' and 'iconCaption' are omitted, this overloaded method selects
 // the icon according to 'progId' and uses the filename for the icon caption.
 builder.insertOleObjectAsIcon(getMyDir() + "Presentation.pptx", "Package", false, getImageDir() + "Logo icon.ico", "My embedded file");

 builder.insertBreak(BreakType.LINE_BREAK);

 try (FileInputStream stream = new FileInputStream(getMyDir() + "Presentation.pptx")) {
     // If 'iconFile' and 'iconCaption' are omitted, this overloaded method selects
     // the icon according to the file extension and uses the filename for the icon caption.
     Shape shape = builder.insertOleObjectAsIcon(stream, "PowerPoint.Application", getImageDir() + "Logo icon.ico",
             "My embedded file stream");

     OlePackage setOlePackage = shape.getOleFormat().getOlePackage();
     setOlePackage.setFileName("Presentation.pptx");
     setOlePackage.setDisplayName("Presentation.pptx");
 }

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertOleObjectAsIcon.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| fileName | java.lang.String | المسار الكامل إلى الملف. |
| progId | java.lang.String | ProgId لكائن OLE. |
| isLinked | boolean | إذا  true  فسيتم إدراج كائن OLE مرتبط وإلا سيتم إدراج كائن OLE مضمّن. |
| iconFile | java.lang.String | المسار الكامل إلى ملف ICO. إذا كانت القيمة  null , ستستخدم Aspose.Words صورة معرفة مسبقًا. |
| iconCaption | java.lang.String | تسمية الأيقونة. إذا كانت القيمة  null , ستستخدم Aspose.Words اسم الملف. |

**Returns:**
[Shape](../../com.aspose.words/shape/) - Shape node containing Ole object and inserted at the current Builder position.
### insertOnlineVideo(String videoUrl, double width, double height) {#insertOnlineVideo-java.lang.String-double-double}
```
public Shape insertOnlineVideo(String videoUrl, double width, double height)
```


إدراج كائن فيديو عبر الإنترنت في المستند وتغيير حجمها إلى الحجم المحدد.

 **Remarks:** 

يمكنك تغيير حجم الصورة وموقعها وطريقة التموضع وإعدادات أخرى باستخدام كائن [Shape](../../com.aspose.words/shape/) الذي تُعيده هذه الطريقة.

يتم دعم إدراج فيديو عبر الإنترنت من الموارد التالية:

 *  https://www.youtube.com/
 *  https://vimeo.com/

إذا لم يتم عرض الفيديو عبر الإنترنت بشكل صحيح، استخدم [insertOnlineVideo(java.lang.String, java.lang.String, byte[], double, double)](../../com.aspose.words/documentbuilder/\#insertOnlineVideo-java.lang.String--java.lang.String--byte----double--double)، الذي يقبل كود HTML مضمّن مخصص.

قد يختلف كود تضمين الفيديو بين المزودين، استشر المزود المناسب لك للحصول على التفاصيل.

 **Examples:** 

يعرض كيفية إدراج فيديو عبر الإنترنت في مستند باستخدام عنوان URL.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.insertOnlineVideo("https://youtu.be/g1N9ke8Prmk", 360.0, 270.0);

 // We can watch the video from Microsoft Word by clicking on the shape.
 doc.save(getArtifactsDir() + "DocumentBuilder.InsertVideoWithUrl.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| videoUrl | java.lang.String | عنوان URL للفيديو. |
| العرض | double | عرض الصورة بالنقاط. يمكن أن يكون قيمة سالبة أو صفر لطلب مقياس 100٪. |
| الارتفاع | double | ارتفاع الصورة بالنقاط. يمكن أن يكون قيمة سالبة أو صفر لطلب مقياس 100٪. |

**Returns:**
[Shape](../../com.aspose.words/shape/) - The image node that was just inserted.
### insertOnlineVideo(String videoUrl, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType) {#insertOnlineVideo-java.lang.String-int-double-int-double-double-double-int}
```
public Shape insertOnlineVideo(String videoUrl, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| videoUrl | java.lang.String |  |
| horzPos | int |  |
| left | double |  |
| vertPos | int |  |
| top | double |  |
| العرض | double |  |
| الارتفاع | double |  |
| wrapType | int |  |

**Returns:**
[Shape](../../com.aspose.words/shape/)
### insertOnlineVideo(String videoUrl, String videoEmbedCode, byte[] thumbnailImageBytes, double width, double height) {#insertOnlineVideo-java.lang.String-java.lang.String-byte---double-double}
```
public Shape insertOnlineVideo(String videoUrl, String videoEmbedCode, byte[] thumbnailImageBytes, double width, double height)
```


إدراج كائن فيديو عبر الإنترنت في المستند وتغيير حجمها إلى الحجم المحدد.

 **Remarks:** 

يمكنك تغيير حجم الصورة وموقعها وطريقة التموضع وإعدادات أخرى باستخدام كائن [Shape](../../com.aspose.words/shape/) الذي تُعيده هذه الطريقة.

 **Examples:** 

يوضح كيفية إدراج فيديو عبر الإنترنت في مستند مع صورة مصغرة مخصصة.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 String videoUrl = "https://vimeo.com/52477838";
 String videoEmbedCode = "";

 byte[] thumbnailImageBytes = IOUtils.toByteArray(getImageUri().toURL().openStream());

 BufferedImage image = ImageIO.read(new ByteArrayInputStream(thumbnailImageBytes));

 // Below are two ways of creating a shape with a custom thumbnail, which links to an online video
 // that will play when we click on the shape in Microsoft Word.
 // 1 -  Insert an inline shape at the builder's node insertion cursor:
 builder.insertOnlineVideo(videoUrl, videoEmbedCode, thumbnailImageBytes, image.getWidth(), image.getHeight());

 builder.insertBreak(BreakType.PAGE_BREAK);

 // 2 -  Insert a floating shape:
 double left = builder.getPageSetup().getRightMargin() - image.getWidth();
 double top = builder.getPageSetup().getBottomMargin() - image.getHeight();

 builder.insertOnlineVideo(videoUrl, videoEmbedCode, thumbnailImageBytes,
         RelativeHorizontalPosition.RIGHT_MARGIN, left, RelativeVerticalPosition.BOTTOM_MARGIN, top,
         image.getWidth(), image.getHeight(), WrapType.SQUARE);

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertOnlineVideoCustomThumbnail.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| videoUrl | java.lang.String | عنوان URL للفيديو. |
| videoEmbedCode | java.lang.String | كود التضمين للفيديو. |
| thumbnailImageBytes | byte[] | بايتات صورة المصغرة. |
| العرض | double | عرض الصورة بالنقاط. يمكن أن يكون قيمة سالبة أو صفر لطلب مقياس 100٪. |
| الارتفاع | double | ارتفاع الصورة بالنقاط. يمكن أن يكون قيمة سالبة أو صفر لطلب مقياس 100٪. |

**Returns:**
[Shape](../../com.aspose.words/shape/) - The image node that was just inserted.
### insertOnlineVideo(String videoUrl, String videoEmbedCode, byte[] thumbnailImageBytes, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType) {#insertOnlineVideo-java.lang.String-java.lang.String-byte---int-double-int-double-double-double-int}
```
public Shape insertOnlineVideo(String videoUrl, String videoEmbedCode, byte[] thumbnailImageBytes, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| videoUrl | java.lang.String |  |
| videoEmbedCode | java.lang.String |  |
| thumbnailImageBytes | byte[] |  |
| horzPos | int |  |
| left | double |  |
| vertPos | int |  |
| top | double |  |
| العرض | double |  |
| الارتفاع | double |  |
| wrapType | int |  |

**Returns:**
[Shape](../../com.aspose.words/shape/)
### insertParagraph() {#insertParagraph}
```
public Paragraph insertParagraph()
```


يدرج فاصل فقرة في المستند.

 **Remarks:** 

يتم استخدام تنسيق الفقرة الحالي المحدد بواسطة الخاصية [getParagraphFormat()](../../com.aspose.words/documentbuilder/\#getParagraphFormat).

يقسم الفقرة الحالية إلى جزأين. بعد إدراج الفقرة، يُوضع المؤشر في بداية الفقرة الجديدة.

يتم إلقاء استثناء إذا لم يكن من الممكن إدراج فاصل فقرة في موضع المؤشر الحالي.

 **Examples:** 

يوضح كيفية إدراج فقرة في المستند.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Font font = builder.getFont();
 font.setSize(16.0);
 font.setBold(true);
 font.setColor(Color.BLUE);
 font.setName("Arial");
 font.setUnderline(Underline.DASH);

 ParagraphFormat paragraphFormat = builder.getParagraphFormat();
 paragraphFormat.setFirstLineIndent(8.0);
 paragraphFormat.setAlignment(ParagraphAlignment.JUSTIFY);
 paragraphFormat.setAddSpaceBetweenFarEastAndAlpha(true);
 paragraphFormat.setAddSpaceBetweenFarEastAndDigit(true);
 paragraphFormat.setKeepTogether(true);

 // The "Writeln" method ends the paragraph after appending text
 // and then starts a new line, adding a new paragraph.
 builder.writeln("Hello world!");

 Assert.assertTrue(builder.getCurrentParagraph().isEndOfDocument());
 
```

**Returns:**
[Paragraph](../../com.aspose.words/paragraph/) - The paragraph node that was just inserted. It is the same node as [getCurrentParagraph()](../../com.aspose.words/documentbuilder/\#getCurrentParagraph).
### insertShape(int shapeType, double width, double height) {#insertShape-int-double-double}
```
public Shape insertShape(int shapeType, double width, double height)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| shapeType | int |  |
| العرض | double |  |
| الارتفاع | double |  |

**Returns:**
[Shape](../../com.aspose.words/shape/)
### insertShape(int shapeType, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType) {#insertShape-int-int-double-int-double-double-double-int}
```
public Shape insertShape(int shapeType, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| shapeType | int |  |
| horzPos | int |  |
| left | double |  |
| vertPos | int |  |
| top | double |  |
| العرض | double |  |
| الارتفاع | double |  |
| wrapType | int |  |

**Returns:**
[Shape](../../com.aspose.words/shape/)
### insertSignatureLine(SignatureLineOptions signatureLineOptions) {#insertSignatureLine-com.aspose.words.SignatureLineOptions}
```
public Shape insertSignatureLine(SignatureLineOptions signatureLineOptions)
```


يدرج سطر توقيع في الموضع الحالي.

 **Examples:** 

يعرض كيفية توقيع مستند بشهادة شخصية وسطر توقيع.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 SignatureLineOptions signatureLineOptions = new SignatureLineOptions();
 signatureLineOptions.setSigner("vderyushev");
 signatureLineOptions.setSignerTitle("QA");
 signatureLineOptions.setEmail("vderyushev@aspose.com");
 signatureLineOptions.setShowDate(true);
 signatureLineOptions.setDefaultInstructions(false);
 signatureLineOptions.setInstructions("Please sign here.");
 signatureLineOptions.setAllowComments(true);

 SignatureLine signatureLine = builder.insertSignatureLine(signatureLineOptions).getSignatureLine();
 signatureLine.setProviderId(UUID.fromString("CF5A7BB4-8F3C-4756-9DF6-BEF7F13259A2"));

 Assert.assertFalse(signatureLine.isSigned());
 Assert.assertFalse(signatureLine.isValid());

 doc.save(getArtifactsDir() + "DocumentBuilder.SignatureLineProviderId.docx");

 Date currentDate = new Date();

 SignOptions signOptions = new SignOptions();
 signOptions.setSignatureLineId(signatureLine.getId());
 signOptions.setProviderId(signatureLine.getProviderId());
 signOptions.setComments("Document was signed by vderyushev");
 signOptions.setSignTime(currentDate);

 CertificateHolder certHolder = CertificateHolder.create(getMyDir() + "morzal.pfx", "aw");

 DigitalSignatureUtil.sign(getArtifactsDir() + "DocumentBuilder.SignatureLineProviderId.docx",
         getArtifactsDir() + "DocumentBuilder.SignatureLineProviderId.Signed.docx", certHolder, signOptions);

 // Re-open our saved document, and verify that the "IsSigned" and "IsValid" properties both equal "true",
 // indicating that the signature line contains a signature.
 doc = new Document(getArtifactsDir() + "DocumentBuilder.SignatureLineProviderId.Signed.docx");
 Shape shape = (Shape) doc.getChild(NodeType.SHAPE, 0, true);
 signatureLine = shape.getSignatureLine();

 Assert.assertTrue(signatureLine.isSigned());
 Assert.assertTrue(signatureLine.isValid());
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| signatureLineOptions | [SignatureLineOptions](../../com.aspose.words/signaturelineoptions/) | الكائن الذي يخزن معلمات إنشاء سطر التوقيع. |

**Returns:**
[Shape](../../com.aspose.words/shape/) - The signature line node that was just inserted.
### insertSignatureLine(SignatureLineOptions signatureLineOptions, int horzPos, double left, int vertPos, double top, int wrapType) {#insertSignatureLine-com.aspose.words.SignatureLineOptions-int-double-int-double-int}
```
public Shape insertSignatureLine(SignatureLineOptions signatureLineOptions, int horzPos, double left, int vertPos, double top, int wrapType)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| signatureLineOptions | [SignatureLineOptions](../../com.aspose.words/signaturelineoptions/) |  |
| horzPos | int |  |
| left | double |  |
| vertPos | int |  |
| top | double |  |
| wrapType | int |  |

**Returns:**
[Shape](../../com.aspose.words/shape/)
### insertStructuredDocumentTag(int type) {#insertStructuredDocumentTag-int}
```
public StructuredDocumentTag insertStructuredDocumentTag(int type)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| نوع | int |  |

**Returns:**
[StructuredDocumentTag](../../com.aspose.words/structureddocumenttag/)
### insertStyleSeparator() {#insertStyleSeparator}
```
public void insertStyleSeparator()
```


يدرج فاصل نمط في المستند.

 **Remarks:** 

تسمح هذه الطريقة بتطبيق أنماط فقرة مختلفة على جزأين مختلفين من سطر النص.

 **Examples:** 

يوضح كيفية العمل مع فواصل الأنماط.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Each paragraph can only have one style.
 // The InsertStyleSeparator method allows us to work around this limitation.
 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_1);
 builder.write("This text is in a Heading style. ");
 builder.insertStyleSeparator();

 Style paraStyle = builder.getDocument().getStyles().add(StyleType.PARAGRAPH, "MyParaStyle");
 paraStyle.getFont().setBold(false);
 paraStyle.getFont().setSize(8.0);
 paraStyle.getFont().setName("Arial");

 builder.getParagraphFormat().setStyleName(paraStyle.getName());
 builder.write("This text is in a custom style. ");

 // Calling the InsertStyleSeparator method creates another paragraph,
 // which can have a different style to the previous. There will be no break between paragraphs.
 // The text in the output document will look like one paragraph with two styles.
 Assert.assertEquals(2, doc.getFirstSection().getBody().getParagraphs().getCount());
 Assert.assertEquals("Heading 1", doc.getFirstSection().getBody().getParagraphs().get(0).getParagraphFormat().getStyle().getName());
 Assert.assertEquals("MyParaStyle", doc.getFirstSection().getBody().getParagraphs().get(1).getParagraphFormat().getStyle().getName());

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertStyleSeparator.docx");
 
```

### insertTableOfContents(String switches) {#insertTableOfContents-java.lang.String}
```
public Field insertTableOfContents(String switches)
```


يدرج حقل فهرس (جدول المحتويات) في المستند.

 **Remarks:** 

تقوم هذه الطريقة بإدراج حقل فهرس (TOC) في المستند في الموضع الحالي.

يمكن بناء فهرس في مستند Word بعدة طرق وتنسيقه باستخدام مجموعة متنوعة من الخيارات. طريقة بناء الفهرس وعرضه في Microsoft Word يتم التحكم فيها بواسطة مفاتيح الحقل.

أسهل طريقة لتحديد المفاتيح هي إدراج وتكوين فهرس في مستند Word باستخدام قائمة Insert->Reference->Index and Tables، ثم تشغيل عرض رموز الحقول لرؤية المفاتيح. يمكنك الضغط على Alt+F9 في Microsoft Word لتبديل عرض رموز الحقول تشغيلًا أو إيقافًا.

على سبيل المثال، بعد إنشاء فهرس، يتم إدراج الحقل التالي في المستند: **\{ TOC \\o "1-3" \\h \\z \}**. يمكنك نسخ **\\o "1-3" \\h \\z** واستخدامه كمعامل للمفاتيح.

لاحظ أن [insertTableOfContents(java.lang.String)](../../com.aspose.words/documentbuilder/\#insertTableOfContents-java.lang.String) سيقوم فقط بإدراج حقل TOC، لكنه لن يبني الفهرس فعليًا. يتم بناء الفهرس بواسطة Microsoft Word عندما يتم تحديث الحقل.

إذا قمت بإدراج فهرس باستخدام هذه الطريقة ثم فتحت الملف في Microsoft Word، لن ترى الفهرس لأن حقل TOC لم يتم تحديثه بعد.

في Microsoft Word، لا يتم تحديث الحقول تلقائيًا عند فتح المستند، ولكن يمكنك تحديث الحقول في أي وقت بالضغط على F9.

 **Examples:** 

يوضح كيفية إدراج جدول محتويات (TOC) في المستند باستخدام أنماط العناوين كعناصر.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a table of contents for the first page of the document.
 // Configure the table to pick up paragraphs with headings of levels 1 to 3.
 // Also, set its entries to be hyperlinks that will take us
 // to the location of the heading when left-clicked in Microsoft Word.
 builder.insertTableOfContents("\\o \"1-3\" \\h \\z \\u");
 builder.insertBreak(BreakType.PAGE_BREAK);

 // Populate the table of contents by adding paragraphs with heading styles.
 // Each such heading with a level between 1 and 3 will create an entry in the table.
 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_1);
 builder.writeln("Heading 1");

 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_2);
 builder.writeln("Heading 1.1");
 builder.writeln("Heading 1.2");

 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_1);
 builder.writeln("Heading 2");
 builder.writeln("Heading 3");

 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_2);
 builder.writeln("Heading 3.1");

 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_3);
 builder.writeln("Heading 3.1.1");
 builder.writeln("Heading 3.1.2");
 builder.writeln("Heading 3.1.3");

 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_4);
 builder.writeln("Heading 3.1.3.1");
 builder.writeln("Heading 3.1.3.2");

 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_2);
 builder.writeln("Heading 3.2");
 builder.writeln("Heading 3.3");

 // A table of contents is a field of a type that needs to be updated to show an up-to-date result.
 doc.updateFields();
 doc.save(getArtifactsDir() + "DocumentBuilder.InsertToc.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| المفاتيح | java.lang.String | مفاتيح حقل TOC. |

**Returns:**
[Field](../../com.aspose.words/field/)
### insertTextInput(String name, int type, String format, String fieldValue, int maxLength) {#insertTextInput-java.lang.String-int-java.lang.String-java.lang.String-int}
```
public FormField insertTextInput(String name, int type, String format, String fieldValue, int maxLength)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| الاسم | java.lang.String |  |
| نوع | int |  |
| التنسيق | java.lang.String |  |
| fieldValue | java.lang.String |  |
| maxLength | int |  |

**Returns:**
[FormField](../../com.aspose.words/formfield/)
### isAtEndOfParagraph() {#isAtEndOfParagraph}
```
public boolean isAtEndOfParagraph()
```


يرجع  true  إذا كان المؤشر في نهاية الفقرة الحالية.

 **Examples:** 

يعرض كيفية نقل مؤشر منشئ المستند إلى عقد مختلفة في المستند.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create a valid bookmark, an entity that consists of nodes enclosed by a bookmark start node,
 // and a bookmark end node.
 builder.startBookmark("MyBookmark");
 builder.write("Bookmark contents.");
 builder.endBookmark("MyBookmark");

 NodeCollection firstParagraphNodes = doc.getFirstSection().getBody().getFirstParagraph().getChildNodes(NodeType.ANY, false);

 Assert.assertEquals(NodeType.BOOKMARK_START, firstParagraphNodes.get(0).getNodeType());
 Assert.assertEquals(NodeType.RUN, firstParagraphNodes.get(1).getNodeType());
 Assert.assertEquals("Bookmark contents.", firstParagraphNodes.get(1).getText().trim());
 Assert.assertEquals(NodeType.BOOKMARK_END, firstParagraphNodes.get(2).getNodeType());

 // The document builder's cursor is always ahead of the node that we last added with it.
 // If the builder's cursor is at the end of the document, its current node will be null.
 // The previous node is the bookmark end node that we last added.
 // Adding new nodes with the builder will append them to the last node.
 Assert.assertNull(builder.getCurrentNode());

 // If we wish to edit a different part of the document with the builder,
 // we will need to bring its cursor to the node we wish to edit.
 builder.moveToBookmark("MyBookmark");

 // Moving it to a bookmark will move it to the first node within the bookmark start and end nodes, the enclosed run.
 Assert.assertEquals(firstParagraphNodes.get(1), builder.getCurrentNode());

 // We can also move the cursor to an individual node like this.
 builder.moveTo(doc.getFirstSection().getBody().getFirstParagraph().getChildNodes(NodeType.ANY, false).get(0));

 Assert.assertEquals(NodeType.BOOKMARK_START, builder.getCurrentNode().getNodeType());
 Assert.assertEquals(doc.getFirstSection().getBody().getFirstParagraph(), builder.getCurrentParagraph());
 Assert.assertTrue(builder.isAtStartOfParagraph());

 // We can use specific methods to move to the start/end of a document.
 builder.moveToDocumentEnd();

 Assert.assertTrue(builder.isAtEndOfParagraph());

 builder.moveToDocumentStart();

 Assert.assertTrue(builder.isAtStartOfParagraph());
 
```

**Returns:**
منطقي -  true  إذا كان المؤشر في نهاية الفقرة الحالية.
### isAtEndOfStructuredDocumentTag() {#isAtEndOfStructuredDocumentTag}
```
public boolean isAtEndOfStructuredDocumentTag()
```


يرجع **true** إذا كان المؤشر في نهاية علامة مستند منسقة.

 **Examples:** 

يعرض كيفية نقل مؤشر DocumentBuilder داخل علامة مستند منسقة.

```

 Document doc = new Document(getMyDir() + "Structured document tags.docx");
 DocumentBuilder builder = new DocumentBuilder(doc);

 // There is a several ways to move the cursor:
 // 1 -  Move to the first character of structured document tag by index.
 builder.moveToStructuredDocumentTag(1, 1);

 // 2 -  Move to the first character of structured document tag by object.
 StructuredDocumentTag tag = (StructuredDocumentTag)doc.getChild(NodeType.STRUCTURED_DOCUMENT_TAG, 2, true);
 builder.moveToStructuredDocumentTag(tag, 1);
 builder.write(" New text.");

 Assert.assertEquals("R New text.ichText", tag.getText().trim());

 // 3 -  Move to the end of the second structured document tag.
 builder.moveToStructuredDocumentTag(1, -1);
 Assert.assertTrue(builder.isAtEndOfStructuredDocumentTag());

 // Get currently selected structured document tag.
 builder.getCurrentStructuredDocumentTag().setColor(Color.GREEN);

 doc.save(getArtifactsDir() + "Document.MoveToStructuredDocumentTag.docx");
 
```

**Returns:**
منطقي - **true** إذا كان المؤشر في نهاية علامة مستند منسقة.
### isAtStartOfParagraph() {#isAtStartOfParagraph}
```
public boolean isAtStartOfParagraph()
```


يرجع  true  إذا كان المؤشر في بداية الفقرة الحالية (لا يوجد نص قبل المؤشر).

 **Examples:** 

يعرض كيفية نقل مؤشر منشئ المستند إلى عقد مختلفة في المستند.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create a valid bookmark, an entity that consists of nodes enclosed by a bookmark start node,
 // and a bookmark end node.
 builder.startBookmark("MyBookmark");
 builder.write("Bookmark contents.");
 builder.endBookmark("MyBookmark");

 NodeCollection firstParagraphNodes = doc.getFirstSection().getBody().getFirstParagraph().getChildNodes(NodeType.ANY, false);

 Assert.assertEquals(NodeType.BOOKMARK_START, firstParagraphNodes.get(0).getNodeType());
 Assert.assertEquals(NodeType.RUN, firstParagraphNodes.get(1).getNodeType());
 Assert.assertEquals("Bookmark contents.", firstParagraphNodes.get(1).getText().trim());
 Assert.assertEquals(NodeType.BOOKMARK_END, firstParagraphNodes.get(2).getNodeType());

 // The document builder's cursor is always ahead of the node that we last added with it.
 // If the builder's cursor is at the end of the document, its current node will be null.
 // The previous node is the bookmark end node that we last added.
 // Adding new nodes with the builder will append them to the last node.
 Assert.assertNull(builder.getCurrentNode());

 // If we wish to edit a different part of the document with the builder,
 // we will need to bring its cursor to the node we wish to edit.
 builder.moveToBookmark("MyBookmark");

 // Moving it to a bookmark will move it to the first node within the bookmark start and end nodes, the enclosed run.
 Assert.assertEquals(firstParagraphNodes.get(1), builder.getCurrentNode());

 // We can also move the cursor to an individual node like this.
 builder.moveTo(doc.getFirstSection().getBody().getFirstParagraph().getChildNodes(NodeType.ANY, false).get(0));

 Assert.assertEquals(NodeType.BOOKMARK_START, builder.getCurrentNode().getNodeType());
 Assert.assertEquals(doc.getFirstSection().getBody().getFirstParagraph(), builder.getCurrentParagraph());
 Assert.assertTrue(builder.isAtStartOfParagraph());

 // We can use specific methods to move to the start/end of a document.
 builder.moveToDocumentEnd();

 Assert.assertTrue(builder.isAtEndOfParagraph());

 builder.moveToDocumentStart();

 Assert.assertTrue(builder.isAtStartOfParagraph());
 
```

**Returns:**
منطقي -  true  إذا كان المؤشر في بداية الفقرة الحالية (لا يوجد نص قبل المؤشر).
### moveTo(Node node) {#moveTo-com.aspose.words.Node}
```
public void moveTo(Node node)
```


ينقل المؤشر إلى عقدة مضمنة أو إلى نهاية الفقرة.

 **Remarks:** 

عند كون *node* عقدة من المستوى داخل السطر، يتم نقل المؤشر إلى هذه العقدة وسيتم إدراج المحتوى اللاحق قبل تلك العقدة.

عند كون *node* عبارة عن [Paragraph](../../com.aspose.words/paragraph/)، يتم نقل المؤشر إلى نهاية الفقرة وسيتم إدراج المحتوى اللاحق مباشرةً قبل فاصل الفقرة.

عند كون *node* عقدة من المستوى الكتلي ولكنها ليست [Paragraph](../../com.aspose.words/paragraph/)، يتم نقل المؤشر إلى نهاية الفقرة الأولى داخل عقدة المستوى الكتلي وسيتم إدراج المحتوى اللاحق مباشرةً قبل فاصل الفقرة.

 **Examples:** 

يعرض كيفية نقل مؤشر منشئ المستند إلى عقد مختلفة في المستند.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create a valid bookmark, an entity that consists of nodes enclosed by a bookmark start node,
 // and a bookmark end node.
 builder.startBookmark("MyBookmark");
 builder.write("Bookmark contents.");
 builder.endBookmark("MyBookmark");

 NodeCollection firstParagraphNodes = doc.getFirstSection().getBody().getFirstParagraph().getChildNodes(NodeType.ANY, false);

 Assert.assertEquals(NodeType.BOOKMARK_START, firstParagraphNodes.get(0).getNodeType());
 Assert.assertEquals(NodeType.RUN, firstParagraphNodes.get(1).getNodeType());
 Assert.assertEquals("Bookmark contents.", firstParagraphNodes.get(1).getText().trim());
 Assert.assertEquals(NodeType.BOOKMARK_END, firstParagraphNodes.get(2).getNodeType());

 // The document builder's cursor is always ahead of the node that we last added with it.
 // If the builder's cursor is at the end of the document, its current node will be null.
 // The previous node is the bookmark end node that we last added.
 // Adding new nodes with the builder will append them to the last node.
 Assert.assertNull(builder.getCurrentNode());

 // If we wish to edit a different part of the document with the builder,
 // we will need to bring its cursor to the node we wish to edit.
 builder.moveToBookmark("MyBookmark");

 // Moving it to a bookmark will move it to the first node within the bookmark start and end nodes, the enclosed run.
 Assert.assertEquals(firstParagraphNodes.get(1), builder.getCurrentNode());

 // We can also move the cursor to an individual node like this.
 builder.moveTo(doc.getFirstSection().getBody().getFirstParagraph().getChildNodes(NodeType.ANY, false).get(0));

 Assert.assertEquals(NodeType.BOOKMARK_START, builder.getCurrentNode().getNodeType());
 Assert.assertEquals(doc.getFirstSection().getBody().getFirstParagraph(), builder.getCurrentParagraph());
 Assert.assertTrue(builder.isAtStartOfParagraph());

 // We can use specific methods to move to the start/end of a document.
 builder.moveToDocumentEnd();

 Assert.assertTrue(builder.isAtEndOfParagraph());

 builder.moveToDocumentStart();

 Assert.assertTrue(builder.isAtStartOfParagraph());
 
```

يوضح كيفية نقل موضع مؤشر DocumentBuilder إلى عقدة محددة.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Run 1. ");

 // The document builder has a cursor, which acts as the part of the document
 // where the builder appends new nodes when we use its document construction methods.
 // This cursor functions in the same way as Microsoft Word's blinking cursor,
 // and it also always ends up immediately after any node that the builder just inserted.
 // To append content to a different part of the document,
 // we can move the cursor to a different node with the "MoveTo" method.
 builder.moveTo(doc.getFirstSection().getBody().getFirstParagraph().getRuns().get(0));
 // The cursor is now in front of the node that we moved it to.
 // Adding a second run will insert it in front of the first run.
 builder.writeln("Run 2. ");

 Assert.assertEquals("Run 2. \rRun 1.", doc.getText().trim());

 // Move the cursor to the end of the document to continue appending text to the end as before.
 builder.moveTo(doc.getLastSection().getBody().getLastParagraph());
 builder.writeln("Run 3. ");

 Assert.assertEquals("Run 2. \rRun 1. \rRun 3.", doc.getText().trim());
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| node | [Node](../../com.aspose.words/node/) | يجب أن تكون العقدة فقرة أو طفلاً مباشراً لفقرة. |

### moveToBookmark(String bookmarkName) {#moveToBookmark-java.lang.String}
```
public boolean moveToBookmark(String bookmarkName)
```


ينقل المؤشر إلى إشارة مرجعية.

 **Remarks:** 

ينقل المؤشر إلى موضع يقع مباشرةً بعد بداية العلامة المرجعية ذات الاسم المحدد.

المقارنة غير حساسة لحالة الأحرف. إذا لم يتم العثور على العلامة المرجعية، يتم إرجاع  false  ولا يتم نقل المؤشر.

إدراج نص جديد لا يستبدل النص الموجود للعلامة المرجعية.

لاحظ أن بعض العلامات المرجعية في المستند مخصصة لحقول النموذج. الانتقال إلى مثل هذه العلامة المرجعية وإدراج نص هناك يضيف النص إلى شفرة حقل النموذج. على الرغم من أن ذلك لن يبطل صلاحية حقل النموذج، إلا أن النص المدخل لن يكون مرئياً لأنه يصبح جزءاً من شفرة الحقل.

 **Examples:** 

يعرض كيفية نقل مؤشر منشئ المستند إلى عقد مختلفة في المستند.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create a valid bookmark, an entity that consists of nodes enclosed by a bookmark start node,
 // and a bookmark end node.
 builder.startBookmark("MyBookmark");
 builder.write("Bookmark contents.");
 builder.endBookmark("MyBookmark");

 NodeCollection firstParagraphNodes = doc.getFirstSection().getBody().getFirstParagraph().getChildNodes(NodeType.ANY, false);

 Assert.assertEquals(NodeType.BOOKMARK_START, firstParagraphNodes.get(0).getNodeType());
 Assert.assertEquals(NodeType.RUN, firstParagraphNodes.get(1).getNodeType());
 Assert.assertEquals("Bookmark contents.", firstParagraphNodes.get(1).getText().trim());
 Assert.assertEquals(NodeType.BOOKMARK_END, firstParagraphNodes.get(2).getNodeType());

 // The document builder's cursor is always ahead of the node that we last added with it.
 // If the builder's cursor is at the end of the document, its current node will be null.
 // The previous node is the bookmark end node that we last added.
 // Adding new nodes with the builder will append them to the last node.
 Assert.assertNull(builder.getCurrentNode());

 // If we wish to edit a different part of the document with the builder,
 // we will need to bring its cursor to the node we wish to edit.
 builder.moveToBookmark("MyBookmark");

 // Moving it to a bookmark will move it to the first node within the bookmark start and end nodes, the enclosed run.
 Assert.assertEquals(firstParagraphNodes.get(1), builder.getCurrentNode());

 // We can also move the cursor to an individual node like this.
 builder.moveTo(doc.getFirstSection().getBody().getFirstParagraph().getChildNodes(NodeType.ANY, false).get(0));

 Assert.assertEquals(NodeType.BOOKMARK_START, builder.getCurrentNode().getNodeType());
 Assert.assertEquals(doc.getFirstSection().getBody().getFirstParagraph(), builder.getCurrentParagraph());
 Assert.assertTrue(builder.isAtStartOfParagraph());

 // We can use specific methods to move to the start/end of a document.
 builder.moveToDocumentEnd();

 Assert.assertTrue(builder.isAtEndOfParagraph());

 builder.moveToDocumentStart();

 Assert.assertTrue(builder.isAtStartOfParagraph());
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| bookmarkName | java.lang.String | اسم العلامة المرجعية التي يُنقل إليها المؤشر. |

**Returns:**
منطقي -  true  إذا تم العثور على العلامة المرجعية؛  false  خلاف ذلك.
### moveToBookmark(String bookmarkName, boolean isStart, boolean isAfter) {#moveToBookmark-java.lang.String-boolean-boolean}
```
public boolean moveToBookmark(String bookmarkName, boolean isStart, boolean isAfter)
```


ينقل المؤشر إلى إشارة مرجعية بدقة أكبر.

 **Remarks:** 

ينقل المؤشر إلى موضع قبل أو بعد بداية أو نهاية العلامة المرجعية.

إذا لم يكن الموضع المطلوب على مستوى داخل السطر، ينتقل إلى الفقرة التالية.

المقارنة غير حساسة لحالة الأحرف. إذا لم يتم العثور على العلامة المرجعية، يتم إرجاع  false  ولا يتم نقل المؤشر.

 **Examples:** 

يوضح كيفية نقل مؤشر نقطة إدراج عقدة DocumentBuilder إلى علامة مرجعية.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // A valid bookmark consists of a BookmarkStart node, a BookmarkEnd node with a
 // matching bookmark name somewhere afterward, and contents enclosed by those nodes.
 builder.startBookmark("MyBookmark");
 builder.write("Hello world! ");
 builder.endBookmark("MyBookmark");

 // There are 4 ways of moving a document builder's cursor to a bookmark.
 // If we are between the BookmarkStart and BookmarkEnd nodes, the cursor will be inside the bookmark.
 // This means that any text added by the builder will become a part of the bookmark.
 // 1 -  Outside of the bookmark, in front of the BookmarkStart node:
 Assert.assertTrue(builder.moveToBookmark("MyBookmark", true, false));
 builder.write("1. ");

 Assert.assertEquals("Hello world! ", doc.getRange().getBookmarks().get("MyBookmark").getText());
 Assert.assertEquals("1. Hello world!", doc.getText().trim());

 // 2 -  Inside the bookmark, right after the BookmarkStart node:
 Assert.assertTrue(builder.moveToBookmark("MyBookmark", true, true));
 builder.write("2. ");

 Assert.assertEquals("2. Hello world! ", doc.getRange().getBookmarks().get("MyBookmark").getText());
 Assert.assertEquals("1. 2. Hello world!", doc.getText().trim());

 // 2 -  Inside the bookmark, right in front of the BookmarkEnd node:
 Assert.assertTrue(builder.moveToBookmark("MyBookmark", false, false));
 builder.write("3. ");

 Assert.assertEquals("2. Hello world! 3. ", doc.getRange().getBookmarks().get("MyBookmark").getText());
 Assert.assertEquals("1. 2. Hello world! 3.", doc.getText().trim());

 // 4 -  Outside of the bookmark, after the BookmarkEnd node:
 Assert.assertTrue(builder.moveToBookmark("MyBookmark", false, true));
 builder.write("4.");

 Assert.assertEquals("2. Hello world! 3. ", doc.getRange().getBookmarks().get("MyBookmark").getText());
 Assert.assertEquals("1. 2. Hello world! 3. 4.", doc.getText().trim());
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| bookmarkName | java.lang.String | اسم العلامة المرجعية التي يُنقل إليها المؤشر. |
| isStart | boolean | عند  true , ينقل المؤشر إلى بداية العلامة المرجعية. عند  false , ينقل المؤشر إلى نهاية العلامة المرجعية. |
| isAfter | boolean | عند  true , ينقل المؤشر ليكون بعد موضع بداية أو نهاية العلامة المرجعية. عند  false , ينقل المؤشر ليكون قبل موضع بداية أو نهاية العلامة المرجعية. |

**Returns:**
منطقي -  true  إذا تم العثور على العلامة المرجعية؛  false  خلاف ذلك.
### moveToCell(int tableIndex, int rowIndex, int columnIndex, int characterIndex) {#moveToCell-int-int-int-int}
```
public void moveToCell(int tableIndex, int rowIndex, int columnIndex, int characterIndex)
```


ينقل المؤشر إلى خلية جدول في القسم الحالي.

 **Remarks:** 

يتم تنفيذ التنقل داخل القصة الحالية للقسم الحالي.

بالنسبة لمعلمات الفهرس، عندما يكون الفهرس أكبر من أو يساوي 0، فإنه يحدد فهرسًا من البداية حيث 0 هو العنصر الأول. عندما يكون الفهرس أقل من 0، فإنه يحدد فهرسًا من النهاية حيث -1 هو العنصر الأخير.

 **Examples:** 

يوضح كيفية نقل مؤشر DocumentBuilder إلى خلية في جدول.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create an empty 2x2 table.
 builder.startTable();
 builder.insertCell();
 builder.insertCell();
 builder.endRow();
 builder.insertCell();
 builder.insertCell();
 builder.endTable();

 // Because we have ended the table with the EndTable method,
 // the document builder's cursor is currently outside the table.
 // This cursor has the same function as Microsoft Word's blinking text cursor.
 // It can also be moved to a different location in the document using the builder's MoveTo methods.
 // We can move the cursor back inside the table to a specific cell.
 builder.moveToCell(0, 1, 1, 0);
 builder.write("Column 2, cell 2.");

 doc.save(getArtifactsDir() + "DocumentBuilder.MoveToCell.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| tableIndex | int | فهرس الجدول الذي سيتم الانتقال إليه. |
| rowIndex | int | فهرس الصف في الجدول. |
| columnIndex | int | فهرس العمود في الجدول. |
| characterIndex | int | فهرس الحرف داخل الخلية. القيمة السالبة تسمح لك بتحديد موقع من نهاية الخلية. استخدم -1 للتحرك إلى نهاية الخلية. |

### moveToDocumentEnd() {#moveToDocumentEnd}
```
public void moveToDocumentEnd()
```


ينقل المؤشر إلى نهاية المستند.

 **Examples:** 

يعرض كيفية نقل مؤشر منشئ المستند إلى عقد مختلفة في المستند.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create a valid bookmark, an entity that consists of nodes enclosed by a bookmark start node,
 // and a bookmark end node.
 builder.startBookmark("MyBookmark");
 builder.write("Bookmark contents.");
 builder.endBookmark("MyBookmark");

 NodeCollection firstParagraphNodes = doc.getFirstSection().getBody().getFirstParagraph().getChildNodes(NodeType.ANY, false);

 Assert.assertEquals(NodeType.BOOKMARK_START, firstParagraphNodes.get(0).getNodeType());
 Assert.assertEquals(NodeType.RUN, firstParagraphNodes.get(1).getNodeType());
 Assert.assertEquals("Bookmark contents.", firstParagraphNodes.get(1).getText().trim());
 Assert.assertEquals(NodeType.BOOKMARK_END, firstParagraphNodes.get(2).getNodeType());

 // The document builder's cursor is always ahead of the node that we last added with it.
 // If the builder's cursor is at the end of the document, its current node will be null.
 // The previous node is the bookmark end node that we last added.
 // Adding new nodes with the builder will append them to the last node.
 Assert.assertNull(builder.getCurrentNode());

 // If we wish to edit a different part of the document with the builder,
 // we will need to bring its cursor to the node we wish to edit.
 builder.moveToBookmark("MyBookmark");

 // Moving it to a bookmark will move it to the first node within the bookmark start and end nodes, the enclosed run.
 Assert.assertEquals(firstParagraphNodes.get(1), builder.getCurrentNode());

 // We can also move the cursor to an individual node like this.
 builder.moveTo(doc.getFirstSection().getBody().getFirstParagraph().getChildNodes(NodeType.ANY, false).get(0));

 Assert.assertEquals(NodeType.BOOKMARK_START, builder.getCurrentNode().getNodeType());
 Assert.assertEquals(doc.getFirstSection().getBody().getFirstParagraph(), builder.getCurrentParagraph());
 Assert.assertTrue(builder.isAtStartOfParagraph());

 // We can use specific methods to move to the start/end of a document.
 builder.moveToDocumentEnd();

 Assert.assertTrue(builder.isAtEndOfParagraph());

 builder.moveToDocumentStart();

 Assert.assertTrue(builder.isAtStartOfParagraph());
 
```

### moveToDocumentStart() {#moveToDocumentStart}
```
public void moveToDocumentStart()
```


ينقل المؤشر إلى بداية المستند.

 **Examples:** 

يعرض كيفية نقل مؤشر منشئ المستند إلى عقد مختلفة في المستند.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create a valid bookmark, an entity that consists of nodes enclosed by a bookmark start node,
 // and a bookmark end node.
 builder.startBookmark("MyBookmark");
 builder.write("Bookmark contents.");
 builder.endBookmark("MyBookmark");

 NodeCollection firstParagraphNodes = doc.getFirstSection().getBody().getFirstParagraph().getChildNodes(NodeType.ANY, false);

 Assert.assertEquals(NodeType.BOOKMARK_START, firstParagraphNodes.get(0).getNodeType());
 Assert.assertEquals(NodeType.RUN, firstParagraphNodes.get(1).getNodeType());
 Assert.assertEquals("Bookmark contents.", firstParagraphNodes.get(1).getText().trim());
 Assert.assertEquals(NodeType.BOOKMARK_END, firstParagraphNodes.get(2).getNodeType());

 // The document builder's cursor is always ahead of the node that we last added with it.
 // If the builder's cursor is at the end of the document, its current node will be null.
 // The previous node is the bookmark end node that we last added.
 // Adding new nodes with the builder will append them to the last node.
 Assert.assertNull(builder.getCurrentNode());

 // If we wish to edit a different part of the document with the builder,
 // we will need to bring its cursor to the node we wish to edit.
 builder.moveToBookmark("MyBookmark");

 // Moving it to a bookmark will move it to the first node within the bookmark start and end nodes, the enclosed run.
 Assert.assertEquals(firstParagraphNodes.get(1), builder.getCurrentNode());

 // We can also move the cursor to an individual node like this.
 builder.moveTo(doc.getFirstSection().getBody().getFirstParagraph().getChildNodes(NodeType.ANY, false).get(0));

 Assert.assertEquals(NodeType.BOOKMARK_START, builder.getCurrentNode().getNodeType());
 Assert.assertEquals(doc.getFirstSection().getBody().getFirstParagraph(), builder.getCurrentParagraph());
 Assert.assertTrue(builder.isAtStartOfParagraph());

 // We can use specific methods to move to the start/end of a document.
 builder.moveToDocumentEnd();

 Assert.assertTrue(builder.isAtEndOfParagraph());

 builder.moveToDocumentStart();

 Assert.assertTrue(builder.isAtStartOfParagraph());
 
```

### moveToField(Field field, boolean isAfter) {#moveToField-com.aspose.words.Field-boolean}
```
public void moveToField(Field field, boolean isAfter)
```


ينقل المؤشر إلى حقل في المستند.

 **Examples:** 

يوضح كيفية نقل مؤشر نقطة إدراج العقدة في مُنشئ المستند إلى حقل محدد.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a field using the DocumentBuilder and add a run of text after it.
 Field field = builder.insertField(" AUTHOR \"John Doe\" ");

 // The builder's cursor is currently at end of the document.
 Assert.assertNull(builder.getCurrentNode());

 // Move the cursor to the field while specifying whether to place that cursor before or after the field.
 builder.moveToField(field, moveCursorToAfterTheField);

 // Note that the cursor is outside of the field in both cases.
 // This means that we cannot edit the field using the builder like this.
 // To edit a field, we can use the builder's MoveTo method on a field's FieldStart
 // or FieldSeparator node to place the cursor inside.
 if (moveCursorToAfterTheField) {
     Assert.assertNull(builder.getCurrentNode());
     builder.write(" Text immediately after the field.");

     Assert.assertEquals("AUTHOR \"John Doe\" John Doe Text immediately after the field.",
             doc.getText().trim());
 } else {
     Assert.assertEquals(field.getStart(), builder.getCurrentNode());
     builder.write("Text immediately before the field. ");

     Assert.assertEquals("Text immediately before the field.  AUTHOR \"John Doe\" John Doe",
             doc.getText().trim());
 }
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| field | [Field](../../com.aspose.words/field/) | الحقل الذي سيتم نقل المؤشر إليه. |
| isAfter | boolean | عند  true , ينقل المؤشر ليكون بعد نهاية الحقل. عند  false , ينقل المؤشر ليكون قبل بداية الحقل. |

### moveToHeaderFooter(int headerFooterType) {#moveToHeaderFooter-int}
```
public void moveToHeaderFooter(int headerFooterType)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| headerFooterType | int |  |

### moveToMergeField(String fieldName) {#moveToMergeField-java.lang.String}
```
public boolean moveToMergeField(String fieldName)
```


ينقل المؤشر إلى حقل الدمج المحدد.  ينقل المؤشر إلى موقع يبعد قليلاً عن حقل الدمج المحدد ويزيل حقل الدمج.

 **Remarks:** 

لاحظ أن هذه الطريقة تحذف حقل الدمج من المستند بعد نقل المؤشر.

 **Examples:** 

يعرض كيفية ملء حقول MERGEFIELD بالبيانات باستخدام منشئ المستند بدلاً من دمج البريد.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert some MERGEFIELDS, which accept data from columns of the same name in a data source during a mail merge,
 // and then fill them manually.
 builder.insertField(" MERGEFIELD Chairman ");
 builder.insertField(" MERGEFIELD ChiefFinancialOfficer ");
 builder.insertField(" MERGEFIELD ChiefTechnologyOfficer ");

 builder.moveToMergeField("Chairman");
 builder.setBold(true);
 builder.writeln("John Doe");

 builder.moveToMergeField("ChiefFinancialOfficer");
 builder.setItalic(true);
 builder.writeln("Jane Doe");

 builder.moveToMergeField("ChiefTechnologyOfficer");
 builder.setItalic(true);
 builder.writeln("John Bloggs");

 doc.save(getArtifactsDir() + "DocumentBuilder.FillMergeFields.docx");
 
```

يوضح كيفية إدراج حقول نموذج خانة الاختيار في مستند أثناء دمج البريد.

```

 public void insertCheckBox() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     builder.startTable();
     builder.insertCell();
     builder.insertField(" MERGEFIELD  TableStart:StudentCourse ");
     builder.insertCell();
     builder.insertField(" MERGEFIELD  CourseName ");
     builder.insertCell();
     builder.insertField(" MERGEFIELD  TableEnd:StudentCourse ");
     builder.endTable();

     // Add a handler for the MergeField event
     doc.getMailMerge().setFieldMergingCallback(new HandleMergeFieldInsertCheckBox());

     // Execute mail merge with regions
     DataTable dataTable = getStudentCourseDataTable();
     doc.getMailMerge().executeWithRegions(dataTable);

     // Save resulting document with a new name
     doc.save(getArtifactsDir() + "MailMergeEvent.InsertCheckBox.docx");
 }

 private class HandleMergeFieldInsertCheckBox implements IFieldMergingCallback {
     // This is called for each merge field in the document
     // when Document.MailMerge.ExecuteWithRegions is called.
     public void fieldMerging(final FieldMergingArgs args) throws Exception {
         if (args.getDocumentFieldName().equals("CourseName")) {
             // The name of the table that we are merging can be found here
             Assert.assertEquals(args.getTableName(), "StudentCourse");

             // Insert the checkbox for this merge field, using DocumentBuilder
             DocumentBuilder builder = new DocumentBuilder(args.getDocument());
             builder.moveToMergeField(args.getFieldName());
             builder.insertCheckBox(args.getDocumentFieldName() + mCheckBoxCount, false, 0);
             // Get the actual value of the field
             String fieldValue = args.getFieldValue().toString();

             // In this case, for every record index 'n', the corresponding field value is "Course n"
             Assert.assertEquals(args.getRecordIndex(), Character.getNumericValue(fieldValue.charAt(7)));

             builder.write(fieldValue);
             mCheckBoxCount++;
         }
     }

     public void imageFieldMerging(final ImageFieldMergingArgs args) {
         // Do nothing
     }

     // Counter for CheckBox name generation.
     private int mCheckBoxCount;
 }

 // Create DataTable and fill it with data.
 // In real life this DataTable should be filled from a database.
 private static DataTable getStudentCourseDataTable() throws Exception {
     DataTable dataTable = new DataTable("StudentCourse");
     dataTable.getColumns().add("CourseName");
     for (int i = 0; i < 10; i++) {
         DataRow datarow = dataTable.newRow();
         dataTable.getRows().add(datarow);
         datarow.set(0, "Course " + i);
     }
     return dataTable;
 }
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| fieldName | java.lang.String | اسم حقل دمج البريد غير حساس لحالة الأحرف. |

**Returns:**
منطقي -  true  إذا تم العثور على حقل الدمج وتم نقل المؤشر؛  false  خلاف ذلك.
### moveToMergeField(String fieldName, boolean isAfter, boolean isDeleteField) {#moveToMergeField-java.lang.String-boolean-boolean}
```
public boolean moveToMergeField(String fieldName, boolean isAfter, boolean isDeleteField)
```


ينقل حقل الدمج إلى حقل الدمج المحدد.

 **Examples:** 

يظهر كيفية إدراج الحقول وتحريك مؤشر منشئ المستند إليها.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.insertField("MERGEFIELD MyMergeField1 \\* MERGEFORMAT");
 builder.insertField("MERGEFIELD MyMergeField2 \\* MERGEFORMAT");

 // Move the cursor to the first MERGEFIELD.
 builder.moveToMergeField("MyMergeField1", true, false);

 // Note that the cursor is placed immediately after the first MERGEFIELD, and before the second.
 Assert.assertEquals(doc.getRange().getFields().get(1).getStart(), builder.getCurrentNode());
 Assert.assertEquals(doc.getRange().getFields().get(0).getEnd(), builder.getCurrentNode().getPreviousSibling());

 // If we wish to edit the field's field code or contents using the builder,
 // its cursor would need to be inside a field.
 // To place it inside a field, we would need to call the document builder's MoveTo method
 // and pass the field's start or separator node as an argument.
 builder.write(" Text between our merge fields. ");

 doc.save(getArtifactsDir() + "DocumentBuilder.MergeFields.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| fieldName | java.lang.String | اسم حقل دمج البريد غير حساس لحالة الأحرف. |
| isAfter | boolean | عند  true , ينقل المؤشر ليكون بعد نهاية الحقل. عند  false , ينقل المؤشر ليكون قبل بداية الحقل. |
| isDeleteField | boolean | عند  true , يحذف حقل الدمج. |

**Returns:**
منطقي -  true  إذا تم العثور على حقل الدمج وتم نقل المؤشر؛  false  خلاف ذلك.
### moveToParagraph(int paragraphIndex, int characterIndex) {#moveToParagraph-int-int}
```
public void moveToParagraph(int paragraphIndex, int characterIndex)
```


ينقل المؤشر إلى فقرة في القسم الحالي.

 **Remarks:** 

يتم التنقل داخل القصة الحالية للقسم الحالي. أي إذا نقلت المؤشر إلى الرأس الأساسي للقسم الأول، فإن  paragraphIndex  يحدد فهرس الفقرة داخل ذلك الرأس لهذا القسم.

عند أن يكون  paragraphIndex  أكبر من أو يساوي 0، فإنه يحدد فهرسًا من بداية القسم حيث 0 هو الفقرة الأولى. وعند أن يكون  paragraphIndex  أقل من 0، فإنه يحدد فهرسًا من نهاية القسم حيث -1 هو الفقرة الأخيرة.

 **Examples:** 

يوضح كيفية نقل موضع مؤشر المُنشئ إلى فقرة محددة.

```

 Document doc = new Document(getMyDir() + "Paragraphs.docx");
 ParagraphCollection paragraphs = doc.getFirstSection().getBody().getParagraphs();

 Assert.assertEquals(22, paragraphs.getCount());

 // Create document builder to edit the document. The builder's cursor,
 // which is the point where it will insert new nodes when we call its document construction methods,
 // is currently at the beginning of the document.
 DocumentBuilder builder = new DocumentBuilder(doc);

 Assert.assertEquals(0, paragraphs.indexOf(builder.getCurrentParagraph()));

 // Move that cursor to a different paragraph will place that cursor in front of that paragraph.
 builder.moveToParagraph(2, 0);
 // Any new content that we add will be inserted at that point.
 builder.writeln("This is a new third paragraph. ");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| paragraphIndex | int | فهرس الفقرة التي سيتم الانتقال إليها. |
| characterIndex | int | فهرس الحرف داخل الفقرة. القيمة السالبة تسمح لك بتحديد موقع من نهاية الفقرة. استخدم -1 للتحرك إلى نهاية الفقرة. |

### moveToSection(int sectionIndex) {#moveToSection-int}
```
public void moveToSection(int sectionIndex)
```


ينقل المؤشر إلى بداية الجسم في قسم محدد.

 **Remarks:** 

عند أن يكون  sectionIndex  أكبر من أو يساوي 0، فإنه يحدد فهرسًا من بداية المستند حيث 0 هو القسم الأول. وعند أن يكون  sectionIndex  أقل من 0، فإنه يحدد فهرسًا من نهاية المستند حيث -1 هو آخر قسم.

يتم نقل المؤشر إلى الفقرة الأولى في [Body](../../com.aspose.words/body/) للقسم المحدد.

 **Examples:** 

يوضح كيفية إنشاء رؤوس وتذييلات في المستند باستخدام DocumentBuilder.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Specify that we want different headers and footers for first, even and odd pages.
 builder.getPageSetup().setDifferentFirstPageHeaderFooter(true);
 builder.getPageSetup().setOddAndEvenPagesHeaderFooter(true);

 // Create the headers, then add three pages to the document to display each header type.
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_FIRST);
 builder.write("Header for the first page");
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_EVEN);
 builder.write("Header for even pages");
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 builder.write("Header for all other pages");

 builder.moveToSection(0);
 builder.writeln("Page1");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Page2");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Page3");

 doc.save(getArtifactsDir() + "DocumentBuilder.HeadersAndFooters.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| sectionIndex | int | فهرس القسم الذي سيتم الانتقال إليه. |

### moveToStructuredDocumentTag(StructuredDocumentTag structuredDocumentTag, int characterIndex) {#moveToStructuredDocumentTag-com.aspose.words.StructuredDocumentTag-int}
```
public void moveToStructuredDocumentTag(StructuredDocumentTag structuredDocumentTag, int characterIndex)
```


ينقل المؤشر إلى علامة المستند المنسقة.

 **Examples:** 

يعرض كيفية نقل مؤشر DocumentBuilder داخل علامة مستند منسقة.

```

 Document doc = new Document(getMyDir() + "Structured document tags.docx");
 DocumentBuilder builder = new DocumentBuilder(doc);

 // There is a several ways to move the cursor:
 // 1 -  Move to the first character of structured document tag by index.
 builder.moveToStructuredDocumentTag(1, 1);

 // 2 -  Move to the first character of structured document tag by object.
 StructuredDocumentTag tag = (StructuredDocumentTag)doc.getChild(NodeType.STRUCTURED_DOCUMENT_TAG, 2, true);
 builder.moveToStructuredDocumentTag(tag, 1);
 builder.write(" New text.");

 Assert.assertEquals("R New text.ichText", tag.getText().trim());

 // 3 -  Move to the end of the second structured document tag.
 builder.moveToStructuredDocumentTag(1, -1);
 Assert.assertTrue(builder.isAtEndOfStructuredDocumentTag());

 // Get currently selected structured document tag.
 builder.getCurrentStructuredDocumentTag().setColor(Color.GREEN);

 doc.save(getArtifactsDir() + "Document.MoveToStructuredDocumentTag.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| structuredDocumentTag | [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag/) | علامة المستند المهيكلة التي سيتم الانتقال إليها. |
| characterIndex | int | فهرس الحرف داخل علامة المستند المهيكلة. القيمة السالبة تسمح لك بتحديد موقع من نهاية علامة المستند المهيكلة. استخدم -1 للتحرك إلى نهاية علامة المستند المهيكلة. إذا كانت علامة المستند المهيكلة على مستوى الكتلة، وتريد نقل المؤشر إلى نهاية الفقرة الأخيرة لها، حدد -2. |

### moveToStructuredDocumentTag(int structuredDocumentTagIndex, int characterIndex) {#moveToStructuredDocumentTag-int-int}
```
public void moveToStructuredDocumentTag(int structuredDocumentTagIndex, int characterIndex)
```


ينقل المؤشر إلى علامة مستند منسقة في القسم الحالي.

 **Remarks:** 

يتم التنقل داخل القصة الحالية للقسم الحالي. أي إذا نقلت المؤشر إلى الرأس الأساسي للقسم الأول، فإن  structuredDocumentTagIndex  يحدد فهرس علامة المستند المهيكلة داخل ذلك الرأس لهذا القسم.

عند أن يكون  structuredDocumentTagIndex  أكبر من أو يساوي 0، فإنه يحدد فهرسًا من بداية القسم حيث 0 هي أول علامة مستند مهيكلة. وعند أن يكون  structuredDocumentTagIndex  أقل من 0، فإنه يحدد فهرسًا من نهاية القسم حيث -1 هي آخر علامة مستند مهيكلة.

 **Examples:** 

يعرض كيفية نقل مؤشر DocumentBuilder داخل علامة مستند منسقة.

```

 Document doc = new Document(getMyDir() + "Structured document tags.docx");
 DocumentBuilder builder = new DocumentBuilder(doc);

 // There is a several ways to move the cursor:
 // 1 -  Move to the first character of structured document tag by index.
 builder.moveToStructuredDocumentTag(1, 1);

 // 2 -  Move to the first character of structured document tag by object.
 StructuredDocumentTag tag = (StructuredDocumentTag)doc.getChild(NodeType.STRUCTURED_DOCUMENT_TAG, 2, true);
 builder.moveToStructuredDocumentTag(tag, 1);
 builder.write(" New text.");

 Assert.assertEquals("R New text.ichText", tag.getText().trim());

 // 3 -  Move to the end of the second structured document tag.
 builder.moveToStructuredDocumentTag(1, -1);
 Assert.assertTrue(builder.isAtEndOfStructuredDocumentTag());

 // Get currently selected structured document tag.
 builder.getCurrentStructuredDocumentTag().setColor(Color.GREEN);

 doc.save(getArtifactsDir() + "Document.MoveToStructuredDocumentTag.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| structuredDocumentTagIndex | int | فهرس العلامة المهيكلة للمستند للانتقال إليها. |
| characterIndex | int | فهرس الحرف داخل علامة المستند المهيكلة. القيمة السالبة تسمح لك بتحديد موقع من نهاية علامة المستند المهيكلة. استخدم -1 للتحرك إلى نهاية علامة المستند المهيكلة. إذا كانت علامة المستند المهيكلة على مستوى الكتلة، وتريد نقل المؤشر إلى نهاية الفقرة الأخيرة لها، حدد -2. |

### popFont() {#popFont}
```
public void popFont()
```


يسترجع تنسيق الأحرف الذي تم حفظه مسبقًا على المكدس.

 **Examples:** 

يوضح كيفية استخدام مكدس تنسيق مُنشئ المستند.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Set up font formatting, then write the text that goes before the hyperlink.
 builder.getFont().setName("Arial");
 builder.getFont().setSize(24.0);
 builder.write("To visit Google, hold Ctrl and click ");

 // Preserve our current formatting configuration on the stack.
 builder.pushFont();

 // Alter the builder's current formatting by applying a new style.
 builder.getFont().setStyleIdentifier(StyleIdentifier.HYPERLINK);
 builder.insertHyperlink("here", "http://www.google.com", false);

 Assert.assertEquals(Color.BLUE.getRGB(), builder.getFont().getColor().getRGB());
 Assert.assertEquals(Underline.SINGLE, builder.getFont().getUnderline());

 // Restore the font formatting that we saved earlier and remove the element from the stack.
 builder.popFont();

 Assert.assertEquals(0, builder.getFont().getColor().getRGB());
 Assert.assertEquals(Underline.NONE, builder.getFont().getUnderline());

 builder.write(". We hope you enjoyed the example.");

 doc.save(getArtifactsDir() + "DocumentBuilder.PushPopFont.docx");
 
```

### pushFont() {#pushFont}
```
public void pushFont()
```


يحفظ تنسيق الأحرف الحالي على المكدس.

 **Examples:** 

يوضح كيفية استخدام مكدس تنسيق مُنشئ المستند.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Set up font formatting, then write the text that goes before the hyperlink.
 builder.getFont().setName("Arial");
 builder.getFont().setSize(24.0);
 builder.write("To visit Google, hold Ctrl and click ");

 // Preserve our current formatting configuration on the stack.
 builder.pushFont();

 // Alter the builder's current formatting by applying a new style.
 builder.getFont().setStyleIdentifier(StyleIdentifier.HYPERLINK);
 builder.insertHyperlink("here", "http://www.google.com", false);

 Assert.assertEquals(Color.BLUE.getRGB(), builder.getFont().getColor().getRGB());
 Assert.assertEquals(Underline.SINGLE, builder.getFont().getUnderline());

 // Restore the font formatting that we saved earlier and remove the element from the stack.
 builder.popFont();

 Assert.assertEquals(0, builder.getFont().getColor().getRGB());
 Assert.assertEquals(Underline.NONE, builder.getFont().getUnderline());

 builder.write(". We hope you enjoyed the example.");

 doc.save(getArtifactsDir() + "DocumentBuilder.PushPopFont.docx");
 
```

### removeParaAttr(int key) {#removeParaAttr-int}
```
public void removeParaAttr(int key)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| key | int |  |

### removeRunAttr(int key) {#removeRunAttr-int}
```
public void removeRunAttr(int key)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| key | int |  |

### resetToDefaultAttrs() {#resetToDefaultAttrs}
```
public void resetToDefaultAttrs()
```




### setBold(boolean value) {#setBold-boolean}
```
public void setBold(boolean value)
```


صحيح إذا كان الخط مُنسقًا كغامق.

 **Examples:** 

يعرض كيفية ملء حقول MERGEFIELD بالبيانات باستخدام منشئ المستند بدلاً من دمج البريد.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert some MERGEFIELDS, which accept data from columns of the same name in a data source during a mail merge,
 // and then fill them manually.
 builder.insertField(" MERGEFIELD Chairman ");
 builder.insertField(" MERGEFIELD ChiefFinancialOfficer ");
 builder.insertField(" MERGEFIELD ChiefTechnologyOfficer ");

 builder.moveToMergeField("Chairman");
 builder.setBold(true);
 builder.writeln("John Doe");

 builder.moveToMergeField("ChiefFinancialOfficer");
 builder.setItalic(true);
 builder.writeln("Jane Doe");

 builder.moveToMergeField("ChiefTechnologyOfficer");
 builder.setItalic(true);
 builder.writeln("John Bloggs");

 doc.save(getArtifactsDir() + "DocumentBuilder.FillMergeFields.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | القيمة المنطقية المقابلة. |

### setCellAttr(int key, Object value) {#setCellAttr-int-java.lang.Object}
```
public void setCellAttr(int key, Object value)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| key | int |  |
| قيمة | java.lang.Object |  |

### setDocument(Document value) {#setDocument-com.aspose.words.Document}
```
public void setDocument(Document value)
```


يضبط الكائن [getDocument()](../../com.aspose.words/documentbuilder/\#getDocument) / [setDocument(com.aspose.words.Document)](../../com.aspose.words/documentbuilder/\#setDocument-com.aspose.words.Document) الذي يتم إرفاق هذا الكائن به.

 **Examples:** 

يوضح كيفية تطبيق وإرجاع إعدادات إعداد الصفحة للأقسام في المستند.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Modify the page setup properties for the builder's current section and add text.
 builder.getPageSetup().setOrientation(Orientation.LANDSCAPE);
 builder.getPageSetup().setVerticalAlignment(PageVerticalAlignment.CENTER);
 builder.writeln("This is the first section, which landscape oriented with vertically centered text.");

 // If we start a new section using a document builder,
 // it will inherit the builder's current page setup properties.
 builder.insertBreak(BreakType.SECTION_BREAK_NEW_PAGE);

 Assert.assertEquals(Orientation.LANDSCAPE, doc.getSections().get(1).getPageSetup().getOrientation());
 Assert.assertEquals(PageVerticalAlignment.CENTER, doc.getSections().get(1).getPageSetup().getVerticalAlignment());

 // We can revert its page setup properties to their default values using the "ClearFormatting" method.
 builder.getPageSetup().clearFormatting();

 Assert.assertEquals(Orientation.PORTRAIT, doc.getSections().get(1).getPageSetup().getOrientation());
 Assert.assertEquals(PageVerticalAlignment.TOP, doc.getSections().get(1).getPageSetup().getVerticalAlignment());

 builder.writeln("This is the second section, which is in default Letter paper size, portrait orientation and top alignment.");

 doc.save(getArtifactsDir() + "PageSetup.ClearFormatting.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| value | [Document](../../com.aspose.words/document/) | الكائن [getDocument()](../../com.aspose.words/documentbuilder/\#getDocument) / [setDocument(com.aspose.words.Document)](../../com.aspose.words/documentbuilder/\#setDocument-com.aspose.words.Document) الذي يتم إرفاق هذا الكائن به. |

### setItalic(boolean value) {#setItalic-boolean}
```
public void setItalic(boolean value)
```


صحيح إذا كان الخط مُنسقًا كخط مائل.

 **Examples:** 

يعرض كيفية ملء حقول MERGEFIELD بالبيانات باستخدام منشئ المستند بدلاً من دمج البريد.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert some MERGEFIELDS, which accept data from columns of the same name in a data source during a mail merge,
 // and then fill them manually.
 builder.insertField(" MERGEFIELD Chairman ");
 builder.insertField(" MERGEFIELD ChiefFinancialOfficer ");
 builder.insertField(" MERGEFIELD ChiefTechnologyOfficer ");

 builder.moveToMergeField("Chairman");
 builder.setBold(true);
 builder.writeln("John Doe");

 builder.moveToMergeField("ChiefFinancialOfficer");
 builder.setItalic(true);
 builder.writeln("Jane Doe");

 builder.moveToMergeField("ChiefTechnologyOfficer");
 builder.setItalic(true);
 builder.writeln("John Bloggs");

 doc.save(getArtifactsDir() + "DocumentBuilder.FillMergeFields.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | القيمة المنطقية المقابلة. |

### setParaAttr(int key, Object value) {#setParaAttr-int-java.lang.Object}
```
public void setParaAttr(int key, Object value)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| key | int |  |
| قيمة | java.lang.Object |  |

### setRowAttr(int key, Object value) {#setRowAttr-int-java.lang.Object}
```
public void setRowAttr(int key, Object value)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| key | int |  |
| قيمة | java.lang.Object |  |

### setRunAttr(int fontAttr, Object value) {#setRunAttr-int-java.lang.Object}
```
public void setRunAttr(int fontAttr, Object value)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| fontAttr | int |  |
| قيمة | java.lang.Object |  |

### setUnderline(int value) {#setUnderline-int}
```
public void setUnderline(int value)
```


الحصول/تعيين نوع التسطير للخط الحالي.

 **Examples:** 

يعرض كيفية تنسيق النص الذي يُدرجه منشئ المستند.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.setUnderline(Underline.DASH);
 builder.getFont().setColor(Color.BLUE);
 builder.getFont().setSize(32.0);

 // The builder applies formatting to its current paragraph and any new text added by it afterward.
 builder.writeln("Large, blue, and underlined text.");

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertUnderline.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| value | int | القيمة الصحيحة (int) المقابلة. يجب أن تكون القيمة واحدة من ثوابت [Underline](../../com.aspose.words/underline/). |

### startBookmark(String bookmarkName) {#startBookmark-java.lang.String}
```
public BookmarkStart startBookmark(String bookmarkName)
```


يحدد الموضع الحالي في المستند كبداية إشارة مرجعية.

 **Remarks:** 

يمكن للعلامات المرجعية في المستند أن تتداخل وتغطي أي نطاق. لإنشاء علامة مرجعية صالحة تحتاج إلى استدعاء كل من [startBookmark(java.lang.String)](../../com.aspose.words/documentbuilder/\#startBookmark-java.lang.String) و [endBookmark(java.lang.String)](../../com.aspose.words/documentbuilder/\#endBookmark-java.lang.String) باستخدام نفس معامل  bookmarkName.

سيتم تجاهل العلامات المرجعية المشوهة أو العلامات المرجعية ذات الأسماء المكررة عند حفظ المستند.

 **Examples:** 

يوضح كيفية إنشاء علامة مرجعية.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // A valid bookmark needs to have document body text enclosed by
 // BookmarkStart and BookmarkEnd nodes created with a matching bookmark name.
 builder.startBookmark("MyBookmark");
 builder.writeln("Hello world!");
 builder.endBookmark("MyBookmark");

 Assert.assertEquals(1, doc.getRange().getBookmarks().getCount());
 Assert.assertEquals("MyBookmark", doc.getRange().getBookmarks().get(0).getName());
 Assert.assertEquals("Hello world!", doc.getRange().getBookmarks().get(0).getText().trim());
 
```

يوضح كيفية إدراج ارتباط تشعبي يشير إلى علامة مرجعية محلية.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.startBookmark("Bookmark1");
 builder.write("Bookmarked text. ");
 builder.endBookmark("Bookmark1");
 builder.writeln("Text outside of the bookmark.");

 // Insert a HYPERLINK field that links to the bookmark. We can pass field switches
 // to the "InsertHyperlink" method as part of the argument containing the referenced bookmark's name.
 builder.getFont().setColor(Color.BLUE);
 builder.getFont().setUnderline(Underline.SINGLE);
 FieldHyperlink hyperlink = (FieldHyperlink)builder.insertHyperlink("Link to Bookmark1", "Bookmark1", true);
 hyperlink.setScreenTip("Hyperlink Tip");

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertHyperlinkToLocalBookmark.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| bookmarkName | java.lang.String | اسم العلامة المرجعية. |

**Returns:**
[BookmarkStart](../../com.aspose.words/bookmarkstart/) - The bookmark start node that was just created.
### startColumnBookmark(String bookmarkName) {#startColumnBookmark-java.lang.String}
```
public BookmarkStart startColumnBookmark(String bookmarkName)
```


يحدد الموضع الحالي في المستند كبداية إشارة مرجعية للعمود. يجب أن يكون الموضع داخل خلية جدول.

 **Remarks:** 

تغطي علامة مرجعية عمودية عمودًا أو أكثر في نطاق من الصفوف. لإنشاء علامة مرجعية صالحة تحتاج إلى استدعاء كل من [startColumnBookmark(java.lang.String)](../../com.aspose.words/documentbuilder/\#startColumnBookmark-java.lang.String) و [endColumnBookmark(java.lang.String)](../../com.aspose.words/documentbuilder/\#endColumnBookmark-java.lang.String) باستخدام نفس معامل  bookmarkName.

سيتم تجاهل العلامات المرجعية المشوهة أو العلامات المرجعية ذات الأسماء المكررة عند حفظ المستند.

قد يختلف الموضع الفعلي للعقدة [BookmarkStart](../../com.aspose.words/bookmarkstart/) التي تم إدراجها عن موضع منشئ المستند الحالي.

 **Examples:** 

يعرض كيفية إنشاء إشارة مرجعية للعمود.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.startTable();

 builder.insertCell();
 // Cells 1,2,4,5 will be bookmarked.
 builder.startColumnBookmark("MyBookmark_1");
 // Badly formed bookmarks or bookmarks with duplicate names will be ignored when the document is saved.
 builder.startColumnBookmark("MyBookmark_1");
 builder.startColumnBookmark("BadStartBookmark");
 builder.write("Cell 1");

 builder.insertCell();
 builder.write("Cell 2");

 builder.insertCell();
 builder.write("Cell 3");

 builder.endRow();

 builder.insertCell();
 builder.write("Cell 4");

 builder.insertCell();
 builder.write("Cell 5");
 builder.endColumnBookmark("MyBookmark_1");
 builder.endColumnBookmark("MyBookmark_1");

 builder.insertCell();
 builder.write("Cell 6");

 builder.endRow();
 builder.endTable();

 doc.save(getArtifactsDir() + "Bookmarks.CreateColumnBookmark.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| bookmarkName | java.lang.String | اسم العلامة المرجعية. |

**Returns:**
[BookmarkStart](../../com.aspose.words/bookmarkstart/) - The bookmark start node that was just created.
### startEditableRange() {#startEditableRange}
```
public EditableRangeStart startEditableRange()
```


يحدد الموضع الحالي في المستند كبداية نطاق قابل للتحرير.

 **Remarks:** 

يمكن أن يتداخل النطاق القابل للتحرير في المستند ويمتد عبر أي نطاق. لإنشاء نطاق قابل للتحرير صالح تحتاج إلى استدعاء كل من [startEditableRange()](../../com.aspose.words/documentbuilder/\#startEditableRange) و [endEditableRange()](../../com.aspose.words/documentbuilder/\#endEditableRange) أو طريقة [endEditableRange(com.aspose.words.EditableRangeStart)](../../com.aspose.words/documentbuilder/\#endEditableRange-com.aspose.words.EditableRangeStart).

سيتم تجاهل النطاق القابل للتحرير غير المشكل بشكل صحيح عند حفظ المستند.

 **Examples:** 

يوضح كيفية العمل مع نطاق قابل للتحرير.

```

 Document doc = new Document();
 doc.protect(ProtectionType.READ_ONLY, "MyPassword");

 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world! Since we have set the document's protection level to read-only," +
         " we cannot edit this paragraph without the password.");

 // Editable ranges allow us to leave parts of protected documents open for editing.
 EditableRangeStart editableRangeStart = builder.startEditableRange();
 builder.writeln("This paragraph is inside an editable range, and can be edited.");
 EditableRangeEnd editableRangeEnd = builder.endEditableRange();

 // A well-formed editable range has a start node, and end node.
 // These nodes have matching IDs and encompass editable nodes.
 EditableRange editableRange = editableRangeStart.getEditableRange();

 Assert.assertEquals(editableRangeStart.getId(), editableRange.getId());
 Assert.assertEquals(editableRangeEnd.getId(), editableRange.getId());

 // Different parts of the editable range link to each other.
 Assert.assertEquals(editableRangeStart.getId(), editableRange.getEditableRangeStart().getId());
 Assert.assertEquals(editableRangeStart.getId(), editableRangeEnd.getEditableRangeStart().getId());
 Assert.assertEquals(editableRange.getId(), editableRangeStart.getEditableRange().getId());
 Assert.assertEquals(editableRangeEnd.getId(), editableRange.getEditableRangeEnd().getId());

 // We can access the node types of each part like this. The editable range itself is not a node,
 // but an entity which consists of a start, an end, and their enclosed contents.
 Assert.assertEquals(NodeType.EDITABLE_RANGE_START, editableRangeStart.getNodeType());
 Assert.assertEquals(NodeType.EDITABLE_RANGE_END, editableRangeEnd.getNodeType());

 builder.writeln("This paragraph is outside the editable range, and cannot be edited.");

 doc.save(getArtifactsDir() + "EditableRange.CreateAndRemove.docx");

 // Remove an editable range. All the nodes that were inside the range will remain intact.
 editableRange.remove();
 
```

يوضح كيفية إنشاء نطاقات قابلة للتحرير متداخلة.

```

 Document doc = new Document();
 doc.protect(ProtectionType.READ_ONLY, "MyPassword");

 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world! Since we have set the document's protection level to read-only, " +
         "we cannot edit this paragraph without the password.");

 // Create two nested editable ranges.
 EditableRangeStart outerEditableRangeStart = builder.startEditableRange();
 builder.writeln("This paragraph inside the outer editable range and can be edited.");

 EditableRangeStart innerEditableRangeStart = builder.startEditableRange();
 builder.writeln("This paragraph inside both the outer and inner editable ranges and can be edited.");

 // Currently, the document builder's node insertion cursor is in more than one ongoing editable range.
 // When we want to end an editable range in this situation,
 // we need to specify which of the ranges we wish to end by passing its EditableRangeStart node.
 builder.endEditableRange(innerEditableRangeStart);

 builder.writeln("This paragraph inside the outer editable range and can be edited.");

 builder.endEditableRange(outerEditableRangeStart);

 builder.writeln("This paragraph is outside any editable ranges, and cannot be edited.");

 // If a region of text has two overlapping editable ranges with specified groups,
 // the combined group of users excluded by both groups are prevented from editing it.
 outerEditableRangeStart.getEditableRange().setEditorGroup(EditorType.EVERYONE);
 innerEditableRangeStart.getEditableRange().setEditorGroup(EditorType.CONTRIBUTORS);

 doc.save(getArtifactsDir() + "EditableRange.Nested.docx");
 
```

**Returns:**
[EditableRangeStart](../../com.aspose.words/editablerangestart/) - The editable range start node that was just created.
### startTable() {#startTable}
```
public Table startTable()
```


يبدأ جدولًا في المستند.

 **Remarks:** 

الطريقة التالية التي يجب استدعاؤها هي [insertCell()](../../com.aspose.words/documentbuilder/\#insertCell).

تبدأ هذه الطريقة جدولًا متداخلًا عند استدعائها داخل خلية.

 **Examples:** 

يوضح كيفية إنشاء جدول بحدود مخصصة.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.startTable();

 // Setting table formatting options for a document builder
 // will apply them to every row and cell that we add with it.
 builder.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);

 builder.getCellFormat().clearFormatting();
 builder.getCellFormat().setWidth(150.0);
 builder.getCellFormat().setVerticalAlignment(CellVerticalAlignment.CENTER);
 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.GREEN);
 builder.getCellFormat().setWrapText(false);
 builder.getCellFormat().setFitText(true);

 builder.getRowFormat().clearFormatting();
 builder.getRowFormat().setHeightRule(HeightRule.EXACTLY);
 builder.getRowFormat().setHeight(50.0);
 builder.getRowFormat().getBorders().setLineStyle(LineStyle.ENGRAVE_3_D);
 builder.getRowFormat().getBorders().setColor(Color.ORANGE);

 builder.insertCell();
 builder.write("Row 1, Col 1");

 builder.insertCell();
 builder.write("Row 1, Col 2");
 builder.endRow();

 // Changing the formatting will apply it to the current cell,
 // and any new cells that we create with the builder afterward.
 // This will not affect the cells that we have added previously.
 builder.getCellFormat().getShading().clearFormatting();

 builder.insertCell();
 builder.write("Row 2, Col 1");

 builder.insertCell();
 builder.write("Row 2, Col 2");

 builder.endRow();

 // Increase row height to fit the vertical text.
 builder.insertCell();
 builder.getRowFormat().setHeight(150.0);
 builder.getCellFormat().setOrientation(TextOrientation.UPWARD);
 builder.write("Row 3, Col 1");

 builder.insertCell();
 builder.getCellFormat().setOrientation(TextOrientation.DOWNWARD);
 builder.write("Row 3, Col 2");

 builder.endRow();
 builder.endTable();

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertTable.docx");
 
```

يعرض كيفية إنشاء جدول 2x2 منسق.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.getCellFormat().setVerticalAlignment(CellVerticalAlignment.CENTER);
 builder.write("Row 1, cell 1.");
 builder.insertCell();
 builder.write("Row 1, cell 2.");
 builder.endRow();

 // While building the table, the document builder will apply its current RowFormat/CellFormat property values
 // to the current row/cell that its cursor is in and any new rows/cells as it creates them.
 Assert.assertEquals(CellVerticalAlignment.CENTER, table.getRows().get(0).getCells().get(0).getCellFormat().getVerticalAlignment());
 Assert.assertEquals(CellVerticalAlignment.CENTER, table.getRows().get(0).getCells().get(1).getCellFormat().getVerticalAlignment());

 builder.insertCell();
 builder.getRowFormat().setHeight(100.0);
 builder.getRowFormat().setHeightRule(HeightRule.EXACTLY);
 builder.getCellFormat().setOrientation(TextOrientation.UPWARD);
 builder.write("Row 2, cell 1.");
 builder.insertCell();
 builder.getCellFormat().setOrientation(TextOrientation.DOWNWARD);
 builder.write("Row 2, cell 2.");
 builder.endRow();
 builder.endTable();

 // Previously added rows and cells are not retroactively affected by changes to the builder's formatting.
 Assert.assertEquals(0.0, table.getRows().get(0).getRowFormat().getHeight());
 Assert.assertEquals(HeightRule.AUTO, table.getRows().get(0).getRowFormat().getHeightRule());
 Assert.assertEquals(100.0, table.getRows().get(1).getRowFormat().getHeight());
 Assert.assertEquals(HeightRule.EXACTLY, table.getRows().get(1).getRowFormat().getHeightRule());
 Assert.assertEquals(TextOrientation.UPWARD, table.getRows().get(1).getCells().get(0).getCellFormat().getOrientation());
 Assert.assertEquals(TextOrientation.DOWNWARD, table.getRows().get(1).getCells().get(1).getCellFormat().getOrientation());

 doc.save(getArtifactsDir() + "DocumentBuilder.BuildTable.docx");
 
```

يعرض كيفية تنسيق الخلايا باستخدام منشئ المستند.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Row 1, cell 1.");

 // Insert a second cell, and then configure cell text padding options.
 // The builder will apply these settings at its current cell, and any new cells creates afterwards.
 builder.insertCell();

 CellFormat cellFormat = builder.getCellFormat();
 cellFormat.setWidth(250.0);
 cellFormat.setLeftPadding(30.0);
 cellFormat.setRightPadding(30.0);
 cellFormat.setTopPadding(30.0);
 cellFormat.setBottomPadding(30.0);

 builder.write("Row 1, cell 2.");
 builder.endRow();
 builder.endTable();

 // The first cell was unaffected by the padding reconfiguration, and still holds the default values.
 Assert.assertEquals(0.0d, table.getFirstRow().getCells().get(0).getCellFormat().getWidth());
 Assert.assertEquals(5.4d, table.getFirstRow().getCells().get(0).getCellFormat().getLeftPadding());
 Assert.assertEquals(5.4d, table.getFirstRow().getCells().get(0).getCellFormat().getRightPadding());
 Assert.assertEquals(0.0d, table.getFirstRow().getCells().get(0).getCellFormat().getTopPadding());
 Assert.assertEquals(0.0d, table.getFirstRow().getCells().get(0).getCellFormat().getBottomPadding());

 Assert.assertEquals(250.0d, table.getFirstRow().getCells().get(1).getCellFormat().getWidth());
 Assert.assertEquals(30.0d, table.getFirstRow().getCells().get(1).getCellFormat().getLeftPadding());
 Assert.assertEquals(30.0d, table.getFirstRow().getCells().get(1).getCellFormat().getRightPadding());
 Assert.assertEquals(30.0d, table.getFirstRow().getCells().get(1).getCellFormat().getTopPadding());
 Assert.assertEquals(30.0d, table.getFirstRow().getCells().get(1).getCellFormat().getBottomPadding());

 // The first cell will still grow in the output document to match the size of its neighboring cell.
 doc.save(getArtifactsDir() + "DocumentBuilder.SetCellFormatting.docx");
 
```

**Returns:**
[Table](../../com.aspose.words/table/) - The table node that was just created.
### write(String text) {#write-java.lang.String}
```
public void write(String text)
```


يدرج سلسلة نصية في المستند عند موضع الإدراج الحالي.

 **Remarks:** 

يتم استخدام تنسيق الخط الحالي المحدد بواسطة الخاصية [getFont()](../../com.aspose.words/documentbuilder/\#getFont).

 **Examples:** 

يوضح كيفية إدراج سلسلة محاطة بحد داخل مستند.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().getBorder().setColor(Color.GREEN);
 builder.getFont().getBorder().setLineWidth(2.5);
 builder.getFont().getBorder().setLineStyle(LineStyle.DASH_DOT_STROKER);

 builder.write("Text surrounded by green border.");

 doc.save(getArtifactsDir() + "Border.FontBorder.docx");
 
```

يوضح كيفية إنشاء جدول بحدود مخصصة.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.startTable();

 // Setting table formatting options for a document builder
 // will apply them to every row and cell that we add with it.
 builder.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);

 builder.getCellFormat().clearFormatting();
 builder.getCellFormat().setWidth(150.0);
 builder.getCellFormat().setVerticalAlignment(CellVerticalAlignment.CENTER);
 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.GREEN);
 builder.getCellFormat().setWrapText(false);
 builder.getCellFormat().setFitText(true);

 builder.getRowFormat().clearFormatting();
 builder.getRowFormat().setHeightRule(HeightRule.EXACTLY);
 builder.getRowFormat().setHeight(50.0);
 builder.getRowFormat().getBorders().setLineStyle(LineStyle.ENGRAVE_3_D);
 builder.getRowFormat().getBorders().setColor(Color.ORANGE);

 builder.insertCell();
 builder.write("Row 1, Col 1");

 builder.insertCell();
 builder.write("Row 1, Col 2");
 builder.endRow();

 // Changing the formatting will apply it to the current cell,
 // and any new cells that we create with the builder afterward.
 // This will not affect the cells that we have added previously.
 builder.getCellFormat().getShading().clearFormatting();

 builder.insertCell();
 builder.write("Row 2, Col 1");

 builder.insertCell();
 builder.write("Row 2, Col 2");

 builder.endRow();

 // Increase row height to fit the vertical text.
 builder.insertCell();
 builder.getRowFormat().setHeight(150.0);
 builder.getCellFormat().setOrientation(TextOrientation.UPWARD);
 builder.write("Row 3, Col 1");

 builder.insertCell();
 builder.getCellFormat().setOrientation(TextOrientation.DOWNWARD);
 builder.write("Row 3, Col 2");

 builder.endRow();
 builder.endTable();

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertTable.docx");
 
```

يوضح كيفية استخدام DocumentBuilder لإنشاء جدول.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Start the table, then populate the first row with two cells.
 builder.startTable();
 builder.insertCell();
 builder.write("Row 1, Cell 1.");
 builder.insertCell();
 builder.write("Row 1, Cell 2.");

 // Call the builder's "EndRow" method to start a new row.
 builder.endRow();
 builder.insertCell();
 builder.write("Row 2, Cell 1.");
 builder.insertCell();
 builder.write("Row 2, Cell 2.");
 builder.endTable();

 doc.save(getArtifactsDir() + "DocumentBuilder.CreateTable.docx");
 
```

يعرض كيفية إنشاء جدول 2x2 منسق.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.getCellFormat().setVerticalAlignment(CellVerticalAlignment.CENTER);
 builder.write("Row 1, cell 1.");
 builder.insertCell();
 builder.write("Row 1, cell 2.");
 builder.endRow();

 // While building the table, the document builder will apply its current RowFormat/CellFormat property values
 // to the current row/cell that its cursor is in and any new rows/cells as it creates them.
 Assert.assertEquals(CellVerticalAlignment.CENTER, table.getRows().get(0).getCells().get(0).getCellFormat().getVerticalAlignment());
 Assert.assertEquals(CellVerticalAlignment.CENTER, table.getRows().get(0).getCells().get(1).getCellFormat().getVerticalAlignment());

 builder.insertCell();
 builder.getRowFormat().setHeight(100.0);
 builder.getRowFormat().setHeightRule(HeightRule.EXACTLY);
 builder.getCellFormat().setOrientation(TextOrientation.UPWARD);
 builder.write("Row 2, cell 1.");
 builder.insertCell();
 builder.getCellFormat().setOrientation(TextOrientation.DOWNWARD);
 builder.write("Row 2, cell 2.");
 builder.endRow();
 builder.endTable();

 // Previously added rows and cells are not retroactively affected by changes to the builder's formatting.
 Assert.assertEquals(0.0, table.getRows().get(0).getRowFormat().getHeight());
 Assert.assertEquals(HeightRule.AUTO, table.getRows().get(0).getRowFormat().getHeightRule());
 Assert.assertEquals(100.0, table.getRows().get(1).getRowFormat().getHeight());
 Assert.assertEquals(HeightRule.EXACTLY, table.getRows().get(1).getRowFormat().getHeightRule());
 Assert.assertEquals(TextOrientation.UPWARD, table.getRows().get(1).getCells().get(0).getCellFormat().getOrientation());
 Assert.assertEquals(TextOrientation.DOWNWARD, table.getRows().get(1).getCells().get(1).getCellFormat().getOrientation());

 doc.save(getArtifactsDir() + "DocumentBuilder.BuildTable.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| نص | java.lang.String | السلسلة لإدراجها في المستند. |

### writeln() {#writeln}
```
public void writeln()
```


يدرج فاصل فقرة في المستند.

 **Remarks:** 

يستدعي [insertParagraph()](../../com.aspose.words/documentbuilder/\#insertParagraph).

 **Examples:** 

يوضح كيفية إنشاء رؤوس وتذييلات في المستند باستخدام DocumentBuilder.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Specify that we want different headers and footers for first, even and odd pages.
 builder.getPageSetup().setDifferentFirstPageHeaderFooter(true);
 builder.getPageSetup().setOddAndEvenPagesHeaderFooter(true);

 // Create the headers, then add three pages to the document to display each header type.
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_FIRST);
 builder.write("Header for the first page");
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_EVEN);
 builder.write("Header for even pages");
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 builder.write("Header for all other pages");

 builder.moveToSection(0);
 builder.writeln("Page1");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Page2");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Page3");

 doc.save(getArtifactsDir() + "DocumentBuilder.HeadersAndFooters.docx");
 
```

### writeln(String text) {#writeln-java.lang.String}
```
public void writeln(String text)
```


يدرج سلسلة نصية وفاصل فقرة في المستند.

 **Remarks:** 

يتم استخدام تنسيق الخط والفقرة الحالي المحدد بواسطة الخاصيتين [getFont()](../../com.aspose.words/documentbuilder/\#getFont) و [getParagraphFormat()](../../com.aspose.words/documentbuilder/\#getParagraphFormat).

 **Examples:** 

يعرض كيفية إنشاء جدول 2x2 منسق.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.getCellFormat().setVerticalAlignment(CellVerticalAlignment.CENTER);
 builder.write("Row 1, cell 1.");
 builder.insertCell();
 builder.write("Row 1, cell 2.");
 builder.endRow();

 // While building the table, the document builder will apply its current RowFormat/CellFormat property values
 // to the current row/cell that its cursor is in and any new rows/cells as it creates them.
 Assert.assertEquals(CellVerticalAlignment.CENTER, table.getRows().get(0).getCells().get(0).getCellFormat().getVerticalAlignment());
 Assert.assertEquals(CellVerticalAlignment.CENTER, table.getRows().get(0).getCells().get(1).getCellFormat().getVerticalAlignment());

 builder.insertCell();
 builder.getRowFormat().setHeight(100.0);
 builder.getRowFormat().setHeightRule(HeightRule.EXACTLY);
 builder.getCellFormat().setOrientation(TextOrientation.UPWARD);
 builder.write("Row 2, cell 1.");
 builder.insertCell();
 builder.getCellFormat().setOrientation(TextOrientation.DOWNWARD);
 builder.write("Row 2, cell 2.");
 builder.endRow();
 builder.endTable();

 // Previously added rows and cells are not retroactively affected by changes to the builder's formatting.
 Assert.assertEquals(0.0, table.getRows().get(0).getRowFormat().getHeight());
 Assert.assertEquals(HeightRule.AUTO, table.getRows().get(0).getRowFormat().getHeightRule());
 Assert.assertEquals(100.0, table.getRows().get(1).getRowFormat().getHeight());
 Assert.assertEquals(HeightRule.EXACTLY, table.getRows().get(1).getRowFormat().getHeightRule());
 Assert.assertEquals(TextOrientation.UPWARD, table.getRows().get(1).getCells().get(0).getCellFormat().getOrientation());
 Assert.assertEquals(TextOrientation.DOWNWARD, table.getRows().get(1).getCells().get(1).getCellFormat().getOrientation());

 doc.save(getArtifactsDir() + "DocumentBuilder.BuildTable.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| نص | java.lang.String | السلسلة لإدراجها في المستند. |

