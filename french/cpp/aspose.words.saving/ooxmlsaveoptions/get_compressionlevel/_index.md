---
title: "Aspose::Words::Saving::OoxmlSaveOptions::get_CompressionLevel méthode"
linktitle: "get_CompressionLevel"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::OoxmlSaveOptions::get_CompressionLevel méthode. Spécifie le niveau de compression utilisé pour enregistrer le document. La valeur par défaut est Normal en C++."
type: docs
weight: 4000
url: /fr/cpp/aspose.words.saving/ooxmlsaveoptions/get_compressionlevel/
---
## OoxmlSaveOptions::get_CompressionLevel method


Spécifie le niveau de compression utilisé pour enregistrer le document. La valeur par défaut est [Normal](../../compressionlevel/).

```cpp
Aspose::Words::Saving::CompressionLevel Aspose::Words::Saving::OoxmlSaveOptions::get_CompressionLevel() const
```


## Exemples



Montre comment spécifier le niveau de compression à utiliser lors de l'enregistrement d'un document OOXML.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Big document.docx");

// Lorsque nous enregistrons le document au format OOXML, nous pouvons créer un objet OoxmlSaveOptions
// et le transmettre ensuite à la méthode d'enregistrement du document pour modifier la façon dont nous enregistrons le document.
// Définissez la propriété "CompressionLevel" sur "CompressionLevel.Maximum" pour appliquer la compression la plus forte et la plus lente.
// Définissez la propriété "CompressionLevel" sur "CompressionLevel.Normal" pour appliquer
// la compression par défaut que Aspose.Words utilise lors de l'enregistrement de documents OOXML.
// Définissez la propriété "CompressionLevel" sur "CompressionLevel.Fast" pour appliquer une compression plus rapide et plus faible.
// Définissez la propriété "CompressionLevel" sur "CompressionLevel.SuperFast" pour appliquer
// la compression par défaut que Microsoft Word utilise.
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

## Voir aussi

* Enum [CompressionLevel](../../compressionlevel/)
* Class [OoxmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
