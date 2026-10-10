---
title: "Méthode Aspose::Words::MailMerging::MailMerge::ExecuteWithRegions"
linktitle: "ExecuteWithRegions"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::MailMerging::MailMerge::ExecuteWithRegions. Effectue une fusion de courrier à partir d’une source de données personnalisée avec des régions de fusion de courrier en C++."
type: docs
weight: 4000
url: /fr/cpp/aspose.words.mailmerging/mailmerge/executewithregions/
---
## MailMerge::ExecuteWithRegions(const System::SharedPtr\<Aspose::Words::MailMerging::IMailMergeDataSource\>\&) method


Effectue une fusion de courrier à partir d’une source de données personnalisée avec des régions de fusion de courrier.

```cpp
void Aspose::Words::MailMerging::MailMerge::ExecuteWithRegions(const System::SharedPtr<Aspose::Words::MailMerging::IMailMergeDataSource> &dataSource)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| dataSource | const System::SharedPtr\<Aspose::Words::MailMerging::IMailMergeDataSource\>\& | Un objet qui implémente l'interface personnalisée de source de données de fusion de courrier. |
## Remarques


Utilisez cette méthode pour remplir les champs de fusion de courrier dans le document avec des valeurs provenant de n’importe quelle source de données personnalisée, telle qu’un fichier XML ou des collections d’objets métier. Vous devez écrire votre propre classe qui implémente l’interface [IMailMergeDataSource](../../imailmergedatasource/).

Vous ne pouvez utiliser cette méthode que lorsque [IsBidiTextSupportedOnUpdate](../../../aspose.words.fields/fieldoptions/get_isbiditextsupportedonupdate/) est **false**, c’est‑à‑dire que vous n'avez pas besoin de la compatibilité des langues de droite à gauche (comme l'arabe ou l'hébreu).

## Voir aussi

* Interface [IMailMergeDataSource](../../imailmergedatasource/)
* Class [MailMerge](../)
* Namespace [Aspose::Words::MailMerging](../../)
* Library [Aspose.Words for C++](../../../)
## MailMerge::ExecuteWithRegions(const System::SharedPtr\<Aspose::Words::MailMerging::IMailMergeDataSourceRoot\>\&) method


Effectue une fusion de courrier à partir d’une source de données personnalisée avec des régions de fusion de courrier.

```cpp
void Aspose::Words::MailMerging::MailMerge::ExecuteWithRegions(const System::SharedPtr<Aspose::Words::MailMerging::IMailMergeDataSourceRoot> &dataSourceRoot)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| dataSourceRoot | const System::SharedPtr\<Aspose::Words::MailMerging::IMailMergeDataSourceRoot\>\& | Un objet qui implémente l’interface racine de source de données personnalisée pour la fusion de courrier. |
## Remarques


Utilisez cette méthode pour remplir les champs de fusion de courrier dans le document avec des valeurs provenant de n’importe quelle source de données personnalisée, telle qu’un fichier XML ou des collections d’objets métier. Vous devez écrire vos propres classes qui implémentent les interfaces [IMailMergeDataSourceRoot](../../imailmergedatasourceroot/) et [IMailMergeDataSource](../../imailmergedatasource/).

Vous ne pouvez utiliser cette méthode que lorsque [IsBidiTextSupportedOnUpdate](../../../aspose.words.fields/fieldoptions/get_isbiditextsupportedonupdate/) est **false**, c’est‑à‑dire que vous n'avez pas besoin de la compatibilité des langues de droite à gauche (comme l'arabe ou l'hébreu).

## Voir aussi

* Interface [IMailMergeDataSourceRoot](../../imailmergedatasourceroot/)
* Class [MailMerge](../)
* Namespace [Aspose::Words::MailMerging](../../)
* Library [Aspose.Words for C++](../../../)
