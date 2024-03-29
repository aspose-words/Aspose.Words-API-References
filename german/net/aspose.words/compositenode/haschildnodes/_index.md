---
title: CompositeNode.HasChildNodes
linktitle: HasChildNodes
articleTitle: HasChildNodes
second_title: Aspose.Words für .NET
description: CompositeNode HasChildNodes eigendom. Gibt zurückWAHR wenn dieser Knoten untergeordnete Knoten hat in C#.
type: docs
weight: 30
url: /de/net/aspose.words/compositenode/haschildnodes/
---
## CompositeNode.HasChildNodes property

Gibt zurück`WAHR` wenn dieser Knoten untergeordnete Knoten hat.

```csharp
public bool HasChildNodes { get; }
```

## Beispiele

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

* class [CompositeNode](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
