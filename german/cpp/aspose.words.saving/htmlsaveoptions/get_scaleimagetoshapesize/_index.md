---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ScaleImageToShapeSize Methode"
linktitle: "get_ScaleImageToShapeSize"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ScaleImageToShapeSize Methode. Gibt an, ob Bilder von Aspose.Words auf die Begrenzungsformgröße skaliert werden, wenn sie nach HTML, MHTML oder EPUB exportiert werden. Der Standardwert ist true in C++."
type: docs
weight: 46000
url: /de/cpp/aspose.words.saving/htmlsaveoptions/get_scaleimagetoshapesize/
---
## HtmlSaveOptions::get_ScaleImageToShapeSize method


Gibt an, ob Bilder von Aspose.Words beim Exportieren nach HTML, MHTML oder EPUB auf die Größe der umgebenden Form skaliert werden. Standardwert ist **true**.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ScaleImageToShapeSize() const
```

## Hinweise


Ein Bild in einem Microsoft‑Word‑Dokument ist eine Form. Die Form hat eine Größe und das Bild hat seine eigene Größe. Die Größen sind nicht direkt miteinander verknüpft. Zum Beispiel kann das Bild 1024 × 786 Pixel groß sein, aber die Form, die dieses Bild anzeigt, kann 400 × 300 Punkte groß sein.

Um ein Bild im Browser anzuzeigen, muss es auf die Formgröße skaliert werden. Die Eigenschaft [ScaleImageToShapeSize](./) steuert, wo die Skalierung des Bildes erfolgt: in Aspose.Words beim Export nach HTML oder im Browser bei der Anzeige des Dokuments.

Wenn [ScaleImageToShapeSize](./) **true** ist, wird das Bild von [Aspose.Words](../../../aspose.words/) mit hochwertiger Skalierung beim Export nach HTML skaliert. Wenn [ScaleImageToShapeSize](./) **false** ist, wird das Bild in seiner Originalgröße ausgegeben und der Browser muss es skalieren.

Im Allgemeinen führen Browser eine schnelle, aber qualitativ schlechte Skalierung durch. Infolgedessen erhalten Sie normalerweise eine bessere Anzeigequalität im Browser und eine kleinere Dateigröße, wenn [ScaleImageToShapeSize](./) **true** ist, aber eine bessere Druckqualität und schnellere Konvertierung, wenn [ScaleImageToShapeSize](./) **false** ist.

Zusätzlich zu Formen, die einzelne Rasterbilder enthalten, wirkt sich diese Option auch auf Gruppformen aus, die aus Rasterbildern bestehen. Wenn [ScaleImageToShapeSize](./) **false** ist und eine Gruppform Rasterbilder enthält, deren intrinsische Auflösung höher ist als der in [ImageResolution](../get_imageresolution/) angegebene Wert, erhöht Aspose.Words die Renderauflösung für diese Gruppe. Dadurch lässt sich die Qualität von gruppierten hochauflösenden Bildern beim Speichern nach HTML besser erhalten.

## Siehe auch

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
