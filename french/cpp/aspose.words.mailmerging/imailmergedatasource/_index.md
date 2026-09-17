---
title: "interface Aspose::Words::MailMerging::IMailMergeDataSource"
linktitle: "IMailMergeDataSource"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "interface Aspose::Words::MailMerging::IMailMergeDataSource. Implémentez cette interface pour permettre la fusion de courrier à partir d'une source de données personnalisée, telle qu'une liste d'objets. Les données maître-détail sont également prises en charge en C++."
type: docs
weight: 9000
url: /fr/cpp/aspose.words.mailmerging/imailmergedatasource/
---
## IMailMergeDataSource interface


Implémentez cette interface pour permettre la fusion de courrier à partir d'une source de données personnalisée, telle qu'une liste d'objets. Les données maître-détail sont également prises en charge.

```cpp
class IMailMergeDataSource : public virtual System::Object
```

## Méthodes

| Méthode | Description |
| --- | --- |
| virtual [get_TableName](./get_tablename/)() | Renvoie le nom de la source de données. |
| virtual [GetChildDataSource](./getchilddatasource/)(System::String) | Le moteur de fusion de courrier Aspose.Words invoque cette méthode lorsqu'il rencontre le début d'une région de fusion de courrier imbriquée. |
| [GetType](./gettype/)() const override |  |
| virtual [GetValue](./getvalue/)(System::String, System::SharedPtr\<System::Object\>\&) |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [MoveNext](./movenext/)() | Passe à l'enregistrement suivant dans la source de données. |
| static [Type](./type/)() |  |
## Remarques


Lorsqu'une source de données est créée, elle doit être initialisée pour pointer vers le BOF (avant le premier enregistrement). Le moteur de fusion de courrier Aspose.Words invoquera [MoveNext](./movenext/) pour passer à l'enregistrement suivant, puis invoquera [GetValue()](./getvalue/) pour chaque champ de fusion rencontré dans le document ou la région de fusion de courrier actuelle.

## Voir aussi

* Namespace [Aspose::Words::MailMerging](../)
* Library [Aspose.Words for C++](../../)
