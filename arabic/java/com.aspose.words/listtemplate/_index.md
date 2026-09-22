---
title: "ListTemplate"
linktitle: "ListTemplate"
second_title: "Aspose.Words لـ Java"
description: "يحدد أحد تنسيقات القوائم المعرفة مسبقًا المتاحة في Microsoft Word في Java."
type: docs
weight: 432
url: /ar/java/com.aspose.words/listtemplate/
---

**Inheritance:**
java.lang.Object
```
public class ListTemplate
```

يحدد أحد تنسيقات القوائم المعرفة مسبقًا المتوفرة في Microsoft Word.

 **Remarks:** 

يتم استخدام قيمة قالب القائمة كمعامل في طريقة **M:Aspose.Words.Lists.ListCollection.Add(Aspose.Words.Lists.ListTemplate)**.

قوالب القوائم في Aspose.Words تتطابق مع 21 قالب قائمة المتاحة في مربع حوار الرموز النقطية والترقيم في Microsoft Word 2003.

 **Examples:** 

يعرض كيفية العمل مع مستويات القوائم.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Assert.assertFalse(builder.getListFormat().isListItem());

 // A list allows us to organize and decorate sets of paragraphs with prefix symbols and indents.
 // We can create nested lists by increasing the indent level.
 // We can begin and end a list by using a document builder's "ListFormat" property.
 // Each paragraph that we add between a list's start and the end will become an item in the list.
 // Below are two types of lists that we can create using a document builder.
 // 1 -  A numbered list:
 // Numbered lists create a logical order for their paragraphs by numbering each item.
 builder.getListFormat().setList(doc.getLists().add(ListTemplate.NUMBER_DEFAULT));

 Assert.assertTrue(builder.getListFormat().isListItem());

 // By setting the "ListLevelNumber" property, we can increase the list level
 // to begin a self-contained sub-list at the current list item.
 // The Microsoft Word list template called "NumberDefault" uses numbers to create list levels for the first list level.
 // Deeper list levels use letters and lowercase Roman numerals.
 for (int i = 0; i < 9; i++) {
     builder.getListFormat().setListLevelNumber(i);
     builder.writeln("Level " + i);
 }

 // 2 -  A bulleted list:
 // This list will apply an indent and a bullet symbol ("\u2022") before each paragraph.
 // Deeper levels of this list will use different symbols, such as "\u25a0" and "\u25cb".
 builder.getListFormat().setList(doc.getLists().add(ListTemplate.BULLET_DEFAULT));

 for (int i = 0; i < 9; i++) {
     builder.getListFormat().setListLevelNumber(i);
     builder.writeln("Level " + i);
 }

 // We can disable list formatting to not format any subsequent paragraphs as lists by un-setting the "List" flag.
 builder.getListFormat().setList(null);

 Assert.assertFalse(builder.getListFormat().isListItem());

 doc.save(getArtifactsDir() + "Lists.SpecifyListLevel.docx");
 
```

يعرض كيفية إعادة بدء الترقيم في قائمة عن طريق نسخ القائمة.

```

 Document doc = new Document();

 // A list allows us to organize and decorate sets of paragraphs with prefix symbols and indents.
 // We can create nested lists by increasing the indent level.
 // We can begin and end a list by using a document builder's "ListFormat" property.
 // Each paragraph that we add between a list's start and the end will become an item in the list.
 // Create a list from a Microsoft Word template, and customize its first list level.
 List list1 = doc.getLists().add(ListTemplate.NUMBER_ARABIC_PARENTHESIS);
 list1.getListLevels().get(0).getFont().setColor(Color.RED);
 list1.getListLevels().get(0).setAlignment(ListLevelAlignment.RIGHT);

 // Apply our list to some paragraphs.
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("List 1 starts below:");
 builder.getListFormat().setList(list1);
 builder.writeln("Item 1");
 builder.writeln("Item 2");
 builder.getListFormat().removeNumbers();

 // We can add a copy of an existing list to the document's list collection
 // to create a similar list without making changes to the original.
 List list2 = doc.getLists().addCopy(list1);
 list2.getListLevels().get(0).getFont().setColor(Color.BLUE);
 list2.getListLevels().get(0).setStartAt(10);

 // Apply the second list to new paragraphs.
 builder.writeln("List 2 starts below:");
 builder.getListFormat().setList(list2);
 builder.writeln("Item 1");
 builder.writeln("Item 2");
 builder.getListFormat().removeNumbers();

 doc.save(getArtifactsDir() + "Lists.RestartNumberingUsingListCopy.docx");
 
```

يعرض كيفية إنشاء مستند يحتوي على جميع قوالب قوائم عناوين المخطط.

```

 public void outlineHeadingTemplates() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     List docList = doc.getLists().add(ListTemplate.OUTLINE_HEADINGS_ARTICLE_SECTION);
     addOutlineHeadingParagraphs(builder, docList, "Aspose.Words Outline - \"Article Section\"");

     docList = doc.getLists().add(ListTemplate.OUTLINE_HEADINGS_LEGAL);
     addOutlineHeadingParagraphs(builder, docList, "Aspose.Words Outline - \"Legal\"");

     builder.insertBreak(BreakType.PAGE_BREAK);

     docList = doc.getLists().add(ListTemplate.OUTLINE_HEADINGS_NUMBERS);
     addOutlineHeadingParagraphs(builder, docList, "Aspose.Words Outline - \"Numbers\"");

     docList = doc.getLists().add(ListTemplate.OUTLINE_HEADINGS_CHAPTER);
     addOutlineHeadingParagraphs(builder, docList, "Aspose.Words Outline - \"Chapters\"");

     doc.save(getArtifactsDir() + "Lists.OutlineHeadingTemplates.docx");
 }

 private static void addOutlineHeadingParagraphs(final DocumentBuilder builder, final List docList, final String title) {
     builder.getParagraphFormat().clearFormatting();
     builder.writeln(title);

     for (int i = 0; i < 9; i++) {
         builder.getListFormat().setList(docList);
         builder.getListFormat().setListLevelNumber(i);

         String styleName = "Heading " + (i + 1);
         builder.getParagraphFormat().setStyleName(styleName);
         builder.writeln(styleName);
     }

     builder.getListFormat().removeNumbers();
 }
 
```
## الحقول

| حقل | الوصف |
| --- | --- |
| [BULLET_ARROW_HEAD](#BULLET-ARROW-HEAD) | رمز النقطة للمستوى الأول هو حرف Wingding على شكل رأس سهم. |
| [BULLET_CIRCLE](#BULLET-CIRCLE) | رمز النقطة للمستوى الأول هو دائرة. |
| [BULLET_DEFAULT](#BULLET-DEFAULT) | قائمة نقطية افتراضية مع 9 مستويات. |
| [BULLET_DIAMONDS](#BULLET-DIAMONDS) | رمز النقطة للمستوى الأول هو حرف Wingding على شكل 4 ألماس. |
| [BULLET_DISK](#BULLET-DISK) | نفسه مثل [BULLET\_DEFAULT](../../com.aspose.words/listtemplate/\#BULLET-DEFAULT). |
| [BULLET_SQUARE](#BULLET-SQUARE) | رمز النقطة للمستوى الأول هو مربع. |
| [BULLET_TICK](#BULLET-TICK) | رمز النقطة للمستوى الأول هو حرف Wingding على شكل علامة اختيار. |
| [NUMBER_ARABIC_DOT](#NUMBER-ARABIC-DOT) | نفسه مثل [NUMBER\_DEFAULT](../../com.aspose.words/listtemplate/\#NUMBER-DEFAULT). |
| [NUMBER_ARABIC_PARENTHESIS](#NUMBER-ARABIC-PARENTHESIS) | رقم المستوى الأول هو "1)". |
| [NUMBER_DEFAULT](#NUMBER-DEFAULT) | قائمة مرقمة افتراضية مع 9 مستويات. |
| [NUMBER_LOWERCASE_LETTER_DOT](#NUMBER-LOWERCASE-LETTER-DOT) | رقم المستوى الأول هو "a.". |
| [NUMBER_LOWERCASE_LETTER_PARENTHESIS](#NUMBER-LOWERCASE-LETTER-PARENTHESIS) | رقم المستوى الأول هو "a)". |
| [NUMBER_LOWERCASE_ROMAN_DOT](#NUMBER-LOWERCASE-ROMAN-DOT) | رقم المستوى الأول هو "i.". |
| [NUMBER_UPPERCASE_LETTER_DOT](#NUMBER-UPPERCASE-LETTER-DOT) | رقم المستوى الأول هو "A.". |
| [NUMBER_UPPERCASE_ROMAN_DOT](#NUMBER-UPPERCASE-ROMAN-DOT) | رقم المستوى الأول هو "I.". |
| [OUTLINE_BULLETS](#OUTLINE-BULLETS) | قائمة مخطط تحتوي على نقاط متنوعة للمستويات المختلفة. |
| [OUTLINE_HEADINGS_ARTICLE_SECTION](#OUTLINE-HEADINGS-ARTICLE-SECTION) | قائمة مخطط مع مستويات مرتبطة بأنماط العناوين. |
| [OUTLINE_HEADINGS_CHAPTER](#OUTLINE-HEADINGS-CHAPTER) | قائمة مخطط مع مستويات مرتبطة بأنماط العناوين. |
| [OUTLINE_HEADINGS_LEGAL](#OUTLINE-HEADINGS-LEGAL) | قائمة مخطط مع مستويات مرتبطة بأنماط العناوين. |
| [OUTLINE_HEADINGS_NUMBERS](#OUTLINE-HEADINGS-NUMBERS) | قائمة مخطط مع مستويات مرتبطة بأنماط العناوين. |
| [OUTLINE_LEGAL](#OUTLINE-LEGAL) | قائمة مخطط مع مستويات مرقمة "1., 1.1., 1.1.1, ...". |
| [OUTLINE_NUMBERS](#OUTLINE-NUMBERS) | قائمة مخطط مع مستويات مرقمة "1), a), i), (1), (a), (i), 1., a., i.". |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String listTemplateName)](#fromName-java.lang.String) |  |
| [getName(int listTemplate)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int listTemplate)](#toString-int) |  |
### BULLET_ARROW_HEAD {#BULLET-ARROW-HEAD}
```
public static int BULLET_ARROW_HEAD
```


النقطة في المستوى الأول هي حرف Wingding على شكل رأس سهم. المستويات المتبقية هي نفسها كما في [BULLET\_DEFAULT](../../com.aspose.words/listtemplate/\#BULLET-DEFAULT).

يتطابق مع قالب القائمة النقطية السادس في مربع الحوار القوائم النقطية والترقيم في Microsoft Word.

### BULLET_CIRCLE {#BULLET-CIRCLE}
```
public static int BULLET_CIRCLE
```


النقطة في المستوى الأول هي دائرة. المستويات المتبقية هي نفسها كما في [BULLET\_DEFAULT](../../com.aspose.words/listtemplate/\#BULLET-DEFAULT).

يتطابق مع قالب القائمة النقطية الثاني في مربع الحوار القوائم النقطية والترقيم في Microsoft Word.

### BULLET_DEFAULT {#BULLET-DEFAULT}
```
public static int BULLET_DEFAULT
```


قائمة نقطية افتراضية مع 9 مستويات. النقطة في المستوى الأول هي قرص، النقطة في المستوى الثاني هي دائرة، النقطة في المستوى الثالث هي مربع. ثم يتكرر التنسيق للمستويات المتبقية.

كل مستوى مُزاح إلى اليمين بمقدار 0.25" مقارنة بالمستوى السابق.

يتطابق مع قالب القائمة النقطية الأول في مربع الحوار القوائم النقطية والترقيم في Microsoft Word.

### BULLET_DIAMONDS {#BULLET-DIAMONDS}
```
public static int BULLET_DIAMONDS
```


النقطة في المستوى الأول هي حرف Wingding على شكل 4 ألماس. المستويات المتبقية هي نفسها كما في [BULLET\_DEFAULT](../../com.aspose.words/listtemplate/\#BULLET-DEFAULT).

يتطابق مع قالب القائمة النقطية الخامس في مربع الحوار القوائم النقطية والترقيم في Microsoft Word.

### BULLET_DISK {#BULLET-DISK}
```
public static int BULLET_DISK
```


نفسه مثل [BULLET\_DEFAULT](../../com.aspose.words/listtemplate/\#BULLET-DEFAULT).

يتطابق مع قالب القائمة النقطية الأول في مربع الحوار القوائم النقطية والترقيم في Microsoft Word.

### BULLET_SQUARE {#BULLET-SQUARE}
```
public static int BULLET_SQUARE
```


النقطة في المستوى الأول هي مربع. المستويات المتبقية هي نفسها كما في [BULLET\_DEFAULT](../../com.aspose.words/listtemplate/\#BULLET-DEFAULT).

يتطابق مع قالب القائمة النقطية الثالث في مربع الحوار القوائم النقطية والترقيم في Microsoft Word.

### BULLET_TICK {#BULLET-TICK}
```
public static int BULLET_TICK
```


النقطة في المستوى الأول هي حرف Wingding على شكل علامة صح. المستويات المتبقية هي نفسها كما في [BULLET\_DEFAULT](../../com.aspose.words/listtemplate/\#BULLET-DEFAULT).

يتطابق مع قالب القائمة النقطية السابع في مربع الحوار القوائم النقطية والترقيم في Microsoft Word.

### NUMBER_ARABIC_DOT {#NUMBER-ARABIC-DOT}
```
public static int NUMBER_ARABIC_DOT
```


نفسه مثل [NUMBER\_DEFAULT](../../com.aspose.words/listtemplate/\#NUMBER-DEFAULT).

يتطابق مع قالب القائمة المرقمة الأول في مربع الحوار القوائم النقطية والترقيم في Microsoft Word.

### NUMBER_ARABIC_PARENTHESIS {#NUMBER-ARABIC-PARENTHESIS}
```
public static int NUMBER_ARABIC_PARENTHESIS
```


رقم المستوى الأول هو "1)". المستويات المتبقية هي نفسها كما في [NUMBER\_DEFAULT](../../com.aspose.words/listtemplate/\#NUMBER-DEFAULT).

يتطابق مع قالب القائمة المرقمة الثاني في مربع الحوار القوائم النقطية والترقيم في Microsoft Word.

### NUMBER_DEFAULT {#NUMBER-DEFAULT}
```
public static int NUMBER_DEFAULT
```


قائمة مرقمة افتراضية مع 9 مستويات. ترقيم عربي (1., 2., 3., ...) للمستوى الأول، ترقيم بحروف صغيرة (a., b., c., ...) للمستوى الثاني، ترقيم روماني بحروف صغيرة (i., ii., iii., ...) للمستوى الثالث. ثم يتكرر التنسيق للمستويات المتبقية.

كل مستوى مُزاح إلى اليمين بمقدار 0.25" مقارنة بالمستوى السابق.

يتطابق مع قالب القائمة المرقمة الأول في مربع الحوار القوائم النقطية والترقيم في Microsoft Word.

### NUMBER_LOWERCASE_LETTER_DOT {#NUMBER-LOWERCASE-LETTER-DOT}
```
public static int NUMBER_LOWERCASE_LETTER_DOT
```


رقم المستوى الأول هو "a.". المستويات المتبقية هي نفسها كما في [NUMBER\_DEFAULT](../../com.aspose.words/listtemplate/\#NUMBER-DEFAULT).

يتطابق مع قالب القائمة المرقمة السادس في مربع حوار النقاط والترقيم في Microsoft Word.

### NUMBER_LOWERCASE_LETTER_PARENTHESIS {#NUMBER-LOWERCASE-LETTER-PARENTHESIS}
```
public static int NUMBER_LOWERCASE_LETTER_PARENTHESIS
```


رقم المستوى الأول هو "a)". المستويات المتبقية هي نفسها كما في [NUMBER\\_DEFAULT](../../com.aspose.words/listtemplate/\\#NUMBER-DEFAULT).

يتطابق مع قالب القائمة المرقمة الخامس في مربع حوار النقاط والترقيم في Microsoft Word.

### NUMBER_LOWERCASE_ROMAN_DOT {#NUMBER-LOWERCASE-ROMAN-DOT}
```
public static int NUMBER_LOWERCASE_ROMAN_DOT
```


رقم المستوى الأول هو "i.". المستويات المتبقية هي نفسها كما في [NUMBER\\_DEFAULT](../../com.aspose.words/listtemplate/\\#NUMBER-DEFAULT).

يتطابق مع قالب القائمة المرقمة السابع في مربع حوار النقاط والترقيم في Microsoft Word.

### NUMBER_UPPERCASE_LETTER_DOT {#NUMBER-UPPERCASE-LETTER-DOT}
```
public static int NUMBER_UPPERCASE_LETTER_DOT
```


رقم المستوى الأول هو "A.". المستويات المتبقية هي نفسها كما في [NUMBER\\_DEFAULT](../../com.aspose.words/listtemplate/\\#NUMBER-DEFAULT).

يتطابق مع قالب القائمة المرقمة الرابع في مربع حوار النقاط والترقيم في Microsoft Word.

### NUMBER_UPPERCASE_ROMAN_DOT {#NUMBER-UPPERCASE-ROMAN-DOT}
```
public static int NUMBER_UPPERCASE_ROMAN_DOT
```


رقم المستوى الأول هو "I.". المستويات المتبقية هي نفسها كما في [NUMBER\\_DEFAULT](../../com.aspose.words/listtemplate/\\#NUMBER-DEFAULT).

يتطابق مع قالب القائمة المرقمة الثالث في مربع حوار النقاط والترقيم في Microsoft Word.

### OUTLINE_BULLETS {#OUTLINE-BULLETS}
```
public static int OUTLINE_BULLETS
```


قائمة مخطط تحتوي على نقاط متنوعة للمستويات المختلفة.

يتطابق مع قالب القائمة التخطيطية الثالث في مربع حوار النقاط والترقيم في Microsoft Word.

### OUTLINE_HEADINGS_ARTICLE_SECTION {#OUTLINE-HEADINGS-ARTICLE-SECTION}
```
public static int OUTLINE_HEADINGS_ARTICLE_SECTION
```


قائمة مخطط مع مستويات مرتبطة بأنماط العناوين.

يتطابق مع قالب القائمة التخطيطية الرابع في مربع حوار النقاط والترقيم في Microsoft Word.

### OUTLINE_HEADINGS_CHAPTER {#OUTLINE-HEADINGS-CHAPTER}
```
public static int OUTLINE_HEADINGS_CHAPTER
```


قائمة مخطط مع مستويات مرتبطة بأنماط العناوين.

يتطابق مع قالب القائمة التخطيطية السابع في مربع حوار النقاط والترقيم في Microsoft Word.

### OUTLINE_HEADINGS_LEGAL {#OUTLINE-HEADINGS-LEGAL}
```
public static int OUTLINE_HEADINGS_LEGAL
```


قائمة مخطط مع مستويات مرتبطة بأنماط العناوين.

يتطابق مع قالب القائمة التخطيطية الخامس في مربع حوار النقاط والترقيم في Microsoft Word.

### OUTLINE_HEADINGS_NUMBERS {#OUTLINE-HEADINGS-NUMBERS}
```
public static int OUTLINE_HEADINGS_NUMBERS
```


قائمة مخطط مع مستويات مرتبطة بأنماط العناوين.

يتطابق مع قالب القائمة التخطيطية السادس في مربع حوار النقاط والترقيم في Microsoft Word.

### OUTLINE_LEGAL {#OUTLINE-LEGAL}
```
public static int OUTLINE_LEGAL
```


قائمة مخطط مع مستويات مرقمة "1., 1.1., 1.1.1, ...".

يتطابق مع قالب القائمة التخطيطية الثاني في مربع حوار النقاط والترقيم في Microsoft Word.

### OUTLINE_NUMBERS {#OUTLINE-NUMBERS}
```
public static int OUTLINE_NUMBERS
```


قائمة مخطط مع مستويات مرقمة "1), a), i), (1), (a), (i), 1., a., i.".

يتطابق مع قالب القائمة التخطيطية الأول في مربع حوار النقاط والترقيم في Microsoft Word.

### length {#length}
```
public static int length
```


### fromName(String listTemplateName) {#fromName-java.lang.String}
```
public static int fromName(String listTemplateName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| listTemplateName | java.lang.String |  |

**Returns:**
int
### getName(int listTemplate) {#getName-int}
```
public static String getName(int listTemplate)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| listTemplate | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int listTemplate) {#toString-int}
```
public static String toString(int listTemplate)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| listTemplate | int |  |

**Returns:**
java.lang.String
