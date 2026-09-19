---
title: "classe Aspose::Words::Saving::DocumentPartSavingArgs"
linktitle: "DocumentPartSavingArgs"
second_title: "Riferimento API Aspose.Words per C++"
description: "classe Aspose::Words::Saving::DocumentPartSavingArgs. Fornisce dati per il callback DocumentPartSaving(). Per saperne di più, visita l'articolo di documentazione in C++."
type: docs
weight: 4000
url: /it/cpp/aspose.words.saving/documentpartsavingargs/
---
## DocumentPartSavingArgs class


Fornisce dati per il callback [DocumentPartSaving()](../idocumentpartsavingcallback/documentpartsaving/). Per saperne di più, visita l'articolo di documentazione [Save a Document](https://docs.aspose.com/words/cpp/save-a-document/).

```cpp
class DocumentPartSavingArgs : public System::Object
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [get_Document](./get_document/)() const | Ottiene l'oggetto documento che viene salvato. |
| [get_DocumentPartFileName](./get_documentpartfilename/)() const | Ottiene o imposta il nome file (senza percorso) dove verrà salvata la parte del documento. |
| [get_DocumentPartStream](./get_documentpartstream/)() const | Consente di specificare lo stream dove verrà salvata la parte del documento. |
| [get_KeepDocumentPartStreamOpen](./get_keepdocumentpartstreamopen/)() const | Specifica se Aspose.Words deve mantenere lo stream aperto o chiuderlo dopo aver salvato una parte del documento. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_DocumentPartFileName](./set_documentpartfilename/)(const System::String\&) | Impostatore per [Aspose::Words::Saving::DocumentPartSavingArgs::get_DocumentPartFileName](./get_documentpartfilename/). |
| [set_DocumentPartStream](./set_documentpartstream/)(const System::SharedPtr\<System::IO::Stream\>\&) | Impostatore per [Aspose::Words::Saving::DocumentPartSavingArgs::get_DocumentPartStream](./get_documentpartstream/). |
| [set_DocumentPartStream](./set_documentpartstream/)(std::basic_ostream\<CharType, Traits\>\&) |  |
| [set_KeepDocumentPartStreamOpen](./set_keepdocumentpartstreamopen/)(bool) | Impostatore per [Aspose::Words::Saving::DocumentPartSavingArgs::get_KeepDocumentPartStreamOpen](./get_keepdocumentpartstreamopen/). |
| static [Type](./type/)() |  |
## Note


Quando Aspose.Words salva un documento in HTML o formati correlati e viene specificato [DocumentSplitCriteria](../htmlsaveoptions/get_documentsplitcriteria/), il documento viene suddiviso in parti e, per impostazione predefinita, ogni parte del documento viene salvata in un file separato.

La classe [DocumentPartSavingArgs](./) consente di controllare come verrà salvata ogni parte del documento. Permette di ridefinire come vengono generati i nomi dei file o di evitare completamente il salvataggio delle parti del documento in file fornendo i propri oggetti stream.

Per salvare le parti del documento in stream invece che in file, utilizza la proprietà [DocumentPartStream](./get_documentpartstream/).
## Vedi anche

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
