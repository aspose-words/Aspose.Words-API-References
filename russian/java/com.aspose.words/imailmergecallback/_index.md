---
title: "IMailMergeCallback"
linktitle: "IMailMergeCallback"
second_title: "Aspose.Words для Java"
description: "Реализуйте этот интерфейс, если хотите получать уведомления во время выполнения слияния почты в Java."
type: docs
weight: 775
url: /ru/java/com.aspose.words/imailmergecallback/
---
```
public interface IMailMergeCallback
```

Реализуйте этот интерфейс, если вы хотите получать уведомления во время выполнения слияния почты.

 **Examples:** 

Показывает, как определить пользовательскую логику обработки событий во время слияния почты.

```

 public void testTagsReplacedEventShouldRisedWithUseNonMergeFieldsOption() throws Exception {
     Document document = new Document();
     document.getMailMerge().setUseNonMergeFields(true);

     MailMergeCallbackStub mailMergeCallbackStub = new MailMergeCallbackStub();
     document.getMailMerge().setMailMergeCallback(mailMergeCallbackStub);

     document.getMailMerge().execute(new String[0], new Object[0]);

     Assert.assertEquals(mailMergeCallbackStub.getTagsReplacedCounter(), 1);
 }

 private static class MailMergeCallbackStub implements IMailMergeCallback {
     public void tagsReplaced() {
         mTagsReplacedCounter++;
     }

     public int getTagsReplacedCounter() {
         return mTagsReplacedCounter;
     }

     private int mTagsReplacedCounter;
 }
 
```
## Методы

| Метод | Описание |
| --- | --- |
| [tagsReplaced()](#tagsReplaced) | Вызывается, когда текстовые теги \"mustache\" заменяются полями MERGEFIELD. |
### tagsReplaced() {#tagsReplaced}
```
public abstract void tagsReplaced()
```


Вызывается, когда текстовые теги \"mustache\" заменяются полями MERGEFIELD.

 **Examples:** 

Показывает, как определить пользовательскую логику обработки событий во время слияния почты.

```

 public void testTagsReplacedEventShouldRisedWithUseNonMergeFieldsOption() throws Exception {
     Document document = new Document();
     document.getMailMerge().setUseNonMergeFields(true);

     MailMergeCallbackStub mailMergeCallbackStub = new MailMergeCallbackStub();
     document.getMailMerge().setMailMergeCallback(mailMergeCallbackStub);

     document.getMailMerge().execute(new String[0], new Object[0]);

     Assert.assertEquals(mailMergeCallbackStub.getTagsReplacedCounter(), 1);
 }

 private static class MailMergeCallbackStub implements IMailMergeCallback {
     public void tagsReplaced() {
         mTagsReplacedCounter++;
     }

     public int getTagsReplacedCounter() {
         return mTagsReplacedCounter;
     }

     private int mTagsReplacedCounter;
 }
 
```

