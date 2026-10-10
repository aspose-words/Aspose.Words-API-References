---
title: "classe Aspose::Words::Saving::PageSavingArgs"
linktitle: "PageSavingArgs"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "classe Aspose::Words::Saving::PageSavingArgs. Fournit des données pour l'événement PageSaving(). Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 19000
url: /fr/cpp/aspose.words.saving/pagesavingargs/
---
## PageSavingArgs class


Fournit des données pour l'événement [PageSaving()](../ipagesavingcallback/pagesaving/). Pour en savoir plus, consultez l'article de documentation [Programming with Documents](https://docs.aspose.com/words/cpp/programming-with-documents/).

```cpp
class PageSavingArgs : public System::Object
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [get_KeepPageStreamOpen](./get_keeppagestreamopen/)() const | Spécifie si Aspose.Words doit garder le flux ouvert ou le fermer après l'enregistrement d'une page de document. |
| [get_PageFileName](./get_pagefilename/)() const | Obtient le nom de fichier où la page du document sera enregistrée. |
| [get_PageIndex](./get_pageindex/)() const | Indice de la page actuelle. |
| [get_PageStream](./get_pagestream/)() const | Permet de spécifier le flux où la page du document sera enregistrée. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [PageSavingArgs](./pagesavingargs/)() |  |
| [set_KeepPageStreamOpen](./set_keeppagestreamopen/)(bool) | Définisseur pour [Aspose::Words::Saving::PageSavingArgs::get_KeepPageStreamOpen](./get_keeppagestreamopen/). |
| [set_PageFileName](./set_pagefilename/)(const System::String\&) | Définit le nom de fichier où la page du document sera enregistrée. |
| [set_PageStream](./set_pagestream/)(const System::SharedPtr\<System::IO::Stream\>\&) | Définisseur pour [Aspose::Words::Saving::PageSavingArgs::get_PageStream](./get_pagestream/). |
| [set_PageStream](./set_pagestream/)(std::basic_ostream\<CharType, Traits\>\&) |  |
| static [Type](./type/)() |  |
## Voir aussi

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
