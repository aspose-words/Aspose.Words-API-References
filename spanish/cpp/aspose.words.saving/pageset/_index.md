---
title: "Clase Aspose::Words::Saving::PageSet"
linktitle: "PageSet"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Clase Aspose::Words::Saving::PageSet. Describe un conjunto aleatorio de páginas. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 20000
url: /es/cpp/aspose.words.saving/pageset/
---
## PageSet class


Describe un conjunto aleatorio de páginas. Para obtener más información, visite el artículo de documentación [Programming with Documents](https://docs.aspose.com/words/cpp/programming-with-documents/).

```cpp
class PageSet : public System::Collections::Generic::IEnumerable<int32_t>
```

## Métodos

| Método | Descripción |
| --- | --- |
| static [get_All](./get_all/)() | Obtiene un conjunto con todas las páginas del documento en su orden original. |
| static [get_Even](./get_even/)() | Obtiene un conjunto con todas las páginas pares del documento en su orden original. |
| static [get_Odd](./get_odd/)() | Obtiene un conjunto con todas las páginas impares del documento en su orden original. |
| [GetEnumerator](./getenumerator/)() override |  |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [PageSet](./pageset/)(int32_t) | Crea un conjunto de una página basado en un índice de página exacto. |
| [PageSet](./pageset/)(const System::ArrayPtr\<int32_t\>\&) | Crea un conjunto de páginas basado en índices de página exactos. |
| [PageSet](./pageset/)(const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Saving::PageRange\>\>\&) | Crea un conjunto de páginas basado en rangos. |
| static [Type](./type/)() |  |

## Ejemplos



Muestra cómo renderizar una página de un documento a una imagen JPEG.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Page 1.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Page 2.");
builder->InsertImage(get_ImageDir() + u"Logo.jpg");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Page 3.");

// Cree un objeto "ImageSaveOptions" que podamos pasar al método "Save" del documento
// para modificar la forma en que ese método renderiza el documento en una imagen.
auto options = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Jpeg);
// Establezca "PageSet" en "1" para seleccionar la segunda página mediante
// el índice basado en cero desde el cual comenzar a renderizar el documento.
options->set_PageSet(System::MakeObject<Aspose::Words::Saving::PageSet>(1));

// Al guardar el documento en formato JPEG, Aspose.Words solo renderiza una página.
// Esta imagen contendrá una página a partir de la página dos,
// que será simplemente la segunda página del documento original.
doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.OnePage.jpg", options);
```

## Ver también

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
