---
title: "Aspose::Words::Document::Clone méthode"
linktitle: "Clone"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Document::Clone méthode. Effectue une copie profonde du Document en C++."
type: docs
weight: 7000
url: /fr/cpp/aspose.words/document/clone/
---
## Document::Clone method


Effectue une copie profonde du [Document](../).

```cpp
System::SharedPtr<Aspose::Words::Document> Aspose::Words::Document::Clone()
```


### ReturnValue

Le document cloné.

## Exemples



Montre comment cloner profondément un document.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Hello world!");

// Le clonage produira un nouveau document avec le même contenu que l'original,
// mais avec une copie unique de chaque nœud du document original.
System::SharedPtr<Aspose::Words::Document> clone = doc->Clone();

ASSERT_EQ(doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0)->GetText(), clone->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0)->get_Text());
ASSERT_NE(System::ObjectExt::GetHashCode(doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0)), System::ObjectExt::GetHashCode(clone->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0)));
```

## Voir aussi

* Class [Document](../)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
