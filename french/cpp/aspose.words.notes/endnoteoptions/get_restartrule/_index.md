---
title: "Aspose::Words::Notes::EndnoteOptions::get_RestartRule méthode"
linktitle: "get_RestartRule"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Notes::EndnoteOptions::get_RestartRule méthode. Détermine quand le numérotage automatique redémarre en C++."
type: docs
weight: 4000
url: /fr/cpp/aspose.words.notes/endnoteoptions/get_restartrule/
---
## EndnoteOptions::get_RestartRule method


Détermine quand le numéro automatique redémarre.

```cpp
Aspose::Words::Notes::FootnoteNumberingRule Aspose::Words::Notes::EndnoteOptions::get_RestartRule() override
```

## Remarques


Toutes les valeurs ne s’appliquent pas aux notes de fin. Pour déterminer quelles valeurs sont applicables, voir [FootnoteNumberingRule](../../footnotenumberingrule/).

## Exemples



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

## Voir aussi

* Enum [FootnoteNumberingRule](../../footnotenumberingrule/)
* Class [EndnoteOptions](../)
* Namespace [Aspose::Words::Notes](../../)
* Library [Aspose.Words for C++](../../../)
