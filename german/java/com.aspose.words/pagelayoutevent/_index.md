---
title: "PageLayoutEvent"
linktitle: "PageLayoutEvent"
second_title: "Aspose.Words für Java"
description: "Ein Code für ein Ereignis, das während des Aufbaus und der Darstellung des Seitenlayoutmodells in Java ausgelöst wird."
type: docs
weight: 515
url: /de/java/com.aspose.words/pagelayoutevent/
---

**Inheritance:**
java.lang.Object
```
public class PageLayoutEvent
```

Ein Ereigniscode, der während des Aufbaus und Renderns des Seitenlayout‑Modells ausgelöst wird.

Das Seitenlayoutmodell wird in zwei Schritten erstellt. Erstens der "Konvertierungsschritt", bei dem das Seitenlayout den Dokumentinhalt abruft und einen Objektgraphen erstellt. Zweitens der "Reflow-Schritt", bei dem Strukturen aufgeteilt, zusammengeführt und zu Seiten angeordnet werden.

Abhängig von der Operation, die den Aufbau ausgelöst hat, kann das Seitenlayoutmodell weiter in ein festes Seitenformat gerendert werden oder nicht. Beispielsweise erfordert die Berechnung der Seitenzahl im Dokument oder das Aktualisieren von Feldern kein Rendering, während der Export nach PDF dies tut.

 **Examples:** 

Zeigt, wie Layout-Änderungen mit einem Layout-Callback verfolgt werden können.

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
## Felder

| Feld | Beschreibung |
| --- | --- |
| [BUILD_FINISHED](#BUILD-FINISHED) | Der Aufbau des Seitenlayouts ist abgeschlossen. |
| [BUILD_STARTED](#BUILD-STARTED) | Der Aufbau des Seitenlayouts hat begonnen. |
| [CONVERSION_FINISHED](#CONVERSION-FINISHED) | Die Konvertierung des Dokumentmodells zum Seitenlayout ist abgeschlossen. |
| [CONVERSION_STARTED](#CONVERSION-STARTED) | Die Konvertierung des Dokumentmodells zum Seitenlayout hat begonnen. |
| [NONE](#NONE) | Standardwert |
| [PART_REFLOW_FINISHED](#PART-REFLOW-FINISHED) | Der Reflow der Seite ist abgeschlossen. |
| [PART_REFLOW_STARTED](#PART-REFLOW-STARTED) | Der Reflow der Seite hat begonnen. |
| [PART_RENDERING_FINISHED](#PART-RENDERING-FINISHED) | Das Rendern der Seite ist abgeschlossen. |
| [PART_RENDERING_STARTED](#PART-RENDERING-STARTED) | Das Rendern der Seite hat begonnen. |
| [REFLOW_FINISHED](#REFLOW-FINISHED) | Der Reflow des Seitenlayouts ist abgeschlossen. |
| [REFLOW_STARTED](#REFLOW-STARTED) | Das Umfließen des Seitenlayouts hat begonnen. |
| [WATCH_DOG](#WATCH-DOG) | Entspricht einem Prüfpunkt im Code, der häufig besucht wird und sich zum Abbrechen des Prozesses eignet. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String pageLayoutEventName)](#fromName-java.lang.String) |  |
| [getName(int pageLayoutEvent)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int pageLayoutEvent)](#toString-int) |  |
### BUILD_FINISHED {#BUILD-FINISHED}
```
public static int BUILD_FINISHED
```


Der Aufbau des Seitenlayouts ist abgeschlossen. Wird einmal ausgelöst. Dies ist das letzte Ereignis, das auftritt, wenn [Document.updatePageLayout()](../../com.aspose.words/document/\#updatePageLayout) aufgerufen wird.

### BUILD_STARTED {#BUILD-STARTED}
```
public static int BUILD_STARTED
```


Der Aufbau des Seitenlayouts hat begonnen. Wird einmal ausgelöst. Dies ist das erste Ereignis, das auftritt, wenn [Document.updatePageLayout()](../../com.aspose.words/document/\#updatePageLayout) aufgerufen wird.

### CONVERSION_FINISHED {#CONVERSION-FINISHED}
```
public static int CONVERSION_FINISHED
```


Die Konvertierung des Dokumentmodells in das Seitenlayout ist abgeschlossen. Wird einmal ausgelöst. Dies geschieht, wenn das Layoutmodell aufhört, Dokumentinhalte zu ziehen.

### CONVERSION_STARTED {#CONVERSION-STARTED}
```
public static int CONVERSION_STARTED
```


Die Konvertierung des Dokumentmodells in das Seitenlayout hat begonnen. Wird einmal ausgelöst. Dies geschieht, wenn das Layoutmodell beginnt, Dokumentinhalte zu ziehen.

### NONE {#NONE}
```
public static int NONE
```


Standardwert

### PART_REFLOW_FINISHED {#PART-REFLOW-FINISHED}
```
public static int PART_REFLOW_FINISHED
```


Das Umfließen der Seite ist abgeschlossen. Beachten Sie, dass die Seite mehrfach umfließen kann und dass das Umfließen vor dem Abschluss neu gestartet werden kann.

### PART_REFLOW_STARTED {#PART-REFLOW-STARTED}
```
public static int PART_REFLOW_STARTED
```


Das Umfließen der Seite hat begonnen. Beachten Sie, dass die Seite mehrfach umfließen kann und dass das Umfließen vor dem Abschluss neu gestartet werden kann.

### PART_RENDERING_FINISHED {#PART-RENDERING-FINISHED}
```
public static int PART_RENDERING_FINISHED
```


Das Rendern der Seite ist abgeschlossen. Dies wird einmal pro Seite ausgelöst.

### PART_RENDERING_STARTED {#PART-RENDERING-STARTED}
```
public static int PART_RENDERING_STARTED
```


Das Rendern der Seite hat begonnen. Dies wird einmal pro Seite ausgelöst.

### REFLOW_FINISHED {#REFLOW-FINISHED}
```
public static int REFLOW_FINISHED
```


Das Umfließen des Seitenlayouts ist abgeschlossen. Wird einmal ausgelöst. Dies geschieht, wenn das Layoutmodell aufhört, Dokumentinhalte umfließen zu lassen.

### REFLOW_STARTED {#REFLOW-STARTED}
```
public static int REFLOW_STARTED
```


Das Umfließen des Seitenlayouts hat begonnen. Wird einmal ausgelöst. Dies geschieht, wenn das Layoutmodell beginnt, Dokumentinhalte umfließen zu lassen.

### WATCH_DOG {#WATCH-DOG}
```
public static int WATCH_DOG
```


Entspricht einem Prüfpunkt im Code, der häufig besucht wird und sich zum Abbrechen des Prozesses eignet.

Während Sie sich innerhalb von [IPageLayoutCallback.notify(com.aspose.words.PageLayoutCallbackArgs)](../../com.aspose.words/ipagelayoutcallback/\#notify-com.aspose.words.PageLayoutCallbackArgs) befinden, werfen Sie eine benutzerdefinierte Ausnahme, um den Prozess abzubrechen.

Sie können beim Umgang mit einem beliebigen Callback-Ereignis eine Ausnahme werfen, um den Prozess abzubrechen.

Beachten Sie, dass bei einem Abbruch des Prozesses das Seitenlayoutmodell in einem undefinierten Zustand verbleibt. Wenn der Prozess jedoch beim Umfließen einer vollständigen Seite abgebrochen wird, sollte es möglich sein, das Layoutmodell bis zum Ende dieser Seite zu verwenden.

### length {#length}
```
public static int length
```


### fromName(String pageLayoutEventName) {#fromName-java.lang.String}
```
public static int fromName(String pageLayoutEventName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| pageLayoutEventName | java.lang.String |  |

**Returns:**
int
### getName(int pageLayoutEvent) {#getName-int}
```
public static String getName(int pageLayoutEvent)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| pageLayoutEvent | int |  |

**Returns:**
java.lang.String
