---
title: "Aspose::Words::Saving::PageSet::PageSet constructor"
linktitle: "PageSet"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Saving::PageSet::PageSet constructor. Crea un conjunto de páginas basado en índices de página exactos en C++."
type: docs
weight: 5000
url: /es/cpp/aspose.words.saving/pageset/pageset/
---
## PageSet::PageSet(const System::ArrayPtr\<int32_t\>\&) constructor


Crea un conjunto de páginas basado en índices de página exactos.

```cpp
Aspose::Words::Saving::PageSet::PageSet(const System::ArrayPtr<int32_t> &pages)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| páginas | const System::ArrayPtr\<int32_t\>\& | Índices basados en cero de las páginas. |

## Ejemplos



Muestra cómo extraer páginas basándose en índices de página exactos.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Agrega cinco páginas al documento.
for (int32_t i = 1; i < 6; i++)
{
    builder->Write(System::String(u"Page ") + i);
    builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
}

// Crea un objeto "XpsSaveOptions", que podemos pasar al método "Save" del documento
// para modificar cómo ese método convierte el documento a .XPS.
auto xpsOptions = System::MakeObject<Aspose::Words::Saving::XpsSaveOptions>();

// Utiliza la propiedad "PageSet" para seleccionar un conjunto de páginas del documento que se guardarán en la salida XPS.
// En este caso, elegiremos, mediante un índice basado en cero, solo tres páginas: página 1, página 2 y página 4.
xpsOptions->set_PageSet(System::MakeObject<Aspose::Words::Saving::PageSet>(System::MakeArray<int32_t>({0, 1, 3})));

doc->Save(get_ArtifactsDir() + u"XpsSaveOptions.ExportExactPages.xps", xpsOptions);
```

## Ver también

* Class [PageSet](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
## PageSet::PageSet(const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Saving::PageRange\>\>\&) constructor


Crea un conjunto de páginas basado en rangos.

```cpp
Aspose::Words::Saving::PageSet::PageSet(const System::ArrayPtr<System::SharedPtr<Aspose::Words::Saving::PageRange>> &ranges)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| rangos | const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Saving::PageRange\>\>\& | Matriz de rangos de páginas. |

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

* Class [PageRange](../../pagerange/)
* Class [PageSet](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
## PageSet::PageSet(int32_t) constructor


Crea un conjunto de una página basado en un índice de página exacto.

```cpp
Aspose::Words::Saving::PageSet::PageSet(int32_t page)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| página | int32_t | Índice basado en cero de la página. |

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

* Class [PageSet](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
