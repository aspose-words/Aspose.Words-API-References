---
title: ImageSaveOptions.Scale
second_title: Aspose.Words für .NET-API-Referenz
description: ImageSaveOptions eigendom. Liest oder setzt den Zoomfaktor für die generierten Bilder.
type: docs
weight: 140
url: /de/net/aspose.words.saving/imagesaveoptions/scale/
---
## ImageSaveOptions.Scale property

Liest oder setzt den Zoomfaktor für die generierten Bilder.

```csharp
public float Scale { get; set; }
```

### Bemerkungen

Der Standardwert ist 1,0. Der Wert muss größer als 0 sein.

### Beispiele

Zeigt, wie ein Office Math-Objekt in eine Bilddatei im lokalen Dateisystem gerendert wird.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

OfficeMath math = (OfficeMath)doc.GetChild(NodeType.OfficeMath, 0, true);

// Erstellen Sie ein "ImageSaveOptions"-Objekt, das an die "Save"-Methode des Node-Renderers übergeben wird, um es zu ändern
// wie es den OfficeMath-Knoten in ein Bild rendert.
ImageSaveOptions saveOptions = new ImageSaveOptions(SaveFormat.Png);

// Setzen Sie die Eigenschaft "Scale" auf 5, um das Objekt auf das Fünffache seiner ursprünglichen Größe zu rendern.
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

// Wenn wir das Dokument als Bild speichern, können wir ein SaveOptions-Objekt an übergeben
// das Bild bearbeiten, während der Speichervorgang es rendert.
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png)
{
    // Wir können diese Eigenschaften anpassen, um die Helligkeit und den Kontrast des Bildes zu ändern.
    // Beide liegen auf einer Skala von 0-1 und sind standardmäßig bei 0,5.
    ImageBrightness = 0.3f,
    ImageContrast = 0.7f,

    // Mit diesen Eigenschaften können wir die horizontale und vertikale Auflösung anpassen.
    // Dies wirkt sich auf die Abmessungen des Bildes aus.
    // Der Standardwert für diese Eigenschaften ist 96,0 für eine Auflösung von 96 dpi.
    HorizontalResolution = 72f,
    VerticalResolution = 72f,

    // Mit dieser Eigenschaft können wir das Bild skalieren. Der Standardwert ist 1,0 für eine Skalierung von 100 %.
    // Wir können diese Eigenschaft verwenden, um alle Änderungen der Bildabmessungen zu negieren, die eine Änderung der Auflösung verursachen würde.
    Scale = 96f / 72f
};

doc.Save(ArtifactsDir + "ImageSaveOptions.EditImage.png", options);
```

### Siehe auch

* class [ImageSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../imagesaveoptions/)
* Montage [Aspose.Words](../../../)


