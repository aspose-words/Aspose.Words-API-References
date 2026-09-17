---
title: "Aspose::Words::Notes::EndnoteOptions::get_StartNumber méthode"
linktitle: "get_StartNumber"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Notes::EndnoteOptions::get_StartNumber méthode. Spécifie le numéro ou le caractère de départ pour les premières notes de fin numérotées automatiquement en C++."
type: docs
weight: 5000
url: /fr/cpp/aspose.words.notes/endnoteoptions/get_startnumber/
---
## EndnoteOptions::get_StartNumber method


Spécifie le numéro ou le caractère de départ pour les premières notes de fin automatiquement numérotées.

```cpp
int32_t Aspose::Words::Notes::EndnoteOptions::get_StartNumber() override
```

## Remarques


Cette propriété n'a d'effet que lorsque [RestartRule](../get_restartrule/) est définie sur [Continuous](../../footnotenumberingrule/).

## Exemples



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

* Class [EndnoteOptions](../)
* Namespace [Aspose::Words::Notes](../../)
* Library [Aspose.Words for C++](../../../)
