---
title: "Aspose::Words::MailMerging::MailMerge::Execute méthode"
linktitle: "Exécuter"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::MailMerging::MailMerge::Execute méthode. Effectue une opération de fusion de courrier pour un seul enregistrement en C++."
type: docs
weight: 3000
url: /fr/cpp/aspose.words.mailmerging/mailmerge/execute/
---
## MailMerge::Execute(const System::ArrayPtr\<System::String\>\&, const System::ArrayPtr\<System::SharedPtr\<System::Object\>\>\&) method


Effectue une opération de publipostage pour un enregistrement unique.

```cpp
void Aspose::Words::MailMerging::MailMerge::Execute(const System::ArrayPtr<System::String> &fieldNames, const System::ArrayPtr<System::SharedPtr<System::Object>> &values)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| fieldNames | const System::ArrayPtr\<System::String\>\& | Tableau des noms de champs de fusion. Les noms de champs ne sont pas sensibles à la casse. Si un nom de champ introuvable dans le document est rencontré, il est ignoré. |
| values | const System::ArrayPtr\<System::SharedPtr\<System::Object\>\>\& | Tableau des valeurs à insérer dans les champs de fusion. Le nombre d'éléments de ce tableau doit être identique au nombre d'éléments de *fieldNames*. |
## Remarques


Utilisez cette méthode pour remplir les champs de fusion du document avec des valeurs provenant d'un tableau d'objets.

Cette méthode fusionne les données pour un seul enregistrement. Le tableau des noms de champs et le tableau des valeurs représentent les données d'un seul enregistrement.

Cette méthode n'utilise pas les régions de fusion de courrier.

Cette méthode ignore l'option [RemoveUnusedRegions](../../mailmergecleanupoptions/).

## Exemples



Montre comment fusionner une image à partir d'une URI en tant que donnée de fusion de courrier dans un MERGEFIELD.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Les MERGEFIELDs avec des balises "Image:" recevront une image lors d'une fusion de courrier.
// La chaîne après les deux-points dans la balise "Image:" correspond à un nom de colonne
// dans la source de données dont les cellules contiennent des URI de fichiers image.
builder->InsertField(u"MERGEFIELD  Image:logo_FromWeb ");
builder->InsertField(u"MERGEFIELD  Image:logo_FromFileSystem ");

// Créez une source de données contenant les URI d'images que nous allons fusionner.
// Une URI peut être une URL web pointant vers une image, ou le nom de fichier d'une image sur le système de fichiers local.
System::ArrayPtr<System::String> columns = System::MakeArray<System::String>({u"logo_FromWeb", u"logo_FromFileSystem"});
System::ArrayPtr<System::SharedPtr<System::Object>> URIs = System::MakeArray<System::SharedPtr<System::Object>>({System::ExplicitCast<System::Object>(get_ImageUrl()), System::ExplicitCast<System::Object>(get_ImageDir() + u"Logo.jpg")});

// Exécutez une fusion de courrier sur une source de données contenant une ligne.
doc->get_MailMerge()->Execute(columns, URIs);

doc->Save(get_ArtifactsDir() + u"MailMergeEvent.ImageFromUrl.docx");
```

## Voir aussi

* Class [MailMerge](../)
* Namespace [Aspose::Words::MailMerging](../../)
* Library [Aspose.Words for C++](../../../)
## MailMerge::Execute(const System::SharedPtr\<Aspose::Words::MailMerging::IMailMergeDataSource\>\&) method


Effectue un publipostage à partir d'une source de données personnalisée.

```cpp
void Aspose::Words::MailMerging::MailMerge::Execute(const System::SharedPtr<Aspose::Words::MailMerging::IMailMergeDataSource> &dataSource)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| dataSource | const System::SharedPtr\<Aspose::Words::MailMerging::IMailMergeDataSource\>\& | Un objet qui implémente l'interface personnalisée de source de données de fusion de courrier. |
## Remarques


Utilisez cette méthode pour remplir les champs de fusion de courrier dans le document avec des valeurs provenant de n'importe quelle source de données telle qu'une liste, une table de hachage ou des objets. Vous devez écrire votre propre classe qui implémente l'interface [IMailMergeDataSource](../../imailmergedatasource/).

Vous ne pouvez utiliser cette méthode que lorsque [IsBidiTextSupportedOnUpdate](../../../aspose.words.fields/fieldoptions/get_isbiditextsupportedonupdate/) est **false**, c’est‑à‑dire que vous n'avez pas besoin de la compatibilité des langues de droite à gauche (comme l'arabe ou l'hébreu).

Cette méthode ignore l'option [RemoveUnusedRegions](../../mailmergecleanupoptions/).

## Voir aussi

* Interface [IMailMergeDataSource](../../imailmergedatasource/)
* Class [MailMerge](../)
* Namespace [Aspose::Words::MailMerging](../../)
* Library [Aspose.Words for C++](../../../)
