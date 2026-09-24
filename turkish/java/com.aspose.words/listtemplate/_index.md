---
title: "ListTemplate"
linktitle: "ListTemplate"
second_title: "Aspose.Words Java için"
description: "Microsoft Word'ün Java sürümünde mevcut önceden tanımlanmış liste biçimlerinden birini belirtir."
type: docs
weight: 432
url: /tr/java/com.aspose.words/listtemplate/
---

**Inheritance:**
java.lang.Object
```
public class ListTemplate
```

Microsoft Word'de mevcut önceden tanımlanmış liste biçimlerinden birini belirtir.

 **Remarks:** 

Bir liste şablonu değeri, **M:Aspose.Words.Lists.ListCollection.Add(Aspose.Words.Lists.ListTemplate)** yöntemine bir parametre olarak kullanılır.

Aspose.Words liste şablonları, Microsoft Word 2003'teki Madde İşaretleri ve Numaralandırma iletişim kutusunda bulunan 21 liste şablonuna karşılık gelir.

 **Examples:** 

Liste seviyeleriyle nasıl çalışılacağını gösterir.

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

Bir listeyi kopyalayarak listede numaralandırmayı nasıl yeniden başlatacağını gösterir.

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

Tüm taslak başlıkları liste şablonlarını içeren bir belge nasıl oluşturulacağını gösterir.

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
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [BULLET_ARROW_HEAD](#BULLET-ARROW-HEAD) | İlk seviyenin madde işareti bir ok başı Wingding karakteridir. |
| [BULLET_CIRCLE](#BULLET-CIRCLE) | İlk seviyenin madde işareti bir dairedir. |
| [BULLET_DEFAULT](#BULLET-DEFAULT) | 9 seviyeli varsayılan madde işaretli liste. |
| [BULLET_DIAMONDS](#BULLET-DIAMONDS) | İlk seviyenin madde işareti bir 4-karo Wingding karakteridir. |
| [BULLET_DISK](#BULLET-DISK) | Aynı [BULLET\_DEFAULT](../../com.aspose.words/listtemplate/\#BULLET-DEFAULT) ile. |
| [BULLET_SQUARE](#BULLET-SQUARE) | İlk seviyenin madde işareti bir karedir. |
| [BULLET_TICK](#BULLET-TICK) | İlk seviyenin madde işareti bir tik Wingding karakteridir. |
| [NUMBER_ARABIC_DOT](#NUMBER-ARABIC-DOT) | Aynı [NUMBER\_DEFAULT](../../com.aspose.words/listtemplate/\#NUMBER-DEFAULT) ile. |
| [NUMBER_ARABIC_PARENTHESIS](#NUMBER-ARABIC-PARENTHESIS) | İlk seviyenin numarası "1)"'dir. |
| [NUMBER_DEFAULT](#NUMBER-DEFAULT) | 9 seviyeli varsayılan numaralı liste. |
| [NUMBER_LOWERCASE_LETTER_DOT](#NUMBER-LOWERCASE-LETTER-DOT) | İlk seviyenin numarası "a."'dır. |
| [NUMBER_LOWERCASE_LETTER_PARENTHESIS](#NUMBER-LOWERCASE-LETTER-PARENTHESIS) | İlk seviyenin numarası "a)"'dır. |
| [NUMBER_LOWERCASE_ROMAN_DOT](#NUMBER-LOWERCASE-ROMAN-DOT) | İlk seviyenin numarası "i.". |
| [NUMBER_UPPERCASE_LETTER_DOT](#NUMBER-UPPERCASE-LETTER-DOT) | İlk seviyenin numarası "A.". |
| [NUMBER_UPPERCASE_ROMAN_DOT](#NUMBER-UPPERCASE-ROMAN-DOT) | İlk seviyenin numarası "I.". |
| [OUTLINE_BULLETS](#OUTLINE-BULLETS) | Bir taslak, farklı seviyeler için çeşitli madde işaretleri listeler. |
| [OUTLINE_HEADINGS_ARTICLE_SECTION](#OUTLINE-HEADINGS-ARTICLE-SECTION) | Başlık stillerine bağlı seviyeler içeren bir taslak listesi. |
| [OUTLINE_HEADINGS_CHAPTER](#OUTLINE-HEADINGS-CHAPTER) | Başlık stillerine bağlı seviyeler içeren bir taslak listesi. |
| [OUTLINE_HEADINGS_LEGAL](#OUTLINE-HEADINGS-LEGAL) | Başlık stillerine bağlı seviyeler içeren bir taslak listesi. |
| [OUTLINE_HEADINGS_NUMBERS](#OUTLINE-HEADINGS-NUMBERS) | Başlık stillerine bağlı seviyeler içeren bir taslak listesi. |
| [OUTLINE_LEGAL](#OUTLINE-LEGAL) | Seviyeleri "1., 1.1., 1.1.1, ..." şeklinde numaralandırılmış bir taslak listesi. |
| [OUTLINE_NUMBERS](#OUTLINE-NUMBERS) | Seviyeleri "1), a), i), (1), (a), (i), 1., a., i." şeklinde numaralandırılmış bir taslak listesi. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String listTemplateName)](#fromName-java.lang.String) |  |
| [getName(int listTemplate)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int listTemplate)](#toString-int) |  |
### BULLET_ARROW_HEAD {#BULLET-ARROW-HEAD}
```
public static int BULLET_ARROW_HEAD
```


İlk seviyenin madde işareti bir ok başı Wingding karakteridir. Kalan seviyeler [BULLET\_DEFAULT](../../com.aspose.words/listtemplate/\#BULLET-DEFAULT) içindekilerle aynıdır.

Microsoft Word'deki Madde İşaretleri ve Numaralandırma iletişim kutusundaki 6. madde işaretli liste şablonuna karşılık gelir.

### BULLET_CIRCLE {#BULLET-CIRCLE}
```
public static int BULLET_CIRCLE
```


İlk seviyenin madde işareti bir dairedir. Kalan seviyeler [BULLET\_DEFAULT](../../com.aspose.words/listtemplate/\#BULLET-DEFAULT) içindekilerle aynıdır.

Microsoft Word'deki Madde İşaretleri ve Numaralandırma iletişim kutusundaki 2. madde işaretli liste şablonuna karşılık gelir.

### BULLET_DEFAULT {#BULLET-DEFAULT}
```
public static int BULLET_DEFAULT
```


9 seviyeli varsayılan madde işaretli liste. İlk seviyenin madde işareti bir disk, ikinci seviyenin madde işareti bir daire, üçüncü seviyenin madde işareti bir kare. Ardından biçimlendirme kalan seviyeler için tekrarlanır.

Her seviye, bir önceki seviyeye göre sağa 0.25" kaydırılmıştır.

Microsoft Word'deki Madde İşaretleri ve Numaralandırma iletişim kutusundaki 1. madde işaretli liste şablonuna karşılık gelir.

### BULLET_DIAMONDS {#BULLET-DIAMONDS}
```
public static int BULLET_DIAMONDS
```


İlk seviyenin madde işareti 4-karo Wingding karakteridir. Kalan seviyeler [BULLET\_DEFAULT](../../com.aspose.words/listtemplate/\#BULLET-DEFAULT) içindekilerle aynıdır.

Microsoft Word'deki Madde İşaretleri ve Numaralandırma iletişim kutusundaki 5. madde işaretli liste şablonuna karşılık gelir.

### BULLET_DISK {#BULLET-DISK}
```
public static int BULLET_DISK
```


Aynı [BULLET\_DEFAULT](../../com.aspose.words/listtemplate/\#BULLET-DEFAULT) ile.

Microsoft Word'deki Madde İşaretleri ve Numaralandırma iletişim kutusundaki 1. madde işaretli liste şablonuna karşılık gelir.

### BULLET_SQUARE {#BULLET-SQUARE}
```
public static int BULLET_SQUARE
```


İlk seviyenin madde işareti bir karedir. Kalan seviyeler [BULLET\_DEFAULT](../../com.aspose.words/listtemplate/\#BULLET-DEFAULT) içindekilerle aynıdır.

Microsoft Word'deki Madde İşaretleri ve Numaralandırma iletişim kutusundaki 3. madde işaretli liste şablonuna karşılık gelir.

### BULLET_TICK {#BULLET-TICK}
```
public static int BULLET_TICK
```


İlk seviyenin madde işareti bir onay işareti Wingding karakteridir. Kalan seviyeler [BULLET\_DEFAULT](../../com.aspose.words/listtemplate/\#BULLET-DEFAULT) içindekilerle aynıdır.

Microsoft Word'deki Madde İşaretleri ve Numaralandırma iletişim kutusundaki 7. madde işaretli liste şablonuna karşılık gelir.

### NUMBER_ARABIC_DOT {#NUMBER-ARABIC-DOT}
```
public static int NUMBER_ARABIC_DOT
```


Aynı [NUMBER\_DEFAULT](../../com.aspose.words/listtemplate/\#NUMBER-DEFAULT) ile.

Microsoft Word'deki Madde İşaretleri ve Numaralandırma iletişim kutusundaki 1. numaralı liste şablonuna karşılık gelir.

### NUMBER_ARABIC_PARENTHESIS {#NUMBER-ARABIC-PARENTHESIS}
```
public static int NUMBER_ARABIC_PARENTHESIS
```


İlk seviyenin numarası "1)". Kalan seviyeler [NUMBER\_DEFAULT](../../com.aspose.words/listtemplate/\#NUMBER-DEFAULT) içindekilerle aynıdır.

Microsoft Word'deki Madde İşaretleri ve Numaralandırma iletişim kutusundaki 2. numaralı liste şablonuna karşılık gelir.

### NUMBER_DEFAULT {#NUMBER-DEFAULT}
```
public static int NUMBER_DEFAULT
```


9 seviyeli varsayılan numaralı liste. İlk seviye için Arapça numaralandırma (1., 2., 3., ...), ikinci seviye için küçük harfli harf numaralandırması (a., b., c., ...), üçüncü seviye için küçük harfli Roma rakamı numaralandırması (i., ii., iii., ...) kullanılır. Ardından biçimlendirme kalan seviyeler için tekrarlanır.

Her seviye, bir önceki seviyeye göre sağa 0.25" kaydırılmıştır.

Microsoft Word'deki Madde İşaretleri ve Numaralandırma iletişim kutusundaki 1. numaralı liste şablonuna karşılık gelir.

### NUMBER_LOWERCASE_LETTER_DOT {#NUMBER-LOWERCASE-LETTER-DOT}
```
public static int NUMBER_LOWERCASE_LETTER_DOT
```


İlk seviyenin numarası "a.". Kalan seviyeler [NUMBER\_DEFAULT](../../com.aspose.words/listtemplate/\#NUMBER-DEFAULT) içindekilerle aynıdır.

Microsoft Word'teki Madde İşaretleri ve Numaralandırma iletişim kutusundaki 6. numaralı liste şablonuna karşılık gelir.

### NUMBER_LOWERCASE_LETTER_PARENTHESIS {#NUMBER-LOWERCASE-LETTER-PARENTHESIS}
```
public static int NUMBER_LOWERCASE_LETTER_PARENTHESIS
```


İlk seviyenin numarası "a)"'dır. Kalan seviyeler [NUMBER\_DEFAULT](../../com.aspose.words/listtemplate/\#NUMBER-DEFAULT) ile aynıdır.

Microsoft Word'teki Madde İşaretleri ve Numaralandırma iletişim kutusundaki 5. numaralı liste şablonuna karşılık gelir.

### NUMBER_LOWERCASE_ROMAN_DOT {#NUMBER-LOWERCASE-ROMAN-DOT}
```
public static int NUMBER_LOWERCASE_ROMAN_DOT
```


İlk seviyenin numarası "i."'dir. Kalan seviyeler [NUMBER\_DEFAULT](../../com.aspose.words/listtemplate/\#NUMBER-DEFAULT) ile aynıdır.

Microsoft Word'teki Madde İşaretleri ve Numaralandırma iletişim kutusundaki 7. numaralı liste şablonuna karşılık gelir.

### NUMBER_UPPERCASE_LETTER_DOT {#NUMBER-UPPERCASE-LETTER-DOT}
```
public static int NUMBER_UPPERCASE_LETTER_DOT
```


İlk seviyenin numarası "A."'dır. Kalan seviyeler [NUMBER\_DEFAULT](../../com.aspose.words/listtemplate/\#NUMBER-DEFAULT) ile aynıdır.

Microsoft Word'teki Madde İşaretleri ve Numaralandırma iletişim kutusundaki 4. numaralı liste şablonuna karşılık verir.

### NUMBER_UPPERCASE_ROMAN_DOT {#NUMBER-UPPERCASE-ROMAN-DOT}
```
public static int NUMBER_UPPERCASE_ROMAN_DOT
```


İlk seviyenin numarası "I."'dir. Kalan seviyeler [NUMBER\_DEFAULT](../../com.aspose.words/listtemplate/\#NUMBER-DEFAULT) ile aynıdır.

Microsoft Word'teki Madde İşaretleri ve Numaralandırma iletişim kutusundaki 3. numaralı liste şablonuna karşılık verir.

### OUTLINE_BULLETS {#OUTLINE-BULLETS}
```
public static int OUTLINE_BULLETS
```


Bir taslak, farklı seviyeler için çeşitli madde işaretleri listeler.

Microsoft Word'teki Madde İşaretleri ve Numaralandırma iletişim kutusundaki 3. taslak liste şablonuna karşılık verir.

### OUTLINE_HEADINGS_ARTICLE_SECTION {#OUTLINE-HEADINGS-ARTICLE-SECTION}
```
public static int OUTLINE_HEADINGS_ARTICLE_SECTION
```


Başlık stillerine bağlı seviyeler içeren bir taslak listesi.

Microsoft Word'teki Madde İşaretleri ve Numaralandırma iletişim kutusundaki 4. taslak liste şablonuna karşılık verir.

### OUTLINE_HEADINGS_CHAPTER {#OUTLINE-HEADINGS-CHAPTER}
```
public static int OUTLINE_HEADINGS_CHAPTER
```


Başlık stillerine bağlı seviyeler içeren bir taslak listesi.

Microsoft Word'teki Madde İşaretleri ve Numaralandırma iletişim kutusundaki 7. taslak liste şablonuna karşılık verir.

### OUTLINE_HEADINGS_LEGAL {#OUTLINE-HEADINGS-LEGAL}
```
public static int OUTLINE_HEADINGS_LEGAL
```


Başlık stillerine bağlı seviyeler içeren bir taslak listesi.

Microsoft Word'teki Madde İşaretleri ve Numaralandırma iletişim kutusundaki 5. taslak liste şablonuna karşılık verir.

### OUTLINE_HEADINGS_NUMBERS {#OUTLINE-HEADINGS-NUMBERS}
```
public static int OUTLINE_HEADINGS_NUMBERS
```


Başlık stillerine bağlı seviyeler içeren bir taslak listesi.

Microsoft Word'teki Madde İşaretleri ve Numaralandırma iletişim kutusundaki 6. taslak liste şablonuna karşılık verir.

### OUTLINE_LEGAL {#OUTLINE-LEGAL}
```
public static int OUTLINE_LEGAL
```


Seviyeleri "1., 1.1., 1.1.1, ..." şeklinde numaralandırılmış bir taslak listesi.

Microsoft Word'teki Madde İşaretleri ve Numaralandırma iletişim kutusundaki 2. taslak liste şablonuna karşılık verir.

### OUTLINE_NUMBERS {#OUTLINE-NUMBERS}
```
public static int OUTLINE_NUMBERS
```


Seviyeleri "1), a), i), (1), (a), (i), 1., a., i." şeklinde numaralandırılmış bir taslak listesi.

Microsoft Word'teki Madde İşaretleri ve Numaralandırma iletişim kutusundaki 1. taslak liste şablonuna karşılık verir.

### length {#length}
```
public static int length
```


### fromName(String listTemplateName) {#fromName-java.lang.String}
```
public static int fromName(String listTemplateName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| listTemplateName | java.lang.String |  |

**Returns:**
int
### getName(int listTemplate) {#getName-int}
```
public static String getName(int listTemplate)
```




**Parameters:**
| Parametre | Tür | Açıklama |
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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| listTemplate | int |  |

**Returns:**
java.lang.String
