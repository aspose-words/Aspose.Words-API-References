---
title: Range.Text
linktitle: Text
articleTitle: Text
second_title: Aspose.Words für .NET
description: Range Text eigendom. Ruft den Text des Bereichs ab in C#.
type: docs
weight: 60
url: /de/net/aspose.words/range/text/
---
## Range.Text property

Ruft den Text des Bereichs ab.

```csharp
public string Text { get; }
```

## Bemerkungen

Die zurückgegebene Zeichenfolge enthält alle Steuer- und Sonderzeichen, wie in beschrieben[`ControlChar`](../../controlchar/).

## Beispiele

Zeigt, wie der Textinhalt aller Knoten abgerufen wird, die ein Bereich abdeckt.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Hello world!");

Assert.AreEqual("Hello world!", doc.Range.Text.Trim());
```

### Siehe auch

* class [Range](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
