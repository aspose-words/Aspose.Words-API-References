---
title: FieldAdvance.LeftOffset
linktitle: LeftOffset
articleTitle: LeftOffset
second_title: Aspose.Words for .NET
description: Discover the FieldAdvance LeftOffset property to easily adjust text alignment by setting points for precise left movement. Enhance your document layout!
type: docs
weight: 40
url: /net/aspose.words.fields/fieldadvance/leftoffset/
---
## FieldAdvance.LeftOffset property

Gets or sets the number of points by which the text that follows the field should be moved left.

```csharp
public string LeftOffset { get; set; }
```

## Examples

Shows how to insert an ADVANCE field, and edit its properties.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("This text is in its normal place.");

// Below are two ways of using the ADVANCE field to adjust the position of text that follows it.
// The effects of an ADVANCE field continue to be applied until the paragraph ends,
// or another ADVANCE field updates the offset/coordinate values.
// 1 -  Specify a directional offset:
FieldAdvance field = (FieldAdvance)builder.InsertField(FieldType.FieldAdvance, true);
field.RightOffset = "5";
field.UpOffset = "5";

Assert.That(field.GetFieldCode(), Is.EqualTo(" ADVANCE  \\r 5 \\u 5"));

builder.Write("This text will be moved up and to the right.");

field = (FieldAdvance)builder.InsertField(FieldType.FieldAdvance, true);
field.DownOffset = "5";
field.LeftOffset = "100";

Assert.That(field.GetFieldCode(), Is.EqualTo(" ADVANCE  \\d 5 \\l 100"));

builder.Writeln("This text is moved down and to the left, overlapping the previous text.");

// 2 -  Move text to a position specified by coordinates:
field = (FieldAdvance)builder.InsertField(FieldType.FieldAdvance, true);
field.HorizontalPosition = "-100";
field.VerticalPosition = "200";

Assert.That(field.GetFieldCode(), Is.EqualTo(" ADVANCE  \\x -100 \\y 200"));

builder.Write("This text is in a custom position.");

doc.Save(ArtifactsDir + "Field.ADVANCE.docx");
```

### See Also

* class [FieldAdvance](../)
* namespace [Aspose.Words.Fields](../../../aspose.words.fields/)
* assembly [Aspose.Words](../../../)
