---
title: Row.EnsureMinimum
linktitle: EnsureMinimum
articleTitle: EnsureMinimum
second_title: Aspose.Words för .NET
description: Upptäck Row EnsureMinimum-metoden, skapa och lägg enkelt till en cell när ingen finns, vilket förbättrar din datastrukturhantering.
type: docs
weight: 150
url: /sv/net/aspose.words.tables/row/ensureminimum/
---
## Row.EnsureMinimum method

Om[`Row`](../) har inga celler, skapar och lägger till en[`Cell`](../../cell/) .

```csharp
public void EnsureMinimum()
```

## Exempel

Visar hur man säkerställer att en radnod innehåller de noder vi behöver för att börja lägga till innehåll i den.

```csharp
Document doc = new Document();
Table table = new Table(doc);
doc.FirstSection.Body.AppendChild(table);
Row row = new Row(doc);
table.AppendChild(row);

// Rader innehåller celler som innehåller stycken med typiska element som sekvenser, former och även andra tabeller.
// Vår nya rad har ingen av dessa noder, och vi kan inte lägga till innehåll i den förrän den har det.
Assert.AreEqual(0, row.GetChildNodes(NodeType.Any, true).Count);

// Att anropa metoden "EnsureMinimum" på en tabell säkerställer att
// tabellen har minst en cell med ett tomt stycke.
row.EnsureMinimum();
row.FirstCell.FirstParagraph.AppendChild(new Run(doc, "Hello world!"));
```

### Se även

* class [Row](../)
* namnutrymme [Aspose.Words.Tables](../../../aspose.words.tables/)
* hopsättning [Aspose.Words](../../../)
