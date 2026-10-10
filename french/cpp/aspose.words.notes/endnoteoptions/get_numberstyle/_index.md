---
title: "Aspose::Words::Notes::EndnoteOptions::get_NumberStyle méthode"
linktitle: "get_NumberStyle"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Notes::EndnoteOptions::get_NumberStyle méthode. Spécifie le format de numéro pour les notes de fin numérotées automatiquement en C++."
type: docs
weight: 2000
url: /fr/cpp/aspose.words.notes/endnoteoptions/get_numberstyle/
---
## EndnoteOptions::get_NumberStyle method


Spécifie le format de nombre pour les notes de fin auto‑numérotées.

```cpp
Aspose::Words::NumberStyle Aspose::Words::Notes::EndnoteOptions::get_NumberStyle() override
```

## Remarques


Tous les styles de numérotation ne sont pas applicables à cette propriété. Pour la liste des styles de numérotation applicables, consultez la boîte de dialogue Insérer [Footnote](../../footnote/) ou Endnote dans Microsoft Word. Si vous sélectionnez un style de numérotation qui n'est pas applicable, Microsoft Word reviendra à la valeur par défaut.

## Exemples



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

## Voir aussi

* Enum [NumberStyle](../../../aspose.words/numberstyle/)
* Class [EndnoteOptions](../)
* Namespace [Aspose::Words::Notes](../../)
* Library [Aspose.Words for C++](../../../)
