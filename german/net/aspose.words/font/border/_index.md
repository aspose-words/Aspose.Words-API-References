---
title: Font.Border
linktitle: Border
articleTitle: Border
second_title: Aspose.Words für .NET
description: Font Border eigendom. Gibt a zurückBorder Objekt das den Rahmen für die Schriftart angibt in C#.
type: docs
weight: 60
url: /de/net/aspose.words/font/border/
---
## Font.Border property

Gibt a zurück[`Border`](../../border/) Objekt, das den Rahmen für die Schriftart angibt.

```csharp
public Border Border { get; }
```

## Beispiele

Zeigt, wie man eine von einem Rahmen umgebene Zeichenfolge in ein Dokument einfügt.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Border.Color = Color.Green;
builder.Font.Border.LineWidth = 2.5d;
builder.Font.Border.LineStyle = LineStyle.DashDotStroker;

builder.Write("Text surrounded by green border.");

doc.Save(ArtifactsDir + "Border.FontBorder.docx");
```

### Siehe auch

* class [Border](../../border/)
* class [Font](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
