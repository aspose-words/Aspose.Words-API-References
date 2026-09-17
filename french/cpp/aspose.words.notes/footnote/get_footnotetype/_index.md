---
title: "Aspose::Words::Notes::Footnote::get_FootnoteType method"
linktitle: "get_FootnoteType"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Notes::Footnote::get_FootnoteType method. Retourne une valeur qui indique s’il s’agit d’une note de bas de page ou d’une note de fin en C++."
type: docs
weight: 4000
url: /fr/cpp/aspose.words.notes/footnote/get_footnotetype/
---
## Footnote::get_FootnoteType method


Renvoie une valeur qui indique s’il s’agit d’une note de bas de page ou d’une note de fin.

```cpp
Aspose::Words::Notes::FootnoteType Aspose::Words::Notes::Footnote::get_FootnoteType() const
```


## Exemples



Montre la différence entre les notes de bas de page et les notes de fin.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Voici deux manières d’attacher des références numérotées au texte. Ces références ajouteront un
// petit signe de référence en exposant à l’endroit où nous les insérons.
// Le signe de référence, par défaut, est le numéro d’index de la référence parmi toutes les références du document.
// Chaque référence créera également une entrée, qui aura le même signe de référence que dans le texte principal
// et le texte de référence, que nous transmettrons à la méthode "InsertFootnote" du constructeur de document.
// 1 -  Une note de bas de page, dont l’entrée apparaîtra sur la même page que le texte auquel elle fait référence :
builder->Write(u"Footnote referenced main body text.");
System::SharedPtr<Aspose::Words::Notes::Footnote> footnote = builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote text, will appear at the bottom of the page that contains the referenced text.");

// 2 -  Une note de fin, dont l’entrée apparaîtra à la fin du document:
builder->Write(u"Endnote referenced main body text.");
System::SharedPtr<Aspose::Words::Notes::Footnote> endnote = builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote text, will appear at the very end of the document.");

builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);

ASSERT_EQ(Aspose::Words::Notes::FootnoteType::Footnote, footnote->get_FootnoteType());
ASSERT_EQ(Aspose::Words::Notes::FootnoteType::Endnote, endnote->get_FootnoteType());

doc->Save(get_ArtifactsDir() + u"InlineStory.FootnoteEndnote.docx");
```

## Voir aussi

* Enum [FootnoteType](../../footnotetype/)
* Class [Footnote](../)
* Namespace [Aspose::Words::Notes](../../)
* Library [Aspose.Words for C++](../../../)
