---
title: ParagraphFormat class
linktitle: ParagraphFormat class
articleTitle: ParagraphFormat class
second_title: Aspose.Words for Node.js
description: "Aspose.Words.ParagraphFormat class. Represents all the formatting for a paragraph"
type: docs
weight: 1030
url: /nodejs-net/aspose.words/paragraphformat/
---

## ParagraphFormat class

Represents all the formatting for a paragraph.
To learn more, visit the [Working with Paragraphs](https://docs.aspose.com/words/nodejs-net/working-with-paragraphs/) documentation article.




### Properties

| Name | Description |
| --- | --- |
| [addSpaceBetweenFarEastAndAlpha](./addSpaceBetweenFarEastAndAlpha/) | Gets or sets a flag indicating whether inter-character spacing is automatically adjusted between regions of Latin text and regions of East Asian text in the current paragraph. |
| [addSpaceBetweenFarEastAndDigit](./addSpaceBetweenFarEastAndDigit/) | Gets or sets a flag indicating whether inter-character spacing is automatically adjusted between regions of numbers and regions of East Asian text in the current paragraph. |
| [alignment](./alignment/) | Gets or sets text alignment for the paragraph. |
| [baselineAlignment](./baselineAlignment/) | Gets or sets fonts vertical position on a line. |
| [bidi](./bidi/) | Gets or sets whether this is a right-to-left paragraph. |
| [borders](./borders/) | Gets collection of borders of the paragraph. |
| [characterUnitFirstLineIndent](./characterUnitFirstLineIndent/) | Gets or sets the value (in characters) for the first-line or hanging indent. Use positive values to set the first-line indent, and negative values to set the hanging indent. |
| [characterUnitLeftIndent](./characterUnitLeftIndent/) | Gets or sets the left indent value (in characters) for the specified paragraphs. |
| [characterUnitRightIndent](./characterUnitRightIndent/) | Gets or sets the right indent value (in characters) for the specified paragraphs. |
| [dropCapPosition](./dropCapPosition/) | Gets or sets the position for a drop cap text. |
| [farEastLineBreakControl](./farEastLineBreakControl/) | Gets or sets a flag indicating whether East Asian line-breaking rules are applied to the current paragraph. |
| [firstLineIndent](./firstLineIndent/) | Gets or sets the value (in points) for a first line or hanging indent. Use positive values to set the first-line indent, and negative values to set the hanging indent. |
| [hangingPunctuation](./hangingPunctuation/) | Gets or sets a flag indicating whether hanging punctuation is enabled for the current paragraph. |
| [isHeading](./isHeading/) | True when the paragraph style is one of the built-in Heading styles. |
| [isListItem](./isListItem/) | True when the paragraph is an item in a bulleted or numbered list. |
| [keepTogether](./keepTogether/) | True if all lines in the paragraph are to remain on the same page. |
| [keepWithNext](./keepWithNext/) | True if the paragraph is to remains on the same page as the paragraph that follows it. |
| [leftIndent](./leftIndent/) | Gets or sets the value (in points) that represents the left indent for paragraph. |
| [lineSpacing](./lineSpacing/) | Gets or sets the line spacing (in points) for the paragraph. |
| [lineSpacingRule](./lineSpacingRule/) | Gets or sets the line spacing for the paragraph. |
| [lineUnitAfter](./lineUnitAfter/) | Gets or sets the amount of spacing (in gridlines) after the paragraphs. |
| [lineUnitBefore](./lineUnitBefore/) | Gets or sets the amount of spacing (in gridlines) before the paragraphs. |
| [linesToDrop](./linesToDrop/) | Gets or sets the number of lines of the paragraph text used to calculate the drop cap height. |
| [mirrorIndents](./mirrorIndents/) | Gets or sets a flag indicating whether the left and right indents are of the same width. |
| [noSpaceBetweenParagraphsOfSameStyle](./noSpaceBetweenParagraphsOfSameStyle/) | When ``true``, [ParagraphFormat.spaceBefore](./spaceBefore/) and [ParagraphFormat.spaceAfter](./spaceAfter/) will be ignored between the paragraphs of the same style. |
| [outlineLevel](./outlineLevel/) | Specifies the outline level of the paragraph in the document. |
| [pageBreakBefore](./pageBreakBefore/) | True if a page break is forced before the paragraph. |
| [rightIndent](./rightIndent/) | Gets or sets the value (in points) that represents the right indent for paragraph. |
| [shading](./shading/) | Returns a [Shading](../shading/) object that refers to the shading formatting for the paragraph. |
| [snapToGrid](./snapToGrid/) | Specifies whether the current paragraph should use the document grid lines per page settings when laying out the contents in the paragraph. |
| [spaceAfter](./spaceAfter/) | Gets or sets the amount of spacing (in points) after the paragraph. |
| [spaceAfterAuto](./spaceAfterAuto/) | True if the amount of spacing after the paragraph is set automatically. |
| [spaceBefore](./spaceBefore/) | Gets or sets the amount of spacing (in points) before the paragraph. |
| [spaceBeforeAuto](./spaceBeforeAuto/) | True if the amount of spacing before the paragraph is set automatically. |
| [style](./style/) | Gets or sets the paragraph style applied to this formatting. |
| [styleIdentifier](./styleIdentifier/) | Gets or sets the locale independent style identifier of the paragraph style applied to this formatting. |
| [styleName](./styleName/) | Gets or sets the name of the paragraph style applied to this formatting. |
| [suppressAutoHyphens](./suppressAutoHyphens/) | Specifies whether the current paragraph should be exempted from any hyphenation which is applied in the document settings. |
| [suppressLineNumbers](./suppressLineNumbers/) | Specifies whether the current paragraph's lines should be exempted from line numbering which is applied in the parent section. |
| [tabStops](./tabStops/) | Gets the collection of custom tab stops defined for this object. |
| [widowControl](./widowControl/) | True if the first and last lines in the paragraph are to remain on the same page as the rest of the paragraph. |
| [wordWrap](./wordWrap/) | If this property is ``false``, Latin text in the middle of a word can be wrapped for the current paragraph. Otherwise Latin text is wrapped by whole words. |

### Methods

| Name | Description |
| --- | --- |
|[ clearFormatting()](./clearFormatting/#default) | Resets to default paragraph formatting. |

### Examples

Shows how to construct an Aspose.words document by hand.

```js
let doc = new aw.Document();

// A blank document contains one section, one body and one paragraph.
// Call the "RemoveAllChildren" method to remove all those nodes,
// and end up with a document node with no children.
doc.removeAllChildren();

// This document now has no composite child nodes that we can add content to.
// If we wish to edit it, we will need to repopulate its node collection.
// First, create a new section, and then append it as a child to the root document node.
let section = new aw.Section(doc);
doc.appendChild(section);

// Set some page setup properties for the section.
section.pageSetup.sectionStart = aw.SectionStart.NewPage;
section.pageSetup.paperSize = aw.PaperSize.Letter;

// A section needs a body, which will contain and display all its contents
// on the page between the section's header and footer.
let body = new aw.Body(doc);
section.appendChild(body);

// Create a paragraph, set some formatting properties, and then append it as a child to the body.
let para = new aw.Paragraph(doc);

para.paragraphFormat.styleName = "Heading 1";
para.paragraphFormat.alignment = aw.ParagraphAlignment.Center;

body.appendChild(para);

// Finally, add some content to do the document. Create a run,
// set its appearance and contents, and then append it as a child to the paragraph.
let run = new aw.Run(doc);
run.text = "Hello World!";
run.font.color = "#FF0000";
para.appendChild(run);

expect(doc.getText().trim()).toEqual("Hello World!");

doc.save(base.artifactsDir + "Section.CreateManually.docx");
```

### See Also

* module [Aspose.Words](../)

