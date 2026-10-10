---
title: "ImportFormatOptions"
linktitle: "ImportFormatOptions"
second_title: "Aspose.Words لـ Java"
description: "يسمح بتحديد خيارات استيراد مختلفة لتنسيق المخرجات في Java."
type: docs
weight: 401
url: /ar/java/com.aspose.words/importformatoptions/
---

**Inheritance:**
java.lang.Object
```
public class ImportFormatOptions
```

يسمح بتحديد خيارات استيراد متنوعة لتنسيق المخرجات.

لمزيد من المعلومات، زر مقالة الوثائق [ Specify Load Options ][Specify Load Options].

 **Examples:** 

يظهر كيفية حل الأنماط المكررة أثناء إدراج المستندات.

```

 Document dstDoc = new Document();
 DocumentBuilder builder = new DocumentBuilder(dstDoc);

 Style myStyle = builder.getDocument().getStyles().add(StyleType.PARAGRAPH, "MyStyle");
 myStyle.getFont().setSize(14.0);
 myStyle.getFont().setName("Courier New");
 myStyle.getFont().setColor(Color.BLUE);

 builder.getParagraphFormat().setStyleName(myStyle.getName());
 builder.writeln("Hello world!");

 // Clone the document and edit the clone's "MyStyle" style, so it is a different color than that of the original.
 // If we insert the clone into the original document, the two styles with the same name will cause a clash.
 Document srcDoc = dstDoc.deepClone();
 srcDoc.getStyles().get("MyStyle").getFont().setColor(Color.RED);

 // When we enable SmartStyleBehavior and use the KeepSourceFormatting import format mode,
 // Aspose.Words will resolve style clashes by converting source document styles.
 // with the same names as destination styles into direct paragraph attributes.
 ImportFormatOptions options = new ImportFormatOptions();
 options.setSmartStyleBehavior(true);

 builder.insertDocument(srcDoc, ImportFormatMode.KEEP_SOURCE_FORMATTING, options);

 dstDoc.save(getArtifactsDir() + "DocumentBuilder.SmartStyleBehavior.docx");
 
```


[Specify Load Options]: https://docs.aspose.com/words/java/specify-load-options/
## الطرق

| طريقة | الوصف |
| --- | --- |
| [getAdjustSentenceAndWordSpacing()](#getAdjustSentenceAndWordSpacing) | يحصل على قيمة منطقية تحدد ما إذا كان يجب تعديل تباعد الجمل والكلمات تلقائيًا. |
| [getAppendDocumentWithNewPage()](#getAppendDocumentWithNewPage) | يحصل على قيمة منطقية تشير إلى ما إذا كان يجب تغيير نوع القسم الأول المستورد إلى [SectionStart.NEW\_PAGE](../../com.aspose.words/sectionstart/\#NEW-PAGE) بالقوة عند استدعاء **M:Aspose.Words.Document.AppendDocument(Aspose.Words.Document,Aspose.Words.ImportFormatMode,Aspose.Words.ImportFormatOptions)**. |
| [getForceCopyStyles()](#getForceCopyStyles) | يحصل على قيمة منطقية تشير إلى إما نسخ الأنماط المتضاربة في وضع [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode/\#KEEP-SOURCE-FORMATTING). |
| [getIgnoreHeaderFooter()](#getIgnoreHeaderFooter) | يحصل على قيمة منطقية تحدد أن تنسيق المصدر لمحتوى رؤوس/تذييلات الصفحات يتم تجاهله إذا تم استخدام وضع [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode/\#KEEP-SOURCE-FORMATTING). |
| [getIgnoreTextBoxes()](#getIgnoreTextBoxes) | يحصل على قيمة منطقية تحدد أن تنسيق المصدر لمحتوى صناديق النص يتم تجاهله إذا تم استخدام وضع [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode/\#KEEP-SOURCE-FORMATTING). |
| [getKeepSourceNumbering()](#getKeepSourceNumbering) | يحصل على قيمة منطقية تحدد كيفية استيراد الترقيم عندما يتصادم في المستندات المصدر والوجهة. |
| [getMergePastedLists()](#getMergePastedLists) | يحصل على قيمة منطقية تحدد ما إذا كانت القوائم الملصوقة ستُدمج مع القوائم المحيطة. |
| [getResolveThemeColors()](#getResolveThemeColors) | يحصل على قيمة منطقية تحدد ما إذا كان يجب حل ألوان السمة للأشكال بالقوة. |
| [getSmartStyleBehavior()](#getSmartStyleBehavior) | يحصل على قيمة منطقية تحدد كيفية استيراد الأنماط عندما يكون لها نفس الأسماء في المستندات المصدر والوجهة. |
| [setAdjustSentenceAndWordSpacing(boolean value)](#setAdjustSentenceAndWordSpacing-boolean) | يضبط قيمة منطقية تحدد ما إذا كان يجب تعديل تباعد الجمل والكلمات تلقائيًا. |
| [setAppendDocumentWithNewPage(boolean value)](#setAppendDocumentWithNewPage-boolean) | يضبط قيمة منطقية تشير إلى ما إذا كان يجب تغيير نوع القسم الأول المستورد إلى [SectionStart.NEW\_PAGE](../../com.aspose.words/sectionstart/\#NEW-PAGE) بالقوة عند استدعاء **M:Aspose.Words.Document.AppendDocument(Aspose.Words.Document,Aspose.Words.ImportFormatMode,Aspose.Words.ImportFormatOptions)**. |
| [setForceCopyStyles(boolean value)](#setForceCopyStyles-boolean) | يضبط قيمة منطقية تشير إلى ما إذا كان يجب نسخ الأنماط المتضاربة في وضع [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode/\#KEEP-SOURCE-FORMATTING). |
| [setIgnoreHeaderFooter(boolean value)](#setIgnoreHeaderFooter-boolean) | يضبط قيمة منطقية تحدد أن تنسيق المصدر لمحتوى رؤوس/تذييلات الصفحات يتم تجاهله إذا تم استخدام وضع [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode/\#KEEP-SOURCE-FORMATTING). |
| [setIgnoreTextBoxes(boolean value)](#setIgnoreTextBoxes-boolean) | يضبط قيمة منطقية تحدد أن تنسيق المصدر لمحتوى مربعات النص يتم تجاهله إذا تم استخدام وضع [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode/\#KEEP-SOURCE-FORMATTING). |
| [setKeepSourceNumbering(boolean value)](#setKeepSourceNumbering-boolean) | يضبط قيمة منطقية تحدد كيفية استيراد الترقيم عندما يتصادم في المستندات المصدر والوجهة. |
| [setMergePastedLists(boolean value)](#setMergePastedLists-boolean) | يضبط قيمة منطقية تحدد ما إذا كانت القوائم الملصوقة ستُدمج مع القوائم المحيطة. |
| [setResolveThemeColors(boolean value)](#setResolveThemeColors-boolean) | يضبط قيمة منطقية تحدد ما إذا كان يجب حل ألوان السمة للأشكال بالقوة. |
| [setSmartStyleBehavior(boolean value)](#setSmartStyleBehavior-boolean) | يضبط قيمة منطقية تحدد كيفية استيراد الأنماط عندما يكون لها نفس الأسماء في المستندات المصدر والوجهة. |
### getAdjustSentenceAndWordSpacing() {#getAdjustSentenceAndWordSpacing}
```
public boolean getAdjustSentenceAndWordSpacing()
```


يحصل على قيمة منطقية تحدد ما إذا كان يجب تعديل تباعد الجمل والكلمات تلقائيًا. القيمة الافتراضية هي false.

 **Examples:** 

يعرض كيفية تعديل تباعد الجمل والكلمات تلقائيًا.

```

 Document srcDoc = new Document();
 Document dstDoc = new Document();

 DocumentBuilder builder = new DocumentBuilder(srcDoc);
 builder.write("Dolor sit amet.");

 builder = new DocumentBuilder(dstDoc);
 builder.write("Lorem ipsum.");

 ImportFormatOptions options = new ImportFormatOptions(); { options.setAdjustSentenceAndWordSpacing(true); }
 builder.insertDocument(srcDoc, ImportFormatMode.USE_DESTINATION_STYLES, options);

 Assert.assertEquals("Lorem ipsum. Dolor sit amet.", dstDoc.getFirstSection().getBody().getFirstParagraph().getText().trim());
 
```

**Returns:**
منطقي - قيمة منطقية تحدد ما إذا كان يجب تعديل تباعد الجمل والكلمات تلقائيًا.
### getAppendDocumentWithNewPage() {#getAppendDocumentWithNewPage}
```
public boolean getAppendDocumentWithNewPage()
```


يحصل على قيمة منطقية تشير إلى ما إذا كان يجب تغيير نوع القسم الأول المستورد إلى [SectionStart.NEW\_PAGE](../../com.aspose.words/sectionstart/\#NEW-PAGE) بالقوة عند استدعاء **M:Aspose.Words.Document.AppendDocument(Aspose.Words.Document,Aspose.Words.ImportFormatMode,Aspose.Words.ImportFormatOptions)**.

القيمة الافتراضية هي  true .

 **Remarks:** 

يرجى ملاحظة أن هذا الخيار ذو صلة فقط بطريقة **M:Aspose.Words.Document.AppendDocument(Aspose.Words.Document,Aspose.Words.ImportFormatMode,Aspose.Words.ImportFormatOptions)** ولا يؤثر على طرق الاستيراد الأخرى.

 **Examples:** 

يعرض كيفية الحفاظ على نوع القسم الأصلي.

```

 Document dstDoc = new Document();
 Document srcDoc = new Document();

 srcDoc.getFirstSection().getPageSetup().setSectionStart(SectionStart.CONTINUOUS);

 ImportFormatOptions options = new ImportFormatOptions();
 options.setAppendDocumentWithNewPage(false);
 dstDoc.appendDocument(srcDoc, ImportFormatMode.KEEP_SOURCE_FORMATTING, options);

 Assert.assertEquals(SectionStart.CONTINUOUS, dstDoc.getSections().get(1).getPageSetup().getSectionStart());
 
```

**Returns:**
منطقي - قيمة منطقية تشير إلى ما إذا كان يجب تغيير نوع القسم الأول المستورد إلى [SectionStart.NEW\_PAGE](../../com.aspose.words/sectionstart/\#NEW-PAGE) بالقوة عند استدعاء **M:Aspose.Words.Document.AppendDocument(Aspose.Words.Document,Aspose.Words.ImportFormatMode,Aspose.Words.ImportFormatOptions)**.
### getForceCopyStyles() {#getForceCopyStyles}
```
public boolean getForceCopyStyles()
```


يحصل على قيمة منطقية تشير إلى ما إذا كان يجب نسخ الأنماط المتضاربة في وضع [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode/\#KEEP-SOURCE-FORMATTING). القيمة الافتراضية هي false.

 **Remarks:** 

بشكل افتراضي، إذا كان هناك نمط مطابق موجود بالفعل في مستند الوجهة، يتم توسيع تنسيق النمط المصدر إلى سمات العقدة المباشرة وتُعاد تعيين نمط هذه العقدة إلى القيمة الافتراضية.

عند ضبط هذا الخيار على true، سيتم نسخ النمط المصدر بالقوة إلى مستند الوجهة باسم فريد وتطبيقه على العقدة المستوردة.

ملاحظة، في هذه الحالة لا يُضمن الحفاظ على تنسيق العقدة المستوردة في مستند الوجهة.

 **Examples:** 

يعرض كيفية نسخ أنماط المصدر بأسماء فريدة بالقوة.

```

 // Both documents contain MyStyle1 and MyStyle2, MyStyle3 exists only in a source document.
 Document srcDoc = new Document(getMyDir() + "Styles source.docx");
 Document dstDoc = new Document(getMyDir() + "Styles destination.docx");

 ImportFormatOptions options = new ImportFormatOptions(); { options.setForceCopyStyles(true); }
 dstDoc.appendDocument(srcDoc, ImportFormatMode.KEEP_SOURCE_FORMATTING, options);

 ParagraphCollection paras = dstDoc.getSections().get(1).getBody().getParagraphs();

 Assert.assertEquals(paras.get(0).getParagraphFormat().getStyle().getName(), "MyStyle1_0");
 Assert.assertEquals(paras.get(1).getParagraphFormat().getStyle().getName(), "MyStyle2_0");
 Assert.assertEquals(paras.get(2).getParagraphFormat().getStyle().getName(), "MyStyle3");
 
```

**Returns:**
منطقي - قيمة منطقية تشير إلى ما إذا كان يجب نسخ الأنماط المتضاربة في وضع [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode/\#KEEP-SOURCE-FORMATTING).
### getIgnoreHeaderFooter() {#getIgnoreHeaderFooter}
```
public boolean getIgnoreHeaderFooter()
```


يحصل على قيمة منطقية تحدد أن تنسيق المصدر لمحتوى رؤوس/تذييلات الصفحات يتم تجاهله إذا تم استخدام وضع [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode/\#KEEP-SOURCE-FORMATTING). القيمة الافتراضية هي true.

 **Examples:** 

يعرض كيفية تحديد تجاهل أو عدم تجاهل تنسيق المصدر لمحتوى رؤوس/تذييلات الصفحات.

```

 Document dstDoc = new Document(getMyDir() + "Document.docx");
 Document srcDoc = new Document(getMyDir() + "Header and footer types.docx");

 // If 'IgnoreHeaderFooter' is false then the original formatting for header/footer content
 // from "Header and footer types.docx" will be used.
 // If 'IgnoreHeaderFooter' is true then the formatting for header/footer content
 // from "Document.docx" will be used.
 ImportFormatOptions importFormatOptions = new ImportFormatOptions();
 importFormatOptions.setIgnoreHeaderFooter(false);

 dstDoc.appendDocument(srcDoc, ImportFormatMode.KEEP_SOURCE_FORMATTING, importFormatOptions);

 dstDoc.save(getArtifactsDir() + "DocumentBuilder.DoNotIgnoreHeaderFooter.docx");
 
```

**Returns:**
منطقي - قيمة منطقية تحدد أن تنسيق المصدر لمحتوى رؤوس/تذييلات الصفحات يتم تجاهله إذا تم استخدام وضع [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode/\#KEEP-SOURCE-FORMATTING).
### getIgnoreTextBoxes() {#getIgnoreTextBoxes}
```
public boolean getIgnoreTextBoxes()
```


يحصل على قيمة منطقية تحدد أن تنسيق المصدر لمحتوى صناديق النص يتم تجاهله إذا تم استخدام وضع [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode/\#KEEP-SOURCE-FORMATTING). القيمة الافتراضية هي  true .

 **Examples:** 

يعرض كيفية إدارة تنسيق صندوق النص أثناء إلحاق مستند.

```

 // Create a document that will have nodes from another document inserted into it.
 Document dstDoc = new Document();
 DocumentBuilder builder = new DocumentBuilder(dstDoc);

 builder.writeln("Hello world!");

 // Create another document with a text box, which we will import into the first document.
 Document srcDoc = new Document();
 builder = new DocumentBuilder(srcDoc);

 Shape textBox = builder.insertShape(ShapeType.TEXT_BOX, 300.0, 100.0);
 builder.moveTo(textBox.getFirstParagraph());
 builder.getParagraphFormat().getStyle().getFont().setName("Courier New");
 builder.getParagraphFormat().getStyle().getFont().setSize(24.0);
 builder.write("Textbox contents");

 // Set a flag to specify whether to clear or preserve text box formatting
 // while importing them to other documents.
 ImportFormatOptions importFormatOptions = new ImportFormatOptions();
 importFormatOptions.setIgnoreTextBoxes(ignoreTextBoxes);

 // Import the text box from the source document into the destination document,
 // and then verify whether we have preserved the styling of its text contents.
 NodeImporter importer = new NodeImporter(srcDoc, dstDoc, ImportFormatMode.KEEP_SOURCE_FORMATTING, importFormatOptions);
 Shape importedTextBox = (Shape) importer.importNode(textBox, true);
 dstDoc.getFirstSection().getBody().getParagraphs().get(1).appendChild(importedTextBox);

 if (ignoreTextBoxes) {
     Assert.assertEquals(12.0d, importedTextBox.getFirstParagraph().getRuns().get(0).getFont().getSize());
     Assert.assertEquals("Times New Roman", importedTextBox.getFirstParagraph().getRuns().get(0).getFont().getName());
 } else {
     Assert.assertEquals(24.0d, importedTextBox.getFirstParagraph().getRuns().get(0).getFont().getSize());
     Assert.assertEquals("Courier New", importedTextBox.getFirstParagraph().getRuns().get(0).getFont().getName());
 }

 dstDoc.save(getArtifactsDir() + "DocumentBuilder.IgnoreTextBoxes.docx");
 
```

**Returns:**
منطقي - قيمة منطقية تحدد أن تنسيق المصدر لمحتوى صناديق النص يتم تجاهله إذا تم استخدام وضع [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode/\#KEEP-SOURCE-FORMATTING).
### getKeepSourceNumbering() {#getKeepSourceNumbering}
```
public boolean getKeepSourceNumbering()
```


يحصل على قيمة منطقية تحدد كيفية استيراد الترقيم عندما يتصادم في المستندات المصدر والوجهة. القيمة الافتراضية هي  false .

 **Examples:** 

يعرض كيفية استيراد مستند يحتوي على قوائم مرقمة.

```

 Document srcDoc = new Document(getMyDir() + "List source.docx");
 Document dstDoc = new Document(getMyDir() + "List destination.docx");

 Assert.assertEquals(dstDoc.getLists().getCount(), 4);

 ImportFormatOptions options = new ImportFormatOptions();

 // If there is a clash of list styles, apply the list format of the source document.
 // Set the "KeepSourceNumbering" property to "false" to not import any list numbers into the destination document.
 // Set the "KeepSourceNumbering" property to "true" import all clashing
 // list style numbering with the same appearance that it had in the source document.
 options.setKeepSourceNumbering(isKeepSourceNumbering);

 dstDoc.appendDocument(srcDoc, ImportFormatMode.KEEP_SOURCE_FORMATTING, options);
 dstDoc.updateListLabels();

 if (isKeepSourceNumbering)
     Assert.assertEquals(dstDoc.getLists().getCount(), 5);
 else
     Assert.assertEquals(dstDoc.getLists().getCount(), 4);
 
```

يعرض كيفية حل التعارض عند استيراد مستندات تحتوي على قوائم بنفس معرف تعريف القائمة.

```

 Document srcDoc = new Document(getMyDir() + "List with the same definition identifier - source.docx");
 Document dstDoc = new Document(getMyDir() + "List with the same definition identifier - destination.docx");

 ImportFormatOptions importFormatOptions = new ImportFormatOptions();

 // Set the "KeepSourceNumbering" property to "true" to apply a different list definition ID
 // to identical styles as Aspose.Words imports them into destination documents.
 importFormatOptions.setKeepSourceNumbering(true);
 dstDoc.appendDocument(srcDoc, ImportFormatMode.USE_DESTINATION_STYLES, importFormatOptions);

 dstDoc.updateListLabels();
 
```

يعرض كيفية حل تعارض ترقيم القوائم في المستندات المصدر والوجهة.

```

 // Open a document with a custom list numbering scheme, and then clone it.
 // Since both have the same numbering format, the formats will clash if we import one document into the other.
 Document srcDoc = new Document(getMyDir() + "Custom list numbering.docx");
 Document dstDoc = srcDoc.deepClone();

 // When we import the document's clone into the original and then append it,
 // then the two lists with the same list format will join.
 // If we set the "KeepSourceNumbering" flag to "false", then the list from the document clone
 // that we append to the original will carry on the numbering of the list we append it to.
 // This will effectively merge the two lists into one.
 // If we set the "KeepSourceNumbering" flag to "true", then the document clone
 // list will preserve its original numbering, making the two lists appear as separate lists.
 ImportFormatOptions importFormatOptions = new ImportFormatOptions();
 importFormatOptions.setKeepSourceNumbering(keepSourceNumbering);

 NodeImporter importer = new NodeImporter(srcDoc, dstDoc, ImportFormatMode.KEEP_DIFFERENT_STYLES, importFormatOptions);
 for (Paragraph paragraph : srcDoc.getFirstSection().getBody().getParagraphs()) {
     Node importedNode = importer.importNode(paragraph, true);
     dstDoc.getFirstSection().getBody().appendChild(importedNode);
 }

 dstDoc.updateListLabels();

 if (keepSourceNumbering) {
     Assert.assertEquals(
             "6. Item 1\r\n" +
                     "7. Item 2 \r\n" +
                     "8. Item 3\r\n" +
                     "9. Item 4\r\n" +
                     "6. Item 1\r\n" +
                     "7. Item 2 \r\n" +
                     "8. Item 3\r\n" +
                     "9. Item 4", dstDoc.getFirstSection().getBody().toString(SaveFormat.TEXT).trim());
 } else {
     Assert.assertEquals(
             "6. Item 1\r\n" +
                     "7. Item 2 \r\n" +
                     "8. Item 3\r\n" +
                     "9. Item 4\r\n" +
                     "10. Item 1\r\n" +
                     "11. Item 2 \r\n" +
                     "12. Item 3\r\n" +
                     "13. Item 4", dstDoc.getFirstSection().getBody().toString(SaveFormat.TEXT).trim());
 }
 
```

**Returns:**
منطقي - قيمة منطقية تحدد كيفية استيراد الترقيم عندما يتصادم في المستندات المصدر والوجهة.
### getMergePastedLists() {#getMergePastedLists}
```
public boolean getMergePastedLists()
```


يحصل على قيمة منطقية تحدد ما إذا كانت القوائم الملصوقة ستدمج مع القوائم المحيطة. القيمة الافتراضية هي  false .

 **Examples:** 

يعرض كيفية دمج القوائم من مستند.

```

 Document srcDoc = new Document(getMyDir() + "List item.docx");
 Document dstDoc = new Document(getMyDir() + "List destination.docx");

 ImportFormatOptions options = new ImportFormatOptions(); { options.setMergePastedLists(true); }

 // Set the "MergePastedLists" property to "true" pasted lists will be merged with surrounding lists.
 dstDoc.appendDocument(srcDoc, ImportFormatMode.USE_DESTINATION_STYLES, options);

 dstDoc.save(getArtifactsDir() + "Document.MergePastedLists.docx");
 
```

**Returns:**
منطقي - قيمة منطقية تحدد ما إذا كانت القوائم الملصوقة ستدمج مع القوائم المحيطة.
### getResolveThemeColors() {#getResolveThemeColors}
```
public boolean getResolveThemeColors()
```


يحصل على قيمة منطقية تحدد ما إذا كان سيتم حل ألوان السمة للأشكال بالقوة. القيمة الافتراضية هي  false .

 **Remarks:** 

يرجى ملاحظة أن هذا الخيار ذو صلة فقط بوضع [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode/\#KEEP-SOURCE-FORMATTING).

عادةً، لا يقوم **Aspose.Words** بحل ألوان السمة المصدرية عند استيراد الأنماط التي يمكن حفظها دون توسيع سمات التنسيق إلى سمات مباشرة. ومع ذلك، في هذه الحالة قد تختلف الألوان الفعلية للأشكال المستوردة عن تلك التي كانت في المستند الأصلي. السبب في ذلك هو اختلاف ألوان السمة بين المستندات المصدر والوجهة. ضبط هذا الخيار على  true  يجبر على حل ألوان سمة الشكل المصدرية وبالتالي الحفاظ على اللون الفعلي للأشكال كما هو في المستند المصدر.

 **Examples:** 

يعرض كيفية استيراد عقدة مع حل ألوان سمة الشكل المصدرية.

```

 Document srcDoc = new Document();
 DocumentBuilder builder = new DocumentBuilder(srcDoc);

 // Move to the primary footer and insert a shape that uses theme colors.
 builder.moveToHeaderFooter(HeaderFooterType.FOOTER_PRIMARY);
 Shape shape = builder.insertShape(ShapeType.RECTANGLE, 100.0, 50.0);
 shape.getStroke().setForeThemeColor(ThemeColor.DARK_1);

 Document dstDoc = new Document();
 // Import the source footer into the destination document with theme colors resolved,
 // so the shape preserves its actual color from the source document.
 HeaderFooter footer = srcDoc.getFirstSection().getHeadersFooters().getByHeaderFooterType(HeaderFooterType.FOOTER_PRIMARY);

 ImportFormatOptions options = new ImportFormatOptions();
 options.setResolveThemeColors(true);
 HeaderFooter importedFooter = (HeaderFooter)dstDoc.importNode(footer, true, ImportFormatMode.KEEP_SOURCE_FORMATTING, options);

 dstDoc.getFirstSection().getHeadersFooters().add(importedFooter);

 dstDoc.save(getArtifactsDir() + "DocumentBase.ImportNodeWithResolveThemeColors.docx");
 
```

**Returns:**
منطقي - قيمة منطقية تحدد ما إذا كان سيتم حل ألوان سمة الأشكال بالقوة.
### getSmartStyleBehavior() {#getSmartStyleBehavior}
```
public boolean getSmartStyleBehavior()
```


يحصل على قيمة منطقية تحدد كيفية استيراد الأنماط عندما تكون لها أسماء متساوية في المستندات المصدر والوجهة. القيمة الافتراضية هي  false .

 **Remarks:** 

عندما يكون هذا الخيار **مُمكّنًا**، سيتم توسيع النمط المصدر إلى سمات مباشرة داخل المستند الوجهة، إذا تم استخدام وضع الاستيراد [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode/\#KEEP-SOURCE-FORMATTING).

عندما يكون هذا الخيار **معطَّلًا**، سيتم توسيع النمط المصدر فقط إذا كان مرقمًا. لن يتم استبدال السمات الموجودة في الوجهة، بما في ذلك القوائم.

 **Examples:** 

يظهر كيفية حل الأنماط المكررة أثناء إدراج المستندات.

```

 Document dstDoc = new Document();
 DocumentBuilder builder = new DocumentBuilder(dstDoc);

 Style myStyle = builder.getDocument().getStyles().add(StyleType.PARAGRAPH, "MyStyle");
 myStyle.getFont().setSize(14.0);
 myStyle.getFont().setName("Courier New");
 myStyle.getFont().setColor(Color.BLUE);

 builder.getParagraphFormat().setStyleName(myStyle.getName());
 builder.writeln("Hello world!");

 // Clone the document and edit the clone's "MyStyle" style, so it is a different color than that of the original.
 // If we insert the clone into the original document, the two styles with the same name will cause a clash.
 Document srcDoc = dstDoc.deepClone();
 srcDoc.getStyles().get("MyStyle").getFont().setColor(Color.RED);

 // When we enable SmartStyleBehavior and use the KeepSourceFormatting import format mode,
 // Aspose.Words will resolve style clashes by converting source document styles.
 // with the same names as destination styles into direct paragraph attributes.
 ImportFormatOptions options = new ImportFormatOptions();
 options.setSmartStyleBehavior(true);

 builder.insertDocument(srcDoc, ImportFormatMode.KEEP_SOURCE_FORMATTING, options);

 dstDoc.save(getArtifactsDir() + "DocumentBuilder.SmartStyleBehavior.docx");
 
```

**Returns:**
منطقي - قيمة منطقية تحدد كيفية استيراد الأنماط عندما تكون لها أسماء متساوية في المستندات المصدر والوجهة.
### setAdjustSentenceAndWordSpacing(boolean value) {#setAdjustSentenceAndWordSpacing-boolean}
```
public void setAdjustSentenceAndWordSpacing(boolean value)
```


يضبط قيمة منطقية تحدد ما إذا كان سيتم تعديل تباعد الجمل والكلمات تلقائيًا. القيمة الافتراضية هي  false .

 **Examples:** 

يعرض كيفية تعديل تباعد الجمل والكلمات تلقائيًا.

```

 Document srcDoc = new Document();
 Document dstDoc = new Document();

 DocumentBuilder builder = new DocumentBuilder(srcDoc);
 builder.write("Dolor sit amet.");

 builder = new DocumentBuilder(dstDoc);
 builder.write("Lorem ipsum.");

 ImportFormatOptions options = new ImportFormatOptions(); { options.setAdjustSentenceAndWordSpacing(true); }
 builder.insertDocument(srcDoc, ImportFormatMode.USE_DESTINATION_STYLES, options);

 Assert.assertEquals("Lorem ipsum. Dolor sit amet.", dstDoc.getFirstSection().getBody().getFirstParagraph().getText().trim());
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | قيمة منطقية تحدد ما إذا كان سيتم تعديل تباعد الجمل والكلمات تلقائيًا. |

### setAppendDocumentWithNewPage(boolean value) {#setAppendDocumentWithNewPage-boolean}
```
public void setAppendDocumentWithNewPage(boolean value)
```


يضبط قيمة منطقية تشير إلى ما إذا كان يجب تغيير نوع القسم الأول المستورد إلى [SectionStart.NEW\_PAGE](../../com.aspose.words/sectionstart/\#NEW-PAGE) بالقوة عند استدعاء **M:Aspose.Words.Document.AppendDocument(Aspose.Words.Document,Aspose.Words.ImportFormatMode,Aspose.Words.ImportFormatOptions)**.

القيمة الافتراضية هي  true .

 **Remarks:** 

يرجى ملاحظة أن هذا الخيار ذو صلة فقط بطريقة **M:Aspose.Words.Document.AppendDocument(Aspose.Words.Document,Aspose.Words.ImportFormatMode,Aspose.Words.ImportFormatOptions)** ولا يؤثر على طرق الاستيراد الأخرى.

 **Examples:** 

يعرض كيفية الحفاظ على نوع القسم الأصلي.

```

 Document dstDoc = new Document();
 Document srcDoc = new Document();

 srcDoc.getFirstSection().getPageSetup().setSectionStart(SectionStart.CONTINUOUS);

 ImportFormatOptions options = new ImportFormatOptions();
 options.setAppendDocumentWithNewPage(false);
 dstDoc.appendDocument(srcDoc, ImportFormatMode.KEEP_SOURCE_FORMATTING, options);

 Assert.assertEquals(SectionStart.CONTINUOUS, dstDoc.getSections().get(1).getPageSetup().getSectionStart());
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| value | boolean | قيمة منطقية تشير إلى ما إذا كان سيتم تغيير نوع القسم الأول المستورد إلى [SectionStart.NEW\_PAGE](../../com.aspose.words/sectionstart/\#NEW-PAGE) بالقوة عند استدعاء **M:Aspose.Words.Document.AppendDocument(Aspose.Words.Document,Aspose.Words.ImportFormatMode,Aspose.Words.ImportFormatOptions)**. |

### setForceCopyStyles(boolean value) {#setForceCopyStyles-boolean}
```
public void setForceCopyStyles(boolean value)
```


يضبط قيمة منطقية تشير إلى نسخ الأنماط المتضاربة في وضع [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode/\#KEEP-SOURCE-FORMATTING) . القيمة الافتراضية هي false .

 **Remarks:** 

بشكل افتراضي، إذا كان هناك نمط مطابق موجود بالفعل في مستند الوجهة، يتم توسيع تنسيق النمط المصدر إلى سمات العقدة المباشرة وتُعاد تعيين نمط هذه العقدة إلى القيمة الافتراضية.

عند ضبط هذا الخيار على true، سيتم نسخ النمط المصدر بالقوة إلى مستند الوجهة باسم فريد وتطبيقه على العقدة المستوردة.

ملاحظة، في هذه الحالة لا يُضمن الحفاظ على تنسيق العقدة المستوردة في مستند الوجهة.

 **Examples:** 

يعرض كيفية نسخ أنماط المصدر بأسماء فريدة بالقوة.

```

 // Both documents contain MyStyle1 and MyStyle2, MyStyle3 exists only in a source document.
 Document srcDoc = new Document(getMyDir() + "Styles source.docx");
 Document dstDoc = new Document(getMyDir() + "Styles destination.docx");

 ImportFormatOptions options = new ImportFormatOptions(); { options.setForceCopyStyles(true); }
 dstDoc.appendDocument(srcDoc, ImportFormatMode.KEEP_SOURCE_FORMATTING, options);

 ParagraphCollection paras = dstDoc.getSections().get(1).getBody().getParagraphs();

 Assert.assertEquals(paras.get(0).getParagraphFormat().getStyle().getName(), "MyStyle1_0");
 Assert.assertEquals(paras.get(1).getParagraphFormat().getStyle().getName(), "MyStyle2_0");
 Assert.assertEquals(paras.get(2).getParagraphFormat().getStyle().getName(), "MyStyle3");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| value | boolean | قيمة منطقية تشير إلى نسخ الأنماط المتضاربة في وضع [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode/\#KEEP-SOURCE-FORMATTING) . |

### setIgnoreHeaderFooter(boolean value) {#setIgnoreHeaderFooter-boolean}
```
public void setIgnoreHeaderFooter(boolean value)
```


يضبط قيمة منطقية تحدد أن تنسيق المصدر لمحتوى رؤوس/تذييلات الصفحات يتم تجاهله إذا تم استخدام وضع [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode/\# KEEP-SOURCE-FORMATTING) . القيمة الافتراضية هي true .

 **Examples:** 

يعرض كيفية تحديد تجاهل أو عدم تجاهل تنسيق المصدر لمحتوى رؤوس/تذييلات الصفحات.

```

 Document dstDoc = new Document(getMyDir() + "Document.docx");
 Document srcDoc = new Document(getMyDir() + "Header and footer types.docx");

 // If 'IgnoreHeaderFooter' is false then the original formatting for header/footer content
 // from "Header and footer types.docx" will be used.
 // If 'IgnoreHeaderFooter' is true then the formatting for header/footer content
 // from "Document.docx" will be used.
 ImportFormatOptions importFormatOptions = new ImportFormatOptions();
 importFormatOptions.setIgnoreHeaderFooter(false);

 dstDoc.appendDocument(srcDoc, ImportFormatMode.KEEP_SOURCE_FORMATTING, importFormatOptions);

 dstDoc.save(getArtifactsDir() + "DocumentBuilder.DoNotIgnoreHeaderFooter.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| value | boolean | قيمة منطقية تحدد أن تنسيق المصدر لمحتوى رؤوس/تذييلات الصفحات يتم تجاهله إذا تم استخدام وضع [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode/\#KEEP-SOURCE-FORMATTING) . |

### setIgnoreTextBoxes(boolean value) {#setIgnoreTextBoxes-boolean}
```
public void setIgnoreTextBoxes(boolean value)
```


يضبط قيمة منطقية تحدد أن تنسيق المصدر لمحتوى مربعات النص يتم تجاهله إذا تم استخدام وضع [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode/\#KEEP-SOURCE-FORMATTING) . القيمة الافتراضية هي true .

 **Examples:** 

يعرض كيفية إدارة تنسيق صندوق النص أثناء إلحاق مستند.

```

 // Create a document that will have nodes from another document inserted into it.
 Document dstDoc = new Document();
 DocumentBuilder builder = new DocumentBuilder(dstDoc);

 builder.writeln("Hello world!");

 // Create another document with a text box, which we will import into the first document.
 Document srcDoc = new Document();
 builder = new DocumentBuilder(srcDoc);

 Shape textBox = builder.insertShape(ShapeType.TEXT_BOX, 300.0, 100.0);
 builder.moveTo(textBox.getFirstParagraph());
 builder.getParagraphFormat().getStyle().getFont().setName("Courier New");
 builder.getParagraphFormat().getStyle().getFont().setSize(24.0);
 builder.write("Textbox contents");

 // Set a flag to specify whether to clear or preserve text box formatting
 // while importing them to other documents.
 ImportFormatOptions importFormatOptions = new ImportFormatOptions();
 importFormatOptions.setIgnoreTextBoxes(ignoreTextBoxes);

 // Import the text box from the source document into the destination document,
 // and then verify whether we have preserved the styling of its text contents.
 NodeImporter importer = new NodeImporter(srcDoc, dstDoc, ImportFormatMode.KEEP_SOURCE_FORMATTING, importFormatOptions);
 Shape importedTextBox = (Shape) importer.importNode(textBox, true);
 dstDoc.getFirstSection().getBody().getParagraphs().get(1).appendChild(importedTextBox);

 if (ignoreTextBoxes) {
     Assert.assertEquals(12.0d, importedTextBox.getFirstParagraph().getRuns().get(0).getFont().getSize());
     Assert.assertEquals("Times New Roman", importedTextBox.getFirstParagraph().getRuns().get(0).getFont().getName());
 } else {
     Assert.assertEquals(24.0d, importedTextBox.getFirstParagraph().getRuns().get(0).getFont().getSize());
     Assert.assertEquals("Courier New", importedTextBox.getFirstParagraph().getRuns().get(0).getFont().getName());
 }

 dstDoc.save(getArtifactsDir() + "DocumentBuilder.IgnoreTextBoxes.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| value | boolean | قيمة منطقية تحدد أن تنسيق المصدر لمحتوى مربعات النص يتم تجاهله إذا تم استخدام وضع [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode/\#KEEP-SOURCE-FORMATTING) . |

### setKeepSourceNumbering(boolean value) {#setKeepSourceNumbering-boolean}
```
public void setKeepSourceNumbering(boolean value)
```


يضبط قيمة منطقية تحدد كيفية استيراد الترقيم عندما يتعارض في المستندات المصدر والوجهة. القيمة الافتراضية هي false .

 **Examples:** 

يعرض كيفية استيراد مستند يحتوي على قوائم مرقمة.

```

 Document srcDoc = new Document(getMyDir() + "List source.docx");
 Document dstDoc = new Document(getMyDir() + "List destination.docx");

 Assert.assertEquals(dstDoc.getLists().getCount(), 4);

 ImportFormatOptions options = new ImportFormatOptions();

 // If there is a clash of list styles, apply the list format of the source document.
 // Set the "KeepSourceNumbering" property to "false" to not import any list numbers into the destination document.
 // Set the "KeepSourceNumbering" property to "true" import all clashing
 // list style numbering with the same appearance that it had in the source document.
 options.setKeepSourceNumbering(isKeepSourceNumbering);

 dstDoc.appendDocument(srcDoc, ImportFormatMode.KEEP_SOURCE_FORMATTING, options);
 dstDoc.updateListLabels();

 if (isKeepSourceNumbering)
     Assert.assertEquals(dstDoc.getLists().getCount(), 5);
 else
     Assert.assertEquals(dstDoc.getLists().getCount(), 4);
 
```

يعرض كيفية حل التعارض عند استيراد مستندات تحتوي على قوائم بنفس معرف تعريف القائمة.

```

 Document srcDoc = new Document(getMyDir() + "List with the same definition identifier - source.docx");
 Document dstDoc = new Document(getMyDir() + "List with the same definition identifier - destination.docx");

 ImportFormatOptions importFormatOptions = new ImportFormatOptions();

 // Set the "KeepSourceNumbering" property to "true" to apply a different list definition ID
 // to identical styles as Aspose.Words imports them into destination documents.
 importFormatOptions.setKeepSourceNumbering(true);
 dstDoc.appendDocument(srcDoc, ImportFormatMode.USE_DESTINATION_STYLES, importFormatOptions);

 dstDoc.updateListLabels();
 
```

يعرض كيفية حل تعارض ترقيم القوائم في المستندات المصدر والوجهة.

```

 // Open a document with a custom list numbering scheme, and then clone it.
 // Since both have the same numbering format, the formats will clash if we import one document into the other.
 Document srcDoc = new Document(getMyDir() + "Custom list numbering.docx");
 Document dstDoc = srcDoc.deepClone();

 // When we import the document's clone into the original and then append it,
 // then the two lists with the same list format will join.
 // If we set the "KeepSourceNumbering" flag to "false", then the list from the document clone
 // that we append to the original will carry on the numbering of the list we append it to.
 // This will effectively merge the two lists into one.
 // If we set the "KeepSourceNumbering" flag to "true", then the document clone
 // list will preserve its original numbering, making the two lists appear as separate lists.
 ImportFormatOptions importFormatOptions = new ImportFormatOptions();
 importFormatOptions.setKeepSourceNumbering(keepSourceNumbering);

 NodeImporter importer = new NodeImporter(srcDoc, dstDoc, ImportFormatMode.KEEP_DIFFERENT_STYLES, importFormatOptions);
 for (Paragraph paragraph : srcDoc.getFirstSection().getBody().getParagraphs()) {
     Node importedNode = importer.importNode(paragraph, true);
     dstDoc.getFirstSection().getBody().appendChild(importedNode);
 }

 dstDoc.updateListLabels();

 if (keepSourceNumbering) {
     Assert.assertEquals(
             "6. Item 1\r\n" +
                     "7. Item 2 \r\n" +
                     "8. Item 3\r\n" +
                     "9. Item 4\r\n" +
                     "6. Item 1\r\n" +
                     "7. Item 2 \r\n" +
                     "8. Item 3\r\n" +
                     "9. Item 4", dstDoc.getFirstSection().getBody().toString(SaveFormat.TEXT).trim());
 } else {
     Assert.assertEquals(
             "6. Item 1\r\n" +
                     "7. Item 2 \r\n" +
                     "8. Item 3\r\n" +
                     "9. Item 4\r\n" +
                     "10. Item 1\r\n" +
                     "11. Item 2 \r\n" +
                     "12. Item 3\r\n" +
                     "13. Item 4", dstDoc.getFirstSection().getBody().toString(SaveFormat.TEXT).trim());
 }
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | قيمة منطقية تحدد كيفية استيراد الترقيم عندما يتعارض في المستندات المصدر والوجهة. |

### setMergePastedLists(boolean value) {#setMergePastedLists-boolean}
```
public void setMergePastedLists(boolean value)
```


يضبط قيمة منطقية تحدد ما إذا كانت القوائم الملصوقة ستُدمج مع القوائم المحيطة. القيمة الافتراضية هي false .

 **Examples:** 

يعرض كيفية دمج القوائم من مستند.

```

 Document srcDoc = new Document(getMyDir() + "List item.docx");
 Document dstDoc = new Document(getMyDir() + "List destination.docx");

 ImportFormatOptions options = new ImportFormatOptions(); { options.setMergePastedLists(true); }

 // Set the "MergePastedLists" property to "true" pasted lists will be merged with surrounding lists.
 dstDoc.appendDocument(srcDoc, ImportFormatMode.USE_DESTINATION_STYLES, options);

 dstDoc.save(getArtifactsDir() + "Document.MergePastedLists.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | قيمة منطقية تحدد ما إذا كانت القوائم الملصوقة ستُدمج مع القوائم المحيطة. |

### setResolveThemeColors(boolean value) {#setResolveThemeColors-boolean}
```
public void setResolveThemeColors(boolean value)
```


يضبط قيمة منطقية تحدد ما إذا كان يجب حل ألوان السمة للأشكال بالقوة. القيمة الافتراضية هي false .

 **Remarks:** 

يرجى ملاحظة أن هذا الخيار ذو صلة فقط بوضع [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode/\#KEEP-SOURCE-FORMATTING).

عادةً، لا يقوم **Aspose.Words** بحل ألوان السمة المصدرية عند استيراد الأنماط التي يمكن حفظها دون توسيع سمات التنسيق إلى سمات مباشرة. ومع ذلك، في هذه الحالة قد تختلف الألوان الفعلية للأشكال المستوردة عن تلك التي كانت في المستند الأصلي. السبب في ذلك هو اختلاف ألوان السمة بين المستندات المصدر والوجهة. ضبط هذا الخيار على  true  يجبر على حل ألوان سمة الشكل المصدرية وبالتالي الحفاظ على اللون الفعلي للأشكال كما هو في المستند المصدر.

 **Examples:** 

يعرض كيفية استيراد عقدة مع حل ألوان سمة الشكل المصدرية.

```

 Document srcDoc = new Document();
 DocumentBuilder builder = new DocumentBuilder(srcDoc);

 // Move to the primary footer and insert a shape that uses theme colors.
 builder.moveToHeaderFooter(HeaderFooterType.FOOTER_PRIMARY);
 Shape shape = builder.insertShape(ShapeType.RECTANGLE, 100.0, 50.0);
 shape.getStroke().setForeThemeColor(ThemeColor.DARK_1);

 Document dstDoc = new Document();
 // Import the source footer into the destination document with theme colors resolved,
 // so the shape preserves its actual color from the source document.
 HeaderFooter footer = srcDoc.getFirstSection().getHeadersFooters().getByHeaderFooterType(HeaderFooterType.FOOTER_PRIMARY);

 ImportFormatOptions options = new ImportFormatOptions();
 options.setResolveThemeColors(true);
 HeaderFooter importedFooter = (HeaderFooter)dstDoc.importNode(footer, true, ImportFormatMode.KEEP_SOURCE_FORMATTING, options);

 dstDoc.getFirstSection().getHeadersFooters().add(importedFooter);

 dstDoc.save(getArtifactsDir() + "DocumentBase.ImportNodeWithResolveThemeColors.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | قيمة منطقية تحدد ما إذا كان يجب حل ألوان السمة للأشكال بالقوة. |

### setSmartStyleBehavior(boolean value) {#setSmartStyleBehavior-boolean}
```
public void setSmartStyleBehavior(boolean value)
```


يضبط قيمة منطقية تحدد كيفية استيراد الأنماط عندما تكون لها أسماء متساوية في المستندات المصدر والوجهة. القيمة الافتراضية هي false .

 **Remarks:** 

عندما يكون هذا الخيار **مُمكّنًا**، سيتم توسيع النمط المصدر إلى سمات مباشرة داخل المستند الوجهة، إذا تم استخدام وضع الاستيراد [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode/\#KEEP-SOURCE-FORMATTING).

عندما يكون هذا الخيار **معطَّلًا**، سيتم توسيع النمط المصدر فقط إذا كان مرقمًا. لن يتم استبدال السمات الموجودة في الوجهة، بما في ذلك القوائم.

 **Examples:** 

يظهر كيفية حل الأنماط المكررة أثناء إدراج المستندات.

```

 Document dstDoc = new Document();
 DocumentBuilder builder = new DocumentBuilder(dstDoc);

 Style myStyle = builder.getDocument().getStyles().add(StyleType.PARAGRAPH, "MyStyle");
 myStyle.getFont().setSize(14.0);
 myStyle.getFont().setName("Courier New");
 myStyle.getFont().setColor(Color.BLUE);

 builder.getParagraphFormat().setStyleName(myStyle.getName());
 builder.writeln("Hello world!");

 // Clone the document and edit the clone's "MyStyle" style, so it is a different color than that of the original.
 // If we insert the clone into the original document, the two styles with the same name will cause a clash.
 Document srcDoc = dstDoc.deepClone();
 srcDoc.getStyles().get("MyStyle").getFont().setColor(Color.RED);

 // When we enable SmartStyleBehavior and use the KeepSourceFormatting import format mode,
 // Aspose.Words will resolve style clashes by converting source document styles.
 // with the same names as destination styles into direct paragraph attributes.
 ImportFormatOptions options = new ImportFormatOptions();
 options.setSmartStyleBehavior(true);

 builder.insertDocument(srcDoc, ImportFormatMode.KEEP_SOURCE_FORMATTING, options);

 dstDoc.save(getArtifactsDir() + "DocumentBuilder.SmartStyleBehavior.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | قيمة منطقية تحدد كيفية استيراد الأنماط عندما تكون لها أسماء متساوية في المستندات المصدر والوجهة. |

