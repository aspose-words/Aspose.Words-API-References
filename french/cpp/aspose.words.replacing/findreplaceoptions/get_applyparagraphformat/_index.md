---
title: "Aspose::Words::Replacing::FindReplaceOptions::get_ApplyParagraphFormat méthode"
linktitle: "get_ApplyParagraphFormat"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Replacing::FindReplaceOptions::get_ApplyParagraphFormat méthode. Formatage de paragraphe appliqué au nouveau contenu en C++."
type: docs
weight: 4000
url: /fr/cpp/aspose.words.replacing/findreplaceoptions/get_applyparagraphformat/
---
## FindReplaceOptions::get_ApplyParagraphFormat method


[Paragraph](../../../aspose.words/paragraph/) formatting applied to new content.

```cpp
System::SharedPtr<Aspose::Words::ParagraphFormat> Aspose::Words::Replacing::FindReplaceOptions::get_ApplyParagraphFormat() const
```


## Exemples



Montre comment ajouter du formatage aux paragraphes dans lesquels une opération de recherche et remplacement a trouvé des correspondances.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Every paragraph that ends with a full stop like this one will be right aligned.");
builder->Writeln(u"This one will not!");
builder->Write(u"This one also will.");

System::SharedPtr<Aspose::Words::ParagraphCollection> paragraphs = doc->get_FirstSection()->get_Body()->get_Paragraphs();

ASSERT_EQ(Aspose::Words::ParagraphAlignment::Left, paragraphs->idx_get(0)->get_ParagraphFormat()->get_Alignment());
ASSERT_EQ(Aspose::Words::ParagraphAlignment::Left, paragraphs->idx_get(1)->get_ParagraphFormat()->get_Alignment());
ASSERT_EQ(Aspose::Words::ParagraphAlignment::Left, paragraphs->idx_get(2)->get_ParagraphFormat()->get_Alignment());

// Nous pouvons utiliser un objet "FindReplaceOptions" pour modifier le processus de recherche et remplacement.
auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();

// Définissez la propriété "Alignment" sur "ParagraphAlignment.Right" pour aligner à droite chaque paragraphe.
// qui contient une correspondance trouvée par l'opération de recherche et remplacement.
options->get_ApplyParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Right);

// Remplacez chaque point final qui se trouve juste avant un saut de paragraphe par un point d'exclamation.
int32_t count = doc->get_Range()->Replace(u".&p", u"!&p", options);

ASSERT_EQ(2, count);
ASSERT_EQ(Aspose::Words::ParagraphAlignment::Right, paragraphs->idx_get(0)->get_ParagraphFormat()->get_Alignment());
ASSERT_EQ(Aspose::Words::ParagraphAlignment::Left, paragraphs->idx_get(1)->get_ParagraphFormat()->get_Alignment());
ASSERT_EQ(Aspose::Words::ParagraphAlignment::Right, paragraphs->idx_get(2)->get_ParagraphFormat()->get_Alignment());
ASSERT_EQ(System::String(u"Every paragraph that ends with a full stop like this one will be right aligned!\r") + u"This one will not!\r" + u"This one also will!", doc->GetText().Trim());
```

## Voir aussi

* Class [ParagraphFormat](../../../aspose.words/paragraphformat/)
* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
