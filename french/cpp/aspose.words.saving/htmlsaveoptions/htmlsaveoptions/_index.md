---
title: "Constructeur Aspose::Words::Saving::HtmlSaveOptions::HtmlSaveOptions"
linktitle: "HtmlSaveOptions"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Constructeur Aspose::Words::Saving::HtmlSaveOptions::HtmlSaveOptions. Initialise une nouvelle instance de cette classe qui peut être utilisée pour enregistrer un document au format Html en C++."
type: docs
weight: 2000
url: /fr/cpp/aspose.words.saving/htmlsaveoptions/htmlsaveoptions/
---
## HtmlSaveOptions::HtmlSaveOptions() constructor


Initialise une nouvelle instance de cette classe qui peut être utilisée pour enregistrer un document au format [Html](../../../aspose.words/saveformat/).

```cpp
Aspose::Words::Saving::HtmlSaveOptions::HtmlSaveOptions()
```


## Exemples



Montre comment utiliser un encodage spécifique lors de l'enregistrement d'un document au format .epub.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

// Utilisez un objet SaveOptions pour spécifier le codage d'un document que nous allons enregistrer.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
saveOptions->set_SaveFormat(Aspose::Words::SaveFormat::Epub);
saveOptions->set_Encoding(System::Text::Encoding::get_UTF8());

// Par défaut, un document .epub de sortie contiendra tous ses éléments dans une seule partie HTML.
// Un critère de division nous permet de segmenter le document en plusieurs parties HTML.
// Nous définirons les critères pour diviser le document en paragraphes d'en-tête.
// Ceci est utile pour les lecteurs qui ne peuvent pas lire des fichiers HTML de taille supérieure à une taille spécifique.
saveOptions->set_DocumentSplitCriteria(Aspose::Words::Saving::DocumentSplitCriteria::HeadingParagraph);

// Spécifiez que nous voulons exporter les propriétés du document.
saveOptions->set_ExportDocumentProperties(true);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.Doc2EpubSaveOptions.epub", saveOptions);
```

## Voir aussi

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
## HtmlSaveOptions::HtmlSaveOptions(Aspose::Words::SaveFormat) constructor


Initialise une nouvelle instance de cette classe qui peut être utilisée pour enregistrer un document aux formats [Html](../../../aspose.words/saveformat/), [Mhtml](../../../aspose.words/saveformat/), [Epub](../../../aspose.words/saveformat/), [Azw3](../../../aspose.words/saveformat/) ou [Mobi](../../../aspose.words/saveformat/).

```cpp
Aspose::Words::Saving::HtmlSaveOptions::HtmlSaveOptions(Aspose::Words::SaveFormat saveFormat)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| saveFormat | Aspose::Words::SaveFormat | Peut être [Html](../../../aspose.words/saveformat/), [Mhtml](../../../aspose.words/saveformat/), [Epub](../../../aspose.words/saveformat/), [Azw3](../../../aspose.words/saveformat/) ou [Mobi](../../../aspose.words/saveformat/). |

## Exemples



Montre comment enregistrer un document dans une version spécifique de HTML.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>(Aspose::Words::SaveFormat::Html);
options->set_HtmlVersion(htmlVersion);
options->set_PrettyFormat(true);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.HtmlVersions.html", options);

// Nos documents HTML présenteront de légères différences pour être compatibles avec différentes versions de HTML.
System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlSaveOptions.HtmlVersions.html");

switch (htmlVersion)
{
    case Aspose::Words::Saving::HtmlVersion::Html5:
        ASSERT_TRUE(outDocContents.Contains(u"<a id=\"_Toc76372689\"></a>"));
        ASSERT_TRUE(outDocContents.Contains(u"<a id=\"_Toc76372689\"></a>"));
        ASSERT_TRUE(outDocContents.Contains(u"<table style=\"padding:0pt; -aw-border:0.5pt single #000000; -aw-border-insideh:0.5pt single #000000; -aw-border-insidev:0.5pt single #000000; border-collapse:collapse\">"));
        break;

    case Aspose::Words::Saving::HtmlVersion::Xhtml:
        ASSERT_TRUE(outDocContents.Contains(u"<a name=\"_Toc76372689\"></a>"));
        ASSERT_TRUE(outDocContents.Contains(u"<ul type=\"disc\" style=\"margin:0pt; padding-left:0pt\">"));
        ASSERT_TRUE(outDocContents.Contains(u"<table cellspacing=\"0\" cellpadding=\"0\" style=\"-aw-border:0.5pt single #000000; -aw-border-insideh:0.5pt single #000000; -aw-border-insidev:0.5pt single #000000; border-collapse:collapse\""));
        break;

}
```

## Voir aussi

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
