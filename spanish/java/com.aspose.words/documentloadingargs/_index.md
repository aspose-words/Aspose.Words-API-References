---
title: "DocumentLoadingArgs"
linktitle: "DocumentLoadingArgs"
second_title: "Aspose.Words para Java"
description: "Un argumento pasado a IDocumentLoadingCallback.notifycom.aspose.words.DocumentLoadingArgs en Java."
type: docs
weight: 166
url: /es/java/com.aspose.words/documentloadingargs/
---

**Inheritance:**
java.lang.Object
```
public class DocumentLoadingArgs
```

Un argumento pasado a [IDocumentLoadingCallback.notify(com.aspose.words.DocumentLoadingArgs)](../../com.aspose.words/idocumentloadingcallback/\#notify-com.aspose.words.DocumentLoadingArgs).

Para obtener más información, visite el artículo de documentación [ Specify Load Options ][Specify Load Options].

 **Examples:** 

Muestra cómo notificar al usuario si la carga del documento supera el tiempo de carga esperado.

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
## Métodos

| Método | Descripción |
| --- | --- |
| [getEstimatedProgress()](#getEstimatedProgress) | Progreso porcentual estimado total. |
### getEstimatedProgress() {#getEstimatedProgress}
```
public double getEstimatedProgress()
```


Progreso porcentual estimado total.

 **Examples:** 

Muestra cómo notificar al usuario si la carga del documento supera el tiempo de carga esperado.

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
double - El valor  double  correspondiente.
