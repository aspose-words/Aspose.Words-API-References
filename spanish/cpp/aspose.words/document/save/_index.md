---
title: "Método Aspose::Words::Document::Save"
linktitle: "Save"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Document::Save. Guarda el documento en un flujo usando el formato especificado en C++."
type: docs
weight: 72000
url: /es/cpp/aspose.words/document/save/
---
## Document::Save(const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat) method


Guarda el documento en un flujo usando el formato especificado.

```cpp
System::SharedPtr<Aspose::Words::Saving::SaveOutputParameters> Aspose::Words::Document::Save(const System::SharedPtr<System::IO::Stream> &stream, Aspose::Words::SaveFormat saveFormat)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| flujo | const System::SharedPtr\<System::IO::Stream\>\& | Flujo donde guardar el documento. |
| saveFormat | Aspose::Words::SaveFormat | El formato en el que guardar el documento. |

### ReturnValue

Información adicional que puede usar opcionalmente.

## Ejemplos



Muestra cómo guardar un documento en una imagen mediante un flujo, y luego leer la imagen desde ese flujo.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Name(u"Times New Roman");
builder->get_Font()->set_Size(24);
builder->Writeln(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

builder->InsertImage(get_ImageDir() + u"Logo.jpg");
```


Muestra cómo guardar un documento en un flujo.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

{
    auto dstStream = System::MakeObject<System::IO::MemoryStream>();
    doc->Save(dstStream, Aspose::Words::SaveFormat::Docx);

    // Verifique que el flujo contenga el documento.
    ASSERT_EQ(u"Hello World!\r\rHello Word!\r\r\rHello World!", System::MakeObject<Aspose::Words::Document>(dstStream)->GetText().Trim());
}
```

## Ver también

* Class [SaveOutputParameters](../../../aspose.words.saving/saveoutputparameters/)
* Enum [SaveFormat](../../saveformat/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::Save(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) method


Guarda el documento en un flujo usando las opciones de guardado especificadas.

```cpp
System::SharedPtr<Aspose::Words::Saving::SaveOutputParameters> Aspose::Words::Document::Save(const System::SharedPtr<System::IO::Stream> &stream, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| flujo | const System::SharedPtr\<System::IO::Stream\>\& | Flujo donde guardar el documento. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Especifica las opciones que controlan cómo se guarda el documento. Puede ser **null**. Si es **null**, el documento se guardará en el formato binario DOC. |

### ReturnValue

Información adicional que puede usar opcionalmente.

## Ver también

* Class [SaveOutputParameters](../../../aspose.words.saving/saveoutputparameters/)
* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::Save(const System::String\&) method


Guarda el documento en un archivo. Determina automáticamente el formato de guardado a partir de la extensión.

```cpp
System::SharedPtr<Aspose::Words::Saving::SaveOutputParameters> Aspose::Words::Document::Save(const System::String &fileName)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| fileName | const System::String\& | El nombre del documento. Si ya existe un documento con el nombre de archivo especificado, el documento existente se sobrescribe. |

### ReturnValue

Información adicional que puede usar opcionalmente.

## Ejemplos



Muestra cómo abrir un documento y convertirlo a .PDF.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

doc->Save(get_ArtifactsDir() + u"Document.ConvertToPdf.pdf");
```

## Ver también

* Class [SaveOutputParameters](../../../aspose.words.saving/saveoutputparameters/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::Save(const System::String\&, Aspose::Words::SaveFormat) method


Guarda el documento en un archivo en el formato especificado.

```cpp
System::SharedPtr<Aspose::Words::Saving::SaveOutputParameters> Aspose::Words::Document::Save(const System::String &fileName, Aspose::Words::SaveFormat saveFormat)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| fileName | const System::String\& | El nombre del documento. Si ya existe un documento con el nombre de archivo especificado, el documento existente se sobrescribe. |
| saveFormat | Aspose::Words::SaveFormat | El formato en el que guardar el documento. |

### ReturnValue

Información adicional que puede usar opcionalmente.

## Ejemplos



Muestra cómo convertir de formato DOCX a HTML.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

doc->Save(get_ArtifactsDir() + u"Document.ConvertToHtml.html", Aspose::Words::SaveFormat::Html);
```

## Ver también

* Class [SaveOutputParameters](../../../aspose.words.saving/saveoutputparameters/)
* Enum [SaveFormat](../../saveformat/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::Save(const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) method


Guarda el documento en un archivo usando las opciones de guardado especificadas.

```cpp
System::SharedPtr<Aspose::Words::Saving::SaveOutputParameters> Aspose::Words::Document::Save(const System::String &fileName, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| fileName | const System::String\& | El nombre del documento. Si ya existe un documento con el nombre de archivo especificado, el documento existente se sobrescribe. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Especifica las opciones que controlan cómo se guarda el documento. Puede ser **null**. |

### ReturnValue

Información adicional que puede usar opcionalmente.

## Ejemplos



Muestra cómo mejorar la calidad de un documento renderizado con SaveOptions.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Size(60);
builder->Writeln(u"Some text.");

System::SharedPtr<Aspose::Words::Saving::SaveOptions> options = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Jpeg);

doc->Save(get_ArtifactsDir() + u"Document.ImageSaveOptions.Default.jpg", options);

options->set_UseAntiAliasing(true);
options->set_UseHighQualityRendering(true);

doc->Save(get_ArtifactsDir() + u"Document.ImageSaveOptions.HighQuality.jpg", options);
```


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


Muestra cómo renderizar cada página de un documento a una imagen TIFF separada.
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
auto options = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Tiff);

for (int32_t i = 0; i < doc->get_PageCount(); i++)
{
    // Establezca la propiedad "PageSet" al número de la primera página desde
    // desde la cual comenzar a renderizar el documento.
    options->set_PageSet(System::MakeObject<Aspose::Words::Saving::PageSet>(i));
    // Exportar página a 2325x5325 píxeles y 600 ppp.
    options->set_Resolution(600.0f);
    options->set_ImageSize(System::Drawing::Size(2325, 5325));

    doc->Save(get_ArtifactsDir() + System::String::Format(u"ImageSaveOptions.PageByPage.{0}.tiff", i + 1), options);
}
```


Muestra cómo configurar la compresión al guardar un documento como JPEG.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->InsertImage(get_ImageDir() + u"Logo.jpg");

// Cree un objeto "ImageSaveOptions" que podamos pasar al método "Save" del documento
// para modificar la forma en que ese método renderiza el documento en una imagen.
auto imageOptions = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Jpeg);
// Establezca la propiedad "JpegQuality" a "10" para usar una compresión más fuerte al renderizar el documento.
// Esto reducirá el tamaño del archivo del documento, pero la imagen mostrará artefactos de compresión más prominentes.
imageOptions->set_JpegQuality(10);
doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.JpegQuality.HighCompression.jpg", imageOptions);

// Establezca la propiedad "JpegQuality" a "100" para usar una compresión más débil al renderizar el documento.
// Esto mejorará la calidad de la imagen a costa de un mayor tamaño de archivo.
imageOptions->set_JpegQuality(100);
doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.JpegQuality.HighQuality.jpg", imageOptions);
```

## Ver también

* Class [SaveOutputParameters](../../../aspose.words.saving/saveoutputparameters/)
* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::Save(std::basic_ostream\<CharType, Traits\>\&, Aspose::Words::SaveFormat) method




```cpp
template<typename CharType,typename Traits> System::SharedPtr<Aspose::Words::Saving::SaveOutputParameters> Aspose::Words::Document::Save(std::basic_ostream<CharType, Traits> &stream, Aspose::Words::SaveFormat saveFormat)
```

## Ver también

* Class [SaveOutputParameters](../../../aspose.words.saving/saveoutputparameters/)
* Enum [SaveFormat](../../saveformat/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::Save(std::basic_ostream\<CharType, Traits\>\&, System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>) method




```cpp
template<typename CharType,typename Traits> System::SharedPtr<Aspose::Words::Saving::SaveOutputParameters> Aspose::Words::Document::Save(std::basic_ostream<CharType, Traits> &stream, System::SharedPtr<Aspose::Words::Saving::SaveOptions> saveOptions)
```

## Ver también

* Class [SaveOutputParameters](../../../aspose.words.saving/saveoutputparameters/)
* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
