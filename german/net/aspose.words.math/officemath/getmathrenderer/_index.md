---
title: OfficeMath.GetMathRenderer
linktitle: GetMathRenderer
articleTitle: GetMathRenderer
second_title: Aspose.Words für .NET
description: Entdecken Sie die GetMathRenderer-Methode von OfficeMath, um Gleichungen mühelos in Bilder umzuwandeln und Ihre Dokumente mit klaren, professionellen Grafiken aufzuwerten.
type: docs
weight: 90
url: /de/net/aspose.words.math/officemath/getmathrenderer/
---
## OfficeMath.GetMathRenderer method

Erstellt und gibt ein Objekt zurück, mit dem diese Gleichung in ein Bild umgewandelt werden kann.

```csharp
public OfficeMathRenderer GetMathRenderer()
```

### Rückgabewert

Das Rendererobjekt für diese Gleichung.

## Bemerkungen

Diese Methode ruft lediglich die[`OfficeMathRenderer`](../../../aspose.words.rendering/officemathrenderer/) Konstruktor und übergibt dieses Objekt als Parameter.

## Beispiele

Zeigt, wie ein Office Math-Objekt in eine Bilddatei im lokalen Dateisystem gerendert wird.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

OfficeMath math = (OfficeMath)doc.GetChild(NodeType.OfficeMath, 0, true);

// Erstellen Sie ein "ImageSaveOptions"-Objekt, das Sie an die "Save"-Methode des Knoten-Renderers übergeben, um es zu ändern
// wie es den OfficeMath-Knoten in ein Bild rendert.
ImageSaveOptions saveOptions = new ImageSaveOptions(SaveFormat.Png);

// Setzen Sie die Eigenschaft „Scale“ auf 5, um das Objekt auf das Fünffache seiner Originalgröße zu rendern.
saveOptions.Scale = 5;

math.GetMathRenderer().Save(ArtifactsDir + "Shape.RenderOfficeMath.png", saveOptions);
```

### Siehe auch

* class [OfficeMathRenderer](../../../aspose.words.rendering/officemathrenderer/)
* class [OfficeMath](../)
* namensraum [Aspose.Words.Math](../../../aspose.words.math/)
* Montage [Aspose.Words](../../../)
