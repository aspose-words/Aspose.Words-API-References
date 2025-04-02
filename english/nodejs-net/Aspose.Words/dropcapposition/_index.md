---
title: DropCapPosition enumeration
linktitle: DropCapPosition enumeration
articleTitle: DropCapPosition enumeration
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.DropCapPosition enumeration. Specifies the position for a drop cap text."
type: docs
weight: 360
url: /nodejs-net/Aspose.Words/dropcapposition/
---

## DropCapPosition enumeration

Specifies the position for a drop cap text.


### Members

| Name | Description |
| --- | --- |
| None | The paragraph does not have a drop cap. |
| Normal | The drop cap is positioned inside the text margin on the anchor paragraph. |
| Margin | The drop cap is positioned outside the text margin on the anchor paragraph. |

### Examples

Shows how to create a drop cap.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// Insert one paragraph with a large letter that the text in the second and third paragraphs begins with.
builder.font.size = 54;
builder.writeln("L");

builder.font.size = 18;
builder.writeln("orem ipsum dolor sit amet, consectetur adipiscing elit, " +
  "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ");
builder.writeln("Ut enim ad minim veniam, quis nostrud exercitation " +
  "ullamco laboris nisi ut aliquip ex ea commodo consequat.");

// Currently, the second and third paragraphs will appear underneath the first.
// We can convert the first paragraph as a drop cap for the other paragraphs via its "ParagraphFormat" object.
// Set the "DropCapPosition" property to "DropCapPosition.Margin" to place the drop cap
// outside the left-hand side page margin if our text is left-to-right.
// Set the "DropCapPosition" property to "DropCapPosition.Normal" to place the drop cap within the page margins
// and to wrap the rest of the text around it.
// "DropCapPosition.None" is the default state for all paragraphs.
let format = doc.firstSection.body.firstParagraph.paragraphFormat;
format.dropCapPosition = dropCapPosition;

doc.save(base.artifactsDir + "ParagraphFormat.DropCap.docx");
```

### See Also

* module [Aspose.Words](../)

