---
title: "Aspose::Words::Layout::PageLayoutEvent enum"
linktitle: "PageLayoutEvent"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Layout::PageLayoutEvent enum. Un codice di evento generato durante la costruzione e il rendering del modello di layout della pagina. Il modello di layout della pagina è costruito in due fasi. Prima, \"conversion step\", è quando il layout della pagina preleva il contenuto del documento e crea il grafo degli oggetti. Seconda, \"reflow step\", è quando le strutture vengono suddivise, unite e organizzate in pagine. A seconda dell'operazione che ha innescato la costruzione, il modello di layout della pagina può o non può essere ulteriormente renderizzato in formato pagina fissa. Per esempio, il calcolo del numero di pagine nel documento o l'aggiornamento dei campi non richiedono il rendering, mentre l'esportazione in PDF lo richiede in C++."
type: docs
weight: 10000
url: /it/cpp/aspose.words.layout/pagelayoutevent/
---
## PageLayoutEvent enum


Un codice dell'evento sollevato durante la costruzione e il rendering del modello di layout di pagina. Il modello di layout di pagina è costruito in due fasi. Prima, "fase di conversione", in cui il layout di pagina estrae il contenuto del documento e crea il grafo di oggetti. Seconda, "fase di reflow", in cui le strutture sono suddivise, fuse e organizzate in pagine. A seconda dell'operazione che ha innescato la costruzione, il modello di layout di pagina può o non può essere ulteriormente renderizzato in formato pagina fissa. Per esempio, il calcolo del numero di pagine nel documento o l'aggiornamento dei campi non richiedono il rendering, mentre l'esportazione in PDF lo richiede.

```cpp
enum class PageLayoutEvent
```

### Valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| None | 0 | Valore predefinito. |
| WatchDog | 1 | Corrisponde a un punto di controllo nel codice che viene spesso visitato e che è adatto per interrompere il processo. Mentre si è all'interno di [Notify()](../ipagelayoutcallback/notify/) lancia un'eccezione personalizzata per interrompere il processo. È possibile lanciare l'eccezione durante la gestione di qualsiasi evento di callback per interrompere il processo. Nota che se il processo viene interrotto il modello di layout della pagina rimane in uno stato indefinito. Se il processo viene interrotto durante il reflow di una pagina completa, tuttavia, dovrebbe essere possibile utilizzare il modello di layout fino alla fine di quella pagina. |
| BuildStarted | 2 | La costruzione del layout della pagina è iniziata. Emessa una volta. Questo è il primo evento che si verifica quando viene chiamato [UpdatePageLayout](../../aspose.words/document/updatepagelayout/). |
| BuildFinished | 3 | La costruzione del layout della pagina è terminata. Emessa una volta. Questo è l'ultimo evento che si verifica quando viene chiamato [UpdatePageLayout](../../aspose.words/document/updatepagelayout/). |
| ConversionStarted | 4 | La conversione del modello di documento in layout della pagina è iniziata. Emessa una volta. Questo avviene quando il modello di layout inizia a prelevare il contenuto del documento. |
| ConversionFinished | 5 | La conversione del modello di documento in layout della pagina è terminata. Emessa una volta. Questo avviene quando il modello di layout smette di prelevare il contenuto del documento. |
| ReflowStarted | 6 | Il reflow del layout della pagina è iniziato. Emessa una volta. Questo avviene quando il modello di layout inizia a fare il reflow del contenuto del documento. |
| ReflowFinished | 7 | Il reflow del layout della pagina è terminato. Emessa una volta. Questo avviene quando il modello di layout smette di fare il reflow del contenuto del documento. |
| PartReflowStarted | 8 | Il reflow della pagina è iniziato. Nota che la pagina può subire il reflow più volte e che il reflow può riavviarsi prima di essere terminato. |
| PartReflowFinished | 9 | Il reflow della pagina è terminato. Nota che la pagina può subire il reflow più volte e che il reflow può riavviarsi prima di essere terminato. |
| PartRenderingStarted | 10 | [Rendering](../../aspose.words.rendering/) della pagina è iniziato. Questo è emesso una volta per pagina. |
| PartRenderingFinished | 11 | [Rendering](../../aspose.words.rendering/) della pagina è terminato. Questo è emesso una volta per pagina. |

## Vedi anche

* Namespace [Aspose::Words::Layout](../)
* Library [Aspose.Words for C++](../../)
