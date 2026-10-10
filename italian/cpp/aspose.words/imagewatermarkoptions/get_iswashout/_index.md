---
title: "Aspose::Words::ImageWatermarkOptions::get_IsWashout metodo"
linktitle: "get_IsWashout"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::ImageWatermarkOptions::get_IsWashout metodo. Ottiene o imposta un valore booleano che è responsabile dell'effetto di sbiadimento della filigrana. Il valore predefinito è true in C++."
type: docs
weight: 3000
url: /it/cpp/aspose.words/imagewatermarkoptions/get_iswashout/
---
## ImageWatermarkOptions::get_IsWashout method


Ottiene o imposta un valore booleano responsabile dell'effetto di sbiadimento del watermark. Il valore predefinito è **true**.

```cpp
bool Aspose::Words::ImageWatermarkOptions::get_IsWashout() const
```


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

* Class [ImageWatermarkOptions](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
