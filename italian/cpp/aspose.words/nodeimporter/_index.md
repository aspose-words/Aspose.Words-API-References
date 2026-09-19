---
title: "Aspose::Words::NodeImporter class"
linktitle: "NodeImporter"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::NodeImporter class. Consente di eseguire in modo efficiente importazioni ripetute di nodi da un documento all'altro. Per saperne di più, visita l'articolo della documentazione in C++."
type: docs
weight: 44000
url: /it/cpp/aspose.words/nodeimporter/
---
## NodeImporter class


Consente di eseguire in modo efficiente importazioni ripetute di nodi da un documento a un altro. Per saperne di più, visita l'articolo di documentazione [Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/cpp/aspose-words-document-object-model/).

```cpp
class NodeImporter : public System::Object
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [ImportNode](./importnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&, bool) | Importa un nodo da un documento a un altro. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [NodeImporter](./nodeimporter/)(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, Aspose::Words::ImportFormatMode) | Inizializza una nuova istanza della classe [NodeImporter](./). |
| [NodeImporter](./nodeimporter/)(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, Aspose::Words::ImportFormatMode, const System::SharedPtr\<Aspose::Words::ImportFormatOptions\>\&) | Inizializza una nuova istanza della classe [NodeImporter](./). |
| static [Type](./type/)() |  |
## Note


Aspose.Words fornisce funzionalità per copiare e spostare facilmente frammenti tra documenti Microsoft Word. Questo è noto come "importazione di nodi". Prima di poter inserire un frammento da un documento a un altro, è necessario "importarlo". L'importazione crea un clone profondo del nodo originale, pronto per essere inserito nel documento di destinazione.

Il modo più semplice per importare un nodo è utilizzare il metodo [ImportNode()](../) fornito dall'oggetto [DocumentBase](../documentbase/).

Tuttavia, quando è necessario importare nodi da un documento a un altro più volte, è preferibile utilizzare la classe [NodeImporter](./). La classe [NodeImporter](./) consente di ridurre al minimo il numero di stili e elenchi creati nel documento di destinazione.

Copiare o spostare frammenti da un documento Microsoft Word a un altro presenta una serie di sfide tecniche per Aspose.Words. In un documento Word, gli stili e la formattazione degli elenchi sono memorizzati centralmente, separatamente dal testo del documento. I paragrafi e le sequenze di testo fanno semplicemente riferimento agli stili tramite identificatori unici interni.

Le difficoltà derivano dal fatto che gli stili e gli elenchi differiscono tra documenti. Ad esempio, per copiare un paragrafo formattato con lo stile Titolo 1 da un documento a un altro, è necessario considerare diversi aspetti: decidere se copiare lo stile Titolo 1 dal documento di origine a quello di destinazione, clonare il paragrafo, aggiornare il paragrafo clonato affinché faccia riferimento allo stile Titolo 1 corretto nel documento di destinazione. Se lo stile deve essere copiato, tutti gli stili a cui fa riferimento (basati sullo stile e sullo stile del paragrafo successivo) devono essere analizzati e possibilmente copiati anch'essi, e così via. Problemi simili si verificano quando si copiano paragrafi puntati o numerati perché Microsoft Word memorizza le definizioni degli elenchi separatamente dal testo.

La classe [NodeImporter](./) è come un contesto, che contiene le "tabelle di traduzione" durante l'importazione. Traduce correttamente tra stili ed elenchi nei documenti di origine e destinazione.

## Vedi anche

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
