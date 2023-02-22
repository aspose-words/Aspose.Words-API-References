---
title: HtmlSaveOptions.ScaleImageToShapeSize
second_title: Aspose.Words für .NET-API-Referenz
description: HtmlSaveOptions eigendom. Gibt an ob Bilder beim Exportieren nach HTML MHTML oder EPUB von Aspose.Words auf die Größe der Begrenzungsform skaliert werden. Standardwert istStimmt .
type: docs
weight: 450
url: /de/net/aspose.words.saving/htmlsaveoptions/scaleimagetoshapesize/
---
## HtmlSaveOptions.ScaleImageToShapeSize property

Gibt an, ob Bilder beim Exportieren nach HTML, MHTML oder EPUB von Aspose.Words auf die Größe der Begrenzungsform skaliert werden. Standardwert ist`Stimmt` .

```csharp
public bool ScaleImageToShapeSize { get; set; }
```

### Bemerkungen

Ein Bild in einem Microsoft Word-Dokument ist eine Form. Die Form hat eine Größe und das Bild hat seine eigene Größe. Die Größen sind nicht direkt verknüpft. Das Bild kann beispielsweise 1024 x 786 Pixel groß sein, , aber die Form, die dieses Bild anzeigt, kann 400 x 300 Punkte groß sein.

Um ein Bild im Browser anzuzeigen, muss es auf die Formgröße skaliert werden. Die`ScaleImageToShapeSize` Eigenschaft steuert, wo die Skalierung des Bildes stattfindet: in Aspose.Words beim Export nach HTML oder im Browser beim Anzeigen des Dokuments.

Wann`ScaleImageToShapeSize` ist`Stimmt` , wird das Bild von Aspose.Words skaliert, wobei während des Exports in HTML eine hochwertige Skalierung verwendet wird. Wann`ScaleImageToShapeSize` ist`FALSCH`wird das Bild in Originalgröße ausgegeben und der Browser muss es skalieren.

Im Allgemeinen skalieren Browser schnell und in schlechter Qualität. Als Ergebnis erhalten Sie normalerweise eine bessere -Anzeigequalität im Browser und eine kleinere Dateigröße, wenn`ScaleImageToShapeSize` ist`Stimmt` , , aber bessere Druckqualität und schnellere Konvertierung, wenn`ScaleImageToShapeSize` ist`FALSCH`.

### Beispiele

Zeigt, wie Sie die Skalierung von Bildern auf die Abmessungen ihrer übergeordneten Form beim Speichern in .html deaktivieren.

```csharp
Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            // Fügen Sie eine Form ein, die ein Bild enthält, und machen Sie diese Form dann erheblich kleiner als das Bild.
#if NET48 || JAVA
            Image image = Image.FromFile(ImageDir + "Transparent background logo.png");

            Assert.AreEqual(400, image.Size.Width);
            Assert.AreEqual(400, image.Size.Height);
#elif NET5_0_OR_GREATER
            SKBitmap image = SKBitmap.Decode(ImageDir + "Transparent background logo.png");

            Assert.AreEqual(400, image.Width);
            Assert.AreEqual(400, image.Height);
#endif

            Shape imageShape = builder.InsertImage(image);
            imageShape.Width = 50;
            imageShape.Height = 50;

            // Beim Speichern eines Dokuments, das Formen mit Bildern enthält, in HTML wird eine Bilddatei im lokalen Dateisystem erstellt
            // für jede solche Form. Das ausgegebene HTML-Dokument verwendet <image> Tags zum Verlinken und Anzeigen dieser Bilder.
            // Wenn wir das Dokument im HTML-Format speichern, können wir ein SaveOptions-Objekt zur Bestimmung übergeben
            // ob alle Bilder, die sich innerhalb von Formen befinden, auf die Größe ihrer Formen skaliert werden sollen.
            // Wenn Sie das Flag "ScaleImageToShapeSize" auf "true" setzen, wird jedes Bild verkleinert
            // auf die Größe der Form, die es enthält, sodass keine gespeicherten Bilder größer sind, als das Dokument es erfordert.
            // Wenn Sie das Flag "ScaleImageToShapeSize" auf "false" setzen, werden die Originalgrößen dieser Bilder beibehalten,
            // was im Austausch für die Beibehaltung der Bildqualität mehr Platz benötigt.
            HtmlSaveOptions options = new HtmlSaveOptions { ScaleImageToShapeSize = scaleImageToShapeSize };

            doc.Save(ArtifactsDir + "HtmlSaveOptions.ScaleImageToShapeSize.html", options);

            FileInfo fileInfo = new FileInfo(ArtifactsDir + "HtmlSaveOptions.ScaleImageToShapeSize.001.png");

#if NET48 || JAVA
        if (scaleImageToShapeSize)
            Assert.That(3000, Is.AtLeast(fileInfo.Length));
        else
            Assert.That(20000, Is.LessThan(fileInfo.Length));
#elif NET5_0_OR_GREATER
        if (scaleImageToShapeSize)
            Assert.That(10000, Is.AtLeast(fileInfo.Length));
        else
            Assert.That(30000, Is.LessThan(fileInfo.Length));
#endif
```

### Siehe auch

* property [ImageResolution](../imageresolution/)
* class [HtmlSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../htmlsaveoptions/)
* Montage [Aspose.Words](../../../)


