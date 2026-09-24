---
title: "ListFormat"
linktitle: "ListFormat"
second_title: "Aspose.Words Java için"
description: "Java'da bir paragrafta uygulanan liste biçimlendirmesini kontrol etmeyi sağlar."
type: docs
weight: 427
url: /tr/java/com.aspose.words/listformat/
---

**Inheritance:**
java.lang.Object
```
public class ListFormat
```

Bir paragraf için hangi liste biçimlendirmesinin uygulanacağını kontrol etmeye izin verir.

Daha fazla bilgi için, [ Working with Lists ][Working with Lists] dokümantasyon makalesini ziyaret edin.

 **Remarks:** 

Microsoft Word belgesindeki bir paragraf madde işaretli veya numaralı olabilir. Bir paragraf madde işaretli veya numaralı olduğunda, o paragrafın liste biçimlendirmesi uygulandığı söylenir.

Doğrudan [ListFormat](../../com.aspose.words/listformat/) sınıfının nesnelerini oluşturmazsınız. [ListFormat](../../com.aspose.words/listformat/) sınıfına, liste biçimlendirmesiyle ilişkili olabilen başka bir nesnenin özelliği olarak erişirsiniz. Şu anda liste biçimlendirmesine sahip olabilen nesneler şunlardır: [Paragraph](../../com.aspose.words/paragraph/), [Style](../../com.aspose.words/style/) ve [DocumentBuilder](../../com.aspose.words/documentbuilder/).

[ListFormat](../../com.aspose.words/listformat/) of a [Paragraph](../../com.aspose.words/paragraph/) specifies what list formatting and list level is applied to that particular paragraph.

[ListFormat](../../com.aspose.words/listformat/) of a [Style](../../com.aspose.words/style/) (applicable to paragraph styles only) allows to specify what list formatting and list level is applied to all paragraphs of that particular style.

[ListFormat](../../com.aspose.words/listformat/) of a [DocumentBuilder](../../com.aspose.words/documentbuilder/) provides access to the list formatting at the current cursor position inside the [DocumentBuilder](../../com.aspose.words/documentbuilder/).

Liste biçimlendirmesi, paragraflardan ayrı olarak depolanan bir [List](../../com.aspose.words/list/) nesnesi içinde saklanır. Liste nesneleri bir [ListCollection](../../com.aspose.words/listcollection/) koleksiyonu içinde depolanır. Her [Document](../../com.aspose.words/document/) için tek bir [ListCollection](../../com.aspose.words/listcollection/) koleksiyonu bulunur.

Paragraflar fiziksel olarak bir listeye ait değildir. Paragraflar, belirli bir liste nesnesine [getList()](../../com.aspose.words/listformat/\#getList) / [setList(com.aspose.words.List)](../../com.aspose.words/listformat/\#setList-com.aspose.words.List) özelliği aracılığıyla ve listedeki belirli bir seviyeye [getListLevelNumber()](../../com.aspose.words/listformat/\#getListLevelNumber) / [setListLevelNumber(int)](../../com.aspose.words/listformat/\#setListLevelNumber-int) özelliği aracılığıyla referans verir. Bu iki özelliği ayarlayarak bir paragrafın hangi madde işaretleri ve numaralandırma ile biçimlendirileceğini kontrol edersiniz.

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


[Working with Lists]: https://docs.aspose.com/words/java/working-with-lists/
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [applyBulletDefault()](#applyBulletDefault) | Yeni bir varsayılan madde işaretli liste başlatır ve paragrafa uygular. |
| [applyNumberDefault()](#applyNumberDefault) | Yeni bir varsayılan numaralı liste başlatır ve paragrafa uygular. |
| [getList()](#getList) | Bu paragrafın üye olduğu listeyi alır. |
| [getListLevel()](#getListLevel) | Mevcut paragraf için uygulanan liste seviye biçimlendirmesini ve olası biçimlendirme geçersiz kılmalarını döndürür. |
| [getListLevelNumber()](#getListLevelNumber) | Paragraf için liste seviye numarasını (0'dan 8'e) alır. |
| [isListItem()](#isListItem) | Paragrafın madde işaretli veya numaralı biçimlendirme uygulanmış olması durumunda true döner. |
| [listIndent()](#listIndent) | Mevcut paragrafın liste seviyesini bir seviye artırır. |
| [listOutdent()](#listOutdent) | Mevcut paragrafın liste seviyesini bir seviye azaltır. |
| [removeNumbers()](#removeNumbers) | Mevcut paragraftan numaraları veya madde işaretlerini kaldırır ve liste seviyesini sıfıra ayarlar. |
| [setList(List value)](#setList-com.aspose.words.List) | Bu paragrafın üye olduğu listeyi ayarlar. |
| [setListLevelNumber(int value)](#setListLevelNumber-int) | Paragraf için liste seviyesi numarasını (0'dan 8'e) ayarlar. |
### applyBulletDefault() {#applyBulletDefault}
```
public void applyBulletDefault()
```


Yeni bir varsayılan madde işaretli liste başlatır ve paragrafa uygular.

 **Remarks:** 

Bu, varsayılan madde işareti şablonunu kullanarak yeni bir liste oluşturan, paragraf uygulayan ve ilk liste seviyesini seçen bir kısayol yöntemidir.

 **Examples:** 

Madde işaretli ve numaralı listeler oluşturmayı gösterir.

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

### applyNumberDefault() {#applyNumberDefault}
```
public void applyNumberDefault()
```


Yeni bir varsayılan numaralı liste başlatır ve paragrafa uygular.

 **Remarks:** 

Bu, varsayılan numaralı şablonu kullanarak yeni bir liste oluşturan, paragraf uygulayan ve ilk liste seviyesini seçen bir kısayol yöntemidir.

 **Examples:** 

Madde işaretli ve numaralı listeler oluşturmayı gösterir.

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

### getList() {#getList}
```
public List getList()
```


Bu paragrafın üye olduğu listeyi alır.

 **Remarks:** 

Bu özelliğe atanacak listenin mevcut belgeye ait olması gerekir.

Bu özelliğe atanacak listenin bir liste stili tanımı olmaması gerekir.

Bu özelliği  null  olarak ayarlamak, paragraftan madde işaretlerini ve numaralandırmayı kaldırır ve liste seviyesi numarasını sıfıra ayarlar. Bu özelliği  null  olarak ayarlamak, [removeNumbers()](../../com.aspose.words/listformat/\#removeNumbers) metodunu çağırmaya eşdeğerdir.

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

Bir listenin başka bir listenin içinde nasıl iç içe yerleştirileceğini gösterir.

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
[List](../../com.aspose.words/list/) - The list this paragraph is a member of.
### getListLevel() {#getListLevel}
```
public ListLevel getListLevel()
```


Mevcut paragraf için uygulanan liste seviye biçimlendirmesini ve olası biçimlendirme geçersiz kılmalarını döndürür.

 **Examples:** 

DocumentBuilder kullanırken paragraflara özel liste biçimlendirmesinin nasıl uygulanacağını gösterir.

```

 Document doc = new Document();

 // A list allows us to organize and decorate sets of paragraphs with prefix symbols and indents.
 // We can create nested lists by increasing the indent level.
 // We can begin and end a list by using a document builder's "ListFormat" property.
 // Each paragraph that we add between a list's start and the end will become an item in the list.
 // Create a list from a Microsoft Word template, and customize the first two of its list levels.
 List docList = doc.getLists().add(ListTemplate.NUMBER_DEFAULT);

 ListLevel listLevel = docList.getListLevels().get(0);
 listLevel.getFont().setColor(Color.RED);
 listLevel.getFont().setSize(24.0);
 listLevel.setNumberStyle(NumberStyle.ORDINAL_TEXT);
 listLevel.setStartAt(21);
 listLevel.setNumberFormat(" ");

 listLevel.setNumberPosition(-36);
 listLevel.setTextPosition(144.0);
 listLevel.setTabPosition(144.0);

 listLevel = docList.getListLevels().get(1);
 listLevel.setAlignment(ListLevelAlignment.RIGHT);
 listLevel.setNumberStyle(NumberStyle.BULLET);
 listLevel.getFont().setName("Wingdings");
 listLevel.getFont().setColor(Color.BLUE);
 listLevel.getFont().setSize(24.0);

 // This NumberFormat value will create star-shaped bullet list symbols.
 listLevel.setNumberFormat("\uf0af");
 listLevel.setTrailingCharacter(ListTrailingCharacter.SPACE);
 listLevel.setNumberPosition(144.0);

 // Create paragraphs and apply both list levels of our custom list formatting to them.
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getListFormat().setList(docList);
 builder.writeln("The quick brown fox...");
 builder.writeln("The quick brown fox...");

 builder.getListFormat().listIndent();
 builder.writeln("jumped over the lazy dog.");
 builder.writeln("jumped over the lazy dog.");

 builder.getListFormat().listOutdent();
 builder.writeln("The quick brown fox...");

 builder.getListFormat().removeNumbers();

 builder.getDocument().save(getArtifactsDir() + "Lists.CreateCustomList.docx");
 
```

**Returns:**
[ListLevel](../../com.aspose.words/listlevel/) - The list level formatting plus any formatting overrides applied to the current paragraph.
### getListLevelNumber() {#getListLevelNumber}
```
public int getListLevelNumber()
```


Paragraf için liste seviye numarasını (0'dan 8'e) alır.

 **Remarks:** 

Word belgelerinde, listeler 1'den 9'a kadar (0'dan 8'e numaralandırılmış) seviyelerden oluşabilir.

Yalnızca [getList()](../../com.aspose.words/listformat/\#getList) / [setList(com.aspose.words.List)](../../com.aspose.words/listformat/\#setList-com.aspose.words.List) özelliği geçerli bir listeye referans verecek şekilde ayarlandığında etkili olur.

 **Examples:** 

Madde işaretli ve numaralı listeler oluşturmayı gösterir.

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

**Returns:**
int - Paragraf için liste seviyesi numarası (0'dan 8'e).
### isListItem() {#isListItem}
```
public boolean isListItem()
```


Paragrafın madde işaretli veya numaralı biçimlendirme uygulanmış olması durumunda true döner.

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

Bir belgede liste öğesi olan tüm paragrafların nasıl çıktılanacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getListFormat().applyNumberDefault();
 builder.writeln("Numbered list item 1");
 builder.writeln("Numbered list item 2");
 builder.writeln("Numbered list item 3");
 builder.getListFormat().removeNumbers();

 builder.getListFormat().applyBulletDefault();
 builder.writeln("Bulleted list item 1");
 builder.writeln("Bulleted list item 2");
 builder.writeln("Bulleted list item 3");
 builder.getListFormat().removeNumbers();

 NodeCollection paras = doc.getChildNodes(NodeType.PARAGRAPH, true);
 for (Paragraph para : (Iterable) paras) {
     if (para.getListFormat().isListItem()) {
         System.out.println(java.text.MessageFormat.format("*** A paragraph belongs to list {0}", para.getListFormat().getList().getListId()));
         System.out.println(para.getText());
     }
 }
 
```

**Returns:**
boolean - İlgili  boolean  değeri.
### listIndent() {#listIndent}
```
public void listIndent()
```


Mevcut paragrafın liste seviyesini bir seviye artırır.

 **Remarks:** 

Bu yöntem liste seviyesini değiştirir ve yeni seviyenin biçimlendirme özelliklerini uygular.

Word belgelerinde, listeler en fazla dokuz seviyeden oluşabilir. Her seviyenin liste biçimlendirmesi, kullanılan madde işareti veya numara, sol girinti, madde işareti ile metin arasındaki boşluk vb. şeyleri belirler.

 **Examples:** 

Madde işaretli ve numaralı listeler oluşturmayı gösterir.

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

### listOutdent() {#listOutdent}
```
public void listOutdent()
```


Mevcut paragrafın liste seviyesini bir seviye azaltır.

 **Remarks:** 

Bu yöntem liste seviyesini değiştirir ve yeni seviyenin biçimlendirme özelliklerini uygular.

Word belgelerinde, listeler en fazla dokuz seviyeden oluşabilir. Her seviyenin liste biçimlendirmesi, kullanılan madde işareti veya numara, sol girinti, madde işareti ile metin arasındaki boşluk vb. şeyleri belirler.

 **Examples:** 

Madde işaretli ve numaralı listeler oluşturmayı gösterir.

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

### removeNumbers() {#removeNumbers}
```
public void removeNumbers()
```


Mevcut paragraftan numaraları veya madde işaretlerini kaldırır ve liste seviyesini sıfıra ayarlar.

 **Remarks:** 

Bu yöntemi çağırmak, [getList()](../../com.aspose.words/listformat/\#getList) / [setList(com.aspose.words.List)](../../com.aspose.words/listformat/\#setList-com.aspose.words.List) özelliğini  null  olarak ayarlamaya eşdeğerdir.

 **Examples:** 

Madde işaretli ve numaralı listeler oluşturmayı gösterir.

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

Bir bölümün ana metnindeki tüm paragraflardan liste biçimlendirmesini nasıl kaldıracağınızı gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getListFormat().applyNumberDefault();
 builder.writeln("Numbered list item 1");
 builder.writeln("Numbered list item 2");
 builder.writeln("Numbered list item 3");
 builder.getListFormat().removeNumbers();

 NodeCollection paras = doc.getChildNodes(NodeType.PARAGRAPH, true);

 Assert.assertEquals(3, DocumentHelper.getListItemCount(paras));

 for (Paragraph paragraph : doc.getFirstSection().getBody().getParagraphs())
     paragraph.getListFormat().removeNumbers();

 paras = doc.getChildNodes(NodeType.PARAGRAPH, true);

 Assert.assertEquals(0, DocumentHelper.getListItemCount(paras));
 
```

### setList(List value) {#setList-com.aspose.words.List}
```
public void setList(List value)
```


Bu paragrafın üye olduğu listeyi ayarlar.

 **Remarks:** 

Bu özelliğe atanacak listenin mevcut belgeye ait olması gerekir.

Bu özelliğe atanacak listenin bir liste stili tanımı olmaması gerekir.

Bu özelliği  null  olarak ayarlamak, paragraftan madde işaretlerini ve numaralandırmayı kaldırır ve liste seviyesi numarasını sıfıra ayarlar. Bu özelliği  null  olarak ayarlamak, [removeNumbers()](../../com.aspose.words/listformat/\#removeNumbers) metodunu çağırmaya eşdeğerdir.

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

Bir listenin başka bir listenin içinde nasıl iç içe yerleştirileceğini gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | [List](../../com.aspose.words/list/) | Bu paragrafın üye olduğu liste. |

### setListLevelNumber(int value) {#setListLevelNumber-int}
```
public void setListLevelNumber(int value)
```


Paragraf için liste seviyesi numarasını (0'dan 8'e) ayarlar.

 **Remarks:** 

Word belgelerinde, listeler 1'den 9'a kadar (0'dan 8'e numaralandırılmış) seviyelerden oluşabilir.

Yalnızca [getList()](../../com.aspose.words/listformat/\#getList) / [setList(com.aspose.words.List)](../../com.aspose.words/listformat/\#setList-com.aspose.words.List) özelliği geçerli bir listeye referans verecek şekilde ayarlandığında etkili olur.

 **Examples:** 

Madde işaretli ve numaralı listeler oluşturmayı gösterir.

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

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | int | Paragraf için liste seviyesi numarası (0'dan 8'e). |

