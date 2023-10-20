---
title: HtmlSaveOptions.ScaleImageToShapeSize
linktitle: ScaleImageToShapeSize
articleTitle: ScaleImageToShapeSize
second_title: Aspose.Words für .NET
description: HtmlSaveOptions ScaleImageToShapeSize eigendom. Gibt an ob Bilder beim Exportieren nach HTML MHTML oder EPUB von Aspose.Words auf die Größe der Begrenzungsform skaliert werden. Der Standardwert istWAHR  in C#.
type: docs
weight: 450
url: /de/net/aspose.words.saving/htmlsaveoptions/scaleimagetoshapesize/
---
## HtmlSaveOptions.ScaleImageToShapeSize property

Gibt an, ob Bilder beim Exportieren nach HTML, MHTML oder EPUB von Aspose.Words auf die Größe der Begrenzungsform skaliert werden. Der Standardwert ist`WAHR` .

```csharp
public bool ScaleImageToShapeSize { get; set; }
```

## Bemerkungen

Ein Bild in einem Microsoft Word-Dokument ist eine Form. Die Form hat eine Größe und das Bild hat eine eigene Größe. Die Größen sind nicht direkt miteinander verknüpft. Das Bild kann beispielsweise 1024 x 786 Pixel groß sein, , aber die Form, die dieses Bild anzeigt, kann 400 x 300 Punkte groß sein.

Um ein Bild im Browser anzuzeigen, muss es auf die Formgröße skaliert werden. Das`ScaleImageToShapeSize` Die Eigenschaft steuert, wo die Skalierung des image stattfindet: in Aspose.Words beim Export nach HTML oder im Browser beim Anzeigen des Dokuments.

Wann`ScaleImageToShapeSize` Ist`WAHR` , das Bild wird von Aspose.Words unter Verwendung einer hochwertigen Skalierung während des Exports in HTML skaliert. Wann`ScaleImageToShapeSize` ist`FALSCH`, wird das Bild in Originalgröße ausgegeben und der Browser muss es skalieren.

Im Allgemeinen führen Browser eine schnelle und qualitativ schlechte Skalierung durch. Dadurch erhalten Sie normalerweise eine bessere Anzeigequalität im Browser und eine kleinere Dateigröße`ScaleImageToShapeSize` Ist`WAHR` , , aber bessere Druckqualität und schnellere Konvertierung, wenn`ScaleImageToShapeSize` Ist`FALSCH`.

Zusätzlich zu Formen, die einzelne Rasterbilder enthalten, betrifft diese Option auch Gruppenformen, die aus Rasterbildern bestehen. Wenn`ScaleImageToShapeSize` Ist`FALSCH` und eine Gruppenform enthält Rasterbilder , deren intrinsische Auflösung höher ist als der in angegebene Wert[`ImageResolution`](../imageresolution/), Aspose.Words erhöht die Rendering-Auflösung für diese Gruppe. Dies ermöglicht eine bessere Qualität gruppierter hochauflösender -Bilder beim Speichern in HTML.

## Beispiele

Zeigt, wie die Skalierung von Bildern auf die Abmessungen ihrer übergeordneten Form beim Speichern im HTML-Format deaktiviert wird.

```csharp
Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            // Fügen Sie eine Form ein, die ein Bild enthält, und verkleinern Sie diese Form dann erheblich als das Bild.
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

            // Beim Speichern eines Dokuments, das Formen mit Bildern enthält, im HTML-Format wird eine Bilddatei im lokalen Dateisystem erstellt
            // für jede dieser Formen. Das ausgegebene HTML-Dokument verwendet <image> Tags zum Verlinken und Anzeigen dieser Bilder.
            // Wenn wir das Dokument in HTML speichern, können wir zur Bestimmung ein SaveOptions-Objekt übergeben
            // ob alle Bilder, die sich innerhalb von Formen befinden, auf die Größe ihrer Formen skaliert werden sollen.
            // Wenn Sie das Flag „ScaleImageToShapeSize“ auf „true“ setzen, wird jedes Bild verkleinert
            // auf die Größe der Form anpassen, die es enthält, sodass keine gespeicherten Bilder größer sind, als das Dokument es erfordert.
            // Wenn Sie das Flag „ScaleImageToShapeSize“ auf „false“ setzen, bleiben die Originalgrößen dieser Bilder erhalten.
            // was im Austausch für die Beibehaltung der Bildqualität mehr Platz beansprucht.
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
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
