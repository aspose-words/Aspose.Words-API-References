---
title: Row.Hidden
linktitle: Hidden
articleTitle: Hidden
second_title: Aspose.Words for .NET
description: Row Hidden property. Gets or sets a flag indicating whether this row is hidden or not.
type: docs
weight: 40
url: /net/aspose.words.tables/row/hidden/
---
## Row.Hidden property

Gets or sets a flag indicating whether this row is hidden or not.

```csharp
public bool Hidden { get; set; }
```

## Remarks

Hidden row is not supported for WordML and ODT documents.

## Examples

Shows how to hide a table row.

```csharp
Document doc = new Document(MyDir + "Tables.docx");

Row row = doc.FirstSection.Body.Tables[0].FirstRow;
row.Hidden = true;

doc.Save(ArtifactsDir + "Table.HiddenRow.docx");

doc = new Document(ArtifactsDir + "Table.HiddenRow.docx");

row = doc.FirstSection.Body.Tables[0].FirstRow;
Assert.That(row.Hidden, Is.True);

foreach (Cell cell in row.Cells)
{
    foreach (Paragraph para in cell.Paragraphs)
    {
        foreach (Run run in para.Runs)
            Assert.That(run.Font.Hidden, Is.True);
    }
}
```

### See Also

* class [Row](../)
* namespace [Aspose.Words.Tables](../../../aspose.words.tables/)
* assembly [Aspose.Words](../../../)
