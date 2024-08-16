---
title: ParagraphFormat
linktitle: ParagraphFormat
second_title: Aspose.Words for Java
description: Represents all the formatting for a paragraph in Java.
type: docs
weight: 490
url: /java/com.aspose.words/paragraphformat/
---

**Inheritance:**
java.lang.Object
```
public class ParagraphFormat
```

Represents all the formatting for a paragraph.

To learn more, visit the [ Working with Paragraphs ][Working with Paragraphs] documentation article.

 **Examples:** 

Shows how to construct an Aspose.Words document by hand.

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
## Methods

| Method | Description |
| --- | --- |
| [clearFormatting()](#clearFormatting) | Resets to default paragraph formatting. |
| [fetchInheritedBorderAttr(int key)](#fetchInheritedBorderAttr-int) |  |
| [fetchInheritedShadingAttr(int key)](#fetchInheritedShadingAttr-int) |  |
| [getAddSpaceBetweenFarEastAndAlpha()](#getAddSpaceBetweenFarEastAndAlpha) | Gets a flag indicating whether inter-character spacing is automatically adjusted between regions of Latin text and regions of East Asian text in the current paragraph. |
| [getAddSpaceBetweenFarEastAndDigit()](#getAddSpaceBetweenFarEastAndDigit) | Gets a flag indicating whether inter-character spacing is automatically adjusted between regions of numbers and regions of East Asian text in the current paragraph. |
| [getAlignment()](#getAlignment) | Gets text alignment for the paragraph. |
| [getBaselineAlignment()](#getBaselineAlignment) | Gets fonts vertical position on a line. |
| [getBidi()](#getBidi) | Gets whether this is a right-to-left paragraph. |
| [getBorders()](#getBorders) | Gets collection of borders of the paragraph. |
| [getCharacterUnitFirstLineIndent()](#getCharacterUnitFirstLineIndent) | Gets the value (in characters) for the first-line or hanging indent. |
| [getCharacterUnitLeftIndent()](#getCharacterUnitLeftIndent) | Gets the left indent value (in characters) for the specified paragraphs. |
| [getCharacterUnitRightIndent()](#getCharacterUnitRightIndent) | Gets the right indent value (in characters) for the specified paragraphs. |
| [getDirectBorderAttr(int key)](#getDirectBorderAttr-int) |  |
| [getDropCapPosition()](#getDropCapPosition) | Gets the position for a drop cap text. |
| [getFarEastLineBreakControl()](#getFarEastLineBreakControl) | Gets a flag indicating whether East Asian line-breaking rules are applied to the current paragraph. |
| [getFirstLineIndent()](#getFirstLineIndent) | Gets the value (in points) for a first line or hanging indent. |
| [getHangingPunctuation()](#getHangingPunctuation) | Gets a flag indicating whether hanging punctuation is enabled for the current paragraph. |
| [getKeepTogether()](#getKeepTogether) | True if all lines in the paragraph are to remain on the same page. |
| [getKeepWithNext()](#getKeepWithNext) | True if the paragraph is to remains on the same page as the paragraph that follows it. |
| [getLeftIndent()](#getLeftIndent) | Gets the value (in points) that represents the left indent for paragraph. |
| [getLineSpacing()](#getLineSpacing) | Gets the line spacing (in points) for the paragraph. |
| [getLineSpacingRule()](#getLineSpacingRule) | Gets the line spacing for the paragraph. |
| [getLineUnitAfter()](#getLineUnitAfter) | Gets the amount of spacing (in gridlines) after the paragraphs. |
| [getLineUnitBefore()](#getLineUnitBefore) | Gets the amount of spacing (in gridlines) before the paragraphs. |
| [getLinesToDrop()](#getLinesToDrop) | Gets the number of lines of the paragraph text used to calculate the drop cap height. |
| [getMirrorIndents()](#getMirrorIndents) | Gets a flag indicating whether the left and right indents are of the same width. |
| [getNoSpaceBetweenParagraphsOfSameStyle()](#getNoSpaceBetweenParagraphsOfSameStyle) | When  true , [getSpaceBefore()](../../com.aspose.words/paragraphformat/\#getSpaceBefore) / [setSpaceBefore(double)](../../com.aspose.words/paragraphformat/\#setSpaceBefore-double) and [getSpaceAfter()](../../com.aspose.words/paragraphformat/\#getSpaceAfter) / [setSpaceAfter(double)](../../com.aspose.words/paragraphformat/\#setSpaceAfter-double) will be ignored between the paragraphs of the same style. |
| [getOutlineLevel()](#getOutlineLevel) | Specifies the outline level of the paragraph in the document. |
| [getPageBreakBefore()](#getPageBreakBefore) | True if a page break is forced before the paragraph. |
| [getRightIndent()](#getRightIndent) | Gets the value (in points) that represents the right indent for paragraph. |
| [getShading()](#getShading) | Returns a [Shading](../../com.aspose.words/shading/) object that refers to the shading formatting for the paragraph. |
| [getSnapToGrid()](#getSnapToGrid) | Specifies whether the current paragraph should use the document grid lines per page settings when laying out the contents in the paragraph. |
| [getSpaceAfter()](#getSpaceAfter) | Gets the amount of spacing (in points) after the paragraph. |
| [getSpaceAfterAuto()](#getSpaceAfterAuto) | True if the amount of spacing after the paragraph is set automatically. |
| [getSpaceBefore()](#getSpaceBefore) | Gets the amount of spacing (in points) before the paragraph. |
| [getSpaceBeforeAuto()](#getSpaceBeforeAuto) | True if the amount of spacing before the paragraph is set automatically. |
| [getStyle()](#getStyle) | Gets the paragraph style applied to this formatting. |
| [getStyleIdentifier()](#getStyleIdentifier) | Gets the locale independent style identifier of the paragraph style applied to this formatting. |
| [getStyleName()](#getStyleName) | Gets the name of the paragraph style applied to this formatting. |
| [getSuppressAutoHyphens()](#getSuppressAutoHyphens) | Specifies whether the current paragraph should be exempted from any hyphenation which is applied in the document settings. |
| [getSuppressLineNumbers()](#getSuppressLineNumbers) | Specifies whether the current paragraph's lines should be exempted from line numbering which is applied in the parent section. |
| [getTabStops()](#getTabStops) | Gets the collection of custom tab stops defined for this object. |
| [getWidowControl()](#getWidowControl) | True if the first and last lines in the paragraph are to remain on the same page as the rest of the paragraph. |
| [getWordWrap()](#getWordWrap) | If this property is  false , Latin text in the middle of a word can be wrapped for the current paragraph. |
| [isHeading()](#isHeading) | True when the paragraph style is one of the built-in Heading styles. |
| [isListItem()](#isListItem) | True when the paragraph is an item in a bulleted or numbered list. |
| [setAddSpaceBetweenFarEastAndAlpha(boolean value)](#setAddSpaceBetweenFarEastAndAlpha-boolean) | Sets a flag indicating whether inter-character spacing is automatically adjusted between regions of Latin text and regions of East Asian text in the current paragraph. |
| [setAddSpaceBetweenFarEastAndDigit(boolean value)](#setAddSpaceBetweenFarEastAndDigit-boolean) | Sets a flag indicating whether inter-character spacing is automatically adjusted between regions of numbers and regions of East Asian text in the current paragraph. |
| [setAlignment(int value)](#setAlignment-int) | Sets text alignment for the paragraph. |
| [setBaselineAlignment(int value)](#setBaselineAlignment-int) | Sets fonts vertical position on a line. |
| [setBidi(boolean value)](#setBidi-boolean) | Sets whether this is a right-to-left paragraph. |
| [setBorderAttr(int key, Object value)](#setBorderAttr-int-java.lang.Object) |  |
| [setCharacterUnitFirstLineIndent(double value)](#setCharacterUnitFirstLineIndent-double) | Sets the value (in characters) for the first-line or hanging indent. |
| [setCharacterUnitLeftIndent(double value)](#setCharacterUnitLeftIndent-double) | Sets the left indent value (in characters) for the specified paragraphs. |
| [setCharacterUnitRightIndent(double value)](#setCharacterUnitRightIndent-double) | Sets the right indent value (in characters) for the specified paragraphs. |
| [setDropCapPosition(int value)](#setDropCapPosition-int) | Sets the position for a drop cap text. |
| [setFarEastLineBreakControl(boolean value)](#setFarEastLineBreakControl-boolean) | Sets a flag indicating whether East Asian line-breaking rules are applied to the current paragraph. |
| [setFirstLineIndent(double value)](#setFirstLineIndent-double) | Sets the value (in points) for a first line or hanging indent. |
| [setHangingPunctuation(boolean value)](#setHangingPunctuation-boolean) | Sets a flag indicating whether hanging punctuation is enabled for the current paragraph. |
| [setKeepTogether(boolean value)](#setKeepTogether-boolean) | True if all lines in the paragraph are to remain on the same page. |
| [setKeepWithNext(boolean value)](#setKeepWithNext-boolean) | True if the paragraph is to remains on the same page as the paragraph that follows it. |
| [setLeftIndent(double value)](#setLeftIndent-double) | Sets the value (in points) that represents the left indent for paragraph. |
| [setLineSpacing(double value)](#setLineSpacing-double) | Sets the line spacing (in points) for the paragraph. |
| [setLineSpacingRule(int value)](#setLineSpacingRule-int) | Sets the line spacing for the paragraph. |
| [setLineUnitAfter(double value)](#setLineUnitAfter-double) | Sets the amount of spacing (in gridlines) after the paragraphs. |
| [setLineUnitBefore(double value)](#setLineUnitBefore-double) | Sets the amount of spacing (in gridlines) before the paragraphs. |
| [setLinesToDrop(int value)](#setLinesToDrop-int) | Sets the number of lines of the paragraph text used to calculate the drop cap height. |
| [setMirrorIndents(boolean value)](#setMirrorIndents-boolean) | Sets a flag indicating whether the left and right indents are of the same width. |
| [setNoSpaceBetweenParagraphsOfSameStyle(boolean value)](#setNoSpaceBetweenParagraphsOfSameStyle-boolean) | When  true , [getSpaceBefore()](../../com.aspose.words/paragraphformat/\#getSpaceBefore) / [setSpaceBefore(double)](../../com.aspose.words/paragraphformat/\#setSpaceBefore-double) and [getSpaceAfter()](../../com.aspose.words/paragraphformat/\#getSpaceAfter) / [setSpaceAfter(double)](../../com.aspose.words/paragraphformat/\#setSpaceAfter-double) will be ignored between the paragraphs of the same style. |
| [setOutlineLevel(int value)](#setOutlineLevel-int) | Specifies the outline level of the paragraph in the document. |
| [setPageBreakBefore(boolean value)](#setPageBreakBefore-boolean) | True if a page break is forced before the paragraph. |
| [setRightIndent(double value)](#setRightIndent-double) | Sets the value (in points) that represents the right indent for paragraph. |
| [setSnapToGrid(boolean value)](#setSnapToGrid-boolean) | Specifies whether the current paragraph should use the document grid lines per page settings when laying out the contents in the paragraph. |
| [setSpaceAfter(double value)](#setSpaceAfter-double) | Sets the amount of spacing (in points) after the paragraph. |
| [setSpaceAfterAuto(boolean value)](#setSpaceAfterAuto-boolean) | True if the amount of spacing after the paragraph is set automatically. |
| [setSpaceBefore(double value)](#setSpaceBefore-double) | Sets the amount of spacing (in points) before the paragraph. |
| [setSpaceBeforeAuto(boolean value)](#setSpaceBeforeAuto-boolean) | True if the amount of spacing before the paragraph is set automatically. |
| [setStyle(Style value)](#setStyle-com.aspose.words.Style) | Sets the paragraph style applied to this formatting. |
| [setStyleIdentifier(int value)](#setStyleIdentifier-int) | Sets the locale independent style identifier of the paragraph style applied to this formatting. |
| [setStyleName(String value)](#setStyleName-java.lang.String) | Sets the name of the paragraph style applied to this formatting. |
| [setSuppressAutoHyphens(boolean value)](#setSuppressAutoHyphens-boolean) | Specifies whether the current paragraph should be exempted from any hyphenation which is applied in the document settings. |
| [setSuppressLineNumbers(boolean value)](#setSuppressLineNumbers-boolean) | Specifies whether the current paragraph's lines should be exempted from line numbering which is applied in the parent section. |
| [setWidowControl(boolean value)](#setWidowControl-boolean) | True if the first and last lines in the paragraph are to remain on the same page as the rest of the paragraph. |
| [setWordWrap(boolean value)](#setWordWrap-boolean) | If this property is  false , Latin text in the middle of a word can be wrapped for the current paragraph. |
### clearFormatting() {#clearFormatting}
```
public void clearFormatting()
```


Resets to default paragraph formatting.

 **Remarks:** 

Default paragraph formatting is Normal style, left aligned, no indentation, no spacing, no borders and no shading.

 **Examples:** 

Shows how to nest a list inside another list.

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
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### fetchInheritedShadingAttr(int key) {#fetchInheritedShadingAttr-int}
```
public Object fetchInheritedShadingAttr(int key)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### getAddSpaceBetweenFarEastAndAlpha() {#getAddSpaceBetweenFarEastAndAlpha}
```
public boolean getAddSpaceBetweenFarEastAndAlpha()
```


Gets a flag indicating whether inter-character spacing is automatically adjusted between regions of Latin text and regions of East Asian text in the current paragraph.

 **Examples:** 

Shows how to insert a paragraph into the document.

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
boolean - A flag indicating whether inter-character spacing is automatically adjusted between regions of Latin text and regions of East Asian text in the current paragraph.
### getAddSpaceBetweenFarEastAndDigit() {#getAddSpaceBetweenFarEastAndDigit}
```
public boolean getAddSpaceBetweenFarEastAndDigit()
```


Gets a flag indicating whether inter-character spacing is automatically adjusted between regions of numbers and regions of East Asian text in the current paragraph.

 **Examples:** 

Shows how to insert a paragraph into the document.

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
boolean - A flag indicating whether inter-character spacing is automatically adjusted between regions of numbers and regions of East Asian text in the current paragraph.
### getAlignment() {#getAlignment}
```
public int getAlignment()
```


Gets text alignment for the paragraph.

 **Examples:** 

Shows how to insert a paragraph into the document.

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

Shows how to construct an Aspose.Words document by hand.

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
int - Text alignment for the paragraph. The returned value is one of [ParagraphAlignment](../../com.aspose.words/paragraphalignment/) constants.
### getBaselineAlignment() {#getBaselineAlignment}
```
public int getBaselineAlignment()
```


Gets fonts vertical position on a line.

 **Examples:** 

Shows how to set fonts vertical position on a line.

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
int - Fonts vertical position on a line. The returned value is one of [BaselineAlignment](../../com.aspose.words/baselinealignment/) constants.
### getBidi() {#getBidi}
```
public boolean getBidi()
```


Gets whether this is a right-to-left paragraph.

 **Remarks:** 

When  true , the runs and other inline objects in this paragraph are laid out right to left.

 **Examples:** 

Shows how to detect plaintext document text direction.

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

Shows how to create right-to-left language-compatible lists with BIDIOUTLINE fields.

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

**Returns:**
boolean - Whether this is a right-to-left paragraph.
### getBorders() {#getBorders}
```
public BorderCollection getBorders()
```


Gets collection of borders of the paragraph.

 **Examples:** 

Shows how to insert a paragraph with a top border.

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


Gets the value (in characters) for the first-line or hanging indent.

Use positive values to set the first-line indent, and negative values to set the hanging indent.

 **Examples:** 

Shows how to change paragraph spacing and indents.

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
double - The value (in characters) for the first-line or hanging indent.
### getCharacterUnitLeftIndent() {#getCharacterUnitLeftIndent}
```
public double getCharacterUnitLeftIndent()
```


Gets the left indent value (in characters) for the specified paragraphs.

 **Examples:** 

Shows how to change paragraph spacing and indents.

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
double - The left indent value (in characters) for the specified paragraphs.
### getCharacterUnitRightIndent() {#getCharacterUnitRightIndent}
```
public double getCharacterUnitRightIndent()
```


Gets the right indent value (in characters) for the specified paragraphs.

 **Examples:** 

Shows how to change paragraph spacing and indents.

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
double - The right indent value (in characters) for the specified paragraphs.
### getDirectBorderAttr(int key) {#getDirectBorderAttr-int}
```
public Object getDirectBorderAttr(int key)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### getDropCapPosition() {#getDropCapPosition}
```
public int getDropCapPosition()
```


Gets the position for a drop cap text.

 **Examples:** 

Shows how to nest a list inside another list.

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
int - The position for a drop cap text. The returned value is one of [DropCapPosition](../../com.aspose.words/dropcapposition/) constants.
### getFarEastLineBreakControl() {#getFarEastLineBreakControl}
```
public boolean getFarEastLineBreakControl()
```


Gets a flag indicating whether East Asian line-breaking rules are applied to the current paragraph.

 **Examples:** 

Shows how to set special properties for Asian typography.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 ParagraphFormat format = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat();
 format.setFarEastLineBreakControl(true);
 format.setWordWrap(false);
 format.setHangingPunctuation(true);

 doc.save(getArtifactsDir() + "ParagraphFormat.AsianTypographyProperties.docx");
 
```

**Returns:**
boolean - A flag indicating whether East Asian line-breaking rules are applied to the current paragraph.
### getFirstLineIndent() {#getFirstLineIndent}
```
public double getFirstLineIndent()
```


Gets the value (in points) for a first line or hanging indent.

Use positive values to set the first-line indent, and negative values to set the hanging indent.

 **Examples:** 

Shows how to insert a paragraph into the document.

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
double - The value (in points) for a first line or hanging indent.
### getHangingPunctuation() {#getHangingPunctuation}
```
public boolean getHangingPunctuation()
```


Gets a flag indicating whether hanging punctuation is enabled for the current paragraph.

 **Examples:** 

Shows how to set special properties for Asian typography.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 ParagraphFormat format = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat();
 format.setFarEastLineBreakControl(true);
 format.setWordWrap(false);
 format.setHangingPunctuation(true);

 doc.save(getArtifactsDir() + "ParagraphFormat.AsianTypographyProperties.docx");
 
```

**Returns:**
boolean - A flag indicating whether hanging punctuation is enabled for the current paragraph.
### getKeepTogether() {#getKeepTogether}
```
public boolean getKeepTogether()
```


True if all lines in the paragraph are to remain on the same page.

 **Examples:** 

Shows how to insert a paragraph into the document.

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
boolean - The corresponding  boolean  value.
### getKeepWithNext() {#getKeepWithNext}
```
public boolean getKeepWithNext()
```


True if the paragraph is to remains on the same page as the paragraph that follows it.

 **Examples:** 

Shows how to set a table to stay together on the same page.

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
boolean - The corresponding  boolean  value.
### getLeftIndent() {#getLeftIndent}
```
public double getLeftIndent()
```


Gets the value (in points) that represents the left indent for paragraph.

 **Examples:** 

Shows how to configure paragraph formatting to create off-center text.

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
double - The value (in points) that represents the left indent for paragraph.
### getLineSpacing() {#getLineSpacing}
```
public double getLineSpacing()
```


Gets the line spacing (in points) for the paragraph.

 **Remarks:** 

When [getLineSpacingRule()](../../com.aspose.words/paragraphformat/\#getLineSpacingRule) / [setLineSpacingRule(int)](../../com.aspose.words/paragraphformat/\#setLineSpacingRule-int) property is set to [LineSpacingRule.AT\_LEAST](../../com.aspose.words/linespacingrule/\#AT-LEAST), the line spacing can be greater than or equal to, but never less than the specified [getLineSpacing()](../../com.aspose.words/paragraphformat/\#getLineSpacing) / [setLineSpacing(double)](../../com.aspose.words/paragraphformat/\#setLineSpacing-double) value.

When [getLineSpacingRule()](../../com.aspose.words/paragraphformat/\#getLineSpacingRule) / [setLineSpacingRule(int)](../../com.aspose.words/paragraphformat/\#setLineSpacingRule-int) property is set to [LineSpacingRule.EXACTLY](../../com.aspose.words/linespacingrule/\#EXACTLY), the line spacing never changes from the specified [getLineSpacing()](../../com.aspose.words/paragraphformat/\#getLineSpacing) / [setLineSpacing(double)](../../com.aspose.words/paragraphformat/\#setLineSpacing-double) value, even if a larger font is used within the paragraph.

 **Examples:** 

Shows how to work with line spacing.

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
double - The line spacing (in points) for the paragraph.
### getLineSpacingRule() {#getLineSpacingRule}
```
public int getLineSpacingRule()
```


Gets the line spacing for the paragraph.

 **Examples:** 

Shows how to work with line spacing.

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
int - The line spacing for the paragraph. The returned value is one of [LineSpacingRule](../../com.aspose.words/linespacingrule/) constants.
### getLineUnitAfter() {#getLineUnitAfter}
```
public double getLineUnitAfter()
```


Gets the amount of spacing (in gridlines) after the paragraphs.

 **Examples:** 

Shows how to change paragraph spacing and indents.

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
double - The amount of spacing (in gridlines) after the paragraphs.
### getLineUnitBefore() {#getLineUnitBefore}
```
public double getLineUnitBefore()
```


Gets the amount of spacing (in gridlines) before the paragraphs.

 **Examples:** 

Shows how to change paragraph spacing and indents.

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
double - The amount of spacing (in gridlines) before the paragraphs.
### getLinesToDrop() {#getLinesToDrop}
```
public int getLinesToDrop()
```


Gets the number of lines of the paragraph text used to calculate the drop cap height.

 **Examples:** 

Shows how to set the size of a drop cap.

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
int - The number of lines of the paragraph text used to calculate the drop cap height.
### getMirrorIndents() {#getMirrorIndents}
```
public boolean getMirrorIndents()
```


Gets a flag indicating whether the left and right indents are of the same width.

 **Examples:** 

Show how to make left and right indents the same.

```

 Document doc = new Document(getMyDir() + "Document.docx");
 ParagraphFormat format = doc.getFirstSection().getBody().getParagraphs().get(0).getParagraphFormat();

 format.setMirrorIndents(true);

 doc.save(getArtifactsDir() + "ParagraphFormat.MirrorIndents.docx");
 
```

**Returns:**
boolean - A flag indicating whether the left and right indents are of the same width.
### getNoSpaceBetweenParagraphsOfSameStyle() {#getNoSpaceBetweenParagraphsOfSameStyle}
```
public boolean getNoSpaceBetweenParagraphsOfSameStyle()
```


When  true , [getSpaceBefore()](../../com.aspose.words/paragraphformat/\#getSpaceBefore) / [setSpaceBefore(double)](../../com.aspose.words/paragraphformat/\#setSpaceBefore-double) and [getSpaceAfter()](../../com.aspose.words/paragraphformat/\#getSpaceAfter) / [setSpaceAfter(double)](../../com.aspose.words/paragraphformat/\#setSpaceAfter-double) will be ignored between the paragraphs of the same style.

 **Remarks:** 

This setting only takes affect when applied to a paragraph style. If applied to a paragraph directly, it has no effect.

 **Examples:** 

Shows how to apply no spacing between paragraphs with the same style.

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
boolean - The corresponding  boolean  value.
### getOutlineLevel() {#getOutlineLevel}
```
public int getOutlineLevel()
```


Specifies the outline level of the paragraph in the document.

 **Examples:** 

Shows how to configure paragraph outline levels to create collapsible text.

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
int - The corresponding  int  value. The returned value is one of [OutlineLevel](../../com.aspose.words/outlinelevel/) constants.
### getPageBreakBefore() {#getPageBreakBefore}
```
public boolean getPageBreakBefore()
```


True if a page break is forced before the paragraph.

 **Examples:** 

Shows how to create paragraphs with page breaks at the beginning.

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
boolean - The corresponding  boolean  value.
### getRightIndent() {#getRightIndent}
```
public double getRightIndent()
```


Gets the value (in points) that represents the right indent for paragraph.

 **Examples:** 

Shows how to configure paragraph formatting to create off-center text.

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
double - The value (in points) that represents the right indent for paragraph.
### getShading() {#getShading}
```
public Shading getShading()
```


Returns a [Shading](../../com.aspose.words/shading/) object that refers to the shading formatting for the paragraph.

 **Examples:** 

Shows how to decorate text with borders and shading.

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


Specifies whether the current paragraph should use the document grid lines per page settings when laying out the contents in the paragraph.

 **Examples:** 

Shows how to specify a limit for the number of lines that each page may have.

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
boolean - The corresponding  boolean  value.
### getSpaceAfter() {#getSpaceAfter}
```
public double getSpaceAfter()
```


Gets the amount of spacing (in points) after the paragraph.

**Returns:**
double - The amount of spacing (in points) after the paragraph.
### getSpaceAfterAuto() {#getSpaceAfterAuto}
```
public boolean getSpaceAfterAuto()
```


True if the amount of spacing after the paragraph is set automatically.

 **Remarks:** 

When set to  true , overrides the effect of [getSpaceAfter()](../../com.aspose.words/paragraphformat/\#getSpaceAfter) / [setSpaceAfter(double)](../../com.aspose.words/paragraphformat/\#setSpaceAfter-double).

When you set paragraph Space Before and Space After to Auto, Microsoft Word adds 14 points spacing between paragraphs automatically according to the following rules:

 *  Normally, spacing is added after all paragraphs.
 *  In a bulleted or numbered list, spacing is added only after the last item in the list. Spacing is not added between the list items.
 *  In a nested bulleted or numbered list spacing is not added.
 *  Spacing is normally added after a table.
 *  Spacing is not added after a table if it is the last block in a table cell.
 *  Spacing is not added after the last paragraph in a table cell.

 **Examples:** 

Shows how to set automatic paragraph spacing.

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
boolean - The corresponding  boolean  value.
### getSpaceBefore() {#getSpaceBefore}
```
public double getSpaceBefore()
```


Gets the amount of spacing (in points) before the paragraph.

**Returns:**
double - The amount of spacing (in points) before the paragraph.
### getSpaceBeforeAuto() {#getSpaceBeforeAuto}
```
public boolean getSpaceBeforeAuto()
```


True if the amount of spacing before the paragraph is set automatically.

 **Remarks:** 

When set to  true , overrides the effect of [getSpaceBefore()](../../com.aspose.words/paragraphformat/\#getSpaceBefore) / [setSpaceBefore(double)](../../com.aspose.words/paragraphformat/\#setSpaceBefore-double).

When you set paragraph Space Before and Space After to Auto, Microsoft Word adds 14 points spacing between paragraphs automatically according to the following rules:

 *  Normally, spacing is added after all paragraphs.
 *  In a bulleted or numbered list, spacing is added only after the last item in the list. Spacing is not added between the list items.
 *  In a nested bulleted or numbered list spacing is not added.
 *  Spacing is normally added after a table.
 *  Spacing is not added after a table if it is the last block in a table cell.
 *  Spacing is not added after the last paragraph in a table cell.

 **Examples:** 

Shows how to set automatic paragraph spacing.

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
boolean - The corresponding  boolean  value.
### getStyle() {#getStyle}
```
public Style getStyle()
```


Gets the paragraph style applied to this formatting.

 **Examples:** 

Shows how to create and use a paragraph style with list formatting.

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


Gets the locale independent style identifier of the paragraph style applied to this formatting.

 **Examples:** 

Shows how to insert a Table of contents (TOC) into a document using heading styles as entries.

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
int - The locale independent style identifier of the paragraph style applied to this formatting. The returned value is one of [StyleIdentifier](../../com.aspose.words/styleidentifier/) constants.
### getStyleName() {#getStyleName}
```
public String getStyleName()
```


Gets the name of the paragraph style applied to this formatting.

 **Examples:** 

Shows how to construct an Aspose.Words document by hand.

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
java.lang.String - The name of the paragraph style applied to this formatting.
### getSuppressAutoHyphens() {#getSuppressAutoHyphens}
```
public boolean getSuppressAutoHyphens()
```


Specifies whether the current paragraph should be exempted from any hyphenation which is applied in the document settings.

 **Examples:** 

Shows how to suppress hyphenation for a paragraph.

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
boolean - The corresponding  boolean  value.
### getSuppressLineNumbers() {#getSuppressLineNumbers}
```
public boolean getSuppressLineNumbers()
```


Specifies whether the current paragraph's lines should be exempted from line numbering which is applied in the parent section.

 **Examples:** 

Shows how to enable line numbering for a section.

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
boolean - The corresponding  boolean  value.
### getTabStops() {#getTabStops}
```
public TabStopCollection getTabStops()
```


Gets the collection of custom tab stops defined for this object.

 **Examples:** 

Shows how to modify the position of the right tab stop in TOC related paragraphs.

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


True if the first and last lines in the paragraph are to remain on the same page as the rest of the paragraph.

 **Examples:** 

Shows how to enable widow/orphan control for a paragraph.

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
boolean - The corresponding  boolean  value.
### getWordWrap() {#getWordWrap}
```
public boolean getWordWrap()
```


If this property is  false , Latin text in the middle of a word can be wrapped for the current paragraph. Otherwise Latin text is wrapped by whole words.

 **Examples:** 

Shows how to set special properties for Asian typography.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 ParagraphFormat format = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat();
 format.setFarEastLineBreakControl(true);
 format.setWordWrap(false);
 format.setHangingPunctuation(true);

 doc.save(getArtifactsDir() + "ParagraphFormat.AsianTypographyProperties.docx");
 
```

**Returns:**
boolean - The corresponding  boolean  value.
### isHeading() {#isHeading}
```
public boolean isHeading()
```


True when the paragraph style is one of the built-in Heading styles.

 **Examples:** 

Shows how to limit the headings' level that will appear in the outline of a saved PDF document.

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
boolean - The corresponding  boolean  value.
### isListItem() {#isListItem}
```
public boolean isListItem()
```


True when the paragraph is an item in a bulleted or numbered list.

 **Examples:** 

Shows how to nest a list inside another list.

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
boolean - The corresponding  boolean  value.
### setAddSpaceBetweenFarEastAndAlpha(boolean value) {#setAddSpaceBetweenFarEastAndAlpha-boolean}
```
public void setAddSpaceBetweenFarEastAndAlpha(boolean value)
```


Sets a flag indicating whether inter-character spacing is automatically adjusted between regions of Latin text and regions of East Asian text in the current paragraph.

 **Examples:** 

Shows how to insert a paragraph into the document.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A flag indicating whether inter-character spacing is automatically adjusted between regions of Latin text and regions of East Asian text in the current paragraph. |

### setAddSpaceBetweenFarEastAndDigit(boolean value) {#setAddSpaceBetweenFarEastAndDigit-boolean}
```
public void setAddSpaceBetweenFarEastAndDigit(boolean value)
```


Sets a flag indicating whether inter-character spacing is automatically adjusted between regions of numbers and regions of East Asian text in the current paragraph.

 **Examples:** 

Shows how to insert a paragraph into the document.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A flag indicating whether inter-character spacing is automatically adjusted between regions of numbers and regions of East Asian text in the current paragraph. |

### setAlignment(int value) {#setAlignment-int}
```
public void setAlignment(int value)
```


Sets text alignment for the paragraph.

 **Examples:** 

Shows how to insert a paragraph into the document.

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

Shows how to construct an Aspose.Words document by hand.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | Text alignment for the paragraph. The value must be one of [ParagraphAlignment](../../com.aspose.words/paragraphalignment/) constants. |

### setBaselineAlignment(int value) {#setBaselineAlignment-int}
```
public void setBaselineAlignment(int value)
```


Sets fonts vertical position on a line.

 **Examples:** 

Shows how to set fonts vertical position on a line.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | Fonts vertical position on a line. The value must be one of [BaselineAlignment](../../com.aspose.words/baselinealignment/) constants. |

### setBidi(boolean value) {#setBidi-boolean}
```
public void setBidi(boolean value)
```


Sets whether this is a right-to-left paragraph.

 **Remarks:** 

When  true , the runs and other inline objects in this paragraph are laid out right to left.

 **Examples:** 

Shows how to detect plaintext document text direction.

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

Shows how to create right-to-left language-compatible lists with BIDIOUTLINE fields.

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

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | Whether this is a right-to-left paragraph. |

### setBorderAttr(int key, Object value) {#setBorderAttr-int-java.lang.Object}
```
public void setBorderAttr(int key, Object value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |
| value | java.lang.Object |  |

### setCharacterUnitFirstLineIndent(double value) {#setCharacterUnitFirstLineIndent-double}
```
public void setCharacterUnitFirstLineIndent(double value)
```


Sets the value (in characters) for the first-line or hanging indent.

Use positive values to set the first-line indent, and negative values to set the hanging indent.

 **Examples:** 

Shows how to change paragraph spacing and indents.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The value (in characters) for the first-line or hanging indent. |

### setCharacterUnitLeftIndent(double value) {#setCharacterUnitLeftIndent-double}
```
public void setCharacterUnitLeftIndent(double value)
```


Sets the left indent value (in characters) for the specified paragraphs.

 **Examples:** 

Shows how to change paragraph spacing and indents.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The left indent value (in characters) for the specified paragraphs. |

### setCharacterUnitRightIndent(double value) {#setCharacterUnitRightIndent-double}
```
public void setCharacterUnitRightIndent(double value)
```


Sets the right indent value (in characters) for the specified paragraphs.

 **Examples:** 

Shows how to change paragraph spacing and indents.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The right indent value (in characters) for the specified paragraphs. |

### setDropCapPosition(int value) {#setDropCapPosition-int}
```
public void setDropCapPosition(int value)
```


Sets the position for a drop cap text.

 **Examples:** 

Shows how to nest a list inside another list.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The position for a drop cap text. The value must be one of [DropCapPosition](../../com.aspose.words/dropcapposition/) constants. |

### setFarEastLineBreakControl(boolean value) {#setFarEastLineBreakControl-boolean}
```
public void setFarEastLineBreakControl(boolean value)
```


Sets a flag indicating whether East Asian line-breaking rules are applied to the current paragraph.

 **Examples:** 

Shows how to set special properties for Asian typography.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 ParagraphFormat format = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat();
 format.setFarEastLineBreakControl(true);
 format.setWordWrap(false);
 format.setHangingPunctuation(true);

 doc.save(getArtifactsDir() + "ParagraphFormat.AsianTypographyProperties.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A flag indicating whether East Asian line-breaking rules are applied to the current paragraph. |

### setFirstLineIndent(double value) {#setFirstLineIndent-double}
```
public void setFirstLineIndent(double value)
```


Sets the value (in points) for a first line or hanging indent.

Use positive values to set the first-line indent, and negative values to set the hanging indent.

 **Examples:** 

Shows how to insert a paragraph into the document.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The value (in points) for a first line or hanging indent. |

### setHangingPunctuation(boolean value) {#setHangingPunctuation-boolean}
```
public void setHangingPunctuation(boolean value)
```


Sets a flag indicating whether hanging punctuation is enabled for the current paragraph.

 **Examples:** 

Shows how to set special properties for Asian typography.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 ParagraphFormat format = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat();
 format.setFarEastLineBreakControl(true);
 format.setWordWrap(false);
 format.setHangingPunctuation(true);

 doc.save(getArtifactsDir() + "ParagraphFormat.AsianTypographyProperties.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A flag indicating whether hanging punctuation is enabled for the current paragraph. |

### setKeepTogether(boolean value) {#setKeepTogether-boolean}
```
public void setKeepTogether(boolean value)
```


True if all lines in the paragraph are to remain on the same page.

 **Examples:** 

Shows how to insert a paragraph into the document.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setKeepWithNext(boolean value) {#setKeepWithNext-boolean}
```
public void setKeepWithNext(boolean value)
```


True if the paragraph is to remains on the same page as the paragraph that follows it.

 **Examples:** 

Shows how to set a table to stay together on the same page.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setLeftIndent(double value) {#setLeftIndent-double}
```
public void setLeftIndent(double value)
```


Sets the value (in points) that represents the left indent for paragraph.

 **Examples:** 

Shows how to configure paragraph formatting to create off-center text.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The value (in points) that represents the left indent for paragraph. |

### setLineSpacing(double value) {#setLineSpacing-double}
```
public void setLineSpacing(double value)
```


Sets the line spacing (in points) for the paragraph.

 **Remarks:** 

When [getLineSpacingRule()](../../com.aspose.words/paragraphformat/\#getLineSpacingRule) / [setLineSpacingRule(int)](../../com.aspose.words/paragraphformat/\#setLineSpacingRule-int) property is set to [LineSpacingRule.AT\_LEAST](../../com.aspose.words/linespacingrule/\#AT-LEAST), the line spacing can be greater than or equal to, but never less than the specified [getLineSpacing()](../../com.aspose.words/paragraphformat/\#getLineSpacing) / [setLineSpacing(double)](../../com.aspose.words/paragraphformat/\#setLineSpacing-double) value.

When [getLineSpacingRule()](../../com.aspose.words/paragraphformat/\#getLineSpacingRule) / [setLineSpacingRule(int)](../../com.aspose.words/paragraphformat/\#setLineSpacingRule-int) property is set to [LineSpacingRule.EXACTLY](../../com.aspose.words/linespacingrule/\#EXACTLY), the line spacing never changes from the specified [getLineSpacing()](../../com.aspose.words/paragraphformat/\#getLineSpacing) / [setLineSpacing(double)](../../com.aspose.words/paragraphformat/\#setLineSpacing-double) value, even if a larger font is used within the paragraph.

 **Examples:** 

Shows how to work with line spacing.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The line spacing (in points) for the paragraph. |

### setLineSpacingRule(int value) {#setLineSpacingRule-int}
```
public void setLineSpacingRule(int value)
```


Sets the line spacing for the paragraph.

 **Examples:** 

Shows how to work with line spacing.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The line spacing for the paragraph. The value must be one of [LineSpacingRule](../../com.aspose.words/linespacingrule/) constants. |

### setLineUnitAfter(double value) {#setLineUnitAfter-double}
```
public void setLineUnitAfter(double value)
```


Sets the amount of spacing (in gridlines) after the paragraphs.

 **Examples:** 

Shows how to change paragraph spacing and indents.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The amount of spacing (in gridlines) after the paragraphs. |

### setLineUnitBefore(double value) {#setLineUnitBefore-double}
```
public void setLineUnitBefore(double value)
```


Sets the amount of spacing (in gridlines) before the paragraphs.

 **Examples:** 

Shows how to change paragraph spacing and indents.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The amount of spacing (in gridlines) before the paragraphs. |

### setLinesToDrop(int value) {#setLinesToDrop-int}
```
public void setLinesToDrop(int value)
```


Sets the number of lines of the paragraph text used to calculate the drop cap height.

 **Examples:** 

Shows how to set the size of a drop cap.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The number of lines of the paragraph text used to calculate the drop cap height. |

### setMirrorIndents(boolean value) {#setMirrorIndents-boolean}
```
public void setMirrorIndents(boolean value)
```


Sets a flag indicating whether the left and right indents are of the same width.

 **Examples:** 

Show how to make left and right indents the same.

```

 Document doc = new Document(getMyDir() + "Document.docx");
 ParagraphFormat format = doc.getFirstSection().getBody().getParagraphs().get(0).getParagraphFormat();

 format.setMirrorIndents(true);

 doc.save(getArtifactsDir() + "ParagraphFormat.MirrorIndents.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A flag indicating whether the left and right indents are of the same width. |

### setNoSpaceBetweenParagraphsOfSameStyle(boolean value) {#setNoSpaceBetweenParagraphsOfSameStyle-boolean}
```
public void setNoSpaceBetweenParagraphsOfSameStyle(boolean value)
```


When  true , [getSpaceBefore()](../../com.aspose.words/paragraphformat/\#getSpaceBefore) / [setSpaceBefore(double)](../../com.aspose.words/paragraphformat/\#setSpaceBefore-double) and [getSpaceAfter()](../../com.aspose.words/paragraphformat/\#getSpaceAfter) / [setSpaceAfter(double)](../../com.aspose.words/paragraphformat/\#setSpaceAfter-double) will be ignored between the paragraphs of the same style.

 **Remarks:** 

This setting only takes affect when applied to a paragraph style. If applied to a paragraph directly, it has no effect.

 **Examples:** 

Shows how to apply no spacing between paragraphs with the same style.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setOutlineLevel(int value) {#setOutlineLevel-int}
```
public void setOutlineLevel(int value)
```


Specifies the outline level of the paragraph in the document.

 **Examples:** 

Shows how to configure paragraph outline levels to create collapsible text.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [OutlineLevel](../../com.aspose.words/outlinelevel/) constants. |

### setPageBreakBefore(boolean value) {#setPageBreakBefore-boolean}
```
public void setPageBreakBefore(boolean value)
```


True if a page break is forced before the paragraph.

 **Examples:** 

Shows how to create paragraphs with page breaks at the beginning.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setRightIndent(double value) {#setRightIndent-double}
```
public void setRightIndent(double value)
```


Sets the value (in points) that represents the right indent for paragraph.

 **Examples:** 

Shows how to configure paragraph formatting to create off-center text.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The value (in points) that represents the right indent for paragraph. |

### setSnapToGrid(boolean value) {#setSnapToGrid-boolean}
```
public void setSnapToGrid(boolean value)
```


Specifies whether the current paragraph should use the document grid lines per page settings when laying out the contents in the paragraph.

 **Examples:** 

Shows how to specify a limit for the number of lines that each page may have.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setSpaceAfter(double value) {#setSpaceAfter-double}
```
public void setSpaceAfter(double value)
```


Sets the amount of spacing (in points) after the paragraph.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The amount of spacing (in points) after the paragraph. |

### setSpaceAfterAuto(boolean value) {#setSpaceAfterAuto-boolean}
```
public void setSpaceAfterAuto(boolean value)
```


True if the amount of spacing after the paragraph is set automatically.

 **Remarks:** 

When set to  true , overrides the effect of [getSpaceAfter()](../../com.aspose.words/paragraphformat/\#getSpaceAfter) / [setSpaceAfter(double)](../../com.aspose.words/paragraphformat/\#setSpaceAfter-double).

When you set paragraph Space Before and Space After to Auto, Microsoft Word adds 14 points spacing between paragraphs automatically according to the following rules:

 *  Normally, spacing is added after all paragraphs.
 *  In a bulleted or numbered list, spacing is added only after the last item in the list. Spacing is not added between the list items.
 *  In a nested bulleted or numbered list spacing is not added.
 *  Spacing is normally added after a table.
 *  Spacing is not added after a table if it is the last block in a table cell.
 *  Spacing is not added after the last paragraph in a table cell.

 **Examples:** 

Shows how to set automatic paragraph spacing.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setSpaceBefore(double value) {#setSpaceBefore-double}
```
public void setSpaceBefore(double value)
```


Sets the amount of spacing (in points) before the paragraph.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The amount of spacing (in points) before the paragraph. |

### setSpaceBeforeAuto(boolean value) {#setSpaceBeforeAuto-boolean}
```
public void setSpaceBeforeAuto(boolean value)
```


True if the amount of spacing before the paragraph is set automatically.

 **Remarks:** 

When set to  true , overrides the effect of [getSpaceBefore()](../../com.aspose.words/paragraphformat/\#getSpaceBefore) / [setSpaceBefore(double)](../../com.aspose.words/paragraphformat/\#setSpaceBefore-double).

When you set paragraph Space Before and Space After to Auto, Microsoft Word adds 14 points spacing between paragraphs automatically according to the following rules:

 *  Normally, spacing is added after all paragraphs.
 *  In a bulleted or numbered list, spacing is added only after the last item in the list. Spacing is not added between the list items.
 *  In a nested bulleted or numbered list spacing is not added.
 *  Spacing is normally added after a table.
 *  Spacing is not added after a table if it is the last block in a table cell.
 *  Spacing is not added after the last paragraph in a table cell.

 **Examples:** 

Shows how to set automatic paragraph spacing.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setStyle(Style value) {#setStyle-com.aspose.words.Style}
```
public void setStyle(Style value)
```


Sets the paragraph style applied to this formatting.

 **Examples:** 

Shows how to create and use a paragraph style with list formatting.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | [Style](../../com.aspose.words/style/) | The paragraph style applied to this formatting. |

### setStyleIdentifier(int value) {#setStyleIdentifier-int}
```
public void setStyleIdentifier(int value)
```


Sets the locale independent style identifier of the paragraph style applied to this formatting.

 **Examples:** 

Shows how to insert a Table of contents (TOC) into a document using heading styles as entries.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The locale independent style identifier of the paragraph style applied to this formatting. The value must be one of [StyleIdentifier](../../com.aspose.words/styleidentifier/) constants. |

### setStyleName(String value) {#setStyleName-java.lang.String}
```
public void setStyleName(String value)
```


Sets the name of the paragraph style applied to this formatting.

 **Examples:** 

Shows how to construct an Aspose.Words document by hand.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The name of the paragraph style applied to this formatting. |

### setSuppressAutoHyphens(boolean value) {#setSuppressAutoHyphens-boolean}
```
public void setSuppressAutoHyphens(boolean value)
```


Specifies whether the current paragraph should be exempted from any hyphenation which is applied in the document settings.

 **Examples:** 

Shows how to suppress hyphenation for a paragraph.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setSuppressLineNumbers(boolean value) {#setSuppressLineNumbers-boolean}
```
public void setSuppressLineNumbers(boolean value)
```


Specifies whether the current paragraph's lines should be exempted from line numbering which is applied in the parent section.

 **Examples:** 

Shows how to enable line numbering for a section.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setWidowControl(boolean value) {#setWidowControl-boolean}
```
public void setWidowControl(boolean value)
```


True if the first and last lines in the paragraph are to remain on the same page as the rest of the paragraph.

 **Examples:** 

Shows how to enable widow/orphan control for a paragraph.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setWordWrap(boolean value) {#setWordWrap-boolean}
```
public void setWordWrap(boolean value)
```


If this property is  false , Latin text in the middle of a word can be wrapped for the current paragraph. Otherwise Latin text is wrapped by whole words.

 **Examples:** 

Shows how to set special properties for Asian typography.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 ParagraphFormat format = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat();
 format.setFarEastLineBreakControl(true);
 format.setWordWrap(false);
 format.setHangingPunctuation(true);

 doc.save(getArtifactsDir() + "ParagraphFormat.AsianTypographyProperties.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

