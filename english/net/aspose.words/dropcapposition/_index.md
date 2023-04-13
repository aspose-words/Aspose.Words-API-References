---
title: DropCapPosition Enum
linktitle: DropCapPosition
second_title: Aspose.Words for .NET API Reference
description: Aspose.Words.DropCapPosition enum. Specifies the position for a drop cap text in C#.
type: docs
weight: 1300
url: /net/aspose.words/dropcapposition/
---
## DropCapPosition enumeration

Specifies the position for a drop cap text.

```csharp
public enum DropCapPosition
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| None | `0` | The paragraph does not have a drop cap. |
| Normal | `1` | The drop cap is positioned inside the text margin on the anchor paragraph. |
| Margin | `2` | The drop cap is positioned outside the text margin on the anchor paragraph. |

## Examples

Shows how to create a drop cap.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insert one paragraph with a large letter that the text in the second and third paragraphs begins with.
builder.Font.Size = 54;
builder.Writeln("L");

builder.Font.Size = 18;
builder.Writeln("orem ipsum dolor sit amet, consectetur adipiscing elit, " +
                "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ");
builder.Writeln("Ut enim ad minim veniam, quis nostrud exercitation " +
                "ullamco laboris nisi ut aliquip ex ea commodo consequat.");

// Currently, the second and third paragraphs will appear underneath the first.
// We can convert the first paragraph as a drop cap for the other paragraphs via its "ParagraphFormat" object.
// Set the "DropCapPosition" property to "DropCapPosition.Margin" to place the drop cap
// outside the left-hand side page margin if our text is left-to-right.
// Set the "DropCapPosition" property to "DropCapPosition.Normal" to place the drop cap within the page margins
// and to wrap the rest of the text around it.
// "DropCapPosition.None" is the default state for all paragraphs.
ParagraphFormat format = doc.FirstSection.Body.FirstParagraph.ParagraphFormat;
format.DropCapPosition = dropCapPosition;

doc.Save(ArtifactsDir + "ParagraphFormat.DropCap.docx");
```

### See Also

* namespace [Aspose.Words](../../aspose.words/)
* assembly [Aspose.Words](../../)
