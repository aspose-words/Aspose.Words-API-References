---
title: "Aspose::Words::Drawing::OleFormat classe"
linktitle: "OleFormat"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::OleFormat classe. Fournit un accès aux données d'un objet OLE ou d'un contrôle ActiveX. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 8000
url: /fr/cpp/aspose.words.drawing/oleformat/
---
## OleFormat class


Fournit l'accès aux données d'un objet OLE ou d'un contrôle ActiveX. Pour en savoir plus, consultez l'article de documentation [Working with Ole Objects](https://docs.aspose.com/words/cpp/working-with-ole-objects/) .

```cpp
class OleFormat : public System::Object
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [get_AutoUpdate](./get_autoupdate/)() | Spécifie si le lien vers l'objet OLE est automatiquement mis à jour ou non dans Microsoft Word. |
| [get_Clsid](./get_clsid/)() | Obtient le CLSID de l'objet OLE. |
| [get_IconCaption](./get_iconcaption/)() | Obtient la légende de l'icône de l'objet OLE. Dans le cas où l'objet OLE n'a pas d'icône ou qu'une légende ne peut pas être récupérée, renvoie une chaîne vide. |
| [get_IsLink](./get_islink/)() | Renvoie **true** si l'objet OLE est lié (lorsque [SourceFullName](./get_sourcefullname/) est spécifié). |
| [get_IsLocked](./get_islocked/)() | Spécifie si le lien vers l'objet OLE est verrouillé contre les mises à jour. |
| [get_OleControl](./get_olecontrol/)() | Obtient les objets [OleControl](./get_olecontrol/) si cet objet OLE est un contrôle ActiveX. Sinon, cette propriété est null. |
| [get_OleIcon](./get_oleicon/)() | Obtient l'aspect d'affichage de l'objet OLE. Lorsque **true**, l'objet OLE est affiché sous forme d'icône. Lorsque **false**, l'objet OLE est affiché sous forme de contenu. |
| [get_OlePackage](./get_olepackage/)() | Fournit un accès à [OlePackage](../olepackage/) si l'objet OLE est un package OLE. Renvoie **null** sinon. |
| [get_ProgId](./get_progid/)() | Obtient ou définit le ProgID de l'objet OLE. |
| [get_SourceFullName](./get_sourcefullname/)() | Obtient ou définit le chemin et le nom du fichier source pour l'objet OLE lié. |
| [get_SourceItem](./get_sourceitem/)() | Obtient ou définit une chaîne utilisée pour identifier la partie du fichier source qui est liée. |
| [get_SuggestedExtension](./get_suggestedextension/)() | Obtient l'extension de fichier suggérée pour l'objet incorporé actuel si vous souhaitez l'enregistrer dans un fichier. |
| [get_SuggestedFileName](./get_suggestedfilename/)() | Obtient le nom de fichier suggéré pour l'objet incorporé actuel si vous souhaitez l'enregistrer dans un fichier. |
| [GetOleEntry](./getoleentry/)(const System::String\&) | Obtient l'entrée de données de l'objet OLE. |
| [GetRawData](./getrawdata/)() | Obtient les données brutes de l'objet OLE. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Save](./save/)(const System::SharedPtr\<System::IO::Stream\>\&) | Enregistre les données de l'objet intégré dans le flux spécifié. |
| [Save](./save/)(const System::String\&) | Enregistre les données de l'objet intégré dans un fichier avec le nom spécifié. |
| [Save](./save/)(std::basic_ostream\<CharType, Traits\>\&) |  |
| [set_AutoUpdate](./set_autoupdate/)(bool) | Mutateur pour [Aspose::Words::Drawing::OleFormat::get_AutoUpdate](./get_autoupdate/). |
| [set_IsLocked](./set_islocked/)(bool) | Mutateur pour [Aspose::Words::Drawing::OleFormat::get_IsLocked](./get_islocked/). |
| [set_ProgId](./set_progid/)(const System::String\&) | Mutateur pour [Aspose::Words::Drawing::OleFormat::get_ProgId](./get_progid/). |
| [set_SourceFullName](./set_sourcefullname/)(const System::String\&) | Mutateur pour [Aspose::Words::Drawing::OleFormat::get_SourceFullName](./get_sourcefullname/). |
| [set_SourceItem](./set_sourceitem/)(const System::String\&) | Mutateur pour [Aspose::Words::Drawing::OleFormat::get_SourceItem](./get_sourceitem/). |
| static [Type](./type/)() |  |
## Remarques


Utilisez la propriété [OleFormat](../shape/get_oleformat/) pour accéder aux données d'un objet OLE. Vous ne créez pas d'instances de la classe [OleFormat](./) directement.

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

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
