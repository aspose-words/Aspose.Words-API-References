---
title: "Aspose::Words::Saving::ImageSavingArgs class"
linktitle: "ImageSavingArgs"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Saving::ImageSavingArgs class. Fornisce dati per l'evento ImageSaving(). Per saperne di più, visita l'articolo di documentazione in C++."
type: docs
weight: 12000
url: /it/cpp/aspose.words.saving/imagesavingargs/
---
## ImageSavingArgs class


Fornisce dati per l'evento [ImageSaving()](../iimagesavingcallback/imagesaving/). Per saperne di più, visita l'articolo di documentazione [Save a Document](https://docs.aspose.com/words/cpp/save-a-document/).

```cpp
class ImageSavingArgs : public System::Object
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [get_CurrentShape](./get_currentshape/)() const | Ottiene l'oggetto [ShapeBase](../../aspose.words.drawing/shapebase/) corrispondente alla forma o al gruppo di forme che sta per essere salvato. |
| [get_Document](./get_document/)() | Ottiene l'oggetto documento che è attualmente in fase di salvataggio. |
| [get_ImageFileName](./get_imagefilename/)() const | Ottiene o imposta il nome file (senza percorso) dove l'immagine verrà salvata. |
| [get_ImageStream](./get_imagestream/)() const | Consente di specificare lo stream dove l'immagine verrà salvata. |
| [get_IsImageAvailable](./get_isimageavailable/)() const | Restituisce **true** se l'immagine corrente è disponibile per l'esportazione. |
| [get_KeepImageStreamOpen](./get_keepimagestreamopen/)() const | Specifica se Aspose.Words deve mantenere lo stream aperto o chiuderlo dopo il salvataggio di un'immagine. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_ImageFileName](./set_imagefilename/)(const System::String\&) | Setter per [Aspose::Words::Saving::ImageSavingArgs::get_ImageFileName](./get_imagefilename/). |
| [set_ImageStream](./set_imagestream/)(const System::SharedPtr\<System::IO::Stream\>\&) | Impostatore per [Aspose::Words::Saving::ImageSavingArgs::get_ImageStream](./get_imagestream/). |
| [set_ImageStream](./set_imagestream/)(std::basic_ostream\<CharType, Traits\>\&) |  |
| [set_KeepImageStreamOpen](./set_keepimagestreamopen/)(bool) | Impostatore per [Aspose::Words::Saving::ImageSavingArgs::get_KeepImageStreamOpen](./get_keepimagestreamopen/). |
| static [Type](./type/)() |  |
## Note


Per impostazione predefinita, quando Aspose.Words salva un documento in HTML, salva ogni immagine in un file separato. Aspose.Words utilizza il nome del file del documento e un numero univoco per generare un nome file unico per ogni immagine trovata nel documento.

[ImageSavingArgs](./) allows to redefine how image file names are generated or to completely circumvent saving of images into files by providing your own stream objects.

Per applicare la tua logica per generare i nomi dei file immagine, usa le proprietà [ImageFileName](./get_imagefilename/), [CurrentShape](./get_currentshape/) e [IsImageAvailable](./get_isimageavailable/).

Per salvare le immagini in stream invece che in file, usa la proprietà [ImageStream](./get_imagestream/).
## Vedi anche

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
