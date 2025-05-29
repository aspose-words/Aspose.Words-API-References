---
title: CellFormat.Borders
linktitle: Borders
articleTitle: Borders
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft „CellFormat Borders“, um auf Zellrahmensammlungen zuzugreifen und diese anzupassen, um das Design und die Funktionalität von Tabellenkalkulationen zu verbessern.
type: docs
weight: 10
url: /de/net/aspose.words.tables/cellformat/borders/
---
## CellFormat.Borders property

Ruft eine Sammlung von Zellrändern ab.

```csharp
public BorderCollection Borders { get; }
```

## Beispiele

Zeigt, wie die Zeilen aus zwei Tabellen zu einer kombiniert werden.

```csharp
Document doc = new Document(MyDir + "Tables.docx");

// Unten sind zwei Möglichkeiten, eine Tabelle aus einem Dokument zu erhalten.
// 1 – Aus der „Tabellen“-Sammlung eines Body-Knotens:
Table firstTable = doc.FirstSection.Body.Tables[0];

// 2 - Verwenden der Methode „GetChild“:
Table secondTable = (Table)doc.GetChild(NodeType.Table, 1, true);

// Alle Zeilen der aktuellen Tabelle an die nächste anhängen.
while (secondTable.HasChildNodes)
    firstTable.Rows.Add(secondTable.FirstRow);

// Entfernen Sie den leeren Tabellencontainer.
secondTable.Remove();

doc.Save(ArtifactsDir + "Table.CombineTables.docx");
```

### Siehe auch

* class [BorderCollection](../../../aspose.words/bordercollection/)
* class [CellFormat](../)
* namensraum [Aspose.Words.Tables](../../../aspose.words.tables/)
* Montage [Aspose.Words](../../../)
