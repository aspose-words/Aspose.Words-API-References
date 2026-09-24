---
title: "ParagraphFormat"
linktitle: "ParagraphFormat"
second_title: "Aspose.Words Java için"
description: "Java'da bir paragraf için tüm biçimlendirmeyi temsil eder."
type: docs
weight: 525
url: /tr/java/com.aspose.words/paragraphformat/
---

**Inheritance:**
java.lang.Object
```
public class ParagraphFormat
```

Bir paragraf için tüm biçimlendirmeyi temsil eder.

Daha fazla bilgi edinmek için [ Working with Paragraphs ][Working with Paragraphs] dokümantasyon makalesini ziyaret edin.

 **Examples:** 

Aspose.Words belgesini elle nasıl oluşturacağınızı gösterir.

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
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [clearFormatting()](#clearFormatting) | Paragraf biçimlendirmesini varsayılan ayarlara sıfırlar. |
| [fetchInheritedBorderAttr(int key)](#fetchInheritedBorderAttr-int) |  |
| [fetchInheritedShadingAttr(int key)](#fetchInheritedShadingAttr-int) |  |
| [getAddSpaceBetweenFarEastAndAlpha()](#getAddSpaceBetweenFarEastAndAlpha) | Geçerli paragrafta Latin metin bölgeleri ile Doğu Asya metin bölgeleri arasındaki karakterler arası boşluğun otomatik olarak ayarlanıp ayarlanmadığını gösteren bir bayrak alır. |
| [getAddSpaceBetweenFarEastAndDigit()](#getAddSpaceBetweenFarEastAndDigit) | Geçerli paragrafta sayı bölgeleri ile Doğu Asya metin bölgeleri arasındaki karakterler arası boşluğun otomatik olarak ayarlanıp ayarlanmadığını gösteren bir bayrak alır. |
| [getAlignment()](#getAlignment) | Paragraf için metin hizalamasını alır. |
| [getBaselineAlignment()](#getBaselineAlignment) | Bir satırdaki yazı tiplerinin dikey konumunu alır. |
| [getBidi()](#getBidi) | Bunun sağdan sola bir paragraf olup olmadığını alır. |
| [getBorders()](#getBorders) | Paragrafın kenarlık koleksiyonunu alır. |
| [getCharacterUnitFirstLineIndent()](#getCharacterUnitFirstLineIndent) | İlk satır veya sarkan girinti için değeri (karakter cinsinden) alır. |
| [getCharacterUnitLeftIndent()](#getCharacterUnitLeftIndent) | Belirtilen paragraflar için sol girinti değerini (karakter cinsinden) alır. |
| [getCharacterUnitRightIndent()](#getCharacterUnitRightIndent) | Belirtilen paragraflar için sağ girinti değerini (karakter cinsinden) alır. |
| [getDirectBorderAttr(int key)](#getDirectBorderAttr-int) |  |
| [getDropCapPosition()](#getDropCapPosition) | Büyük harf (drop cap) metni için konumu alır. |
| [getFarEastLineBreakControl()](#getFarEastLineBreakControl) | Geçerli paragrafta Doğu Asya satır sonlandırma kurallarının uygulanıp uygulanmadığını gösteren bir bayrak alır. |
| [getFirstLineIndent()](#getFirstLineIndent) | İlk satır veya sarkan girinti için değeri (nokta cinsinden) alır. |
| [getHangingPunctuation()](#getHangingPunctuation) | Geçerli paragrafta sarkan noktalama işaretlerinin etkin olup olmadığını gösteren bir bayrak alır. |
| [getKeepTogether()](#getKeepTogether) | Doğru, paragraftaki tüm satırların aynı sayfada kalması gerekiyorsa. |
| [getKeepWithNext()](#getKeepWithNext) | Doğru, paragrafın, ardından gelen paragrafla aynı sayfada kalması gerekiyorsa. |
| [getLeftIndent()](#getLeftIndent) | Paragraf için sol girintiyi temsil eden değeri (puan cinsinden) alır. |
| [getLineSpacing()](#getLineSpacing) | Paragraf için satır aralığını (puan cinsinden) alır. |
| [getLineSpacingRule()](#getLineSpacingRule) | Paragraf için satır aralığını alır. |
| [getLineUnitAfter()](#getLineUnitAfter) | Paragraflardan sonraki boşluk miktarını (ızgara satırları cinsinden) alır. |
| [getLineUnitBefore()](#getLineUnitBefore) | Paragraflardan önceki boşluk miktarını (ızgara satırları cinsinden) alır. |
| [getLinesToDrop()](#getLinesToDrop) | Büyük harf yüksekliğini hesaplamak için kullanılan paragraf metni satır sayısını alır. |
| [getMirrorIndents()](#getMirrorIndents) | Sol ve sağ girintilerin aynı genişlikte olup olmadığını gösteren bayrağı alır. |
| [getNoSpaceBetweenParagraphsOfSameStyle()](#getNoSpaceBetweenParagraphsOfSameStyle) | Doğru olduğunda, [getSpaceBefore()](../../com.aspose.words/paragraphformat/\#getSpaceBefore) / [setSpaceBefore(double)](../../com.aspose.words/paragraphformat/\#setSpaceBefore-double) ve [getSpaceAfter()](../../com.aspose.words/paragraphformat/\#getSpaceAfter) / [setSpaceAfter(double)](../../com.aspose.words/paragraphformat/\#setSpaceAfter-double) aynı stilin paragrafları arasında yok sayılacaktır. |
| [getOutlineLevel()](#getOutlineLevel) | Paragrafın belgedeki taslak seviyesini belirtir. |
| [getPageBreakBefore()](#getPageBreakBefore) | Doğru, paragraftan önce bir sayfa sonu zorlanıyorsa. |
| [getRightIndent()](#getRightIndent) | Paragraf için sağ girintiyi temsil eden değeri (puan cinsinden) alır. |
| [getShading()](#getShading) | Paragrafın gölgelendirme biçimlendirmesine referans veren bir [Shading](../../com.aspose.words/shading/) nesnesi döndürür. |
| [getSnapToGrid()](#getSnapToGrid) | Geçerli paragrafın, paragraftaki içeriği düzenlerken sayfa başına belge ızgara satırları ayarlarını kullanıp kullanmayacağını belirtir. |
| [getSpaceAfter()](#getSpaceAfter) | Paragraftan sonraki boşluk miktarını (puan cinsinden) alır. |
| [getSpaceAfterAuto()](#getSpaceAfterAuto) | Doğru, paragraftan sonraki boşluk miktarı otomatik olarak ayarlanıyorsa. |
| [getSpaceBefore()](#getSpaceBefore) | Paragraftan önceki boşluk miktarını (puan cinsinden) alır. |
| [getSpaceBeforeAuto()](#getSpaceBeforeAuto) | Doğru, paragraftan önceki boşluk miktarı otomatik olarak ayarlanıyorsa. |
| [getStyle()](#getStyle) | Bu biçimlendirmeye uygulanan paragraf stilini alır. |
| [getStyleIdentifier()](#getStyleIdentifier) | Bu biçimlendirmeye uygulanan paragraf stilinin bölge bağımsız stil tanımlayıcısını alır. |
| [getStyleName()](#getStyleName) | Bu biçimlendirmeye uygulanan paragraf stilinin adını alır. |
| [getSuppressAutoHyphens()](#getSuppressAutoHyphens) | Geçerli paragrafın, belge ayarlarında uygulanan herhangi bir hecelemeye tabi olup olmayacağını belirtir. |
| [getSuppressLineNumbers()](#getSuppressLineNumbers) | Geçerli paragrafın satırlarının, üst bölümde uygulanan satır numaralandırmasından muaf tutulup tutulmayacağını belirtir. |
| [getTabStops()](#getTabStops) | Bu nesne için tanımlanan özel sekme duraklarının koleksiyonunu alır. |
| [getWidowControl()](#getWidowControl) | Paragraftaki ilk ve son satırların, paragrafın geri kalanıyla aynı sayfada kalması durumunda doğrudur. |
| [getWordWrap()](#getWordWrap) | Bu özellik false ise, bir kelimenin ortasındaki Latin metni mevcut paragraf için kaydırılabilir. |
| [isHeading()](#isHeading) | Paragraf stili yerleşik Başlık stillerinden biri olduğunda doğrudur. |
| [isListItem()](#isListItem) | Paragraf, madde işaretli veya numaralı bir listede öğe olduğunda doğrudur. |
| [setAddSpaceBetweenFarEastAndAlpha(boolean value)](#setAddSpaceBetweenFarEastAndAlpha-boolean) | Mevcut paragrafta Latin metin bölgeleri ile Doğu Asya metin bölgeleri arasındaki karakterler arası boşluğun otomatik olarak ayarlanıp ayarlanmadığını gösteren bir bayrak ayarlar. |
| [setAddSpaceBetweenFarEastAndDigit(boolean value)](#setAddSpaceBetweenFarEastAndDigit-boolean) | Mevcut paragrafta sayı bölgeleri ile Doğu Asya metin bölgeleri arasındaki karakterler arası boşluğun otomatik olarak ayarlanıp ayarlanmadığını gösteren bir bayrak ayarlar. |
| [setAlignment(int value)](#setAlignment-int) | Paragraf için metin hizalamasını ayarlar. |
| [setBaselineAlignment(int value)](#setBaselineAlignment-int) | Satırdaki yazı tiplerinin dikey konumunu ayarlar. |
| [setBidi(boolean value)](#setBidi-boolean) | Bunun sağdan sola bir paragraf olup olmadığını ayarlar. |
| [setBorderAttr(int key, Object value)](#setBorderAttr-int-java.lang.Object) |  |
| [setCharacterUnitFirstLineIndent(double value)](#setCharacterUnitFirstLineIndent-double) | İlk satır veya sarkan girinti için değeri (karakter cinsinden) ayarlar. |
| [setCharacterUnitLeftIndent(double value)](#setCharacterUnitLeftIndent-double) | Belirtilen paragraflar için sol girinti değerini (karakter cinsinden) ayarlar. |
| [setCharacterUnitRightIndent(double value)](#setCharacterUnitRightIndent-double) | Belirtilen paragraflar için sağ girinti değerini (karakter cinsinden) ayarlar. |
| [setDropCapPosition(int value)](#setDropCapPosition-int) | Büyük harf (drop cap) metni için konumu ayarlar. |
| [setFarEastLineBreakControl(boolean value)](#setFarEastLineBreakControl-boolean) | Mevcut paragrafta Doğu Asya satır sonlandırma kurallarının uygulanıp uygulanmadığını gösteren bir bayrak ayarlar. |
| [setFirstLineIndent(double value)](#setFirstLineIndent-double) | İlk satır veya sarkan girinti için değeri (puan cinsinden) ayarlar. |
| [setHangingPunctuation(boolean value)](#setHangingPunctuation-boolean) | Mevcut paragrafta sarkan noktalama işaretlerinin etkin olup olmadığını gösteren bir bayrak ayarlar. |
| [setKeepTogether(boolean value)](#setKeepTogether-boolean) | Doğru, paragraftaki tüm satırların aynı sayfada kalması gerekiyorsa. |
| [setKeepWithNext(boolean value)](#setKeepWithNext-boolean) | Doğru, paragrafın, ardından gelen paragrafla aynı sayfada kalması gerekiyorsa. |
| [setLeftIndent(double value)](#setLeftIndent-double) | Paragraf için sol girintiyi temsil eden değeri (puan cinsinden) ayarlar. |
| [setLineSpacing(double value)](#setLineSpacing-double) | Paragraf için satır aralığını (puan cinsinden) ayarlar. |
| [setLineSpacingRule(int value)](#setLineSpacingRule-int) | Paragraf için satır aralığını ayarlar. |
| [setLineUnitAfter(double value)](#setLineUnitAfter-double) | Paragraflardan sonraki boşluk miktarını (ızgara satırı cinsinden) ayarlar. |
| [setLineUnitBefore(double value)](#setLineUnitBefore-double) | Paragraflardan önceki boşluk miktarını (ızgara satırı cinsinden) ayarlar. |
| [setLinesToDrop(int value)](#setLinesToDrop-int) | Büyük harf (drop cap) yüksekliğini hesaplamak için kullanılan paragraf metni satır sayısını ayarlar. |
| [setMirrorIndents(boolean value)](#setMirrorIndents-boolean) | Sol ve sağ girintilerin aynı genişlikte olup olmadığını gösteren bir bayrak ayarlar. |
| [setNoSpaceBetweenParagraphsOfSameStyle(boolean value)](#setNoSpaceBetweenParagraphsOfSameStyle-boolean) | Doğru olduğunda, [getSpaceBefore()](../../com.aspose.words/paragraphformat/\#getSpaceBefore) / [setSpaceBefore(double)](../../com.aspose.words/paragraphformat/\#setSpaceBefore-double) ve [getSpaceAfter()](../../com.aspose.words/paragraphformat/\#getSpaceAfter) / [setSpaceAfter(double)](../../com.aspose.words/paragraphformat/\#setSpaceAfter-double) aynı stilin paragrafları arasında yok sayılacaktır. |
| [setOutlineLevel(int value)](#setOutlineLevel-int) | Paragrafın belgedeki taslak seviyesini belirtir. |
| [setPageBreakBefore(boolean value)](#setPageBreakBefore-boolean) | Doğru, paragraftan önce bir sayfa sonu zorlanıyorsa. |
| [setRightIndent(double value)](#setRightIndent-double) | Paragraf için sağ girintiyi temsil eden değeri (puan cinsinden) ayarlar. |
| [setSnapToGrid(boolean value)](#setSnapToGrid-boolean) | Geçerli paragrafın, paragraftaki içeriği düzenlerken sayfa başına belge ızgara satırları ayarlarını kullanıp kullanmayacağını belirtir. |
| [setSpaceAfter(double value)](#setSpaceAfter-double) | Paragraftan sonraki boşluk miktarını (puan cinsinden) ayarlar. |
| [setSpaceAfterAuto(boolean value)](#setSpaceAfterAuto-boolean) | Doğru, paragraftan sonraki boşluk miktarı otomatik olarak ayarlanıyorsa. |
| [setSpaceBefore(double value)](#setSpaceBefore-double) | Paragrafın önündeki boşluk miktarını (nokta cinsinden) ayarlar. |
| [setSpaceBeforeAuto(boolean value)](#setSpaceBeforeAuto-boolean) | Doğru, paragraftan önceki boşluk miktarı otomatik olarak ayarlanıyorsa. |
| [setStyle(Style value)](#setStyle-com.aspose.words.Style) | Bu biçimlendirmeye uygulanan paragraf stilini ayarlar. |
| [setStyleIdentifier(int value)](#setStyleIdentifier-int) | Bu biçimlendirmeye uygulanan paragraf stilinin bölge bağımsız stil tanımlayıcısını ayarlar. |
| [setStyleName(String value)](#setStyleName-java.lang.String) | Bu biçimlendirmeye uygulanan paragraf stilinin adını ayarlar. |
| [setSuppressAutoHyphens(boolean value)](#setSuppressAutoHyphens-boolean) | Geçerli paragrafın, belge ayarlarında uygulanan herhangi bir hecelemeye tabi olup olmayacağını belirtir. |
| [setSuppressLineNumbers(boolean value)](#setSuppressLineNumbers-boolean) | Geçerli paragrafın satırlarının, üst bölümde uygulanan satır numaralandırmasından muaf tutulup tutulmayacağını belirtir. |
| [setWidowControl(boolean value)](#setWidowControl-boolean) | Paragraftaki ilk ve son satırların, paragrafın geri kalanıyla aynı sayfada kalması durumunda doğrudur. |
| [setWordWrap(boolean value)](#setWordWrap-boolean) | Bu özellik false ise, bir kelimenin ortasındaki Latin metni mevcut paragraf için kaydırılabilir. |
### clearFormatting() {#clearFormatting}
```
public void clearFormatting()
```


Paragraf biçimlendirmesini varsayılan ayarlara sıfırlar.

 **Remarks:** 

Varsayılan paragraf biçimlendirmesi Normal stil, sola hizalı, girintisiz, boşluksuz, kenarlık ve gölgelendirme içermez.

 **Examples:** 

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

### fetchInheritedBorderAttr(int key) {#fetchInheritedBorderAttr-int}
```
public Object fetchInheritedBorderAttr(int key)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### fetchInheritedShadingAttr(int key) {#fetchInheritedShadingAttr-int}
```
public Object fetchInheritedShadingAttr(int key)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### getAddSpaceBetweenFarEastAndAlpha() {#getAddSpaceBetweenFarEastAndAlpha}
```
public boolean getAddSpaceBetweenFarEastAndAlpha()
```


Geçerli paragrafta Latin metin bölgeleri ile Doğu Asya metin bölgeleri arasındaki karakterler arası boşluğun otomatik olarak ayarlanıp ayarlanmadığını gösteren bir bayrak alır.

 **Examples:** 

Belgeye bir paragraf eklemenin nasıl yapılacağını gösterir.

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
boolean - Geçerli paragrafta Latin metin bölgeleri ile Doğu Asya metin bölgeleri arasındaki karakterler arası boşluğun otomatik olarak ayarlanıp ayarlanmadığını gösteren bir işaret.
### getAddSpaceBetweenFarEastAndDigit() {#getAddSpaceBetweenFarEastAndDigit}
```
public boolean getAddSpaceBetweenFarEastAndDigit()
```


Geçerli paragrafta sayı bölgeleri ile Doğu Asya metin bölgeleri arasındaki karakterler arası boşluğun otomatik olarak ayarlanıp ayarlanmadığını gösteren bir bayrak alır.

 **Examples:** 

Belgeye bir paragraf eklemenin nasıl yapılacağını gösterir.

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
boolean - Geçerli paragrafta sayı bölgeleri ile Doğu Asya metin bölgeleri arasındaki karakterler arası boşluğun otomatik olarak ayarlanıp ayarlanmadığını gösteren bir işaret.
### getAlignment() {#getAlignment}
```
public int getAlignment()
```


Paragraf için metin hizalamasını alır.

 **Examples:** 

Belgeye bir paragraf eklemenin nasıl yapılacağını gösterir.

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

Aspose.Words belgesini elle nasıl oluşturacağınızı gösterir.

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
int - Paragraf için metin hizalaması. Döndürülen değer [ParagraphAlignment](../../com.aspose.words/paragraphalignment/) sabitlerinden biridir.
### getBaselineAlignment() {#getBaselineAlignment}
```
public int getBaselineAlignment()
```


Bir satırdaki yazı tiplerinin dikey konumunu alır.

 **Examples:** 

Bir satırdaki yazı tiplerinin dikey konumunu nasıl ayarlayacağınızı gösterir.

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
int - Bir satırdaki fontların dikey konumu. Döndürülen değer [BaselineAlignment](../../com.aspose.words/baselinealignment/) sabitlerinden biridir.
### getBidi() {#getBidi}
```
public boolean getBidi()
```


Bunun sağdan sola bir paragraf olup olmadığını alır.

 **Remarks:** 

true olduğunda, bu paragraftaki run'lar ve diğer satır içi nesneler sağdan sola yerleştirilir.

 **Examples:** 

BIDIOUTLINE alanlarıyla sağdan sola dillerle uyumlu listelerin nasıl oluşturulacağını gösterir.

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

Düz metin belge metin yönünün nasıl algılanacağını gösterir.

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
boolean - Bunun sağdan sola bir paragraf olup olmadığı.
### getBorders() {#getBorders}
```
public BorderCollection getBorders()
```


Paragrafın kenarlık koleksiyonunu alır.

 **Examples:** 

Üst kenarlı bir paragraf eklemenin nasıl yapılacağını gösterir.

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


İlk satır veya sarkan girinti için değeri (karakter cinsinden) alır.

İlk satır girintisini ayarlamak için pozitif değerleri, sarkan girintiyi ayarlamak için negatif değerleri kullanın.

 **Examples:** 

Paragraf boşluklarını ve girintilerini nasıl değiştireceğinizi gösterir.

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
double - İlk satır veya sarkan girinti için değer (karakter cinsinden).
### getCharacterUnitLeftIndent() {#getCharacterUnitLeftIndent}
```
public double getCharacterUnitLeftIndent()
```


Belirtilen paragraflar için sol girinti değerini (karakter cinsinden) alır.

 **Examples:** 

Paragraf boşluklarını ve girintilerini nasıl değiştireceğinizi gösterir.

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
double - Belirtilen paragraflar için sol girinti değeri (karakter cinsinden).
### getCharacterUnitRightIndent() {#getCharacterUnitRightIndent}
```
public double getCharacterUnitRightIndent()
```


Belirtilen paragraflar için sağ girinti değerini (karakter cinsinden) alır.

 **Examples:** 

Paragraf boşluklarını ve girintilerini nasıl değiştireceğinizi gösterir.

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
double - Belirtilen paragraflar için sağ girinti değeri (karakter cinsinden).
### getDirectBorderAttr(int key) {#getDirectBorderAttr-int}
```
public Object getDirectBorderAttr(int key)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### getDropCapPosition() {#getDropCapPosition}
```
public int getDropCapPosition()
```


Büyük harf (drop cap) metni için konumu alır.

 **Examples:** 

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
int - Bir drop cap metni için konum. Döndürülen değer [DropCapPosition](../../com.aspose.words/dropcapposition/) sabitlerinden biridir.
### getFarEastLineBreakControl() {#getFarEastLineBreakControl}
```
public boolean getFarEastLineBreakControl()
```


Geçerli paragrafta Doğu Asya satır sonlandırma kurallarının uygulanıp uygulanmadığını gösteren bir bayrak alır.

 **Examples:** 

Asya tipografisi için özel özelliklerin nasıl ayarlanacağını gösterir.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 ParagraphFormat format = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat();
 format.setFarEastLineBreakControl(true);
 format.setWordWrap(false);
 format.setHangingPunctuation(true);

 doc.save(getArtifactsDir() + "ParagraphFormat.AsianTypographyProperties.docx");
 
```

**Returns:**
boolean - Doğu Asya satır sonu kurallarının geçerli paragraf için uygulanıp uygulanmadığını gösteren bir işaret.
### getFirstLineIndent() {#getFirstLineIndent}
```
public double getFirstLineIndent()
```


İlk satır veya sarkan girinti için değeri (nokta cinsinden) alır.

İlk satır girintisini ayarlamak için pozitif değerleri, sarkan girintiyi ayarlamak için negatif değerleri kullanın.

 **Examples:** 

Belgeye bir paragraf eklemenin nasıl yapılacağını gösterir.

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
double - İlk satır veya sarkan girinti için değer (nokta cinsinden).
### getHangingPunctuation() {#getHangingPunctuation}
```
public boolean getHangingPunctuation()
```


Geçerli paragrafta sarkan noktalama işaretlerinin etkin olup olmadığını gösteren bir bayrak alır.

 **Examples:** 

Asya tipografisi için özel özelliklerin nasıl ayarlanacağını gösterir.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 ParagraphFormat format = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat();
 format.setFarEastLineBreakControl(true);
 format.setWordWrap(false);
 format.setHangingPunctuation(true);

 doc.save(getArtifactsDir() + "ParagraphFormat.AsianTypographyProperties.docx");
 
```

**Returns:**
boolean - Geçerli paragrafta sarkan noktalama işaretlerinin etkin olup olmadığını gösteren bir işaret.
### getKeepTogether() {#getKeepTogether}
```
public boolean getKeepTogether()
```


Doğru, paragraftaki tüm satırların aynı sayfada kalması gerekiyorsa.

 **Examples:** 

Belgeye bir paragraf eklemenin nasıl yapılacağını gösterir.

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
boolean - İlgili  boolean  değeri.
### getKeepWithNext() {#getKeepWithNext}
```
public boolean getKeepWithNext()
```


Doğru, paragrafın, ardından gelen paragrafla aynı sayfada kalması gerekiyorsa.

 **Examples:** 

Bir tablonun aynı sayfada birlikte kalmasını nasıl ayarlayacağınızı gösterir.

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
boolean - İlgili  boolean  değeri.
### getLeftIndent() {#getLeftIndent}
```
public double getLeftIndent()
```


Paragraf için sol girintiyi temsil eden değeri (puan cinsinden) alır.

 **Examples:** 

Paragraf biçimlendirmesini, merkezin dışına kaymış metin oluşturmak için nasıl yapılandıracağınızı gösterir.

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
double - Paragraf için sol girintiyi temsil eden değer (nokta cinsinden).
### getLineSpacing() {#getLineSpacing}
```
public double getLineSpacing()
```


Paragraf için satır aralığını (puan cinsinden) alır.

 **Remarks:** 

When [getLineSpacingRule()](../../com.aspose.words/paragraphformat/\#getLineSpacingRule) / [setLineSpacingRule(int)](../../com.aspose.words/paragraphformat/\#setLineSpacingRule-int) özelliği [LineSpacingRule.AT\_LEAST](../../com.aspose.words/linespacingrule/\#AT-LEAST) olarak ayarlandığında, satır aralığı belirtilen [getLineSpacing()](../../com.aspose.words/paragraphformat/\#getLineSpacing) / [setLineSpacing(double)](../../com.aspose.words/paragraphformat/\#setLineSpacing-double) değerine eşit ya da daha büyük olabilir, ancak asla daha düşük olamaz.

When [getLineSpacingRule()](../../com.aspose.words/paragraphformat/\#getLineSpacingRule) / [setLineSpacingRule(int)](../../com.aspose.words/paragraphformat/\#setLineSpacingRule-int) özelliği [LineSpacingRule.EXACTLY](../../com.aspose.words/linespacingrule/\#EXACTLY) olarak ayarlandığında, satır aralığı paragrafta daha büyük bir font kullanılsa bile belirtilen [getLineSpacing()](../../com.aspose.words/paragraphformat/\#getLineSpacing) / [setLineSpacing(double)](../../com.aspose.words/paragraphformat/\#setLineSpacing-double) değerinden asla değişmez.

 **Examples:** 

Satır aralığıyla nasıl çalışılacağını gösterir.

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
double - Paragraf için satır aralığı (nokta cinsinden).
### getLineSpacingRule() {#getLineSpacingRule}
```
public int getLineSpacingRule()
```


Paragraf için satır aralığını alır.

 **Examples:** 

Satır aralığıyla nasıl çalışılacağını gösterir.

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
int - Paragraf için satır aralığı. Döndürülen değer, [LineSpacingRule](../../com.aspose.words/linespacingrule/) sabitlerinden biridir.
### getLineUnitAfter() {#getLineUnitAfter}
```
public double getLineUnitAfter()
```


Paragraflardan sonraki boşluk miktarını (ızgara satırları cinsinden) alır.

 **Examples:** 

Paragraf boşluklarını ve girintilerini nasıl değiştireceğinizi gösterir.

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
double - Paragraflardan sonraki boşluk miktarı (ızgara satırı cinsinden).
### getLineUnitBefore() {#getLineUnitBefore}
```
public double getLineUnitBefore()
```


Paragraflardan önceki boşluk miktarını (ızgara satırları cinsinden) alır.

 **Examples:** 

Paragraf boşluklarını ve girintilerini nasıl değiştireceğinizi gösterir.

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
double - Paragraflardan önceki boşluk miktarı (ızgara satırı cinsinden).
### getLinesToDrop() {#getLinesToDrop}
```
public int getLinesToDrop()
```


Büyük harf yüksekliğini hesaplamak için kullanılan paragraf metni satır sayısını alır.

 **Examples:** 

Bir drop cap boyutunun nasıl ayarlanacağını gösterir.

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
int - Drop cap yüksekliğini hesaplamak için kullanılan paragraf metni satır sayısı.
### getMirrorIndents() {#getMirrorIndents}
```
public boolean getMirrorIndents()
```


Sol ve sağ girintilerin aynı genişlikte olup olmadığını gösteren bayrağı alır.

 **Examples:** 

Sol ve sağ girintilerin aynı olmasını nasıl yapacağınızı gösterir.

```

 Document doc = new Document(getMyDir() + "Document.docx");
 ParagraphFormat format = doc.getFirstSection().getBody().getParagraphs().get(0).getParagraphFormat();

 format.setMirrorIndents(true);

 doc.save(getArtifactsDir() + "ParagraphFormat.MirrorIndents.docx");
 
```

**Returns:**
boolean - Sol ve sağ girintilerin aynı genişlikte olup olmadığını gösteren bir işaret.
### getNoSpaceBetweenParagraphsOfSameStyle() {#getNoSpaceBetweenParagraphsOfSameStyle}
```
public boolean getNoSpaceBetweenParagraphsOfSameStyle()
```


Doğru olduğunda, [getSpaceBefore()](../../com.aspose.words/paragraphformat/\#getSpaceBefore) / [setSpaceBefore(double)](../../com.aspose.words/paragraphformat/\#setSpaceBefore-double) ve [getSpaceAfter()](../../com.aspose.words/paragraphformat/\#getSpaceAfter) / [setSpaceAfter(double)](../../com.aspose.words/paragraphformat/\#setSpaceAfter-double) aynı stilin paragrafları arasında yok sayılacaktır.

 **Remarks:** 

Bu ayar yalnızca bir paragraf stiline uygulandığında etkili olur. Doğrudan bir paragrafa uygulanırsa etkisi yoktur.

 **Examples:** 

Aynı stile sahip paragraflar arasında boşluk bırakmamanın nasıl uygulanacağını gösterir.

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
boolean - İlgili  boolean  değeri.
### getOutlineLevel() {#getOutlineLevel}
```
public int getOutlineLevel()
```


Paragrafın belgedeki taslak seviyesini belirtir.

 **Examples:** 

Paragraf anahat seviyelerini yapılandırarak katlanabilir metin oluşturmayı gösterir.

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
int - İlgili int değeri. Döndürülen değer, [OutlineLevel](../../com.aspose.words/outlinelevel/) sabitlerinden biridir.
### getPageBreakBefore() {#getPageBreakBefore}
```
public boolean getPageBreakBefore()
```


Doğru, paragraftan önce bir sayfa sonu zorlanıyorsa.

 **Examples:** 

Paragrafların başında sayfa sonu eklemenin nasıl yapılacağını gösterir.

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
boolean - İlgili  boolean  değeri.
### getRightIndent() {#getRightIndent}
```
public double getRightIndent()
```


Paragraf için sağ girintiyi temsil eden değeri (puan cinsinden) alır.

 **Examples:** 

Paragraf biçimlendirmesini, merkezin dışına kaymış metin oluşturmak için nasıl yapılandıracağınızı gösterir.

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
double - Paragraf için sağ girintiyi temsil eden değer (nokta cinsinden).
### getShading() {#getShading}
```
public Shading getShading()
```


Paragrafın gölgelendirme biçimlendirmesine referans veren bir [Shading](../../com.aspose.words/shading/) nesnesi döndürür.

 **Examples:** 

Metni kenarlıklar ve gölgelendirme ile nasıl süsleneceğini gösterir.

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


Geçerli paragrafın, paragraftaki içeriği düzenlerken sayfa başına belge ızgara satırları ayarlarını kullanıp kullanmayacağını belirtir.

 **Examples:** 

Her sayfanın sahip olabileceği satır sayısı için bir sınırın nasıl belirtileceğini gösterir.

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
boolean - İlgili  boolean  değeri.
### getSpaceAfter() {#getSpaceAfter}
```
public double getSpaceAfter()
```


Paragraftan sonraki boşluk miktarını (puan cinsinden) alır.

**Returns:**
double - Paragraftan sonraki boşluk miktarı (nokta cinsinden).
### getSpaceAfterAuto() {#getSpaceAfterAuto}
```
public boolean getSpaceAfterAuto()
```


Doğru, paragraftan sonraki boşluk miktarı otomatik olarak ayarlanıyorsa.

 **Remarks:** 

true olarak ayarlandığında, [getSpaceAfter()](../../com.aspose.words/paragraphformat/\#getSpaceAfter) / [setSpaceAfter(double)](../../com.aspose.words/paragraphformat/\#setSpaceAfter-double) etkisini geçersiz kılar.

Paragraf Ön Boşluğu ve Son Boşluğu'nu Otomatik olarak ayarladığınızda, Microsoft Word aşağıdaki kurallara göre paragraflar arasında otomatik olarak 14 nokta boşluk ekler:

 *  Normally, spacing is added after all paragraphs.
 *  In a bulleted or numbered list, spacing is added only after the last item in the list. Spacing is not added between the list items.
 *  In a nested bulleted or numbered list spacing is not added.
 *  Spacing is normally added after a table.
 *  Spacing is not added after a table if it is the last block in a table cell.
 *  Spacing is not added after the last paragraph in a table cell.

 **Examples:** 

Otomatik paragraf boşluğunu ayarlamanın nasıl yapılacağını gösterir.

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
boolean - İlgili  boolean  değeri.
### getSpaceBefore() {#getSpaceBefore}
```
public double getSpaceBefore()
```


Paragraftan önceki boşluk miktarını (puan cinsinden) alır.

**Returns:**
double - Paragraftan önceki boşluk miktarı (nokta cinsinden).
### getSpaceBeforeAuto() {#getSpaceBeforeAuto}
```
public boolean getSpaceBeforeAuto()
```


Doğru, paragraftan önceki boşluk miktarı otomatik olarak ayarlanıyorsa.

 **Remarks:** 

true olarak ayarlandığında, [getSpaceBefore()](../../com.aspose.words/paragraphformat/\#getSpaceBefore) / [setSpaceBefore(double)](../../com.aspose.words/paragraphformat/\#setSpaceBefore-double) etkisini geçersiz kılar.

Paragraf Ön Boşluğu ve Son Boşluğu'nu Otomatik olarak ayarladığınızda, Microsoft Word aşağıdaki kurallara göre paragraflar arasında otomatik olarak 14 nokta boşluk ekler:

 *  Normally, spacing is added after all paragraphs.
 *  In a bulleted or numbered list, spacing is added only after the last item in the list. Spacing is not added between the list items.
 *  In a nested bulleted or numbered list spacing is not added.
 *  Spacing is normally added after a table.
 *  Spacing is not added after a table if it is the last block in a table cell.
 *  Spacing is not added after the last paragraph in a table cell.

 **Examples:** 

Otomatik paragraf boşluğunu ayarlamanın nasıl yapılacağını gösterir.

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
boolean - İlgili  boolean  değeri.
### getStyle() {#getStyle}
```
public Style getStyle()
```


Bu biçimlendirmeye uygulanan paragraf stilini alır.

 **Examples:** 

Liste biçimlendirmeli bir paragraf stilinin nasıl oluşturulacağını ve kullanılacağını gösterir.

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


Bu biçimlendirmeye uygulanan paragraf stilinin bölge bağımsız stil tanımlayıcısını alır.

 **Examples:** 

Başlık stillerini giriş olarak kullanarak bir belgeye İçindekiler Tablosu (TOC) nasıl eklenir gösterir.

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
int - Bu biçimlendirmeye uygulanan paragraf stilinin bölge bağımsız stil tanımlayıcısı. Döndürülen değer, [StyleIdentifier](../../com.aspose.words/styleidentifier/) sabitlerinden biridir.
### getStyleName() {#getStyleName}
```
public String getStyleName()
```


Bu biçimlendirmeye uygulanan paragraf stilinin adını alır.

 **Examples:** 

Aspose.Words belgesini elle nasıl oluşturacağınızı gösterir.

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
java.lang.String - Bu biçimlendirmeye uygulanan paragraf stilinin adı.
### getSuppressAutoHyphens() {#getSuppressAutoHyphens}
```
public boolean getSuppressAutoHyphens()
```


Geçerli paragrafın, belge ayarlarında uygulanan herhangi bir hecelemeye tabi olup olmayacağını belirtir.

 **Examples:** 

Bir paragraf için hecelemeyi nasıl bastıracağınızı gösterir.

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
boolean - İlgili  boolean  değeri.
### getSuppressLineNumbers() {#getSuppressLineNumbers}
```
public boolean getSuppressLineNumbers()
```


Geçerli paragrafın satırlarının, üst bölümde uygulanan satır numaralandırmasından muaf tutulup tutulmayacağını belirtir.

 **Examples:** 

Bir bölüm için satır numaralandırmayı nasıl etkinleştireceğinizi gösterir.

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
boolean - İlgili  boolean  değeri.
### getTabStops() {#getTabStops}
```
public TabStopCollection getTabStops()
```


Bu nesne için tanımlanan özel sekme duraklarının koleksiyonunu alır.

 **Examples:** 

TOC ile ilgili paragraflarda sağ sekme durağının konumunu nasıl değiştireceğinizi gösterir.

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


Paragraftaki ilk ve son satırların, paragrafın geri kalanıyla aynı sayfada kalması durumunda doğrudur.

 **Examples:** 

Bir paragraf için yetim/yalnız satır kontrolünü nasıl etkinleştireceğinizi gösterir.

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
boolean - İlgili  boolean  değeri.
### getWordWrap() {#getWordWrap}
```
public boolean getWordWrap()
```


Bu özellik false ise, bir kelimenin ortasındaki Latin metni mevcut paragrafta bölünebilir. Aksi takdirde Latin metni bütün kelimeler halinde bölünür.

 **Examples:** 

Asya tipografisi için özel özelliklerin nasıl ayarlanacağını gösterir.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 ParagraphFormat format = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat();
 format.setFarEastLineBreakControl(true);
 format.setWordWrap(false);
 format.setHangingPunctuation(true);

 doc.save(getArtifactsDir() + "ParagraphFormat.AsianTypographyProperties.docx");
 
```

**Returns:**
boolean - İlgili  boolean  değeri.
### isHeading() {#isHeading}
```
public boolean isHeading()
```


Paragraf stili yerleşik Başlık stillerinden biri olduğunda doğrudur.

 **Examples:** 

Kaydedilmiş bir PDF belgesinin taslak görünümünde görünecek başlık seviyesinin nasıl sınırlanacağını gösterir.

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
boolean - İlgili  boolean  değeri.
### isListItem() {#isListItem}
```
public boolean isListItem()
```


Paragraf, madde işaretli veya numaralı bir listede öğe olduğunda doğrudur.

 **Examples:** 

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
boolean - İlgili  boolean  değeri.
### setAddSpaceBetweenFarEastAndAlpha(boolean value) {#setAddSpaceBetweenFarEastAndAlpha-boolean}
```
public void setAddSpaceBetweenFarEastAndAlpha(boolean value)
```


Mevcut paragrafta Latin metin bölgeleri ile Doğu Asya metin bölgeleri arasındaki karakterler arası boşluğun otomatik olarak ayarlanıp ayarlanmadığını gösteren bir bayrak ayarlar.

 **Examples:** 

Belgeye bir paragraf eklemenin nasıl yapılacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | Geçerli paragrafta Latin metin bölgeleri ile Doğu Asya metin bölgeleri arasında karakterler arası boşluğun otomatik olarak ayarlanıp ayarlanmadığını gösteren bir işaret. |

### setAddSpaceBetweenFarEastAndDigit(boolean value) {#setAddSpaceBetweenFarEastAndDigit-boolean}
```
public void setAddSpaceBetweenFarEastAndDigit(boolean value)
```


Mevcut paragrafta sayı bölgeleri ile Doğu Asya metin bölgeleri arasındaki karakterler arası boşluğun otomatik olarak ayarlanıp ayarlanmadığını gösteren bir bayrak ayarlar.

 **Examples:** 

Belgeye bir paragraf eklemenin nasıl yapılacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | Geçerli paragrafta sayı bölgeleri ile Doğu Asya metin bölgeleri arasında karakterler arası boşluğun otomatik olarak ayarlanıp ayarlanmadığını gösteren bir işaret. |

### setAlignment(int value) {#setAlignment-int}
```
public void setAlignment(int value)
```


Paragraf için metin hizalamasını ayarlar.

 **Examples:** 

Belgeye bir paragraf eklemenin nasıl yapılacağını gösterir.

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

Aspose.Words belgesini elle nasıl oluşturacağınızı gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | int | Paragraf için metin hizalaması. Değer, [ParagraphAlignment](../../com.aspose.words/paragraphalignment/) sabitlerinden biri olmalıdır. |

### setBaselineAlignment(int value) {#setBaselineAlignment-int}
```
public void setBaselineAlignment(int value)
```


Satırdaki yazı tiplerinin dikey konumunu ayarlar.

 **Examples:** 

Bir satırdaki yazı tiplerinin dikey konumunu nasıl ayarlayacağınızı gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | int | Bir satırdaki yazı tiplerinin dikey konumu. Değer, [BaselineAlignment](../../com.aspose.words/baselinealignment/) sabitlerinden biri olmalıdır. |

### setBidi(boolean value) {#setBidi-boolean}
```
public void setBidi(boolean value)
```


Bunun sağdan sola bir paragraf olup olmadığını ayarlar.

 **Remarks:** 

true olduğunda, bu paragraftaki run'lar ve diğer satır içi nesneler sağdan sola yerleştirilir.

 **Examples:** 

BIDIOUTLINE alanlarıyla sağdan sola dillerle uyumlu listelerin nasıl oluşturulacağını gösterir.

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

Düz metin belge metin yönünün nasıl algılanacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | Bu paragrafın sağdan sola mı olduğunu gösterir. |

### setBorderAttr(int key, Object value) {#setBorderAttr-int-java.lang.Object}
```
public void setBorderAttr(int key, Object value)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| key | int |  |
| değer | java.lang.Object |  |

### setCharacterUnitFirstLineIndent(double value) {#setCharacterUnitFirstLineIndent-double}
```
public void setCharacterUnitFirstLineIndent(double value)
```


İlk satır veya sarkan girinti için değeri (karakter cinsinden) ayarlar.

İlk satır girintisini ayarlamak için pozitif değerleri, sarkan girintiyi ayarlamak için negatif değerleri kullanın.

 **Examples:** 

Paragraf boşluklarını ve girintilerini nasıl değiştireceğinizi gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | double | İlk satır veya sarkıt girinti için değer (karakter cinsinden). |

### setCharacterUnitLeftIndent(double value) {#setCharacterUnitLeftIndent-double}
```
public void setCharacterUnitLeftIndent(double value)
```


Belirtilen paragraflar için sol girinti değerini (karakter cinsinden) ayarlar.

 **Examples:** 

Paragraf boşluklarını ve girintilerini nasıl değiştireceğinizi gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | double | Belirtilen paragraflar için sol girinti değeri (karakter cinsinden). |

### setCharacterUnitRightIndent(double value) {#setCharacterUnitRightIndent-double}
```
public void setCharacterUnitRightIndent(double value)
```


Belirtilen paragraflar için sağ girinti değerini (karakter cinsinden) ayarlar.

 **Examples:** 

Paragraf boşluklarını ve girintilerini nasıl değiştireceğinizi gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | double | Belirtilen paragraflar için sağ girinti değeri (karakter cinsinden). |

### setDropCapPosition(int value) {#setDropCapPosition-int}
```
public void setDropCapPosition(int value)
```


Büyük harf (drop cap) metni için konumu ayarlar.

 **Examples:** 

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
| value | int | Büyük harf baş harf (drop cap) metni için konum. Değer, [DropCapPosition](../../com.aspose.words/dropcapposition/) sabitlerinden biri olmalıdır. |

### setFarEastLineBreakControl(boolean value) {#setFarEastLineBreakControl-boolean}
```
public void setFarEastLineBreakControl(boolean value)
```


Mevcut paragrafta Doğu Asya satır sonlandırma kurallarının uygulanıp uygulanmadığını gösteren bir bayrak ayarlar.

 **Examples:** 

Asya tipografisi için özel özelliklerin nasıl ayarlanacağını gösterir.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 ParagraphFormat format = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat();
 format.setFarEastLineBreakControl(true);
 format.setWordWrap(false);
 format.setHangingPunctuation(true);

 doc.save(getArtifactsDir() + "ParagraphFormat.AsianTypographyProperties.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | Geçerli paragrafta Doğu Asya satır sonlandırma kurallarının uygulanıp uygulanmadığını gösteren bir işaret. |

### setFirstLineIndent(double value) {#setFirstLineIndent-double}
```
public void setFirstLineIndent(double value)
```


İlk satır veya sarkan girinti için değeri (puan cinsinden) ayarlar.

İlk satır girintisini ayarlamak için pozitif değerleri, sarkan girintiyi ayarlamak için negatif değerleri kullanın.

 **Examples:** 

Belgeye bir paragraf eklemenin nasıl yapılacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | double | İlk satır veya sarkıt girinti için değer (puan cinsinden). |

### setHangingPunctuation(boolean value) {#setHangingPunctuation-boolean}
```
public void setHangingPunctuation(boolean value)
```


Mevcut paragrafta sarkan noktalama işaretlerinin etkin olup olmadığını gösteren bir bayrak ayarlar.

 **Examples:** 

Asya tipografisi için özel özelliklerin nasıl ayarlanacağını gösterir.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 ParagraphFormat format = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat();
 format.setFarEastLineBreakControl(true);
 format.setWordWrap(false);
 format.setHangingPunctuation(true);

 doc.save(getArtifactsDir() + "ParagraphFormat.AsianTypographyProperties.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | Geçerli paragrafta sarkıt noktalama işaretlerinin etkin olup olmadığını gösteren bir işaret. |

### setKeepTogether(boolean value) {#setKeepTogether-boolean}
```
public void setKeepTogether(boolean value)
```


Doğru, paragraftaki tüm satırların aynı sayfada kalması gerekiyorsa.

 **Examples:** 

Belgeye bir paragraf eklemenin nasıl yapılacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | İlgili  boolean  değeri. |

### setKeepWithNext(boolean value) {#setKeepWithNext-boolean}
```
public void setKeepWithNext(boolean value)
```


Doğru, paragrafın, ardından gelen paragrafla aynı sayfada kalması gerekiyorsa.

 **Examples:** 

Bir tablonun aynı sayfada birlikte kalmasını nasıl ayarlayacağınızı gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | İlgili  boolean  değeri. |

### setLeftIndent(double value) {#setLeftIndent-double}
```
public void setLeftIndent(double value)
```


Paragraf için sol girintiyi temsil eden değeri (puan cinsinden) ayarlar.

 **Examples:** 

Paragraf biçimlendirmesini, merkezin dışına kaymış metin oluşturmak için nasıl yapılandıracağınızı gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | double | Paragraf için sol girintiyi temsil eden değer (puan cinsinden). |

### setLineSpacing(double value) {#setLineSpacing-double}
```
public void setLineSpacing(double value)
```


Paragraf için satır aralığını (puan cinsinden) ayarlar.

 **Remarks:** 

When [getLineSpacingRule()](../../com.aspose.words/paragraphformat/\#getLineSpacingRule) / [setLineSpacingRule(int)](../../com.aspose.words/paragraphformat/\#setLineSpacingRule-int) özelliği [LineSpacingRule.AT\_LEAST](../../com.aspose.words/linespacingrule/\#AT-LEAST) olarak ayarlandığında, satır aralığı belirtilen [getLineSpacing()](../../com.aspose.words/paragraphformat/\#getLineSpacing) / [setLineSpacing(double)](../../com.aspose.words/paragraphformat/\#setLineSpacing-double) değerine eşit ya da daha büyük olabilir, ancak asla daha düşük olamaz.

When [getLineSpacingRule()](../../com.aspose.words/paragraphformat/\#getLineSpacingRule) / [setLineSpacingRule(int)](../../com.aspose.words/paragraphformat/\#setLineSpacingRule-int) özelliği [LineSpacingRule.EXACTLY](../../com.aspose.words/linespacingrule/\#EXACTLY) olarak ayarlandığında, satır aralığı paragrafta daha büyük bir font kullanılsa bile belirtilen [getLineSpacing()](../../com.aspose.words/paragraphformat/\#getLineSpacing) / [setLineSpacing(double)](../../com.aspose.words/paragraphformat/\#setLineSpacing-double) değerinden asla değişmez.

 **Examples:** 

Satır aralığıyla nasıl çalışılacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | double | Paragraf için satır aralığı (puan cinsinden). |

### setLineSpacingRule(int value) {#setLineSpacingRule-int}
```
public void setLineSpacingRule(int value)
```


Paragraf için satır aralığını ayarlar.

 **Examples:** 

Satır aralığıyla nasıl çalışılacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | int | Paragraf için satır aralığı. Değer, [LineSpacingRule](../../com.aspose.words/linespacingrule/) sabitlerinden biri olmalıdır. |

### setLineUnitAfter(double value) {#setLineUnitAfter-double}
```
public void setLineUnitAfter(double value)
```


Paragraflardan sonraki boşluk miktarını (ızgara satırı cinsinden) ayarlar.

 **Examples:** 

Paragraf boşluklarını ve girintilerini nasıl değiştireceğinizi gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | double | Paragraflardan sonraki boşluk miktarı (ızgara satırı cinsinden). |

### setLineUnitBefore(double value) {#setLineUnitBefore-double}
```
public void setLineUnitBefore(double value)
```


Paragraflardan önceki boşluk miktarını (ızgara satırı cinsinden) ayarlar.

 **Examples:** 

Paragraf boşluklarını ve girintilerini nasıl değiştireceğinizi gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | double | Paragraflardan önceki boşluk miktarı (ızgara satırı cinsinden). |

### setLinesToDrop(int value) {#setLinesToDrop-int}
```
public void setLinesToDrop(int value)
```


Büyük harf (drop cap) yüksekliğini hesaplamak için kullanılan paragraf metni satır sayısını ayarlar.

 **Examples:** 

Bir drop cap boyutunun nasıl ayarlanacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | int | Büyük harf baş harf yüksekliğini hesaplamak için kullanılan paragraf metni satır sayısı. |

### setMirrorIndents(boolean value) {#setMirrorIndents-boolean}
```
public void setMirrorIndents(boolean value)
```


Sol ve sağ girintilerin aynı genişlikte olup olmadığını gösteren bir bayrak ayarlar.

 **Examples:** 

Sol ve sağ girintilerin aynı olmasını nasıl yapacağınızı gösterir.

```

 Document doc = new Document(getMyDir() + "Document.docx");
 ParagraphFormat format = doc.getFirstSection().getBody().getParagraphs().get(0).getParagraphFormat();

 format.setMirrorIndents(true);

 doc.save(getArtifactsDir() + "ParagraphFormat.MirrorIndents.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | Sol ve sağ girintilerin aynı genişlikte olup olmadığını gösteren bir işaret. |

### setNoSpaceBetweenParagraphsOfSameStyle(boolean value) {#setNoSpaceBetweenParagraphsOfSameStyle-boolean}
```
public void setNoSpaceBetweenParagraphsOfSameStyle(boolean value)
```


Doğru olduğunda, [getSpaceBefore()](../../com.aspose.words/paragraphformat/\#getSpaceBefore) / [setSpaceBefore(double)](../../com.aspose.words/paragraphformat/\#setSpaceBefore-double) ve [getSpaceAfter()](../../com.aspose.words/paragraphformat/\#getSpaceAfter) / [setSpaceAfter(double)](../../com.aspose.words/paragraphformat/\#setSpaceAfter-double) aynı stilin paragrafları arasında yok sayılacaktır.

 **Remarks:** 

Bu ayar yalnızca bir paragraf stiline uygulandığında etkili olur. Doğrudan bir paragrafa uygulanırsa etkisi yoktur.

 **Examples:** 

Aynı stile sahip paragraflar arasında boşluk bırakmamanın nasıl uygulanacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | İlgili  boolean  değeri. |

### setOutlineLevel(int value) {#setOutlineLevel-int}
```
public void setOutlineLevel(int value)
```


Paragrafın belgedeki taslak seviyesini belirtir.

 **Examples:** 

Paragraf anahat seviyelerini yapılandırarak katlanabilir metin oluşturmayı gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | int | İlgili int değeri. Değer, [OutlineLevel](../../com.aspose.words/outlinelevel/) sabitlerinden biri olmalıdır. |

### setPageBreakBefore(boolean value) {#setPageBreakBefore-boolean}
```
public void setPageBreakBefore(boolean value)
```


Doğru, paragraftan önce bir sayfa sonu zorlanıyorsa.

 **Examples:** 

Paragrafların başında sayfa sonu eklemenin nasıl yapılacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | İlgili  boolean  değeri. |

### setRightIndent(double value) {#setRightIndent-double}
```
public void setRightIndent(double value)
```


Paragraf için sağ girintiyi temsil eden değeri (puan cinsinden) ayarlar.

 **Examples:** 

Paragraf biçimlendirmesini, merkezin dışına kaymış metin oluşturmak için nasıl yapılandıracağınızı gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | double | Paragraf için sağ girintiyi temsil eden değer (puan cinsinden). |

### setSnapToGrid(boolean value) {#setSnapToGrid-boolean}
```
public void setSnapToGrid(boolean value)
```


Geçerli paragrafın, paragraftaki içeriği düzenlerken sayfa başına belge ızgara satırları ayarlarını kullanıp kullanmayacağını belirtir.

 **Examples:** 

Her sayfanın sahip olabileceği satır sayısı için bir sınırın nasıl belirtileceğini gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | İlgili  boolean  değeri. |

### setSpaceAfter(double value) {#setSpaceAfter-double}
```
public void setSpaceAfter(double value)
```


Paragraftan sonraki boşluk miktarını (puan cinsinden) ayarlar.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | double | Paragraftan sonraki boşluk miktarı (puan cinsinden). |

### setSpaceAfterAuto(boolean value) {#setSpaceAfterAuto-boolean}
```
public void setSpaceAfterAuto(boolean value)
```


Doğru, paragraftan sonraki boşluk miktarı otomatik olarak ayarlanıyorsa.

 **Remarks:** 

true olarak ayarlandığında, [getSpaceAfter()](../../com.aspose.words/paragraphformat/\#getSpaceAfter) / [setSpaceAfter(double)](../../com.aspose.words/paragraphformat/\#setSpaceAfter-double) etkisini geçersiz kılar.

Paragraf Ön Boşluğu ve Son Boşluğu'nu Otomatik olarak ayarladığınızda, Microsoft Word aşağıdaki kurallara göre paragraflar arasında otomatik olarak 14 nokta boşluk ekler:

 *  Normally, spacing is added after all paragraphs.
 *  In a bulleted or numbered list, spacing is added only after the last item in the list. Spacing is not added between the list items.
 *  In a nested bulleted or numbered list spacing is not added.
 *  Spacing is normally added after a table.
 *  Spacing is not added after a table if it is the last block in a table cell.
 *  Spacing is not added after the last paragraph in a table cell.

 **Examples:** 

Otomatik paragraf boşluğunu ayarlamanın nasıl yapılacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | İlgili  boolean  değeri. |

### setSpaceBefore(double value) {#setSpaceBefore-double}
```
public void setSpaceBefore(double value)
```


Paragrafın önündeki boşluk miktarını (nokta cinsinden) ayarlar.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | double | Paragraftan önceki boşluk miktarı (puan cinsinden). |

### setSpaceBeforeAuto(boolean value) {#setSpaceBeforeAuto-boolean}
```
public void setSpaceBeforeAuto(boolean value)
```


Doğru, paragraftan önceki boşluk miktarı otomatik olarak ayarlanıyorsa.

 **Remarks:** 

true olarak ayarlandığında, [getSpaceBefore()](../../com.aspose.words/paragraphformat/\#getSpaceBefore) / [setSpaceBefore(double)](../../com.aspose.words/paragraphformat/\#setSpaceBefore-double) etkisini geçersiz kılar.

Paragraf Ön Boşluğu ve Son Boşluğu'nu Otomatik olarak ayarladığınızda, Microsoft Word aşağıdaki kurallara göre paragraflar arasında otomatik olarak 14 nokta boşluk ekler:

 *  Normally, spacing is added after all paragraphs.
 *  In a bulleted or numbered list, spacing is added only after the last item in the list. Spacing is not added between the list items.
 *  In a nested bulleted or numbered list spacing is not added.
 *  Spacing is normally added after a table.
 *  Spacing is not added after a table if it is the last block in a table cell.
 *  Spacing is not added after the last paragraph in a table cell.

 **Examples:** 

Otomatik paragraf boşluğunu ayarlamanın nasıl yapılacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | İlgili  boolean  değeri. |

### setStyle(Style value) {#setStyle-com.aspose.words.Style}
```
public void setStyle(Style value)
```


Bu biçimlendirmeye uygulanan paragraf stilini ayarlar.

 **Examples:** 

Liste biçimlendirmeli bir paragraf stilinin nasıl oluşturulacağını ve kullanılacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | [Style](../../com.aspose.words/style/) | Bu biçimlendirmeye uygulanan paragraf stili. |

### setStyleIdentifier(int value) {#setStyleIdentifier-int}
```
public void setStyleIdentifier(int value)
```


Bu biçimlendirmeye uygulanan paragraf stilinin bölge bağımsız stil tanımlayıcısını ayarlar.

 **Examples:** 

Başlık stillerini giriş olarak kullanarak bir belgeye İçindekiler Tablosu (TOC) nasıl eklenir gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | int | Bu biçimlendirmeye uygulanan paragraf stilinin yerel bağımsız stil tanımlayıcısı. Değer, [StyleIdentifier](../../com.aspose.words/styleidentifier/) sabitlerinden biri olmalıdır. |

### setStyleName(String value) {#setStyleName-java.lang.String}
```
public void setStyleName(String value)
```


Bu biçimlendirmeye uygulanan paragraf stilinin adını ayarlar.

 **Examples:** 

Aspose.Words belgesini elle nasıl oluşturacağınızı gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.lang.String | Bu biçimlendirmeye uygulanan paragraf stilinin adı. |

### setSuppressAutoHyphens(boolean value) {#setSuppressAutoHyphens-boolean}
```
public void setSuppressAutoHyphens(boolean value)
```


Geçerli paragrafın, belge ayarlarında uygulanan herhangi bir hecelemeye tabi olup olmayacağını belirtir.

 **Examples:** 

Bir paragraf için hecelemeyi nasıl bastıracağınızı gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | İlgili  boolean  değeri. |

### setSuppressLineNumbers(boolean value) {#setSuppressLineNumbers-boolean}
```
public void setSuppressLineNumbers(boolean value)
```


Geçerli paragrafın satırlarının, üst bölümde uygulanan satır numaralandırmasından muaf tutulup tutulmayacağını belirtir.

 **Examples:** 

Bir bölüm için satır numaralandırmayı nasıl etkinleştireceğinizi gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | İlgili  boolean  değeri. |

### setWidowControl(boolean value) {#setWidowControl-boolean}
```
public void setWidowControl(boolean value)
```


Paragraftaki ilk ve son satırların, paragrafın geri kalanıyla aynı sayfada kalması durumunda doğrudur.

 **Examples:** 

Bir paragraf için yetim/yalnız satır kontrolünü nasıl etkinleştireceğinizi gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | İlgili  boolean  değeri. |

### setWordWrap(boolean value) {#setWordWrap-boolean}
```
public void setWordWrap(boolean value)
```


Bu özellik false ise, bir kelimenin ortasındaki Latin metni mevcut paragrafta bölünebilir. Aksi takdirde Latin metni bütün kelimeler halinde bölünür.

 **Examples:** 

Asya tipografisi için özel özelliklerin nasıl ayarlanacağını gösterir.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 ParagraphFormat format = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat();
 format.setFarEastLineBreakControl(true);
 format.setWordWrap(false);
 format.setHangingPunctuation(true);

 doc.save(getArtifactsDir() + "ParagraphFormat.AsianTypographyProperties.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | İlgili  boolean  değeri. |

