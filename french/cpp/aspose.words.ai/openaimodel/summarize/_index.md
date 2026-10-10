---
title: "Méthode Aspose::Words::AI::OpenAiModel::Summarize"
linktitle: "Résumer"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::AI::OpenAiModel::Summarize. Génère des résumés pour un tableau de documents, avec des options pour contrôler la longueur du résumé et d'autres paramètres. Cette méthode utilise le modèle d'IA connecté pour traiter chaque document du tableau en C++."
type: docs
weight: 3334
url: /fr/cpp/aspose.words.ai/openaimodel/summarize/
---
## OpenAiModel::Summarize(System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Document\>\>, System::SharedPtr\<Aspose::Words::AI::SummarizeOptions\>) method


Génère des résumés pour un tableau de documents, avec des options pour contrôler la longueur du résumé et d'autres paramètres. Cette méthode utilise le modèle [AI](../../) connecté pour traiter chaque document du tableau.

```cpp
System::SharedPtr<Aspose::Words::Document> Aspose::Words::AI::OpenAiModel::Summarize(System::ArrayPtr<System::SharedPtr<Aspose::Words::Document>> sourceDocuments, System::SharedPtr<Aspose::Words::AI::SummarizeOptions> options=nullptr) override
```


| Paramètre | Type | Description |
| --- | --- | --- |
| sourceDocuments | System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Document\>\> | Un tableau de documents à résumer. |
| options | System::SharedPtr\<Aspose::Words::AI::SummarizeOptions\> | Paramètres optionnels pour contrôler la longueur du résumé et d'autres paramètres |

### ReturnValue

Une version résumée du contenu du document.

## Voir aussi

* Class [Document](../../../aspose.words/document/)
* Class [SummarizeOptions](../../summarizeoptions/)
* Class [OpenAiModel](../)
* Namespace [Aspose::Words::AI](../../)
* Library [Aspose.Words for C++](../../../)
## OpenAiModel::Summarize(System::SharedPtr\<Aspose::Words::Document\>, System::SharedPtr\<Aspose::Words::AI::SummarizeOptions\>) method


Génère un résumé du document spécifié, avec des options pour ajuster la longueur du résumé. Cette opération utilise le modèle [AI](../../) connecté pour le traitement du contenu.

```cpp
System::SharedPtr<Aspose::Words::Document> Aspose::Words::AI::OpenAiModel::Summarize(System::SharedPtr<Aspose::Words::Document> sourceDocument, System::SharedPtr<Aspose::Words::AI::SummarizeOptions> options=nullptr) override
```


| Paramètre | Type | Description |
| --- | --- | --- |
| sourceDocument | System::SharedPtr\<Aspose::Words::Document\> | Le document à résumer. |
| options | System::SharedPtr\<Aspose::Words::AI::SummarizeOptions\> | Paramètres optionnels pour contrôler la longueur du résumé et d'autres paramètres. |

### ReturnValue

Une version résumée du contenu du document.

## Voir aussi

* Class [Document](../../../aspose.words/document/)
* Class [SummarizeOptions](../../summarizeoptions/)
* Class [OpenAiModel](../)
* Namespace [Aspose::Words::AI](../../)
* Library [Aspose.Words for C++](../../../)
