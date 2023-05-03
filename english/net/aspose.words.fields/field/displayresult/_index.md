---
title: Field.DisplayResult
linktitle: DisplayResult
articleTitle: DisplayResult
second_title: Aspose.Words for .NET API Reference
description: Field DisplayResult property. Gets the text that represents the displayed field result in C#.
type: docs
weight: 10
url: /net/aspose.words.fields/field/displayresult/
---
## Field.DisplayResult property

Gets the text that represents the displayed field result.

```csharp
public string DisplayResult { get; }
```

## Remarks

The [`UpdateListLabels`](../../../aspose.words/document/updatelistlabels/) method must be called to obtain correct value for the [`FieldListNum`](../../fieldlistnum/), [`FieldAutoNum`](../../fieldautonum/), [`FieldAutoNumOut`](../../fieldautonumout/) and [`FieldAutoNumLgl`](../../fieldautonumlgl/) fields.

## Examples

Shows how to get the real text that a field displays in the document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("This document was written by ");
FieldAuthor fieldAuthor = (FieldAuthor)builder.InsertField(FieldType.FieldAuthor, true);
fieldAuthor.AuthorName = "John Doe";

// We can use the DisplayResult property to verify what exact text
// a field would display in its place in the document.
Assert.AreEqual(string.Empty, fieldAuthor.DisplayResult);

// Fields do not maintain accurate result values in real-time. 
// To make sure our fields display accurate results at any given time,
// such as right before a save operation, we need to update them manually.
fieldAuthor.Update();

Assert.AreEqual("John Doe", fieldAuthor.DisplayResult);

doc.Save(ArtifactsDir + "Field.DisplayResult.docx");
```

### See Also

* class [Field](../)
* namespace [Aspose.Words.Fields](../../field/)
* assembly [Aspose.Words](../../../)
