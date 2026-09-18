---
title: "Aspose::Words::WatermarkType Enum"
linktitle: "WatermarkType"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::WatermarkType Enum. Gibt den Wasserzeichen-Typ in C++ an."
type: docs
weight: 131000
url: /de/cpp/aspose.words/watermarktype/
---
## WatermarkType enum


Gibt den Typ des Wasserzeichens an.

```cpp
enum class WatermarkType
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Text | 0 | Gibt an, dass der Text als Wasserzeichen verwendet wird. Ein solches Wasserzeichen entspricht einem WordArt-Objekt. |
| Image | 1 | Gibt an, dass das Bild als Wasserzeichen verwendet wird. Ein solches Wasserzeichen entspricht einer Form mit Bild. |
| Keine | 2 | Gibt an, dass das Wasserzeichen nicht gesetzt ist. |


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
