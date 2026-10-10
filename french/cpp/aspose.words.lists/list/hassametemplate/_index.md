---
title: "Aspose::Words::Lists::List::HasSameTemplate méthode"
linktitle: "HasSameTemplate"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Lists::List::HasSameTemplate méthode. Retourne true si la liste actuelle et la liste fournie sont créées à partir du même modèle en C++."
type: docs
weight: 14000
url: /fr/cpp/aspose.words.lists/list/hassametemplate/
---
## List::HasSameTemplate method


Renvoie true si la liste actuelle et la liste donnée sont créées à partir du même modèle.

```cpp
bool Aspose::Words::Lists::List::HasSameTemplate(const System::SharedPtr<Aspose::Words::Lists::List> &other)
```


## Exemples



Montre comment définir des listes avec le même ListDefId.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Different lists.docx");

ASSERT_TRUE(doc->get_Lists()->idx_get(0)->HasSameTemplate(doc->get_Lists()->idx_get(1)));
ASSERT_FALSE(doc->get_Lists()->idx_get(1)->HasSameTemplate(doc->get_Lists()->idx_get(2)));
```

## Voir aussi

* Class [List](../)
* Class [List](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words for C++](../../../)
