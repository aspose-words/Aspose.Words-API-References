---
title: "Aspose::Words::Drawing::ImageType enum"
linktitle: "ImageType"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::ImageType enum. Spécifie le type (format) d'une image dans un document Microsoft Word en C++."
type: docs
weight: 28000
url: /fr/cpp/aspose.words.drawing/imagetype/
---
## ImageType enum


Spécifie le type (format) d'une image dans un document Microsoft Word.

```cpp
enum class ImageType
```

### Valeurs

| Nom | Valeur | Description |
| --- | --- | --- |
| NoImage | 0 | Il n'y a pas de données d'image. |
| Inconnu | 1 | Un type d'image inconnu ou un type d'image qui ne peut pas être stocké directement dans un document Microsoft Word. |
| Emf | 2 | Metafile Windows amélioré. |
| Wmf | 3 | Windows Metafile. |
| Pict | 4 | Macintosh PICT. Une image existante sera conservée dans un document, mais l’insertion de nouvelles images PICT dans un document n’est pas prise en charge. |
| Jpeg | 5 | JPEG JFIF. |
| Png | 6 | Portable Network Graphics. |
| Bmp | 7 | Windows Bitmap. |
| Eps | 8 | Encapsulated PostScript. |
| WebP | 9 | WebP. |
| Gif | 10 | GIF. |


## Exemples



Montre comment ajouter une image à une forme et vérifier son type.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> imgShape = builder->InsertImage(get_ImageDir() + u"Logo.jpg");
ASSERT_EQ(Aspose::Words::Drawing::ImageType::Jpeg, imgShape->get_ImageData()->get_ImageType());
```

## Voir aussi

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
