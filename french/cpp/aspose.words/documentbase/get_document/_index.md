---
title: "Aspose::Words::DocumentBase::get_Document méthode"
linktitle: "get_Document"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::DocumentBase::get_Document méthode. Obtient cette instance en C++."
type: docs
weight: 3000
url: /fr/cpp/aspose.words/documentbase/get_document/
---
## DocumentBase::get_Document method


Obtient cette instance.

```cpp
System::SharedPtr<Aspose::Words::DocumentBase> Aspose::Words::DocumentBase::get_Document() const override
```


## Exemples



Montre comment créer un document simple.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Les nouveaux objets Document sont, par défaut, fournis avec l'ensemble minimal de nœuds
// nécessaires pour commencer à ajouter du contenu tel que du texte et des formes : une Section, un Corps et un Paragraphe.
doc->AppendChild<System::SharedPtr<Aspose::Words::Section>>(System::MakeObject<Aspose::Words::Section>(doc))->AppendChild<System::SharedPtr<Aspose::Words::Body>>(System::MakeObject<Aspose::Words::Body>(doc))->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(System::MakeObject<Aspose::Words::Paragraph>(doc))->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!"));
```

## Voir aussi

* Class [DocumentBase](../)
* Class [DocumentBase](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
