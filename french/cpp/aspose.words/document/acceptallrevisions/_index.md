---
title: "Aspose::Words::Document::AcceptAllRevisions méthode"
linktitle: "AcceptAllRevisions"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Document::AcceptAllRevisions méthode. Accepte toutes les modifications suivies dans le document en C++."
type: docs
weight: 4000
url: /fr/cpp/aspose.words/document/acceptallrevisions/
---
## Document::AcceptAllRevisions method


Accepte toutes les modifications suivies dans le document.

```cpp
void Aspose::Words::Document::AcceptAllRevisions()
```


## Exemples



Montre comment accepter toutes les modifications suivies dans le document.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Modifiez le document tout en suivant les modifications pour créer quelques révisions.
doc->StartTrackRevisions(u"John Doe");
builder->Write(u"Hello world! ");
builder->Write(u"Hello again! ");
builder->Write(u"This is another revision.");
doc->StopTrackRevisions();

ASSERT_EQ(3, doc->get_Revisions()->get_Count());

// Nous pouvons parcourir chaque révision et l'accepter ou la rejeter dans le cadre de notre document.
// Si nous savons que nous souhaitons accepter chaque révision, nous pouvons le faire de manière plus simple en appelant cette méthode.
doc->AcceptAllRevisions();

ASSERT_EQ(0, doc->get_Revisions()->get_Count());
ASSERT_EQ(u"Hello world! Hello again! This is another revision.", doc->GetText().Trim());
```

## Voir aussi

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
