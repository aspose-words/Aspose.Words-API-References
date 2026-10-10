---
title: "FindReplaceOptions"
linktitle: "FindReplaceOptions"
second_title: "Aspose.Words لـ Java"
description: "يحدد الخيارات لعمليات البحث/الاستبدال في Java."
type: docs
weight: 314
url: /ar/java/com.aspose.words/findreplaceoptions/
---

**Inheritance:**
java.lang.Object
```
public class FindReplaceOptions
```

يحدد الخيارات لعمليات البحث/الاستبدال.

للتعرف على المزيد، زر مقالة الوثائق [ Find and Replace ][Find and Replace].

 **Examples:** 

يوضح كيفية تبديل حساسية الحالة عند تنفيذ عملية البحث والاستبدال.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Ruby bought a ruby necklace.");

 // We can use a "FindReplaceOptions" object to modify the find-and-replace process.
 FindReplaceOptions options = new FindReplaceOptions();

 // Set the "MatchCase" flag to "true" to apply case sensitivity while finding strings to replace.
 // Set the "MatchCase" flag to "false" to ignore character case while searching for text to replace.
 options.setMatchCase(matchCase);

 doc.getRange().replace("Ruby", "Jade", options);

 Assert.assertEquals(matchCase ? "Jade bought a ruby necklace." : "Jade bought a Jade necklace.",
         doc.getText().trim());
 
```

يوضح كيفية تبديل عمليات البحث والاستبدال التي تقتصر على كلمة مستقلة.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Jackson will meet you in Jacksonville.");

 // We can use a "FindReplaceOptions" object to modify the find-and-replace process.
 FindReplaceOptions options = new FindReplaceOptions();

 // Set the "FindWholeWordsOnly" flag to "true" to replace the found text if it is not a part of another word.
 // Set the "FindWholeWordsOnly" flag to "false" to replace all text regardless of its surroundings.
 options.setFindWholeWordsOnly(findWholeWordsOnly);

 doc.getRange().replace("Jackson", "Louis", options);

 Assert.assertEquals(
         findWholeWordsOnly ? "Louis will meet you in Jacksonville." : "Louis will meet you in Louisville.",
         doc.getText().trim());
 
```


[Find and Replace]: https://docs.aspose.com/words/java/find-and-replace/
## المنشئات

| المنشئ | الوصف |
| --- | --- |
| [FindReplaceOptions()](#FindReplaceOptions) | ينشئ نسخة جديدة من فئة FindReplaceOptions بالإعدادات الافتراضية. |
| [FindReplaceOptions(int direction)](#FindReplaceOptions-int) | يقوم بتهيئة نسخة جديدة من هذه الفئة. |
| [FindReplaceOptions(IReplacingCallback replacingCallback)](#FindReplaceOptions-com.aspose.words.IReplacingCallback) | ينشئ نسخة جديدة من فئة FindReplaceOptions مع رد الاتصال المحدد للاستبدال. |
| [FindReplaceOptions(int direction, IReplacingCallback replacingCallback)](#FindReplaceOptions-int-com.aspose.words.IReplacingCallback) | يقوم بتهيئة نسخة جديدة من هذه الفئة. |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [getApplyFont()](#getApplyFont) | تنسيق النص المطبق على المحتوى الجديد. |
| [getApplyParagraphFormat()](#getApplyParagraphFormat) | تنسيق الفقرة المطبق على المحتوى الجديد. |
| [getDirection()](#getDirection) | يختار الاتجاه للاستبدال. |
| [getFindWholeWordsOnly()](#getFindWholeWordsOnly) | True تشير إلى أن oldValue يجب أن تكون كلمة مستقلة. |
| [getIgnoreDeleted()](#getIgnoreDeleted) | يحصل على قيمة منطقية تشير إلى ما إذا كان يجب تجاهل النص داخل مراجعات الحذف. |
| [getIgnoreFieldCodes()](#getIgnoreFieldCodes) | يحصل على قيمة منطقية تشير إلى ما إذا كان يجب تجاهل النص داخل رموز الحقول. |
| [getIgnoreFields()](#getIgnoreFields) | يحصل على قيمة منطقية تشير إلى ما إذا كان يجب تجاهل النص داخل الحقول. |
| [getIgnoreFootnotes()](#getIgnoreFootnotes) | يحصل على قيمة منطقية تشير إلى ما إذا كان يجب تجاهل الحواشي. |
| [getIgnoreInserted()](#getIgnoreInserted) | يحصل على قيمة منطقية تشير إلى تجاهل النص داخل مراجعات الإدراج. |
| [getIgnoreOfficeMath()](#getIgnoreOfficeMath) | يحصل على قيمة منطقية تشير إلى تجاهل النص داخل OfficeMath/>. |
| [getIgnoreShapes()](#getIgnoreShapes) | يحصل أو يضبط قيمة منطقية تشير إلى تجاهل الأشكال داخل النص. |
| [getIgnoreStructuredDocumentTags()](#getIgnoreStructuredDocumentTags) | يحصل على قيمة منطقية تشير إلى تجاهل محتوى [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag/). |
| [getLegacyMode()](#getLegacyMode) | يحصل على قيمة منطقية تشير إلى استخدام خوارزمية البحث/الاستبدال القديمة. |
| [getMatchCase()](#getMatchCase) | True تشير إلى مقارنة حساسة لحالة الأحرف، false تشير إلى مقارنة غير حساسة لحالة الأحرف. |
| [getReplacementFormat()](#getReplacementFormat) | يحدد تنسيق الاستبدال. |
| [getReplacingCallback()](#getReplacingCallback) | الطريقة المعرفة من قبل المستخدم التي تُستدعى قبل كل حدوث استبدال. |
| [getSmartParagraphBreakReplacement()](#getSmartParagraphBreakReplacement) | يحصل أو يضبط قيمة منطقية تشير إلى السماح باستبدال فاصل الفقرة عندما لا يوجد فقرة شقيقة تالية. |
| [getUseLegacyOrder()](#getUseLegacyOrder) | True تشير إلى أن البحث النصي يتم بشكل متسلسل من الأعلى إلى الأسفل مع مراعاة صناديق النص. |
| [getUseSubstitutions()](#getUseSubstitutions) | يحصل على قيمة منطقية تشير إلى ما إذا كان يجب التعرف على الاستبدالات واستخدامها داخل أنماط الاستبدال. |
| [setDirection(int value)](#setDirection-int) | يختار الاتجاه للاستبدال. |
| [setFindWholeWordsOnly(boolean value)](#setFindWholeWordsOnly-boolean) | True تشير إلى أن oldValue يجب أن تكون كلمة مستقلة. |
| [setIgnoreDeleted(boolean value)](#setIgnoreDeleted-boolean) | يضبط قيمة منطقية تشير إلى تجاهل النص داخل مراجعات الحذف. |
| [setIgnoreFieldCodes(boolean value)](#setIgnoreFieldCodes-boolean) | يضبط قيمة منطقية تشير إلى تجاهل النص داخل رموز الحقول. |
| [setIgnoreFields(boolean value)](#setIgnoreFields-boolean) | يضبط قيمة منطقية تشير إلى تجاهل النص داخل الحقول. |
| [setIgnoreFootnotes(boolean value)](#setIgnoreFootnotes-boolean) | يضبط قيمة منطقية تشير إلى تجاهل الحواشي السفلية. |
| [setIgnoreInserted(boolean value)](#setIgnoreInserted-boolean) | يضبط قيمة منطقية تشير إلى تجاهل النص داخل مراجعات الإدراج. |
| [setIgnoreOfficeMath(boolean value)](#setIgnoreOfficeMath-boolean) | يضبط قيمة منطقية تشير إلى تجاهل النص داخل OfficeMath/>. |
| [setIgnoreShapes(boolean value)](#setIgnoreShapes-boolean) | يحصل أو يضبط قيمة منطقية تشير إلى تجاهل الأشكال داخل النص. |
| [setIgnoreStructuredDocumentTags(boolean value)](#setIgnoreStructuredDocumentTags-boolean) | يضبط قيمة منطقية تشير إلى تجاهل محتوى [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag/). |
| [setLegacyMode(boolean value)](#setLegacyMode-boolean) | يضبط قيمة منطقية تشير إلى استخدام خوارزمية البحث/الاستبدال القديمة. |
| [setMatchCase(boolean value)](#setMatchCase-boolean) | True تشير إلى مقارنة حساسة لحالة الأحرف، false تشير إلى مقارنة غير حساسة لحالة الأحرف. |
| [setReplacementFormat(int value)](#setReplacementFormat-int) | يحدد تنسيق الاستبدال. |
| [setReplacingCallback(IReplacingCallback value)](#setReplacingCallback-com.aspose.words.IReplacingCallback) | الطريقة المعرفة من قبل المستخدم التي تُستدعى قبل كل حدوث استبدال. |
| [setSmartParagraphBreakReplacement(boolean value)](#setSmartParagraphBreakReplacement-boolean) | يحصل أو يضبط قيمة منطقية تشير إلى السماح باستبدال فاصل الفقرة عندما لا يوجد فقرة شقيقة تالية. |
| [setUseLegacyOrder(boolean value)](#setUseLegacyOrder-boolean) | True تشير إلى أن البحث النصي يتم بشكل متسلسل من الأعلى إلى الأسفل مع مراعاة صناديق النص. |
| [setUseSubstitutions(boolean value)](#setUseSubstitutions-boolean) | يضبط قيمة منطقية تشير إلى ما إذا كان يجب التعرف على الاستبدالات واستخدامها داخل أنماط الاستبدال. |
### FindReplaceOptions() {#FindReplaceOptions}
```
public FindReplaceOptions()
```


ينشئ نسخة جديدة من فئة FindReplaceOptions بالإعدادات الافتراضية.

 **Examples:** 

يوضح كيفية التعرف على الاستبدالات واستخدامها داخل أنماط الاستبدال.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.write("Jason gave money to Paul.");

 String regex = "([A-z]+) gave money to ([A-z]+)";

 FindReplaceOptions options = new FindReplaceOptions();
 options.setUseSubstitutions(true);

 // Using legacy mode does not support many advanced features, so we need to set it to 'false'.
 options.setLegacyMode(false);

 doc.getRange().replace(Pattern.compile(regex), "$2 took money from $1", options);

 Assert.assertEquals(doc.getText(), "Paul took money from Jason.\f");
 
```

### FindReplaceOptions(int direction) {#FindReplaceOptions-int}
```
public FindReplaceOptions(int direction)
```


يقوم بتهيئة نسخة جديدة من هذه الفئة.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| direction | int |  |

### FindReplaceOptions(IReplacingCallback replacingCallback) {#FindReplaceOptions-com.aspose.words.IReplacingCallback}
```
public FindReplaceOptions(IReplacingCallback replacingCallback)
```


ينشئ نسخة جديدة من فئة FindReplaceOptions مع رد الاتصال المحدد للاستبدال.

 **Examples:** 

يوضح كيفية تتبع الترتيب الذي تتنقل فيه عملية استبدال النص عبر العقد.

```

 public void order(boolean differentFirstPageHeaderFooter) throws Exception {
     Document doc = new Document(getMyDir() + "Header and footer types.docx");

     Section firstPageSection = doc.getFirstSection();

     ReplaceLog logger = new ReplaceLog();
     FindReplaceOptions options = new FindReplaceOptions();
     {
         options.setReplacingCallback(logger);
     }

     // Using a different header/footer for the first page will affect the search order.
     firstPageSection.getPageSetup().setDifferentFirstPageHeaderFooter(differentFirstPageHeaderFooter);
     doc.getRange().replace(Pattern.compile("(header|footer)"), "", options);

     if (differentFirstPageHeaderFooter)
         Assert.assertEquals("First headerFirst footerSecond headerSecond footerThird headerThird footer",
                 logger.Text().replace("\r", ""));
     else
         Assert.assertEquals("Third headerFirst headerThird footerFirst footerSecond headerSecond footer",
                 logger.Text().replace("\r", ""));
 }

 public static Object[][] orderDataProvider() throws Exception {
     return new Object[][]
             {
                     {false},
                     {true},
             };
 }

 /// 
 /// During a find-and-replace operation, records the contents of every node that has text that the operation 'finds',
 /// in the state it is in before the replacement takes place.
 /// This will display the order in which the text replacement operation traverses nodes.
 /// 
 private static class ReplaceLog implements IReplacingCallback {
     public int replacing(ReplacingArgs args) {
         mTextBuilder.append(args.getMatchNode().getText());
         return ReplaceAction.SKIP;
     }

     public String Text() {
         return mTextBuilder.toString();
     }

     private final StringBuilder mTextBuilder = new StringBuilder();
 }
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| replacingCallback | [IReplacingCallback](../../com.aspose.words/ireplacingcallback/) | دالة الاستدعاء التي تُستخدم لاستبدال النص المكتشف. |

### FindReplaceOptions(int direction, IReplacingCallback replacingCallback) {#FindReplaceOptions-int-com.aspose.words.IReplacingCallback}
```
public FindReplaceOptions(int direction, IReplacingCallback replacingCallback)
```


يقوم بتهيئة نسخة جديدة من هذه الفئة.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| direction | int |  |
| replacingCallback | [IReplacingCallback](../../com.aspose.words/ireplacingcallback/) |  |

### getApplyFont() {#getApplyFont}
```
public Font getApplyFont()
```


تنسيق النص المطبق على المحتوى الجديد.

 **Examples:** 

يوضح كيفية تطبيق خط مختلف على المحتوى الجديد عبر FindReplaceOptions.

```

 public void convertNumbersToHexadecimal() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     builder.getFont().setName("Arial");
     builder.writeln("Numbers that the find-and-replace operation will convert to hexadecimal and highlight:\n" +
             "123, 456, 789 and 17379.");

     // We can use a "FindReplaceOptions" object to modify the find-and-replace process.
     FindReplaceOptions options = new FindReplaceOptions();

     // Set the "HighlightColor" property to a background color that we want to apply to the operation's resulting text.
     options.getApplyFont().setHighlightColor(Color.GRAY);

     NumberHexer numberHexer = new NumberHexer();
     options.setReplacingCallback(numberHexer);

     int replacementCount = doc.getRange().replace(Pattern.compile("[0-9]+"), "", options);

     System.out.println(numberHexer.getLog());

     Assert.assertEquals(4, replacementCount);
     Assert.assertEquals("Numbers that the find-and-replace operation will convert to hexadecimal and highlight:\r" +
             "0x123, 0x456, 0x789 and 0x17,379.", doc.getText().trim());
 }

 /// 
 /// Replaces numeric find-and-replacement matches with their hexadecimal equivalents.
 /// Maintains a log of every replacement.
 /// 
 private static class NumberHexer implements IReplacingCallback {
     public int replacing(ReplacingArgs args) {
         mCurrentReplacementNumber++;

         int number = Integer.parseInt(args.getMatch().group(0));

         args.setReplacement(MessageFormat.format("0x{0}", number));

         mLog.append(MessageFormat.format("Match #{0}", mCurrentReplacementNumber));
         mLog.append(MessageFormat.format("\tOriginal value:\t{0}", args.getMatch().group(0)));
         mLog.append(MessageFormat.format("\tReplacement:\t{0}", args.getReplacement()));
         mLog.append(MessageFormat.format("\tOffset in parent {0} node:\t{1}", args.getMatchNode().getNodeType(), args.getMatchOffset()));

         return ReplaceAction.REPLACE;
     }

     public String getLog() {
         return mLog.toString();
     }

     private int mCurrentReplacementNumber;
     private final StringBuilder mLog = new StringBuilder();
 }
 
```

**Returns:**
[Font](../../com.aspose.words/font/) - The corresponding [Font](../../com.aspose.words/font/) value.
### getApplyParagraphFormat() {#getApplyParagraphFormat}
```
public ParagraphFormat getApplyParagraphFormat()
```


تنسيق الفقرة المطبق على المحتوى الجديد.

 **Examples:** 

يوضح كيفية إضافة تنسيق إلى الفقرات التي وجدت فيها عملية البحث والاستبدال تطابقات.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Every paragraph that ends with a full stop like this one will be right aligned.");
 builder.writeln("This one will not!");
 builder.write("This one also will.");

 ParagraphCollection paragraphs = doc.getFirstSection().getBody().getParagraphs();

 Assert.assertEquals(ParagraphAlignment.LEFT, paragraphs.get(0).getParagraphFormat().getAlignment());
 Assert.assertEquals(ParagraphAlignment.LEFT, paragraphs.get(1).getParagraphFormat().getAlignment());
 Assert.assertEquals(ParagraphAlignment.LEFT, paragraphs.get(2).getParagraphFormat().getAlignment());

 // We can use a "FindReplaceOptions" object to modify the find-and-replace process.
 FindReplaceOptions options = new FindReplaceOptions();

 // Set the "Alignment" property to "ParagraphAlignment.Right" to right-align every paragraph
 // that contains a match that the find-and-replace operation finds.
 options.getApplyParagraphFormat().setAlignment(ParagraphAlignment.RIGHT);

 // Replace every full stop that is right before a paragraph break with an exclamation point.
 int count = doc.getRange().replace(".&p", "!&p", options);

 Assert.assertEquals(2, count);
 Assert.assertEquals(ParagraphAlignment.RIGHT, paragraphs.get(0).getParagraphFormat().getAlignment());
 Assert.assertEquals(ParagraphAlignment.LEFT, paragraphs.get(1).getParagraphFormat().getAlignment());
 Assert.assertEquals(ParagraphAlignment.RIGHT, paragraphs.get(2).getParagraphFormat().getAlignment());
 Assert.assertEquals("Every paragraph that ends with a full stop like this one will be right aligned!\r" +
         "This one will not!\r" +
         "This one also will!", doc.getText().trim());
 
```

**Returns:**
[ParagraphFormat](../../com.aspose.words/paragraphformat/) - The corresponding [ParagraphFormat](../../com.aspose.words/paragraphformat/) value.
### getDirection() {#getDirection}
```
public int getDirection()
```


يحدد الاتجاه للاستبدال. القيمة الافتراضية هي [FindReplaceDirection.FORWARD](../../com.aspose.words/findreplacedirection/\#FORWARD).

 **Examples:** 

يعرض كيفية تحديد الاتجاه الذي ينتقل فيه عملية البحث والاستبدال عبر المستند.

```

 public void direction(int findReplaceDirection) throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Insert three runs which we can search for using a regex pattern.
     // Place one of those runs inside a text box.
     builder.writeln("Match 1.");
     builder.writeln("Match 2.");
     builder.writeln("Match 3.");
     builder.writeln("Match 4.");

     // We can use a "FindReplaceOptions" object to modify the find-and-replace process.
     FindReplaceOptions options = new FindReplaceOptions();

     // Assign a custom callback to the "ReplacingCallback" property.
     TextReplacementRecorder callback = new TextReplacementRecorder();
     options.setReplacingCallback(callback);

     // Set the "Direction" property to "FindReplaceDirection.Backward" to get the find-and-replace
     // operation to start from the end of the range, and traverse back to the beginning.
     // Set the "Direction" property to "FindReplaceDirection.Forward" to get the find-and-replace
     // operation to start from the beginning of the range, and traverse to the end.
     options.setDirection(findReplaceDirection);

     doc.getRange().replace(Pattern.compile("Match \\d*"), "Replacement", options);

     Assert.assertEquals("Replacement.\r" +
             "Replacement.\r" +
             "Replacement.\r" +
             "Replacement.", doc.getText().trim());

     switch (findReplaceDirection) {
         case FindReplaceDirection.FORWARD:
             Assert.assertEquals(new String[]{"Match 1", "Match 2", "Match 3", "Match 4"}, callback.getMatches().toArray());
             break;
         case FindReplaceDirection.BACKWARD:
             Assert.assertEquals(new String[]{"Match 4", "Match 3", "Match 2", "Match 1"}, callback.getMatches().toArray());
             break;
     }
 }

 public static Object[][] directionDataProvider() {
     return new Object[][]
             {
                     {FindReplaceDirection.BACKWARD},
                     {FindReplaceDirection.FORWARD},
             };
 }

 /// 
 /// Records all matches that occur during a find-and-replace operation in the order that they take place.
 /// 
 private static class TextReplacementRecorder implements IReplacingCallback {
     public int replacing(ReplacingArgs e) {
         mMatches.add(e.getMatch().group(0));
         return ReplaceAction.REPLACE;
     }

     public ArrayList getMatches() {
         return mMatches;
     }
     private ArrayList mMatches = new ArrayList<>();
 }
 
```

**Returns:**
int - القيمة المقابلة من نوع  int . القيمة المرجعة هي واحدة من ثوابت [FindReplaceDirection](../../com.aspose.words/findreplacedirection/).
### getFindWholeWordsOnly() {#getFindWholeWordsOnly}
```
public boolean getFindWholeWordsOnly()
```


True تشير إلى أن oldValue يجب أن تكون كلمة مستقلة.

 **Examples:** 

يوضح كيفية تبديل عمليات البحث والاستبدال التي تقتصر على كلمة مستقلة.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Jackson will meet you in Jacksonville.");

 // We can use a "FindReplaceOptions" object to modify the find-and-replace process.
 FindReplaceOptions options = new FindReplaceOptions();

 // Set the "FindWholeWordsOnly" flag to "true" to replace the found text if it is not a part of another word.
 // Set the "FindWholeWordsOnly" flag to "false" to replace all text regardless of its surroundings.
 options.setFindWholeWordsOnly(findWholeWordsOnly);

 doc.getRange().replace("Jackson", "Louis", options);

 Assert.assertEquals(
         findWholeWordsOnly ? "Louis will meet you in Jacksonville." : "Louis will meet you in Louisville.",
         doc.getText().trim());
 
```

**Returns:**
boolean - القيمة المنطقية المقابلة.
### getIgnoreDeleted() {#getIgnoreDeleted}
```
public boolean getIgnoreDeleted()
```


يحصل على قيمة منطقية تشير إلى ما إذا كان يجب تجاهل النص داخل مراجعات الحذف. القيمة الافتراضية هي  false .

 **Examples:** 

يعرض كيفية تضمين أو تجاهل النص داخل مراجعات الحذف أثناء عملية البحث والاستبدال.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Hello world!");
 builder.writeln("Hello again!");

 // Start tracking revisions and remove the second paragraph, which will create a delete revision.
 // That paragraph will persist in the document until we accept the delete revision.
 doc.startTrackRevisions("John Doe", new Date());
 doc.getFirstSection().getBody().getParagraphs().get(1).remove();
 doc.stopTrackRevisions();

 Assert.assertTrue(doc.getFirstSection().getBody().getParagraphs().get(1).isDeleteRevision());

 // We can use a "FindReplaceOptions" object to modify the find and replace process.
 FindReplaceOptions options = new FindReplaceOptions();

 // Set the "IgnoreDeleted" flag to "true" to get the find-and-replace
 // operation to ignore paragraphs that are delete revisions.
 // Set the "IgnoreDeleted" flag to "false" to get the find-and-replace
 // operation to also search for text inside delete revisions.
 options.setIgnoreDeleted(ignoreTextInsideDeleteRevisions);

 doc.getRange().replace("Hello", "Greetings", options);

 Assert.assertEquals(
         ignoreTextInsideDeleteRevisions
                 ? "Greetings world!\rHello again!"
                 : "Greetings world!\rGreetings again!", doc.getText().trim());
 
```

**Returns:**
boolean - قيمة منطقية تشير إلى ما إذا كان يجب تجاهل النص داخل مراجعات الحذف.
### getIgnoreFieldCodes() {#getIgnoreFieldCodes}
```
public boolean getIgnoreFieldCodes()
```


يحصل على قيمة منطقية تشير إلى ما إذا كان يجب تجاهل النص داخل رموز الحقول. القيمة الافتراضية هي  false .

 **Remarks:** 

هذا الخيار يؤثر فقط على رموز الحقول (لا يتجاهل العقد بين [NodeType.FIELD\_SEPARATOR](../../com.aspose.words/nodetype/\#FIELD-SEPARATOR) و [NodeType.FIELD\_END](../../com.aspose.words/nodetype/\#FIELD-END)).

لتجاهل الحقل بالكامل، يرجى استخدام الخيار المقابل [getIgnoreFields()](../../com.aspose.words/findreplaceoptions/\#getIgnoreFields) / [setIgnoreFields(boolean)](../../com.aspose.words/findreplaceoptions/\#setIgnoreFields-boolean).

 **Examples:** 

يعرض كيفية تجاهل النص داخل رموز الحقول.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.insertField("INCLUDETEXT", "Test IT!");

 FindReplaceOptions options = new FindReplaceOptions(); {options.setIgnoreFieldCodes(ignoreFieldCodes);}

 // Replace 'T' in document ignoring text inside field code or not.
 doc.getRange().replace(Pattern.compile("T"), "*", options);
 System.out.println(doc.getText());

 Assert.assertEquals(
         ignoreFieldCodes
                 ? "INCLUDETEXT*est I*!"
                 : "INCLUDE*EX**est I*!", doc.getText().trim());
 
```

**Returns:**
boolean - قيمة منطقية تشير إلى ما إذا كان يجب تجاهل النص داخل رموز الحقول.
### getIgnoreFields() {#getIgnoreFields}
```
public boolean getIgnoreFields()
```


يحصل على قيمة منطقية تشير إلى ما إذا كان يجب تجاهل النص داخل الحقول. القيمة الافتراضية هي  false .

 **Remarks:** 

هذا الخيار يؤثر على الحقل بالكامل (جميع العقد بين [NodeType.FIELD\_START](../../com.aspose.words/nodetype/\#FIELD-START) و [NodeType.FIELD\_END](../../com.aspose.words/nodetype/\#FIELD-END)).

لتجاهل رموز الحقول فقط، يرجى استخدام الخيار المقابل [getIgnoreFieldCodes()](../../com.aspose.words/findreplaceoptions/\#getIgnoreFieldCodes) / [setIgnoreFieldCodes(boolean)](../../com.aspose.words/findreplaceoptions/\#setIgnoreFieldCodes-boolean).

 **Examples:** 

يعرض كيفية تجاهل النص داخل الحقول.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Hello world!");
 builder.insertField("QUOTE", "Hello again!");

 // We can use a "FindReplaceOptions" object to modify the find-and-replace process.
 FindReplaceOptions options = new FindReplaceOptions();

 // Set the "IgnoreFields" flag to "true" to get the find-and-replace
 // operation to ignore text inside fields.
 // Set the "IgnoreFields" flag to "false" to get the find-and-replace
 // operation to also search for text inside fields.
 options.setIgnoreFields(ignoreTextInsideFields);

 doc.getRange().replace("Hello", "Greetings", options);

 Assert.assertEquals(
         ignoreTextInsideFields
                 ? "Greetings world!\rQUOTEHello again!"
                 : "Greetings world!\rQUOTEGreetings again!", doc.getText().trim());
 
```

**Returns:**
boolean - قيمة منطقية تشير إلى ما إذا كان يجب تجاهل النص داخل الحقول.
### getIgnoreFootnotes() {#getIgnoreFootnotes}
```
public boolean getIgnoreFootnotes()
```


يحصل على قيمة منطقية تشير إلى ما إذا كان يجب تجاهل الحواشي السفلية. القيمة الافتراضية هي  false .

 **Examples:** 

يعرض كيفية تجاهل الحواشي السفلية أثناء عملية البحث والاستبدال.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.write("Lorem ipsum dolor sit amet, consectetur adipiscing elit.");
 builder.insertFootnote(FootnoteType.FOOTNOTE, "Lorem ipsum dolor sit amet, consectetur adipiscing elit.");

 builder.insertParagraph();

 builder.write("Lorem ipsum dolor sit amet, consectetur adipiscing elit.");
 builder.insertFootnote(FootnoteType.ENDNOTE, "Lorem ipsum dolor sit amet, consectetur adipiscing elit.");

 // Set the "IgnoreFootnotes" flag to "true" to get the find-and-replace
 // operation to ignore text inside footnotes.
 // Set the "IgnoreFootnotes" flag to "false" to get the find-and-replace
 // operation to also search for text inside footnotes.
 FindReplaceOptions options = new FindReplaceOptions();
 {
     options.setIgnoreFootnotes(isIgnoreFootnotes);
 }
 doc.getRange().replace("Lorem ipsum", "Replaced Lorem ipsum", options);
 
```

**Returns:**
boolean - قيمة منطقية تشير إلى ما إذا كان يجب تجاهل الحواشي السفلية.
### getIgnoreInserted() {#getIgnoreInserted}
```
public boolean getIgnoreInserted()
```


يحصل على قيمة منطقية تشير إلى ما إذا كان يجب تجاهل النص داخل مراجعات الإدراج. القيمة الافتراضية هي  false .

 **Examples:** 

يعرض كيفية تضمين أو تجاهل النص داخل مراجعات الإدراج أثناء عملية البحث والاستبدال.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Hello world!");

 // Start tracking revisions and insert a paragraph. That paragraph will be an insert revision.
 doc.startTrackRevisions("John Doe", new Date());
 builder.writeln("Hello again!");
 doc.stopTrackRevisions();

 Assert.assertTrue(doc.getFirstSection().getBody().getParagraphs().get(1).isInsertRevision());

 // We can use a "FindReplaceOptions" object to modify the find-and-replace process.
 FindReplaceOptions options = new FindReplaceOptions();

 // Set the "IgnoreInserted" flag to "true" to get the find-and-replace
 // operation to ignore paragraphs that are insert revisions.
 // Set the "IgnoreInserted" flag to "false" to get the find-and-replace
 // operation to also search for text inside insert revisions.
 options.setIgnoreInserted(ignoreTextInsideInsertRevisions);

 doc.getRange().replace("Hello", "Greetings", options);

 Assert.assertEquals(
         ignoreTextInsideInsertRevisions
                 ? "Greetings world!\rHello again!"
                 : "Greetings world!\rGreetings again!", doc.getText().trim());
 
```

**Returns:**
boolean - قيمة منطقية تشير إلى ما إذا كان يجب تجاهل النص داخل مراجعات الإدراج.
### getIgnoreOfficeMath() {#getIgnoreOfficeMath}
```
public boolean getIgnoreOfficeMath()
```


يحصل على قيمة منطقية تشير إلى ما إذا كان يجب تجاهل النص داخل OfficeMath/>. القيمة الافتراضية هي  true .

 **Examples:** 

يعرض كيفية البحث واستبدال النص داخل OfficeMath.

```

 Document doc = new Document(getMyDir() + "Office math.docx");

 Assert.assertEquals("i+b-c\u2265iM+bM-cM", doc.getFirstSection().getBody().getFirstParagraph().getText().trim());

 FindReplaceOptions options = new FindReplaceOptions();
 options.setIgnoreOfficeMath(isIgnoreOfficeMath);
 doc.getRange().replace("b", "x", options);

 if (isIgnoreOfficeMath)
     Assert.assertEquals("i+b-c\u2265iM+bM-cM", doc.getFirstSection().getBody().getFirstParagraph().getText().trim());
 else
     Assert.assertEquals("i+x-c\u2265iM+xM-cM", doc.getFirstSection().getBody().getFirstParagraph().getText().trim());
 
```

**Returns:**
boolean - قيمة منطقية تشير إلى ما إذا كان يجب تجاهل النص داخل OfficeMath/>.
### getIgnoreShapes() {#getIgnoreShapes}
```
public boolean getIgnoreShapes()
```


يحصل أو يضبط قيمة منطقية تشير إلى تجاهل الأشكال داخل النص.

القيمة الافتراضية هي false.

 **Examples:** 

يعرض كيفية تجاهل الأشكال أثناء استبدال النص.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.write("Lorem ipsum dolor sit amet, consectetur adipiscing elit.");
 builder.insertShape(ShapeType.BALLOON, 200.0, 200.0);
 builder.write("Lorem ipsum dolor sit amet, consectetur adipiscing elit.");

 FindReplaceOptions findReplaceOptions = new FindReplaceOptions(); { findReplaceOptions.setIgnoreShapes(true); }
 builder.getDocument().getRange().replace("Lorem ipsum dolor sit amet, consectetur adipiscing elit.Lorem ipsum dolor sit amet, consectetur adipiscing elit.",
     "Lorem ipsum dolor sit amet, consectetur adipiscing elit.", findReplaceOptions);
 Assert.assertEquals("Lorem ipsum dolor sit amet, consectetur adipiscing elit.", builder.getDocument().getText().trim());
 
```

**Returns:**
boolean - القيمة المنطقية المقابلة.
### getIgnoreStructuredDocumentTags() {#getIgnoreStructuredDocumentTags}
```
public boolean getIgnoreStructuredDocumentTags()
```


يحصل على قيمة منطقية تشير إلى ما إذا كان يجب تجاهل محتوى [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag/). القيمة الافتراضية هي false.

 **Remarks:** 

عند ضبط هذا الخيار على true، سيتم اعتبار محتوى [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag/) نصًا بسيطًا.

إلا، سيتم معالجة [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag/) كقصة مستقلة وسيتم البحث عن نمط الاستبدال بشكل منفصل لكل [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag/)، بحيث إذا كان النمط يعبر [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag/)، فلن يتم تنفيذ الاستبدال لهذا النمط.

 **Examples:** 

يوضح كيفية تجاهل محتوى العلامات أثناء الاستبدال.

```

 Document doc = new Document(getMyDir() + "Structured document tags.docx");

 // This paragraph contains SDT.
 Paragraph p = (Paragraph)doc.getFirstSection().getBody().getChild(NodeType.PARAGRAPH, 2, true);
 String textToSearch = p.toString(SaveFormat.TEXT).trim();

 FindReplaceOptions options = new FindReplaceOptions();
 options.setIgnoreStructuredDocumentTags(true);
 doc.getRange().replace(textToSearch, "replacement", options);

 doc.save(getArtifactsDir() + "StructuredDocumentTag.IgnoreStructuredDocumentTags.docx");
 
```

**Returns:**
boolean - قيمة منطقية تشير إلى ما إذا كان يجب تجاهل محتوى [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag/).
### getLegacyMode() {#getLegacyMode}
```
public boolean getLegacyMode()
```


يحصل على قيمة منطقية تشير إلى استخدام خوارزمية البحث/الاستبدال القديمة.

 **Remarks:** 

استخدم هذه العلامة إذا كنت بحاجة إلى نفس السلوك تمامًا كما كان قبل تقديم ميزة البحث/الاستبدال المتقدمة. لاحظ أن الخوارزمية القديمة لا تدعم الميزات المتقدمة مثل الاستبدال مع الفواصل، تطبيق التنسيق وما إلى ذلك.

 **Examples:** 

يوضح كيفية التعرف على الاستبدالات واستخدامها داخل أنماط الاستبدال.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.write("Jason gave money to Paul.");

 String regex = "([A-z]+) gave money to ([A-z]+)";

 FindReplaceOptions options = new FindReplaceOptions();
 options.setUseSubstitutions(true);

 // Using legacy mode does not support many advanced features, so we need to set it to 'false'.
 options.setLegacyMode(false);

 doc.getRange().replace(Pattern.compile(regex), "$2 took money from $1", options);

 Assert.assertEquals(doc.getText(), "Paul took money from Jason.\f");
 
```

**Returns:**
boolean - قيمة منطقية تشير إلى أنه يتم استخدام خوارزمية البحث/الاستبدال القديمة.
### getMatchCase() {#getMatchCase}
```
public boolean getMatchCase()
```


True تشير إلى مقارنة حساسة لحالة الأحرف، false تشير إلى مقارنة غير حساسة لحالة الأحرف.

 **Examples:** 

يوضح كيفية تبديل حساسية الحالة عند تنفيذ عملية البحث والاستبدال.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Ruby bought a ruby necklace.");

 // We can use a "FindReplaceOptions" object to modify the find-and-replace process.
 FindReplaceOptions options = new FindReplaceOptions();

 // Set the "MatchCase" flag to "true" to apply case sensitivity while finding strings to replace.
 // Set the "MatchCase" flag to "false" to ignore character case while searching for text to replace.
 options.setMatchCase(matchCase);

 doc.getRange().replace("Ruby", "Jade", options);

 Assert.assertEquals(matchCase ? "Jade bought a ruby necklace." : "Jade bought a Jade necklace.",
         doc.getText().trim());
 
```

**Returns:**
boolean - القيمة المنطقية المقابلة.
### getReplacementFormat() {#getReplacementFormat}
```
public int getReplacementFormat()
```


يحدد تنسيق الاستبدال. الافتراضي هو [ReplacementFormat.TEXT](../../com.aspose.words/replacementformat/\#TEXT).

 **Remarks:** 

يكون له تأثير فقط عند الاستخدام في [Replacer](../../com.aspose.words/replacer/)

**Returns:**
int - القيمة الصحيحة المقابلة. القيمة المرجعة هي واحدة من ثوابت [ReplacementFormat](../../com.aspose.words/replacementformat/).
### getReplacingCallback() {#getReplacingCallback}
```
public IReplacingCallback getReplacingCallback()
```


الطريقة المعرفة من قبل المستخدم التي تُستدعى قبل كل حدوث استبدال.

 **Examples:** 

يوضح كيفية استبدال جميع تكرارات نمط التعبير النمطي بسلسلة أخرى، مع تتبع جميع هذه الاستبدالات.

```

 public void replaceWithCallback() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     builder.writeln("Our new location in New York City is opening tomorrow. " +
             "Hope to see all our NYC-based customers at the opening!");

     // We can use a "FindReplaceOptions" object to modify the find-and-replace process.
     FindReplaceOptions options = new FindReplaceOptions();

     // Set a callback that tracks any replacements that the "Replace" method will make.
     TextFindAndReplacementLogger logger = new TextFindAndReplacementLogger();
     options.setReplacingCallback(logger);

     doc.getRange().replace(Pattern.compile("New York City|NYC"), "Washington", options);

     Assert.assertEquals("Our new location in (Old value:\"New York City\") Washington is opening tomorrow. " +
             "Hope to see all our (Old value:\"NYC\") Washington-based customers at the opening!", doc.getText().trim());

     Assert.assertEquals("\"New York City\" converted to \"Washington\" 20 characters into a 21 node." +
             "\"NYC\" converted to \"Washington\" 42 characters into a 21 node.", logger.getLog().trim());
 }

 /// 
 /// Maintains a log of every text replacement done by a find-and-replace operation
 /// and notes the original matched text's value.
 /// 
 private static class TextFindAndReplacementLogger implements IReplacingCallback {
     public int replacing(ReplacingArgs args) {
         mLog.append(MessageFormat.format("\"{0}\" converted to \"{1}\" {2} characters into a {3} node.", args.getMatch().group(0), args.getReplacement(), args.getMatchOffset(), args.getMatchNode().getNodeType()));

         args.setReplacement(MessageFormat.format("(Old value:\"{0}\") {1}", args.getMatch().group(0), args.getReplacement()));
         return ReplaceAction.REPLACE;
     }

     public String getLog() {
         return mLog.toString();
     }

     private final StringBuilder mLog = new StringBuilder();
 }
 
```

يوضح كيفية تطبيق خط مختلف على المحتوى الجديد عبر FindReplaceOptions.

```

 public void convertNumbersToHexadecimal() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     builder.getFont().setName("Arial");
     builder.writeln("Numbers that the find-and-replace operation will convert to hexadecimal and highlight:\n" +
             "123, 456, 789 and 17379.");

     // We can use a "FindReplaceOptions" object to modify the find-and-replace process.
     FindReplaceOptions options = new FindReplaceOptions();

     // Set the "HighlightColor" property to a background color that we want to apply to the operation's resulting text.
     options.getApplyFont().setHighlightColor(Color.GRAY);

     NumberHexer numberHexer = new NumberHexer();
     options.setReplacingCallback(numberHexer);

     int replacementCount = doc.getRange().replace(Pattern.compile("[0-9]+"), "", options);

     System.out.println(numberHexer.getLog());

     Assert.assertEquals(4, replacementCount);
     Assert.assertEquals("Numbers that the find-and-replace operation will convert to hexadecimal and highlight:\r" +
             "0x123, 0x456, 0x789 and 0x17,379.", doc.getText().trim());
 }

 /// 
 /// Replaces numeric find-and-replacement matches with their hexadecimal equivalents.
 /// Maintains a log of every replacement.
 /// 
 private static class NumberHexer implements IReplacingCallback {
     public int replacing(ReplacingArgs args) {
         mCurrentReplacementNumber++;

         int number = Integer.parseInt(args.getMatch().group(0));

         args.setReplacement(MessageFormat.format("0x{0}", number));

         mLog.append(MessageFormat.format("Match #{0}", mCurrentReplacementNumber));
         mLog.append(MessageFormat.format("\tOriginal value:\t{0}", args.getMatch().group(0)));
         mLog.append(MessageFormat.format("\tReplacement:\t{0}", args.getReplacement()));
         mLog.append(MessageFormat.format("\tOffset in parent {0} node:\t{1}", args.getMatchNode().getNodeType(), args.getMatchOffset()));

         return ReplaceAction.REPLACE;
     }

     public String getLog() {
         return mLog.toString();
     }

     private int mCurrentReplacementNumber;
     private final StringBuilder mLog = new StringBuilder();
 }
 
```

**Returns:**
[IReplacingCallback](../../com.aspose.words/ireplacingcallback/) - The corresponding [IReplacingCallback](../../com.aspose.words/ireplacingcallback/) value.
### getSmartParagraphBreakReplacement() {#getSmartParagraphBreakReplacement}
```
public boolean getSmartParagraphBreakReplacement()
```


يحصل أو يضبط قيمة منطقية تشير إلى السماح باستبدال فاصل الفقرة عندما لا يوجد فقرة شقيقة تالية.

القيمة الافتراضية هي false.

 **Remarks:** 

يسمح هذا الخيار باستبدال فاصل الفقرة عندما لا يكون هناك فقرة شقيقة تالية يمكن نقل جميع العقد الفرعية إليها، عن طريق العثور على أي فقرة تالية (ليس بالضرورة شقيقة) بعد الفقرة التي يتم استبدالها.

 **Examples:** 

يوضح كيفية إزالة الفقرة من خلية جدول تحتوي على جدول متداخل.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create table with paragraph and inner table in first cell.
 builder.startTable();
 builder.insertCell();
 builder.write("TEXT1");
 builder.startTable();
 builder.insertCell();
 builder.endTable();
 builder.endTable();
 builder.writeln();

 FindReplaceOptions options = new FindReplaceOptions();
 // When the following option is set to 'true', Aspose.Words will remove paragraph's text
 // completely with its paragraph mark. Otherwise, Aspose.Words will mimic Word and remove
 // only paragraph's text and leaves the paragraph mark intact (when a table follows the text).
 options.setSmartParagraphBreakReplacement(isSmartParagraphBreakReplacement);
 doc.getRange().replace("TEXT1&p", "", options);

 doc.save(getArtifactsDir() + "Table.RemoveParagraphTextAndMark.docx");
 
```

**Returns:**
boolean - القيمة المنطقية المقابلة.
### getUseLegacyOrder() {#getUseLegacyOrder}
```
public boolean getUseLegacyOrder()
```


True تشير إلى أن البحث النصي يتم بشكل متسلسل من الأعلى إلى الأسفل مع مراعاة صناديق النص. القيمة الافتراضية هي false.

 **Examples:** 

يوضح كيفية تغيير ترتيب البحث عن العقد عند تنفيذ عملية البحث والاستبدال النصي.

```

 public void useLegacyOrder(boolean useLegacyOrder) throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Insert three runs which we can search for using a regex pattern.
     // Place one of those runs inside a text box.
     builder.writeln("[tag 1]");
     Shape textBox = builder.insertShape(ShapeType.TEXT_BOX, 100.0, 50.0);
     builder.writeln("[tag 2]");
     builder.moveTo(textBox.getFirstParagraph());
     builder.write("[tag 3]");

     // We can use a "FindReplaceOptions" object to modify the find-and-replace process.
     FindReplaceOptions options = new FindReplaceOptions();

     // Assign a custom callback to the "ReplacingCallback" property.
     TextReplacementTracker callback = new TextReplacementTracker();
     options.setReplacingCallback(callback);

     // If we set the "UseLegacyOrder" property to "true", the
     // find-and-replace operation will go through all the runs outside of a text box
     // before going through the ones inside a text box.
     // If we set the "UseLegacyOrder" property to "false", the
     // find-and-replace operation will go over all the runs in a range in sequential order.
     options.setUseLegacyOrder(useLegacyOrder);

     doc.getRange().replace("\[tag d*\]", "", options);
 }

 public static Object[][] useLegacyOrderDataProvider() {
     return new Object[][]
             {
                     {true},
                     {false},
             };
 }

 /// 
 /// Records the order of all matches that occur during a find-and-replace operation.
 /// 
 private static class TextReplacementTracker implements IReplacingCallback {
     public int replacing(ReplacingArgs e) {
         mMatches.add(e.getMatch().group(1));
         return ReplaceAction.REPLACE;
     }

     public ArrayList getMatches() {
         return mMatches;
     }

     private ArrayList mMatches;
 }
 
```

**Returns:**
boolean - القيمة المنطقية المقابلة.
### getUseSubstitutions() {#getUseSubstitutions}
```
public boolean getUseSubstitutions()
```


يحصل على قيمة منطقية تشير إلى ما إذا كان يجب التعرف على الاستبدالات واستخدامها داخل أنماط الاستبدال. القيمة الافتراضية هي false.

 **Remarks:** 

للتفاصيل حول عناصر الاستبدال يرجى الرجوع إلى: https://docs.microsoft.com/en-us/dotnet/standard/base-types/substitutions-in-regular-expressions.

 **Examples:** 

يوضح كيفية التعرف على الاستبدالات واستخدامها داخل أنماط الاستبدال.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.write("Jason gave money to Paul.");

 String regex = "([A-z]+) gave money to ([A-z]+)";

 FindReplaceOptions options = new FindReplaceOptions();
 options.setUseSubstitutions(true);

 // Using legacy mode does not support many advanced features, so we need to set it to 'false'.
 options.setLegacyMode(false);

 doc.getRange().replace(Pattern.compile(regex), "$2 took money from $1", options);

 Assert.assertEquals(doc.getText(), "Paul took money from Jason.\f");
 
```

يوضح كيفية استبدال النص باستخدام الاستبدالات.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("John sold a car to Paul.");
 builder.writeln("Jane sold a house to Joe.");

 // We can use a "FindReplaceOptions" object to modify the find-and-replace process.
 FindReplaceOptions options = new FindReplaceOptions();

 // Set the "UseSubstitutions" property to "true" to get
 // the find-and-replace operation to recognize substitution elements.
 // Set the "UseSubstitutions" property to "false" to ignore substitution elements.
 options.setUseSubstitutions(useSubstitutions);

 doc.getRange().replace(Pattern.compile("([A-z]+) sold a ([A-z]+) to ([A-z]+)"), "$3 bought a $2 from $1", options);

 Assert.assertEquals(
         useSubstitutions
                 ? "Paul bought a car from John.\rJoe bought a house from Jane."
                 : "$3 bought a $2 from $1.\r$3 bought a $2 from $1.", doc.getText().trim());
 
```

**Returns:**
boolean - قيمة منطقية تشير إلى ما إذا كان يجب التعرف على الاستبدالات واستخدامها داخل أنماط الاستبدال.
### setDirection(int value) {#setDirection-int}
```
public void setDirection(int value)
```


يحدد الاتجاه للاستبدال. القيمة الافتراضية هي [FindReplaceDirection.FORWARD](../../com.aspose.words/findreplacedirection/\#FORWARD).

 **Examples:** 

يعرض كيفية تحديد الاتجاه الذي ينتقل فيه عملية البحث والاستبدال عبر المستند.

```

 public void direction(int findReplaceDirection) throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Insert three runs which we can search for using a regex pattern.
     // Place one of those runs inside a text box.
     builder.writeln("Match 1.");
     builder.writeln("Match 2.");
     builder.writeln("Match 3.");
     builder.writeln("Match 4.");

     // We can use a "FindReplaceOptions" object to modify the find-and-replace process.
     FindReplaceOptions options = new FindReplaceOptions();

     // Assign a custom callback to the "ReplacingCallback" property.
     TextReplacementRecorder callback = new TextReplacementRecorder();
     options.setReplacingCallback(callback);

     // Set the "Direction" property to "FindReplaceDirection.Backward" to get the find-and-replace
     // operation to start from the end of the range, and traverse back to the beginning.
     // Set the "Direction" property to "FindReplaceDirection.Forward" to get the find-and-replace
     // operation to start from the beginning of the range, and traverse to the end.
     options.setDirection(findReplaceDirection);

     doc.getRange().replace(Pattern.compile("Match \\d*"), "Replacement", options);

     Assert.assertEquals("Replacement.\r" +
             "Replacement.\r" +
             "Replacement.\r" +
             "Replacement.", doc.getText().trim());

     switch (findReplaceDirection) {
         case FindReplaceDirection.FORWARD:
             Assert.assertEquals(new String[]{"Match 1", "Match 2", "Match 3", "Match 4"}, callback.getMatches().toArray());
             break;
         case FindReplaceDirection.BACKWARD:
             Assert.assertEquals(new String[]{"Match 4", "Match 3", "Match 2", "Match 1"}, callback.getMatches().toArray());
             break;
     }
 }

 public static Object[][] directionDataProvider() {
     return new Object[][]
             {
                     {FindReplaceDirection.BACKWARD},
                     {FindReplaceDirection.FORWARD},
             };
 }

 /// 
 /// Records all matches that occur during a find-and-replace operation in the order that they take place.
 /// 
 private static class TextReplacementRecorder implements IReplacingCallback {
     public int replacing(ReplacingArgs e) {
         mMatches.add(e.getMatch().group(0));
         return ReplaceAction.REPLACE;
     }

     public ArrayList getMatches() {
         return mMatches;
     }
     private ArrayList mMatches = new ArrayList<>();
 }
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| value | int | القيمة الصحيحة المقابلة. يجب أن تكون القيمة واحدة من ثوابت [FindReplaceDirection](../../com.aspose.words/findreplacedirection/). |

### setFindWholeWordsOnly(boolean value) {#setFindWholeWordsOnly-boolean}
```
public void setFindWholeWordsOnly(boolean value)
```


True تشير إلى أن oldValue يجب أن تكون كلمة مستقلة.

 **Examples:** 

يوضح كيفية تبديل عمليات البحث والاستبدال التي تقتصر على كلمة مستقلة.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Jackson will meet you in Jacksonville.");

 // We can use a "FindReplaceOptions" object to modify the find-and-replace process.
 FindReplaceOptions options = new FindReplaceOptions();

 // Set the "FindWholeWordsOnly" flag to "true" to replace the found text if it is not a part of another word.
 // Set the "FindWholeWordsOnly" flag to "false" to replace all text regardless of its surroundings.
 options.setFindWholeWordsOnly(findWholeWordsOnly);

 doc.getRange().replace("Jackson", "Louis", options);

 Assert.assertEquals(
         findWholeWordsOnly ? "Louis will meet you in Jacksonville." : "Louis will meet you in Louisville.",
         doc.getText().trim());
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | القيمة المنطقية المقابلة. |

### setIgnoreDeleted(boolean value) {#setIgnoreDeleted-boolean}
```
public void setIgnoreDeleted(boolean value)
```


يضبط قيمة منطقية تشير إلى ما إذا كان يجب تجاهل النص داخل مراجعات الحذف. القيمة الافتراضية هي false.

 **Examples:** 

يعرض كيفية تضمين أو تجاهل النص داخل مراجعات الحذف أثناء عملية البحث والاستبدال.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Hello world!");
 builder.writeln("Hello again!");

 // Start tracking revisions and remove the second paragraph, which will create a delete revision.
 // That paragraph will persist in the document until we accept the delete revision.
 doc.startTrackRevisions("John Doe", new Date());
 doc.getFirstSection().getBody().getParagraphs().get(1).remove();
 doc.stopTrackRevisions();

 Assert.assertTrue(doc.getFirstSection().getBody().getParagraphs().get(1).isDeleteRevision());

 // We can use a "FindReplaceOptions" object to modify the find and replace process.
 FindReplaceOptions options = new FindReplaceOptions();

 // Set the "IgnoreDeleted" flag to "true" to get the find-and-replace
 // operation to ignore paragraphs that are delete revisions.
 // Set the "IgnoreDeleted" flag to "false" to get the find-and-replace
 // operation to also search for text inside delete revisions.
 options.setIgnoreDeleted(ignoreTextInsideDeleteRevisions);

 doc.getRange().replace("Hello", "Greetings", options);

 Assert.assertEquals(
         ignoreTextInsideDeleteRevisions
                 ? "Greetings world!\rHello again!"
                 : "Greetings world!\rGreetings again!", doc.getText().trim());
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | قيمة منطقية تشير إلى ما إذا كان يجب تجاهل النص داخل مراجعات الحذف. |

### setIgnoreFieldCodes(boolean value) {#setIgnoreFieldCodes-boolean}
```
public void setIgnoreFieldCodes(boolean value)
```


يضبط قيمة منطقية تشير إلى ما إذا كان يجب تجاهل النص داخل رموز الحقول. القيمة الافتراضية هي false.

 **Remarks:** 

هذا الخيار يؤثر فقط على رموز الحقول (لا يتجاهل العقد بين [NodeType.FIELD\_SEPARATOR](../../com.aspose.words/nodetype/\#FIELD-SEPARATOR) و [NodeType.FIELD\_END](../../com.aspose.words/nodetype/\#FIELD-END)).

لتجاهل الحقل بالكامل، يرجى استخدام الخيار المقابل [getIgnoreFields()](../../com.aspose.words/findreplaceoptions/\#getIgnoreFields) / [setIgnoreFields(boolean)](../../com.aspose.words/findreplaceoptions/\#setIgnoreFields-boolean).

 **Examples:** 

يعرض كيفية تجاهل النص داخل رموز الحقول.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.insertField("INCLUDETEXT", "Test IT!");

 FindReplaceOptions options = new FindReplaceOptions(); {options.setIgnoreFieldCodes(ignoreFieldCodes);}

 // Replace 'T' in document ignoring text inside field code or not.
 doc.getRange().replace(Pattern.compile("T"), "*", options);
 System.out.println(doc.getText());

 Assert.assertEquals(
         ignoreFieldCodes
                 ? "INCLUDETEXT*est I*!"
                 : "INCLUDE*EX**est I*!", doc.getText().trim());
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | قيمة منطقية تشير إلى ما إذا كان يجب تجاهل النص داخل رموز الحقول. |

### setIgnoreFields(boolean value) {#setIgnoreFields-boolean}
```
public void setIgnoreFields(boolean value)
```


يضبط قيمة منطقية تشير إلى ما إذا كان يجب تجاهل النص داخل الحقول. القيمة الافتراضية هي false.

 **Remarks:** 

هذا الخيار يؤثر على الحقل بالكامل (جميع العقد بين [NodeType.FIELD\_START](../../com.aspose.words/nodetype/\#FIELD-START) و [NodeType.FIELD\_END](../../com.aspose.words/nodetype/\#FIELD-END)).

لتجاهل رموز الحقول فقط، يرجى استخدام الخيار المقابل [getIgnoreFieldCodes()](../../com.aspose.words/findreplaceoptions/\#getIgnoreFieldCodes) / [setIgnoreFieldCodes(boolean)](../../com.aspose.words/findreplaceoptions/\#setIgnoreFieldCodes-boolean).

 **Examples:** 

يعرض كيفية تجاهل النص داخل الحقول.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Hello world!");
 builder.insertField("QUOTE", "Hello again!");

 // We can use a "FindReplaceOptions" object to modify the find-and-replace process.
 FindReplaceOptions options = new FindReplaceOptions();

 // Set the "IgnoreFields" flag to "true" to get the find-and-replace
 // operation to ignore text inside fields.
 // Set the "IgnoreFields" flag to "false" to get the find-and-replace
 // operation to also search for text inside fields.
 options.setIgnoreFields(ignoreTextInsideFields);

 doc.getRange().replace("Hello", "Greetings", options);

 Assert.assertEquals(
         ignoreTextInsideFields
                 ? "Greetings world!\rQUOTEHello again!"
                 : "Greetings world!\rQUOTEGreetings again!", doc.getText().trim());
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | قيمة منطقية تشير إلى تجاهل النص داخل الحقول. |

### setIgnoreFootnotes(boolean value) {#setIgnoreFootnotes-boolean}
```
public void setIgnoreFootnotes(boolean value)
```


يضبط قيمة منطقية تشير إلى تجاهل الحواشي السفلية. القيمة الافتراضية هي  false .

 **Examples:** 

يعرض كيفية تجاهل الحواشي السفلية أثناء عملية البحث والاستبدال.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.write("Lorem ipsum dolor sit amet, consectetur adipiscing elit.");
 builder.insertFootnote(FootnoteType.FOOTNOTE, "Lorem ipsum dolor sit amet, consectetur adipiscing elit.");

 builder.insertParagraph();

 builder.write("Lorem ipsum dolor sit amet, consectetur adipiscing elit.");
 builder.insertFootnote(FootnoteType.ENDNOTE, "Lorem ipsum dolor sit amet, consectetur adipiscing elit.");

 // Set the "IgnoreFootnotes" flag to "true" to get the find-and-replace
 // operation to ignore text inside footnotes.
 // Set the "IgnoreFootnotes" flag to "false" to get the find-and-replace
 // operation to also search for text inside footnotes.
 FindReplaceOptions options = new FindReplaceOptions();
 {
     options.setIgnoreFootnotes(isIgnoreFootnotes);
 }
 doc.getRange().replace("Lorem ipsum", "Replaced Lorem ipsum", options);
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | قيمة منطقية تشير إلى تجاهل الحواشي السفلية. |

### setIgnoreInserted(boolean value) {#setIgnoreInserted-boolean}
```
public void setIgnoreInserted(boolean value)
```


يضبط قيمة منطقية تشير إلى تجاهل النص داخل مراجعات الإدراج. القيمة الافتراضية هي  false .

 **Examples:** 

يعرض كيفية تضمين أو تجاهل النص داخل مراجعات الإدراج أثناء عملية البحث والاستبدال.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Hello world!");

 // Start tracking revisions and insert a paragraph. That paragraph will be an insert revision.
 doc.startTrackRevisions("John Doe", new Date());
 builder.writeln("Hello again!");
 doc.stopTrackRevisions();

 Assert.assertTrue(doc.getFirstSection().getBody().getParagraphs().get(1).isInsertRevision());

 // We can use a "FindReplaceOptions" object to modify the find-and-replace process.
 FindReplaceOptions options = new FindReplaceOptions();

 // Set the "IgnoreInserted" flag to "true" to get the find-and-replace
 // operation to ignore paragraphs that are insert revisions.
 // Set the "IgnoreInserted" flag to "false" to get the find-and-replace
 // operation to also search for text inside insert revisions.
 options.setIgnoreInserted(ignoreTextInsideInsertRevisions);

 doc.getRange().replace("Hello", "Greetings", options);

 Assert.assertEquals(
         ignoreTextInsideInsertRevisions
                 ? "Greetings world!\rHello again!"
                 : "Greetings world!\rGreetings again!", doc.getText().trim());
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | قيمة منطقية تشير إلى تجاهل النص داخل مراجعات الإدراج. |

### setIgnoreOfficeMath(boolean value) {#setIgnoreOfficeMath-boolean}
```
public void setIgnoreOfficeMath(boolean value)
```


يضبط قيمة منطقية تشير إلى تجاهل النص داخل OfficeMath/>. القيمة الافتراضية هي  true .

 **Examples:** 

يعرض كيفية البحث واستبدال النص داخل OfficeMath.

```

 Document doc = new Document(getMyDir() + "Office math.docx");

 Assert.assertEquals("i+b-c\u2265iM+bM-cM", doc.getFirstSection().getBody().getFirstParagraph().getText().trim());

 FindReplaceOptions options = new FindReplaceOptions();
 options.setIgnoreOfficeMath(isIgnoreOfficeMath);
 doc.getRange().replace("b", "x", options);

 if (isIgnoreOfficeMath)
     Assert.assertEquals("i+b-c\u2265iM+bM-cM", doc.getFirstSection().getBody().getFirstParagraph().getText().trim());
 else
     Assert.assertEquals("i+x-c\u2265iM+xM-cM", doc.getFirstSection().getBody().getFirstParagraph().getText().trim());
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | قيمة منطقية تشير إلى تجاهل النص داخل OfficeMath/>. |

### setIgnoreShapes(boolean value) {#setIgnoreShapes-boolean}
```
public void setIgnoreShapes(boolean value)
```


يحصل أو يضبط قيمة منطقية تشير إلى تجاهل الأشكال داخل النص.

القيمة الافتراضية هي false.

 **Examples:** 

يعرض كيفية تجاهل الأشكال أثناء استبدال النص.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.write("Lorem ipsum dolor sit amet, consectetur adipiscing elit.");
 builder.insertShape(ShapeType.BALLOON, 200.0, 200.0);
 builder.write("Lorem ipsum dolor sit amet, consectetur adipiscing elit.");

 FindReplaceOptions findReplaceOptions = new FindReplaceOptions(); { findReplaceOptions.setIgnoreShapes(true); }
 builder.getDocument().getRange().replace("Lorem ipsum dolor sit amet, consectetur adipiscing elit.Lorem ipsum dolor sit amet, consectetur adipiscing elit.",
     "Lorem ipsum dolor sit amet, consectetur adipiscing elit.", findReplaceOptions);
 Assert.assertEquals("Lorem ipsum dolor sit amet, consectetur adipiscing elit.", builder.getDocument().getText().trim());
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | القيمة المنطقية المقابلة. |

### setIgnoreStructuredDocumentTags(boolean value) {#setIgnoreStructuredDocumentTags-boolean}
```
public void setIgnoreStructuredDocumentTags(boolean value)
```


يضبط قيمة منطقية تشير إلى تجاهل محتوى [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag/). القيمة الافتراضية هي  false .

 **Remarks:** 

عند ضبط هذا الخيار على true، سيتم اعتبار محتوى [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag/) نصًا بسيطًا.

إلا، سيتم معالجة [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag/) كقصة مستقلة وسيتم البحث عن نمط الاستبدال بشكل منفصل لكل [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag/)، بحيث إذا كان النمط يعبر [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag/)، فلن يتم تنفيذ الاستبدال لهذا النمط.

 **Examples:** 

يوضح كيفية تجاهل محتوى العلامات أثناء الاستبدال.

```

 Document doc = new Document(getMyDir() + "Structured document tags.docx");

 // This paragraph contains SDT.
 Paragraph p = (Paragraph)doc.getFirstSection().getBody().getChild(NodeType.PARAGRAPH, 2, true);
 String textToSearch = p.toString(SaveFormat.TEXT).trim();

 FindReplaceOptions options = new FindReplaceOptions();
 options.setIgnoreStructuredDocumentTags(true);
 doc.getRange().replace(textToSearch, "replacement", options);

 doc.save(getArtifactsDir() + "StructuredDocumentTag.IgnoreStructuredDocumentTags.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| value | boolean | قيمة منطقية تشير إلى تجاهل محتوى [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag/). |

### setLegacyMode(boolean value) {#setLegacyMode-boolean}
```
public void setLegacyMode(boolean value)
```


يضبط قيمة منطقية تشير إلى استخدام خوارزمية البحث/الاستبدال القديمة.

 **Remarks:** 

استخدم هذه العلامة إذا كنت بحاجة إلى نفس السلوك تمامًا كما كان قبل تقديم ميزة البحث/الاستبدال المتقدمة. لاحظ أن الخوارزمية القديمة لا تدعم الميزات المتقدمة مثل الاستبدال مع الفواصل، تطبيق التنسيق وما إلى ذلك.

 **Examples:** 

يوضح كيفية التعرف على الاستبدالات واستخدامها داخل أنماط الاستبدال.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.write("Jason gave money to Paul.");

 String regex = "([A-z]+) gave money to ([A-z]+)";

 FindReplaceOptions options = new FindReplaceOptions();
 options.setUseSubstitutions(true);

 // Using legacy mode does not support many advanced features, so we need to set it to 'false'.
 options.setLegacyMode(false);

 doc.getRange().replace(Pattern.compile(regex), "$2 took money from $1", options);

 Assert.assertEquals(doc.getText(), "Paul took money from Jason.\f");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | قيمة منطقية تشير إلى استخدام خوارزمية البحث/الاستبدال القديمة. |

### setMatchCase(boolean value) {#setMatchCase-boolean}
```
public void setMatchCase(boolean value)
```


True تشير إلى مقارنة حساسة لحالة الأحرف، false تشير إلى مقارنة غير حساسة لحالة الأحرف.

 **Examples:** 

يوضح كيفية تبديل حساسية الحالة عند تنفيذ عملية البحث والاستبدال.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Ruby bought a ruby necklace.");

 // We can use a "FindReplaceOptions" object to modify the find-and-replace process.
 FindReplaceOptions options = new FindReplaceOptions();

 // Set the "MatchCase" flag to "true" to apply case sensitivity while finding strings to replace.
 // Set the "MatchCase" flag to "false" to ignore character case while searching for text to replace.
 options.setMatchCase(matchCase);

 doc.getRange().replace("Ruby", "Jade", options);

 Assert.assertEquals(matchCase ? "Jade bought a ruby necklace." : "Jade bought a Jade necklace.",
         doc.getText().trim());
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | القيمة المنطقية المقابلة. |

### setReplacementFormat(int value) {#setReplacementFormat-int}
```
public void setReplacementFormat(int value)
```


يحدد تنسيق الاستبدال. الافتراضي هو [ReplacementFormat.TEXT](../../com.aspose.words/replacementformat/\#TEXT).

 **Remarks:** 

يكون له تأثير فقط عند الاستخدام في [Replacer](../../com.aspose.words/replacer/)

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| value | int | القيمة  int  المقابلة. يجب أن تكون القيمة واحدة من ثابتات [ReplacementFormat](../../com.aspose.words/replacementformat/). |

### setReplacingCallback(IReplacingCallback value) {#setReplacingCallback-com.aspose.words.IReplacingCallback}
```
public void setReplacingCallback(IReplacingCallback value)
```


الطريقة المعرفة من قبل المستخدم التي تُستدعى قبل كل حدوث استبدال.

 **Examples:** 

يوضح كيفية استبدال جميع تكرارات نمط التعبير النمطي بسلسلة أخرى، مع تتبع جميع هذه الاستبدالات.

```

 public void replaceWithCallback() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     builder.writeln("Our new location in New York City is opening tomorrow. " +
             "Hope to see all our NYC-based customers at the opening!");

     // We can use a "FindReplaceOptions" object to modify the find-and-replace process.
     FindReplaceOptions options = new FindReplaceOptions();

     // Set a callback that tracks any replacements that the "Replace" method will make.
     TextFindAndReplacementLogger logger = new TextFindAndReplacementLogger();
     options.setReplacingCallback(logger);

     doc.getRange().replace(Pattern.compile("New York City|NYC"), "Washington", options);

     Assert.assertEquals("Our new location in (Old value:\"New York City\") Washington is opening tomorrow. " +
             "Hope to see all our (Old value:\"NYC\") Washington-based customers at the opening!", doc.getText().trim());

     Assert.assertEquals("\"New York City\" converted to \"Washington\" 20 characters into a 21 node." +
             "\"NYC\" converted to \"Washington\" 42 characters into a 21 node.", logger.getLog().trim());
 }

 /// 
 /// Maintains a log of every text replacement done by a find-and-replace operation
 /// and notes the original matched text's value.
 /// 
 private static class TextFindAndReplacementLogger implements IReplacingCallback {
     public int replacing(ReplacingArgs args) {
         mLog.append(MessageFormat.format("\"{0}\" converted to \"{1}\" {2} characters into a {3} node.", args.getMatch().group(0), args.getReplacement(), args.getMatchOffset(), args.getMatchNode().getNodeType()));

         args.setReplacement(MessageFormat.format("(Old value:\"{0}\") {1}", args.getMatch().group(0), args.getReplacement()));
         return ReplaceAction.REPLACE;
     }

     public String getLog() {
         return mLog.toString();
     }

     private final StringBuilder mLog = new StringBuilder();
 }
 
```

يوضح كيفية تطبيق خط مختلف على المحتوى الجديد عبر FindReplaceOptions.

```

 public void convertNumbersToHexadecimal() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     builder.getFont().setName("Arial");
     builder.writeln("Numbers that the find-and-replace operation will convert to hexadecimal and highlight:\n" +
             "123, 456, 789 and 17379.");

     // We can use a "FindReplaceOptions" object to modify the find-and-replace process.
     FindReplaceOptions options = new FindReplaceOptions();

     // Set the "HighlightColor" property to a background color that we want to apply to the operation's resulting text.
     options.getApplyFont().setHighlightColor(Color.GRAY);

     NumberHexer numberHexer = new NumberHexer();
     options.setReplacingCallback(numberHexer);

     int replacementCount = doc.getRange().replace(Pattern.compile("[0-9]+"), "", options);

     System.out.println(numberHexer.getLog());

     Assert.assertEquals(4, replacementCount);
     Assert.assertEquals("Numbers that the find-and-replace operation will convert to hexadecimal and highlight:\r" +
             "0x123, 0x456, 0x789 and 0x17,379.", doc.getText().trim());
 }

 /// 
 /// Replaces numeric find-and-replacement matches with their hexadecimal equivalents.
 /// Maintains a log of every replacement.
 /// 
 private static class NumberHexer implements IReplacingCallback {
     public int replacing(ReplacingArgs args) {
         mCurrentReplacementNumber++;

         int number = Integer.parseInt(args.getMatch().group(0));

         args.setReplacement(MessageFormat.format("0x{0}", number));

         mLog.append(MessageFormat.format("Match #{0}", mCurrentReplacementNumber));
         mLog.append(MessageFormat.format("\tOriginal value:\t{0}", args.getMatch().group(0)));
         mLog.append(MessageFormat.format("\tReplacement:\t{0}", args.getReplacement()));
         mLog.append(MessageFormat.format("\tOffset in parent {0} node:\t{1}", args.getMatchNode().getNodeType(), args.getMatchOffset()));

         return ReplaceAction.REPLACE;
     }

     public String getLog() {
         return mLog.toString();
     }

     private int mCurrentReplacementNumber;
     private final StringBuilder mLog = new StringBuilder();
 }
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| value | [IReplacingCallback](../../com.aspose.words/ireplacingcallback/) | القيمة المقابلة لـ [IReplacingCallback](../../com.aspose.words/ireplacingcallback/). |

### setSmartParagraphBreakReplacement(boolean value) {#setSmartParagraphBreakReplacement-boolean}
```
public void setSmartParagraphBreakReplacement(boolean value)
```


يحصل أو يضبط قيمة منطقية تشير إلى السماح باستبدال فاصل الفقرة عندما لا يوجد فقرة شقيقة تالية.

القيمة الافتراضية هي false.

 **Remarks:** 

يسمح هذا الخيار باستبدال فاصل الفقرة عندما لا يكون هناك فقرة شقيقة تالية يمكن نقل جميع العقد الفرعية إليها، عن طريق العثور على أي فقرة تالية (ليس بالضرورة شقيقة) بعد الفقرة التي يتم استبدالها.

 **Examples:** 

يوضح كيفية إزالة الفقرة من خلية جدول تحتوي على جدول متداخل.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create table with paragraph and inner table in first cell.
 builder.startTable();
 builder.insertCell();
 builder.write("TEXT1");
 builder.startTable();
 builder.insertCell();
 builder.endTable();
 builder.endTable();
 builder.writeln();

 FindReplaceOptions options = new FindReplaceOptions();
 // When the following option is set to 'true', Aspose.Words will remove paragraph's text
 // completely with its paragraph mark. Otherwise, Aspose.Words will mimic Word and remove
 // only paragraph's text and leaves the paragraph mark intact (when a table follows the text).
 options.setSmartParagraphBreakReplacement(isSmartParagraphBreakReplacement);
 doc.getRange().replace("TEXT1&p", "", options);

 doc.save(getArtifactsDir() + "Table.RemoveParagraphTextAndMark.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | القيمة المنطقية المقابلة. |

### setUseLegacyOrder(boolean value) {#setUseLegacyOrder-boolean}
```
public void setUseLegacyOrder(boolean value)
```


True تشير إلى أن البحث النصي يتم بشكل متسلسل من الأعلى إلى الأسفل مع مراعاة صناديق النص. القيمة الافتراضية هي false.

 **Examples:** 

يوضح كيفية تغيير ترتيب البحث عن العقد عند تنفيذ عملية البحث والاستبدال النصي.

```

 public void useLegacyOrder(boolean useLegacyOrder) throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Insert three runs which we can search for using a regex pattern.
     // Place one of those runs inside a text box.
     builder.writeln("[tag 1]");
     Shape textBox = builder.insertShape(ShapeType.TEXT_BOX, 100.0, 50.0);
     builder.writeln("[tag 2]");
     builder.moveTo(textBox.getFirstParagraph());
     builder.write("[tag 3]");

     // We can use a "FindReplaceOptions" object to modify the find-and-replace process.
     FindReplaceOptions options = new FindReplaceOptions();

     // Assign a custom callback to the "ReplacingCallback" property.
     TextReplacementTracker callback = new TextReplacementTracker();
     options.setReplacingCallback(callback);

     // If we set the "UseLegacyOrder" property to "true", the
     // find-and-replace operation will go through all the runs outside of a text box
     // before going through the ones inside a text box.
     // If we set the "UseLegacyOrder" property to "false", the
     // find-and-replace operation will go over all the runs in a range in sequential order.
     options.setUseLegacyOrder(useLegacyOrder);

     doc.getRange().replace("\[tag d*\]", "", options);
 }

 public static Object[][] useLegacyOrderDataProvider() {
     return new Object[][]
             {
                     {true},
                     {false},
             };
 }

 /// 
 /// Records the order of all matches that occur during a find-and-replace operation.
 /// 
 private static class TextReplacementTracker implements IReplacingCallback {
     public int replacing(ReplacingArgs e) {
         mMatches.add(e.getMatch().group(1));
         return ReplaceAction.REPLACE;
     }

     public ArrayList getMatches() {
         return mMatches;
     }

     private ArrayList mMatches;
 }
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | القيمة المنطقية المقابلة. |

### setUseSubstitutions(boolean value) {#setUseSubstitutions-boolean}
```
public void setUseSubstitutions(boolean value)
```


يضبط قيمة منطقية تشير إلى ما إذا كان يجب التعرف على الاستبدالات واستخدامها داخل أنماط الاستبدال. القيمة الافتراضية هي  false .

 **Remarks:** 

للتفاصيل حول عناصر الاستبدال يرجى الرجوع إلى: https://docs.microsoft.com/en-us/dotnet/standard/base-types/substitutions-in-regular-expressions.

 **Examples:** 

يوضح كيفية التعرف على الاستبدالات واستخدامها داخل أنماط الاستبدال.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.write("Jason gave money to Paul.");

 String regex = "([A-z]+) gave money to ([A-z]+)";

 FindReplaceOptions options = new FindReplaceOptions();
 options.setUseSubstitutions(true);

 // Using legacy mode does not support many advanced features, so we need to set it to 'false'.
 options.setLegacyMode(false);

 doc.getRange().replace(Pattern.compile(regex), "$2 took money from $1", options);

 Assert.assertEquals(doc.getText(), "Paul took money from Jason.\f");
 
```

يوضح كيفية استبدال النص باستخدام الاستبدالات.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("John sold a car to Paul.");
 builder.writeln("Jane sold a house to Joe.");

 // We can use a "FindReplaceOptions" object to modify the find-and-replace process.
 FindReplaceOptions options = new FindReplaceOptions();

 // Set the "UseSubstitutions" property to "true" to get
 // the find-and-replace operation to recognize substitution elements.
 // Set the "UseSubstitutions" property to "false" to ignore substitution elements.
 options.setUseSubstitutions(useSubstitutions);

 doc.getRange().replace(Pattern.compile("([A-z]+) sold a ([A-z]+) to ([A-z]+)"), "$3 bought a $2 from $1", options);

 Assert.assertEquals(
         useSubstitutions
                 ? "Paul bought a car from John.\rJoe bought a house from Jane."
                 : "$3 bought a $2 from $1.\r$3 bought a $2 from $1.", doc.getText().trim());
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | قيمة منطقية تشير إلى ما إذا كان يجب التعرف على الاستبدالات واستخدامها داخل أنماط الاستبدال. |

