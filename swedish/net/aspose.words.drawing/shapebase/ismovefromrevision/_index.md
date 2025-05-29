---
title: ShapeBase.IsMoveFromRevision
linktitle: IsMoveFromRevision
articleTitle: IsMoveFromRevision
second_title: Aspose.Words för .NET
description: Upptäck egenskapen ShapeBase IsMoveFromRevision i Microsoft Word. Spåra enkelt ändringar och identifiera flyttade eller borttagna objekt med precision.
type: docs
weight: 340
url: /sv/net/aspose.words.drawing/shapebase/ismovefromrevision/
---
## ShapeBase.IsMoveFromRevision property

Returer`sann` om det här objektet flyttades (raderades) i Microsoft Word medan ändringsspårning var aktiverad.

```csharp
public bool IsMoveFromRevision { get; }
```

## Exempel

Visar hur man identifierar former för flyttrevisioner.

```csharp
// En flytt- och revisionsåtgärd är när vi flyttar ett element i dokumentets brödtext genom att klippa ut och klistra in det i Microsoft Word samtidigt som
// spårning av ändringar. Om vi använder en inbäddad form i en sådan textförflyttning, kommer den formen också att vara en revision.
// Att kopiera och klistra in eller flytta flytande former skapar inte flyttningsrevideringar.
Document doc = new Document(MyDir + "Revision shape.docx");

// Flyttade revisioner består av par av "Flytta från" och "Flytta till" revisioner. Vi flyttade i det här dokumentet i en form,
// men tills vi accepterar eller avvisar flyttrevisionen kommer det att finnas två instanser av den formen.
Shape[] shapes = doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>().ToArray();

Assert.AreEqual(2, shapes.Length);

// Detta är "Flytta till"-revisionen, vilket är formen vid dess ankomstdestination.
// Om vi accepterar revisionen kommer denna "Flytta till" revisionsform att försvinna,
// och revisionsformen "Flytta från" kommer att finnas kvar.
Assert.False(shapes[0].IsMoveFromRevision);
Assert.True(shapes[0].IsMoveToRevision);

// Detta är "Flytta från"-revisionen, vilket är formen på sin ursprungliga plats.
// Om vi accepterar revisionen kommer denna "Flytta från" revisionsform att försvinna,
// och revisionsformen "Flytta till" kommer att finnas kvar.
Assert.True(shapes[1].IsMoveFromRevision);
Assert.False(shapes[1].IsMoveToRevision);
```

### Se även

* class [ShapeBase](../)
* namnutrymme [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../../)
