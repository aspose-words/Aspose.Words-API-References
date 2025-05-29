---
title: HtmlSaveOptions.ScaleImageToShapeSize
linktitle: ScaleImageToShapeSize
articleTitle: ScaleImageToShapeSize
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie die ScaleImageToShapeSize-Eigenschaft von HtmlSaveOptions die Bildskalierung in Aspose.Words für HTML-, MHTML- oder EPUB-Exporte optimiert. Optimieren Sie Ihre Dokumente!
type: docs
weight: 470
url: /de/net/aspose.words.saving/htmlsaveoptions/scaleimagetoshapesize/
---
## HtmlSaveOptions.ScaleImageToShapeSize property

Gibt an, ob Bilder von Aspose.Words beim Exportieren in HTML, MHTML oder EPUB auf die Größe der Begrenzungsform skaliert werden. Der Standardwert ist`WAHR` .

```csharp
public bool ScaleImageToShapeSize { get; set; }
```

## Bemerkungen

Ein Bild in einem Microsoft Word-Dokument ist eine Form. Die Form hat eine Größe, und das Bild hat eine eigene Größe. Die Größen sind nicht direkt verknüpft. Beispielsweise kann das Bild 1024 x 786 Pixel groß sein, , aber die Form, die dieses Bild anzeigt, kann 400 x 300 Punkte groß sein.

Um ein Bild im Browser anzuzeigen, muss es auf die Formgröße skaliert werden. Die`ScaleImageToShapeSize` Die Eigenschaft steuert, wo die Skalierung des Bildes stattfindet: in Aspose.Words beim Export nach HTML oder im Browser bei der Anzeige des Dokuments.

Wann`ScaleImageToShapeSize` Ist`WAHR` wird das Bild beim Export nach HTML von Aspose.Words mit hochwertiger Skalierung skaliert. Wenn`ScaleImageToShapeSize` ist`FALSCH`, das Bild wird in Originalgröße ausgegeben und muss vom Browser skaliert werden.

Browser skalieren im Allgemeinen schnell und in schlechter Qualität. Dadurch erhalten Sie normalerweise eine bessere Anzeigequalität im Browser und eine kleinere Dateigröße, wenn`ScaleImageToShapeSize` Ist`WAHR` , aber bessere Druckqualität und schnellere Konvertierung wenn`ScaleImageToShapeSize` Ist`FALSCH`.

Diese Option betrifft nicht nur Formen, die einzelne Rasterbilder enthalten, sondern auch Gruppenformen, die aus Rasterbildern bestehen. Wenn`ScaleImageToShapeSize` Ist`FALSCH` und eine Gruppenform enthält Rasterbilder , deren intrinsische Auflösung höher ist als der in[`ImageResolution`](../imageresolution/)Aspose.Words erhöht die Rendering-Auflösung für diese Gruppe. Dadurch bleibt die Qualität gruppierter hochauflösender Bilder beim Speichern im HTML-Format besser erhalten.

## Beispiele

Zeigt, wie die Skalierung von Bildern auf die Abmessungen ihrer übergeordneten Form beim Speichern im HTML-Format deaktiviert wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Fügen Sie eine Form ein, die ein Bild enthält, und machen Sie diese Form dann erheblich kleiner als das Bild.
Shape imageShape = builder.InsertImage(ImageDir + "Transparent background logo.png");
imageShape.Width = 50;
imageShape.Height = 50;

// Wenn Sie ein Dokument, das Formen mit Bildern enthält, im HTML-Format speichern, wird eine Bilddatei im lokalen Dateisystem erstellt
// für jede solche Form. Das ausgegebene HTML-Dokument verwendet <image>-Tags, um auf diese Bilder zu verlinken und sie anzuzeigen.
// Wenn wir das Dokument als HTML speichern, können wir ein SaveOptions-Objekt übergeben, um zu bestimmen
// ob alle Bilder, die sich innerhalb von Formen befinden, auf die Größe ihrer Formen skaliert werden sollen.
// Wenn Sie das Flag „ScaleImageToShapeSize“ auf „true“ setzen, wird jedes Bild verkleinert
// auf die Größe der Form, die es enthält, sodass keine gespeicherten Bilder größer sind, als es das Dokument erfordert.
// Wenn Sie das Flag „ScaleImageToShapeSize“ auf „false“ setzen, bleiben die Originalgrößen dieser Bilder erhalten.
// was mehr Platz beansprucht, im Gegenzug aber die Bildqualität erhält.
HtmlSaveOptions options = new HtmlSaveOptions { ScaleImageToShapeSize = scaleImageToShapeSize };

doc.Save(ArtifactsDir + "HtmlSaveOptions.ScaleImageToShapeSize.html", options);
```

### Siehe auch

* property [ImageResolution](../imageresolution/)
* class [HtmlSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
