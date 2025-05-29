---
title: Font.LineSpacing
linktitle: LineSpacing
articleTitle: LineSpacing
second_title: Aspose.Words für .NET
description: Entdecken Sie die Font LineSpacing-Eigenschaft, die den genauen Zeilenabstand in Punkten bereitstellt und so die Lesbarkeit und das Design Ihres Textes verbessert.
type: docs
weight: 190
url: /de/net/aspose.words/font/linespacing/
---
## Font.LineSpacing property

Gibt den Zeilenabstand dieser Schriftart (in Punkten) zurück.

```csharp
public double LineSpacing { get; }
```

## Beispiele

Zeigt, wie der Zeilenabstand einer Schriftart in Punkten ermittelt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Legen Sie für den DocumentBuilder unterschiedliche Schriftarten fest und überprüfen Sie deren Zeilenabstand.
builder.Font.Name = "Calibri";
Assert.AreEqual(14.6484375d, builder.Font.LineSpacing);

builder.Font.Name = "Times New Roman";
Assert.AreEqual(13.798828125d, builder.Font.LineSpacing);
```

### Siehe auch

* class [Font](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
