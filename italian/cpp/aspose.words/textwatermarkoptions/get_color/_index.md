---
title: "Metodo Aspose::Words::TextWatermarkOptions::get_Color"
linktitle: "get_Color"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::TextWatermarkOptions::get_Color. Ottiene o imposta il colore del carattere. Il valore predefinito è Silver in C++."
type: docs
weight: 3000
url: /it/cpp/aspose.words/textwatermarkoptions/get_color/
---
## TextWatermarkOptions::get_Color method


Ottiene o imposta il colore del carattere. Il valore predefinito è **Silver**.

```cpp
System::Drawing::Color Aspose::Words::TextWatermarkOptions::get_Color() const
```


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

* Class [TextWatermarkOptions](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
