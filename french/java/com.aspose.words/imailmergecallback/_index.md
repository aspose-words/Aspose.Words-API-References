---
title: "IMailMergeCallback"
linktitle: "IMailMergeCallback"
second_title: "Aspose.Words pour Java"
description: "Implémentez cette interface si vous souhaitez recevoir des notifications pendant l'exécution de la fusion de courrier en Java."
type: docs
weight: 775
url: /fr/java/com.aspose.words/imailmergecallback/
---
```
public interface IMailMergeCallback
```

Implémentez cette interface si vous souhaitez recevoir des notifications pendant l'exécution de la fusion de courrier.

 **Examples:** 

Montre comment définir une logique personnalisée pour gérer les événements pendant la fusion de courrier.

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
## Méthodes

| Méthode | Description |
| --- | --- |
| [tagsReplaced()](#tagsReplaced) | Appelé lorsque les balises de texte "mustache" sont remplacées par des champs MERGEFIELD. |
### tagsReplaced() {#tagsReplaced}
```
public abstract void tagsReplaced()
```


Appelé lorsque les balises de texte "mustache" sont remplacées par des champs MERGEFIELD.

 **Examples:** 

Montre comment définir une logique personnalisée pour gérer les événements pendant la fusion de courrier.

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

