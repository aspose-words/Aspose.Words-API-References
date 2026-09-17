---
title: "Aspose::Words::DocumentBuilder::InsertTableOfContents méthode"
linktitle: "InsertTableOfContents"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::DocumentBuilder::InsertTableOfContents méthode. Insère un champ TOC (table des matières) dans le document en C++."
type: docs
weight: 48000
url: /fr/cpp/aspose.words/documentbuilder/inserttableofcontents/
---
## DocumentBuilder::InsertTableOfContents method


Insère un champ TOC (table des matières) dans le document.

```cpp
System::SharedPtr<Aspose::Words::Fields::Field> Aspose::Words::DocumentBuilder::InsertTableOfContents(const System::String &switches)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| commutateurs | const System::String\& | Les commutateurs du champ TOC. |
## Remarques


Cette méthode insère un champ TOC (table des matières) dans le document à la position actuelle.

Une table des matières dans un document Word peut être générée de plusieurs manières et formatée à l'aide d'une variété d'options. La façon dont la table est générée et affichée par Microsoft Word est contrôlée par les commutateurs du champ.

Le moyen le plus simple de spécifier les commutateurs consiste à insérer et configurer une table des matières dans un document Word en utilisant le menu Insert->Reference->Index et le menu [Tables](../../../aspose.words.tables/), puis à activer l'affichage des codes de champ pour voir les commutateurs. Vous pouvez appuyer sur Alt+F9 dans Microsoft Word pour basculer l'affichage des codes de champ on ou off.

Par exemple, après avoir créé une table des matières, le champ suivant est inséré dans le document : **%{ TOC \o "1-3" \h \z }**. Vous pouvez copier **%\o "1-3" \h \z** et l'utiliser comme paramètre des commutateurs.

Notez que [InsertTableOfContents()](../) n'insérera qu'un champ TOC, mais ne construira pas réellement la table des matières. La table des matières est générée par Microsoft Word lorsque le champ est mis à jour.

Si vous insérez une table des matières en utilisant cette méthode puis ouvrez le fichier dans Microsoft Word, vous ne verrez pas la table des matières car le champ TOC n'a pas encore été mis à jour.

Dans Microsoft Word, les champs ne sont pas mis à jour automatiquement à l'ouverture d'un document, mais vous pouvez mettre à jour les champs d'un document à tout moment en appuyant sur F9.

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

* Class [Field](../../../aspose.words.fields/field/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
