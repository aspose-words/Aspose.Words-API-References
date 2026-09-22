---
title: "IMailMergeCallback"
linktitle: "IMailMergeCallback"
second_title: "Aspose.Words لـ Java"
description: "نفّذ هذه الواجهة إذا كنت ترغب في تلقي إشعارات أثناء تنفيذ دمج البريد في Java."
type: docs
weight: 775
url: /ar/java/com.aspose.words/imailmergecallback/
---
```
public interface IMailMergeCallback
```

قم بتنفيذ هذه الواجهة إذا كنت تريد تلقي الإشعارات أثناء تنفيذ دمج البريد.

 **Examples:** 

يوضح كيفية تعريف منطق مخصص لمعالجة الأحداث أثناء دمج البريد.

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
## الطرق

| طريقة | الوصف |
| --- | --- |
| [tagsReplaced()](#tagsReplaced) | يُستدعى عندما يتم استبدال وسوم النص "mustache" بحقول MERGEFIELD. |
### tagsReplaced() {#tagsReplaced}
```
public abstract void tagsReplaced()
```


يُستدعى عندما يتم استبدال وسوم النص "mustache" بحقول MERGEFIELD.

 **Examples:** 

يوضح كيفية تعريف منطق مخصص لمعالجة الأحداث أثناء دمج البريد.

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

