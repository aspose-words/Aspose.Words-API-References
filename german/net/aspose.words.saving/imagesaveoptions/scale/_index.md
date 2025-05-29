---
title: ImageSaveOptions.Scale
linktitle: Scale
articleTitle: Scale
second_title: Aspose.Words für .NET
description: Entdecken Sie die Skalierungseigenschaft von ImageSaveOptions, um den Zoomfaktor Ihrer Bilder mühelos anzupassen und so die Qualität und Anpassungsfähigkeit zu verbessern.
type: docs
weight: 150
url: /de/net/aspose.words.saving/imagesaveoptions/scale/
---
## ImageSaveOptions.Scale property

Ruft den Zoomfaktor für die generierten Bilder ab oder legt ihn fest.

```csharp
public float Scale { get; set; }
```

## Bemerkungen

Der Standardwert ist 1,0. Der Wert muss größer als 0 sein.

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

Zeigt, wie das Bild bearbeitet wird, während Aspose.Words ein Dokument in eins konvertiert.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
builder.Writeln("Hello world!");
builder.InsertImage(ImageDir + "Logo.jpg");

// Wenn wir das Dokument als Bild speichern, können wir ein SaveOptions-Objekt übergeben an
// Bearbeiten Sie das Bild, während der Speichervorgang es rendert.
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png)
{
    // Wir können diese Eigenschaften anpassen, um die Helligkeit und den Kontrast des Bildes zu ändern.
    // Beide liegen auf einer Skala von 0 bis 1 und sind standardmäßig auf 0,5 eingestellt.
    ImageBrightness = 0.3f,
    ImageContrast = 0.7f,

    // Mit diesen Eigenschaften können wir die horizontale und vertikale Auflösung anpassen.
    // Dies wirkt sich auf die Abmessungen des Bildes aus.
    // Der Standardwert für diese Eigenschaften ist 96,0, für eine Auflösung von 96 dpi.
    HorizontalResolution = 72f,
    VerticalResolution = 72f,

    // Mit dieser Eigenschaft können wir das Bild skalieren. Der Standardwert ist 1,0, was einer Skalierung von 100 % entspricht.
    // Wir können diese Eigenschaft verwenden, um alle Änderungen der Bildabmessungen zu negieren, die durch eine Änderung der Auflösung verursacht würden.
    Scale = 96f / 72f
};

doc.Save(ArtifactsDir + "ImageSaveOptions.EditImage.png", options);
```

### Siehe auch

* class [ImageSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
