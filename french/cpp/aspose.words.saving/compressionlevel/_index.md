---
title: "Énumération Aspose::Words::Saving::CompressionLevel"
linktitle: "CompressionLevel"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Énumération Aspose::Words::Saving::CompressionLevel. Niveau de compression pour les fichiers OOXML et XPS. (Les fichiers DOCX, DOTX et XPS sont internement une archive ZIP, cette propriété contrôle le niveau de compression de l'archive. Notez que le fichier FlatOpc n'est pas une archive ZIP, par conséquent, cette propriété n'affecte pas les fichiers FlatOpc.) en C++."
type: docs
weight: 47000
url: /fr/cpp/aspose.words.saving/compressionlevel/
---
## CompressionLevel enum


Niveau de compression pour les fichiers OOXML et XPS. (Les fichiers DOCX, DOTX et XPS sont internement une archive ZIP, cette propriété contrôle le niveau de compression de l'archive. Notez que le fichier FlatOpc n'est pas une archive ZIP, par conséquent, cette propriété n'affecte pas les fichiers FlatOpc.)

```cpp
enum class CompressionLevel
```

### Valeurs

| Nom | Valeur | Description |
| --- | --- | --- |
| Normal | 0 | Niveau de compression normal. Niveau de compression par défaut utilisé par [Aspose.Words](../../aspose.words/). |
| Maximum | 1 | Niveau de compression maximal. |
| Rapide | 2 | Niveau de compression rapide. |
| SuperFast | 3 | Niveau de compression super rapide. Microsoft Word utilise ce niveau de compression. |


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


Montre comment contrôler le niveau de compression lors de l'enregistrement d'un document au format XPS.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Sample document for XPS compression test.");

// Créez un objet XpsSaveOptions et définissez le niveau de compression.
auto options = System::MakeObject<Aspose::Words::Saving::XpsSaveOptions>();
options->set_CompressionLevel(Aspose::Words::Saving::CompressionLevel::Maximum);

doc->Save(get_ArtifactsDir() + u"XpsSaveOptions.CompressionLevelXps.xps", options);
```

## Voir aussi

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
