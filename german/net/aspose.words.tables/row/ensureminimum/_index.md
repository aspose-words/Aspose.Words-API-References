---
title: Row.EnsureMinimum
linktitle: EnsureMinimum
articleTitle: EnsureMinimum
second_title: Aspose.Words für .NET
description: Entdecken Sie die Row EnsureMinimum-Methode, mit der Sie mühelos eine Zelle erstellen und anhängen können, wenn keine vorhanden ist, und so Ihr Datenstrukturmanagement verbessern.
type: docs
weight: 150
url: /de/net/aspose.words.tables/row/ensureminimum/
---
## Row.EnsureMinimum method

Wenn die[`Row`](../) hat keine Zellen, erstellt und fügt eine hinzu[`Cell`](../../cell/) .

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
// Unsere neue Zeile hat keinen dieser Knoten und wir können ihr keine Inhalte hinzufügen, bis sie welche hat.
Assert.AreEqual(0, row.GetChildNodes(NodeType.Any, true).Count);

// Der Aufruf der Methode "EnsureMinimum" für eine Tabelle stellt sicher, dass
// Die Tabelle hat mindestens eine Zelle mit einem leeren Absatz.
row.EnsureMinimum();
row.FirstCell.FirstParagraph.AppendChild(new Run(doc, "Hello world!"));
```

### Siehe auch

* class [Row](../)
* namensraum [Aspose.Words.Tables](../../../aspose.words.tables/)
* Montage [Aspose.Words](../../../)
