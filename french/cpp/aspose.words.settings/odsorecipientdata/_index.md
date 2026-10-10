---
title: "Classe Aspose::Words::Settings::OdsoRecipientData"
linktitle: "OdsoRecipientData"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Classe Aspose::Words::Settings::OdsoRecipientData. Représente les informations concernant un enregistrement unique d’une source de données externe qui doit être exclu de la fusion de courrier. Pour en savoir plus, consultez l’article de documentation en C++."
type: docs
weight: 7000
url: /fr/cpp/aspose.words.settings/odsorecipientdata/
---
## OdsoRecipientData class


Représente les informations concernant un enregistrement unique d'une source de données externe qui doit être exclu de la fusion et publipostage. Pour en savoir plus, consultez l'article de documentation [Mail Merge and Reporting](https://docs.aspose.com/words/cpp/mail-merge-and-reporting/).

```cpp
class OdsoRecipientData : public System::Object
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [Clone](./clone/)() | Renvoie une copie profonde de cet objet. |
| [get_Active](./get_active/)() const | Spécifie si l’enregistrement provenant de la source de données doit être importé dans un document lors de l’exécution de la fusion de courrier. La valeur par défaut est **true**. |
| [get_Column](./get_column/)() const | Spécifie la colonne de la source de données contenant les données uniques pour l’enregistrement actuel. La valeur par défaut est 0. |
| [get_Hash](./get_hash/)() const | Représente le code de hachage pour cet enregistrement. Parfois, Microsoft Word utilise le [Hash](./get_hash/) d’un enregistrement complet au lieu d’une valeur [UniqueTag](./get_uniquetag/). La valeur par défaut est 0. |
| [get_UniqueTag](./get_uniquetag/)() const | Spécifie le contenu d’un enregistrement donné dans la colonne contenant les données uniques. La valeur par défaut est **null**. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [OdsoRecipientData](./odsorecipientdata/)() |  |
| [set_Active](./set_active/)(bool) | Spécifie si l’enregistrement provenant de la source de données doit être importé dans un document lors de l’exécution de la fusion de courrier. La valeur par défaut est **true**. |
| [set_Column](./set_column/)(int32_t) | Spécifie la colonne de la source de données contenant les données uniques pour l’enregistrement actuel. La valeur par défaut est 0. |
| [set_Hash](./set_hash/)(int32_t) | Représente le code de hachage pour cet enregistrement. Parfois, Microsoft Word utilise le [Hash](./get_hash/) d’un enregistrement complet au lieu d’une valeur [UniqueTag](./get_uniquetag/). La valeur par défaut est 0. |
| [set_UniqueTag](./set_uniquetag/)(const System::ArrayPtr\<uint8_t\>\&) | Spécifie le contenu d’un enregistrement donné dans la colonne contenant les données uniques. La valeur par défaut est **null**. |
| static [Type](./type/)() |  |
## Remarques


Si un enregistrement doit être fusionné dans un document fusionné, aucune information n’est requise à son sujet. En revanche, si un enregistrement donné ne doit pas être fusionné dans un document fusionné, la valeur de la clé unique pour cet enregistrement doit être stockée dans la propriété [UniqueTag](./get_uniquetag/) de cet objet afin d’indiquer cette exclusion.
## Voir aussi

* Namespace [Aspose::Words::Settings](../)
* Library [Aspose.Words for C++](../../)
