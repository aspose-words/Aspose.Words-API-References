---
title: "Metodo Aspose::Words::AI::AiModel::CheckGrammar"
linktitle: "CheckGrammar"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::AI::AiModel::CheckGrammar. Controlla la grammatica del documento fornito. Questa operazione utilizza il modello AI collegato per il controllo grammaticale del documento in C++."
type: docs
weight: 2500
url: /it/cpp/aspose.words.ai/aimodel/checkgrammar/
---
## AiModel::CheckGrammar method


Controlla la grammatica del documento fornito. Questa operazione utilizza il modello [AI](../../) collegato per il controllo grammaticale del documento.

```cpp
virtual System::SharedPtr<Aspose::Words::Document> Aspose::Words::AI::AiModel::CheckGrammar(System::SharedPtr<Aspose::Words::Document> sourceDocument, System::SharedPtr<Aspose::Words::AI::CheckGrammarOptions> options=nullptr)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| sourceDocument | System::SharedPtr\<Aspose::Words::Document\> | Il documento che viene controllato per la grammatica. |
| opzioni | System::SharedPtr\<Aspose::Words::AI::CheckGrammarOptions\> | Impostazioni opzionali per controllare come verrà verificata la grammatica. |

### ReturnValue

Un nuovo [Document](../../../aspose.words/document/) con grammatica controllata.

## Esempi



Mostra come controllare la grammatica di un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Big document.docx");

System::String apiKey = System::Environment::GetEnvironmentVariable(u"API_KEY");
// Utilizza i modelli di linguaggio generativi di OpenAI.
System::SharedPtr<Aspose::Words::AI::AiModel> model = Aspose::Words::AI::AiModel::Create(Aspose::Words::AI::AiModelType::Gpt4OMini)->WithApiKey(apiKey);

auto grammarOptions = System::MakeObject<Aspose::Words::AI::CheckGrammarOptions>();
grammarOptions->set_ImproveStylistics(true);

System::SharedPtr<Aspose::Words::Document> proofedDoc = model->CheckGrammar(doc, grammarOptions);
proofedDoc->Save(get_ArtifactsDir() + u"AI.AiGrammar.docx");
```

## Vedi anche

* Class [Document](../../../aspose.words/document/)
* Class [CheckGrammarOptions](../../checkgrammaroptions/)
* Class [AiModel](../)
* Namespace [Aspose::Words::AI](../../)
* Library [Aspose.Words for C++](../../../)
