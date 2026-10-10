---
title: "ParagraphFormat"
linktitle: "ParagraphFormat"
second_title: "Aspose.Words لـ Java"
description: "يمثل جميع تنسيقات الفقرة في Java."
type: docs
weight: 525
url: /ar/java/com.aspose.words/paragraphformat/
---

**Inheritance:**
java.lang.Object
```
public class ParagraphFormat
```

يمثل جميع تنسيقات الفقرة.

لمزيد من المعلومات، زر مقالة الوثائق [ Working with Paragraphs ][Working with Paragraphs].

 **Examples:** 

يوضح كيفية إنشاء مستند Aspose.Words يدوياً.

```

 Document doc = new Document();

 // A blank document contains one section, one body and one paragraph.
 // Call the "RemoveAllChildren" method to remove all those nodes,
 // and end up with a document node with no children.
 doc.removeAllChildren();

 // This document now has no composite child nodes that we can add content to.
 // If we wish to edit it, we will need to repopulate its node collection.
 // First, create a new section, and then append it as a child to the root document node.
 Section section = new Section(doc);
 doc.appendChild(section);

 // Set some page setup properties for the section.
 section.getPageSetup().setSectionStart(SectionStart.NEW_PAGE);
 section.getPageSetup().setPaperSize(PaperSize.LETTER);

 // A section needs a body, which will contain and display all its contents
 // on the page between the section's header and footer.
 Body body = new Body(doc);
 section.appendChild(body);

 // Create a paragraph, set some formatting properties, and then append it as a child to the body.
 Paragraph para = new Paragraph(doc);

 para.getParagraphFormat().setStyleName("Heading 1");
 para.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);

 body.appendChild(para);

 // Finally, add some content to do the document. Create a run,
 // set its appearance and contents, and then append it as a child to the paragraph.
 Run run = new Run(doc);
 run.setText("Hello World!");
 run.getFont().setColor(Color.RED);
 para.appendChild(run);

 Assert.assertEquals("Hello World!", doc.getText().trim());

 doc.save(getArtifactsDir() + "Section.CreateManually.docx");
 
```


[Working with Paragraphs]: https://docs.aspose.com/words/java/working-with-paragraphs/
## الطرق

| طريقة | الوصف |
| --- | --- |
| [clearFormatting()](#clearFormatting) | يعيد تعيين تنسيق الفقرة إلى الإعدادات الافتراضية. |
| [fetchInheritedBorderAttr(int key)](#fetchInheritedBorderAttr-int) |  |
| [fetchInheritedShadingAttr(int key)](#fetchInheritedShadingAttr-int) |  |
| [getAddSpaceBetweenFarEastAndAlpha()](#getAddSpaceBetweenFarEastAndAlpha) | يحصل على علم يوضح ما إذا كان يتم تعديل التباعد بين الأحرف تلقائيًا بين مناطق النص اللاتيني ومناطق النص الآسيوي الشرقي في الفقرة الحالية. |
| [getAddSpaceBetweenFarEastAndDigit()](#getAddSpaceBetweenFarEastAndDigit) | يحصل على علم يوضح ما إذا كان يتم تعديل التباعد بين الأحرف تلقائيًا بين مناطق الأرقام ومناطق النص الآسيوي الشرقي في الفقرة الحالية. |
| [getAlignment()](#getAlignment) | يحصل على محاذاة النص للفقرة. |
| [getBaselineAlignment()](#getBaselineAlignment) | يحصل على الموضع العمودي للخطوط على السطر. |
| [getBidi()](#getBidi) | يحصل على ما إذا كانت هذه الفقرة من اليمين إلى اليسار. |
| [getBorders()](#getBorders) | يحصل على مجموعة حدود الفقرة. |
| [getCharacterUnitFirstLineIndent()](#getCharacterUnitFirstLineIndent) | يحصل على القيمة (بالحروف) للمسافة البادئة للسطر الأول أو المعلقة. |
| [getCharacterUnitLeftIndent()](#getCharacterUnitLeftIndent) | يحصل على قيمة المسافة البادئة اليسرى (بالحروف) للفقرات المحددة. |
| [getCharacterUnitRightIndent()](#getCharacterUnitRightIndent) | يحصل على قيمة المسافة البادئة اليمنى (بالحروف) للفقرات المحددة. |
| [getDirectBorderAttr(int key)](#getDirectBorderAttr-int) |  |
| [getDropCapPosition()](#getDropCapPosition) | يحصل على موضع النص المتدلي (drop cap). |
| [getFarEastLineBreakControl()](#getFarEastLineBreakControl) | يحصل على علم يوضح ما إذا كانت قواعد كسر السطر الآسيوي الشرقي مطبقة على الفقرة الحالية. |
| [getFirstLineIndent()](#getFirstLineIndent) | يحصل على القيمة (بالنقاط) للمسافة البادئة للسطر الأول أو المعلقة. |
| [getHangingPunctuation()](#getHangingPunctuation) | يحصل على علم يوضح ما إذا كانت علامات الترقيم المعلقة مفعلة للفقرة الحالية. |
| [getKeepTogether()](#getKeepTogether) | صحيح إذا كان يجب أن تبقى جميع الأسطر في الفقرة على نفس الصفحة. |
| [getKeepWithNext()](#getKeepWithNext) | صحيح إذا كان يجب أن تبقى الفقرة على نفس الصفحة مع الفقرة التي تليها. |
| [getLeftIndent()](#getLeftIndent) | يحصل على القيمة (بالنقاط) التي تمثل المسافة البادئة اليسرى للفقرة. |
| [getLineSpacing()](#getLineSpacing) | يحصل على تباعد السطر (بالنقاط) للفقرة. |
| [getLineSpacingRule()](#getLineSpacingRule) | يحصل على تباعد السطر للفقرة. |
| [getLineUnitAfter()](#getLineUnitAfter) | يحصل على مقدار المسافة (بالخطوط الشبكية) بعد الفقرات. |
| [getLineUnitBefore()](#getLineUnitBefore) | يحصل على مقدار المسافة (بالخطوط الشبكية) قبل الفقرات. |
| [getLinesToDrop()](#getLinesToDrop) | يحصل على عدد أسطر نص الفقرة المستخدمة لحساب ارتفاع الحرف الأول الكبير. |
| [getMirrorIndents()](#getMirrorIndents) | يحصل على علم يشير إلى ما إذا كانت المسافات البادئة اليسرى واليمنى ذات عرض متساوٍ. |
| [getNoSpaceBetweenParagraphsOfSameStyle()](#getNoSpaceBetweenParagraphsOfSameStyle) | عند true، سيتم تجاهل [getSpaceBefore()](../../com.aspose.words/paragraphformat/\#getSpaceBefore) / [setSpaceBefore(double)](../../com.aspose.words/paragraphformat/\#setSpaceBefore-double) و [getSpaceAfter()](../../com.aspose.words/paragraphformat/\#getSpaceAfter) / [setSpaceAfter(double)](../../com.aspose.words/paragraphformat/\#setSpaceAfter-double) بين الفقرات ذات النمط نفسه. |
| [getOutlineLevel()](#getOutlineLevel) | يحدد مستوى المخطط للفقرة في المستند. |
| [getPageBreakBefore()](#getPageBreakBefore) | صحيح إذا تم فرض فاصل صفحة قبل الفقرة. |
| [getRightIndent()](#getRightIndent) | يحصل على القيمة (بالنقاط) التي تمثل المسافة البادئة اليمنى للفقرة. |
| [getShading()](#getShading) | يعيد كائن [Shading](../../com.aspose.words/shading/) الذي يشير إلى تنسيق التظليل للفقرة. |
| [getSnapToGrid()](#getSnapToGrid) | يحدد ما إذا كان يجب على الفقرة الحالية استخدام إعدادات خطوط شبكة المستند لكل صفحة عند تنسيق المحتوى داخل الفقرة. |
| [getSpaceAfter()](#getSpaceAfter) | يحصل على مقدار المسافة (بالنقاط) بعد الفقرة. |
| [getSpaceAfterAuto()](#getSpaceAfterAuto) | صحيح إذا تم تعيين مقدار المسافة بعد الفقرة تلقائيًا. |
| [getSpaceBefore()](#getSpaceBefore) | يحصل على مقدار المسافة (بالنقاط) قبل الفقرة. |
| [getSpaceBeforeAuto()](#getSpaceBeforeAuto) | صحيح إذا تم تعيين مقدار المسافة قبل الفقرة تلقائيًا. |
| [getStyle()](#getStyle) | يحصل على نمط الفقرة المطبق على هذا التنسيق. |
| [getStyleIdentifier()](#getStyleIdentifier) | يحصل على معرف النمط المستقل عن اللغة لنمط الفقرة المطبق على هذا التنسيق. |
| [getStyleName()](#getStyleName) | يحصل على اسم نمط الفقرة المطبق على هذا التنسيق. |
| [getSuppressAutoHyphens()](#getSuppressAutoHyphens) | يحدد ما إذا كان يجب إعفاء الفقرة الحالية من أي تجزئة تُطبق في إعدادات المستند. |
| [getSuppressLineNumbers()](#getSuppressLineNumbers) | يحدد ما إذا كان يجب إعفاء أسطر الفقرة الحالية من ترقيم الأسطر الذي يُطبق في القسم الأب. |
| [getTabStops()](#getTabStops) | يحصل على مجموعة نقاط التبويب المخصصة المعرفة لهذا الكائن. |
| [getWidowControl()](#getWidowControl) | صحيح إذا كان يجب أن تبقى السطران الأول والأخير في الفقرة على نفس الصفحة مع باقي الفقرة. |
| [getWordWrap()](#getWordWrap) | إذا كانت هذه الخاصية خاطئة، يمكن لف النص اللاتيني في وسط الكلمة للفقرة الحالية. |
| [isHeading()](#isHeading) | صحيح عندما يكون نمط الفقرة أحد أنماط العناوين المدمجة. |
| [isListItem()](#isListItem) | صحيح عندما تكون الفقرة عنصرًا في قائمة نقطية أو رقمية. |
| [setAddSpaceBetweenFarEastAndAlpha(boolean value)](#setAddSpaceBetweenFarEastAndAlpha-boolean) | يضبط علامة تشير إلى ما إذا كان يتم تعديل التباعد بين الأحرف تلقائيًا بين مناطق النص اللاتيني ومناطق النص الآسيوي الشرقي في الفقرة الحالية. |
| [setAddSpaceBetweenFarEastAndDigit(boolean value)](#setAddSpaceBetweenFarEastAndDigit-boolean) | يضبط علامة تشير إلى ما إذا كان يتم تعديل التباعد بين الأحرف تلقائيًا بين مناطق الأرقام ومناطق النص الآسيوي الشرقي في الفقرة الحالية. |
| [setAlignment(int value)](#setAlignment-int) | يضبط محاذاة النص للفقرة. |
| [setBaselineAlignment(int value)](#setBaselineAlignment-int) | يضبط الموضع الرأسي للخطوط على السطر. |
| [setBidi(boolean value)](#setBidi-boolean) | يضبط ما إذا كانت هذه الفقرة من اليمين إلى اليسار. |
| [setBorderAttr(int key, Object value)](#setBorderAttr-int-java.lang.Object) |  |
| [setCharacterUnitFirstLineIndent(double value)](#setCharacterUnitFirstLineIndent-double) | يضبط القيمة (بالحروف) للسطر الأول أو الإزاحة المتدلية. |
| [setCharacterUnitLeftIndent(double value)](#setCharacterUnitLeftIndent-double) | يضبط قيمة الإزاحة اليسرى (بالحروف) للفقرات المحددة. |
| [setCharacterUnitRightIndent(double value)](#setCharacterUnitRightIndent-double) | يضبط قيمة الإزاحة اليمنى (بالحروف) للفقرات المحددة. |
| [setDropCapPosition(int value)](#setDropCapPosition-int) | يضبط موضع النص بالحرف الأول الكبير. |
| [setFarEastLineBreakControl(boolean value)](#setFarEastLineBreakControl-boolean) | يضبط علامة تشير إلى ما إذا كانت قواعد كسر السطر الآسيوي الشرقي مطبقة على الفقرة الحالية. |
| [setFirstLineIndent(double value)](#setFirstLineIndent-double) | يضبط القيمة (بالنقاط) للسطر الأول أو الإزاحة المتدلية. |
| [setHangingPunctuation(boolean value)](#setHangingPunctuation-boolean) | يضبط علامة تشير إلى ما إذا كانت علامات الترقيم المتدلية مفعلة للفقرة الحالية. |
| [setKeepTogether(boolean value)](#setKeepTogether-boolean) | صحيح إذا كان يجب أن تبقى جميع الأسطر في الفقرة على نفس الصفحة. |
| [setKeepWithNext(boolean value)](#setKeepWithNext-boolean) | صحيح إذا كان يجب أن تبقى الفقرة على نفس الصفحة مع الفقرة التي تليها. |
| [setLeftIndent(double value)](#setLeftIndent-double) | يضبط القيمة (بالنقاط) التي تمثل الإزاحة اليسرى للفقرة. |
| [setLineSpacing(double value)](#setLineSpacing-double) | يضبط تباعد السطر (بالنقاط) للفقرة. |
| [setLineSpacingRule(int value)](#setLineSpacingRule-int) | يضبط تباعد السطر للفقرة. |
| [setLineUnitAfter(double value)](#setLineUnitAfter-double) | يضبط مقدار التباعد (بخطوط الشبكة) بعد الفقرات. |
| [setLineUnitBefore(double value)](#setLineUnitBefore-double) | يضبط مقدار التباعد (بخطوط الشبكة) قبل الفقرات. |
| [setLinesToDrop(int value)](#setLinesToDrop-int) | يضبط عدد أسطر نص الفقرة المستخدمة لحساب ارتفاع الحرف الأول الكبير. |
| [setMirrorIndents(boolean value)](#setMirrorIndents-boolean) | يضبط علامة تشير إلى ما إذا كانت الإزاحات اليسرى واليمنى ذات عرض متساوٍ. |
| [setNoSpaceBetweenParagraphsOfSameStyle(boolean value)](#setNoSpaceBetweenParagraphsOfSameStyle-boolean) | عند true، سيتم تجاهل [getSpaceBefore()](../../com.aspose.words/paragraphformat/\#getSpaceBefore) / [setSpaceBefore(double)](../../com.aspose.words/paragraphformat/\#setSpaceBefore-double) و [getSpaceAfter()](../../com.aspose.words/paragraphformat/\#getSpaceAfter) / [setSpaceAfter(double)](../../com.aspose.words/paragraphformat/\#setSpaceAfter-double) بين الفقرات ذات النمط نفسه. |
| [setOutlineLevel(int value)](#setOutlineLevel-int) | يحدد مستوى المخطط للفقرة في المستند. |
| [setPageBreakBefore(boolean value)](#setPageBreakBefore-boolean) | صحيح إذا تم فرض فاصل صفحة قبل الفقرة. |
| [setRightIndent(double value)](#setRightIndent-double) | يضبط القيمة (بالنقاط) التي تمثل الإزاحة اليمنى للفقرة. |
| [setSnapToGrid(boolean value)](#setSnapToGrid-boolean) | يحدد ما إذا كان يجب على الفقرة الحالية استخدام إعدادات خطوط شبكة المستند لكل صفحة عند تنسيق المحتوى داخل الفقرة. |
| [setSpaceAfter(double value)](#setSpaceAfter-double) | يضبط مقدار التباعد (بالنقاط) بعد الفقرة. |
| [setSpaceAfterAuto(boolean value)](#setSpaceAfterAuto-boolean) | صحيح إذا تم تعيين مقدار المسافة بعد الفقرة تلقائيًا. |
| [setSpaceBefore(double value)](#setSpaceBefore-double) | يضبط مقدار المسافة (بالنقاط) قبل الفقرة. |
| [setSpaceBeforeAuto(boolean value)](#setSpaceBeforeAuto-boolean) | صحيح إذا تم تعيين مقدار المسافة قبل الفقرة تلقائيًا. |
| [setStyle(Style value)](#setStyle-com.aspose.words.Style) | يضبط نمط الفقرة المطبق على هذا التنسيق. |
| [setStyleIdentifier(int value)](#setStyleIdentifier-int) | يضبط معرف النمط المستقل عن اللغة لنمط الفقرة المطبق على هذا التنسيق. |
| [setStyleName(String value)](#setStyleName-java.lang.String) | يضبط اسم نمط الفقرة المطبق على هذا التنسيق. |
| [setSuppressAutoHyphens(boolean value)](#setSuppressAutoHyphens-boolean) | يحدد ما إذا كان يجب إعفاء الفقرة الحالية من أي تجزئة تُطبق في إعدادات المستند. |
| [setSuppressLineNumbers(boolean value)](#setSuppressLineNumbers-boolean) | يحدد ما إذا كان يجب إعفاء أسطر الفقرة الحالية من ترقيم الأسطر الذي يُطبق في القسم الأب. |
| [setWidowControl(boolean value)](#setWidowControl-boolean) | صحيح إذا كان يجب أن تبقى السطران الأول والأخير في الفقرة على نفس الصفحة مع باقي الفقرة. |
| [setWordWrap(boolean value)](#setWordWrap-boolean) | إذا كانت هذه الخاصية خاطئة، يمكن لف النص اللاتيني في وسط الكلمة للفقرة الحالية. |
### clearFormatting() {#clearFormatting}
```
public void clearFormatting()
```


يعيد تعيين تنسيق الفقرة إلى الإعدادات الافتراضية.

 **Remarks:** 

تنسيق الفقرة الافتراضي هو النمط العادي، محاذاة إلى اليسار، بدون إزاحة، بدون مسافة، بدون حدود وبدون تظليل.

 **Examples:** 

يوضح كيفية تضمين قائمة داخل قائمة أخرى.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // A list allows us to organize and decorate sets of paragraphs with prefix symbols and indents.
 // We can create nested lists by increasing the indent level.
 // We can begin and end a list by using a document builder's "ListFormat" property.
 // Each paragraph that we add between a list's start and the end will become an item in the list.
 // Create an outline list for the headings.
 List outlineList = doc.getLists().add(ListTemplate.OUTLINE_NUMBERS);
 builder.getListFormat().setList(outlineList);
 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_1);
 builder.writeln("This is my Chapter 1");

 // Create a numbered list.
 List numberedList = doc.getLists().add(ListTemplate.NUMBER_DEFAULT);
 builder.getListFormat().setList(numberedList);
 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.NORMAL);
 builder.writeln("Numbered list item 1.");

 // Every paragraph that comprises a list will have this flag.
 Assert.assertTrue(builder.getCurrentParagraph().isListItem());
 Assert.assertTrue(builder.getParagraphFormat().isListItem());

 // Create a bulleted list.
 List bulletedList = doc.getLists().add(ListTemplate.BULLET_DEFAULT);
 builder.getListFormat().setList(bulletedList);
 builder.getParagraphFormat().setLeftIndent(72.0);
 builder.writeln("Bulleted list item 1.");
 builder.writeln("Bulleted list item 2.");
 builder.getParagraphFormat().clearFormatting();

 // Revert to the numbered list.
 builder.getListFormat().setList(numberedList);
 builder.writeln("Numbered list item 2.");
 builder.writeln("Numbered list item 3.");

 // Revert to the outline list.
 builder.getListFormat().setList(outlineList);
 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_1);
 builder.writeln("This is my Chapter 2");

 builder.getParagraphFormat().clearFormatting();

 builder.getDocument().save(getArtifactsDir() + "Lists.NestedLists.docx");
 
```

### fetchInheritedBorderAttr(int key) {#fetchInheritedBorderAttr-int}
```
public Object fetchInheritedBorderAttr(int key)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### fetchInheritedShadingAttr(int key) {#fetchInheritedShadingAttr-int}
```
public Object fetchInheritedShadingAttr(int key)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### getAddSpaceBetweenFarEastAndAlpha() {#getAddSpaceBetweenFarEastAndAlpha}
```
public boolean getAddSpaceBetweenFarEastAndAlpha()
```


يحصل على علم يوضح ما إذا كان يتم تعديل التباعد بين الأحرف تلقائيًا بين مناطق النص اللاتيني ومناطق النص الآسيوي الشرقي في الفقرة الحالية.

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
منطقي - علامة تشير إلى ما إذا كان تعديل المسافة بين الأحرف يتم تلقائيًا بين مناطق النص اللاتيني ومناطق النص شرق آسيوي في الفقرة الحالية.
### getAddSpaceBetweenFarEastAndDigit() {#getAddSpaceBetweenFarEastAndDigit}
```
public boolean getAddSpaceBetweenFarEastAndDigit()
```


يحصل على علم يوضح ما إذا كان يتم تعديل التباعد بين الأحرف تلقائيًا بين مناطق الأرقام ومناطق النص الآسيوي الشرقي في الفقرة الحالية.

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
منطقي - علامة تشير إلى ما إذا كان تعديل المسافة بين الأحرف يتم تلقائيًا بين مناطق الأرقام ومناطق النص شرق آسيوي في الفقرة الحالية.
### getAlignment() {#getAlignment}
```
public int getAlignment()
```


يحصل على محاذاة النص للفقرة.

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

يوضح كيفية إنشاء مستند Aspose.Words يدوياً.

```

 Document doc = new Document();

 // A blank document contains one section, one body and one paragraph.
 // Call the "RemoveAllChildren" method to remove all those nodes,
 // and end up with a document node with no children.
 doc.removeAllChildren();

 // This document now has no composite child nodes that we can add content to.
 // If we wish to edit it, we will need to repopulate its node collection.
 // First, create a new section, and then append it as a child to the root document node.
 Section section = new Section(doc);
 doc.appendChild(section);

 // Set some page setup properties for the section.
 section.getPageSetup().setSectionStart(SectionStart.NEW_PAGE);
 section.getPageSetup().setPaperSize(PaperSize.LETTER);

 // A section needs a body, which will contain and display all its contents
 // on the page between the section's header and footer.
 Body body = new Body(doc);
 section.appendChild(body);

 // Create a paragraph, set some formatting properties, and then append it as a child to the body.
 Paragraph para = new Paragraph(doc);

 para.getParagraphFormat().setStyleName("Heading 1");
 para.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);

 body.appendChild(para);

 // Finally, add some content to do the document. Create a run,
 // set its appearance and contents, and then append it as a child to the paragraph.
 Run run = new Run(doc);
 run.setText("Hello World!");
 run.getFont().setColor(Color.RED);
 para.appendChild(run);

 Assert.assertEquals("Hello World!", doc.getText().trim());

 doc.save(getArtifactsDir() + "Section.CreateManually.docx");
 
```

**Returns:**
عدد صحيح - محاذاة النص للفقرة. القيمة المرجعة هي واحدة من ثوابت [ParagraphAlignment](../../com.aspose.words/paragraphalignment/).
### getBaselineAlignment() {#getBaselineAlignment}
```
public int getBaselineAlignment()
```


يحصل على الموضع العمودي للخطوط على السطر.

 **Examples:** 

يظهر كيفية ضبط الموضع العمودي للخطوط على سطر.

```

 Document doc = new Document(getMyDir() + "Office math.docx");

 ParagraphFormat format = doc.getFirstSection().getBody().getParagraphs().get(0).getParagraphFormat();
 if (format.getBaselineAlignment() == BaselineAlignment.AUTO)
 {
     format.setBaselineAlignment(BaselineAlignment.TOP);
 }

 doc.save(getArtifactsDir() + "ParagraphFormat.ParagraphBaselineAlignment.docx");
 
```

**Returns:**
عدد صحيح - الموضع العمودي للخطوط على السطر. القيمة المرجعة هي واحدة من ثوابت [BaselineAlignment](../../com.aspose.words/baselinealignment/).
### getBidi() {#getBidi}
```
public boolean getBidi()
```


يحصل على ما إذا كانت هذه الفقرة من اليمين إلى اليسار.

 **Remarks:** 

عند true، يتم ترتيب المقاطع والكائنات المضمنة الأخرى في هذه الفقرة من اليمين إلى اليسار.

 **Examples:** 

يوضح كيفية إنشاء قوائم متوافقة مع اللغات من اليمين إلى اليسار باستخدام حقول BIDIOUTLINE.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // The BIDIOUTLINE field numbers paragraphs like the AUTONUM/LISTNUM fields,
 // but is only visible when a right-to-left editing language is enabled, such as Hebrew or Arabic.
 // The following field will display ".1", the RTL equivalent of list number "1.".
 FieldBidiOutline field = (FieldBidiOutline) builder.insertField(FieldType.FIELD_BIDI_OUTLINE, true);
 builder.writeln("\u05e9\u05dc\u05d5\u05dd");

 Assert.assertEquals(" BIDIOUTLINE ", field.getFieldCode());

 // Add two more BIDIOUTLINE fields, which will display ".2" and ".3".
 builder.insertField(FieldType.FIELD_BIDI_OUTLINE, true);
 builder.writeln("\u05e9\u05dc\u05d5\u05dd");
 builder.insertField(FieldType.FIELD_BIDI_OUTLINE, true);
 builder.writeln("\u05e9\u05dc\u05d5\u05dd");

 // Set the horizontal text alignment for every paragraph in the document to RTL.
 for (Paragraph para : (Iterable) doc.getChildNodes(NodeType.PARAGRAPH, true)) {
     para.getParagraphFormat().setBidi(true);
 }

 // If we enable a right-to-left editing language in Microsoft Word, our fields will display numbers.
 // Otherwise, they will display "###".
 doc.save(getArtifactsDir() + "Field.BIDIOUTLINE.docx");
 
```

يوضح كيفية اكتشاف اتجاه نص المستند النصي العادي.

```

 // Create a "TxtLoadOptions" object, which we can pass to a document's constructor
 // to modify how we load a plaintext document.
 TxtLoadOptions loadOptions = new TxtLoadOptions();

 // Set the "DocumentDirection" property to "DocumentDirection.Auto" automatically detects
 // the direction of every paragraph of text that Aspose.Words loads from plaintext.
 // Each paragraph's "Bidi" property will store its direction.
 loadOptions.setDocumentDirection(DocumentDirection.AUTO);

 // Detect Hebrew text as right-to-left.
 Document doc = new Document(getMyDir() + "Hebrew text.txt", loadOptions);

 Assert.assertTrue(doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat().getBidi());

 // Detect English text as right-to-left.
 doc = new Document(getMyDir() + "English text.txt", loadOptions);

 Assert.assertFalse(doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat().getBidi());
 
```

**Returns:**
منطقي - ما إذا كانت هذه الفقرة من اليمين إلى اليسار.
### getBorders() {#getBorders}
```
public BorderCollection getBorders()
```


يحصل على مجموعة حدود الفقرة.

 **Examples:** 

يظهر كيفية إدراج فقرة بحد أعلى.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Border topBorder = builder.getParagraphFormat().getBorders().getByBorderType(BorderType.TOP);
 topBorder.setLineWidth(4.0d);
 topBorder.setLineStyle(LineStyle.DASH_SMALL_GAP);
 // Set ThemeColor only when LineWidth or LineStyle setted.
 topBorder.setThemeColor(ThemeColor.ACCENT_1);
 topBorder.setTintAndShade(0.25d);

 builder.writeln("Text with a top border.");

 doc.save(getArtifactsDir() + "Border.ParagraphTopBorder.docx");
 
```

**Returns:**
[BorderCollection](../../com.aspose.words/bordercollection/) - Collection of borders of the paragraph.
### getCharacterUnitFirstLineIndent() {#getCharacterUnitFirstLineIndent}
```
public double getCharacterUnitFirstLineIndent()
```


يحصل على القيمة (بالحروف) للمسافة البادئة للسطر الأول أو المعلقة.

استخدم القيم الموجبة لضبط إزاحة السطر الأول، والقيم السالبة لضبط الإزاحة المتدلية.

 **Examples:** 

يظهر كيفية تغيير مسافات الفقرة والإزاحات.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 ParagraphFormat format = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat();

 // Below are five different spacing options, along with the properties that their configuration indirectly affects.
 // 1 -  Left indent:
 Assert.assertEquals(format.getLeftIndent(), 0.0d);

 format.setCharacterUnitLeftIndent(10.0);

 Assert.assertEquals(format.getLeftIndent(), 120.0d);

 // 2 -  Right indent:
 Assert.assertEquals(format.getRightIndent(), 0.0d);

 format.setCharacterUnitRightIndent(-5.5);

 Assert.assertEquals(format.getRightIndent(), -66.0d);

 // 3 -  Hanging indent:
 Assert.assertEquals(format.getFirstLineIndent(), 0.0d);

 format.setCharacterUnitFirstLineIndent(20.3);

 Assert.assertEquals(format.getFirstLineIndent(), 243.59d, 0.1d);

 // 4 -  Line spacing before paragraphs:
 Assert.assertEquals(format.getSpaceBefore(), 0.0d);

 format.setLineUnitBefore(5.1);

 Assert.assertEquals(format.getSpaceBefore(), 61.1d, 0.1d);

 // 5 -  Line spacing after paragraphs:
 Assert.assertEquals(format.getSpaceAfter(), 0.0d);

 format.setLineUnitAfter(10.9);

 Assert.assertEquals(format.getSpaceAfter(), 130.8d, 0.1d);

 builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
         "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
 builder.write("\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5" +
         "\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863");
 
```

**Returns:**
عدد مزدوج - القيمة (بالحروف) للإزاحة الأولى أو المتدلية.
### getCharacterUnitLeftIndent() {#getCharacterUnitLeftIndent}
```
public double getCharacterUnitLeftIndent()
```


يحصل على قيمة المسافة البادئة اليسرى (بالحروف) للفقرات المحددة.

 **Examples:** 

يظهر كيفية تغيير مسافات الفقرة والإزاحات.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 ParagraphFormat format = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat();

 // Below are five different spacing options, along with the properties that their configuration indirectly affects.
 // 1 -  Left indent:
 Assert.assertEquals(format.getLeftIndent(), 0.0d);

 format.setCharacterUnitLeftIndent(10.0);

 Assert.assertEquals(format.getLeftIndent(), 120.0d);

 // 2 -  Right indent:
 Assert.assertEquals(format.getRightIndent(), 0.0d);

 format.setCharacterUnitRightIndent(-5.5);

 Assert.assertEquals(format.getRightIndent(), -66.0d);

 // 3 -  Hanging indent:
 Assert.assertEquals(format.getFirstLineIndent(), 0.0d);

 format.setCharacterUnitFirstLineIndent(20.3);

 Assert.assertEquals(format.getFirstLineIndent(), 243.59d, 0.1d);

 // 4 -  Line spacing before paragraphs:
 Assert.assertEquals(format.getSpaceBefore(), 0.0d);

 format.setLineUnitBefore(5.1);

 Assert.assertEquals(format.getSpaceBefore(), 61.1d, 0.1d);

 // 5 -  Line spacing after paragraphs:
 Assert.assertEquals(format.getSpaceAfter(), 0.0d);

 format.setLineUnitAfter(10.9);

 Assert.assertEquals(format.getSpaceAfter(), 130.8d, 0.1d);

 builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
         "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
 builder.write("\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5" +
         "\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863");
 
```

**Returns:**
عدد مزدوج - قيمة الإزاحة اليسرى (بالحروف) للفقرات المحددة.
### getCharacterUnitRightIndent() {#getCharacterUnitRightIndent}
```
public double getCharacterUnitRightIndent()
```


يحصل على قيمة المسافة البادئة اليمنى (بالحروف) للفقرات المحددة.

 **Examples:** 

يظهر كيفية تغيير مسافات الفقرة والإزاحات.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 ParagraphFormat format = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat();

 // Below are five different spacing options, along with the properties that their configuration indirectly affects.
 // 1 -  Left indent:
 Assert.assertEquals(format.getLeftIndent(), 0.0d);

 format.setCharacterUnitLeftIndent(10.0);

 Assert.assertEquals(format.getLeftIndent(), 120.0d);

 // 2 -  Right indent:
 Assert.assertEquals(format.getRightIndent(), 0.0d);

 format.setCharacterUnitRightIndent(-5.5);

 Assert.assertEquals(format.getRightIndent(), -66.0d);

 // 3 -  Hanging indent:
 Assert.assertEquals(format.getFirstLineIndent(), 0.0d);

 format.setCharacterUnitFirstLineIndent(20.3);

 Assert.assertEquals(format.getFirstLineIndent(), 243.59d, 0.1d);

 // 4 -  Line spacing before paragraphs:
 Assert.assertEquals(format.getSpaceBefore(), 0.0d);

 format.setLineUnitBefore(5.1);

 Assert.assertEquals(format.getSpaceBefore(), 61.1d, 0.1d);

 // 5 -  Line spacing after paragraphs:
 Assert.assertEquals(format.getSpaceAfter(), 0.0d);

 format.setLineUnitAfter(10.9);

 Assert.assertEquals(format.getSpaceAfter(), 130.8d, 0.1d);

 builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
         "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
 builder.write("\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5" +
         "\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863");
 
```

**Returns:**
عدد مزدوج - قيمة الإزاحة اليمنى (بالحروف) للفقرات المحددة.
### getDirectBorderAttr(int key) {#getDirectBorderAttr-int}
```
public Object getDirectBorderAttr(int key)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### getDropCapPosition() {#getDropCapPosition}
```
public int getDropCapPosition()
```


يحصل على موضع النص المتدلي (drop cap).

 **Examples:** 

يوضح كيفية تضمين قائمة داخل قائمة أخرى.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // A list allows us to organize and decorate sets of paragraphs with prefix symbols and indents.
 // We can create nested lists by increasing the indent level.
 // We can begin and end a list by using a document builder's "ListFormat" property.
 // Each paragraph that we add between a list's start and the end will become an item in the list.
 // Create an outline list for the headings.
 List outlineList = doc.getLists().add(ListTemplate.OUTLINE_NUMBERS);
 builder.getListFormat().setList(outlineList);
 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_1);
 builder.writeln("This is my Chapter 1");

 // Create a numbered list.
 List numberedList = doc.getLists().add(ListTemplate.NUMBER_DEFAULT);
 builder.getListFormat().setList(numberedList);
 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.NORMAL);
 builder.writeln("Numbered list item 1.");

 // Every paragraph that comprises a list will have this flag.
 Assert.assertTrue(builder.getCurrentParagraph().isListItem());
 Assert.assertTrue(builder.getParagraphFormat().isListItem());

 // Create a bulleted list.
 List bulletedList = doc.getLists().add(ListTemplate.BULLET_DEFAULT);
 builder.getListFormat().setList(bulletedList);
 builder.getParagraphFormat().setLeftIndent(72.0);
 builder.writeln("Bulleted list item 1.");
 builder.writeln("Bulleted list item 2.");
 builder.getParagraphFormat().clearFormatting();

 // Revert to the numbered list.
 builder.getListFormat().setList(numberedList);
 builder.writeln("Numbered list item 2.");
 builder.writeln("Numbered list item 3.");

 // Revert to the outline list.
 builder.getListFormat().setList(outlineList);
 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_1);
 builder.writeln("This is my Chapter 2");

 builder.getParagraphFormat().clearFormatting();

 builder.getDocument().save(getArtifactsDir() + "Lists.NestedLists.docx");
 
```

**Returns:**
عدد صحيح - موضع نص الحرف الأول الكبير. القيمة المرجعة هي واحدة من ثوابت [DropCapPosition](../../com.aspose.words/dropcapposition/).
### getFarEastLineBreakControl() {#getFarEastLineBreakControl}
```
public boolean getFarEastLineBreakControl()
```


يحصل على علم يوضح ما إذا كانت قواعد كسر السطر الآسيوي الشرقي مطبقة على الفقرة الحالية.

 **Examples:** 

يظهر كيفية ضبط خصائص خاصة للطباعة الآسيوية.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 ParagraphFormat format = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat();
 format.setFarEastLineBreakControl(true);
 format.setWordWrap(false);
 format.setHangingPunctuation(true);

 doc.save(getArtifactsDir() + "ParagraphFormat.AsianTypographyProperties.docx");
 
```

**Returns:**
منطقي - علامة تشير إلى ما إذا كانت قواعد كسر السطر شرق آسيوي مطبقة على الفقرة الحالية.
### getFirstLineIndent() {#getFirstLineIndent}
```
public double getFirstLineIndent()
```


يحصل على القيمة (بالنقاط) للمسافة البادئة للسطر الأول أو المعلقة.

استخدم القيم الموجبة لضبط إزاحة السطر الأول، والقيم السالبة لضبط الإزاحة المتدلية.

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
عدد مزدوج - القيمة (بالنقاط) للإزاحة الأولى أو المتدلية.
### getHangingPunctuation() {#getHangingPunctuation}
```
public boolean getHangingPunctuation()
```


يحصل على علم يوضح ما إذا كانت علامات الترقيم المعلقة مفعلة للفقرة الحالية.

 **Examples:** 

يظهر كيفية ضبط خصائص خاصة للطباعة الآسيوية.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 ParagraphFormat format = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat();
 format.setFarEastLineBreakControl(true);
 format.setWordWrap(false);
 format.setHangingPunctuation(true);

 doc.save(getArtifactsDir() + "ParagraphFormat.AsianTypographyProperties.docx");
 
```

**Returns:**
منطقي - علامة تشير إلى ما إذا كانت علامات الترقيم المتدلية مفعلة للفقرة الحالية.
### getKeepTogether() {#getKeepTogether}
```
public boolean getKeepTogether()
```


صحيح إذا كان يجب أن تبقى جميع الأسطر في الفقرة على نفس الصفحة.

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
boolean - القيمة المنطقية المقابلة.
### getKeepWithNext() {#getKeepWithNext}
```
public boolean getKeepWithNext()
```


صحيح إذا كان يجب أن تبقى الفقرة على نفس الصفحة مع الفقرة التي تليها.

 **Examples:** 

يوضح كيفية ضبط جدول للبقاء معًا في نفس الصفحة.

```

 Document doc = new Document(getMyDir() + "Table spanning two pages.docx");
 Table table = doc.getFirstSection().getBody().getTables().get(0);

 // Enabling KeepWithNext for every paragraph in the table except for the
 // last ones in the last row will prevent the table from splitting across multiple pages.
 for (Cell cell : (Iterable) table.getChildNodes(NodeType.CELL, true))
     for (Paragraph para : cell.getParagraphs()) {
         Assert.assertTrue(para.isInCell());

         if (!(cell.getParentRow().isLastRow() && para.isEndOfCell()))
             para.getParagraphFormat().setKeepWithNext(true);
     }

 doc.save(getArtifactsDir() + "Table.KeepTableTogether.docx");
 
```

**Returns:**
boolean - القيمة المنطقية المقابلة.
### getLeftIndent() {#getLeftIndent}
```
public double getLeftIndent()
```


يحصل على القيمة (بالنقاط) التي تمثل المسافة البادئة اليسرى للفقرة.

 **Examples:** 

يظهر كيفية تكوين تنسيق الفقرة لإنشاء نص غير مركزي.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Center all text that the document builder writes, and set up indents.
 // The indent configuration below will create a body of text that will sit asymmetrically on the page.
 // The "center" that we align the text to will be the middle of the body of text, not the middle of the page.
 ParagraphFormat paragraphFormat = builder.getParagraphFormat();
 paragraphFormat.setAlignment(ParagraphAlignment.CENTER);
 paragraphFormat.setLeftIndent(100.0);
 paragraphFormat.setRightIndent(50.0);
 paragraphFormat.setSpaceAfter(25.0);

 builder.writeln(
         "This paragraph demonstrates how left and right indentation affects word wrapping.");
 builder.writeln(
         "The space between the above paragraph and this one depends on the DocumentBuilder's paragraph format.");

 doc.save(getArtifactsDir() + "DocumentBuilder.SetParagraphFormatting.docx");
 
```

**Returns:**
عدد مزدوج - القيمة (بالنقاط) التي تمثل الإزاحة اليسرى للفقرة.
### getLineSpacing() {#getLineSpacing}
```
public double getLineSpacing()
```


يحصل على تباعد السطر (بالنقاط) للفقرة.

 **Remarks:** 

عند ضبط خاصية [getLineSpacingRule()](../../com.aspose.words/paragraphformat/\#getLineSpacingRule) / [setLineSpacingRule(int)](../../com.aspose.words/paragraphformat/\#setLineSpacingRule-int) إلى [LineSpacingRule.AT\_LEAST](../../com.aspose.words/linespacingrule/\#AT-LEAST)، يمكن أن تكون مسافة السطر أكبر من أو مساوية، ولكن لا تكون أبداً أقل من القيمة المحددة لـ [getLineSpacing()](../../com.aspose.words/paragraphformat/\#getLineSpacing) / [setLineSpacing(double)](../../com.aspose.words/paragraphformat/\#setLineSpacing-double).

عند ضبط خاصية [getLineSpacingRule()](../../com.aspose.words/paragraphformat/\#getLineSpacingRule) / [setLineSpacingRule(int)](../../com.aspose.words/paragraphformat/\#setLineSpacingRule-int) إلى [LineSpacingRule.EXACTLY](../../com.aspose.words/linespacingrule/\#EXACTLY)، لا تتغير مسافة السطر أبداً عن القيمة المحددة لـ [getLineSpacing()](../../com.aspose.words/paragraphformat/\#getLineSpacing) / [setLineSpacing(double)](../../com.aspose.words/paragraphformat/\#setLineSpacing-double)، حتى إذا تم استخدام خط أكبر داخل الفقرة.

 **Examples:** 

يظهر كيفية التعامل مع تباعد الأسطر.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Below are three line spacing rules that we can define using the
 // paragraph's "LineSpacingRule" property to configure spacing between paragraphs.
 // 1 -  Set a minimum amount of spacing.
 // This will give vertical padding to lines of text of any size
 // that is too small to maintain the minimum line-height.
 builder.getParagraphFormat().setLineSpacingRule(LineSpacingRule.AT_LEAST);
 builder.getParagraphFormat().setLineSpacing(20.0);

 builder.writeln("Minimum line spacing of 20.");
 builder.writeln("Minimum line spacing of 20.");

 // 2 -  Set exact spacing.
 // Using font sizes that are too large for the spacing will truncate the text.
 builder.getParagraphFormat().setLineSpacingRule(LineSpacingRule.EXACTLY);
 builder.getParagraphFormat().setLineSpacing(5.0);

 builder.writeln("Line spacing of exactly 5.");
 builder.writeln("Line spacing of exactly 5.");

 // 3 -  Set spacing as a multiple of default line spacing, which is 12 points by default.
 // This kind of spacing will scale to different font sizes.
 builder.getParagraphFormat().setLineSpacingRule(LineSpacingRule.MULTIPLE);
 builder.getParagraphFormat().setLineSpacing(18.0);

 builder.writeln("Line spacing of 1.5 default lines.");
 builder.writeln("Line spacing of 1.5 default lines.");

 doc.save(getArtifactsDir() + "ParagraphFormat.LineSpacing.docx");
 
```

**Returns:**
double - تباعد السطر (بالنقاط) للفقرة.
### getLineSpacingRule() {#getLineSpacingRule}
```
public int getLineSpacingRule()
```


يحصل على تباعد السطر للفقرة.

 **Examples:** 

يظهر كيفية التعامل مع تباعد الأسطر.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Below are three line spacing rules that we can define using the
 // paragraph's "LineSpacingRule" property to configure spacing between paragraphs.
 // 1 -  Set a minimum amount of spacing.
 // This will give vertical padding to lines of text of any size
 // that is too small to maintain the minimum line-height.
 builder.getParagraphFormat().setLineSpacingRule(LineSpacingRule.AT_LEAST);
 builder.getParagraphFormat().setLineSpacing(20.0);

 builder.writeln("Minimum line spacing of 20.");
 builder.writeln("Minimum line spacing of 20.");

 // 2 -  Set exact spacing.
 // Using font sizes that are too large for the spacing will truncate the text.
 builder.getParagraphFormat().setLineSpacingRule(LineSpacingRule.EXACTLY);
 builder.getParagraphFormat().setLineSpacing(5.0);

 builder.writeln("Line spacing of exactly 5.");
 builder.writeln("Line spacing of exactly 5.");

 // 3 -  Set spacing as a multiple of default line spacing, which is 12 points by default.
 // This kind of spacing will scale to different font sizes.
 builder.getParagraphFormat().setLineSpacingRule(LineSpacingRule.MULTIPLE);
 builder.getParagraphFormat().setLineSpacing(18.0);

 builder.writeln("Line spacing of 1.5 default lines.");
 builder.writeln("Line spacing of 1.5 default lines.");

 doc.save(getArtifactsDir() + "ParagraphFormat.LineSpacing.docx");
 
```

**Returns:**
int - تباعد السطر للفقرة. القيمة المرجعة هي واحدة من ثوابت [LineSpacingRule](../../com.aspose.words/linespacingrule/).
### getLineUnitAfter() {#getLineUnitAfter}
```
public double getLineUnitAfter()
```


يحصل على مقدار المسافة (بالخطوط الشبكية) بعد الفقرات.

 **Examples:** 

يظهر كيفية تغيير مسافات الفقرة والإزاحات.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 ParagraphFormat format = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat();

 // Below are five different spacing options, along with the properties that their configuration indirectly affects.
 // 1 -  Left indent:
 Assert.assertEquals(format.getLeftIndent(), 0.0d);

 format.setCharacterUnitLeftIndent(10.0);

 Assert.assertEquals(format.getLeftIndent(), 120.0d);

 // 2 -  Right indent:
 Assert.assertEquals(format.getRightIndent(), 0.0d);

 format.setCharacterUnitRightIndent(-5.5);

 Assert.assertEquals(format.getRightIndent(), -66.0d);

 // 3 -  Hanging indent:
 Assert.assertEquals(format.getFirstLineIndent(), 0.0d);

 format.setCharacterUnitFirstLineIndent(20.3);

 Assert.assertEquals(format.getFirstLineIndent(), 243.59d, 0.1d);

 // 4 -  Line spacing before paragraphs:
 Assert.assertEquals(format.getSpaceBefore(), 0.0d);

 format.setLineUnitBefore(5.1);

 Assert.assertEquals(format.getSpaceBefore(), 61.1d, 0.1d);

 // 5 -  Line spacing after paragraphs:
 Assert.assertEquals(format.getSpaceAfter(), 0.0d);

 format.setLineUnitAfter(10.9);

 Assert.assertEquals(format.getSpaceAfter(), 130.8d, 0.1d);

 builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
         "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
 builder.write("\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5" +
         "\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863");
 
```

**Returns:**
double - مقدار التباعد (بخطوط الشبكة) بعد الفقرات.
### getLineUnitBefore() {#getLineUnitBefore}
```
public double getLineUnitBefore()
```


يحصل على مقدار المسافة (بالخطوط الشبكية) قبل الفقرات.

 **Examples:** 

يظهر كيفية تغيير مسافات الفقرة والإزاحات.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 ParagraphFormat format = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat();

 // Below are five different spacing options, along with the properties that their configuration indirectly affects.
 // 1 -  Left indent:
 Assert.assertEquals(format.getLeftIndent(), 0.0d);

 format.setCharacterUnitLeftIndent(10.0);

 Assert.assertEquals(format.getLeftIndent(), 120.0d);

 // 2 -  Right indent:
 Assert.assertEquals(format.getRightIndent(), 0.0d);

 format.setCharacterUnitRightIndent(-5.5);

 Assert.assertEquals(format.getRightIndent(), -66.0d);

 // 3 -  Hanging indent:
 Assert.assertEquals(format.getFirstLineIndent(), 0.0d);

 format.setCharacterUnitFirstLineIndent(20.3);

 Assert.assertEquals(format.getFirstLineIndent(), 243.59d, 0.1d);

 // 4 -  Line spacing before paragraphs:
 Assert.assertEquals(format.getSpaceBefore(), 0.0d);

 format.setLineUnitBefore(5.1);

 Assert.assertEquals(format.getSpaceBefore(), 61.1d, 0.1d);

 // 5 -  Line spacing after paragraphs:
 Assert.assertEquals(format.getSpaceAfter(), 0.0d);

 format.setLineUnitAfter(10.9);

 Assert.assertEquals(format.getSpaceAfter(), 130.8d, 0.1d);

 builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
         "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
 builder.write("\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5" +
         "\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863");
 
```

**Returns:**
double - مقدار التباعد (بخطوط الشبكة) قبل الفقرات.
### getLinesToDrop() {#getLinesToDrop}
```
public int getLinesToDrop()
```


يحصل على عدد أسطر نص الفقرة المستخدمة لحساب ارتفاع الحرف الأول الكبير.

 **Examples:** 

يظهر كيفية ضبط حجم الحرف الأول الكبير.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Modify the "LinesToDrop" property to designate a paragraph as a drop cap,
 // which will turn it into a large capital letter that will decorate the next paragraph.
 // Give this property a value of 4 to give the drop cap the height of four text lines.
 builder.getParagraphFormat().setLinesToDrop(4);
 builder.writeln("H");

 // Reset the "LinesToDrop" property to 0 to turn the next paragraph into an ordinary paragraph.
 // The text in this paragraph will wrap around the drop cap.
 builder.getParagraphFormat().setLinesToDrop(0);
 builder.writeln("ello world!");

 doc.save(getArtifactsDir() + "ParagraphFormat.LinesToDrop.odt");
 
```

**Returns:**
int - عدد الأسطر من نص الفقرة المستخدمة لحساب ارتفاع الحرف الأول الكبير.
### getMirrorIndents() {#getMirrorIndents}
```
public boolean getMirrorIndents()
```


يحصل على علم يشير إلى ما إذا كانت المسافات البادئة اليسرى واليمنى ذات عرض متساوٍ.

 **Examples:** 

يظهر كيفية جعل الهوامش اليسرى واليمنى متساوية.

```

 Document doc = new Document(getMyDir() + "Document.docx");
 ParagraphFormat format = doc.getFirstSection().getBody().getParagraphs().get(0).getParagraphFormat();

 format.setMirrorIndents(true);

 doc.save(getArtifactsDir() + "ParagraphFormat.MirrorIndents.docx");
 
```

**Returns:**
boolean - علم يشير إلى ما إذا كانت الهوامش اليسرى واليمنى ذات عرض متساوٍ.
### getNoSpaceBetweenParagraphsOfSameStyle() {#getNoSpaceBetweenParagraphsOfSameStyle}
```
public boolean getNoSpaceBetweenParagraphsOfSameStyle()
```


عند true، سيتم تجاهل [getSpaceBefore()](../../com.aspose.words/paragraphformat/\#getSpaceBefore) / [setSpaceBefore(double)](../../com.aspose.words/paragraphformat/\#setSpaceBefore-double) و [getSpaceAfter()](../../com.aspose.words/paragraphformat/\#getSpaceAfter) / [setSpaceAfter(double)](../../com.aspose.words/paragraphformat/\#setSpaceAfter-double) بين الفقرات ذات النمط نفسه.

 **Remarks:** 

هذا الإعداد لا يؤثر إلا عندما يُطبق على نمط فقرة. إذا تم تطبيقه مباشرة على فقرة، فلن يكون له أي تأثير.

 **Examples:** 

يظهر كيفية تطبيق عدم وجود تباعد بين الفقرات ذات النمط نفسه.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Apply a large amount of spacing before and after paragraphs that this builder will create.
 builder.getParagraphFormat().setSpaceBefore(24.0);
 builder.getParagraphFormat().setSpaceAfter(24.0);

 // Set the "NoSpaceBetweenParagraphsOfSameStyle" flag to "true" to apply
 // no spacing between paragraphs with the same style, which will group similar paragraphs.
 // Leave the "NoSpaceBetweenParagraphsOfSameStyle" flag as "false"
 // to evenly apply spacing to every paragraph.
 builder.getParagraphFormat().setNoSpaceBetweenParagraphsOfSameStyle(noSpaceBetweenParagraphsOfSameStyle);

 builder.getParagraphFormat().setStyle(doc.getStyles().get("Normal"));
 builder.writeln(MessageFormat.format("Paragraph in the \"{0}\" style.", builder.getParagraphFormat().getStyle().getName()));
 builder.writeln(MessageFormat.format("Paragraph in the \"{0}\" style.", builder.getParagraphFormat().getStyle().getName()));
 builder.writeln(MessageFormat.format("Paragraph in the \"{0}\" style.", builder.getParagraphFormat().getStyle().getName()));
 builder.getParagraphFormat().setStyle(doc.getStyles().get("Quote"));
 builder.writeln(MessageFormat.format("Paragraph in the \"{0}\" style.", builder.getParagraphFormat().getStyle().getName()));
 builder.writeln(MessageFormat.format("Paragraph in the \"{0}\" style.", builder.getParagraphFormat().getStyle().getName()));
 builder.getParagraphFormat().setStyle(doc.getStyles().get("Normal"));
 builder.writeln(MessageFormat.format("Paragraph in the \"{0}\" style.", builder.getParagraphFormat().getStyle().getName()));
 builder.writeln(MessageFormat.format("Paragraph in the \"{0}\" style.", builder.getParagraphFormat().getStyle().getName()));

 doc.save(getArtifactsDir() + "ParagraphFormat.ParagraphSpacingSameStyle.docx");
 
```

**Returns:**
boolean - القيمة المنطقية المقابلة.
### getOutlineLevel() {#getOutlineLevel}
```
public int getOutlineLevel()
```


يحدد مستوى المخطط للفقرة في المستند.

 **Examples:** 

يوضح كيفية تكوين مستويات مخطط الفقرات لإنشاء نص قابل للطي.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Each paragraph has an OutlineLevel, which could be any number from 1 to 9, or at the default "BodyText" value.
 // Setting the property to one of the numbered values will show an arrow to the left
 // of the beginning of the paragraph.
 builder.getParagraphFormat().setOutlineLevel(OutlineLevel.LEVEL_1);
 builder.writeln("Paragraph outline level 1.");

 // Level 1 is the topmost level. If there is a paragraph with a lower level below a paragraph with a higher level,
 // collapsing the higher-level paragraph will collapse the lower level paragraph.
 builder.getParagraphFormat().setOutlineLevel(OutlineLevel.LEVEL_2);
 builder.writeln("Paragraph outline level 2.");

 // Two paragraphs of the same level will not collapse each other,
 // and the arrows do not collapse the paragraphs they point to.
 builder.getParagraphFormat().setOutlineLevel(OutlineLevel.LEVEL_3);
 builder.writeln("Paragraph outline level 3.");
 builder.writeln("Paragraph outline level 3.");

 // The default "BodyText" value is the lowest, which a paragraph of any level can collapse.
 builder.getParagraphFormat().setOutlineLevel(OutlineLevel.BODY_TEXT);
 builder.writeln("Paragraph at main text level.");

 doc.save(getArtifactsDir() + "ParagraphFormat.ParagraphOutlineLevel.docx");
 
```

**Returns:**
int - القيمة الصحيحة المقابلة. القيمة المرجعة هي واحدة من ثوابت [OutlineLevel](../../com.aspose.words/outlinelevel/).
### getPageBreakBefore() {#getPageBreakBefore}
```
public boolean getPageBreakBefore()
```


صحيح إذا تم فرض فاصل صفحة قبل الفقرة.

 **Examples:** 

يظهر كيفية إنشاء فقرات مع فواصل صفحات في البداية.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Set this flag to "true" to apply a page break to each paragraph's beginning
 // that the document builder will create under this ParagraphFormat configuration.
 // The first paragraph will not receive a page break.
 // Leave this flag as "false" to start each new paragraph on the same page
 // as the previous, provided there is sufficient space.
 builder.getParagraphFormat().setPageBreakBefore(pageBreakBefore);

 builder.writeln("Paragraph 1.");
 builder.writeln("Paragraph 2.");

 LayoutCollector layoutCollector = new LayoutCollector(doc);
 ParagraphCollection paragraphs = doc.getFirstSection().getBody().getParagraphs();

 if (pageBreakBefore) {
     Assert.assertEquals(1, layoutCollector.getStartPageIndex(paragraphs.get(0)));
     Assert.assertEquals(2, layoutCollector.getStartPageIndex(paragraphs.get(1)));
 } else {
     Assert.assertEquals(1, layoutCollector.getStartPageIndex(paragraphs.get(0)));
     Assert.assertEquals(1, layoutCollector.getStartPageIndex(paragraphs.get(1)));
 }

 doc.save(getArtifactsDir() + "ParagraphFormat.PageBreakBefore.docx");
 
```

**Returns:**
boolean - القيمة المنطقية المقابلة.
### getRightIndent() {#getRightIndent}
```
public double getRightIndent()
```


يحصل على القيمة (بالنقاط) التي تمثل المسافة البادئة اليمنى للفقرة.

 **Examples:** 

يظهر كيفية تكوين تنسيق الفقرة لإنشاء نص غير مركزي.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Center all text that the document builder writes, and set up indents.
 // The indent configuration below will create a body of text that will sit asymmetrically on the page.
 // The "center" that we align the text to will be the middle of the body of text, not the middle of the page.
 ParagraphFormat paragraphFormat = builder.getParagraphFormat();
 paragraphFormat.setAlignment(ParagraphAlignment.CENTER);
 paragraphFormat.setLeftIndent(100.0);
 paragraphFormat.setRightIndent(50.0);
 paragraphFormat.setSpaceAfter(25.0);

 builder.writeln(
         "This paragraph demonstrates how left and right indentation affects word wrapping.");
 builder.writeln(
         "The space between the above paragraph and this one depends on the DocumentBuilder's paragraph format.");

 doc.save(getArtifactsDir() + "DocumentBuilder.SetParagraphFormatting.docx");
 
```

**Returns:**
double - القيمة (بالنقاط) التي تمثل الهامش الأيمن للفقرة.
### getShading() {#getShading}
```
public Shading getShading()
```


يعيد كائن [Shading](../../com.aspose.words/shading/) الذي يشير إلى تنسيق التظليل للفقرة.

 **Examples:** 

يوضح كيفية تزيين النص بالحدود والتظليل.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 BorderCollection borders = builder.getParagraphFormat().getBorders();
 borders.setDistanceFromText(20.0);
 borders.getByBorderType(BorderType.LEFT).setLineStyle(LineStyle.DOUBLE);
 borders.getByBorderType(BorderType.RIGHT).setLineStyle(LineStyle.DOUBLE);
 borders.getByBorderType(BorderType.TOP).setLineStyle(LineStyle.DOUBLE);
 borders.getByBorderType(BorderType.BOTTOM).setLineStyle(LineStyle.DOUBLE);

 Shading shading = builder.getParagraphFormat().getShading();
 shading.setTexture(TextureIndex.TEXTURE_DIAGONAL_CROSS);
 shading.setBackgroundPatternColor(new Color(240, 128, 128));  // Light Coral
 shading.setForegroundPatternColor(new Color(255, 160, 122));  // Light Salmon

 builder.write("This paragraph is formatted with a double border and shading.");
 doc.save(getArtifactsDir() + "DocumentBuilder.ApplyBordersAndShading.docx");
 
```

**Returns:**
[Shading](../../com.aspose.words/shading/) - A [Shading](../../com.aspose.words/shading/) object that refers to the shading formatting for the paragraph.
### getSnapToGrid() {#getSnapToGrid}
```
public boolean getSnapToGrid()
```


يحدد ما إذا كان يجب على الفقرة الحالية استخدام إعدادات خطوط شبكة المستند لكل صفحة عند تنسيق المحتوى داخل الفقرة.

 **Examples:** 

يظهر كيفية تحديد حد لعدد الأسطر التي قد يحتويها كل صفحة.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Enable pitching, and then use it to set the number of lines per page in this section.
 // A large enough font size will push some lines down onto the next page to avoid overlapping characters.
 builder.getPageSetup().setLayoutMode(SectionLayoutMode.LINE_GRID);
 builder.getPageSetup().setLinesPerPage(15);

 builder.getParagraphFormat().setSnapToGrid(true);

 for (int i = 0; i < 30; i++)
     builder.write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ");

 doc.save(getArtifactsDir() + "PageSetup.LinesPerPage.docx");
 
```

**Returns:**
boolean - القيمة المنطقية المقابلة.
### getSpaceAfter() {#getSpaceAfter}
```
public double getSpaceAfter()
```


يحصل على مقدار المسافة (بالنقاط) بعد الفقرة.

**Returns:**
double - مقدار التباعد (بالنقاط) بعد الفقرة.
### getSpaceAfterAuto() {#getSpaceAfterAuto}
```
public boolean getSpaceAfterAuto()
```


صحيح إذا تم تعيين مقدار المسافة بعد الفقرة تلقائيًا.

 **Remarks:** 

عند ضبطه على  true , يتجاوز تأثير [getSpaceAfter()](../../com.aspose.words/paragraphformat/\#getSpaceAfter) / [setSpaceAfter(double)](../../com.aspose.words/paragraphformat/\#setSpaceAfter-double).

عند ضبط مسافة الفقرة قبل وبعد إلى تلقائي، يضيف Microsoft Word تباعدًا قدره 14 نقطة بين الفقرات تلقائيًا وفقًا للقواعد التالية:

 *  Normally, spacing is added after all paragraphs.
 *  In a bulleted or numbered list, spacing is added only after the last item in the list. Spacing is not added between the list items.
 *  In a nested bulleted or numbered list spacing is not added.
 *  Spacing is normally added after a table.
 *  Spacing is not added after a table if it is the last block in a table cell.
 *  Spacing is not added after the last paragraph in a table cell.

 **Examples:** 

يظهر كيفية ضبط تباعد الفقرة التلقائي.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Apply a large amount of spacing before and after paragraphs that this builder will create.
 builder.getParagraphFormat().setSpaceBefore(24.0);
 builder.getParagraphFormat().setSpaceAfter(24.0);

 // Set these flags to "true" to apply automatic spacing,
 // effectively ignoring the spacing in the properties we set above.
 // Leave them as "false" will apply our custom paragraph spacing.
 builder.getParagraphFormat().setSpaceAfterAuto(autoSpacing);
 builder.getParagraphFormat().setSpaceBeforeAuto(autoSpacing);

 // Insert two paragraphs that will have spacing above and below them and save the document.
 builder.writeln("Paragraph 1.");
 builder.writeln("Paragraph 2.");

 doc.save(getArtifactsDir() + "ParagraphFormat.ParagraphSpacingAuto.docx");
 
```

**Returns:**
boolean - القيمة المنطقية المقابلة.
### getSpaceBefore() {#getSpaceBefore}
```
public double getSpaceBefore()
```


يحصل على مقدار المسافة (بالنقاط) قبل الفقرة.

**Returns:**
double - مقدار التباعد (بالنقاط) قبل الفقرة.
### getSpaceBeforeAuto() {#getSpaceBeforeAuto}
```
public boolean getSpaceBeforeAuto()
```


صحيح إذا تم تعيين مقدار المسافة قبل الفقرة تلقائيًا.

 **Remarks:** 

عند ضبطه على  true , يتجاوز تأثير [getSpaceBefore()](../../com.aspose.words/paragraphformat/\#getSpaceBefore) / [setSpaceBefore(double)](../../com.aspose.words/paragraphformat/\#setSpaceBefore-double).

عند ضبط مسافة الفقرة قبل وبعد إلى تلقائي، يضيف Microsoft Word تباعدًا قدره 14 نقطة بين الفقرات تلقائيًا وفقًا للقواعد التالية:

 *  Normally, spacing is added after all paragraphs.
 *  In a bulleted or numbered list, spacing is added only after the last item in the list. Spacing is not added between the list items.
 *  In a nested bulleted or numbered list spacing is not added.
 *  Spacing is normally added after a table.
 *  Spacing is not added after a table if it is the last block in a table cell.
 *  Spacing is not added after the last paragraph in a table cell.

 **Examples:** 

يظهر كيفية ضبط تباعد الفقرة التلقائي.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Apply a large amount of spacing before and after paragraphs that this builder will create.
 builder.getParagraphFormat().setSpaceBefore(24.0);
 builder.getParagraphFormat().setSpaceAfter(24.0);

 // Set these flags to "true" to apply automatic spacing,
 // effectively ignoring the spacing in the properties we set above.
 // Leave them as "false" will apply our custom paragraph spacing.
 builder.getParagraphFormat().setSpaceAfterAuto(autoSpacing);
 builder.getParagraphFormat().setSpaceBeforeAuto(autoSpacing);

 // Insert two paragraphs that will have spacing above and below them and save the document.
 builder.writeln("Paragraph 1.");
 builder.writeln("Paragraph 2.");

 doc.save(getArtifactsDir() + "ParagraphFormat.ParagraphSpacingAuto.docx");
 
```

**Returns:**
boolean - القيمة المنطقية المقابلة.
### getStyle() {#getStyle}
```
public Style getStyle()
```


يحصل على نمط الفقرة المطبق على هذا التنسيق.

 **Examples:** 

يوضح كيفية إنشاء واستخدام نمط فقرة مع تنسيق القوائم.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create a custom paragraph style.
 Style style = doc.getStyles().add(StyleType.PARAGRAPH, "MyStyle1");
 style.getFont().setSize(24.0);
 style.getFont().setName("Verdana");
 style.getParagraphFormat().setSpaceAfter(12.0);

 // Create a list and make sure the paragraphs that use this style will use this list.
 style.getListFormat().setList(doc.getLists().add(ListTemplate.BULLET_DEFAULT));
 style.getListFormat().setListLevelNumber(0);

 // Apply the paragraph style to the document builder's current paragraph, and then add some text.
 builder.getParagraphFormat().setStyle(style);
 builder.writeln("Hello World: MyStyle1, bulleted list.");

 // Change the document builder's style to one that has no list formatting and write another paragraph.
 builder.getParagraphFormat().setStyle(doc.getStyles().get("Normal"));
 builder.writeln("Hello World: Normal.");

 builder.getDocument().save(getArtifactsDir() + "Styles.ParagraphStyleBulletedList.docx");
 
```

**Returns:**
[Style](../../com.aspose.words/style/) - The paragraph style applied to this formatting.
### getStyleIdentifier() {#getStyleIdentifier}
```
public int getStyleIdentifier()
```


يحصل على معرف النمط المستقل عن اللغة لنمط الفقرة المطبق على هذا التنسيق.

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

**Returns:**
int - معرف النمط المستقل عن اللغة لنمط الفقرة المطبق على هذا التنسيق. القيمة المرجعة هي واحدة من ثوابت [StyleIdentifier](../../com.aspose.words/styleidentifier/).
### getStyleName() {#getStyleName}
```
public String getStyleName()
```


يحصل على اسم نمط الفقرة المطبق على هذا التنسيق.

 **Examples:** 

يوضح كيفية إنشاء مستند Aspose.Words يدوياً.

```

 Document doc = new Document();

 // A blank document contains one section, one body and one paragraph.
 // Call the "RemoveAllChildren" method to remove all those nodes,
 // and end up with a document node with no children.
 doc.removeAllChildren();

 // This document now has no composite child nodes that we can add content to.
 // If we wish to edit it, we will need to repopulate its node collection.
 // First, create a new section, and then append it as a child to the root document node.
 Section section = new Section(doc);
 doc.appendChild(section);

 // Set some page setup properties for the section.
 section.getPageSetup().setSectionStart(SectionStart.NEW_PAGE);
 section.getPageSetup().setPaperSize(PaperSize.LETTER);

 // A section needs a body, which will contain and display all its contents
 // on the page between the section's header and footer.
 Body body = new Body(doc);
 section.appendChild(body);

 // Create a paragraph, set some formatting properties, and then append it as a child to the body.
 Paragraph para = new Paragraph(doc);

 para.getParagraphFormat().setStyleName("Heading 1");
 para.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);

 body.appendChild(para);

 // Finally, add some content to do the document. Create a run,
 // set its appearance and contents, and then append it as a child to the paragraph.
 Run run = new Run(doc);
 run.setText("Hello World!");
 run.getFont().setColor(Color.RED);
 para.appendChild(run);

 Assert.assertEquals("Hello World!", doc.getText().trim());

 doc.save(getArtifactsDir() + "Section.CreateManually.docx");
 
```

**Returns:**
java.lang.String - اسم نمط الفقرة المطبق على هذا التنسيق.
### getSuppressAutoHyphens() {#getSuppressAutoHyphens}
```
public boolean getSuppressAutoHyphens()
```


يحدد ما إذا كان يجب إعفاء الفقرة الحالية من أي تجزئة تُطبق في إعدادات المستند.

 **Examples:** 

يظهر كيفية إلغاء تجزئة الكلمات لفقرة.

```

 Hyphenation.registerDictionary("de-CH", getMyDir() + "hyph_de_CH.dic");

 Assert.assertTrue(Hyphenation.isDictionaryRegistered("de-CH"));

 // Open a document containing text with a locale matching that of our dictionary.
 // When we save this document to a fixed page save format, its text will have hyphenation.
 Document doc = new Document(getMyDir() + "German text.docx");

 // We can set the "SuppressAutoHyphens" property to "true" to disable hyphenation
 // for a specific paragraph while keeping it enabled for the rest of the document.
 // The default value for this property is "false",
 // which means every paragraph by default uses hyphenation if any is available.
 doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat().setSuppressAutoHyphens(suppressAutoHyphens);

 doc.save(getArtifactsDir() + "ParagraphFormat.SuppressHyphens.pdf");
 
```

**Returns:**
boolean - القيمة المنطقية المقابلة.
### getSuppressLineNumbers() {#getSuppressLineNumbers}
```
public boolean getSuppressLineNumbers()
```


يحدد ما إذا كان يجب إعفاء أسطر الفقرة الحالية من ترقيم الأسطر الذي يُطبق في القسم الأب.

 **Examples:** 

يظهر كيفية تمكين ترقيم الأسطر لقسم.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // We can use the section's PageSetup object to display numbers to the left of the section's text lines.
 // This is the same behavior as a List object,
 // but it covers the entire section and does not modify the text in any way.
 // Our section will restart the numbering on each new page from 1 and display the number,
 // if it is a multiple of 3, at 50pt to the left of the line.
 PageSetup pageSetup = builder.getPageSetup();
 pageSetup.setLineStartingNumber(1);
 pageSetup.setLineNumberCountBy(3);
 pageSetup.setLineNumberRestartMode(LineNumberRestartMode.RESTART_PAGE);
 pageSetup.setLineNumberDistanceFromText(50.0d);

 for (int i = 1; i <= 25; i++)
     builder.writeln(MessageFormat.format("Line {0}.", i));

 // The line counter will skip any paragraph with the "SuppressLineNumbers" flag set to "true".
 // This paragraph is on the 15th line, which is a multiple of 3, and thus would normally display a line number.
 // The section's line counter will also ignore this line, treat the next line as the 15th,
 // and continue the count from that point onward.
 doc.getFirstSection().getBody().getParagraphs().get(14).getParagraphFormat().setSuppressLineNumbers(true);

 doc.save(getArtifactsDir() + "PageSetup.LineNumbers.docx");
 
```

**Returns:**
boolean - القيمة المنطقية المقابلة.
### getTabStops() {#getTabStops}
```
public TabStopCollection getTabStops()
```


يحصل على مجموعة نقاط التبويب المخصصة المعرفة لهذا الكائن.

 **Examples:** 

يعرض كيفية تعديل موضع علامة التبويب اليمنى في الفقرات المتعلقة بالفهرس.

```

 Document doc = new Document(getMyDir() + "Table of contents.docx");

 // Iterate through all paragraphs with TOC result-based styles; this is any style between TOC and TOC9.
 for (Paragraph para : (Iterable) doc.getChildNodes(NodeType.PARAGRAPH, true)) {
     if (para.getParagraphFormat().getStyle().getStyleIdentifier() >= StyleIdentifier.TOC_1
             && para.getParagraphFormat().getStyle().getStyleIdentifier() <= StyleIdentifier.TOC_9) {
         // Get the first tab used in this paragraph, this should be the tab used to align the page numbers.
         TabStop tab = para.getParagraphFormat().getTabStops().get(0);

         // Replace the first default tab, stop with a custom tab stop.
         para.getParagraphFormat().getTabStops().removeByPosition(tab.getPosition());
         para.getParagraphFormat().getTabStops().add(tab.getPosition() - 50.0, tab.getAlignment(), tab.getLeader());
     }
 }

 doc.save(getArtifactsDir() + "Styles.ChangeTocsTabStops.docx");
 
```

**Returns:**
[TabStopCollection](../../com.aspose.words/tabstopcollection/) - The collection of custom tab stops defined for this object.
### getWidowControl() {#getWidowControl}
```
public boolean getWidowControl()
```


صحيح إذا كان يجب أن تبقى السطران الأول والأخير في الفقرة على نفس الصفحة مع باقي الفقرة.

 **Examples:** 

يظهر كيفية تمكين التحكم في القُرّات/الأيتام لفقرة.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // When we write the text that does not fit onto one page, one line may spill over onto the next page.
 // The single line that ends up on the next page is called an "Orphan",
 // and the previous line where the orphan broke off is called a "Widow".
 // We can fix orphans and widows by rearranging text via font size, spacing, or page margins.
 // If we wish to preserve our document's dimensions, we can set this flag to "true"
 // to push widows onto the same page as their respective orphans.
 // Leave this flag as "false" will leave widow/orphan pairs in text.
 // Every paragraph has this setting accessible in Microsoft Word via Home -> Paragraph -> Paragraph Settings
 // (button on bottom right hand corner of "Paragraph" tab) -> "Widow/Orphan control".
 builder.getParagraphFormat().setWidowControl(widowControl);

 // Insert text that produces an orphan and a widow.
 builder.getFont().setSize(68.0);
 builder.write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
         "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

 doc.save(getArtifactsDir() + "ParagraphFormat.WidowControl.docx");
 
```

**Returns:**
boolean - القيمة المنطقية المقابلة.
### getWordWrap() {#getWordWrap}
```
public boolean getWordWrap()
```


إذا كانت هذه الخاصية  false , يمكن لف النص اللاتيني في وسط كلمة للفقرة الحالية. وإلا يتم لف النص اللاتيني بكلمات كاملة.

 **Examples:** 

يظهر كيفية ضبط خصائص خاصة للطباعة الآسيوية.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 ParagraphFormat format = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat();
 format.setFarEastLineBreakControl(true);
 format.setWordWrap(false);
 format.setHangingPunctuation(true);

 doc.save(getArtifactsDir() + "ParagraphFormat.AsianTypographyProperties.docx");
 
```

**Returns:**
boolean - القيمة المنطقية المقابلة.
### isHeading() {#isHeading}
```
public boolean isHeading()
```


صحيح عندما يكون نمط الفقرة أحد أنماط العناوين المدمجة.

 **Examples:** 

يظهر كيفية تحديد مستوى العناوين التي ستظهر في مخطط مستند PDF المحفوظ.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert headings that can serve as TOC entries of levels 1, 2, and then 3.
 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_1);

 Assert.assertTrue(builder.getParagraphFormat().isHeading());

 builder.writeln("Heading 1");

 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_2);

 builder.writeln("Heading 1.1");
 builder.writeln("Heading 1.2");

 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_3);

 builder.writeln("Heading 1.2.1");
 builder.writeln("Heading 1.2.2");

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 PdfSaveOptions saveOptions = new PdfSaveOptions();
 saveOptions.setSaveFormat(SaveFormat.PDF);

 // The output PDF document will contain an outline, which is a table of contents that lists headings in the document body.
 // Clicking on an entry in this outline will take us to the location of its respective heading.
 // Set the "HeadingsOutlineLevels" property to "2" to exclude all headings whose levels are above 2 from the outline.
 // The last two headings we have inserted above will not appear.
 saveOptions.getOutlineOptions().setHeadingsOutlineLevels(2);

 doc.save(getArtifactsDir() + "PdfSaveOptions.HeadingsOutlineLevels.pdf", saveOptions);
 
```

**Returns:**
boolean - القيمة المنطقية المقابلة.
### isListItem() {#isListItem}
```
public boolean isListItem()
```


صحيح عندما تكون الفقرة عنصرًا في قائمة نقطية أو رقمية.

 **Examples:** 

يوضح كيفية تضمين قائمة داخل قائمة أخرى.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // A list allows us to organize and decorate sets of paragraphs with prefix symbols and indents.
 // We can create nested lists by increasing the indent level.
 // We can begin and end a list by using a document builder's "ListFormat" property.
 // Each paragraph that we add between a list's start and the end will become an item in the list.
 // Create an outline list for the headings.
 List outlineList = doc.getLists().add(ListTemplate.OUTLINE_NUMBERS);
 builder.getListFormat().setList(outlineList);
 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_1);
 builder.writeln("This is my Chapter 1");

 // Create a numbered list.
 List numberedList = doc.getLists().add(ListTemplate.NUMBER_DEFAULT);
 builder.getListFormat().setList(numberedList);
 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.NORMAL);
 builder.writeln("Numbered list item 1.");

 // Every paragraph that comprises a list will have this flag.
 Assert.assertTrue(builder.getCurrentParagraph().isListItem());
 Assert.assertTrue(builder.getParagraphFormat().isListItem());

 // Create a bulleted list.
 List bulletedList = doc.getLists().add(ListTemplate.BULLET_DEFAULT);
 builder.getListFormat().setList(bulletedList);
 builder.getParagraphFormat().setLeftIndent(72.0);
 builder.writeln("Bulleted list item 1.");
 builder.writeln("Bulleted list item 2.");
 builder.getParagraphFormat().clearFormatting();

 // Revert to the numbered list.
 builder.getListFormat().setList(numberedList);
 builder.writeln("Numbered list item 2.");
 builder.writeln("Numbered list item 3.");

 // Revert to the outline list.
 builder.getListFormat().setList(outlineList);
 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_1);
 builder.writeln("This is my Chapter 2");

 builder.getParagraphFormat().clearFormatting();

 builder.getDocument().save(getArtifactsDir() + "Lists.NestedLists.docx");
 
```

**Returns:**
boolean - القيمة المنطقية المقابلة.
### setAddSpaceBetweenFarEastAndAlpha(boolean value) {#setAddSpaceBetweenFarEastAndAlpha-boolean}
```
public void setAddSpaceBetweenFarEastAndAlpha(boolean value)
```


يضبط علامة تشير إلى ما إذا كان يتم تعديل التباعد بين الأحرف تلقائيًا بين مناطق النص اللاتيني ومناطق النص الآسيوي الشرقي في الفقرة الحالية.

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

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | علامة تشير إلى ما إذا تم تعديل التباعد بين الأحرف تلقائيًا بين مناطق النص اللاتيني ومناطق النص الآسيوي الشرقي في الفقرة الحالية. |

### setAddSpaceBetweenFarEastAndDigit(boolean value) {#setAddSpaceBetweenFarEastAndDigit-boolean}
```
public void setAddSpaceBetweenFarEastAndDigit(boolean value)
```


يضبط علامة تشير إلى ما إذا كان يتم تعديل التباعد بين الأحرف تلقائيًا بين مناطق الأرقام ومناطق النص الآسيوي الشرقي في الفقرة الحالية.

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

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | علامة تشير إلى ما إذا تم تعديل التباعد بين الأحرف تلقائيًا بين مناطق الأرقام ومناطق النص الآسيوي الشرقي في الفقرة الحالية. |

### setAlignment(int value) {#setAlignment-int}
```
public void setAlignment(int value)
```


يضبط محاذاة النص للفقرة.

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

يوضح كيفية إنشاء مستند Aspose.Words يدوياً.

```

 Document doc = new Document();

 // A blank document contains one section, one body and one paragraph.
 // Call the "RemoveAllChildren" method to remove all those nodes,
 // and end up with a document node with no children.
 doc.removeAllChildren();

 // This document now has no composite child nodes that we can add content to.
 // If we wish to edit it, we will need to repopulate its node collection.
 // First, create a new section, and then append it as a child to the root document node.
 Section section = new Section(doc);
 doc.appendChild(section);

 // Set some page setup properties for the section.
 section.getPageSetup().setSectionStart(SectionStart.NEW_PAGE);
 section.getPageSetup().setPaperSize(PaperSize.LETTER);

 // A section needs a body, which will contain and display all its contents
 // on the page between the section's header and footer.
 Body body = new Body(doc);
 section.appendChild(body);

 // Create a paragraph, set some formatting properties, and then append it as a child to the body.
 Paragraph para = new Paragraph(doc);

 para.getParagraphFormat().setStyleName("Heading 1");
 para.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);

 body.appendChild(para);

 // Finally, add some content to do the document. Create a run,
 // set its appearance and contents, and then append it as a child to the paragraph.
 Run run = new Run(doc);
 run.setText("Hello World!");
 run.getFont().setColor(Color.RED);
 para.appendChild(run);

 Assert.assertEquals("Hello World!", doc.getText().trim());

 doc.save(getArtifactsDir() + "Section.CreateManually.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| value | int | محاذاة النص للفقرة. يجب أن تكون القيمة واحدة من ثوابت [ParagraphAlignment](../../com.aspose.words/paragraphalignment/). |

### setBaselineAlignment(int value) {#setBaselineAlignment-int}
```
public void setBaselineAlignment(int value)
```


يضبط الموضع الرأسي للخطوط على السطر.

 **Examples:** 

يظهر كيفية ضبط الموضع العمودي للخطوط على سطر.

```

 Document doc = new Document(getMyDir() + "Office math.docx");

 ParagraphFormat format = doc.getFirstSection().getBody().getParagraphs().get(0).getParagraphFormat();
 if (format.getBaselineAlignment() == BaselineAlignment.AUTO)
 {
     format.setBaselineAlignment(BaselineAlignment.TOP);
 }

 doc.save(getArtifactsDir() + "ParagraphFormat.ParagraphBaselineAlignment.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| value | int | الموضع العمودي للخطوط على السطر. يجب أن تكون القيمة واحدة من ثوابت [BaselineAlignment](../../com.aspose.words/baselinealignment/). |

### setBidi(boolean value) {#setBidi-boolean}
```
public void setBidi(boolean value)
```


يضبط ما إذا كانت هذه الفقرة من اليمين إلى اليسار.

 **Remarks:** 

عند true، يتم ترتيب المقاطع والكائنات المضمنة الأخرى في هذه الفقرة من اليمين إلى اليسار.

 **Examples:** 

يوضح كيفية إنشاء قوائم متوافقة مع اللغات من اليمين إلى اليسار باستخدام حقول BIDIOUTLINE.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // The BIDIOUTLINE field numbers paragraphs like the AUTONUM/LISTNUM fields,
 // but is only visible when a right-to-left editing language is enabled, such as Hebrew or Arabic.
 // The following field will display ".1", the RTL equivalent of list number "1.".
 FieldBidiOutline field = (FieldBidiOutline) builder.insertField(FieldType.FIELD_BIDI_OUTLINE, true);
 builder.writeln("\u05e9\u05dc\u05d5\u05dd");

 Assert.assertEquals(" BIDIOUTLINE ", field.getFieldCode());

 // Add two more BIDIOUTLINE fields, which will display ".2" and ".3".
 builder.insertField(FieldType.FIELD_BIDI_OUTLINE, true);
 builder.writeln("\u05e9\u05dc\u05d5\u05dd");
 builder.insertField(FieldType.FIELD_BIDI_OUTLINE, true);
 builder.writeln("\u05e9\u05dc\u05d5\u05dd");

 // Set the horizontal text alignment for every paragraph in the document to RTL.
 for (Paragraph para : (Iterable) doc.getChildNodes(NodeType.PARAGRAPH, true)) {
     para.getParagraphFormat().setBidi(true);
 }

 // If we enable a right-to-left editing language in Microsoft Word, our fields will display numbers.
 // Otherwise, they will display "###".
 doc.save(getArtifactsDir() + "Field.BIDIOUTLINE.docx");
 
```

يوضح كيفية اكتشاف اتجاه نص المستند النصي العادي.

```

 // Create a "TxtLoadOptions" object, which we can pass to a document's constructor
 // to modify how we load a plaintext document.
 TxtLoadOptions loadOptions = new TxtLoadOptions();

 // Set the "DocumentDirection" property to "DocumentDirection.Auto" automatically detects
 // the direction of every paragraph of text that Aspose.Words loads from plaintext.
 // Each paragraph's "Bidi" property will store its direction.
 loadOptions.setDocumentDirection(DocumentDirection.AUTO);

 // Detect Hebrew text as right-to-left.
 Document doc = new Document(getMyDir() + "Hebrew text.txt", loadOptions);

 Assert.assertTrue(doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat().getBidi());

 // Detect English text as right-to-left.
 doc = new Document(getMyDir() + "English text.txt", loadOptions);

 Assert.assertFalse(doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat().getBidi());
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | ما إذا كانت هذه فقرة من اليمين إلى اليسار. |

### setBorderAttr(int key, Object value) {#setBorderAttr-int-java.lang.Object}
```
public void setBorderAttr(int key, Object value)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| key | int |  |
| قيمة | java.lang.Object |  |

### setCharacterUnitFirstLineIndent(double value) {#setCharacterUnitFirstLineIndent-double}
```
public void setCharacterUnitFirstLineIndent(double value)
```


يضبط القيمة (بالحروف) للسطر الأول أو الإزاحة المتدلية.

استخدم القيم الموجبة لضبط إزاحة السطر الأول، والقيم السالبة لضبط الإزاحة المتدلية.

 **Examples:** 

يظهر كيفية تغيير مسافات الفقرة والإزاحات.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 ParagraphFormat format = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat();

 // Below are five different spacing options, along with the properties that their configuration indirectly affects.
 // 1 -  Left indent:
 Assert.assertEquals(format.getLeftIndent(), 0.0d);

 format.setCharacterUnitLeftIndent(10.0);

 Assert.assertEquals(format.getLeftIndent(), 120.0d);

 // 2 -  Right indent:
 Assert.assertEquals(format.getRightIndent(), 0.0d);

 format.setCharacterUnitRightIndent(-5.5);

 Assert.assertEquals(format.getRightIndent(), -66.0d);

 // 3 -  Hanging indent:
 Assert.assertEquals(format.getFirstLineIndent(), 0.0d);

 format.setCharacterUnitFirstLineIndent(20.3);

 Assert.assertEquals(format.getFirstLineIndent(), 243.59d, 0.1d);

 // 4 -  Line spacing before paragraphs:
 Assert.assertEquals(format.getSpaceBefore(), 0.0d);

 format.setLineUnitBefore(5.1);

 Assert.assertEquals(format.getSpaceBefore(), 61.1d, 0.1d);

 // 5 -  Line spacing after paragraphs:
 Assert.assertEquals(format.getSpaceAfter(), 0.0d);

 format.setLineUnitAfter(10.9);

 Assert.assertEquals(format.getSpaceAfter(), 130.8d, 0.1d);

 builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
         "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
 builder.write("\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5" +
         "\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | double | القيمة (بالحروف) للمسافة البادئة للسطرة الأولى أو المتدلية. |

### setCharacterUnitLeftIndent(double value) {#setCharacterUnitLeftIndent-double}
```
public void setCharacterUnitLeftIndent(double value)
```


يضبط قيمة الإزاحة اليسرى (بالحروف) للفقرات المحددة.

 **Examples:** 

يظهر كيفية تغيير مسافات الفقرة والإزاحات.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 ParagraphFormat format = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat();

 // Below are five different spacing options, along with the properties that their configuration indirectly affects.
 // 1 -  Left indent:
 Assert.assertEquals(format.getLeftIndent(), 0.0d);

 format.setCharacterUnitLeftIndent(10.0);

 Assert.assertEquals(format.getLeftIndent(), 120.0d);

 // 2 -  Right indent:
 Assert.assertEquals(format.getRightIndent(), 0.0d);

 format.setCharacterUnitRightIndent(-5.5);

 Assert.assertEquals(format.getRightIndent(), -66.0d);

 // 3 -  Hanging indent:
 Assert.assertEquals(format.getFirstLineIndent(), 0.0d);

 format.setCharacterUnitFirstLineIndent(20.3);

 Assert.assertEquals(format.getFirstLineIndent(), 243.59d, 0.1d);

 // 4 -  Line spacing before paragraphs:
 Assert.assertEquals(format.getSpaceBefore(), 0.0d);

 format.setLineUnitBefore(5.1);

 Assert.assertEquals(format.getSpaceBefore(), 61.1d, 0.1d);

 // 5 -  Line spacing after paragraphs:
 Assert.assertEquals(format.getSpaceAfter(), 0.0d);

 format.setLineUnitAfter(10.9);

 Assert.assertEquals(format.getSpaceAfter(), 130.8d, 0.1d);

 builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
         "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
 builder.write("\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5" +
         "\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | double | قيمة المسافة البادئة اليسرى (بالحروف) للفقرات المحددة. |

### setCharacterUnitRightIndent(double value) {#setCharacterUnitRightIndent-double}
```
public void setCharacterUnitRightIndent(double value)
```


يضبط قيمة الإزاحة اليمنى (بالحروف) للفقرات المحددة.

 **Examples:** 

يظهر كيفية تغيير مسافات الفقرة والإزاحات.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 ParagraphFormat format = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat();

 // Below are five different spacing options, along with the properties that their configuration indirectly affects.
 // 1 -  Left indent:
 Assert.assertEquals(format.getLeftIndent(), 0.0d);

 format.setCharacterUnitLeftIndent(10.0);

 Assert.assertEquals(format.getLeftIndent(), 120.0d);

 // 2 -  Right indent:
 Assert.assertEquals(format.getRightIndent(), 0.0d);

 format.setCharacterUnitRightIndent(-5.5);

 Assert.assertEquals(format.getRightIndent(), -66.0d);

 // 3 -  Hanging indent:
 Assert.assertEquals(format.getFirstLineIndent(), 0.0d);

 format.setCharacterUnitFirstLineIndent(20.3);

 Assert.assertEquals(format.getFirstLineIndent(), 243.59d, 0.1d);

 // 4 -  Line spacing before paragraphs:
 Assert.assertEquals(format.getSpaceBefore(), 0.0d);

 format.setLineUnitBefore(5.1);

 Assert.assertEquals(format.getSpaceBefore(), 61.1d, 0.1d);

 // 5 -  Line spacing after paragraphs:
 Assert.assertEquals(format.getSpaceAfter(), 0.0d);

 format.setLineUnitAfter(10.9);

 Assert.assertEquals(format.getSpaceAfter(), 130.8d, 0.1d);

 builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
         "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
 builder.write("\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5" +
         "\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | double | قيمة المسافة البادئة اليمنى (بالحروف) للفقرات المحددة. |

### setDropCapPosition(int value) {#setDropCapPosition-int}
```
public void setDropCapPosition(int value)
```


يضبط موضع النص بالحرف الأول الكبير.

 **Examples:** 

يوضح كيفية تضمين قائمة داخل قائمة أخرى.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // A list allows us to organize and decorate sets of paragraphs with prefix symbols and indents.
 // We can create nested lists by increasing the indent level.
 // We can begin and end a list by using a document builder's "ListFormat" property.
 // Each paragraph that we add between a list's start and the end will become an item in the list.
 // Create an outline list for the headings.
 List outlineList = doc.getLists().add(ListTemplate.OUTLINE_NUMBERS);
 builder.getListFormat().setList(outlineList);
 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_1);
 builder.writeln("This is my Chapter 1");

 // Create a numbered list.
 List numberedList = doc.getLists().add(ListTemplate.NUMBER_DEFAULT);
 builder.getListFormat().setList(numberedList);
 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.NORMAL);
 builder.writeln("Numbered list item 1.");

 // Every paragraph that comprises a list will have this flag.
 Assert.assertTrue(builder.getCurrentParagraph().isListItem());
 Assert.assertTrue(builder.getParagraphFormat().isListItem());

 // Create a bulleted list.
 List bulletedList = doc.getLists().add(ListTemplate.BULLET_DEFAULT);
 builder.getListFormat().setList(bulletedList);
 builder.getParagraphFormat().setLeftIndent(72.0);
 builder.writeln("Bulleted list item 1.");
 builder.writeln("Bulleted list item 2.");
 builder.getParagraphFormat().clearFormatting();

 // Revert to the numbered list.
 builder.getListFormat().setList(numberedList);
 builder.writeln("Numbered list item 2.");
 builder.writeln("Numbered list item 3.");

 // Revert to the outline list.
 builder.getListFormat().setList(outlineList);
 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_1);
 builder.writeln("This is my Chapter 2");

 builder.getParagraphFormat().clearFormatting();

 builder.getDocument().save(getArtifactsDir() + "Lists.NestedLists.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| value | int | الموضع لنص الحرف الأول المتناثر. يجب أن تكون القيمة واحدة من ثوابت [DropCapPosition](../../com.aspose.words/dropcapposition/). |

### setFarEastLineBreakControl(boolean value) {#setFarEastLineBreakControl-boolean}
```
public void setFarEastLineBreakControl(boolean value)
```


يضبط علامة تشير إلى ما إذا كانت قواعد كسر السطر الآسيوي الشرقي مطبقة على الفقرة الحالية.

 **Examples:** 

يظهر كيفية ضبط خصائص خاصة للطباعة الآسيوية.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 ParagraphFormat format = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat();
 format.setFarEastLineBreakControl(true);
 format.setWordWrap(false);
 format.setHangingPunctuation(true);

 doc.save(getArtifactsDir() + "ParagraphFormat.AsianTypographyProperties.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | علامة تشير إلى ما إذا تم تطبيق قواعد كسر السطر الآسيوي الشرقي على الفقرة الحالية. |

### setFirstLineIndent(double value) {#setFirstLineIndent-double}
```
public void setFirstLineIndent(double value)
```


يضبط القيمة (بالنقاط) للسطر الأول أو الإزاحة المتدلية.

استخدم القيم الموجبة لضبط إزاحة السطر الأول، والقيم السالبة لضبط الإزاحة المتدلية.

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

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | double | القيمة (بالنقاط) للمسافة البادئة للسطرة الأولى أو المتدلية. |

### setHangingPunctuation(boolean value) {#setHangingPunctuation-boolean}
```
public void setHangingPunctuation(boolean value)
```


يضبط علامة تشير إلى ما إذا كانت علامات الترقيم المتدلية مفعلة للفقرة الحالية.

 **Examples:** 

يظهر كيفية ضبط خصائص خاصة للطباعة الآسيوية.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 ParagraphFormat format = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat();
 format.setFarEastLineBreakControl(true);
 format.setWordWrap(false);
 format.setHangingPunctuation(true);

 doc.save(getArtifactsDir() + "ParagraphFormat.AsianTypographyProperties.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | علامة تشير إلى ما إذا تم تمكين علامات الترقيم المتدلية للفقرة الحالية. |

### setKeepTogether(boolean value) {#setKeepTogether-boolean}
```
public void setKeepTogether(boolean value)
```


صحيح إذا كان يجب أن تبقى جميع الأسطر في الفقرة على نفس الصفحة.

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

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | القيمة المنطقية المقابلة. |

### setKeepWithNext(boolean value) {#setKeepWithNext-boolean}
```
public void setKeepWithNext(boolean value)
```


صحيح إذا كان يجب أن تبقى الفقرة على نفس الصفحة مع الفقرة التي تليها.

 **Examples:** 

يوضح كيفية ضبط جدول للبقاء معًا في نفس الصفحة.

```

 Document doc = new Document(getMyDir() + "Table spanning two pages.docx");
 Table table = doc.getFirstSection().getBody().getTables().get(0);

 // Enabling KeepWithNext for every paragraph in the table except for the
 // last ones in the last row will prevent the table from splitting across multiple pages.
 for (Cell cell : (Iterable) table.getChildNodes(NodeType.CELL, true))
     for (Paragraph para : cell.getParagraphs()) {
         Assert.assertTrue(para.isInCell());

         if (!(cell.getParentRow().isLastRow() && para.isEndOfCell()))
             para.getParagraphFormat().setKeepWithNext(true);
     }

 doc.save(getArtifactsDir() + "Table.KeepTableTogether.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | القيمة المنطقية المقابلة. |

### setLeftIndent(double value) {#setLeftIndent-double}
```
public void setLeftIndent(double value)
```


يضبط القيمة (بالنقاط) التي تمثل الإزاحة اليسرى للفقرة.

 **Examples:** 

يظهر كيفية تكوين تنسيق الفقرة لإنشاء نص غير مركزي.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Center all text that the document builder writes, and set up indents.
 // The indent configuration below will create a body of text that will sit asymmetrically on the page.
 // The "center" that we align the text to will be the middle of the body of text, not the middle of the page.
 ParagraphFormat paragraphFormat = builder.getParagraphFormat();
 paragraphFormat.setAlignment(ParagraphAlignment.CENTER);
 paragraphFormat.setLeftIndent(100.0);
 paragraphFormat.setRightIndent(50.0);
 paragraphFormat.setSpaceAfter(25.0);

 builder.writeln(
         "This paragraph demonstrates how left and right indentation affects word wrapping.");
 builder.writeln(
         "The space between the above paragraph and this one depends on the DocumentBuilder's paragraph format.");

 doc.save(getArtifactsDir() + "DocumentBuilder.SetParagraphFormatting.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | double | القيمة (بالنقاط) التي تمثل المسافة البادئة اليسرى للفقرة. |

### setLineSpacing(double value) {#setLineSpacing-double}
```
public void setLineSpacing(double value)
```


يضبط تباعد السطر (بالنقاط) للفقرة.

 **Remarks:** 

عند ضبط خاصية [getLineSpacingRule()](../../com.aspose.words/paragraphformat/\#getLineSpacingRule) / [setLineSpacingRule(int)](../../com.aspose.words/paragraphformat/\#setLineSpacingRule-int) إلى [LineSpacingRule.AT\_LEAST](../../com.aspose.words/linespacingrule/\#AT-LEAST)، يمكن أن تكون مسافة السطر أكبر من أو مساوية، ولكن لا تكون أبداً أقل من القيمة المحددة لـ [getLineSpacing()](../../com.aspose.words/paragraphformat/\#getLineSpacing) / [setLineSpacing(double)](../../com.aspose.words/paragraphformat/\#setLineSpacing-double).

عند ضبط خاصية [getLineSpacingRule()](../../com.aspose.words/paragraphformat/\#getLineSpacingRule) / [setLineSpacingRule(int)](../../com.aspose.words/paragraphformat/\#setLineSpacingRule-int) إلى [LineSpacingRule.EXACTLY](../../com.aspose.words/linespacingrule/\#EXACTLY)، لا تتغير مسافة السطر أبداً عن القيمة المحددة لـ [getLineSpacing()](../../com.aspose.words/paragraphformat/\#getLineSpacing) / [setLineSpacing(double)](../../com.aspose.words/paragraphformat/\#setLineSpacing-double)، حتى إذا تم استخدام خط أكبر داخل الفقرة.

 **Examples:** 

يظهر كيفية التعامل مع تباعد الأسطر.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Below are three line spacing rules that we can define using the
 // paragraph's "LineSpacingRule" property to configure spacing between paragraphs.
 // 1 -  Set a minimum amount of spacing.
 // This will give vertical padding to lines of text of any size
 // that is too small to maintain the minimum line-height.
 builder.getParagraphFormat().setLineSpacingRule(LineSpacingRule.AT_LEAST);
 builder.getParagraphFormat().setLineSpacing(20.0);

 builder.writeln("Minimum line spacing of 20.");
 builder.writeln("Minimum line spacing of 20.");

 // 2 -  Set exact spacing.
 // Using font sizes that are too large for the spacing will truncate the text.
 builder.getParagraphFormat().setLineSpacingRule(LineSpacingRule.EXACTLY);
 builder.getParagraphFormat().setLineSpacing(5.0);

 builder.writeln("Line spacing of exactly 5.");
 builder.writeln("Line spacing of exactly 5.");

 // 3 -  Set spacing as a multiple of default line spacing, which is 12 points by default.
 // This kind of spacing will scale to different font sizes.
 builder.getParagraphFormat().setLineSpacingRule(LineSpacingRule.MULTIPLE);
 builder.getParagraphFormat().setLineSpacing(18.0);

 builder.writeln("Line spacing of 1.5 default lines.");
 builder.writeln("Line spacing of 1.5 default lines.");

 doc.save(getArtifactsDir() + "ParagraphFormat.LineSpacing.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | double | تباعد الأسطر (بالنقاط) للفقرة. |

### setLineSpacingRule(int value) {#setLineSpacingRule-int}
```
public void setLineSpacingRule(int value)
```


يضبط تباعد السطر للفقرة.

 **Examples:** 

يظهر كيفية التعامل مع تباعد الأسطر.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Below are three line spacing rules that we can define using the
 // paragraph's "LineSpacingRule" property to configure spacing between paragraphs.
 // 1 -  Set a minimum amount of spacing.
 // This will give vertical padding to lines of text of any size
 // that is too small to maintain the minimum line-height.
 builder.getParagraphFormat().setLineSpacingRule(LineSpacingRule.AT_LEAST);
 builder.getParagraphFormat().setLineSpacing(20.0);

 builder.writeln("Minimum line spacing of 20.");
 builder.writeln("Minimum line spacing of 20.");

 // 2 -  Set exact spacing.
 // Using font sizes that are too large for the spacing will truncate the text.
 builder.getParagraphFormat().setLineSpacingRule(LineSpacingRule.EXACTLY);
 builder.getParagraphFormat().setLineSpacing(5.0);

 builder.writeln("Line spacing of exactly 5.");
 builder.writeln("Line spacing of exactly 5.");

 // 3 -  Set spacing as a multiple of default line spacing, which is 12 points by default.
 // This kind of spacing will scale to different font sizes.
 builder.getParagraphFormat().setLineSpacingRule(LineSpacingRule.MULTIPLE);
 builder.getParagraphFormat().setLineSpacing(18.0);

 builder.writeln("Line spacing of 1.5 default lines.");
 builder.writeln("Line spacing of 1.5 default lines.");

 doc.save(getArtifactsDir() + "ParagraphFormat.LineSpacing.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| value | int | تباعد الأسطر للفقرة. يجب أن تكون القيمة واحدة من ثوابت [LineSpacingRule](../../com.aspose.words/linespacingrule/). |

### setLineUnitAfter(double value) {#setLineUnitAfter-double}
```
public void setLineUnitAfter(double value)
```


يضبط مقدار التباعد (بخطوط الشبكة) بعد الفقرات.

 **Examples:** 

يظهر كيفية تغيير مسافات الفقرة والإزاحات.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 ParagraphFormat format = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat();

 // Below are five different spacing options, along with the properties that their configuration indirectly affects.
 // 1 -  Left indent:
 Assert.assertEquals(format.getLeftIndent(), 0.0d);

 format.setCharacterUnitLeftIndent(10.0);

 Assert.assertEquals(format.getLeftIndent(), 120.0d);

 // 2 -  Right indent:
 Assert.assertEquals(format.getRightIndent(), 0.0d);

 format.setCharacterUnitRightIndent(-5.5);

 Assert.assertEquals(format.getRightIndent(), -66.0d);

 // 3 -  Hanging indent:
 Assert.assertEquals(format.getFirstLineIndent(), 0.0d);

 format.setCharacterUnitFirstLineIndent(20.3);

 Assert.assertEquals(format.getFirstLineIndent(), 243.59d, 0.1d);

 // 4 -  Line spacing before paragraphs:
 Assert.assertEquals(format.getSpaceBefore(), 0.0d);

 format.setLineUnitBefore(5.1);

 Assert.assertEquals(format.getSpaceBefore(), 61.1d, 0.1d);

 // 5 -  Line spacing after paragraphs:
 Assert.assertEquals(format.getSpaceAfter(), 0.0d);

 format.setLineUnitAfter(10.9);

 Assert.assertEquals(format.getSpaceAfter(), 130.8d, 0.1d);

 builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
         "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
 builder.write("\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5" +
         "\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | double | كمية التباعد (بالخطوط الشبكية) بعد الفقرات. |

### setLineUnitBefore(double value) {#setLineUnitBefore-double}
```
public void setLineUnitBefore(double value)
```


يضبط مقدار التباعد (بخطوط الشبكة) قبل الفقرات.

 **Examples:** 

يظهر كيفية تغيير مسافات الفقرة والإزاحات.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 ParagraphFormat format = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat();

 // Below are five different spacing options, along with the properties that their configuration indirectly affects.
 // 1 -  Left indent:
 Assert.assertEquals(format.getLeftIndent(), 0.0d);

 format.setCharacterUnitLeftIndent(10.0);

 Assert.assertEquals(format.getLeftIndent(), 120.0d);

 // 2 -  Right indent:
 Assert.assertEquals(format.getRightIndent(), 0.0d);

 format.setCharacterUnitRightIndent(-5.5);

 Assert.assertEquals(format.getRightIndent(), -66.0d);

 // 3 -  Hanging indent:
 Assert.assertEquals(format.getFirstLineIndent(), 0.0d);

 format.setCharacterUnitFirstLineIndent(20.3);

 Assert.assertEquals(format.getFirstLineIndent(), 243.59d, 0.1d);

 // 4 -  Line spacing before paragraphs:
 Assert.assertEquals(format.getSpaceBefore(), 0.0d);

 format.setLineUnitBefore(5.1);

 Assert.assertEquals(format.getSpaceBefore(), 61.1d, 0.1d);

 // 5 -  Line spacing after paragraphs:
 Assert.assertEquals(format.getSpaceAfter(), 0.0d);

 format.setLineUnitAfter(10.9);

 Assert.assertEquals(format.getSpaceAfter(), 130.8d, 0.1d);

 builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
         "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
 builder.write("\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5" +
         "\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | double | كمية التباعد (بالخطوط الشبكية) قبل الفقرات. |

### setLinesToDrop(int value) {#setLinesToDrop-int}
```
public void setLinesToDrop(int value)
```


يضبط عدد أسطر نص الفقرة المستخدمة لحساب ارتفاع الحرف الأول الكبير.

 **Examples:** 

يظهر كيفية ضبط حجم الحرف الأول الكبير.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Modify the "LinesToDrop" property to designate a paragraph as a drop cap,
 // which will turn it into a large capital letter that will decorate the next paragraph.
 // Give this property a value of 4 to give the drop cap the height of four text lines.
 builder.getParagraphFormat().setLinesToDrop(4);
 builder.writeln("H");

 // Reset the "LinesToDrop" property to 0 to turn the next paragraph into an ordinary paragraph.
 // The text in this paragraph will wrap around the drop cap.
 builder.getParagraphFormat().setLinesToDrop(0);
 builder.writeln("ello world!");

 doc.save(getArtifactsDir() + "ParagraphFormat.LinesToDrop.odt");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | int | عدد أسطر نص الفقرة المستخدمة لحساب ارتفاع الحرف الأول المتناثر. |

### setMirrorIndents(boolean value) {#setMirrorIndents-boolean}
```
public void setMirrorIndents(boolean value)
```


يضبط علامة تشير إلى ما إذا كانت الإزاحات اليسرى واليمنى ذات عرض متساوٍ.

 **Examples:** 

يظهر كيفية جعل الهوامش اليسرى واليمنى متساوية.

```

 Document doc = new Document(getMyDir() + "Document.docx");
 ParagraphFormat format = doc.getFirstSection().getBody().getParagraphs().get(0).getParagraphFormat();

 format.setMirrorIndents(true);

 doc.save(getArtifactsDir() + "ParagraphFormat.MirrorIndents.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | علامة تشير إلى ما إذا كانت المسافات البادئة اليسرى واليمنى ذات عرض متساوٍ. |

### setNoSpaceBetweenParagraphsOfSameStyle(boolean value) {#setNoSpaceBetweenParagraphsOfSameStyle-boolean}
```
public void setNoSpaceBetweenParagraphsOfSameStyle(boolean value)
```


عند true، سيتم تجاهل [getSpaceBefore()](../../com.aspose.words/paragraphformat/\#getSpaceBefore) / [setSpaceBefore(double)](../../com.aspose.words/paragraphformat/\#setSpaceBefore-double) و [getSpaceAfter()](../../com.aspose.words/paragraphformat/\#getSpaceAfter) / [setSpaceAfter(double)](../../com.aspose.words/paragraphformat/\#setSpaceAfter-double) بين الفقرات ذات النمط نفسه.

 **Remarks:** 

هذا الإعداد لا يؤثر إلا عندما يُطبق على نمط فقرة. إذا تم تطبيقه مباشرة على فقرة، فلن يكون له أي تأثير.

 **Examples:** 

يظهر كيفية تطبيق عدم وجود تباعد بين الفقرات ذات النمط نفسه.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Apply a large amount of spacing before and after paragraphs that this builder will create.
 builder.getParagraphFormat().setSpaceBefore(24.0);
 builder.getParagraphFormat().setSpaceAfter(24.0);

 // Set the "NoSpaceBetweenParagraphsOfSameStyle" flag to "true" to apply
 // no spacing between paragraphs with the same style, which will group similar paragraphs.
 // Leave the "NoSpaceBetweenParagraphsOfSameStyle" flag as "false"
 // to evenly apply spacing to every paragraph.
 builder.getParagraphFormat().setNoSpaceBetweenParagraphsOfSameStyle(noSpaceBetweenParagraphsOfSameStyle);

 builder.getParagraphFormat().setStyle(doc.getStyles().get("Normal"));
 builder.writeln(MessageFormat.format("Paragraph in the \"{0}\" style.", builder.getParagraphFormat().getStyle().getName()));
 builder.writeln(MessageFormat.format("Paragraph in the \"{0}\" style.", builder.getParagraphFormat().getStyle().getName()));
 builder.writeln(MessageFormat.format("Paragraph in the \"{0}\" style.", builder.getParagraphFormat().getStyle().getName()));
 builder.getParagraphFormat().setStyle(doc.getStyles().get("Quote"));
 builder.writeln(MessageFormat.format("Paragraph in the \"{0}\" style.", builder.getParagraphFormat().getStyle().getName()));
 builder.writeln(MessageFormat.format("Paragraph in the \"{0}\" style.", builder.getParagraphFormat().getStyle().getName()));
 builder.getParagraphFormat().setStyle(doc.getStyles().get("Normal"));
 builder.writeln(MessageFormat.format("Paragraph in the \"{0}\" style.", builder.getParagraphFormat().getStyle().getName()));
 builder.writeln(MessageFormat.format("Paragraph in the \"{0}\" style.", builder.getParagraphFormat().getStyle().getName()));

 doc.save(getArtifactsDir() + "ParagraphFormat.ParagraphSpacingSameStyle.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | القيمة المنطقية المقابلة. |

### setOutlineLevel(int value) {#setOutlineLevel-int}
```
public void setOutlineLevel(int value)
```


يحدد مستوى المخطط للفقرة في المستند.

 **Examples:** 

يوضح كيفية تكوين مستويات مخطط الفقرات لإنشاء نص قابل للطي.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Each paragraph has an OutlineLevel, which could be any number from 1 to 9, or at the default "BodyText" value.
 // Setting the property to one of the numbered values will show an arrow to the left
 // of the beginning of the paragraph.
 builder.getParagraphFormat().setOutlineLevel(OutlineLevel.LEVEL_1);
 builder.writeln("Paragraph outline level 1.");

 // Level 1 is the topmost level. If there is a paragraph with a lower level below a paragraph with a higher level,
 // collapsing the higher-level paragraph will collapse the lower level paragraph.
 builder.getParagraphFormat().setOutlineLevel(OutlineLevel.LEVEL_2);
 builder.writeln("Paragraph outline level 2.");

 // Two paragraphs of the same level will not collapse each other,
 // and the arrows do not collapse the paragraphs they point to.
 builder.getParagraphFormat().setOutlineLevel(OutlineLevel.LEVEL_3);
 builder.writeln("Paragraph outline level 3.");
 builder.writeln("Paragraph outline level 3.");

 // The default "BodyText" value is the lowest, which a paragraph of any level can collapse.
 builder.getParagraphFormat().setOutlineLevel(OutlineLevel.BODY_TEXT);
 builder.writeln("Paragraph at main text level.");

 doc.save(getArtifactsDir() + "ParagraphFormat.ParagraphOutlineLevel.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| value | int | القيمة الصحيحة (int) المقابلة. يجب أن تكون القيمة واحدة من ثوابت [OutlineLevel](../../com.aspose.words/outlinelevel/). |

### setPageBreakBefore(boolean value) {#setPageBreakBefore-boolean}
```
public void setPageBreakBefore(boolean value)
```


صحيح إذا تم فرض فاصل صفحة قبل الفقرة.

 **Examples:** 

يظهر كيفية إنشاء فقرات مع فواصل صفحات في البداية.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Set this flag to "true" to apply a page break to each paragraph's beginning
 // that the document builder will create under this ParagraphFormat configuration.
 // The first paragraph will not receive a page break.
 // Leave this flag as "false" to start each new paragraph on the same page
 // as the previous, provided there is sufficient space.
 builder.getParagraphFormat().setPageBreakBefore(pageBreakBefore);

 builder.writeln("Paragraph 1.");
 builder.writeln("Paragraph 2.");

 LayoutCollector layoutCollector = new LayoutCollector(doc);
 ParagraphCollection paragraphs = doc.getFirstSection().getBody().getParagraphs();

 if (pageBreakBefore) {
     Assert.assertEquals(1, layoutCollector.getStartPageIndex(paragraphs.get(0)));
     Assert.assertEquals(2, layoutCollector.getStartPageIndex(paragraphs.get(1)));
 } else {
     Assert.assertEquals(1, layoutCollector.getStartPageIndex(paragraphs.get(0)));
     Assert.assertEquals(1, layoutCollector.getStartPageIndex(paragraphs.get(1)));
 }

 doc.save(getArtifactsDir() + "ParagraphFormat.PageBreakBefore.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | القيمة المنطقية المقابلة. |

### setRightIndent(double value) {#setRightIndent-double}
```
public void setRightIndent(double value)
```


يضبط القيمة (بالنقاط) التي تمثل الإزاحة اليمنى للفقرة.

 **Examples:** 

يظهر كيفية تكوين تنسيق الفقرة لإنشاء نص غير مركزي.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Center all text that the document builder writes, and set up indents.
 // The indent configuration below will create a body of text that will sit asymmetrically on the page.
 // The "center" that we align the text to will be the middle of the body of text, not the middle of the page.
 ParagraphFormat paragraphFormat = builder.getParagraphFormat();
 paragraphFormat.setAlignment(ParagraphAlignment.CENTER);
 paragraphFormat.setLeftIndent(100.0);
 paragraphFormat.setRightIndent(50.0);
 paragraphFormat.setSpaceAfter(25.0);

 builder.writeln(
         "This paragraph demonstrates how left and right indentation affects word wrapping.");
 builder.writeln(
         "The space between the above paragraph and this one depends on the DocumentBuilder's paragraph format.");

 doc.save(getArtifactsDir() + "DocumentBuilder.SetParagraphFormatting.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | double | القيمة (بالنقاط) التي تمثل المسافة البادئة اليمنى للفقرة. |

### setSnapToGrid(boolean value) {#setSnapToGrid-boolean}
```
public void setSnapToGrid(boolean value)
```


يحدد ما إذا كان يجب على الفقرة الحالية استخدام إعدادات خطوط شبكة المستند لكل صفحة عند تنسيق المحتوى داخل الفقرة.

 **Examples:** 

يظهر كيفية تحديد حد لعدد الأسطر التي قد يحتويها كل صفحة.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Enable pitching, and then use it to set the number of lines per page in this section.
 // A large enough font size will push some lines down onto the next page to avoid overlapping characters.
 builder.getPageSetup().setLayoutMode(SectionLayoutMode.LINE_GRID);
 builder.getPageSetup().setLinesPerPage(15);

 builder.getParagraphFormat().setSnapToGrid(true);

 for (int i = 0; i < 30; i++)
     builder.write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ");

 doc.save(getArtifactsDir() + "PageSetup.LinesPerPage.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | القيمة المنطقية المقابلة. |

### setSpaceAfter(double value) {#setSpaceAfter-double}
```
public void setSpaceAfter(double value)
```


يضبط مقدار التباعد (بالنقاط) بعد الفقرة.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | double | كمية التباعد (بالنقاط) بعد الفقرة. |

### setSpaceAfterAuto(boolean value) {#setSpaceAfterAuto-boolean}
```
public void setSpaceAfterAuto(boolean value)
```


صحيح إذا تم تعيين مقدار المسافة بعد الفقرة تلقائيًا.

 **Remarks:** 

عند ضبطه على  true , يتجاوز تأثير [getSpaceAfter()](../../com.aspose.words/paragraphformat/\#getSpaceAfter) / [setSpaceAfter(double)](../../com.aspose.words/paragraphformat/\#setSpaceAfter-double).

عند ضبط مسافة الفقرة قبل وبعد إلى تلقائي، يضيف Microsoft Word تباعدًا قدره 14 نقطة بين الفقرات تلقائيًا وفقًا للقواعد التالية:

 *  Normally, spacing is added after all paragraphs.
 *  In a bulleted or numbered list, spacing is added only after the last item in the list. Spacing is not added between the list items.
 *  In a nested bulleted or numbered list spacing is not added.
 *  Spacing is normally added after a table.
 *  Spacing is not added after a table if it is the last block in a table cell.
 *  Spacing is not added after the last paragraph in a table cell.

 **Examples:** 

يظهر كيفية ضبط تباعد الفقرة التلقائي.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Apply a large amount of spacing before and after paragraphs that this builder will create.
 builder.getParagraphFormat().setSpaceBefore(24.0);
 builder.getParagraphFormat().setSpaceAfter(24.0);

 // Set these flags to "true" to apply automatic spacing,
 // effectively ignoring the spacing in the properties we set above.
 // Leave them as "false" will apply our custom paragraph spacing.
 builder.getParagraphFormat().setSpaceAfterAuto(autoSpacing);
 builder.getParagraphFormat().setSpaceBeforeAuto(autoSpacing);

 // Insert two paragraphs that will have spacing above and below them and save the document.
 builder.writeln("Paragraph 1.");
 builder.writeln("Paragraph 2.");

 doc.save(getArtifactsDir() + "ParagraphFormat.ParagraphSpacingAuto.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | القيمة المنطقية المقابلة. |

### setSpaceBefore(double value) {#setSpaceBefore-double}
```
public void setSpaceBefore(double value)
```


يضبط مقدار المسافة (بالنقاط) قبل الفقرة.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | double | كمية التباعد (بالنقاط) قبل الفقرة. |

### setSpaceBeforeAuto(boolean value) {#setSpaceBeforeAuto-boolean}
```
public void setSpaceBeforeAuto(boolean value)
```


صحيح إذا تم تعيين مقدار المسافة قبل الفقرة تلقائيًا.

 **Remarks:** 

عند ضبطه على  true , يتجاوز تأثير [getSpaceBefore()](../../com.aspose.words/paragraphformat/\#getSpaceBefore) / [setSpaceBefore(double)](../../com.aspose.words/paragraphformat/\#setSpaceBefore-double).

عند ضبط مسافة الفقرة قبل وبعد إلى تلقائي، يضيف Microsoft Word تباعدًا قدره 14 نقطة بين الفقرات تلقائيًا وفقًا للقواعد التالية:

 *  Normally, spacing is added after all paragraphs.
 *  In a bulleted or numbered list, spacing is added only after the last item in the list. Spacing is not added between the list items.
 *  In a nested bulleted or numbered list spacing is not added.
 *  Spacing is normally added after a table.
 *  Spacing is not added after a table if it is the last block in a table cell.
 *  Spacing is not added after the last paragraph in a table cell.

 **Examples:** 

يظهر كيفية ضبط تباعد الفقرة التلقائي.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Apply a large amount of spacing before and after paragraphs that this builder will create.
 builder.getParagraphFormat().setSpaceBefore(24.0);
 builder.getParagraphFormat().setSpaceAfter(24.0);

 // Set these flags to "true" to apply automatic spacing,
 // effectively ignoring the spacing in the properties we set above.
 // Leave them as "false" will apply our custom paragraph spacing.
 builder.getParagraphFormat().setSpaceAfterAuto(autoSpacing);
 builder.getParagraphFormat().setSpaceBeforeAuto(autoSpacing);

 // Insert two paragraphs that will have spacing above and below them and save the document.
 builder.writeln("Paragraph 1.");
 builder.writeln("Paragraph 2.");

 doc.save(getArtifactsDir() + "ParagraphFormat.ParagraphSpacingAuto.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | القيمة المنطقية المقابلة. |

### setStyle(Style value) {#setStyle-com.aspose.words.Style}
```
public void setStyle(Style value)
```


يضبط نمط الفقرة المطبق على هذا التنسيق.

 **Examples:** 

يوضح كيفية إنشاء واستخدام نمط فقرة مع تنسيق القوائم.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create a custom paragraph style.
 Style style = doc.getStyles().add(StyleType.PARAGRAPH, "MyStyle1");
 style.getFont().setSize(24.0);
 style.getFont().setName("Verdana");
 style.getParagraphFormat().setSpaceAfter(12.0);

 // Create a list and make sure the paragraphs that use this style will use this list.
 style.getListFormat().setList(doc.getLists().add(ListTemplate.BULLET_DEFAULT));
 style.getListFormat().setListLevelNumber(0);

 // Apply the paragraph style to the document builder's current paragraph, and then add some text.
 builder.getParagraphFormat().setStyle(style);
 builder.writeln("Hello World: MyStyle1, bulleted list.");

 // Change the document builder's style to one that has no list formatting and write another paragraph.
 builder.getParagraphFormat().setStyle(doc.getStyles().get("Normal"));
 builder.writeln("Hello World: Normal.");

 builder.getDocument().save(getArtifactsDir() + "Styles.ParagraphStyleBulletedList.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| value | [Style](../../com.aspose.words/style/) | نمط الفقرة المطبق على هذا التنسيق. |

### setStyleIdentifier(int value) {#setStyleIdentifier-int}
```
public void setStyleIdentifier(int value)
```


يضبط معرف النمط المستقل عن اللغة لنمط الفقرة المطبق على هذا التنسيق.

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
| value | int | معرّف النمط المستقل عن اللغة لنمط الفقرة المطبق على هذا التنسيق. يجب أن تكون القيمة واحدة من ثوابت [StyleIdentifier](../../com.aspose.words/styleidentifier/). |

### setStyleName(String value) {#setStyleName-java.lang.String}
```
public void setStyleName(String value)
```


يضبط اسم نمط الفقرة المطبق على هذا التنسيق.

 **Examples:** 

يوضح كيفية إنشاء مستند Aspose.Words يدوياً.

```

 Document doc = new Document();

 // A blank document contains one section, one body and one paragraph.
 // Call the "RemoveAllChildren" method to remove all those nodes,
 // and end up with a document node with no children.
 doc.removeAllChildren();

 // This document now has no composite child nodes that we can add content to.
 // If we wish to edit it, we will need to repopulate its node collection.
 // First, create a new section, and then append it as a child to the root document node.
 Section section = new Section(doc);
 doc.appendChild(section);

 // Set some page setup properties for the section.
 section.getPageSetup().setSectionStart(SectionStart.NEW_PAGE);
 section.getPageSetup().setPaperSize(PaperSize.LETTER);

 // A section needs a body, which will contain and display all its contents
 // on the page between the section's header and footer.
 Body body = new Body(doc);
 section.appendChild(body);

 // Create a paragraph, set some formatting properties, and then append it as a child to the body.
 Paragraph para = new Paragraph(doc);

 para.getParagraphFormat().setStyleName("Heading 1");
 para.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);

 body.appendChild(para);

 // Finally, add some content to do the document. Create a run,
 // set its appearance and contents, and then append it as a child to the paragraph.
 Run run = new Run(doc);
 run.setText("Hello World!");
 run.getFont().setColor(Color.RED);
 para.appendChild(run);

 Assert.assertEquals("Hello World!", doc.getText().trim());

 doc.save(getArtifactsDir() + "Section.CreateManually.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.lang.String | اسم نمط الفقرة المطبق على هذا التنسيق. |

### setSuppressAutoHyphens(boolean value) {#setSuppressAutoHyphens-boolean}
```
public void setSuppressAutoHyphens(boolean value)
```


يحدد ما إذا كان يجب إعفاء الفقرة الحالية من أي تجزئة تُطبق في إعدادات المستند.

 **Examples:** 

يظهر كيفية إلغاء تجزئة الكلمات لفقرة.

```

 Hyphenation.registerDictionary("de-CH", getMyDir() + "hyph_de_CH.dic");

 Assert.assertTrue(Hyphenation.isDictionaryRegistered("de-CH"));

 // Open a document containing text with a locale matching that of our dictionary.
 // When we save this document to a fixed page save format, its text will have hyphenation.
 Document doc = new Document(getMyDir() + "German text.docx");

 // We can set the "SuppressAutoHyphens" property to "true" to disable hyphenation
 // for a specific paragraph while keeping it enabled for the rest of the document.
 // The default value for this property is "false",
 // which means every paragraph by default uses hyphenation if any is available.
 doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat().setSuppressAutoHyphens(suppressAutoHyphens);

 doc.save(getArtifactsDir() + "ParagraphFormat.SuppressHyphens.pdf");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | القيمة المنطقية المقابلة. |

### setSuppressLineNumbers(boolean value) {#setSuppressLineNumbers-boolean}
```
public void setSuppressLineNumbers(boolean value)
```


يحدد ما إذا كان يجب إعفاء أسطر الفقرة الحالية من ترقيم الأسطر الذي يُطبق في القسم الأب.

 **Examples:** 

يظهر كيفية تمكين ترقيم الأسطر لقسم.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // We can use the section's PageSetup object to display numbers to the left of the section's text lines.
 // This is the same behavior as a List object,
 // but it covers the entire section and does not modify the text in any way.
 // Our section will restart the numbering on each new page from 1 and display the number,
 // if it is a multiple of 3, at 50pt to the left of the line.
 PageSetup pageSetup = builder.getPageSetup();
 pageSetup.setLineStartingNumber(1);
 pageSetup.setLineNumberCountBy(3);
 pageSetup.setLineNumberRestartMode(LineNumberRestartMode.RESTART_PAGE);
 pageSetup.setLineNumberDistanceFromText(50.0d);

 for (int i = 1; i <= 25; i++)
     builder.writeln(MessageFormat.format("Line {0}.", i));

 // The line counter will skip any paragraph with the "SuppressLineNumbers" flag set to "true".
 // This paragraph is on the 15th line, which is a multiple of 3, and thus would normally display a line number.
 // The section's line counter will also ignore this line, treat the next line as the 15th,
 // and continue the count from that point onward.
 doc.getFirstSection().getBody().getParagraphs().get(14).getParagraphFormat().setSuppressLineNumbers(true);

 doc.save(getArtifactsDir() + "PageSetup.LineNumbers.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | القيمة المنطقية المقابلة. |

### setWidowControl(boolean value) {#setWidowControl-boolean}
```
public void setWidowControl(boolean value)
```


صحيح إذا كان يجب أن تبقى السطران الأول والأخير في الفقرة على نفس الصفحة مع باقي الفقرة.

 **Examples:** 

يظهر كيفية تمكين التحكم في القُرّات/الأيتام لفقرة.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // When we write the text that does not fit onto one page, one line may spill over onto the next page.
 // The single line that ends up on the next page is called an "Orphan",
 // and the previous line where the orphan broke off is called a "Widow".
 // We can fix orphans and widows by rearranging text via font size, spacing, or page margins.
 // If we wish to preserve our document's dimensions, we can set this flag to "true"
 // to push widows onto the same page as their respective orphans.
 // Leave this flag as "false" will leave widow/orphan pairs in text.
 // Every paragraph has this setting accessible in Microsoft Word via Home -> Paragraph -> Paragraph Settings
 // (button on bottom right hand corner of "Paragraph" tab) -> "Widow/Orphan control".
 builder.getParagraphFormat().setWidowControl(widowControl);

 // Insert text that produces an orphan and a widow.
 builder.getFont().setSize(68.0);
 builder.write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
         "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

 doc.save(getArtifactsDir() + "ParagraphFormat.WidowControl.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | القيمة المنطقية المقابلة. |

### setWordWrap(boolean value) {#setWordWrap-boolean}
```
public void setWordWrap(boolean value)
```


إذا كانت هذه الخاصية  false , يمكن لف النص اللاتيني في وسط كلمة للفقرة الحالية. وإلا يتم لف النص اللاتيني بكلمات كاملة.

 **Examples:** 

يظهر كيفية ضبط خصائص خاصة للطباعة الآسيوية.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 ParagraphFormat format = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat();
 format.setFarEastLineBreakControl(true);
 format.setWordWrap(false);
 format.setHangingPunctuation(true);

 doc.save(getArtifactsDir() + "ParagraphFormat.AsianTypographyProperties.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | القيمة المنطقية المقابلة. |

