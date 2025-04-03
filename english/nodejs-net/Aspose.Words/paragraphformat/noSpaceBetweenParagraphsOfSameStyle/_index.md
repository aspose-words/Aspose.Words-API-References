---
title: ParagraphFormat.noSpaceBetweenParagraphsOfSameStyle property
linktitle: noSpaceBetweenParagraphsOfSameStyle property
articleTitle: noSpaceBetweenParagraphsOfSameStyle property
second_title: Aspose.Words for NodeJs
description: "ParagraphFormat.noSpaceBetweenParagraphsOfSameStyle property. When ``true``, [ParagraphFormat.spaceBefore](../spaceBefore/) and [ParagraphFormat.spaceAfter](../spaceAfter/) will be ignored between the paragraphs of the same style."
type: docs
weight: 250
url: /nodejs-net/Aspose.Words/paragraphformat/noSpaceBetweenParagraphsOfSameStyle/
---

## ParagraphFormat.noSpaceBetweenParagraphsOfSameStyle property

When ``true``, [ParagraphFormat.spaceBefore](../spaceBefore/) and [ParagraphFormat.spaceAfter](../spaceAfter/) will be ignored
between the paragraphs of the same style.



```js
get noSpaceBetweenParagraphsOfSameStyle(): boolean
```

### Remarks

This setting only takes affect when applied to a paragraph style. If applied to
a paragraph directly, it has no effect.




### Examples

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

