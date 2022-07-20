---
title: EnsureMinimum
second_title: Aspose.Words för .NET API Referens
description: Om Rad har inga celler skapar och lägger till en Cell .
type: docs
weight: 110
url: /sv/net/aspose.words.tables/row/ensureminimum/
---
## Row.EnsureMinimum method

Om **Rad** har inga celler, skapar och lägger till en **Cell** .

```csharp
public void EnsureMinimum()
```

### Exempel

Visar hur man säkerställer att en radnod innehåller de noder vi behöver för att börja lägga till innehåll till den.

```csharp
Document doc = new Document();
Table table = new Table(doc);
doc.FirstSection.Body.AppendChild(table);
Row row = new Row(doc);
table.AppendChild(row);

// Rader innehåller celler som innehåller stycken med typiska element som körningar, former och till och med andra tabeller.
// Vår nya rad har inga av dessa noder, och vi kan inte lägga till innehåll till den förrän den gör det.
Assert.AreEqual(0, row.GetChildNodes(NodeType.Any, true).Count);

// Att anropa metoden "EnsureMinimum" på en tabell säkerställer det
// tabellen har minst en cell med ett tomt stycke.
row.EnsureMinimum();
row.FirstCell.FirstParagraph.AppendChild(new Run(doc, "Hello world!"));
```

### Se även

* class [Row](../../row)
* namnutrymme [Aspose.Words.Tables](../../row)
* hopsättning [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->