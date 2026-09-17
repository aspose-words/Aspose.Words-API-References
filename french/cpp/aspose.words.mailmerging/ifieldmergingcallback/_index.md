---
title: "interface Aspose::Words::MailMerging::IFieldMergingCallback"
linktitle: "IFieldMergingCallback"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Interface Aspose::Words::MailMerging::IFieldMergingCallback. Implémentez cette interface si vous souhaitez contrôler la façon dont les données sont insérées dans les champs de fusion lors d'une opération de publipostage en C++."
type: docs
weight: 7000
url: /fr/cpp/aspose.words.mailmerging/ifieldmergingcallback/
---
## IFieldMergingCallback interface


Implémentez cette interface si vous souhaitez contrôler la façon dont les données sont insérées dans les champs de fusion lors d'une opération de fusion de courrier.

```cpp
class IFieldMergingCallback : public virtual System::Object
```

## Méthodes

| Méthode | Description |
| --- | --- |
| virtual [FieldMerging](./fieldmerging/)(System::SharedPtr\<Aspose::Words::MailMerging::FieldMergingArgs\>) | Appelé lorsque le moteur de publipostage Aspose.Words est sur le point d'insérer des données dans un champ de fusion du document. |
| [GetType](./gettype/)() const override |  |
| virtual [ImageFieldMerging](./imagefieldmerging/)(System::SharedPtr\<Aspose::Words::MailMerging::ImageFieldMergingArgs\>) | Appelé lorsque le moteur de publipostage Aspose.Words est sur le point d'insérer une image dans un champ de fusion. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## Voir aussi

* Namespace [Aspose::Words::MailMerging](../)
* Library [Aspose.Words for C++](../../)
