---
title: "DocumentLoadingArgs"
linktitle: "DocumentLoadingArgs"
second_title: "Aspose.Words Java için"
description: "Java'da IDocumentLoadingCallback.notifycom.aspose.words.DocumentLoadingArgs içine geçirilen bir argüman."
type: docs
weight: 166
url: /tr/java/com.aspose.words/documentloadingargs/
---

**Inheritance:**
java.lang.Object
```
public class DocumentLoadingArgs
```

[IDocumentLoadingCallback.notify(com.aspose.words.DocumentLoadingArgs)](../../com.aspose.words/idocumentloadingcallback/\#notify-com.aspose.words.DocumentLoadingArgs) içine geçirilen bir argüman.

Daha fazla bilgi edinmek için, [ Specify Load Options ][Specify Load Options] dokümantasyon makalesini ziyaret edin.

 **Examples:** 

Belge yüklemesinin beklenen süreden fazla sürmesi durumunda kullanıcıyı nasıl bilgilendireceğinizi gösterir.

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
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [getEstimatedProgress()](#getEstimatedProgress) | Genel tahmini yüzde ilerleme. |
### getEstimatedProgress() {#getEstimatedProgress}
```
public double getEstimatedProgress()
```


Genel tahmini yüzde ilerleme.

 **Examples:** 

Belge yüklemesinin beklenen süreden fazla sürmesi durumunda kullanıcıyı nasıl bilgilendireceğinizi gösterir.

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
double - İlgili  double  değeri.
