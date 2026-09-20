---
title: "Aspose::Words::Saving::OoxmlSaveOptions::get_CompressionLevel método"
linktitle: "get_CompressionLevel"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Saving::OoxmlSaveOptions::get_CompressionLevel método. Especifica el nivel de compresión utilizado para guardar el documento. El valor predeterminado es Normal en C++."
type: docs
weight: 4000
url: /es/cpp/aspose.words.saving/ooxmlsaveoptions/get_compressionlevel/
---
## OoxmlSaveOptions::get_CompressionLevel method


Especifica el nivel de compresión utilizado para guardar el documento. El valor predeterminado es [Normal](../../compressionlevel/).

```cpp
Aspose::Words::Saving::CompressionLevel Aspose::Words::Saving::OoxmlSaveOptions::get_CompressionLevel() const
```


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

## Ver también

* Enum [CompressionLevel](../../compressionlevel/)
* Class [OoxmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
