---
title: "Aspose::Words::Settings::OdsoFieldMapData classe"
linktitle: "OdsoFieldMapData"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Settings::OdsoFieldMapData class. Spécifie comment une colonne de la source de données externe doit être mappée aux champs de fusion prédéfinis du document. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 5000
url: /fr/cpp/aspose.words.settings/odsofieldmapdata/
---
## OdsoFieldMapData class


Spécifie comment une colonne de la source de données externe doit être mappée aux champs de fusion prédéfinis dans le document. Pour en savoir plus, consultez l'article de documentation [Mail Merge and Reporting](https://docs.aspose.com/words/cpp/mail-merge-and-reporting/).

```cpp
class OdsoFieldMapData : public System::Object
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [Clone](./clone/)() | Renvoie une copie profonde de cet objet. |
| [get_Column](./get_column/)() const | Spécifie l'index zéro‑bas de la colonne dans une source de données externe qui doit être mappée au nom local d'un champ MERGEFIELD spécifique. La valeur par défaut est 0. |
| [get_MappedName](./get_mappedname/)() const | Spécifie le nom du champ de fusion prédéfini qui doit être mappé au numéro de colonne indiqué par la propriété [Column](./get_column/) de ce mappage de champ. La valeur par défaut est une chaîne vide. |
| [get_Name](./get_name/)() const | Spécifie le nom de la colonne dans une source de données externe pour la colonne dont l'index est indiqué par la propriété [Column](./get_column/). La valeur par défaut est une chaîne vide. |
| [get_Type](./get_type/)() const | Indique si un champ de publipostage donné a été mappé à une colonne de la source de données externe ou non. La valeur par défaut est [Default](../odsofieldmappingtype/). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [OdsoFieldMapData](./odsofieldmapdata/)() |  |
| [set_Column](./set_column/)(int32_t) | Spécifie l'index zéro‑bas de la colonne dans une source de données externe qui doit être mappée au nom local d'un champ MERGEFIELD spécifique. La valeur par défaut est 0. |
| [set_MappedName](./set_mappedname/)(const System::String\&) | Spécifie le nom du champ de fusion prédéfini qui doit être mappé au numéro de colonne indiqué par la propriété [Column](./get_column/) de ce mappage de champ. La valeur par défaut est une chaîne vide. |
| [set_Name](./set_name/)(const System::String\&) | Spécifie le nom de la colonne dans une source de données externe pour la colonne dont l'index est indiqué par la propriété [Column](./get_column/). La valeur par défaut est une chaîne vide. |
| [set_Type](./set_type/)(Aspose::Words::Settings::OdsoFieldMappingType) | Indique si un champ de publipostage donné a été mappé à une colonne de la source de données externe ou non. La valeur par défaut est [Default](../odsofieldmappingtype/). |
| static [Type](./type/)() |  |
## Remarques


Microsoft Word propose certains noms de champs de fusion prédéfinis qu’il permet d’insérer dans un document en tant que MERGEFIELD ou d’utiliser dans les champs ADDRESSBLOCK ou GREETINGLINE. Les informations spécifiées dans [OdsoFieldMapData](./) permettent de mapper une colonne de la source de données externe à un seul champ de fusion prédéfini.

## Voir aussi

* Namespace [Aspose::Words::Settings](../)
* Library [Aspose.Words for C++](../../)
