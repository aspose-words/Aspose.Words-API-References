---
title: "Aspose::Words::Drawing::ImageType enum"
linktitle: "ImageType"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::ImageType enum. Specifica il tipo (formato) di un'immagine in un documento Microsoft Word in C++."
type: docs
weight: 28000
url: /it/cpp/aspose.words.drawing/imagetype/
---
## ImageType enum


Specifica il tipo (formato) di un'immagine in un documento Microsoft Word.

```cpp
enum class ImageType
```

### Valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| NoImage | 0 | Non ci sono dati dell'immagine. |
| Sconosciuto | 1 | Un tipo di immagine sconosciuto o un tipo di immagine che non può essere memorizzato direttamente all'interno di un documento Microsoft Word. |
| Emf | 2 | Metafile migliorato di Windows. |
| Wmf | 3 | Metafile di Windows. |
| Pict | 4 | Macintosh PICT. Un'immagine esistente verrà conservata in un documento, ma l'inserimento di nuove immagini PICT in un documento non è supportato. |
| Jpeg | 5 | JPEG JFIF. |
| Png | 6 | Portable Network Graphics. |
| Bmp | 7 | Bitmap di Windows. |
| Eps | 8 | PostScript incapsulato. |
| WebP | 9 | WebP. |
| Gif | 10 | GIF. |


## Esempi



Mostra come aggiungere un'immagine a una forma e controllarne il tipo.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> imgShape = builder->InsertImage(get_ImageDir() + u"Logo.jpg");
ASSERT_EQ(Aspose::Words::Drawing::ImageType::Jpeg, imgShape->get_ImageData()->get_ImageType());
```

## Vedi anche

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
