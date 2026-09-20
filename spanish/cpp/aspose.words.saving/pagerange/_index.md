---
title: "Clase Aspose::Words::Saving::PageRange"
linktitle: "PageRange"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Clase Aspose::Words::Saving::PageRange. Representa un rango continuo de páginas. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 18000
url: /es/cpp/aspose.words.saving/pagerange/
---
## PageRange class


Representa un rango continuo de páginas. Para obtener más información, visite el artículo de documentación [Programación con documentos](https://docs.aspose.com/words/cpp/programming-with-documents/).

```cpp
class PageRange : public System::Object
```

## Métodos

| Método | Descripción |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [PageRange](./pagerange/)(int32_t, int32_t) | Crea un nuevo objeto de rango de página. |
| static [Type](./type/)() |  |

## Ejemplos



Muestra cómo extraer páginas basándose en rangos de página exactos.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Images.docx");

auto imageOptions = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Tiff);
auto pageSet = System::MakeObject<Aspose::Words::Saving::PageSet>(System::MakeArray<System::SharedPtr<Aspose::Words::Saving::PageRange>>({System::MakeObject<Aspose::Words::Saving::PageRange>(1, 1), System::MakeObject<Aspose::Words::Saving::PageRange>(2, 3), System::MakeObject<Aspose::Words::Saving::PageRange>(1, 3), System::MakeObject<Aspose::Words::Saving::PageRange>(2, 4), System::MakeObject<Aspose::Words::Saving::PageRange>(1, 1)}));

imageOptions->set_PageSet(pageSet);
doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.ExportVariousPageRanges.tiff", imageOptions);
```

## Ver también

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
