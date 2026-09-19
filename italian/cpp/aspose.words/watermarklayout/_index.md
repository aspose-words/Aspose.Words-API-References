---
title: "Aspose::Words::WatermarkLayout enum"
linktitle: "WatermarkLayout"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::WatermarkLayout enum. Definisce il layout della filigrana rispetto al centro della filigrana in C++."
type: docs
weight: 130000
url: /it/cpp/aspose.words/watermarklayout/
---
## WatermarkLayout enum


Definisce il layout della filigrana rispetto al centro della filigrana.

```cpp
enum class WatermarkLayout
```

### Valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Orizzontale | 0 | Layout della filigrana orizzontale. Corrisponde a 0 gradi di rotazione. |
| Diagonale | 315 | Layout della filigrana diagonale. Corrisponde a 315 gradi di rotazione. |


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
