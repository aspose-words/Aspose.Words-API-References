---
title: Font.Shading
linktitle: Shading
articleTitle: Shading
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft „Font Shading“, die ein Shading-Objekt für die anpassbare Schriftformatierung bereitstellt und so die visuelle Attraktivität Ihres Textes verbessert.
type: docs
weight: 330
url: /de/net/aspose.words/font/shading/
---
## Font.Shading property

Gibt einen[`Shading`](../../shading/) Objekt, das sich auf die Schattierungsformatierung für die Schriftart bezieht.

```csharp
public Shading Shading { get; }
```

## Beispiele

Zeigt, wie Schattierungen auf mit einem Dokumentgenerator erstellten Text angewendet werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Color = Color.White;

// Eine Möglichkeit, den mit unserer weißen Schriftfarbe erstellten Text sichtbar zu machen
// dient zum Anwenden eines Hintergrundschattierungseffekts.
Shading shading = builder.Font.Shading;
shading.Texture = TextureIndex.TextureDiagonalUp;
shading.BackgroundPatternColor = Color.OrangeRed;
shading.ForegroundPatternColor = Color.DarkBlue;

builder.Writeln("White text on an orange background with a two-tone texture.");

doc.Save(ArtifactsDir + "Font.Shading.docx");
```

### Siehe auch

* class [Shading](../../shading/)
* class [Font](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
