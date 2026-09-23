---
title: "IPageLayoutCallback"
linktitle: "IPageLayoutCallback"
second_title: "Aspose.Words für Java"
description: "Implementieren Sie dieses Interface, wenn Sie Ihre eigene benutzerdefinierte Methode haben möchten, die während des Aufbaus und der Darstellung des Seitenlayoutmodells in Java aufgerufen wird."
type: docs
weight: 779
url: /de/java/com.aspose.words/ipagelayoutcallback/
---
```
public interface IPageLayoutCallback
```

Implementieren Sie dieses Interface, wenn Sie eine eigene benutzerdefinierte Methode während des Aufbaus und Renderns des Seitenlayoutmodells aufrufen lassen möchten.

 **Remarks:** 

Der Hauptzweck dieses Interfaces besteht darin, Anwendungscode zu ermöglichen, den Aufbauprozess abzubrechen.

Es ist möglich, das Seitenlayoutmodell nur für einige Seiten zu Beginn des Dokuments zu erstellen, dann den Vorgang abzubrechen und nur das bereits Erstellte zu rendern.

Beachten Sie jedoch, dass die Rendering-Ergebnisse möglicherweise nicht dem entsprechen, was für jede Seite gerendert worden wäre, wenn der Prozess abgeschlossen wäre.

Diese Technik funktioniert möglicherweise nicht bei jedem Dokument oder kann vollständig fehlschlagen.

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
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [notify(PageLayoutCallbackArgs args)](#notify-com.aspose.words.PageLayoutCallbackArgs) | Dies wird aufgerufen, um über den Fortschritt des Layout-Aufbaus und des Renderings zu informieren. |
### notify(PageLayoutCallbackArgs args) {#notify-com.aspose.words.PageLayoutCallbackArgs}
```
public abstract void notify(PageLayoutCallbackArgs args)
```


Dies wird aufgerufen, um über den Fortschritt des Layout-Aufbaus und des Renderings zu informieren.

 **Remarks:** 

Eine von der Implementierung ausgelöste Ausnahme bricht den Layout-Aufbauprozess ab.

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

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| args | [PageLayoutCallbackArgs](../../com.aspose.words/pagelayoutcallbackargs/) | Ein Argument des Ereignisses. |

