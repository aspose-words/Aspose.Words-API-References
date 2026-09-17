---
title: "Méthode Aspose::Words::ParagraphFormat::get_StyleIdentifier"
linktitle: "get_StyleIdentifier"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::ParagraphFormat::get_StyleIdentifier. Obtient ou définit l'identifiant de style indépendant de la locale du style de paragraphe appliqué à ce formatage en C++."
type: docs
weight: 36000
url: /fr/cpp/aspose.words/paragraphformat/get_styleidentifier/
---
## ParagraphFormat::get_StyleIdentifier method


Obtient ou définit l’identifiant de style indépendant de la locale du style de paragraphe appliqué à ce formatage.

```cpp
Aspose::Words::StyleIdentifier Aspose::Words::ParagraphFormat::get_StyleIdentifier()
```


## Exemples



Montre comment insérer une Table des matières (TOC) dans un document en utilisant les styles de titres comme entrées.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Insérez une table des matières pour la première page du document.
// Configurez la table pour récupérer les paragraphes avec des titres de niveaux 1 à 3.
// De plus, définissez ses entrées comme des hyperliens qui nous mèneront
// à l’emplacement du titre lorsqu’on clique dessus avec le bouton gauche dans Microsoft Word.
builder->InsertTableOfContents(u"\\o \"1-3\" \\h \\z \\u");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// Remplissez la table des matières en ajoutant des paragraphes avec des styles de titres.
// Chaque titre de ce type avec un niveau compris entre 1 et 3 créera une entrée dans la table.
builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading1);
builder->Writeln(u"Heading 1");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading2);
builder->Writeln(u"Heading 1.1");
builder->Writeln(u"Heading 1.2");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading1);
builder->Writeln(u"Heading 2");
builder->Writeln(u"Heading 3");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading2);
builder->Writeln(u"Heading 3.1");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading3);
builder->Writeln(u"Heading 3.1.1");
builder->Writeln(u"Heading 3.1.2");
builder->Writeln(u"Heading 3.1.3");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading4);
builder->Writeln(u"Heading 3.1.3.1");
builder->Writeln(u"Heading 3.1.3.2");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading2);
builder->Writeln(u"Heading 3.2");
builder->Writeln(u"Heading 3.3");

// Une table des matières est un champ d'un type qui doit être mis à jour pour afficher un résultat à jour.
doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertToc.docx");
```

## Voir aussi

* Enum [StyleIdentifier](../../styleidentifier/)
* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
