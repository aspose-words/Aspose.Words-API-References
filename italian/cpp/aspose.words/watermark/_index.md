---
title: "Aspose::Words::Watermark classe"
linktitle: "Filigrana"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Watermark classe. Rappresenta la classe per lavorare con la filigrana del documento. Per saperne di più, visita l'articolo di documentazione in C++."
type: docs
weight: 76000
url: /it/cpp/aspose.words/watermark/
---
## Watermark class


Rappresenta la classe per lavorare con la filigrana del documento. Per saperne di più, visita l'articolo di documentazione [Working with Watermark](https://docs.aspose.com/words/cpp/working-with-watermark/).

```cpp
class Watermark : public System::Object
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [get_Type](./get_type/)() | Ottiene il tipo di filigrana. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)() | Rimuove la filigrana. |
| [SetImage](./setimage/)(const System::SharedPtr\<System::Drawing::Image\>\&) | Aggiunge una filigrana immagine al documento. |
| [SetImage](./setimage/)(const System::SharedPtr\<System::Drawing::Image\>\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) | Aggiunge una filigrana immagine al documento. |
| [SetImage](./setimage/)(const System::String\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) | Aggiunge una filigrana immagine al documento. |
| [SetImage](./setimage/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) | Aggiunge una filigrana immagine al documento. |
| [SetText](./settext/)(const System::String\&) | Aggiunge una filigrana di testo al documento. |
| [SetText](./settext/)(const System::String\&, const System::SharedPtr\<Aspose::Words::TextWatermarkOptions\>\&) | Aggiunge una filigrana di testo al documento. |
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
