---
title: "Aspose::Words::Document::JoinRunsWithSameFormatting method"
linktitle: "JoinRunsWithSameFormatting"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Document::JoinRunsWithSameFormatting method. Unisce le run con lo stesso formato in tutti i paragrafi del documento in C++."
type: docs
weight: 65000
url: /it/cpp/aspose.words/document/joinrunswithsameformatting/
---
## Document::JoinRunsWithSameFormatting method


Unisce le sequenze con la stessa formattazione in tutti i paragrafi del documento.

```cpp
int32_t Aspose::Words::Document::JoinRunsWithSameFormatting()
```


### ReturnValue

Numero di unioni eseguite. Quando **N** run adiacenti vengono unite, contano come **N - 1** unioni.
## Note


Questo è un metodo di ottimizzazione. Alcuni documenti contengono run adiacenti con lo stesso formato. Di solito ciò avviene se un documento è stato modificato intensamente manualmente. È possibile ridurre le dimensioni del documento e velocizzare l'elaborazione successiva unendo queste run.

L'operazione controlla ogni nodo [Paragraph](../../paragraph/) nel documento alla ricerca di nodi [Run](../../run/) adiacenti con proprietà identiche. Ignora gli identificatori unici utilizzati per tracciare le sessioni di modifica della creazione e della modifica delle run. La prima run in ogni sequenza di unione accumula tutto il testo. Le run rimanenti vengono eliminate dal documento.

## Esempi



Mostra come unire le run in un documento per ridurre le run non necessarie.
```cpp
// Apri un documento che contiene run di testo adiacenti con formattazione identica,
// che si verifica comunemente se modifichiamo lo stesso paragrafo più volte in Microsoft Word.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

// Se un numero qualsiasi di queste run è adiacente con formattazione identica,
// allora il documento può essere semplificato.
ASSERT_EQ(317, doc->GetChildNodes(Aspose::Words::NodeType::Run, true)->get_Count());

// Combina tali run con questo metodo e verifica il numero di unioni di run che avverranno.
ASSERT_EQ(121, doc->JoinRunsWithSameFormatting());

// Il numero di unioni e il numero di run che abbiamo dopo l'unione
// dovrebbero corrispondere al numero di run che avevamo inizialmente.
ASSERT_EQ(196, doc->GetChildNodes(Aspose::Words::NodeType::Run, true)->get_Count());
```

## Vedi anche

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
