---
title: "PageLayoutEvent"
linktitle: "PageLayoutEvent"
second_title: "Aspose.Words per Java"
description: "Un codice di evento generato durante la costruzione e il rendering del modello di layout di pagina in Java."
type: docs
weight: 515
url: /it/java/com.aspose.words/pagelayoutevent/
---

**Inheritance:**
java.lang.Object
```
public class PageLayoutEvent
```

Un codice di evento generato durante la costruzione e il rendering del modello di layout della pagina.

Il modello di layout di pagina viene costruito in due fasi. Prima, "fase di conversione", in cui il layout di pagina preleva il contenuto del documento e crea il grafo degli oggetti. Seconda, "fase di reflow", in cui le strutture vengono suddivise, unite e organizzate in pagine.

A seconda dell'operazione che ha innescato la costruzione, il modello di layout di pagina può o meno essere ulteriormente renderizzato in formato pagina fissa. Ad esempio, il calcolo del numero di pagine nel documento o l'aggiornamento dei campi non richiedono il rendering, mentre l'esportazione in PDF lo richiede.

 **Examples:** 

Mostra come monitorare le modifiche del layout con una callback di layout.

```

 public void pageLayoutCallback() throws Exception {
     Document doc = new Document();
     doc.getBuiltInDocumentProperties().setTitle("My Document");

     DocumentBuilder builder = new DocumentBuilder(doc);
     builder.writeln("Hello world!");

     doc.getLayoutOptions().setCallback(new RenderPageLayoutCallback());
     doc.updatePageLayout();

     doc.save(getArtifactsDir() + "Layout.PageLayoutCallback.pdf");
 }

 /// 
 /// Notifies us when we save the document to a fixed page format
 /// and renders a page that we perform a page reflow on to an image in the local file system.
 /// 
 private static class RenderPageLayoutCallback implements IPageLayoutCallback {
     public void notify(PageLayoutCallbackArgs a) throws Exception {
         switch (a.getEvent()) {
             case PageLayoutEvent.PART_REFLOW_FINISHED:
                 notifyPartFinished(a);
                 break;
             case PageLayoutEvent.CONVERSION_FINISHED:
                 notifyConversionFinished(a);
                 break;
         }
     }

     private void notifyPartFinished(PageLayoutCallbackArgs a) throws Exception {
         System.out.println(MessageFormat.format("Part at page {0} reflow.", a.getPageIndex() + 1));
         renderPage(a, a.getPageIndex());
     }

     private void notifyConversionFinished(PageLayoutCallbackArgs a) {
         System.out.println(MessageFormat.format("Document \"{0}\" converted to page format.", a.getDocument().getBuiltInDocumentProperties().getTitle()));
     }

     private void renderPage(PageLayoutCallbackArgs a, int pageIndex) throws Exception {
         ImageSaveOptions saveOptions = new ImageSaveOptions(SaveFormat.PNG);
         {
             saveOptions.setPageSet(new PageSet(pageIndex));
         }

         try (FileOutputStream stream = new FileOutputStream(getArtifactsDir() + MessageFormat.format("PageLayoutCallback.page-{0} {1}.png", pageIndex + 1, ++mNum))) {
             a.getDocument().save(stream, saveOptions);
         }
     }

     private int mNum;
 }
 
```
## Campi

| Campo | Descrizione |
| --- | --- |
| [BUILD_FINISHED](#BUILD-FINISHED) | La costruzione del layout di pagina è terminata. |
| [BUILD_STARTED](#BUILD-STARTED) | La costruzione del layout di pagina è iniziata. |
| [CONVERSION_FINISHED](#CONVERSION-FINISHED) | La conversione del modello di documento al layout di pagina è terminata. |
| [CONVERSION_STARTED](#CONVERSION-STARTED) | La conversione del modello di documento al layout di pagina è iniziata. |
| [NONE](#NONE) | Valore predefinito |
| [PART_REFLOW_FINISHED](#PART-REFLOW-FINISHED) | Il reflow della pagina è terminato. |
| [PART_REFLOW_STARTED](#PART-REFLOW-STARTED) | Il reflow della pagina è iniziato. |
| [PART_RENDERING_FINISHED](#PART-RENDERING-FINISHED) | Il rendering della pagina è terminato. |
| [PART_RENDERING_STARTED](#PART-RENDERING-STARTED) | Il rendering della pagina è iniziato. |
| [REFLOW_FINISHED](#REFLOW-FINISHED) | Il ricalcolo del layout della pagina è terminato. |
| [REFLOW_STARTED](#REFLOW-STARTED) | Il ricalcolo del layout della pagina è iniziato. |
| [WATCH_DOG](#WATCH-DOG) | Corrisponde a un punto di controllo nel codice che viene spesso visitato e che è adatto per interrompere il processo. |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fromName(String pageLayoutEventName)](#fromName-java.lang.String) |  |
| [getName(int pageLayoutEvent)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int pageLayoutEvent)](#toString-int) |  |
### BUILD_FINISHED {#BUILD-FINISHED}
```
public static int BUILD_FINISHED
```


La costruzione del layout della pagina è terminata. Generata una sola volta. Questo è l'ultimo evento che si verifica quando viene chiamato [Document.updatePageLayout()](../../com.aspose.words/document/#updatePageLayout).

### BUILD_STARTED {#BUILD-STARTED}
```
public static int BUILD_STARTED
```


La costruzione del layout della pagina è iniziata. Generata una sola volta. Questo è il primo evento che si verifica quando viene chiamato [Document.updatePageLayout()](../../com.aspose.words/document/#updatePageLayout).

### CONVERSION_FINISHED {#CONVERSION-FINISHED}
```
public static int CONVERSION_FINISHED
```


La conversione del modello di documento al layout della pagina è terminata. Generata una sola volta. Questo avviene quando il modello di layout smette di prelevare il contenuto del documento.

### CONVERSION_STARTED {#CONVERSION-STARTED}
```
public static int CONVERSION_STARTED
```


La conversione del modello di documento al layout della pagina è iniziata. Generata una sola volta. Questo avviene quando il modello di layout inizia a prelevare il contenuto del documento.

### NONE {#NONE}
```
public static int NONE
```


Valore predefinito

### PART_REFLOW_FINISHED {#PART-REFLOW-FINISHED}
```
public static int PART_REFLOW_FINISHED
```


Il ricalcolo della pagina è terminato. Nota che la pagina può essere ricalcolata più volte e che il ricalcolo può ricominciare prima di essere terminato.

### PART_REFLOW_STARTED {#PART-REFLOW-STARTED}
```
public static int PART_REFLOW_STARTED
```


Il ricalcolo della pagina è iniziato. Nota che la pagina può essere ricalcolata più volte e che il ricalcolo può ricominciare prima di essere terminato.

### PART_RENDERING_FINISHED {#PART-RENDERING-FINISHED}
```
public static int PART_RENDERING_FINISHED
```


Il rendering della pagina è terminato. Questo è generato una volta per pagina.

### PART_RENDERING_STARTED {#PART-RENDERING-STARTED}
```
public static int PART_RENDERING_STARTED
```


Il rendering della pagina è iniziato. Questo è generato una volta per pagina.

### REFLOW_FINISHED {#REFLOW-FINISHED}
```
public static int REFLOW_FINISHED
```


Il ricalcolo del layout della pagina è terminato. Generato una sola volta. Questo avviene quando il modello di layout smette di ricalcolare il contenuto del documento.

### REFLOW_STARTED {#REFLOW-STARTED}
```
public static int REFLOW_STARTED
```


Il ricalcolo del layout della pagina è iniziato. Generato una sola volta. Questo avviene quando il modello di layout inizia a ricalcolare il contenuto del documento.

### WATCH_DOG {#WATCH-DOG}
```
public static int WATCH_DOG
```


Corrisponde a un punto di controllo nel codice che viene spesso visitato e che è adatto per interrompere il processo.

All'interno di [IPageLayoutCallback.notify(com.aspose.words.PageLayoutCallbackArgs)](../../com.aspose.words/ipagelayoutcallback/#notify-com.aspose.words.PageLayoutCallbackArgs) lancia un'eccezione personalizzata per interrompere il processo.

Puoi lanciare un'eccezione durante la gestione di qualsiasi evento di callback per interrompere il processo.

Nota che se il processo viene interrotto il modello di layout della pagina rimane in uno stato indefinito. Tuttavia, se il processo viene interrotto durante il ricalcolo di una pagina completa, dovrebbe essere possibile utilizzare il modello di layout fino alla fine di quella pagina.

### length {#length}
```
public static int length
```


### fromName(String pageLayoutEventName) {#fromName-java.lang.String}
```
public static int fromName(String pageLayoutEventName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| pageLayoutEventName | java.lang.String |  |

**Returns:**
int
### getName(int pageLayoutEvent) {#getName-int}
```
public static String getName(int pageLayoutEvent)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| pageLayoutEvent | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int pageLayoutEvent) {#toString-int}
```
public static String toString(int pageLayoutEvent)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| pageLayoutEvent | int |  |

**Returns:**
java.lang.String
