---
title: Row.EnsureMinimum
second_title: Aspose.Words für .NET-API-Referenz
description: Row methode. Wenn die Die Zeile hat keine Zellen erstellt und hängt eine an Zelle .
type: docs
weight: 110
url: /de/net/aspose.words.tables/row/ensureminimum/
---
## Row.EnsureMinimum method

Wenn die **Die Zeile** hat keine Zellen, erstellt und hängt eine an **Zelle** .

```csharp
public void EnsureMinimum()
```

### Beispiele

Zeigt, wie sichergestellt wird, dass ein Zeilenknoten die Knoten enthält, die wir benötigen, um mit dem Hinzufügen von Inhalten zu beginnen.

```csharp
Document doc = new Document();
Table table = new Table(doc);
doc.FirstSection.Body.AppendChild(table);
Row row = new Row(doc);
table.AppendChild(row);

// Zeilen enthalten Zellen, die Absätze mit typischen Elementen wie Läufen, Formen und sogar anderen Tabellen enthalten.
// Unsere neue Zeile hat keinen dieser Knoten, und wir können ihr keinen Inhalt hinzufügen, bis dies der Fall ist.
Assert.AreEqual(0, row.GetChildNodes(NodeType.Any, true).Count);

// Das Aufrufen der "EnsureMinimum"-Methode für eine Tabelle stellt dies sicher
// Die Tabelle hat mindestens eine Zelle mit einem leeren Absatz.
row.EnsureMinimum();
row.FirstCell.FirstParagraph.AppendChild(new Run(doc, "Hello world!"));
```

### Siehe auch

* class [Row](../)
* namensraum [Aspose.Words.Tables](../../row/)
* Montage [Aspose.Words](../../../)


