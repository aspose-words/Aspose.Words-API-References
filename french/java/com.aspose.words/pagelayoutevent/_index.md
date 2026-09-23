---
title: "PageLayoutEvent"
linktitle: "PageLayoutEvent"
second_title: "Aspose.Words pour Java"
description: "Un code d'événement déclenché lors de la construction et du rendu du modèle de mise en page en Java."
type: docs
weight: 515
url: /fr/java/com.aspose.words/pagelayoutevent/
---

**Inheritance:**
java.lang.Object
```
public class PageLayoutEvent
```

Un code d'événement déclenché lors de la construction et du rendu du modèle de mise en page.

Le modèle de mise en page est construit en deux étapes. Premièrement, "conversion step", c'est lorsque la mise en page récupère le contenu du document et crée le graphe d'objets. Deuxièmement, "reflow step", c'est lorsque les structures sont divisées, fusionnées et organisées en pages.

Selon l'opération qui a déclenché la construction, le modèle de mise en page peut être ou non rendu davantage au format de page fixe. Par exemple, le calcul du nombre de pages du document ou la mise à jour des champs ne nécessite pas de rendu, alors que l'exportation au PDF le nécessite.

 **Examples:** 

Montre comment suivre les changements de mise en page avec un rappel de mise en page.

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
## Champs

| Champ | Description |
| --- | --- |
| [BUILD_FINISHED](#BUILD-FINISHED) | La construction de la mise en page est terminée. |
| [BUILD_STARTED](#BUILD-STARTED) | La construction de la mise en page a commencé. |
| [CONVERSION_FINISHED](#CONVERSION-FINISHED) | La conversion du modèle de document en mise en page est terminée. |
| [CONVERSION_STARTED](#CONVERSION-STARTED) | La conversion du modèle de document en mise en page a commencé. |
| [NONE](#NONE) | Valeur par défaut |
| [PART_REFLOW_FINISHED](#PART-REFLOW-FINISHED) | Le réagencement de la page est terminé. |
| [PART_REFLOW_STARTED](#PART-REFLOW-STARTED) | Le réagencement de la page a commencé. |
| [PART_RENDERING_FINISHED](#PART-RENDERING-FINISHED) | Le rendu de la page est terminé. |
| [PART_RENDERING_STARTED](#PART-RENDERING-STARTED) | Le rendu de la page a commencé. |
| [REFLOW_FINISHED](#REFLOW-FINISHED) | Le reflow de la mise en page est terminé. |
| [REFLOW_STARTED](#REFLOW-STARTED) | Le reflow de la mise en page a commencé. |
| [WATCH_DOG](#WATCH-DOG) | Correspond à un point de contrôle dans le code qui est souvent visité et qui convient pour interrompre le processus. |
| [length](#length) |  |
## Méthodes

| Méthode | Description |
| --- | --- |
| [fromName(String pageLayoutEventName)](#fromName-java.lang.String) |  |
| [getName(int pageLayoutEvent)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int pageLayoutEvent)](#toString-int) |  |
### BUILD_FINISHED {#BUILD-FINISHED}
```
public static int BUILD_FINISHED
```


La construction de la mise en page est terminée. Déclenché une fois. C’est le dernier événement qui se produit lorsque [Document.updatePageLayout()](../../com.aspose.words/document/\#updatePageLayout) est appelé.

### BUILD_STARTED {#BUILD-STARTED}
```
public static int BUILD_STARTED
```


La construction de la mise en page a commencé. Déclenché une fois. C’est le premier événement qui se produit lorsque [Document.updatePageLayout()](../../com.aspose.words/document/\#updatePageLayout) est appelé.

### CONVERSION_FINISHED {#CONVERSION-FINISHED}
```
public static int CONVERSION_FINISHED
```


La conversion du modèle de document en mise en page est terminée. Déclenchée une fois. Cela se produit lorsque le modèle de mise en page cesse d’extraire le contenu du document.

### CONVERSION_STARTED {#CONVERSION-STARTED}
```
public static int CONVERSION_STARTED
```


La conversion du modèle de document en mise en page a commencé. Déclenchée une fois. Cela se produit lorsque le modèle de mise en page commence à extraire le contenu du document.

### NONE {#NONE}
```
public static int NONE
```


Valeur par défaut

### PART_REFLOW_FINISHED {#PART-REFLOW-FINISHED}
```
public static int PART_REFLOW_FINISHED
```


Le reflow de la page est terminé. Notez que la page peut être reflowée plusieurs fois et que le reflow peut redémarrer avant d’être terminé.

### PART_REFLOW_STARTED {#PART-REFLOW-STARTED}
```
public static int PART_REFLOW_STARTED
```


Le reflow de la page a commencé. Notez que la page peut être reflowée plusieurs fois et que le reflow peut redémarrer avant d’être terminé.

### PART_RENDERING_FINISHED {#PART-RENDERING-FINISHED}
```
public static int PART_RENDERING_FINISHED
```


Le rendu de la page est terminé. Ceci est déclenché une fois par page.

### PART_RENDERING_STARTED {#PART-RENDERING-STARTED}
```
public static int PART_RENDERING_STARTED
```


Le rendu de la page a commencé. Ceci est déclenché une fois par page.

### REFLOW_FINISHED {#REFLOW-FINISHED}
```
public static int REFLOW_FINISHED
```


Le reflow de la mise en page est terminé. Déclenché une fois. Cela se produit lorsque le modèle de mise en page cesse de reflow le contenu du document.

### REFLOW_STARTED {#REFLOW-STARTED}
```
public static int REFLOW_STARTED
```


Le reflow de la mise en page a commencé. Déclenché une fois. Cela se produit lorsque le modèle de mise en page commence à reflow le contenu du document.

### WATCH_DOG {#WATCH-DOG}
```
public static int WATCH_DOG
```


Correspond à un point de contrôle dans le code qui est souvent visité et qui convient pour interrompre le processus.

À l'intérieur de [IPageLayoutCallback.notify(com.aspose.words.PageLayoutCallbackArgs)](../../com.aspose.words/ipagelayoutcallback/\#notify-com.aspose.words.PageLayoutCallbackArgs), lancez une exception personnalisée pour interrompre le processus.

Vous pouvez lancer une exception lors du traitement de tout événement de rappel pour interrompre le processus.

Notez que si le processus est interrompu, le modèle de mise en page reste dans un état indéfini. Cependant, si le processus est interrompu lors du reflow d’une page complète, il devrait être possible d’utiliser le modèle de mise en page jusqu’à la fin de cette page.

### length {#length}
```
public static int length
```


### fromName(String pageLayoutEventName) {#fromName-java.lang.String}
```
public static int fromName(String pageLayoutEventName)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| pageLayoutEventName | java.lang.String |  |

**Returns:**
int
### getName(int pageLayoutEvent) {#getName-int}
```
public static String getName(int pageLayoutEvent)
```




**Parameters:**
| Paramètre | Type | Description |
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
| Paramètre | Type | Description |
| --- | --- | --- |
| pageLayoutEvent | int |  |

**Returns:**
java.lang.String
