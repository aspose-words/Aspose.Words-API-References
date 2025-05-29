---
title: CellFormat.ClearFormatting
linktitle: ClearFormatting
articleTitle: ClearFormatting
second_title: Aspose.Words für .NET
description: Entdecken Sie die CellFormat ClearFormatting-Methode, um Zellenformate mühelos auf die Standardwerte zurückzusetzen, ohne die Zellenbreite zu ändern. Steigern Sie die Effizienz Ihrer Tabellenkalkulation!
type: docs
weight: 160
url: /de/net/aspose.words.tables/cellformat/clearformatting/
---
## CellFormat.ClearFormatting method

Setzt die Zellenformatierung auf die Standardeinstellung zurück. Die Breite der Zelle wird nicht geändert.

```csharp
public void ClearFormatting()
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

* class [CellFormat](../)
* namensraum [Aspose.Words.Tables](../../../aspose.words.tables/)
* Montage [Aspose.Words](../../../)
