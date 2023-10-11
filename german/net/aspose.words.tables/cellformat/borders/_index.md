---
title: CellFormat.Borders
second_title: Aspose.Words für .NET-API-Referenz
description: CellFormat eigendom. Ruft eine Sammlung von Rändern der Zelle ab.
type: docs
weight: 10
url: /de/net/aspose.words.tables/cellformat/borders/
---
## CellFormat.Borders property

Ruft eine Sammlung von Rändern der Zelle ab.

```csharp
public BorderCollection Borders { get; }
```

### Beispiele

Zeigt, wie die Zeilen aus zwei Tabellen zu einer kombiniert werden.

```csharp
Document doc = new Document(MyDir + "Tables.docx");

// Nachfolgend finden Sie zwei Möglichkeiten, eine Tabelle aus einem Dokument abzurufen.
// 1 – Aus der „Tables“-Sammlung eines Body-Knotens:
Table firstTable = doc.FirstSection.Body.Tables[0];

// 2 - Verwendung der Methode „GetChild“:
Table secondTable = (Table)doc.GetChild(NodeType.Table, 1, true);

// Alle Zeilen der aktuellen Tabelle an die nächste anhängen.
while (secondTable.HasChildNodes)
    firstTable.Rows.Add(secondTable.FirstRow);

// Den leeren Tabellencontainer entfernen.
secondTable.Remove();

doc.Save(ArtifactsDir + "Table.CombineTables.docx");
```

### Siehe auch

* class [BorderCollection](../../../aspose.words/bordercollection/)
* class [CellFormat](../)
* namensraum [Aspose.Words.Tables](../../cellformat/)
* Montage [Aspose.Words](../../../)


