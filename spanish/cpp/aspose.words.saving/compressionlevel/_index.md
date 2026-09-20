---
title: "Enumeración Aspose::Words::Saving::CompressionLevel"
linktitle: "CompressionLevel"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Enumeración Aspose::Words::Saving::CompressionLevel. Nivel de compresión para archivos OOXML y XPS. (Los archivos DOCX, DOTX y XPS son internamente un archivo ZIP; esta propiedad controla el nivel de compresión del archivo. Nota: el archivo FlatOpc no es un archivo ZIP, por lo tanto, esta propiedad no afecta a los archivos FlatOpc.) en C++."
type: docs
weight: 47000
url: /es/cpp/aspose.words.saving/compressionlevel/
---
## CompressionLevel enum


Nivel de compresión para archivos OOXML y XPS. (Los archivos DOCX, DOTX y XPS son internamente un archivo ZIP; esta propiedad controla el nivel de compresión del archivo. Tenga en cuenta que el archivo FlatOpc no es un archivo ZIP, por lo tanto, esta propiedad no afecta a los archivos FlatOpc.)

```cpp
enum class CompressionLevel
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Normal | 0 | Nivel de compresión normal. Nivel de compresión predeterminado utilizado por [Aspose.Words](../../aspose.words/). |
| Máximo | 1 | Nivel de compresión máximo. |
| Rápido | 2 | Nivel de compresión rápido. |
| SuperFast | 3 | Nivel de compresión Super Fast. Microsoft Word usa este nivel de compresión. |


## Ejemplos



Muestra cómo especificar el nivel de compresión a usar al guardar un documento OOXML.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Big document.docx");

// Cuando guardamos el documento en un formato OOXML, podemos crear un objeto OoxmlSaveOptions
// y luego pasarlo al método de guardado del documento para modificar cómo guardamos el documento.
// Establezca la propiedad "CompressionLevel" a "CompressionLevel.Maximum" para aplicar la compresión más fuerte y lenta.
// Establezca la propiedad "CompressionLevel" a "CompressionLevel.Normal" para aplicar
// la compresión predeterminada que Aspose.Words utiliza al guardar documentos OOXML.
// Establezca la propiedad "CompressionLevel" a "CompressionLevel.Fast" para aplicar una compresión más rápida y más débil.
// Establezca la propiedad "CompressionLevel" a "CompressionLevel.SuperFast" para aplicar
// la compresión predeterminada que Microsoft Word utiliza.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>(Aspose::Words::SaveFormat::Docx);
saveOptions->set_CompressionLevel(compressionLevel);

System::SharedPtr<System::Diagnostics::Stopwatch> st = System::Diagnostics::Stopwatch::StartNew();
doc->Save(get_ArtifactsDir() + u"OoxmlSaveOptions.DocumentCompression.docx", saveOptions);
st->Stop();

auto fileInfo = System::MakeObject<System::IO::FileInfo>(get_ArtifactsDir() + u"OoxmlSaveOptions.DocumentCompression.docx");

std::cout << System::String::Format(u"Saving operation done using the \"{0}\" compression level:", compressionLevel) << std::endl;
std::cout << System::String::Format(u"\tDuration:\t{0} ms", st->get_ElapsedMilliseconds()) << std::endl;
std::cout << System::String::Format(u"\tFile Size:\t{0} bytes", fileInfo->get_Length()) << std::endl;
```


Muestra cómo controlar el nivel de compresión al guardar un documento en formato XPS.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Sample document for XPS compression test.");

// Cree un objeto XpsSaveOptions y establezca el nivel de compresión.
auto options = System::MakeObject<Aspose::Words::Saving::XpsSaveOptions>();
options->set_CompressionLevel(Aspose::Words::Saving::CompressionLevel::Maximum);

doc->Save(get_ArtifactsDir() + u"XpsSaveOptions.CompressionLevelXps.xps", options);
```

## Ver también

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
