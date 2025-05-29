---
title: Table.EnsureMinimum
linktitle: EnsureMinimum
articleTitle: EnsureMinimum
second_title: Aspose.Words för .NET
description: Upptäck Table EnsureMinimum-metoden, skapa och lägg enkelt till en rad när tabellen är tom för sömlös datahantering.
type: docs
weight: 420
url: /sv/net/aspose.words.tables/table/ensureminimum/
---
## Table.EnsureMinimum method

Om tabellen inte har några rader, skapas och läggs till en[`Row`](../../row/) .

```csharp
public void EnsureMinimum()
```

## Exempel

Visar hur man säkerställer att en tabellnod innehåller de noder vi behöver för att lägga till innehåll.

```csharp
Document doc = new Document();
Table table = new Table(doc);
doc.FirstSection.Body.AppendChild(table);

// Tabeller innehåller rader, som innehåller celler, vilka kan innehålla stycken
// med typiska element som körningar, former och även andra tabeller.
// Vår nya tabell har ingen av dessa noder, och vi kan inte lägga till innehåll i den förrän den har det.
Assert.AreEqual(0, table.GetChildNodes(NodeType.Any, true).Count);

// Att anropa metoden "EnsureMinimum" på en tabell säkerställer att
// tabellen har minst en rad och en cell med ett tomt stycke.
table.EnsureMinimum();
table.FirstRow.FirstCell.FirstParagraph.AppendChild(new Run(doc, "Hello world!"));
```

### Se även

* class [Table](../)
* namnutrymme [Aspose.Words.Tables](../../../aspose.words.tables/)
* hopsättning [Aspose.Words](../../../)
