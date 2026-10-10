---
title: "Metodo Aspose::Words::ImageWatermarkOptions::get_Scale"
linktitle: "get_Scale"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::ImageWatermarkOptions::get_Scale. Ottiene o imposta il fattore di scala espresso come frazione dell'immagine. Il valore predefinito è 0 - auto in C++."
type: docs
weight: 4000
url: /it/cpp/aspose.words/imagewatermarkoptions/get_scale/
---
## ImageWatermarkOptions::get_Scale method


Ottiene o imposta il fattore di scala espresso come frazione dell'immagine. Il valore predefinito è 0 - automatico.

```cpp
double Aspose::Words::ImageWatermarkOptions::get_Scale() const
```

## Note


I valori validi vanno da 0 a 65,5 inclusi.

La scala automatica significa che il watermark verrà scalato alla sua larghezza massima e altezza massima rispetto ai margini della pagina.

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
