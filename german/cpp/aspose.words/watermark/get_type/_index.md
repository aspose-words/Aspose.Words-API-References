---
title: "Aspose::Words::Watermark::get_Type Methode"
linktitle: "get_Type"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Watermark::get_Type Methode. Gibt den Wasserzeichentyp in C++ zurück."
type: docs
weight: 2000
url: /de/cpp/aspose.words/watermark/get_type/
---
## Watermark::get_Type method


Ruft den Wasserzeichentyp ab.

```cpp
Aspose::Words::WatermarkType Aspose::Words::Watermark::get_Type()
```


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

* Enum [WatermarkType](../../watermarktype/)
* Class [Watermark](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
