---
title: Cell.EnsureMinimum
linktitle: EnsureMinimum
articleTitle: EnsureMinimum
second_title: Aspose.Words för .NET
description: Optimera din cellstruktur med EnsureMinimum-metoden, lägg enkelt till ett stycke om det sista underordnade stycket inte är ett. Förbättra dokumentets tydlighet!
type: docs
weight: 160
url: /sv/net/aspose.words.tables/cell/ensureminimum/
---
## Cell.EnsureMinimum method

Om det sista underordnade stycket inte är ett stycke skapas och läggs till ett tomt stycke.

```csharp
public void EnsureMinimum()
```

## Exempel

Visar hur man säkerställer att en cellnod innehåller de noder vi behöver för att börja lägga till innehåll i den.

```csharp
Document doc = new Document();
Table table = new Table(doc);
doc.FirstSection.Body.AppendChild(table);
Row row = new Row(doc);
table.AppendChild(row);
Cell cell = new Cell(doc);
row.AppendChild(cell);

// Celler kan innehålla stycken med typiska element som sekvenser, former och även andra tabeller.
// Vår nya cell har inga stycken, och vi kan inte lägga till innehåll som noder som `run` och `shape` förrän den har det.
Assert.AreEqual(0, cell.GetChildNodes(NodeType.Any, true).Count);

// Att anropa metoden "EnsureMinimum" på en cell säkerställer att
// cellen har minst ett tomt stycke, som vi sedan kan lägga till innehåll i.
cell.EnsureMinimum();
cell.FirstParagraph.AppendChild(new Run(doc, "Hello world!"));
```

### Se även

* class [Cell](../)
* namnutrymme [Aspose.Words.Tables](../../../aspose.words.tables/)
* hopsättning [Aspose.Words](../../../)
