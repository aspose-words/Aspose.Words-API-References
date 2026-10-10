---
title: "Méthode Aspose::Words::Document::get_PunctuationKerning"
linktitle: "get_PunctuationKerning"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Document::get_PunctuationKerning. Spécifie si le crénage s'applique à la fois au texte latin et à la ponctuation en C++."
type: docs
weight: 44500
url: /fr/cpp/aspose.words/document/get_punctuationkerning/
---
## Document::get_PunctuationKerning method


Spécifie si le crénage s'applique à la fois au texte latin et à la ponctuation.

```cpp
bool Aspose::Words::Document::get_PunctuationKerning()
```


## Exemples



Montre comment travailler avec le crénage qui s'applique à la fois au texte latin et à la ponctuation.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");
ASSERT_TRUE(doc->get_PunctuationKerning());
```

## Voir aussi

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
