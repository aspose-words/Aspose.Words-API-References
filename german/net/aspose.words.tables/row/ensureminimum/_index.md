---
title: Row.EnsureMinimum
linktitle: EnsureMinimum
articleTitle: EnsureMinimum
second_title: Aspose.Words für .NET
description: Row EnsureMinimum methode. Wenn dieRow hat keine Zellen erstellt eine und hängt eine anCell  in C#.
type: docs
weight: 130
url: /de/net/aspose.words.tables/row/ensureminimum/
---
## Row.EnsureMinimum method

Wenn die[`Row`](../) hat keine Zellen, erstellt eine und hängt eine an[`Cell`](../../cell/) .

```csharp
public void EnsureMinimum()
```

## Beispiele

Zeigt, wie sichergestellt wird, dass ein Zeilenknoten die Knoten enthält, die wir benötigen, um mit dem Hinzufügen von Inhalten zu beginnen.

```csharp
Document doc = new Document();
Table table = new Table(doc);
doc.FirstSection.Body.AppendChild(table);
Row row = new Row(doc);
table.AppendChild(row);

// Zeilen enthalten Zellen, die Absätze mit typischen Elementen wie Läufen, Formen und sogar anderen Tabellen enthalten.
// Unsere neue Zeile hat keinen dieser Knoten und wir können ihr erst dann Inhalte hinzufügen, wenn dies der Fall ist.
Assert.AreEqual(0, row.GetChildNodes(NodeType.Any, true).Count);

// Der Aufruf der Methode „EnsureMinimum“ für eine Tabelle stellt dies sicher
// Die Tabelle enthält mindestens eine Zelle mit einem leeren Absatz.
row.EnsureMinimum();
row.FirstCell.FirstParagraph.AppendChild(new Run(doc, "Hello world!"));
```

### Siehe auch

* class [Row](../)
* namensraum [Aspose.Words.Tables](../../../aspose.words.tables/)
* Montage [Aspose.Words](../../../)
