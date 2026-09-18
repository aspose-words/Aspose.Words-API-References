---
title: "Aspose::Words::WatermarkLayout enum"
linktitle: "WatermarkLayout"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::WatermarkLayout enum. Definiert das Layout des Wasserzeichens relativ zum Mittelpunkt des Wasserzeichens in C++."
type: docs
weight: 130000
url: /de/cpp/aspose.words/watermarklayout/
---
## WatermarkLayout enum


Definiert das Layout des Wasserzeichens relativ zum Zentrum des Wasserzeichens.

```cpp
enum class WatermarkLayout
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Horizontal | 0 | Horizontales Wasserzeichen-Layout. Entspricht einer Rotation von 0 Grad. |
| Diagonal | 315 | Diagonales Wasserzeichen-Layout. Entspricht einer Drehung von 315 Grad. |


## Beispiele



Zeigt, wie ein Textwasserzeichen erstellt wird.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Fügen Sie ein Wasserzeichen als Klartext hinzu.
doc->get_Watermark()->SetText(u"Aspose Watermark");

// Wenn wir die Textformatierung bearbeiten möchten, indem wir es als Wasserzeichen verwenden,
// können wir dies tun, indem wir beim Erstellen des Wasserzeichens ein TextWatermarkOptions-Objekt übergeben.
auto textWatermarkOptions = System::MakeObject<Aspose::Words::TextWatermarkOptions>();
textWatermarkOptions->set_FontFamily(u"Arial");
textWatermarkOptions->set_FontSize(36.0f);
textWatermarkOptions->set_Color(System::Drawing::Color::get_Black());
textWatermarkOptions->set_Layout(Aspose::Words::WatermarkLayout::Diagonal);
textWatermarkOptions->set_IsSemitrasparent(false);

doc->get_Watermark()->SetText(u"Aspose Watermark", textWatermarkOptions);

doc->Save(get_ArtifactsDir() + u"Document.TextWatermark.docx");

// Wir können ein Wasserzeichen aus einem Dokument wie folgt entfernen.
if (doc->get_Watermark()->get_Type() == Aspose::Words::WatermarkType::Text)
{
    doc->get_Watermark()->Remove();
}
```

## Siehe auch

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
