---
title: "Aspose::Words::Watermark::SetText Methode"
linktitle: "SetText"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Watermark::SetText Methode. Fügt ein Text-Wasserzeichen in das Dokument in C++ ein."
type: docs
weight: 7000
url: /de/cpp/aspose.words/watermark/settext/
---
## Watermark::SetText(const System::String\&) method


Fügt ein Textwasserzeichen in das Dokument ein.

```cpp
void Aspose::Words::Watermark::SetText(const System::String &text)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Text | const System::String\& | Text, der als Wasserzeichen angezeigt wird. |

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
## Watermark::SetText(const System::String\&, const System::SharedPtr\<Aspose::Words::TextWatermarkOptions\>\&) method


Fügt ein Textwasserzeichen in das Dokument ein.

```cpp
void Aspose::Words::Watermark::SetText(const System::String &text, const System::SharedPtr<Aspose::Words::TextWatermarkOptions> &options)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Text | const System::String\& | Text, der als Wasserzeichen angezeigt wird. |
| options | const System::SharedPtr\<Aspose::Words::TextWatermarkOptions\>\& | Definiert zusätzliche Optionen für das Text-Wasserzeichen. |

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

* Class [TextWatermarkOptions](../../textwatermarkoptions/)
* Class [Watermark](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
