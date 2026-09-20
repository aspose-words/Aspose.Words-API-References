---
title: "Aspose::Words::Saving::PageRange::PageRange constructor"
linktitle: "PageRange"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Saving::PageRange::PageRange constructor. Crea un nuevo objeto de rango de página en C++."
type: docs
weight: 2000
url: /es/cpp/aspose.words.saving/pagerange/pagerange/
---
## PageRange::PageRange constructor


Crea un nuevo objeto de rango de página.

```cpp
Aspose::Words::Saving::PageRange::PageRange(int32_t from, int32_t to)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| desde | int32_t | El índice de página inicial basado en cero. |
| hasta | int32_t | El índice de página final basado en cero. Si supera el índice de la última página del documento, se trunca para ajustarse al documento al renderizar. |

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

* Class [PageRange](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
