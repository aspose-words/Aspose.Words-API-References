---
title: "ListTemplate"
linktitle: "ListTemplate"
second_title: "Aspose.Words для Java"
description: "Указывает один из предопределённых форматов списков, доступных в Microsoft Word для Java."
type: docs
weight: 432
url: /ru/java/com.aspose.words/listtemplate/
---

**Inheritance:**
java.lang.Object
```
public class ListTemplate
```

Указывает один из предопределённых форматов списков, доступных в Microsoft Word.

 **Remarks:** 

Значение шаблона списка используется в качестве параметра метода **M:Aspose.Words.Lists.ListCollection.Add(Aspose.Words.Lists.ListTemplate)**.

Шаблоны списков Aspose.Words соответствуют 21 шаблону списков, доступным в диалоговом окне Маркеры и нумерация в Microsoft Word 2003.

 **Examples:** 

Показывает, как работать с уровнями списка.

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

Показывает, как перезапустить нумерацию в списке, копируя список.

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

Показывает, как создать документ, содержащий все шаблоны списков заголовков структуры.

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
## Поля

| Поле | Описание |
| --- | --- |
| [BULLET_ARROW_HEAD](#BULLET-ARROW-HEAD) | Маркер первого уровня — символ Wingding в виде стрелки. |
| [BULLET_CIRCLE](#BULLET-CIRCLE) | Маркер первого уровня — круг. |
| [BULLET_DEFAULT](#BULLET-DEFAULT) | Список с маркерами по умолчанию, содержащий 9 уровней. |
| [BULLET_DIAMONDS](#BULLET-DIAMONDS) | Маркер первого уровня — символ Wingding в виде четырёх ромбов. |
| [BULLET_DISK](#BULLET-DISK) | То же, что и [BULLET\_DEFAULT](../../com.aspose.words/listtemplate/\#BULLET-DEFAULT). |
| [BULLET_SQUARE](#BULLET-SQUARE) | Маркер первого уровня — квадрат. |
| [BULLET_TICK](#BULLET-TICK) | Маркер первого уровня — символ Wingding в виде галочки. |
| [NUMBER_ARABIC_DOT](#NUMBER-ARABIC-DOT) | То же, что и [NUMBER\_DEFAULT](../../com.aspose.words/listtemplate/\#NUMBER-DEFAULT). |
| [NUMBER_ARABIC_PARENTHESIS](#NUMBER-ARABIC-PARENTHESIS) | Номер первого уровня — "1)". |
| [NUMBER_DEFAULT](#NUMBER-DEFAULT) | Нумерованный список по умолчанию, содержащий 9 уровней. |
| [NUMBER_LOWERCASE_LETTER_DOT](#NUMBER-LOWERCASE-LETTER-DOT) | Номер первого уровня — "a.". |
| [NUMBER_LOWERCASE_LETTER_PARENTHESIS](#NUMBER-LOWERCASE-LETTER-PARENTHESIS) | Номер первого уровня — "a)". |
| [NUMBER_LOWERCASE_ROMAN_DOT](#NUMBER-LOWERCASE-ROMAN-DOT) | Номер первого уровня — "i.". |
| [NUMBER_UPPERCASE_LETTER_DOT](#NUMBER-UPPERCASE-LETTER-DOT) | Номер первого уровня — "A.". |
| [NUMBER_UPPERCASE_ROMAN_DOT](#NUMBER-UPPERCASE-ROMAN-DOT) | Номер первого уровня — "I.". |
| [OUTLINE_BULLETS](#OUTLINE-BULLETS) | Контурный список содержит различные маркеры для разных уровней. |
| [OUTLINE_HEADINGS_ARTICLE_SECTION](#OUTLINE-HEADINGS-ARTICLE-SECTION) | Контурный список с уровнями, связанными со стилями заголовков. |
| [OUTLINE_HEADINGS_CHAPTER](#OUTLINE-HEADINGS-CHAPTER) | Контурный список с уровнями, связанными со стилями заголовков. |
| [OUTLINE_HEADINGS_LEGAL](#OUTLINE-HEADINGS-LEGAL) | Контурный список с уровнями, связанными со стилями заголовков. |
| [OUTLINE_HEADINGS_NUMBERS](#OUTLINE-HEADINGS-NUMBERS) | Контурный список с уровнями, связанными со стилями заголовков. |
| [OUTLINE_LEGAL](#OUTLINE-LEGAL) | Контурный список, где уровни нумеруются "1., 1.1., 1.1.1, ...". |
| [OUTLINE_NUMBERS](#OUTLINE-NUMBERS) | Контурный список, где уровни нумеруются "1), a), i), (1), (a), (i), 1., a., i.". |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [fromName(String listTemplateName)](#fromName-java.lang.String) |  |
| [getName(int listTemplate)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int listTemplate)](#toString-int) |  |
### BULLET_ARROW_HEAD {#BULLET-ARROW-HEAD}
```
public static int BULLET_ARROW_HEAD
```


Маркер первого уровня — символ Wingding в виде стрелки. Остальные уровни такие же, как в [BULLET\_DEFAULT](../../com.aspose.words/listtemplate/\#BULLET-DEFAULT).

Соответствует 6‑му шаблону маркированного списка в диалоговом окне Маркеры и нумерация в Microsoft Word.

### BULLET_CIRCLE {#BULLET-CIRCLE}
```
public static int BULLET_CIRCLE
```


Маркер первого уровня — круг. Остальные уровни такие же, как в [BULLET\_DEFAULT](../../com.aspose.words/listtemplate/\#BULLET-DEFAULT).

Соответствует 2‑му шаблону маркированного списка в диалоговом окне Маркеры и нумерация в Microsoft Word.

### BULLET_DEFAULT {#BULLET-DEFAULT}
```
public static int BULLET_DEFAULT
```


Стандартный маркированный список с 9 уровнями. Маркер первого уровня — диск, маркер второго уровня — круг, маркер третьего уровня — квадрат. Затем форматирование повторяется для остальных уровней.

Каждый уровень отступает вправо на 0.25" относительно предыдущего уровня.

Соответствует 1‑му шаблону маркированного списка в диалоговом окне Маркеры и нумерация в Microsoft Word.

### BULLET_DIAMONDS {#BULLET-DIAMONDS}
```
public static int BULLET_DIAMONDS
```


Маркер первого уровня — символ Wingding в виде 4‑угольного ромба. Остальные уровни такие же, как в [BULLET\_DEFAULT](../../com.aspose.words/listtemplate/\#BULLET-DEFAULT).

Соответствует 5‑му шаблону маркированного списка в диалоговом окне Маркеры и нумерация в Microsoft Word.

### BULLET_DISK {#BULLET-DISK}
```
public static int BULLET_DISK
```


То же, что и [BULLET\_DEFAULT](../../com.aspose.words/listtemplate/\#BULLET-DEFAULT).

Соответствует 1‑му шаблону маркированного списка в диалоговом окне Маркеры и нумерация в Microsoft Word.

### BULLET_SQUARE {#BULLET-SQUARE}
```
public static int BULLET_SQUARE
```


Маркер первого уровня — квадрат. Остальные уровни такие же, как в [BULLET\_DEFAULT](../../com.aspose.words/listtemplate/\#BULLET-DEFAULT).

Соответствует 3‑му шаблону маркированного списка в диалоговом окне Маркеры и нумерация в Microsoft Word.

### BULLET_TICK {#BULLET-TICK}
```
public static int BULLET_TICK
```


Маркер первого уровня — символ Wingding в виде галочки. Остальные уровни такие же, как в [BULLET\_DEFAULT](../../com.aspose.words/listtemplate/\#BULLET-DEFAULT).

Соответствует 7‑му шаблону маркированного списка в диалоговом окне Маркеры и нумерация в Microsoft Word.

### NUMBER_ARABIC_DOT {#NUMBER-ARABIC-DOT}
```
public static int NUMBER_ARABIC_DOT
```


То же, что и [NUMBER\_DEFAULT](../../com.aspose.words/listtemplate/\#NUMBER-DEFAULT).

Соответствует 1‑му шаблону нумерованного списка в диалоговом окне Маркеры и нумерация в Microsoft Word.

### NUMBER_ARABIC_PARENTHESIS {#NUMBER-ARABIC-PARENTHESIS}
```
public static int NUMBER_ARABIC_PARENTHESIS
```


Номер первого уровня — "1)". Остальные уровни такие же, как в [NUMBER\_DEFAULT](../../com.aspose.words/listtemplate/\#NUMBER-DEFAULT).

Соответствует 2‑му шаблону нумерованного списка в диалоговом окне Маркеры и нумерация в Microsoft Word.

### NUMBER_DEFAULT {#NUMBER-DEFAULT}
```
public static int NUMBER_DEFAULT
```


Стандартный нумерованный список с 9 уровнями. Арабская нумерация (1., 2., 3., ...) для первого уровня, нумерация строчными буквами (a., b., c., ...) для второго уровня, нумерация строчными римскими цифрами (i., ii., iii., ...) для третьего уровня. Затем форматирование повторяется для остальных уровней.

Каждый уровень отступает вправо на 0.25" относительно предыдущего уровня.

Соответствует 1‑му шаблону нумерованного списка в диалоговом окне Маркеры и нумерация в Microsoft Word.

### NUMBER_LOWERCASE_LETTER_DOT {#NUMBER-LOWERCASE-LETTER-DOT}
```
public static int NUMBER_LOWERCASE_LETTER_DOT
```


Номер первого уровня — "a.". Остальные уровни такие же, как в [NUMBER\_DEFAULT](../../com.aspose.words/listtemplate/\#NUMBER-DEFAULT).

Соответствует 6‑му шаблону нумерованного списка в диалоговом окне Маркеры и нумерация в Microsoft Word.

### NUMBER_LOWERCASE_LETTER_PARENTHESIS {#NUMBER-LOWERCASE-LETTER-PARENTHESIS}
```
public static int NUMBER_LOWERCASE_LETTER_PARENTHESIS
```


Номер первого уровня — "a)". Остальные уровни такие же, как в [NUMBER\_DEFAULT](../../com.aspose.words/listtemplate/\#NUMBER-DEFAULT).

Соответствует 5‑му шаблону нумерованного списка в диалоговом окне Маркеры и нумерация в Microsoft Word.

### NUMBER_LOWERCASE_ROMAN_DOT {#NUMBER-LOWERCASE-ROMAN-DOT}
```
public static int NUMBER_LOWERCASE_ROMAN_DOT
```


Номер первого уровня — "i.". Остальные уровни такие же, как в [NUMBER\_DEFAULT](../../com.aspose.words/listtemplate/\#NUMBER-DEFAULT).

Соответствует 7‑му шаблону нумерованного списка в диалоговом окне Маркеры и нумерация в Microsoft Word.

### NUMBER_UPPERCASE_LETTER_DOT {#NUMBER-UPPERCASE-LETTER-DOT}
```
public static int NUMBER_UPPERCASE_LETTER_DOT
```


Номер первого уровня — "A.". Остальные уровни такие же, как в [NUMBER\_DEFAULT](../../com.aspose.words/listtemplate/\#NUMBER-DEFAULT).

Соответствует 4‑му шаблону нумерованного списка в диалоговом окне Маркеры и нумерация в Microsoft Word.

### NUMBER_UPPERCASE_ROMAN_DOT {#NUMBER-UPPERCASE-ROMAN-DOT}
```
public static int NUMBER_UPPERCASE_ROMAN_DOT
```


Номер первого уровня — "I.". Остальные уровни такие же, как в [NUMBER\_DEFAULT](../../com.aspose.words/listtemplate/\#NUMBER-DEFAULT).

Соответствует 3‑му шаблону нумерованного списка в диалоговом окне Маркеры и нумерация в Microsoft Word.

### OUTLINE_BULLETS {#OUTLINE-BULLETS}
```
public static int OUTLINE_BULLETS
```


Контурный список содержит различные маркеры для разных уровней.

Соответствует 3‑му шаблону контурного списка в диалоговом окне Маркеры и нумерация в Microsoft Word.

### OUTLINE_HEADINGS_ARTICLE_SECTION {#OUTLINE-HEADINGS-ARTICLE-SECTION}
```
public static int OUTLINE_HEADINGS_ARTICLE_SECTION
```


Контурный список с уровнями, связанными со стилями заголовков.

Соответствует 4‑му шаблону контурного списка в диалоговом окне Маркеры и нумерация в Microsoft Word.

### OUTLINE_HEADINGS_CHAPTER {#OUTLINE-HEADINGS-CHAPTER}
```
public static int OUTLINE_HEADINGS_CHAPTER
```


Контурный список с уровнями, связанными со стилями заголовков.

Соответствует 7‑му шаблону контурного списка в диалоговом окне Маркеры и нумерация в Microsoft Word.

### OUTLINE_HEADINGS_LEGAL {#OUTLINE-HEADINGS-LEGAL}
```
public static int OUTLINE_HEADINGS_LEGAL
```


Контурный список с уровнями, связанными со стилями заголовков.

Соответствует 5‑му шаблону контурного списка в диалоговом окне Маркеры и нумерация в Microsoft Word.

### OUTLINE_HEADINGS_NUMBERS {#OUTLINE-HEADINGS-NUMBERS}
```
public static int OUTLINE_HEADINGS_NUMBERS
```


Контурный список с уровнями, связанными со стилями заголовков.

Соответствует 6‑му шаблону контурного списка в диалоговом окне Маркеры и нумерация в Microsoft Word.

### OUTLINE_LEGAL {#OUTLINE-LEGAL}
```
public static int OUTLINE_LEGAL
```


Контурный список, где уровни нумеруются "1., 1.1., 1.1.1, ...".

Соответствует 2‑му шаблону контурного списка в диалоговом окне Маркеры и нумерация в Microsoft Word.

### OUTLINE_NUMBERS {#OUTLINE-NUMBERS}
```
public static int OUTLINE_NUMBERS
```


Контурный список, где уровни нумеруются "1), a), i), (1), (a), (i), 1., a., i.".

Соответствует 1‑му шаблону контурного списка в диалоговом окне Маркеры и нумерация в Microsoft Word.

### length {#length}
```
public static int length
```


### fromName(String listTemplateName) {#fromName-java.lang.String}
```
public static int fromName(String listTemplateName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| listTemplateName | java.lang.String |  |

**Returns:**
int
### getName(int listTemplate) {#getName-int}
```
public static String getName(int listTemplate)
```




**Parameters:**
| Параметр | Тип | Описание |
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
| Параметр | Тип | Описание |
| --- | --- | --- |
| listTemplate | int |  |

**Returns:**
java.lang.String
