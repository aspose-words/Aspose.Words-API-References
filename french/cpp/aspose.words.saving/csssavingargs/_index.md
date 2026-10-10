---
title: "Aspose::Words::Saving::CssSavingArgs classe"
linktitle: "CssSavingArgs"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::CssSavingArgs classe. Fournit des données pour l'événement CssSaving(). Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 2000
url: /fr/cpp/aspose.words.saving/csssavingargs/
---
## CssSavingArgs class


Fournit des données pour l'événement [CssSaving()](../icsssavingcallback/csssaving/). Pour en savoir plus, consultez l'article de documentation [Save a Document](https://docs.aspose.com/words/cpp/save-a-document/).

```cpp
class CssSavingArgs : public System::Object
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [get_CssStream](./get_cssstream/)() const | Permet de spécifier le flux où les informations CSS seront enregistrées. |
| [get_Document](./get_document/)() const | Obtient l'objet document qui est actuellement en cours d'enregistrement. |
| [get_IsExportNeeded](./get_isexportneeded/)() const | Permet de spécifier si le CSS sera exporté vers un fichier et intégré au document HTML. La valeur par défaut est **true**. Lorsque cette propriété est **false**, les informations CSS ne seront pas enregistrées dans un fichier CSS et ne seront pas intégrées au document HTML. |
| [get_KeepCssStreamOpen](./get_keepcssstreamopen/)() const | Spécifie si Aspose.Words doit garder le flux ouvert ou le fermer après l'enregistrement des informations CSS. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_CssStream](./set_cssstream/)(const System::SharedPtr\<System::IO::Stream\>\&) | Définisseur pour [Aspose::Words::Saving::CssSavingArgs::get_CssStream](./get_cssstream/). |
| [set_CssStream](./set_cssstream/)(std::basic_ostream\<CharType, Traits\>\&) |  |
| [set_IsExportNeeded](./set_isexportneeded/)(bool) | Permet de spécifier si le CSS sera exporté vers un fichier et intégré au document HTML. La valeur par défaut est **true**. Lorsque cette propriété est **false**, les informations CSS ne seront pas enregistrées dans un fichier CSS et ne seront pas intégrées au document HTML. |
| [set_KeepCssStreamOpen](./set_keepcssstreamopen/)(bool) | Définisseur pour [Aspose::Words::Saving::CssSavingArgs::get_KeepCssStreamOpen](./get_keepcssstreamopen/). |
| static [Type](./type/)() |  |
## Remarques


Par défaut, lorsque Aspose.Words enregistre un document au format HTML, il enregistre les informations CSS en ligne (comme valeur de l'attribut **style** sur chaque élément).

[CssSavingArgs](./) allows to save CSS information into file by providing your own stream object.

Pour enregistrer le CSS dans un flux, utilisez la propriété [CssStream](./get_cssstream/).

Pour empêcher l'enregistrement du CSS dans un fichier et son intégration au document HTML, utilisez la propriété [IsExportNeeded](./get_isexportneeded/).
## Voir aussi

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
