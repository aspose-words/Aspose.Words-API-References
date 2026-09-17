---
title: "Aspose::Words::Notes::FootnoteType enum"
linktitle: "FootnoteType"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Notes::FootnoteType enum. Spécifie s'il s'agit d'une note de bas de page ou d'une note de fin en C++."
type: docs
weight: 7000
url: /fr/cpp/aspose.words.notes/footnotetype/
---
## FootnoteType enum


Spécifie s’il s’agit d’une note de bas de page ou d’une note de fin.

```cpp
enum class FootnoteType
```

### Valeurs

| Nom | Valeur | Description |
| --- | --- | --- |
| Note de bas de page | 0 | L'objet est une note de bas de page. |
| Note de fin | 1 | L'objet est une note de fin. |

## Remarques


Les notes de bas de page et les notes de fin sont représentées par des objets de la classe [Footnote](./). Utilisez [FootnoteType](../footnote/get_footnotetype/) pour distinguer les notes de bas de page des notes de fin.

## Exemples



Montre comment référencer du texte avec une note de bas de page et une note de fin.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Insérez du texte et marquez-le avec une note de bas de page dont la propriété IsAuto est définie sur "true" par défaut,
// de sorte que le marqueur vu dans le texte principal sera automatiquement numéroté à "1",
// et la note de bas de page apparaîtra en bas de la page.
builder->Write(u"This text will be referenced by a footnote.");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote comment regarding referenced text.");

// Insérez plus de texte et marquez-le avec une note de fin avec une marque de référence personnalisée,
// qui sera utilisée à la place du numéro "2" et définira "IsAuto" sur false.
builder->Write(u"This text will be referenced by an endnote.");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote comment regarding referenced text.", u"CustomMark");

// Les notes de bas de page apparaissent toujours en bas du texte auquel elles se réfèrent,
// de sorte que ce saut de page n'affectera pas la note de bas de page.
// En revanche, les notes de fin sont toujours à la fin du document
// de sorte que ce saut de page poussera la note de fin à la page suivante.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertFootnote.docx");
```


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

* Namespace [Aspose::Words::Notes](../)
* Library [Aspose.Words for C++](../../)
