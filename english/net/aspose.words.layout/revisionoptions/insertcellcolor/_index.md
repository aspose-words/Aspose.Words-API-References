---
title: RevisionOptions.InsertCellColor
linktitle: InsertCellColor
articleTitle: InsertCellColor
second_title: Aspose.Words for .NET
description: Customize your spreadsheet with the InsertCellColor property in RevisionOptions. Choose your preferred color for inserted cells—default is blue!
type: docs
weight: 50
url: /net/aspose.words.layout/revisionoptions/insertcellcolor/
---
## RevisionOptions.InsertCellColor property

Allows to specify the color to be used for inserted cells Insertion. Default value is Blue.

```csharp
public RevisionColor InsertCellColor { get; set; }
```

## Examples

Shows how to work with insert/delete cell revision color.

```csharp
Document doc = new Document(MyDir + "Cell revisions.docx");

doc.LayoutOptions.RevisionOptions.InsertCellColor = RevisionColor.LightBlue;
doc.LayoutOptions.RevisionOptions.DeleteCellColor = RevisionColor.DarkRed;

doc.Save(ArtifactsDir + "Revision.RevisionCellColor.pdf");
```

### See Also

* enum [RevisionColor](../../revisioncolor/)
* class [RevisionOptions](../)
* namespace [Aspose.Words.Layout](../../../aspose.words.layout/)
* assembly [Aspose.Words](../../../)
