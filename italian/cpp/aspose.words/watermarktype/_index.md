---
title: "Aspose::Words::WatermarkType enum"
linktitle: "WatermarkType"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::WatermarkType enum. Specifica il tipo di filigrana in C++."
type: docs
weight: 131000
url: /it/cpp/aspose.words/watermarktype/
---
## WatermarkType enum


Specifica il tipo di filigrana.

```cpp
enum class WatermarkType
```

### Valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Testo | 0 | Indica che il testo verrà utilizzato come filigrana. Tale filigrana corrisponde a un oggetto WordArt. |
| Immagine | 1 | Indica che l'immagine verrà utilizzata come filigrana. Tale filigrana corrisponde a una forma con immagine. |
| None | 2 | Indica che la filigrana non è impostata. |


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
