---
title: "Aspose::Words::Settings::OdsoDataSourceType enum"
linktitle: "OdsoDataSourceType"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Settings::OdsoDataSourceType enum. Spécifie le type de la source de données externe à connecter dans le cadre des informations de connexion ODSO en C++."
type: docs
weight: 19000
url: /fr/cpp/aspose.words.settings/odsodatasourcetype/
---
## OdsoDataSourceType enum


Spécifie le type de la source de données externe à laquelle se connecter dans le cadre des informations de connexion ODSO.

```cpp
enum class OdsoDataSourceType
```

### Valeurs

| Nom | Valeur | Description |
| --- | --- | --- |
| Texte | 0 | Spécifie qu'un document donné a été connecté à un fichier texte. Possiblement wdMergeSubTypeOther. |
| Database | 1 | Spécifie qu'un document donné a été connecté à une base de données. Possiblement wdMergeSubTypeAccess. |
| Carnet d'adresses | 2 | Spécifie qu'un document donné a été connecté à un carnet d'adresses de contacts. Possiblement wdMergeSubTypeOAL. |
| Document1 | 3 | Spécifie qu'un document donné a été connecté à un autre format de document pris en charge par l'application productrice. Possiblement wdMergeSubTypeOLEDBWord. |
| Document2 | 4 | Spécifie qu'un document donné a été connecté à un autre format de document pris en charge par l'application productrice. Possiblement wdMergeSubTypeWorks. |
| Native | 5 | Spécifie qu'un document donné a été connecté à un autre format de document natif à l'application productrice. Possiblement wdMergeSubTypeOLEDBText. |
| Email | 6 | Spécifie qu'un document donné a été connecté à une application de messagerie. Possiblement wdMergeSubTypeOutlook. |
| None | 7 | Le type de la source de données externe n'est pas spécifié. Possiblement wdMergeSubTypeWord. |
| Héritage | 8 | Spécifie qu'un document donné a été connecté à un format de document hérité pris en charge par l'application productrice. Possiblement wdMergeSubTypeWord2000. |
| Maître | 9 | Spécifie qu'un document donné a été connecté à une source de données qui agrège d'autres sources de données. |
| Default | n/a | Égal à [None](./). |

## Remarques


La spécification OOXML est très vague pour cette énumération. Je suppose qu'elle pourrait correspondre à l'énumération WdMergeSubType [http://msdn.microsoft.com/en-us/library/bb237801.aspx](http://msdn.microsoft.com/en-us/library/bb237801.aspx).

## Voir aussi

* Namespace [Aspose::Words::Settings](../)
* Library [Aspose.Words for C++](../../)
