---
title: "Aspose::Words::Watermark::Remove Methode"
linktitle: "Remove"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Watermark::Remove Methode. Entfernt das Wasserzeichen in C++."
type: docs
weight: 5000
url: /de/cpp/aspose.words/watermark/remove/
---
## Watermark::Remove method


Entfernt das Wasserzeichen.

```cpp
void Aspose::Words::Watermark::Remove()
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

* Class [Watermark](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
