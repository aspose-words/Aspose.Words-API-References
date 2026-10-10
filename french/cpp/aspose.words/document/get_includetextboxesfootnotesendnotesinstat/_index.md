---
title: "Aspose::Words::Document::get_IncludeTextboxesFootnotesEndnotesInStat méthode"
linktitle: "get_IncludeTextboxesFootnotesEndnotesInStat"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Document::get_IncludeTextboxesFootnotesEndnotesInStat méthode. Spécifie s’il faut inclure les zones de texte, les notes de bas de page et les notes de fin dans les statistiques de comptage de mots en C++."
type: docs
weight: 33000
url: /fr/cpp/aspose.words/document/get_includetextboxesfootnotesendnotesinstat/
---
## Document::get_IncludeTextboxesFootnotesEndnotesInStat method


Spécifie s'il faut inclure les zones de texte, les notes de bas de page et les notes de fin dans les statistiques de comptage de mots.

```cpp
bool Aspose::Words::Document::get_IncludeTextboxesFootnotesEndnotesInStat()
```


## Exemples



Montre comment inclure ou exclure les zones de texte, les notes de bas de page et les notes de fin des statistiques de comptage de mots.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Lorem ipsum");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"sit amet");

// Par défaut, l’option est définie sur 'false'.
doc->UpdateWordCount();
// Nombre de mots sans zones de texte, notes de bas de page et notes de fin.
ASSERT_EQ(2, doc->get_BuiltInDocumentProperties()->get_Words());

doc->set_IncludeTextboxesFootnotesEndnotesInStat(true);
doc->UpdateWordCount();
// Nombre de mots avec zones de texte, notes de bas de page et notes de fin.
ASSERT_EQ(4, doc->get_BuiltInDocumentProperties()->get_Words());
```

## Voir aussi

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
