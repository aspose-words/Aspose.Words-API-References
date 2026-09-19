---
title: "Aspose::Words::TextWatermarkOptions classe"
linktitle: "TextWatermarkOptions"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::TextWatermarkOptions classe. Contiene le opzioni che possono essere specificate quando si aggiunge una filigrana di testo. Per saperne di più, visita l'articolo della documentazione in C++."
type: docs
weight: 72000
url: /it/cpp/aspose.words/textwatermarkoptions/
---
## TextWatermarkOptions class


Contiene le opzioni che possono essere specificate quando si aggiunge una filigrana con testo. Per saperne di più, visita l'articolo di documentazione [Working with Watermark](https://docs.aspose.com/words/cpp/working-with-watermark/).

```cpp
class TextWatermarkOptions : public System::Object
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [get_Color](./get_color/)() const | Ottiene o imposta il colore del carattere. Il valore predefinito è **Silver**. |
| [get_FontFamily](./get_fontfamily/)() const | Ottiene o imposta il nome della famiglia di caratteri. Il valore predefinito è "Calibri". |
| [get_FontSize](./get_fontsize/)() const | Ottiene o imposta la dimensione del carattere. Il valore predefinito è 0 - automatico. |
| [get_IsSemitrasparent](./get_issemitrasparent/)() const | Ottiene o imposta un valore booleano che determina l'opacità della filigrana. Il valore predefinito è **true**. |
| [get_Layout](./get_layout/)() const | Ottiene o imposta il layout della filigrana. Il valore predefinito è [Diagonal](../watermarklayout/). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Color](./set_color/)(System::Drawing::Color) | Impostatore per [Aspose::Words::TextWatermarkOptions::get_Color](./get_color/). |
| [set_FontFamily](./set_fontfamily/)(const System::String\&) | Impostatore per [Aspose::Words::TextWatermarkOptions::get_FontFamily](./get_fontfamily/). |
| [set_FontSize](./set_fontsize/)(float) | Impostatore per [Aspose::Words::TextWatermarkOptions::get_FontSize](./get_fontsize/). |
| [set_IsSemitrasparent](./set_issemitrasparent/)(bool) | Impostatore per [Aspose::Words::TextWatermarkOptions::get_IsSemitrasparent](./get_issemitrasparent/). |
| [set_Layout](./set_layout/)(Aspose::Words::WatermarkLayout) | Impostatore per [Aspose::Words::TextWatermarkOptions::get_Layout](./get_layout/). |
| [TextWatermarkOptions](./textwatermarkoptions/)() |  |
| static [Type](./type/)() |  |

## Esempi



Mostra come creare una filigrana di testo.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Aggiungi una filigrana di testo semplice.
doc->get_Watermark()->SetText(u"Aspose Watermark");

// Se desideriamo modificare la formattazione del testo usandolo come filigrana,
// possiamo farlo passando un oggetto TextWatermarkOptions durante la creazione della filigrana.
auto textWatermarkOptions = System::MakeObject<Aspose::Words::TextWatermarkOptions>();
textWatermarkOptions->set_FontFamily(u"Arial");
textWatermarkOptions->set_FontSize(36.0f);
textWatermarkOptions->set_Color(System::Drawing::Color::get_Black());
textWatermarkOptions->set_Layout(Aspose::Words::WatermarkLayout::Diagonal);
textWatermarkOptions->set_IsSemitrasparent(false);

doc->get_Watermark()->SetText(u"Aspose Watermark", textWatermarkOptions);

doc->Save(get_ArtifactsDir() + u"Document.TextWatermark.docx");

// Possiamo rimuovere una filigrana da un documento in questo modo.
if (doc->get_Watermark()->get_Type() == Aspose::Words::WatermarkType::Text)
{
    doc->get_Watermark()->Remove();
}
```

## Vedi anche

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
