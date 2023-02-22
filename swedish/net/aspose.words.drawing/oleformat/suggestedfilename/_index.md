---
title: OleFormat.SuggestedFileName
second_title: Aspose.Words för .NET API Referens
description: OleFormat fast egendom. Hämtar filnamnet som föreslås för det aktuella inbäddade objektet om du vill spara det i en fil.
type: docs
weight: 130
url: /sv/net/aspose.words.drawing/oleformat/suggestedfilename/
---
## OleFormat.SuggestedFileName property

Hämtar filnamnet som föreslås för det aktuella inbäddade objektet om du vill spara det i en fil.

```csharp
public string SuggestedFileName { get; }
```

### Exempel

Visar hur man får ett OLE-objekts föreslagna filnamn.

```csharp
Document doc = new Document(MyDir + "OLE shape.rtf");

Shape oleShape = (Shape) doc.FirstSection.Body.GetChild(NodeType.Shape, 0, true);

// OLE-objekt kan ge ett föreslaget filnamn och filtillägg,
// som vi kan använda när vi sparar objektets innehåll i en fil i det lokala filsystemet.
string suggestedFileName = oleShape.OleFormat.SuggestedFileName;

Assert.AreEqual("CSV.csv", suggestedFileName);

using (FileStream fileStream = new FileStream(ArtifactsDir + suggestedFileName, FileMode.Create))
{
    oleShape.OleFormat.Save(fileStream);
}
```

### Se även

* class [OleFormat](../)
* namnutrymme [Aspose.Words.Drawing](../../oleformat/)
* hopsättning [Aspose.Words](../../../)


