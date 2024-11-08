---
title: RevisionOptions.DeleteCellColor
linktitle: DeleteCellColor
articleTitle: DeleteCellColor
second_title: Aspose.Words for .NET
description: RevisionOptions DeleteCellColor property. Allows to specify the color to be used for deleted cells Deletion. Default value is Pink in C#.
type: docs
weight: 20
url: /net/aspose.words.layout/revisionoptions/deletecellcolor/
---
## RevisionOptions.DeleteCellColor property

Allows to specify the color to be used for deleted cells Deletion. Default value is Pink.

```csharp
public RevisionColor DeleteCellColor { get; set; }
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
