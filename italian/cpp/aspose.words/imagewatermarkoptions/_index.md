---
title: "Aspose::Words::ImageWatermarkOptions classe"
linktitle: "ImageWatermarkOptions"
second_title: "Riferimento API Aspose.Words per C++"
description: "Classe Aspose::Words::ImageWatermarkOptions. Contiene le opzioni che possono essere specificate quando si aggiunge un watermark con immagine. Per saperne di più, visita l'articolo della documentazione in C++."
type: docs
weight: 34000
url: /it/cpp/aspose.words/imagewatermarkoptions/
---
## ImageWatermarkOptions class


Contiene le opzioni che possono essere specificate quando si aggiunge una filigrana con immagine. Per saperne di più, visita l'articolo di documentazione [Working with Watermark](https://docs.aspose.com/words/cpp/working-with-watermark/).

```cpp
class ImageWatermarkOptions : public System::Object
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [get_IsWashout](./get_iswashout/)() const | Ottiene o imposta un valore booleano responsabile dell'effetto di sbiadimento del watermark. Il valore predefinito è **true**. |
| [get_Scale](./get_scale/)() const | Ottiene o imposta il fattore di scala espresso come frazione dell'immagine. Il valore predefinito è 0 - automatico. |
| [GetType](./gettype/)() const override |  |
| [ImageWatermarkOptions](./imagewatermarkoptions/)() |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_IsWashout](./set_iswashout/)(bool) | Metodo set per [Aspose::Words::ImageWatermarkOptions::get_IsWashout](./get_iswashout/). |
| [set_Scale](./set_scale/)(double) | Metodo set per [Aspose::Words::ImageWatermarkOptions::get_Scale](./get_scale/). |
| static [Type](./type/)() |  |

## Esempi



Mostra come creare un watermark da un'immagine nel file system locale.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Modifica l'aspetto del watermark immagine con un oggetto ImageWatermarkOptions,
// quindi passalo durante la creazione di un watermark da un file immagine.
auto imageWatermarkOptions = System::MakeObject<Aspose::Words::ImageWatermarkOptions>();
imageWatermarkOptions->set_Scale(5);
imageWatermarkOptions->set_IsWashout(false);

// Abbiamo diverse opzioni per inserire un'immagine.
// Usa uno dei seguenti metodi per aggiungere un watermark immagine.
doc->get_Watermark()->SetImage(System::Drawing::Image::FromFile(get_ImageDir() + u"Logo.jpg"));

doc->get_Watermark()->SetImage(System::Drawing::Image::FromFile(get_ImageDir() + u"Logo.jpg"), imageWatermarkOptions);

doc->get_Watermark()->SetImage(get_ImageDir() + u"Logo.jpg", imageWatermarkOptions);

doc->Save(get_ArtifactsDir() + u"Document.ImageWatermark.docx");
```

## Vedi anche

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
