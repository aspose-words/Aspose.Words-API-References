---
title: "IMailMergeCallback"
linktitle: "IMailMergeCallback"
second_title: "Aspose.Words per Java"
description: "Implementa questa interfaccia se desideri ricevere notifiche durante l'esecuzione del mail merge in Java."
type: docs
weight: 775
url: /it/java/com.aspose.words/imailmergecallback/
---
```
public interface IMailMergeCallback
```

Implementa questa interfaccia se desideri ricevere notifiche durante l'esecuzione dell'unione di stampa.

 **Examples:** 

Mostra come definire una logica personalizzata per gestire gli eventi durante il mail merge.

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
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [tagsReplaced()](#tagsReplaced) | Chiamata quando i tag di testo "mustache" vengono sostituiti con campi MERGEFIELD. |
### tagsReplaced() {#tagsReplaced}
```
public abstract void tagsReplaced()
```


Chiamata quando i tag di testo "mustache" vengono sostituiti con campi MERGEFIELD.

 **Examples:** 

Mostra come definire una logica personalizzata per gestire gli eventi durante il mail merge.

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

