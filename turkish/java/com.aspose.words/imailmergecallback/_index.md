---
title: "IMailMergeCallback"
linktitle: "IMailMergeCallback"
second_title: "Aspose.Words Java için"
description: "Java'da birleştirme işlemi gerçekleştirilirken bildirim almak istiyorsanız bu arabirimi uygulayın."
type: docs
weight: 775
url: /tr/java/com.aspose.words/imailmergecallback/
---
```
public interface IMailMergeCallback
```

Posta birleştirme işlemi sırasında bildirimler almak istiyorsanız bu arabirimi uygulayın.

 **Examples:** 

Birleştirme sırasında olayları işlemek için özel mantık tanımlamanın nasıl yapılacağını gösterir.

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
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [tagsReplaced()](#tagsReplaced) | "mustache" metin etiketleri MERGEFIELD alanlarıyla değiştirildiğinde çağrılır. |
### tagsReplaced() {#tagsReplaced}
```
public abstract void tagsReplaced()
```


"mustache" metin etiketleri MERGEFIELD alanlarıyla değiştirildiğinde çağrılır.

 **Examples:** 

Birleştirme sırasında olayları işlemek için özel mantık tanımlamanın nasıl yapılacağını gösterir.

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

