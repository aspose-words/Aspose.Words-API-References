---
title: "IDocumentLoadingCallback"
linktitle: "IDocumentLoadingCallback"
second_title: "Aspose.Words für Java"
description: "Implementieren Sie dieses Interface, wenn Sie eine eigene benutzerdefinierte Methode während des Ladens eines Dokuments in Java aufrufen möchten."
type: docs
weight: 758
url: /de/java/com.aspose.words/idocumentloadingcallback/
---
```
public interface IDocumentLoadingCallback
```

Implementieren Sie diese Schnittstelle, wenn Sie eine eigene benutzerdefinierte Methode beim Laden eines Dokuments aufrufen möchten.

 **Examples:** 

Zeigt, wie der Benutzer benachrichtigt wird, wenn das Laden des Dokuments die erwartete Ladezeit überschreitet.

```

 public void progressCallback() throws Exception
 {
     LoadingProgressCallback progressCallback = new LoadingProgressCallback();

     LoadOptions loadOptions = new LoadOptions(); { loadOptions.setProgressCallback(progressCallback); }

     try
     {
         new Document(getMyDir() + "Big document.docx", loadOptions);
     }
     catch (IllegalStateException exception)
     {
         System.out.println(exception.getMessage());
         // Handle loading duration issue.
     }
 }

 /// 
 /// Cancel a document loading after the "MaxDuration" seconds.
 /// 
 public static class LoadingProgressCallback implements IDocumentLoadingCallback
 {
     /// 
     /// Ctr.
     /// 
     public LoadingProgressCallback()
     {
         mLoadingStartedAt = new Date();
     }

     /// 
     /// Callback method which called during document loading.
     /// 
     /// Loading arguments.
     public void notify(DocumentLoadingArgs args)
     {
         Date canceledAt = new Date();
         long diff = canceledAt.getTime() - mLoadingStartedAt.getTime();
         long ellapsedSeconds = TimeUnit.MILLISECONDS.toSeconds(diff);

         if (ellapsedSeconds > MAX_DURATION)
             throw new IllegalStateException(MessageFormat.format("EstimatedProgress = {0}; CanceledAt = {1}", args.getEstimatedProgress(), canceledAt));
     }

     /// 
     /// Date and time when document loading is started.
     /// 
     private Date mLoadingStartedAt;

     /// 
     /// Maximum allowed duration in sec.
     /// 
     private static final double MAX_DURATION = 0.5;
 }
 
```
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [notify(DocumentLoadingArgs args)](#notify-com.aspose.words.DocumentLoadingArgs) | Dies wird aufgerufen, um über den Fortschritt des Dokumentenladens zu benachrichtigen. |
### notify(DocumentLoadingArgs args) {#notify-com.aspose.words.DocumentLoadingArgs}
```
public abstract void notify(DocumentLoadingArgs args)
```


Dies wird aufgerufen, um über den Fortschritt des Dokumentenladens zu benachrichtigen.

 **Remarks:** 

Der Hauptzweck dieses Interfaces besteht darin, Anwendungscode zu ermöglichen, den Fortschrittsstatus zu erhalten und den Ladevorgang abzubrechen.

Eine Ausnahme sollte vom Fortschritts-Callback zum Abbruch ausgelöst werden und im aufrufenden Code abgefangen werden.

 **Examples:** 

Zeigt, wie der Benutzer benachrichtigt wird, wenn das Laden des Dokuments die erwartete Ladezeit überschreitet.

```

 public void progressCallback() throws Exception
 {
     LoadingProgressCallback progressCallback = new LoadingProgressCallback();

     LoadOptions loadOptions = new LoadOptions(); { loadOptions.setProgressCallback(progressCallback); }

     try
     {
         new Document(getMyDir() + "Big document.docx", loadOptions);
     }
     catch (IllegalStateException exception)
     {
         System.out.println(exception.getMessage());
         // Handle loading duration issue.
     }
 }

 /// 
 /// Cancel a document loading after the "MaxDuration" seconds.
 /// 
 public static class LoadingProgressCallback implements IDocumentLoadingCallback
 {
     /// 
     /// Ctr.
     /// 
     public LoadingProgressCallback()
     {
         mLoadingStartedAt = new Date();
     }

     /// 
     /// Callback method which called during document loading.
     /// 
     /// Loading arguments.
     public void notify(DocumentLoadingArgs args)
     {
         Date canceledAt = new Date();
         long diff = canceledAt.getTime() - mLoadingStartedAt.getTime();
         long ellapsedSeconds = TimeUnit.MILLISECONDS.toSeconds(diff);

         if (ellapsedSeconds > MAX_DURATION)
             throw new IllegalStateException(MessageFormat.format("EstimatedProgress = {0}; CanceledAt = {1}", args.getEstimatedProgress(), canceledAt));
     }

     /// 
     /// Date and time when document loading is started.
     /// 
     private Date mLoadingStartedAt;

     /// 
     /// Maximum allowed duration in sec.
     /// 
     private static final double MAX_DURATION = 0.5;
 }
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| args | [DocumentLoadingArgs](../../com.aspose.words/documentloadingargs/) | Ein Argument des Ereignisses. |

