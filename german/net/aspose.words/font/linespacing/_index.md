---
title: Font.LineSpacing
second_title: Aspose.Words für .NET-API-Referenz
description: Font eigendom. Gibt den Zeilenabstand dieser Schriftart zurück in Punkt.
type: docs
weight: 190
url: /de/net/aspose.words/font/linespacing/
---
## Font.LineSpacing property

Gibt den Zeilenabstand dieser Schriftart zurück (in Punkt).

```csharp
public double LineSpacing { get; }
```

### Beispiele

Zeigt, wie der Zeilenabstand einer Schriftart in Punkt ermittelt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Verschiedene Schriftarten für den DocumentBuilder festlegen und deren Zeilenabstand überprüfen.
builder.Font.Name = "Calibri";
Assert.AreEqual(14.6484375d, builder.Font.LineSpacing);

builder.Font.Name = "Times New Roman";
Assert.AreEqual(13.798828125d, builder.Font.LineSpacing);
```

### Siehe auch

* class [Font](../)
* namensraum [Aspose.Words](../../font/)
* Montage [Aspose.Words](../../../)


