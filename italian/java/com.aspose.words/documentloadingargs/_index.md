---
title: "DocumentLoadingArgs"
linktitle: "DocumentLoadingArgs"
second_title: "Aspose.Words per Java"
description: "Un argomento passato a IDocumentLoadingCallback.notifycom.aspose.words.DocumentLoadingArgs in Java."
type: docs
weight: 166
url: /it/java/com.aspose.words/documentloadingargs/
---

**Inheritance:**
java.lang.Object
```
public class DocumentLoadingArgs
```

Un argomento passato a [IDocumentLoadingCallback.notify(com.aspose.words.DocumentLoadingArgs)](../../com.aspose.words/idocumentloadingcallback/\\#notify-com.aspose.words.DocumentLoadingArgs).

Per saperne di più, visita l'articolo di documentazione [ Specify Load Options ][Specify Load Options].

 **Examples:** 

Mostra come notificare l'utente se il caricamento del documento ha superato il tempo di caricamento previsto.

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


[Specify Load Options]: https://docs.aspose.com/words/java/specify-load-options/
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [getEstimatedProgress()](#getEstimatedProgress) | Progresso percentuale stimato complessivo. |
### getEstimatedProgress() {#getEstimatedProgress}
```
public double getEstimatedProgress()
```


Progresso percentuale stimato complessivo.

 **Examples:** 

Mostra come notificare l'utente se il caricamento del documento ha superato il tempo di caricamento previsto.

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

**Returns:**
double - Il valore double corrispondente.
