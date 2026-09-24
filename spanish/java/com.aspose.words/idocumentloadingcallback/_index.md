---
title: "IDocumentLoadingCallback"
linktitle: "IDocumentLoadingCallback"
second_title: "Aspose.Words para Java"
description: "Implemente esta interfaz si desea tener su propio método personalizado llamado durante la carga de un documento en Java."
type: docs
weight: 758
url: /es/java/com.aspose.words/idocumentloadingcallback/
---
```
public interface IDocumentLoadingCallback
```

Implemente esta interfaz si desea tener su propio método personalizado llamado durante la carga de un documento.

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
## Métodos

| Método | Descripción |
| --- | --- |
| [notify(DocumentLoadingArgs args)](#notify-com.aspose.words.DocumentLoadingArgs) | Esto se llama para notificar el progreso de carga del documento. |
### notify(DocumentLoadingArgs args) {#notify-com.aspose.words.DocumentLoadingArgs}
```
public abstract void notify(DocumentLoadingArgs args)
```


Esto se llama para notificar el progreso de carga del documento.

 **Remarks:** 

El uso principal de esta interfaz es permitir que el código de la aplicación obtenga el estado de progreso y abortar el proceso de carga.

Se debe lanzar una excepción desde la devolución de llamada de progreso para abortar y debe ser capturada en el código del consumidor.

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

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| args | [DocumentLoadingArgs](../../com.aspose.words/documentloadingargs/) | Un argumento del evento. |

