---
title: "Aspose::Words::AI::AnthropicAiModel::Summarize metodo"
linktitle: "Summarize"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::AI::AnthropicAiModel::Summarize metodo. Genera riepiloghi per un array di documenti, con opzioni per controllare la lunghezza del riepilogo e altre impostazioni. Questo metodo utilizza il modello AI connesso per elaborare ciascun documento nell'array in C++."
type: docs
weight: 4000
url: /it/cpp/aspose.words.ai/anthropicaimodel/summarize/
---
## AnthropicAiModel::Summarize(System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Document\>\>, System::SharedPtr\<Aspose::Words::AI::SummarizeOptions\>) method


Genera riepiloghi per un array di documenti, con opzioni per controllare la lunghezza del riepilogo e altre impostazioni. Questo metodo utilizza il modello [AI](../../) connesso per elaborare ciascun documento nell'array.

```cpp
System::SharedPtr<Aspose::Words::Document> Aspose::Words::AI::AnthropicAiModel::Summarize(System::ArrayPtr<System::SharedPtr<Aspose::Words::Document>> sourceDocuments, System::SharedPtr<Aspose::Words::AI::SummarizeOptions> options=nullptr) override
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| sourceDocuments | System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Document\>\> | Un array di documenti da riassumere. |
| opzioni | System::SharedPtr\<Aspose::Words::AI::SummarizeOptions\> | Impostazioni opzionali per controllare la lunghezza del riassunto e altri parametri |

### ReturnValue

Una versione riassunta del contenuto del documento.

## Vedi anche

* Class [Document](../../../aspose.words/document/)
* Class [SummarizeOptions](../../summarizeoptions/)
* Class [AnthropicAiModel](../)
* Namespace [Aspose::Words::AI](../../)
* Library [Aspose.Words for C++](../../../)
## AnthropicAiModel::Summarize(System::SharedPtr\<Aspose::Words::Document\>, System::SharedPtr\<Aspose::Words::AI::SummarizeOptions\>) method


Genera un riassunto del documento specificato, con opzioni per regolare la lunghezza del riassunto. Questa operazione utilizza il modello [AI](../../) connesso per l'elaborazione del contenuto.

```cpp
System::SharedPtr<Aspose::Words::Document> Aspose::Words::AI::AnthropicAiModel::Summarize(System::SharedPtr<Aspose::Words::Document> sourceDocument, System::SharedPtr<Aspose::Words::AI::SummarizeOptions> options=nullptr) override
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| sourceDocument | System::SharedPtr\<Aspose::Words::Document\> | Il documento da riassumere. |
| opzioni | System::SharedPtr\<Aspose::Words::AI::SummarizeOptions\> | Impostazioni opzionali per controllare la lunghezza del riassunto e altri parametri. |

### ReturnValue

Una versione riassunta del contenuto del documento.

## Vedi anche

* Class [Document](../../../aspose.words/document/)
* Class [SummarizeOptions](../../summarizeoptions/)
* Class [AnthropicAiModel](../)
* Namespace [Aspose::Words::AI](../../)
* Library [Aspose.Words for C++](../../../)
