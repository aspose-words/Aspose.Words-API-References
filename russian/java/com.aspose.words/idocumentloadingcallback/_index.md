---
title: "IDocumentLoadingCallback"
linktitle: "IDocumentLoadingCallback"
second_title: "Aspose.Words для Java"
description: "Реализуйте этот интерфейс, если хотите иметь собственный метод, вызываемый при загрузке документа в Java."
type: docs
weight: 758
url: /ru/java/com.aspose.words/idocumentloadingcallback/
---
```
public interface IDocumentLoadingCallback
```

Реализуйте этот интерфейс, если хотите иметь собственный пользовательский метод, вызываемый при загрузке документа.

 **Examples:** 

Показывает, как уведомить пользователя, если загрузка документа превысила ожидаемое время.

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
## Методы

| Метод | Описание |
| --- | --- |
| [notify(DocumentLoadingArgs args)](#notify-com.aspose.words.DocumentLoadingArgs) | Это вызывается для уведомления о прогрессе загрузки документа. |
### notify(DocumentLoadingArgs args) {#notify-com.aspose.words.DocumentLoadingArgs}
```
public abstract void notify(DocumentLoadingArgs args)
```


Это вызывается для уведомления о прогрессе загрузки документа.

 **Remarks:** 

Основное назначение этого интерфейса — позволить коду приложения получать статус прогресса и прерывать процесс загрузки.

Исключение должно быть выброшено из обратного вызова прогресса для прерывания, и его следует перехватить в коде потребителя.

 **Examples:** 

Показывает, как уведомить пользователя, если загрузка документа превысила ожидаемое время.

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| args | [DocumentLoadingArgs](../../com.aspose.words/documentloadingargs/) | Аргумент события. |

