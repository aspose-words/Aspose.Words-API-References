---
title: "Aspose::Words::Saving::DocumentPartSavingArgs classe"
linktitle: "DocumentPartSavingArgs"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::DocumentPartSavingArgs classe. Fournit des données pour le rappel DocumentPartSaving(). Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 4000
url: /fr/cpp/aspose.words.saving/documentpartsavingargs/
---
## DocumentPartSavingArgs class


Fournit des données pour le rappel [DocumentPartSaving()](../idocumentpartsavingcallback/documentpartsaving/). Pour en savoir plus, consultez l'article de documentation [Enregistrer un document](https://docs.aspose.com/words/cpp/save-a-document/).

```cpp
class DocumentPartSavingArgs : public System::Object
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [get_Document](./get_document/)() const | Obtient l'objet document qui est en cours d'enregistrement. |
| [get_DocumentPartFileName](./get_documentpartfilename/)() const | Obtient ou définit le nom de fichier (sans le chemin) où la partie du document sera enregistrée. |
| [get_DocumentPartStream](./get_documentpartstream/)() const | Permet de spécifier le flux où la partie du document sera enregistrée. |
| [get_KeepDocumentPartStreamOpen](./get_keepdocumentpartstreamopen/)() const | Spécifie si Aspose.Words doit garder le flux ouvert ou le fermer après l'enregistrement d'une partie du document. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_DocumentPartFileName](./set_documentpartfilename/)(const System::String\&) | Définisseur pour [Aspose::Words::Saving::DocumentPartSavingArgs::get_DocumentPartFileName](./get_documentpartfilename/). |
| [set_DocumentPartStream](./set_documentpartstream/)(const System::SharedPtr\<System::IO::Stream\>\&) | Définisseur pour [Aspose::Words::Saving::DocumentPartSavingArgs::get_DocumentPartStream](./get_documentpartstream/). |
| [set_DocumentPartStream](./set_documentpartstream/)(std::basic_ostream\<CharType, Traits\>\&) |  |
| [set_KeepDocumentPartStreamOpen](./set_keepdocumentpartstreamopen/)(bool) | Définisseur pour [Aspose::Words::Saving::DocumentPartSavingArgs::get_KeepDocumentPartStreamOpen](./get_keepdocumentpartstreamopen/). |
| static [Type](./type/)() |  |
## Remarques


Lorsque Aspose.Words enregistre un document au format HTML ou formats associés et que [DocumentSplitCriteria](../htmlsaveoptions/get_documentsplitcriteria/) est spécifié, le document est découpé en parties et, par défaut, chaque partie du document est enregistrée dans un fichier séparé.

La classe [DocumentPartSavingArgs](./) vous permet de contrôler la façon dont chaque partie du document sera enregistrée. Elle permet de redéfinir la génération des noms de fichiers ou de contourner complètement l'enregistrement des parties du document dans des fichiers en fournissant vos propres objets de flux.

Pour enregistrer les parties du document dans des flux au lieu de fichiers, utilisez la propriété [DocumentPartStream](./get_documentpartstream/).
## Voir aussi

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
