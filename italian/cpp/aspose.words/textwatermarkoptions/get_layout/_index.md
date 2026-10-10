---
title: "Metodo Aspose::Words::TextWatermarkOptions::get_Layout"
linktitle: "get_Layout"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::TextWatermarkOptions::get_Layout. Ottiene o imposta il layout della filigrana. Il valore predefinito è Diagonal in C++."
type: docs
weight: 7000
url: /it/cpp/aspose.words/textwatermarkoptions/get_layout/
---
## TextWatermarkOptions::get_Layout method


Ottiene o imposta il layout della filigrana. Il valore predefinito è [Diagonal](../../watermarklayout/).

```cpp
Aspose::Words::WatermarkLayout Aspose::Words::TextWatermarkOptions::get_Layout() const
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

* Enum [WatermarkLayout](../../watermarklayout/)
* Class [TextWatermarkOptions](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
