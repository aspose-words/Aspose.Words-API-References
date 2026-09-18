---
title: "Aspose::Words::TextWatermarkOptions Klasse"
linktitle: "TextWatermarkOptions"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::TextWatermarkOptions Klasse. Enthält Optionen, die angegeben werden können, wenn ein Wasserzeichen mit Text hinzugefügt wird. Um mehr zu erfahren, besuchen Sie den Dokumentationsartikel in C++."
type: docs
weight: 72000
url: /de/cpp/aspose.words/textwatermarkoptions/
---
## TextWatermarkOptions class


Enthält Optionen, die beim Hinzufügen eines Wasserzeichens mit Text angegeben werden können. Weitere Informationen finden Sie im Dokumentationsartikel [Working with Watermark](https://docs.aspose.com/words/cpp/working-with-watermark/).

```cpp
class TextWatermarkOptions : public System::Object
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [get_Color](./get_color/)() const | Liest oder setzt die Schriftfarbe. Der Standardwert ist **Silver**. |
| [get_FontFamily](./get_fontfamily/)() const | Liest oder setzt den Namen der Schriftfamilie. Der Standardwert ist "Calibri". |
| [get_FontSize](./get_fontsize/)() const | Liest oder setzt die Schriftgröße. Der Standardwert ist 0 – automatisch. |
| [get_IsSemitrasparent](./get_issemitrasparent/)() const | Liest oder setzt einen booleschen Wert, der für die Deckkraft des Wasserzeichens verantwortlich ist. Der Standardwert ist **true**. |
| [get_Layout](./get_layout/)() const | Liest oder setzt das Layout des Wasserzeichens. Der Standardwert ist [Diagonal](../watermarklayout/). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Color](./set_color/)(System::Drawing::Color) | Setter für [Aspose::Words::TextWatermarkOptions::get_Color](./get_color/). |
| [set_FontFamily](./set_fontfamily/)(const System::String\&) | Setter für [Aspose::Words::TextWatermarkOptions::get_FontFamily](./get_fontfamily/). |
| [set_FontSize](./set_fontsize/)(float) | Setter für [Aspose::Words::TextWatermarkOptions::get_FontSize](./get_fontsize/). |
| [set_IsSemitrasparent](./set_issemitrasparent/)(bool) | Setter für [Aspose::Words::TextWatermarkOptions::get_IsSemitrasparent](./get_issemitrasparent/). |
| [set_Layout](./set_layout/)(Aspose::Words::WatermarkLayout) | Setter für [Aspose::Words::TextWatermarkOptions::get_Layout](./get_layout/). |
| [TextWatermarkOptions](./textwatermarkoptions/)() |  |
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
