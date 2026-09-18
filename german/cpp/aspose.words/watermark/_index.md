---
title: "Aspose::Words::Watermark Klasse"
linktitle: "Wasserzeichen"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Watermark Klasse. Stellt eine Klasse zum Arbeiten mit Dokumentenwasserzeichen dar. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 76000
url: /de/cpp/aspose.words/watermark/
---
## Watermark class


Stellt eine Klasse zum Arbeiten mit Dokumentwasserzeichen dar. Weitere Informationen finden Sie im Dokumentationsartikel [Working with Watermark](https://docs.aspose.com/words/cpp/working-with-watermark/).

```cpp
class Watermark : public System::Object
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [get_Type](./get_type/)() | Ruft den Wasserzeichentyp ab. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)() | Entfernt das Wasserzeichen. |
| [SetImage](./setimage/)(const System::SharedPtr\<System::Drawing::Image\>\&) | Fügt ein Bildwasserzeichen in das Dokument ein. |
| [SetImage](./setimage/)(const System::SharedPtr\<System::Drawing::Image\>\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) | Fügt ein Bildwasserzeichen in das Dokument ein. |
| [SetImage](./setimage/)(const System::String\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) | Fügt ein Bildwasserzeichen in das Dokument ein. |
| [SetImage](./setimage/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) | Fügt ein Bildwasserzeichen in das Dokument ein. |
| [SetText](./settext/)(const System::String\&) | Fügt ein Textwasserzeichen in das Dokument ein. |
| [SetText](./settext/)(const System::String\&, const System::SharedPtr\<Aspose::Words::TextWatermarkOptions\>\&) | Fügt ein Textwasserzeichen in das Dokument ein. |
| static [Type](./type/)() |  |

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
