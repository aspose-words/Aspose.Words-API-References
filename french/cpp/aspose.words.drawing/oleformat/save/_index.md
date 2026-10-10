---
title: "Aspose::Words::Drawing::OleFormat::Save méthode"
linktitle: "Save"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::OleFormat::Save méthode. Enregistre les données de l'objet incorporé dans le flux spécifié en C++."
type: docs
weight: 19000
url: /fr/cpp/aspose.words.drawing/oleformat/save/
---
## OleFormat::Save(const System::SharedPtr\<System::IO::Stream\>\&) method


Enregistre les données de l'objet intégré dans le flux spécifié.

```cpp
void Aspose::Words::Drawing::OleFormat::Save(const System::SharedPtr<System::IO::Stream> &stream)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| flux | const System::SharedPtr\<System::IO::Stream\>\& | Où enregistrer les données de l'objet. |
## Remarques


Il incombe à l'appelant de libérer le flux.

## Exemples



Montre comment extraire des objets OLE intégrés dans des fichiers.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"OLE spreadsheet.docm");
auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));

// L'objet OLE dans la première forme est une feuille de calcul Microsoft Excel.
System::SharedPtr<Aspose::Words::Drawing::OleFormat> oleFormat = shape->get_OleFormat();

ASSERT_EQ(u"Excel.Sheet.12", oleFormat->get_ProgId());

// Notre objet n'est ni mis à jour automatiquement ni verrouillé contre les mises à jour.
ASSERT_FALSE(oleFormat->get_AutoUpdate());
ASPOSE_ASSERT_EQ(false, oleFormat->get_IsLocked());

// Si nous prévoyons d'enregistrer l'objet OLE dans un fichier du système de fichiers local,
// nous pouvons utiliser la propriété "SuggestedExtension" pour déterminer quelle extension de fichier appliquer au fichier.
ASSERT_EQ(u".xlsx", oleFormat->get_SuggestedExtension());

// Ci-dessous, deux méthodes pour enregistrer un objet OLE dans un fichier du système de fichiers local.
// 1 -  Enregistrez-le via un flux :
{
    auto fs = System::MakeObject<System::IO::FileStream>(get_ArtifactsDir() + u"OLE spreadsheet extracted via stream" + oleFormat->get_SuggestedExtension(), System::IO::FileMode::Create);
    oleFormat->Save(fs);
}

// 2 -  Enregistrez-le directement dans un nom de fichier :
oleFormat->Save(get_ArtifactsDir() + u"OLE spreadsheet saved directly" + oleFormat->get_SuggestedExtension());
```

## Voir aussi

* Class [OleFormat](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
## OleFormat::Save(const System::String\&) method


Enregistre les données de l'objet intégré dans un fichier avec le nom spécifié.

```cpp
void Aspose::Words::Drawing::OleFormat::Save(const System::String &fileName)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| fileName | const System::String\& | Nom du fichier pour enregistrer les données de l'objet OLE. |

## Exemples



Montre comment extraire des objets OLE intégrés dans des fichiers.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"OLE spreadsheet.docm");
auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));

// L'objet OLE dans la première forme est une feuille de calcul Microsoft Excel.
System::SharedPtr<Aspose::Words::Drawing::OleFormat> oleFormat = shape->get_OleFormat();

ASSERT_EQ(u"Excel.Sheet.12", oleFormat->get_ProgId());

// Notre objet n'est ni mis à jour automatiquement ni verrouillé contre les mises à jour.
ASSERT_FALSE(oleFormat->get_AutoUpdate());
ASPOSE_ASSERT_EQ(false, oleFormat->get_IsLocked());

// Si nous prévoyons d'enregistrer l'objet OLE dans un fichier du système de fichiers local,
// nous pouvons utiliser la propriété "SuggestedExtension" pour déterminer quelle extension de fichier appliquer au fichier.
ASSERT_EQ(u".xlsx", oleFormat->get_SuggestedExtension());

// Ci-dessous, deux méthodes pour enregistrer un objet OLE dans un fichier du système de fichiers local.
// 1 -  Enregistrez-le via un flux :
{
    auto fs = System::MakeObject<System::IO::FileStream>(get_ArtifactsDir() + u"OLE spreadsheet extracted via stream" + oleFormat->get_SuggestedExtension(), System::IO::FileMode::Create);
    oleFormat->Save(fs);
}

// 2 -  Enregistrez-le directement dans un nom de fichier :
oleFormat->Save(get_ArtifactsDir() + u"OLE spreadsheet saved directly" + oleFormat->get_SuggestedExtension());
```

## Voir aussi

* Class [OleFormat](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
## OleFormat::Save(std::basic_ostream\<CharType, Traits\>\&) method




```cpp
template<typename CharType,typename Traits> void Aspose::Words::Drawing::OleFormat::Save(std::basic_ostream<CharType, Traits> &stream)
```

## Voir aussi

* Class [OleFormat](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
