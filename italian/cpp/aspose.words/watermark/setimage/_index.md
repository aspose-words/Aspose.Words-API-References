---
title: "Metodo Aspose::Words::Watermark::SetImage"
linktitle: "SetImage"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Watermark::SetImage. Aggiunge una filigrana immagine al documento in C++."
type: docs
weight: 6000
url: /it/cpp/aspose.words/watermark/setimage/
---
## Watermark::SetImage(const System::SharedPtr\<System::Drawing::Image\>\&) method


Aggiunge una filigrana immagine al documento.

```cpp
void Aspose::Words::Watermark::SetImage(const System::SharedPtr<System::Drawing::Image> &image)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| image | const System::SharedPtr\<System::Drawing::Image\>\& | Immagine visualizzata come filigrana. |

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

* Class [Watermark](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Watermark::SetImage(const System::SharedPtr\<System::Drawing::Image\>\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) method


Aggiunge una filigrana immagine al documento.

```cpp
void Aspose::Words::Watermark::SetImage(const System::SharedPtr<System::Drawing::Image> &image, const System::SharedPtr<Aspose::Words::ImageWatermarkOptions> &options)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| image | const System::SharedPtr\<System::Drawing::Image\>\& | Immagine visualizzata come filigrana. |
| opzioni | const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\& | Definisce opzioni aggiuntive per la filigrana immagine. |

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

* Class [ImageWatermarkOptions](../../imagewatermarkoptions/)
* Class [Watermark](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Watermark::SetImage(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) method


Aggiunge una filigrana immagine al documento.

```cpp
void Aspose::Words::Watermark::SetImage(const System::SharedPtr<System::IO::Stream> &imageStream, const System::SharedPtr<Aspose::Words::ImageWatermarkOptions> &options)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| imageStream | const System::SharedPtr\<System::IO::Stream\>\& | Il flusso contenente i dati dell'immagine visualizzata come filigrana. |
| opzioni | const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\& | Definisce opzioni aggiuntive per la filigrana immagine. |

## Esempi



Mostra come creare una filigrana da un flusso di immagine.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Modifica l'aspetto del watermark immagine con un oggetto ImageWatermarkOptions,
// quindi passalo durante la creazione di un watermark da un file immagine.
auto imageWatermarkOptions = System::MakeObject<Aspose::Words::ImageWatermarkOptions>();
imageWatermarkOptions->set_Scale(5);

{
    auto imageStream = System::MakeObject<System::IO::FileStream>(get_ImageDir() + u"Logo.jpg", System::IO::FileMode::Open, System::IO::FileAccess::Read);
    doc->get_Watermark()->SetImage(imageStream, imageWatermarkOptions);
}

doc->Save(get_ArtifactsDir() + u"Document.ImageWatermarkStream.docx");
```

## Vedi anche

* Class [ImageWatermarkOptions](../../imagewatermarkoptions/)
* Class [Watermark](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Watermark::SetImage(const System::String\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) method


Aggiunge una filigrana immagine al documento.

```cpp
void Aspose::Words::Watermark::SetImage(const System::String &imagePath, const System::SharedPtr<Aspose::Words::ImageWatermarkOptions> &options)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| imagePath | const System::String\& | Percorso al file immagine visualizzato come filigrana. |
| opzioni | const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\& | Definisce opzioni aggiuntive per la filigrana immagine. |

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

* Class [ImageWatermarkOptions](../../imagewatermarkoptions/)
* Class [Watermark](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
