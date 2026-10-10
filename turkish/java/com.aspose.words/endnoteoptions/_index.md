---
title: "EndnoteOptions"
linktitle: "EndnoteOptions"
second_title: "Aspose.Words Java için"
description: "Java'da bir belge veya bölüm için dipnot numaralandırma seçeneklerini temsil eder."
type: docs
weight: 189
url: /tr/java/com.aspose.words/endnoteoptions/
---

**Inheritance:**
java.lang.Object
```
public class EndnoteOptions
```

Bir belge veya bölüm için dipnot numaralandırma seçeneklerini temsil eder.

Daha fazla bilgi edinmek için [ Working with Footnote and Endnote ][Working with Footnote and Endnote] dokümantasyon makalesini ziyaret edin.

 **Examples:** 

Belgenin dipnotları topladığı ve gösterdiği farklı bir yeri nasıl seçeceğinizi gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // An endnote is a way to attach a reference or a side comment to text
 // that does not interfere with the main body text's flow.
 // Inserting an endnote adds a small superscript reference symbol
 // at the main body text where we insert the endnote.
 // Each endnote also creates an entry at the end of the document, consisting of a symbol
 // that matches the reference symbol in the main body text.
 // The reference text that we pass to the document builder's "InsertEndnote" method.
 builder.write("Hello world!");
 builder.insertFootnote(FootnoteType.ENDNOTE, "Endnote contents.");
 builder.insertBreak(BreakType.SECTION_BREAK_NEW_PAGE);
 builder.write("This is the second section.");

 // We can use the "Position" property to determine where the document will place all its endnotes.
 // If we set the value of the "Position" property to "EndnotePosition.EndOfDocument",
 // every footnote will show up in a collection at the end of the document. This is the default value.
 // If we set the value of the "Position" property to "EndnotePosition.EndOfSection",
 // every footnote will show up in a collection at the end of the section whose text contains the endnote's reference mark.
 doc.getEndnoteOptions().setPosition(endnotePosition);

 doc.save(getArtifactsDir() + "InlineStory.PositionEndnote.docx");
 
```

Dipnot/sonnot referans işaretlerinin sayı stilini değiştirmenin nasıl yapılacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Footnotes and endnotes are a way to attach a reference or a side comment to text
 // that does not interfere with the main body text's flow.
 // Inserting a footnote/endnote adds a small superscript reference symbol
 // at the main body text where we insert the footnote/endnote.
 // Each footnote/endnote also creates an entry, which consists of a symbol that matches the reference
 // symbol in the main body text. The reference text that we pass to the document builder's "InsertEndnote" method.
 // Footnote entries, by default, show up at the bottom of each page that contains
 // their reference symbols, and endnotes show up at the end of the document.
 builder.write("Text 1. ");
 builder.insertFootnote(FootnoteType.FOOTNOTE, "Footnote 1.");
 builder.write("Text 2. ");
 builder.insertFootnote(FootnoteType.FOOTNOTE, "Footnote 2.");
 builder.write("Text 3. ");
 builder.insertFootnote(FootnoteType.FOOTNOTE, "Footnote 3.", "Custom footnote reference mark");

 builder.insertParagraph();

 builder.write("Text 1. ");
 builder.insertFootnote(FootnoteType.ENDNOTE, "Endnote 1.");
 builder.write("Text 2. ");
 builder.insertFootnote(FootnoteType.ENDNOTE, "Endnote 2.");
 builder.write("Text 3. ");
 builder.insertFootnote(FootnoteType.ENDNOTE, "Endnote 3.", "Custom endnote reference mark");

 // By default, the reference symbol for each footnote and endnote is its index
 // among all the document's footnotes/endnotes. Each document maintains separate counts
 // for footnotes and for endnotes. By default, footnotes display their numbers using Arabic numerals,
 // and endnotes display their numbers in lowercase Roman numerals.
 Assert.assertEquals(NumberStyle.ARABIC, doc.getFootnoteOptions().getNumberStyle());
 Assert.assertEquals(NumberStyle.LOWERCASE_ROMAN, doc.getEndnoteOptions().getNumberStyle());

 // We can use the "NumberStyle" property to apply custom numbering styles to footnotes and endnotes.
 // This will not affect footnotes/endnotes with custom reference marks.
 doc.getFootnoteOptions().setNumberStyle(NumberStyle.UPPERCASE_ROMAN);
 doc.getEndnoteOptions().setNumberStyle(NumberStyle.UPPERCASE_LETTER);

 doc.save(getArtifactsDir() + "InlineStory.RefMarkNumberStyle.docx");
 
```

Belgenin belirli yerlerinde dipnot/sonnot numaralandırmasını yeniden başlatmanın nasıl yapılacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Footnotes and endnotes are a way to attach a reference or a side comment to text
 // that does not interfere with the main body text's flow.
 // Inserting a footnote/endnote adds a small superscript reference symbol
 // at the main body text where we insert the footnote/endnote.
 // Each footnote/endnote also creates an entry, which consists of a symbol that matches the reference
 // symbol in the main body text. The reference text that we pass to the document builder's "InsertEndnote" method.
 // Footnote entries, by default, show up at the bottom of each page that contains
 // their reference symbols, and endnotes show up at the end of the document.
 builder.write("Text 1. ");
 builder.insertFootnote(FootnoteType.FOOTNOTE, "Footnote 1.");
 builder.write("Text 2. ");
 builder.insertFootnote(FootnoteType.FOOTNOTE, "Footnote 2.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.write("Text 3. ");
 builder.insertFootnote(FootnoteType.FOOTNOTE, "Footnote 3.");
 builder.write("Text 4. ");
 builder.insertFootnote(FootnoteType.FOOTNOTE, "Footnote 4.");

 builder.insertBreak(BreakType.PAGE_BREAK);

 builder.write("Text 1. ");
 builder.insertFootnote(FootnoteType.ENDNOTE, "Endnote 1.");
 builder.write("Text 2. ");
 builder.insertFootnote(FootnoteType.ENDNOTE, "Endnote 2.");
 builder.insertBreak(BreakType.SECTION_BREAK_NEW_PAGE);
 builder.write("Text 3. ");
 builder.insertFootnote(FootnoteType.ENDNOTE, "Endnote 3.");
 builder.write("Text 4. ");
 builder.insertFootnote(FootnoteType.ENDNOTE, "Endnote 4.");

 // By default, the reference symbol for each footnote and endnote is its index
 // among all the document's footnotes/endnotes. Each document maintains separate counts
 // for footnotes and endnotes and does not restart these counts at any point.
 Assert.assertEquals(doc.getFootnoteOptions().getRestartRule(), FootnoteNumberingRule.DEFAULT);
 Assert.assertEquals(FootnoteNumberingRule.DEFAULT, FootnoteNumberingRule.CONTINUOUS);

 // We can use the "RestartRule" property to get the document to restart
 // the footnote/endnote counts at a new page or section.
 doc.getFootnoteOptions().setRestartRule(FootnoteNumberingRule.RESTART_PAGE);
 doc.getEndnoteOptions().setRestartRule(FootnoteNumberingRule.RESTART_SECTION);

 doc.save(getArtifactsDir() + "InlineStory.NumberingRule.docx");
 
```

Belgenin dipnot/sonnot sayımına başladığı sayıyı ayarlamanın nasıl yapılacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Footnotes and endnotes are a way to attach a reference or a side comment to text
 // that does not interfere with the main body text's flow.
 // Inserting a footnote/endnote adds a small superscript reference symbol
 // at the main body text where we insert the footnote/endnote.
 // Each footnote/endnote also creates an entry, which consists of a symbol
 // that matches the reference symbol in the main body text.
 // The reference text that we pass to the document builder's "InsertEndnote" method.
 // Footnote entries, by default, show up at the bottom of each page that contains
 // their reference symbols, and endnotes show up at the end of the document.
 builder.write("Text 1. ");
 builder.insertFootnote(FootnoteType.FOOTNOTE, "Footnote 1.");
 builder.write("Text 2. ");
 builder.insertFootnote(FootnoteType.FOOTNOTE, "Footnote 2.");
 builder.write("Text 3. ");
 builder.insertFootnote(FootnoteType.FOOTNOTE, "Footnote 3.");

 builder.insertParagraph();

 builder.write("Text 1. ");
 builder.insertFootnote(FootnoteType.ENDNOTE, "Endnote 1.");
 builder.write("Text 2. ");
 builder.insertFootnote(FootnoteType.ENDNOTE, "Endnote 2.");
 builder.write("Text 3. ");
 builder.insertFootnote(FootnoteType.ENDNOTE, "Endnote 3.");

 // By default, the reference symbol for each footnote and endnote is its index
 // among all the document's footnotes/endnotes. Each document maintains separate counts
 // for footnotes and for endnotes, which both begin at 1.
 Assert.assertEquals(1, doc.getFootnoteOptions().getStartNumber());
 Assert.assertEquals(1, doc.getEndnoteOptions().getStartNumber());

 // We can use the "StartNumber" property to get the document to
 // begin a footnote or endnote count at a different number.
 doc.getEndnoteOptions().setNumberStyle(NumberStyle.ARABIC);
 doc.getEndnoteOptions().setStartNumber(50);

 doc.save(getArtifactsDir() + "InlineStory.StartNumber.docx");
 
```


[Working with Footnote and Endnote]: https://docs.aspose.com/words/java/working-with-footnote-and-endnote/
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [getLocation()](#getLocation) |  |
| [getNumberStyle()](#getNumberStyle) | Otomatik numaralandırılmış dipnotlar için sayı biçimini belirtir. |
| [getPosition()](#getPosition) | Dipnotların konumunu belirtir. |
| [getRestartRule()](#getRestartRule) | Otomatik numaralandırmanın ne zaman yeniden başlayacağını belirler. |
| [getStartNumber()](#getStartNumber) | İlk otomatik numaralandırılmış dipnot için başlangıç numarasını veya karakterini belirtir. |
| [setLocation(int value)](#setLocation-int) |  |
| [setNumberStyle(int value)](#setNumberStyle-int) | Otomatik numaralandırılmış dipnotlar için sayı biçimini belirtir. |
| [setPosition(int value)](#setPosition-int) | Dipnotların konumunu belirtir. |
| [setRestartRule(int value)](#setRestartRule-int) | Otomatik numaralandırmanın ne zaman yeniden başlayacağını belirler. |
| [setStartNumber(int value)](#setStartNumber-int) | İlk otomatik numaralandırılmış dipnot için başlangıç numarasını veya karakterini belirtir. |
### getLocation() {#getLocation}
```
public int getLocation()
```




**Returns:**
int
### getNumberStyle() {#getNumberStyle}
```
public int getNumberStyle()
```


Otomatik numaralandırılmış dipnotlar için sayı biçimini belirtir.

 **Remarks:** 

Bu özellik için tüm sayı stilleri uygulanabilir değildir. Uygulanabilir sayı stillerinin listesi için Microsoft Word'deki Dipnot veya Sonnot Ekle iletişim kutusuna bakın. Uygulanabilir olmayan bir sayı stili seçerseniz, Microsoft Word varsayılan bir değere dönecektir.

 **Examples:** 

Dipnot/sonnot referans işaretlerinin sayı stilini değiştirmenin nasıl yapılacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Footnotes and endnotes are a way to attach a reference or a side comment to text
 // that does not interfere with the main body text's flow.
 // Inserting a footnote/endnote adds a small superscript reference symbol
 // at the main body text where we insert the footnote/endnote.
 // Each footnote/endnote also creates an entry, which consists of a symbol that matches the reference
 // symbol in the main body text. The reference text that we pass to the document builder's "InsertEndnote" method.
 // Footnote entries, by default, show up at the bottom of each page that contains
 // their reference symbols, and endnotes show up at the end of the document.
 builder.write("Text 1. ");
 builder.insertFootnote(FootnoteType.FOOTNOTE, "Footnote 1.");
 builder.write("Text 2. ");
 builder.insertFootnote(FootnoteType.FOOTNOTE, "Footnote 2.");
 builder.write("Text 3. ");
 builder.insertFootnote(FootnoteType.FOOTNOTE, "Footnote 3.", "Custom footnote reference mark");

 builder.insertParagraph();

 builder.write("Text 1. ");
 builder.insertFootnote(FootnoteType.ENDNOTE, "Endnote 1.");
 builder.write("Text 2. ");
 builder.insertFootnote(FootnoteType.ENDNOTE, "Endnote 2.");
 builder.write("Text 3. ");
 builder.insertFootnote(FootnoteType.ENDNOTE, "Endnote 3.", "Custom endnote reference mark");

 // By default, the reference symbol for each footnote and endnote is its index
 // among all the document's footnotes/endnotes. Each document maintains separate counts
 // for footnotes and for endnotes. By default, footnotes display their numbers using Arabic numerals,
 // and endnotes display their numbers in lowercase Roman numerals.
 Assert.assertEquals(NumberStyle.ARABIC, doc.getFootnoteOptions().getNumberStyle());
 Assert.assertEquals(NumberStyle.LOWERCASE_ROMAN, doc.getEndnoteOptions().getNumberStyle());

 // We can use the "NumberStyle" property to apply custom numbering styles to footnotes and endnotes.
 // This will not affect footnotes/endnotes with custom reference marks.
 doc.getFootnoteOptions().setNumberStyle(NumberStyle.UPPERCASE_ROMAN);
 doc.getEndnoteOptions().setNumberStyle(NumberStyle.UPPERCASE_LETTER);

 doc.save(getArtifactsDir() + "InlineStory.RefMarkNumberStyle.docx");
 
```

**Returns:**
int - İlgili  int  değeri. Döndürülen değer, [NumberStyle](../../com.aspose.words/numberstyle/) sabitlerinden biridir.
### getPosition() {#getPosition}
```
public int getPosition()
```


Dipnotların konumunu belirtir.

 **Examples:** 

Belgenin dipnotları topladığı ve gösterdiği farklı bir yeri nasıl seçeceğinizi gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // An endnote is a way to attach a reference or a side comment to text
 // that does not interfere with the main body text's flow.
 // Inserting an endnote adds a small superscript reference symbol
 // at the main body text where we insert the endnote.
 // Each endnote also creates an entry at the end of the document, consisting of a symbol
 // that matches the reference symbol in the main body text.
 // The reference text that we pass to the document builder's "InsertEndnote" method.
 builder.write("Hello world!");
 builder.insertFootnote(FootnoteType.ENDNOTE, "Endnote contents.");
 builder.insertBreak(BreakType.SECTION_BREAK_NEW_PAGE);
 builder.write("This is the second section.");

 // We can use the "Position" property to determine where the document will place all its endnotes.
 // If we set the value of the "Position" property to "EndnotePosition.EndOfDocument",
 // every footnote will show up in a collection at the end of the document. This is the default value.
 // If we set the value of the "Position" property to "EndnotePosition.EndOfSection",
 // every footnote will show up in a collection at the end of the section whose text contains the endnote's reference mark.
 doc.getEndnoteOptions().setPosition(endnotePosition);

 doc.save(getArtifactsDir() + "InlineStory.PositionEndnote.docx");
 
```

**Returns:**
int - İlgili  int  değeri. Döndürülen değer, [EndnotePosition](../../com.aspose.words/endnoteposition/) sabitlerinden biridir.
### getRestartRule() {#getRestartRule}
```
public int getRestartRule()
```


Otomatik numaralandırmanın ne zaman yeniden başlayacağını belirler.

 **Remarks:** 

Tüm değerler dipnotlar için geçerli değildir. Hangi değerlerin geçerli olduğunu belirlemek için [FootnoteNumberingRule](../../com.aspose.words/footnotenumberingrule/) bölümüne bakın.

 **Examples:** 

Belgenin belirli yerlerinde dipnot/sonnot numaralandırmasını yeniden başlatmanın nasıl yapılacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Footnotes and endnotes are a way to attach a reference or a side comment to text
 // that does not interfere with the main body text's flow.
 // Inserting a footnote/endnote adds a small superscript reference symbol
 // at the main body text where we insert the footnote/endnote.
 // Each footnote/endnote also creates an entry, which consists of a symbol that matches the reference
 // symbol in the main body text. The reference text that we pass to the document builder's "InsertEndnote" method.
 // Footnote entries, by default, show up at the bottom of each page that contains
 // their reference symbols, and endnotes show up at the end of the document.
 builder.write("Text 1. ");
 builder.insertFootnote(FootnoteType.FOOTNOTE, "Footnote 1.");
 builder.write("Text 2. ");
 builder.insertFootnote(FootnoteType.FOOTNOTE, "Footnote 2.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.write("Text 3. ");
 builder.insertFootnote(FootnoteType.FOOTNOTE, "Footnote 3.");
 builder.write("Text 4. ");
 builder.insertFootnote(FootnoteType.FOOTNOTE, "Footnote 4.");

 builder.insertBreak(BreakType.PAGE_BREAK);

 builder.write("Text 1. ");
 builder.insertFootnote(FootnoteType.ENDNOTE, "Endnote 1.");
 builder.write("Text 2. ");
 builder.insertFootnote(FootnoteType.ENDNOTE, "Endnote 2.");
 builder.insertBreak(BreakType.SECTION_BREAK_NEW_PAGE);
 builder.write("Text 3. ");
 builder.insertFootnote(FootnoteType.ENDNOTE, "Endnote 3.");
 builder.write("Text 4. ");
 builder.insertFootnote(FootnoteType.ENDNOTE, "Endnote 4.");

 // By default, the reference symbol for each footnote and endnote is its index
 // among all the document's footnotes/endnotes. Each document maintains separate counts
 // for footnotes and endnotes and does not restart these counts at any point.
 Assert.assertEquals(doc.getFootnoteOptions().getRestartRule(), FootnoteNumberingRule.DEFAULT);
 Assert.assertEquals(FootnoteNumberingRule.DEFAULT, FootnoteNumberingRule.CONTINUOUS);

 // We can use the "RestartRule" property to get the document to restart
 // the footnote/endnote counts at a new page or section.
 doc.getFootnoteOptions().setRestartRule(FootnoteNumberingRule.RESTART_PAGE);
 doc.getEndnoteOptions().setRestartRule(FootnoteNumberingRule.RESTART_SECTION);

 doc.save(getArtifactsDir() + "InlineStory.NumberingRule.docx");
 
```

**Returns:**
int - İlgili  int  değeri. Döndürülen değer, [FootnoteNumberingRule](../../com.aspose.words/footnotenumberingrule/) sabitlerinden biridir.
### getStartNumber() {#getStartNumber}
```
public int getStartNumber()
```


İlk otomatik numaralandırılmış dipnot için başlangıç numarasını veya karakterini belirtir.

 **Remarks:** 

Bu özellik yalnızca [getRestartRule()](../../com.aspose.words/endnoteoptions/\#getRestartRule) / [setRestartRule(int)](../../com.aspose.words/endnoteoptions/\#setRestartRule-int) [FootnoteNumberingRule.CONTINUOUS](../../com.aspose.words/footnotenumberingrule/\#CONTINUOUS) olarak ayarlandığında etkili olur.

 **Examples:** 

Belgenin dipnot/sonnot sayımına başladığı sayıyı ayarlamanın nasıl yapılacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Footnotes and endnotes are a way to attach a reference or a side comment to text
 // that does not interfere with the main body text's flow.
 // Inserting a footnote/endnote adds a small superscript reference symbol
 // at the main body text where we insert the footnote/endnote.
 // Each footnote/endnote also creates an entry, which consists of a symbol
 // that matches the reference symbol in the main body text.
 // The reference text that we pass to the document builder's "InsertEndnote" method.
 // Footnote entries, by default, show up at the bottom of each page that contains
 // their reference symbols, and endnotes show up at the end of the document.
 builder.write("Text 1. ");
 builder.insertFootnote(FootnoteType.FOOTNOTE, "Footnote 1.");
 builder.write("Text 2. ");
 builder.insertFootnote(FootnoteType.FOOTNOTE, "Footnote 2.");
 builder.write("Text 3. ");
 builder.insertFootnote(FootnoteType.FOOTNOTE, "Footnote 3.");

 builder.insertParagraph();

 builder.write("Text 1. ");
 builder.insertFootnote(FootnoteType.ENDNOTE, "Endnote 1.");
 builder.write("Text 2. ");
 builder.insertFootnote(FootnoteType.ENDNOTE, "Endnote 2.");
 builder.write("Text 3. ");
 builder.insertFootnote(FootnoteType.ENDNOTE, "Endnote 3.");

 // By default, the reference symbol for each footnote and endnote is its index
 // among all the document's footnotes/endnotes. Each document maintains separate counts
 // for footnotes and for endnotes, which both begin at 1.
 Assert.assertEquals(1, doc.getFootnoteOptions().getStartNumber());
 Assert.assertEquals(1, doc.getEndnoteOptions().getStartNumber());

 // We can use the "StartNumber" property to get the document to
 // begin a footnote or endnote count at a different number.
 doc.getEndnoteOptions().setNumberStyle(NumberStyle.ARABIC);
 doc.getEndnoteOptions().setStartNumber(50);

 doc.save(getArtifactsDir() + "InlineStory.StartNumber.docx");
 
```

**Returns:**
int - İlgili  int  değeri.
### setLocation(int value) {#setLocation-int}
```
public void setLocation(int value)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | int |  |

### setNumberStyle(int value) {#setNumberStyle-int}
```
public void setNumberStyle(int value)
```


Otomatik numaralandırılmış dipnotlar için sayı biçimini belirtir.

 **Remarks:** 

Bu özellik için tüm sayı stilleri uygulanabilir değildir. Uygulanabilir sayı stillerinin listesi için Microsoft Word'deki Dipnot veya Sonnot Ekle iletişim kutusuna bakın. Uygulanabilir olmayan bir sayı stili seçerseniz, Microsoft Word varsayılan bir değere dönecektir.

 **Examples:** 

Dipnot/sonnot referans işaretlerinin sayı stilini değiştirmenin nasıl yapılacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Footnotes and endnotes are a way to attach a reference or a side comment to text
 // that does not interfere with the main body text's flow.
 // Inserting a footnote/endnote adds a small superscript reference symbol
 // at the main body text where we insert the footnote/endnote.
 // Each footnote/endnote also creates an entry, which consists of a symbol that matches the reference
 // symbol in the main body text. The reference text that we pass to the document builder's "InsertEndnote" method.
 // Footnote entries, by default, show up at the bottom of each page that contains
 // their reference symbols, and endnotes show up at the end of the document.
 builder.write("Text 1. ");
 builder.insertFootnote(FootnoteType.FOOTNOTE, "Footnote 1.");
 builder.write("Text 2. ");
 builder.insertFootnote(FootnoteType.FOOTNOTE, "Footnote 2.");
 builder.write("Text 3. ");
 builder.insertFootnote(FootnoteType.FOOTNOTE, "Footnote 3.", "Custom footnote reference mark");

 builder.insertParagraph();

 builder.write("Text 1. ");
 builder.insertFootnote(FootnoteType.ENDNOTE, "Endnote 1.");
 builder.write("Text 2. ");
 builder.insertFootnote(FootnoteType.ENDNOTE, "Endnote 2.");
 builder.write("Text 3. ");
 builder.insertFootnote(FootnoteType.ENDNOTE, "Endnote 3.", "Custom endnote reference mark");

 // By default, the reference symbol for each footnote and endnote is its index
 // among all the document's footnotes/endnotes. Each document maintains separate counts
 // for footnotes and for endnotes. By default, footnotes display their numbers using Arabic numerals,
 // and endnotes display their numbers in lowercase Roman numerals.
 Assert.assertEquals(NumberStyle.ARABIC, doc.getFootnoteOptions().getNumberStyle());
 Assert.assertEquals(NumberStyle.LOWERCASE_ROMAN, doc.getEndnoteOptions().getNumberStyle());

 // We can use the "NumberStyle" property to apply custom numbering styles to footnotes and endnotes.
 // This will not affect footnotes/endnotes with custom reference marks.
 doc.getFootnoteOptions().setNumberStyle(NumberStyle.UPPERCASE_ROMAN);
 doc.getEndnoteOptions().setNumberStyle(NumberStyle.UPPERCASE_LETTER);

 doc.save(getArtifactsDir() + "InlineStory.RefMarkNumberStyle.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | int | İlgili  int  değeri. Değer, [NumberStyle](../../com.aspose.words/numberstyle/) sabitlerinden biri olmalıdır. |

### setPosition(int value) {#setPosition-int}
```
public void setPosition(int value)
```


Dipnotların konumunu belirtir.

 **Examples:** 

Belgenin dipnotları topladığı ve gösterdiği farklı bir yeri nasıl seçeceğinizi gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // An endnote is a way to attach a reference or a side comment to text
 // that does not interfere with the main body text's flow.
 // Inserting an endnote adds a small superscript reference symbol
 // at the main body text where we insert the endnote.
 // Each endnote also creates an entry at the end of the document, consisting of a symbol
 // that matches the reference symbol in the main body text.
 // The reference text that we pass to the document builder's "InsertEndnote" method.
 builder.write("Hello world!");
 builder.insertFootnote(FootnoteType.ENDNOTE, "Endnote contents.");
 builder.insertBreak(BreakType.SECTION_BREAK_NEW_PAGE);
 builder.write("This is the second section.");

 // We can use the "Position" property to determine where the document will place all its endnotes.
 // If we set the value of the "Position" property to "EndnotePosition.EndOfDocument",
 // every footnote will show up in a collection at the end of the document. This is the default value.
 // If we set the value of the "Position" property to "EndnotePosition.EndOfSection",
 // every footnote will show up in a collection at the end of the section whose text contains the endnote's reference mark.
 doc.getEndnoteOptions().setPosition(endnotePosition);

 doc.save(getArtifactsDir() + "InlineStory.PositionEndnote.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | int | İlgili  int  değeri. Değer, [EndnotePosition](../../com.aspose.words/endnoteposition/) sabitlerinden biri olmalıdır. |

### setRestartRule(int value) {#setRestartRule-int}
```
public void setRestartRule(int value)
```


Otomatik numaralandırmanın ne zaman yeniden başlayacağını belirler.

 **Remarks:** 

Tüm değerler dipnotlar için geçerli değildir. Hangi değerlerin geçerli olduğunu belirlemek için [FootnoteNumberingRule](../../com.aspose.words/footnotenumberingrule/) bölümüne bakın.

 **Examples:** 

Belgenin belirli yerlerinde dipnot/sonnot numaralandırmasını yeniden başlatmanın nasıl yapılacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Footnotes and endnotes are a way to attach a reference or a side comment to text
 // that does not interfere with the main body text's flow.
 // Inserting a footnote/endnote adds a small superscript reference symbol
 // at the main body text where we insert the footnote/endnote.
 // Each footnote/endnote also creates an entry, which consists of a symbol that matches the reference
 // symbol in the main body text. The reference text that we pass to the document builder's "InsertEndnote" method.
 // Footnote entries, by default, show up at the bottom of each page that contains
 // their reference symbols, and endnotes show up at the end of the document.
 builder.write("Text 1. ");
 builder.insertFootnote(FootnoteType.FOOTNOTE, "Footnote 1.");
 builder.write("Text 2. ");
 builder.insertFootnote(FootnoteType.FOOTNOTE, "Footnote 2.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.write("Text 3. ");
 builder.insertFootnote(FootnoteType.FOOTNOTE, "Footnote 3.");
 builder.write("Text 4. ");
 builder.insertFootnote(FootnoteType.FOOTNOTE, "Footnote 4.");

 builder.insertBreak(BreakType.PAGE_BREAK);

 builder.write("Text 1. ");
 builder.insertFootnote(FootnoteType.ENDNOTE, "Endnote 1.");
 builder.write("Text 2. ");
 builder.insertFootnote(FootnoteType.ENDNOTE, "Endnote 2.");
 builder.insertBreak(BreakType.SECTION_BREAK_NEW_PAGE);
 builder.write("Text 3. ");
 builder.insertFootnote(FootnoteType.ENDNOTE, "Endnote 3.");
 builder.write("Text 4. ");
 builder.insertFootnote(FootnoteType.ENDNOTE, "Endnote 4.");

 // By default, the reference symbol for each footnote and endnote is its index
 // among all the document's footnotes/endnotes. Each document maintains separate counts
 // for footnotes and endnotes and does not restart these counts at any point.
 Assert.assertEquals(doc.getFootnoteOptions().getRestartRule(), FootnoteNumberingRule.DEFAULT);
 Assert.assertEquals(FootnoteNumberingRule.DEFAULT, FootnoteNumberingRule.CONTINUOUS);

 // We can use the "RestartRule" property to get the document to restart
 // the footnote/endnote counts at a new page or section.
 doc.getFootnoteOptions().setRestartRule(FootnoteNumberingRule.RESTART_PAGE);
 doc.getEndnoteOptions().setRestartRule(FootnoteNumberingRule.RESTART_SECTION);

 doc.save(getArtifactsDir() + "InlineStory.NumberingRule.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | int | İlgili int değeri. Değer, [FootnoteNumberingRule](../../com.aspose.words/footnotenumberingrule/) sabitlerinden biri olmalıdır. |

### setStartNumber(int value) {#setStartNumber-int}
```
public void setStartNumber(int value)
```


İlk otomatik numaralandırılmış dipnot için başlangıç numarasını veya karakterini belirtir.

 **Remarks:** 

Bu özellik yalnızca [getRestartRule()](../../com.aspose.words/endnoteoptions/\#getRestartRule) / [setRestartRule(int)](../../com.aspose.words/endnoteoptions/\#setRestartRule-int) [FootnoteNumberingRule.CONTINUOUS](../../com.aspose.words/footnotenumberingrule/\#CONTINUOUS) olarak ayarlandığında etkili olur.

 **Examples:** 

Belgenin dipnot/sonnot sayımına başladığı sayıyı ayarlamanın nasıl yapılacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Footnotes and endnotes are a way to attach a reference or a side comment to text
 // that does not interfere with the main body text's flow.
 // Inserting a footnote/endnote adds a small superscript reference symbol
 // at the main body text where we insert the footnote/endnote.
 // Each footnote/endnote also creates an entry, which consists of a symbol
 // that matches the reference symbol in the main body text.
 // The reference text that we pass to the document builder's "InsertEndnote" method.
 // Footnote entries, by default, show up at the bottom of each page that contains
 // their reference symbols, and endnotes show up at the end of the document.
 builder.write("Text 1. ");
 builder.insertFootnote(FootnoteType.FOOTNOTE, "Footnote 1.");
 builder.write("Text 2. ");
 builder.insertFootnote(FootnoteType.FOOTNOTE, "Footnote 2.");
 builder.write("Text 3. ");
 builder.insertFootnote(FootnoteType.FOOTNOTE, "Footnote 3.");

 builder.insertParagraph();

 builder.write("Text 1. ");
 builder.insertFootnote(FootnoteType.ENDNOTE, "Endnote 1.");
 builder.write("Text 2. ");
 builder.insertFootnote(FootnoteType.ENDNOTE, "Endnote 2.");
 builder.write("Text 3. ");
 builder.insertFootnote(FootnoteType.ENDNOTE, "Endnote 3.");

 // By default, the reference symbol for each footnote and endnote is its index
 // among all the document's footnotes/endnotes. Each document maintains separate counts
 // for footnotes and for endnotes, which both begin at 1.
 Assert.assertEquals(1, doc.getFootnoteOptions().getStartNumber());
 Assert.assertEquals(1, doc.getEndnoteOptions().getStartNumber());

 // We can use the "StartNumber" property to get the document to
 // begin a footnote or endnote count at a different number.
 doc.getEndnoteOptions().setNumberStyle(NumberStyle.ARABIC);
 doc.getEndnoteOptions().setStartNumber(50);

 doc.save(getArtifactsDir() + "InlineStory.StartNumber.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | int | İlgili  int  değeri. |

