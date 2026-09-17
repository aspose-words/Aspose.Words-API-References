---
title: "Aspose::Words::Notes::Footnote::get_ReferenceMark méthode"
linktitle: "get_ReferenceMark"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Notes::Footnote::get_ReferenceMark méthode. Obtient/definit le marqueur de référence personnalisé à utiliser pour cette note de bas de page. La valeur par défaut est **empty string**, ce qui signifie que des notes de bas de page auto-numérotées sont utilisées en C++."
type: docs
weight: 7000
url: /fr/cpp/aspose.words.notes/footnote/get_referencemark/
---
## Footnote::get_ReferenceMark method


Obtient/definit le repère personnalisé à utiliser pour cette note de bas de page. La valeur par défaut est **empty string**, ce qui signifie que des notes de bas de page auto‑numérotées sont utilisées.

```cpp
System::String Aspose::Words::Notes::Footnote::get_ReferenceMark() const
```

## Remarques


Si cette propriété est définie sur **empty string** ou **null**, alors la propriété [IsAuto](../get_isauto/) sera automatiquement définie sur **true** ; si elle est définie sur autre chose, alors [IsAuto](../get_isauto/) sera définie sur **false**.

Le format RTF ne peut stocker qu'un seul symbole comme marqueur de référence personnalisé, ainsi lors de l'exportation seul le premier symbole sera écrit, les autres seront ignorés.

## Exemples



Montre comment insérer et personnaliser les notes de bas de page.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Ajoutez du texte, et référencez-le avec une note de bas de page. Cette note de bas de page placera une petite référence en exposant
// après le texte auquel elle se réfère et créera une entrée sous le texte principal en bas de la page.
// Cette entrée contiendra le marqueur de référence de la note de bas de page et le texte de référence,
// que nous passerons à la méthode "InsertFootnote" du constructeur de document.
builder->Write(u"Main body text.");
System::SharedPtr<Aspose::Words::Notes::Footnote> footnote = builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote text.");

// Si cette propriété est définie sur "true", alors le marqueur de référence de notre note de bas de page
// sera son indice parmi toutes les notes de bas de page de la section.
// Ceci est la première note de bas de page, donc le marqueur de référence sera "1".
ASSERT_TRUE(footnote->get_IsAuto());

// Nous pouvons déplacer le constructeur de document à l'intérieur de la note de bas de page pour modifier son texte de référence.
builder->MoveTo(footnote->get_FirstParagraph());
builder->Write(u" More text added by a DocumentBuilder.");
builder->MoveToDocumentEnd();

ASSERT_EQ(u"\u0002 Footnote text. More text added by a DocumentBuilder.", footnote->GetText().Trim());

builder->Write(u" More main body text.");
footnote = builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote text.");

// Nous pouvons définir une marque de référence personnalisée que la note de bas de page utilisera à la place de son numéro d'indice.
footnote->set_ReferenceMark(u"RefMark");

ASSERT_FALSE(footnote->get_IsAuto());

// Un signet avec le drapeau "IsAuto" défini sur true affichera toujours son indice réel
// même si les signets précédents affichent des marques de référence personnalisées, donc le marqueur de référence de ce signet sera "3".
builder->Write(u" More main body text.");
footnote = builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote text.");

ASSERT_TRUE(footnote->get_IsAuto());

doc->Save(get_ArtifactsDir() + u"InlineStory.AddFootnote.docx");
```

## Voir aussi

* Class [Footnote](../)
* Namespace [Aspose::Words::Notes](../../)
* Library [Aspose.Words for C++](../../../)
