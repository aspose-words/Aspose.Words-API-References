---
title: CellFormat.SetPaddings
linktitle: SetPaddings
articleTitle: SetPaddings
second_title: Aspose.Words for .NET
description: Discover the CellFormat SetPaddings method to customize cell spacing in points, enhancing your layout for improved readability and design.
type: docs
weight: 170
url: /net/aspose.words.tables/cellformat/setpaddings/
---
## CellFormat.SetPaddings method

Sets the amount of space (in points) to add to the left/top/right/bottom of the contents of cell.

```csharp
public void SetPaddings(double leftPadding, double topPadding, double rightPadding, 
    double bottomPadding)
```

## Examples

Shows how to pad the contents of a cell with whitespace.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Set a padding distance (in points) between the border and the text contents
// of each table cell we create with the document builder. 
builder.CellFormat.SetPaddings(5, 10, 40, 50);

// Create a table with one cell whose contents will have whitespace padding.
builder.StartTable();
builder.InsertCell();
builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. " +
              "Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.");

doc.Save(ArtifactsDir + "CellFormat.Padding.docx");
```

### See Also

* class [CellFormat](../)
* namespace [Aspose.Words.Tables](../../../aspose.words.tables/)
* assembly [Aspose.Words](../../../)
