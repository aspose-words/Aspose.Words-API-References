---
title: "Método Aspose::Words::AI::OpenAiModel::Summarize"
linktitle: "Summarize"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::AI::OpenAiModel::Summarize. Genera resúmenes para una matriz de documentos, con opciones para controlar la longitud del resumen y otras configuraciones. Este método utiliza el modelo de IA conectado para procesar cada documento en la matriz en C++."
type: docs
weight: 3334
url: /es/cpp/aspose.words.ai/openaimodel/summarize/
---
## OpenAiModel::Summarize(System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Document\>\>, System::SharedPtr\<Aspose::Words::AI::SummarizeOptions\>) method


Genera resúmenes para una matriz de documentos, con opciones para controlar la longitud del resumen y otras configuraciones. Este método utiliza el modelo de [AI](../../) conectado para procesar cada documento en la matriz.

```cpp
System::SharedPtr<Aspose::Words::Document> Aspose::Words::AI::OpenAiModel::Summarize(System::ArrayPtr<System::SharedPtr<Aspose::Words::Document>> sourceDocuments, System::SharedPtr<Aspose::Words::AI::SummarizeOptions> options=nullptr) override
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| sourceDocuments | System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Document\>\> | Una matriz de documentos para resumir. |
| opciones | System::SharedPtr\<Aspose::Words::AI::SummarizeOptions\> | Configuraciones opcionales para controlar la longitud del resumen y otros parámetros |

### ReturnValue

Una versión resumida del contenido del documento.

## Ver también

* Class [Document](../../../aspose.words/document/)
* Class [SummarizeOptions](../../summarizeoptions/)
* Class [OpenAiModel](../)
* Namespace [Aspose::Words::AI](../../)
* Library [Aspose.Words for C++](../../../)
## OpenAiModel::Summarize(System::SharedPtr\<Aspose::Words::Document\>, System::SharedPtr\<Aspose::Words::AI::SummarizeOptions\>) method


Genera un resumen del documento especificado, con opciones para ajustar la longitud del resumen. Esta operación aprovecha el modelo [AI](../../) conectado para el procesamiento de contenido.

```cpp
System::SharedPtr<Aspose::Words::Document> Aspose::Words::AI::OpenAiModel::Summarize(System::SharedPtr<Aspose::Words::Document> sourceDocument, System::SharedPtr<Aspose::Words::AI::SummarizeOptions> options=nullptr) override
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| sourceDocument | System::SharedPtr\<Aspose::Words::Document\> | El documento a resumir. |
| opciones | System::SharedPtr\<Aspose::Words::AI::SummarizeOptions\> | Configuraciones opcionales para controlar la longitud del resumen y otros parámetros. |

### ReturnValue

Una versión resumida del contenido del documento.

## Ver también

* Class [Document](../../../aspose.words/document/)
* Class [SummarizeOptions](../../summarizeoptions/)
* Class [OpenAiModel](../)
* Namespace [Aspose::Words::AI](../../)
* Library [Aspose.Words for C++](../../../)
