---
title: ParagraphFormat.spaceBeforeAuto property
linktitle: spaceBeforeAuto property
articleTitle: spaceBeforeAuto property
second_title: Aspose.Words for NodeJs
description: "ParagraphFormat.spaceBeforeAuto property. True if the amount of spacing before the paragraph is set automatically."
type: docs
weight: 340
url: /nodejs-net/Aspose.Words/paragraphformat/spaceBeforeAuto/
---

## ParagraphFormat.spaceBeforeAuto property

True if the amount of spacing before the paragraph is set automatically.


```js
get spaceBeforeAuto(): boolean
```

### Remarks

When set to ``True``, overrides the effect of [ParagraphFormat.spaceBefore](../spaceBefore/).




When you set paragraph Space Before and Space After to Auto,
Microsoft Word adds 14 points spacing between paragraphs automatically
according to the following rules:


* Normally, spacing is added after all paragraphs.
  
* In a bulleted or numbered list, spacing is added only after the last item in the list.
  Spacing is not added between the list items.
  
* In a nested bulleted or numbered list spacing is not added.
  
* Spacing is normally added after a table.
  
* Spacing is not added after a table if it is the last block in a table cell.
  
* Spacing is not added after the last paragraph in a table cell.
  



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

### See Also

* module [Aspose.Words](../../)
* class [ParagraphFormat](../)

