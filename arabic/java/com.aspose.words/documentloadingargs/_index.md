---
title: "DocumentLoadingArgs"
linktitle: "DocumentLoadingArgs"
second_title: "Aspose.Words لـ Java"
description: "معامل يُمرَّر إلى IDocumentLoadingCallback.notifycom.aspose.words.DocumentLoadingArgs في Java."
type: docs
weight: 166
url: /ar/java/com.aspose.words/documentloadingargs/
---

**Inheritance:**
java.lang.Object
```
public class DocumentLoadingArgs
```

معامل يُمرَّر إلى [IDocumentLoadingCallback.notify(com.aspose.words.DocumentLoadingArgs)](../../com.aspose.words/idocumentloadingcallback/\#notify-com.aspose.words.DocumentLoadingArgs).

لمزيد من المعلومات، زر مقالة الوثائق [ Specify Load Options ][Specify Load Options].

 **Examples:** 

يوضح كيفية إبلاغ المستخدم إذا تجاوز تحميل المستند الوقت المتوقع للتحميل.

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
## الطرق

| طريقة | الوصف |
| --- | --- |
| [getEstimatedProgress()](#getEstimatedProgress) | النسبة المئوية التقديرية العامة للتقدم. |
### getEstimatedProgress() {#getEstimatedProgress}
```
public double getEstimatedProgress()
```


النسبة المئوية التقديرية العامة للتقدم.

 **Examples:** 

يوضح كيفية إبلاغ المستخدم إذا تجاوز تحميل المستند الوقت المتوقع للتحميل.

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
double - القيمة المقابلة للـ double.
