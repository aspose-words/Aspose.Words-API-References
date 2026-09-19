---
title: "Aspose::Words::Layout namespace"
linktitle: "Aspose::Words::Layout"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Layout namespace. Il namespace Aspose.Words.Layout fornisce classi che consentono di accedere a informazioni come su quale pagina e dove su una pagina particolari elementi del documento sono posizionati, quando il documento è formattato in pagine in C++."
type: docs
weight: 10000
url: /it/cpp/aspose.words.layout/
---

Il namespace **Aspose.Words.Layout** fornisce classi che consentono di accedere a informazioni come su quale pagina e dove su una pagina sono posizionati i particolari elementi del documento, quando il documento è formattato in pagine.

## Classi

| Classe | Descrizione |
| --- | --- |
| [LayoutCollector](./layoutcollector/) | Questa classe consente di calcolare i numeri di pagina dei nodi del documento. Per saperne di più, visita l'articolo di documentazione [Converting to Fixed-page Format](https://docs.aspose.com/words/cpp/converting-to-fixed-page-format/). |
| [LayoutEnumerator](./layoutenumerator/) | Enumera le entità di layout di pagina di un documento. È possibile utilizzare questa classe per attraversare il modello di layout di pagina. Le proprietà disponibili sono tipo, geometria, testo e indice di pagina dove l'entità è renderizzata, così come la struttura complessiva e le relazioni. Usa la combinazione di [GetEntity()](../) e [Current](./layoutenumerator/get_current/) per spostarti all'entità che corrisponde a un nodo del documento. Per saperne di più, visita l'articolo di documentazione [Converting to Fixed-page Format](https://docs.aspose.com/words/cpp/converting-to-fixed-page-format/). |
| [LayoutOptions](./layoutoptions/) | Contiene le opzioni che consentono di controllare il processo di layout del documento. Per saperne di più, visita l'articolo di documentazione [Converting to Fixed-page Format](https://docs.aspose.com/words/cpp/converting-to-fixed-page-format/). |
| [PageLayoutCallbackArgs](./pagelayoutcallbackargs/) | Un argomento passato a [Notify()](./ipagelayoutcallback/notify/). Per saperne di più, visita l'articolo di documentazione [Converting to Fixed-page Format](https://docs.aspose.com/words/cpp/converting-to-fixed-page-format/). |
| [RevisionOptions](./revisionoptions/) | Consente di controllare come le revisioni del documento vengono gestite durante il processo di layout. Per saperne di più, visita l'articolo di documentazione [Converting to Fixed-page Format](https://docs.aspose.com/words/cpp/converting-to-fixed-page-format/). |
## Interfacce

| Interfaccia | Descrizione |
| --- | --- |
| [IPageLayoutCallback](./ipagelayoutcallback/) | Implementa questa interfaccia se desideri avere il tuo metodo personalizzato chiamato durante la costruzione e il rendering del modello di layout di pagina. |
## Enums

| Enum | Descrizione |
| --- | --- |
| [CommentDisplayMode](./commentdisplaymode/) | Specifica la modalità di rendering per i commenti del documento. |
| [ContinuousSectionRestart](./continuoussectionrestart/) | Rappresenta comportamenti diversi durante il calcolo dei numeri di pagina in una sezione continua che ripristina la numerazione delle pagine. |
| [LayoutEntityType](./layoutentitytype/) | Tipi delle entità di layout. |
| [PageLayoutEvent](./pagelayoutevent/) | Un codice dell'evento sollevato durante la costruzione e il rendering del modello di layout di pagina. Il modello di layout di pagina è costruito in due fasi. Prima, "fase di conversione", in cui il layout di pagina estrae il contenuto del documento e crea il grafo di oggetti. Seconda, "fase di reflow", in cui le strutture sono suddivise, fuse e organizzate in pagine. A seconda dell'operazione che ha innescato la costruzione, il modello di layout di pagina può o non può essere ulteriormente renderizzato in formato pagina fissa. Per esempio, il calcolo del numero di pagine nel documento o l'aggiornamento dei campi non richiedono il rendering, mentre l'esportazione in PDF lo richiede. |
| [RevisionColor](./revisioncolor/) | Consente di specificare il colore delle revisioni del documento. |
| [RevisionTextEffect](./revisiontexteffect/) | Consente di specificare l'effetto di decorazione per le revisioni del testo del documento. |
| [ShowInBalloons](./showinballoons/) | Specifica quali revisioni sono renderizzate in balloon. |
