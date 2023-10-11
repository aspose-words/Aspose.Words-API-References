---
title: OfficeMath.GetMathRenderer
second_title: Aspose.Words für .NET-API-Referenz
description: OfficeMath methode. Erstellt ein Objekt und gibt es zurück das zum Rendern dieser Gleichung in ein Bild verwendet werden kann.
type: docs
weight: 90
url: /de/net/aspose.words.math/officemath/getmathrenderer/
---
## OfficeMath.GetMathRenderer method

Erstellt ein Objekt und gibt es zurück, das zum Rendern dieser Gleichung in ein Bild verwendet werden kann.

```csharp
public OfficeMathRenderer GetMathRenderer()
```

### Rückgabewert

Das Renderer-Objekt für diese Gleichung.

### Bemerkungen

Diese Methode ruft lediglich die auf[`OfficeMathRenderer`](../../../aspose.words.rendering/officemathrenderer/) Konstruktor und übergibt dieses Objekt als Parameter.

### Beispiele

Zeigt, wie ein Office Math-Objekt in eine Bilddatei im lokalen Dateisystem gerendert wird.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

OfficeMath math = (OfficeMath)doc.GetChild(NodeType.OfficeMath, 0, true);

// Erstellen Sie ein „ImageSaveOptions“-Objekt, um es zur Änderung an die „Save“-Methode des Knotenrenderers zu übergeben
// wie der OfficeMath-Knoten in ein Bild gerendert wird.
ImageSaveOptions saveOptions = new ImageSaveOptions(SaveFormat.Png);

// Setzen Sie die Eigenschaft „Scale“ auf 5, um das Objekt auf das Fünffache seiner ursprünglichen Größe darzustellen.
saveOptions.Scale = 5;

math.GetMathRenderer().Save(ArtifactsDir + "Shape.RenderOfficeMath.png", saveOptions);
```

### Siehe auch

* class [OfficeMathRenderer](../../../aspose.words.rendering/officemathrenderer/)
* class [OfficeMath](../)
* namensraum [Aspose.Words.Math](../../officemath/)
* Montage [Aspose.Words](../../../)


