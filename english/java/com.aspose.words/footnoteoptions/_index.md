---
title: FootnoteOptions
linktitle: FootnoteOptions
second_title: Aspose.Words for Java
description: Represents the footnote numbering options for a document or section in Java.
type: docs
weight: 320
url: /java/com.aspose.words/footnoteoptions/
---

**Inheritance:**
java.lang.Object
```
public class FootnoteOptions
```

Represents the footnote numbering options for a document or section.

To learn more, visit the [ Working with Footnote and Endnote ][Working with Footnote and Endnote] documentation article.

 **Examples:** 

Shows how to split the footnote section into a given number of columns.

```

 Document doc = new Document(getMyDir() + "Footnotes and endnotes.docx");
 doc.getFootnoteOptions().setColumns(2);
 doc.save(getArtifactsDir() + "Document.FootnoteColumns.docx");
 
```

Shows how to select a different place where the document collects and displays its footnotes.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // A footnote is a way to attach a reference or a side comment to text
 // that does not interfere with the main body text's flow.
 // Inserting a footnote adds a small superscript reference symbol
 // at the main body text where we insert the footnote.
 // Each footnote also creates an entry at the bottom of the page, consisting of a symbol
 // that matches the reference symbol in the main body text.
 // The reference text that we pass to the document builder's "InsertFootnote" method.
 builder.write("Hello world!");
 builder.insertFootnote(FootnoteType.FOOTNOTE, "Footnote contents.");

 // We can use the "Position" property to determine where the document will place all its footnotes.
 // If we set the value of the "Position" property to "FootnotePosition.BottomOfPage",
 // every footnote will show up at the bottom of the page that contains its reference mark. This is the default value.
 // If we set the value of the "Position" property to "FootnotePosition.BeneathText",
 // every footnote will show up at the end of the page's text that contains its reference mark.
 doc.getFootnoteOptions().setPosition(footnotePosition);

 doc.save(getArtifactsDir() + "InlineStory.PositionFootnote.docx");
 
```

Shows how to set a number at which the document begins the footnote/endnote count.

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

Shows how to change the number style of footnote/endnote reference marks.

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

Shows how to restart footnote/endnote numbering at certain places in the document.

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


[Working with Footnote and Endnote]: https://docs.aspose.com/words/java/working-with-footnote-and-endnote/
## Methods

| Method | Description |
| --- | --- |
| [getColumns()](#getColumns) | Specifies the number of columns with which the footnotes area is formatted. |
| [getLocation()](#getLocation) |  |
| [getNumberStyle()](#getNumberStyle) | Specifies the number format for automatically numbered footnotes. |
| [getPosition()](#getPosition) | Specifies the footnotes position. |
| [getRestartRule()](#getRestartRule) | Determines when automatic numbering restarts. |
| [getStartNumber()](#getStartNumber) | Specifies the starting number or character for the first automatically numbered footnotes. |
| [setColumns(int value)](#setColumns-int) | Specifies the number of columns with which the footnotes area is formatted. |
| [setLocation(int value)](#setLocation-int) |  |
| [setNumberStyle(int value)](#setNumberStyle-int) | Specifies the number format for automatically numbered footnotes. |
| [setPosition(int value)](#setPosition-int) | Specifies the footnotes position. |
| [setRestartRule(int value)](#setRestartRule-int) | Determines when automatic numbering restarts. |
| [setStartNumber(int value)](#setStartNumber-int) | Specifies the starting number or character for the first automatically numbered footnotes. |
### getColumns() {#getColumns}
```
public int getColumns()
```


Specifies the number of columns with which the footnotes area is formatted.

 **Remarks:** 

If this property has the value of 0, the footnotes area is formatted with a number of columns based on the number of columns on the displayed page. The default value is 0.

 **Examples:** 

Shows how to split the footnote section into a given number of columns.

```

 Document doc = new Document(getMyDir() + "Footnotes and endnotes.docx");
 doc.getFootnoteOptions().setColumns(2);
 doc.save(getArtifactsDir() + "Document.FootnoteColumns.docx");
 
```

**Returns:**
int - The corresponding  int  value.
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


Specifies the number format for automatically numbered footnotes.

 **Remarks:** 

Not all number styles are applicable for this property. For the list of applicable number styles see the Insert Footnote or Endnote dialog box in Microsoft Word. If you select a number style that is not applicable, Microsoft Word will revert to a default value.

 **Examples:** 

Shows how to change the number style of footnote/endnote reference marks.

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
int - The corresponding  int  value. The returned value is one of [NumberStyle](../../com.aspose.words/numberstyle/) constants.
### getPosition() {#getPosition}
```
public int getPosition()
```


Specifies the footnotes position.

 **Examples:** 

Shows how to select a different place where the document collects and displays its footnotes.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // A footnote is a way to attach a reference or a side comment to text
 // that does not interfere with the main body text's flow.
 // Inserting a footnote adds a small superscript reference symbol
 // at the main body text where we insert the footnote.
 // Each footnote also creates an entry at the bottom of the page, consisting of a symbol
 // that matches the reference symbol in the main body text.
 // The reference text that we pass to the document builder's "InsertFootnote" method.
 builder.write("Hello world!");
 builder.insertFootnote(FootnoteType.FOOTNOTE, "Footnote contents.");

 // We can use the "Position" property to determine where the document will place all its footnotes.
 // If we set the value of the "Position" property to "FootnotePosition.BottomOfPage",
 // every footnote will show up at the bottom of the page that contains its reference mark. This is the default value.
 // If we set the value of the "Position" property to "FootnotePosition.BeneathText",
 // every footnote will show up at the end of the page's text that contains its reference mark.
 doc.getFootnoteOptions().setPosition(footnotePosition);

 doc.save(getArtifactsDir() + "InlineStory.PositionFootnote.docx");
 
```

**Returns:**
int - The corresponding  int  value. The returned value is one of [FootnotePosition](../../com.aspose.words/footnoteposition/) constants.
### getRestartRule() {#getRestartRule}
```
public int getRestartRule()
```


Determines when automatic numbering restarts.

 **Examples:** 

Shows how to restart footnote/endnote numbering at certain places in the document.

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
int - The corresponding  int  value. The returned value is one of [FootnoteNumberingRule](../../com.aspose.words/footnotenumberingrule/) constants.
### getStartNumber() {#getStartNumber}
```
public int getStartNumber()
```


Specifies the starting number or character for the first automatically numbered footnotes.

 **Remarks:** 

This property has effect only when [getRestartRule()](../../com.aspose.words/footnoteoptions/\#getRestartRule) / [setRestartRule(int)](../../com.aspose.words/footnoteoptions/\#setRestartRule-int) is set to [FootnoteNumberingRule.CONTINUOUS](../../com.aspose.words/footnotenumberingrule/\#CONTINUOUS).

 **Examples:** 

Shows how to set a number at which the document begins the footnote/endnote count.

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
int - The corresponding  int  value.
### setColumns(int value) {#setColumns-int}
```
public void setColumns(int value)
```


Specifies the number of columns with which the footnotes area is formatted.

 **Remarks:** 

If this property has the value of 0, the footnotes area is formatted with a number of columns based on the number of columns on the displayed page. The default value is 0.

 **Examples:** 

Shows how to split the footnote section into a given number of columns.

```

 Document doc = new Document(getMyDir() + "Footnotes and endnotes.docx");
 doc.getFootnoteOptions().setColumns(2);
 doc.save(getArtifactsDir() + "Document.FootnoteColumns.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. |

### setLocation(int value) {#setLocation-int}
```
public void setLocation(int value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int |  |

### setNumberStyle(int value) {#setNumberStyle-int}
```
public void setNumberStyle(int value)
```


Specifies the number format for automatically numbered footnotes.

 **Remarks:** 

Not all number styles are applicable for this property. For the list of applicable number styles see the Insert Footnote or Endnote dialog box in Microsoft Word. If you select a number style that is not applicable, Microsoft Word will revert to a default value.

 **Examples:** 

Shows how to change the number style of footnote/endnote reference marks.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [NumberStyle](../../com.aspose.words/numberstyle/) constants. |

### setPosition(int value) {#setPosition-int}
```
public void setPosition(int value)
```


Specifies the footnotes position.

 **Examples:** 

Shows how to select a different place where the document collects and displays its footnotes.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // A footnote is a way to attach a reference or a side comment to text
 // that does not interfere with the main body text's flow.
 // Inserting a footnote adds a small superscript reference symbol
 // at the main body text where we insert the footnote.
 // Each footnote also creates an entry at the bottom of the page, consisting of a symbol
 // that matches the reference symbol in the main body text.
 // The reference text that we pass to the document builder's "InsertFootnote" method.
 builder.write("Hello world!");
 builder.insertFootnote(FootnoteType.FOOTNOTE, "Footnote contents.");

 // We can use the "Position" property to determine where the document will place all its footnotes.
 // If we set the value of the "Position" property to "FootnotePosition.BottomOfPage",
 // every footnote will show up at the bottom of the page that contains its reference mark. This is the default value.
 // If we set the value of the "Position" property to "FootnotePosition.BeneathText",
 // every footnote will show up at the end of the page's text that contains its reference mark.
 doc.getFootnoteOptions().setPosition(footnotePosition);

 doc.save(getArtifactsDir() + "InlineStory.PositionFootnote.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [FootnotePosition](../../com.aspose.words/footnoteposition/) constants. |

### setRestartRule(int value) {#setRestartRule-int}
```
public void setRestartRule(int value)
```


Determines when automatic numbering restarts.

 **Examples:** 

Shows how to restart footnote/endnote numbering at certain places in the document.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [FootnoteNumberingRule](../../com.aspose.words/footnotenumberingrule/) constants. |

### setStartNumber(int value) {#setStartNumber-int}
```
public void setStartNumber(int value)
```


Specifies the starting number or character for the first automatically numbered footnotes.

 **Remarks:** 

This property has effect only when [getRestartRule()](../../com.aspose.words/footnoteoptions/\#getRestartRule) / [setRestartRule(int)](../../com.aspose.words/footnoteoptions/\#setRestartRule-int) is set to [FootnoteNumberingRule.CONTINUOUS](../../com.aspose.words/footnotenumberingrule/\#CONTINUOUS).

 **Examples:** 

Shows how to set a number at which the document begins the footnote/endnote count.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. |

