---
title: "Constructeur Aspose::Words::Saving::XpsSaveOptions::XpsSaveOptions"
linktitle: "XpsSaveOptions"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Constructeur Aspose::Words::Saving::XpsSaveOptions::XpsSaveOptions. Initialise une nouvelle instance de cette classe qui peut être utilisée pour enregistrer un document au format Xps en C++."
type: docs
weight: 2000
url: /fr/cpp/aspose.words.saving/xpssaveoptions/xpssaveoptions/
---
## XpsSaveOptions::XpsSaveOptions() constructor


Initialise une nouvelle instance de cette classe qui peut être utilisée pour enregistrer un document au format [Xps](../../../aspose.words/saveformat/).

```cpp
Aspose::Words::Saving::XpsSaveOptions::XpsSaveOptions()
```


## Exemples



Montre comment limiter le niveau des titres qui apparaîtront dans le plan d'un document XPS enregistré.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Insérez des titres pouvant servir d'entrées de table des matières aux niveaux 1, 2, puis 3.
builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading1);

ASSERT_TRUE(builder->get_ParagraphFormat()->get_IsHeading());

builder->Writeln(u"Heading 1");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading2);

builder->Writeln(u"Heading 1.1");
builder->Writeln(u"Heading 1.2");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading3);

builder->Writeln(u"Heading 1.2.1");
builder->Writeln(u"Heading 1.2.2");

// Créez un objet "XpsSaveOptions" que nous pouvons transmettre à la méthode "Save" du document
// pour modifier la façon dont cette méthode convertit le document en .XPS.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::XpsSaveOptions>();

ASSERT_EQ(Aspose::Words::SaveFormat::Xps, saveOptions->get_SaveFormat());

// Le document XPS de sortie contiendra un plan, une table des matières qui répertorie les titres dans le corps du document.
// Cliquer sur une entrée de ce plan nous amènera à l'emplacement du titre correspondant.
// Définissez la propriété "HeadingsOutlineLevels" sur "2" pour exclure tous les titres dont le niveau est supérieur à 2 du plan.
// Les deux derniers titres que nous avons insérés ci-dessus n'apparaîtront pas.
saveOptions->get_OutlineOptions()->set_HeadingsOutlineLevels(2);

doc->Save(get_ArtifactsDir() + u"XpsSaveOptions.OutlineLevels.xps", saveOptions);
```

## Voir aussi

* Class [XpsSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
## XpsSaveOptions::XpsSaveOptions(Aspose::Words::SaveFormat) constructor


Initialise une nouvelle instance de cette classe qui peut être utilisée pour enregistrer un document aux formats [Xps](../../../aspose.words/saveformat/) ou [OpenXps](../../../aspose.words/saveformat/).

```cpp
Aspose::Words::Saving::XpsSaveOptions::XpsSaveOptions(Aspose::Words::SaveFormat saveFormat)
```


## Exemples



Montre comment enregistrer un document au format XPS sous forme de pliage de livre.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Paragraphs.docx");

// Créez un objet "XpsSaveOptions" que nous pouvons transmettre à la méthode "Save" du document
// pour modifier la façon dont cette méthode convertit le document en .XPS.
auto xpsOptions = System::MakeObject<Aspose::Words::Saving::XpsSaveOptions>(Aspose::Words::SaveFormat::Xps);

// Définissez la propriété "UseBookFoldPrintingSettings" sur "true" pour organiser le contenu
// dans le XPS de sortie d'une manière qui nous aide à l'utiliser pour créer un livret.
// Définissez la propriété "UseBookFoldPrintingSettings" sur "false" pour rendre le XPS normalement.
xpsOptions->set_UseBookFoldPrintingSettings(renderTextAsBookFold);

// Si nous rendons le document sous forme de livret, nous devons définir la propriété "MultiplePages"
// propriétés des objets de configuration de page de toutes les sections à \"MultiplePagesType.BookFoldPrinting\".
if (renderTextAsBookFold)
{
    for (auto&& s : System::IterateOver<Aspose::Words::Section>(doc->get_Sections()))
    {
        s->get_PageSetup()->set_MultiplePages(Aspose::Words::Settings::MultiplePagesType::BookFoldPrinting);
    }
}

// Une fois que nous imprimons ce document, nous pouvons le transformer en livret en empilant les pages
// pour sortir de l'imprimante et se plier au milieu.
doc->Save(get_ArtifactsDir() + u"XpsSaveOptions.BookFold.xps", xpsOptions);
```

## Voir aussi

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [XpsSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
