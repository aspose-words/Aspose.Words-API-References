---
title: "Aspose::Words::Document::get_EndnoteOptions méthode"
linktitle: "get_EndnoteOptions"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Document::get_EndnoteOptions méthode. Fournit des options qui contrôlent la numérotation et le positionnement des notes de fin dans ce document en C++."
type: docs
weight: 22000
url: /fr/cpp/aspose.words/document/get_endnoteoptions/
---
## Document::get_EndnoteOptions method


Fournit des options qui contrôlent la numérotation et le positionnement des notes de fin dans ce document.

```cpp
System::SharedPtr<Aspose::Words::Notes::EndnoteOptions> Aspose::Words::Document::get_EndnoteOptions()
```


## Exemples



Montre comment sélectionner un autre emplacement où le document collecte et affiche ses notes de fin.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Une note de fin est un moyen d'attacher une référence ou un commentaire marginal au texte
// qui n'interfère pas avec le flux du texte principal.
// L'insertion d'une note de fin ajoute un petit symbole de référence en exposant
// dans le texte principal où nous insérons la note de fin.
// Chaque note de fin crée également une entrée à la fin du document, composée d'un symbole
// qui correspond au symbole de référence dans le texte principal.
// Le texte de référence que nous passons à la méthode "InsertEndnote" du document builder.
builder->Write(u"Hello world!");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote contents.");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);
builder->Write(u"This is the second section.");

// Nous pouvons utiliser la propriété "Position" pour déterminer où le document placera toutes ses notes de fin.
// Si nous définissons la valeur de la propriété "Position" sur "EndnotePosition.EndOfDocument",
// toutes les notes de bas de page apparaîtront dans une collection à la fin du document. C'est la valeur par défaut.
// Si nous définissons la valeur de la propriété "Position" sur "EndnotePosition.EndOfSection",
// toutes les notes de bas de page apparaîtront dans une collection à la fin de la section dont le texte contient la marque de référence de la note de fin.
doc->get_EndnoteOptions()->set_Position(endnotePosition);

doc->Save(get_ArtifactsDir() + u"InlineStory.PositionEndnote.docx");
```


Montre comment changer le style de numérotation des repères de note de bas de page/fin de texte.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Les notes de bas de page et les notes de fin sont un moyen d'attacher une référence ou un commentaire marginal au texte
// qui n'interfère pas avec le flux du texte principal.
// Insérer une note de bas de page/fin ajoute un petit symbole de référence en exposant
// dans le texte principal où nous insérons la note de bas de page/fin.
// Chaque note de bas de page/fin crée également une entrée, qui consiste en un symbole correspondant à la référence
// dans le texte principal. Le texte de référence que nous transmettons à la méthode "InsertEndnote" du constructeur de document.
// Les entrées de notes de bas de page, par défaut, apparaissent en bas de chaque page qui contient
// leurs symboles de référence, et les notes de fin apparaissent à la fin du document.
builder->Write(u"Text 1. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote 1.");
builder->Write(u"Text 2. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote 2.");
builder->Write(u"Text 3. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote 3.", u"Custom footnote reference mark");

builder->InsertParagraph();

builder->Write(u"Text 1. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote 1.");
builder->Write(u"Text 2. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote 2.");
builder->Write(u"Text 3. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote 3.", u"Custom endnote reference mark");

// Par défaut, le symbole de référence pour chaque note de bas de page et note de fin est son indice
// parmi toutes les notes de bas de page/fin du document. Chaque document maintient des comptes séparés
// pour les notes de bas de page et pour les notes de fin. Par défaut, les notes de bas de page affichent leurs numéros en chiffres arabes,
// et les notes de fin affichent leurs numéros en chiffres romains minuscules.
ASSERT_EQ(Aspose::Words::NumberStyle::Arabic, doc->get_FootnoteOptions()->get_NumberStyle());
ASSERT_EQ(Aspose::Words::NumberStyle::LowercaseRoman, doc->get_EndnoteOptions()->get_NumberStyle());

// Nous pouvons utiliser la propriété "NumberStyle" pour appliquer des styles de numérotation personnalisés aux notes de bas de page et aux notes de fin.
// Cela n'affectera pas les notes de bas de page/fin avec des repères de référence personnalisés.
doc->get_FootnoteOptions()->set_NumberStyle(Aspose::Words::NumberStyle::UppercaseRoman);
doc->get_EndnoteOptions()->set_NumberStyle(Aspose::Words::NumberStyle::UppercaseLetter);

doc->Save(get_ArtifactsDir() + u"InlineStory.RefMarkNumberStyle.docx");
```


Montre comment redémarrer la numérotation des notes de bas de page/fin à certains endroits du document.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Les notes de bas de page et les notes de fin sont un moyen d'attacher une référence ou un commentaire marginal au texte
// qui n'interfère pas avec le flux du texte principal.
// Insérer une note de bas de page/fin ajoute un petit symbole de référence en exposant
// dans le texte principal où nous insérons la note de bas de page/fin.
// Chaque note de bas de page/fin crée également une entrée, qui consiste en un symbole correspondant à la référence
// dans le texte principal. Le texte de référence que nous transmettons à la méthode "InsertEndnote" du constructeur de document.
// Les entrées de notes de bas de page, par défaut, apparaissent en bas de chaque page qui contient
// leurs symboles de référence, et les notes de fin apparaissent à la fin du document.
builder->Write(u"Text 1. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote 1.");
builder->Write(u"Text 2. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote 2.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Write(u"Text 3. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote 3.");
builder->Write(u"Text 4. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote 4.");

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

builder->Write(u"Text 1. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote 1.");
builder->Write(u"Text 2. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote 2.");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);
builder->Write(u"Text 3. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote 3.");
builder->Write(u"Text 4. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote 4.");

// Par défaut, le symbole de référence pour chaque note de bas de page et note de fin est son indice
// parmi toutes les notes de bas de page/fin du document. Chaque document maintient des comptes séparés
// pour les notes de bas de page et les notes de fin et ne redémarre pas ces comptes à aucun moment.
ASSERT_EQ(doc->get_FootnoteOptions()->get_RestartRule(), Aspose::Words::Notes::FootnoteNumberingRule::Default);
ASSERT_EQ(Aspose::Words::Notes::FootnoteNumberingRule::Default, Aspose::Words::Notes::FootnoteNumberingRule::Continuous);

// Nous pouvons utiliser la propriété "RestartRule" pour faire redémarrer le document
// les comptes de notes de bas de page/notes de fin à une nouvelle page ou section.
doc->get_FootnoteOptions()->set_RestartRule(Aspose::Words::Notes::FootnoteNumberingRule::RestartPage);
doc->get_EndnoteOptions()->set_RestartRule(Aspose::Words::Notes::FootnoteNumberingRule::RestartSection);

doc->Save(get_ArtifactsDir() + u"InlineStory.NumberingRule.docx");
```


Montre comment définir un nombre auquel le document commence le compte des notes de bas de page/notes de fin.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Les notes de bas de page et les notes de fin sont un moyen d'attacher une référence ou un commentaire marginal au texte
// qui n'interfère pas avec le flux du texte principal.
// Insérer une note de bas de page/fin ajoute un petit symbole de référence en exposant
// dans le texte principal où nous insérons la note de bas de page/fin.
// Chaque note de bas de page/note de fin crée également une entrée, qui consiste en un symbole
// qui correspond au symbole de référence dans le texte principal.
// Le texte de référence que nous passons à la méthode "InsertEndnote" du document builder.
// Les entrées de notes de bas de page, par défaut, apparaissent en bas de chaque page qui contient
// leurs symboles de référence, et les notes de fin apparaissent à la fin du document.
builder->Write(u"Text 1. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote 1.");
builder->Write(u"Text 2. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote 2.");
builder->Write(u"Text 3. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote 3.");

builder->InsertParagraph();

builder->Write(u"Text 1. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote 1.");
builder->Write(u"Text 2. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote 2.");
builder->Write(u"Text 3. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote 3.");

// Par défaut, le symbole de référence pour chaque note de bas de page et note de fin est son indice
// parmi toutes les notes de bas de page/fin du document. Chaque document maintient des comptes séparés
// pour les notes de bas de page et pour les notes de fin, qui commencent toutes deux à 1.
ASSERT_EQ(1, doc->get_FootnoteOptions()->get_StartNumber());
ASSERT_EQ(1, doc->get_EndnoteOptions()->get_StartNumber());

// Nous pouvons utiliser la propriété "StartNumber" pour faire que le document
// commence un compte de note de bas de page ou de note de fin à un nombre différent.
doc->get_EndnoteOptions()->set_NumberStyle(Aspose::Words::NumberStyle::Arabic);
doc->get_EndnoteOptions()->set_StartNumber(50);

doc->Save(get_ArtifactsDir() + u"InlineStory.StartNumber.docx");
```

## Voir aussi

* Class [EndnoteOptions](../../../aspose.words.notes/endnoteoptions/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
