---
title: Range.Text
second_title: Aspose.Words für .NET-API-Referenz
description: Range eigendom. Ruft den Text des Bereichs ab.
type: docs
weight: 50
url: /de/net/aspose.words/range/text/
---
## Range.Text property

Ruft den Text des Bereichs ab.

```csharp
public string Text { get; }
```

### Bemerkungen

Die zurückgegebene Zeichenfolge enthält alle Steuer- und Sonderzeichen, wie in beschrieben[`ControlChar`](../../controlchar/).

### Beispiele

Zeigt, wie der Textinhalt aller Knoten abgerufen wird, die ein Bereich abdeckt.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Hello world!");

Assert.AreEqual("Hello world!", doc.Range.Text.Trim());
```

### Siehe auch

* class [Range](../)
* namensraum [Aspose.Words](../../range/)
* Montage [Aspose.Words](../../../)


