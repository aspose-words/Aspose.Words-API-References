---
title: CompositeNode.HasChildNodes
linktitle: HasChildNodes
articleTitle: HasChildNodes
second_title: Aspose.Words für .NET
description: Ermitteln Sie mit der Eigenschaft „HasChildNodes“, ob ein CompositeNode untergeordnete Knoten hat. Vereinfachen Sie Ihre Programmierung mit dieser wichtigen Funktion für effizientes Knotenmanagement.
type: docs
weight: 30
url: /de/net/aspose.words/compositenode/haschildnodes/
---
## CompositeNode.HasChildNodes property

Rückgaben`WAHR` wenn dieser Knoten untergeordnete Knoten hat.

```csharp
public bool HasChildNodes { get; }
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

* class [CompositeNode](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
