---
title: "Méthode Aspose::Words::ParagraphCollection::ToArray"
linktitle: "ToArray"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::ParagraphCollection::ToArray. Copie tous les paragraphes de la collection dans un nouveau tableau de paragraphes en C++."
type: docs
weight: 5000
url: /fr/cpp/aspose.words/paragraphcollection/toarray/
---
## ParagraphCollection::ToArray method


Copie tous les paragraphes de la collection dans un nouveau tableau de paragraphes.

```cpp
System::ArrayPtr<System::SharedPtr<Aspose::Words::Paragraph>> Aspose::Words::ParagraphCollection::ToArray()
```


### ReturnValue

Un tableau de paragraphes.

## Exemples



Montre comment créer un tableau à partir d'une [NodeCollection](../../nodecollection/).
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Paragraphs.docx");

System::ArrayPtr<System::SharedPtr<Aspose::Words::Paragraph>> paras = doc->get_FirstSection()->get_Body()->get_Paragraphs()->ToArray();

ASSERT_EQ(22, paras->get_Length());
```


Montre comment utiliser la \"suppression à chaud\" pour enlever un nœud pendant l'énumération.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"The first paragraph");
builder->Writeln(u"The second paragraph");
builder->Writeln(u"The third paragraph");
builder->Writeln(u"The fourth paragraph");

// Supprimez un nœud de la collection au milieu d'une énumération.
for (System::SharedPtr<Aspose::Words::Paragraph> para : doc->get_FirstSection()->get_Body()->get_Paragraphs()->ToArray())
{
    if (para->get_Range()->get_Text().Contains(u"third"))
    {
        para->Remove();
    }
}

ASSERT_FALSE(doc->GetText().Contains(u"The third paragraph"));
```

## Voir aussi

* Class [Paragraph](../../paragraph/)
* Class [ParagraphCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
