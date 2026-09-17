---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_DocumentSplitHeadingLevel méthode"
linktitle: "get_DocumentSplitHeadingLevel"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_DocumentSplitHeadingLevel méthode. Spécifie le niveau maximal de titres auquel le document doit être scindé. La valeur par défaut est %2 en C++."
type: docs
weight: 10000
url: /fr/cpp/aspose.words.saving/htmlsaveoptions/get_documentsplitheadinglevel/
---
## HtmlSaveOptions::get_DocumentSplitHeadingLevel method


Spécifie le niveau maximal de titres auquel le document doit être découpé. La valeur par défaut est **%2**.

```cpp
int32_t Aspose::Words::Saving::HtmlSaveOptions::get_DocumentSplitHeadingLevel() const
```

## Remarques


Lorsque [DocumentSplitCriteria](../get_documentsplitcriteria/) inclut [HeadingParagraph](../../documentsplitcriteria/) et que cette propriété est définie sur une valeur de 1 à 9, le document sera scindé aux paragraphes formatés avec les styles **Heading 1**, **Heading 2**, **Heading 3**, etc. jusqu'au niveau de titre spécifié.

Par défaut, seuls les paragraphes **Heading 1** et **Heading 2** provoquent le fractionnement du document. Définir cette propriété à zéro empêchera le document d'être scindé aux paragraphes de titre.

## Exemples



Montre comment scinder un document HTML de sortie par titres en plusieurs parties.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Chaque paragraphe que nous formatons avec un style "Heading" peut servir de titre.
// Chaque titre peut également avoir un niveau de titre, déterminé par le nombre de son style de titre.
// Les titres ci-dessous sont de niveaux 1 à 3.
builder->get_ParagraphFormat()->set_Style(builder->get_Document()->get_Styles()->idx_get(u"Heading 1"));
builder->Writeln(u"Heading #1");
builder->get_ParagraphFormat()->set_Style(builder->get_Document()->get_Styles()->idx_get(u"Heading 2"));
builder->Writeln(u"Heading #2");
builder->get_ParagraphFormat()->set_Style(builder->get_Document()->get_Styles()->idx_get(u"Heading 3"));
builder->Writeln(u"Heading #3");
builder->get_ParagraphFormat()->set_Style(builder->get_Document()->get_Styles()->idx_get(u"Heading 1"));
builder->Writeln(u"Heading #4");
builder->get_ParagraphFormat()->set_Style(builder->get_Document()->get_Styles()->idx_get(u"Heading 2"));
builder->Writeln(u"Heading #5");
builder->get_ParagraphFormat()->set_Style(builder->get_Document()->get_Styles()->idx_get(u"Heading 3"));
builder->Writeln(u"Heading #6");

// Créez un objet HtmlSaveOptions et définissez le critère de division sur "HeadingParagraph".
// Ces critères scinderont le document aux paragraphes avec des styles "Heading" en plusieurs documents plus petits,
// et enregistreront chaque document dans un fichier HTML séparé sur le système de fichiers local.
// Nous définirons également le niveau de titre maximal, ce qui scinde le document à 2.
// En enregistrant le document, il sera scindé aux titres de niveaux 1 et 2, mais pas aux niveaux 3 à 9.
auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
options->set_DocumentSplitCriteria(Aspose::Words::Saving::DocumentSplitCriteria::HeadingParagraph);
options->set_DocumentSplitHeadingLevel(2);

// Notre document comporte quatre titres de niveaux 1 - 2. L'un de ces titres ne sera pas
// un point de division puisqu'il se trouve au début du document.
// L'opération d'enregistrement divisera notre document en trois endroits, en quatre documents plus petits.
doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.HeadingLevels.html", options);

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"HtmlSaveOptions.HeadingLevels.html");

ASSERT_EQ(u"Heading #1", doc->GetText().Trim());

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"HtmlSaveOptions.HeadingLevels-01.html");

ASSERT_EQ(System::String(u"Heading #2\r") + u"Heading #3", doc->GetText().Trim());

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"HtmlSaveOptions.HeadingLevels-02.html");

ASSERT_EQ(u"Heading #4", doc->GetText().Trim());

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"HtmlSaveOptions.HeadingLevels-03.html");

ASSERT_EQ(System::String(u"Heading #5\r") + u"Heading #6", doc->GetText().Trim());
```

## Voir aussi

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
