---
title: ParagraphFormat.spaceAfter property
linktitle: spaceAfter property
articleTitle: spaceAfter property
second_title: Aspose.Words for NodeJs
description: "ParagraphFormat.spaceAfter property. Gets or sets the amount of spacing (in points) after the paragraph."
type: docs
weight: 310
url: /nodejs-net/Aspose.Words/paragraphformat/spaceAfter/
---

## ParagraphFormat.spaceAfter property

Gets or sets the amount of spacing (in points) after the paragraph.


```js
get spaceAfter(): number
```

### Exceptions

| exception | condition |
| --- | --- |
| RuntimeError (Proxy error(ArgumentOutOfRangeException)) | Throws when argument was out of the range of valid values. |

### Remarks

Has no effect when [ParagraphFormat.spaceAfterAuto](../spaceAfterAuto/) is ``True``.

Valid values ​​range from 0 to 1584 inclusive.




### Examples

Shows how to set automatic paragraph spacing.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// Apply a large amount of spacing before and after paragraphs that this builder will create.
builder.paragraphFormat.spaceBefore = 24;
builder.paragraphFormat.spaceAfter = 24;

// Set these flags to "true" to apply automatic spacing,
// effectively ignoring the spacing in the properties we set above.
// Leave them as "false" will apply our custom paragraph spacing.
builder.paragraphFormat.spaceAfterAuto = autoSpacing;
builder.paragraphFormat.spaceBeforeAuto = autoSpacing;

// Insert two paragraphs that will have spacing above and below them and save the document.
builder.writeln("Paragraph 1.");
builder.writeln("Paragraph 2.");

doc.save(base.artifactsDir + "ParagraphFormat.ParagraphSpacingAuto.docx");
```

Shows how to apply no spacing between paragraphs with the same style.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// Apply a large amount of spacing before and after paragraphs that this builder will create.
builder.paragraphFormat.spaceBefore = 24;
builder.paragraphFormat.spaceAfter = 24;

// Set the "NoSpaceBetweenParagraphsOfSameStyle" flag to "true" to apply
// no spacing between paragraphs with the same style, which will group similar paragraphs.
// Leave the "NoSpaceBetweenParagraphsOfSameStyle" flag as "false"
// to evenly apply spacing to every paragraph.
builder.paragraphFormat.noSpaceBetweenParagraphsOfSameStyle = noSpaceBetweenParagraphsOfSameStyle;

builder.paragraphFormat.style = doc.styles.at("Normal");
builder.writeln(`Paragraph in the \"${builder.paragraphFormat.style.name}\" style.`);
builder.writeln(`Paragraph in the \"${builder.paragraphFormat.style.name}\" style.`);
builder.writeln(`Paragraph in the \"${builder.paragraphFormat.style.name}\" style.`);
builder.paragraphFormat.style = doc.styles.at("Quote");
builder.writeln(`Paragraph in the \"${builder.paragraphFormat.style.name}\" style.`);
builder.writeln(`Paragraph in the \"${builder.paragraphFormat.style.name}\" style.`);
builder.paragraphFormat.style = doc.styles.at("Normal");
builder.writeln(`Paragraph in the \"${builder.paragraphFormat.style.name}\" style.`);
builder.writeln(`Paragraph in the \"${builder.paragraphFormat.style.name}\" style.`);

doc.save(base.artifactsDir + "ParagraphFormat.ParagraphSpacingSameStyle.docx");
```

### See Also

* module [Aspose.Words](../../)
* class [ParagraphFormat](../)

