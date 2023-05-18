---
title: Aspose::Words::Saving::CompressionLevel enum
linktitle: CompressionLevel
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::CompressionLevel enum. Compression level for OOXML files. (DOCX and DOTX files are internally a ZIP-archive, this property controls the compression level of the archive. Note, that FlatOpc file is not a ZIP-archive, therefore, this property does not affect the FlatOpc files.) in C++.'
type: docs
weight: 47000
url: /cpp/aspose.words.saving/compressionlevel/
---
## CompressionLevel enum


Compression level for OOXML files. (DOCX and DOTX files are internally a ZIP-archive, this property controls the compression level of the archive. Note, that FlatOpc file is not a ZIP-archive, therefore, this property does not affect the FlatOpc files.)

```cpp
enum class CompressionLevel
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Normal | 0 | Normal compression level. Default compression level used by [Aspose.Words](../../aspose.words/). |
| Maximum | 1 | Maximum compression level. |
| Fast | 2 | Fast compression level. |
| SuperFast | 3 | Super Fast compression level. Microsoft Word uses this compression level. |


## Examples



Shows how to specify the compression level to use while saving an OOXML document. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Big document.docx");

// When we save the document to an OOXML format, we can create an OoxmlSaveOptions object
// and then pass it to the document's saving method to modify how we save the document.
// Set the "CompressionLevel" property to "CompressionLevel.Maximum" to apply the strongest and slowest compression.
// Set the "CompressionLevel" property to "CompressionLevel.Normal" to apply
// the default compression that Aspose.Words uses while saving OOXML documents.
// Set the "CompressionLevel" property to "CompressionLevel.Fast" to apply a faster and weaker compression.
// Set the "CompressionLevel" property to "CompressionLevel.SuperFast" to apply
// the default compression that Microsoft Word uses.
auto saveOptions = MakeObject<OoxmlSaveOptions>(SaveFormat::Docx);
saveOptions->set_CompressionLevel(compressionLevel);

SharedPtr<System::Diagnostics::Stopwatch> st = System::Diagnostics::Stopwatch::StartNew();
doc->Save(ArtifactsDir + u"OoxmlSaveOptions.DocumentCompression.docx", saveOptions);
st->Stop();

auto fileInfo = MakeObject<System::IO::FileInfo>(ArtifactsDir + u"OoxmlSaveOptions.DocumentCompression.docx");

std::cout << String::Format(u"Saving operation done using the \"{0}\" compression level:", compressionLevel) << std::endl;
std::cout << "\tDuration:\t" << st->get_ElapsedMilliseconds() << " ms" << std::endl;
std::cout << "\tFile Size:\t" << fileInfo->get_Length() << " bytes" << std::endl;
```

## See Also

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
