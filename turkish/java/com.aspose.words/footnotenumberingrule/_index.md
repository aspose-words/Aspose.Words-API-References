---
title: "FootnoteNumberingRule"
linktitle: "FootnoteNumberingRule"
second_title: "Aspose.Words Java için"
description: "Java'da otomatik dipnot veya sonnot numaralandırmasının ne zaman yeniden başlayacağını belirler."
type: docs
weight: 340
url: /tr/java/com.aspose.words/footnotenumberingrule/
---

**Inheritance:**
java.lang.Object
```
public class FootnoteNumberingRule
```

Otomatik dipnot veya sonnot numaralandırmasının ne zaman yeniden başlayacağını belirler.

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
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [CONTINUOUS](#CONTINUOUS) | Numaralandırma belgenin tamamında süreklidir. |
| [DEFAULT](#DEFAULT) | Eşittir [CONTINUOUS](../../com.aspose.words/footnotenumberingrule/\#CONTINUOUS). |
| [RESTART_PAGE](#RESTART-PAGE) | Numaralandırma her sayfada yeniden başlar. |
| [RESTART_SECTION](#RESTART-SECTION) | Numaralandırma her bölümde yeniden başlar. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String footnoteNumberingRuleName)](#fromName-java.lang.String) |  |
| [getName(int footnoteNumberingRule)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int footnoteNumberingRule)](#toString-int) |  |
### CONTINUOUS {#CONTINUOUS}
```
public static int CONTINUOUS
```


Numaralandırma belgenin tamamında süreklidir.

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Eşittir [CONTINUOUS](../../com.aspose.words/footnotenumberingrule/\#CONTINUOUS).

### RESTART_PAGE {#RESTART-PAGE}
```
public static int RESTART_PAGE
```


Numaralandırma her sayfada yeniden başlar. Yalnızca dipnotlar için geçerlidir.

### RESTART_SECTION {#RESTART-SECTION}
```
public static int RESTART_SECTION
```


Numaralandırma her bölümde yeniden başlar.

### length {#length}
```
public static int length
```


### fromName(String footnoteNumberingRuleName) {#fromName-java.lang.String}
```
public static int fromName(String footnoteNumberingRuleName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| footnoteNumberingRuleName | java.lang.String |  |

**Returns:**
int
### getName(int footnoteNumberingRule) {#getName-int}
```
public static String getName(int footnoteNumberingRule)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| footnoteNumberingRule | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int footnoteNumberingRule) {#toString-int}
```
public static String toString(int footnoteNumberingRule)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| footnoteNumberingRule | int |  |

**Returns:**
java.lang.String
