---
title: "Méthode Aspose::Words::DocumentBuilder::InsertFootnote"
linktitle: "InsertFootnote"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::DocumentBuilder::InsertFootnote. Insère une note de bas de page ou une note de fin dans le document en C++."
type: docs
weight: 35000
url: /fr/cpp/aspose.words/documentbuilder/insertfootnote/
---
## DocumentBuilder::InsertFootnote(Aspose::Words::Notes::FootnoteType, const System::String\&) method


Insère une note de bas de page ou une note de fin dans le document.

```cpp
System::SharedPtr<Aspose::Words::Notes::Footnote> Aspose::Words::DocumentBuilder::InsertFootnote(Aspose::Words::Notes::FootnoteType footnoteType, const System::String &footnoteText)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| footnoteType | Aspose::Words::Notes::FootnoteType | Spécifie s'il faut insérer une note de bas de page ou une note de fin. |
| footnoteText | const System::String\& | Spécifie le texte de la note de bas de page. |

### ReturnValue

Renvoie un objet footnote qui vient d'être créé.

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

## Voir aussi

* Class [Footnote](../../../aspose.words.notes/footnote/)
* Enum [FootnoteType](../../../aspose.words.notes/footnotetype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertFootnote(Aspose::Words::Notes::FootnoteType, const System::String\&, const System::String\&) method


Insère une note de bas de page ou une note de fin dans le document.

```cpp
System::SharedPtr<Aspose::Words::Notes::Footnote> Aspose::Words::DocumentBuilder::InsertFootnote(Aspose::Words::Notes::FootnoteType footnoteType, const System::String &footnoteText, const System::String &referenceMark)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| footnoteType | Aspose::Words::Notes::FootnoteType | Spécifie s'il faut insérer une note de bas de page ou une note de fin. |
| footnoteText | const System::String\& | Spécifie le texte de la note de bas de page. |
| referenceMark | const System::String\& | Spécifie la marque de référence personnalisée de la note de bas de page. |

### ReturnValue

Renvoie un objet footnote qui vient d'être créé.

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

## Voir aussi

* Class [Footnote](../../../aspose.words.notes/footnote/)
* Enum [FootnoteType](../../../aspose.words.notes/footnotetype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
