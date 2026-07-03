---
title: ListLevel.RemoveTabStop
linktitle: RemoveTabStop
articleTitle: RemoveTabStop
second_title: Aspose.Words for .NET
description: Clean up list formatting by removing custom tab stops from list levels programmatically using Aspose.Words.
type: docs
weight: 190
url: /net/aspose.words.lists/listlevel/removetabstop/
---
## ListLevel.RemoveTabStop method

Removes tab stop from the list level.

```csharp
public void RemoveTabStop()
```

## Examples

Shows how to clear the list level tab stop.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Create a list with default formatting
builder.ListFormat.ApplyNumberDefault();
builder.Writeln("Numbered list item 1");
builder.Writeln("Numbered list item 2");

// Get the list level and remove its tab stop
ListLevel listLevel = builder.ListFormat.ListLevel;
listLevel.RemoveTabStop();

doc.Save(ArtifactsDir + "Paragraph.RemoveTabStopFromListLevel.docx");
```

### See Also

* class [ListLevel](../)
* namespace [Aspose.Words.Lists](../../../aspose.words.lists/)
* assembly [Aspose.Words](../../../)
