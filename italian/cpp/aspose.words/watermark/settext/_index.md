---
title: "Metodo Aspose::Words::Watermark::SetText"
linktitle: "SetText"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Watermark::SetText. Aggiunge una filigrana di testo al documento in C++."
type: docs
weight: 7000
url: /it/cpp/aspose.words/watermark/settext/
---
## Watermark::SetText(const System::String\&) method


Aggiunge una filigrana di testo al documento.

```cpp
void Aspose::Words::Watermark::SetText(const System::String &text)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| testo | const System::String\& | Testo visualizzato come filigrana. |

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

* Class [Watermark](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Watermark::SetText(const System::String\&, const System::SharedPtr\<Aspose::Words::TextWatermarkOptions\>\&) method


Aggiunge una filigrana di testo al documento.

```cpp
void Aspose::Words::Watermark::SetText(const System::String &text, const System::SharedPtr<Aspose::Words::TextWatermarkOptions> &options)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| testo | const System::String\& | Testo visualizzato come filigrana. |
| opzioni | const System::SharedPtr\<Aspose::Words::TextWatermarkOptions\>\& | Definisce opzioni aggiuntive per la filigrana di testo. |

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

* Class [TextWatermarkOptions](../../textwatermarkoptions/)
* Class [Watermark](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
