---
title: "Aspose::Words::MailMerging::IMailMergeCallback interface"
linktitle: "IMailMergeCallback"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::MailMerging::IMailMergeCallback interface. Implémentez cette interface si vous souhaitez recevoir des notifications pendant l'exécution de la fusion de courrier en C++."
type: docs
weight: 8000
url: /fr/cpp/aspose.words.mailmerging/imailmergecallback/
---
## IMailMergeCallback interface


Implémentez cette interface si vous souhaitez recevoir des notifications pendant l'exécution de la fusion de courrier.

```cpp
class IMailMergeCallback : public virtual System::Object
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [TagsReplaced](./tagsreplaced/)() | Appelé lorsque les balises de texte "mustache" sont remplacées par des champs MERGEFIELD. |
| static [Type](./type/)() |  |
## Voir aussi

* Namespace [Aspose::Words::MailMerging](../)
* Library [Aspose.Words for C++](../../)
