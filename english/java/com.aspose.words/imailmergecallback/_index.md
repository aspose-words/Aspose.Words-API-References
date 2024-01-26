---
title: IMailMergeCallback
linktitle: IMailMergeCallback
second_title: Aspose.Words for Java
description: Implement this interface if you want to receive notifications while mail merge is performed in Java.
type: docs
weight: 693
url: /java/com.aspose.words/imailmergecallback/
---
```
public interface IMailMergeCallback
```

Implement this interface if you want to receive notifications while mail merge is performed.

 **Examples:** 

Shows how to define custom logic for handling events during mail merge.

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
## Methods

| Method | Description |
| --- | --- |
| [tagsReplaced()](#tagsReplaced) | Called when "mustache" text tags are replaced with MERGEFIELD fields. |
### tagsReplaced() {#tagsReplaced}
```
public abstract void tagsReplaced()
```


Called when "mustache" text tags are replaced with MERGEFIELD fields.

 **Examples:** 

Shows how to define custom logic for handling events during mail merge.

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

