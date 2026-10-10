---
title: "IMailMergeCallback"
linktitle: "IMailMergeCallback"
second_title: "Aspose.Words für Java"
description: "Implementieren Sie dieses Interface, wenn Sie Benachrichtigungen erhalten möchten, während der Seriendruck in Java ausgeführt wird."
type: docs
weight: 775
url: /de/java/com.aspose.words/imailmergecallback/
---
```
public interface IMailMergeCallback
```

Implementieren Sie dieses Interface, wenn Sie Benachrichtigungen erhalten möchten, während ein Seriendruck durchgeführt wird.

 **Examples:** 

Zeigt, wie benutzerdefinierte Logik für die Ereignisbehandlung während des Seriendrucks definiert wird.

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
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [tagsReplaced()](#tagsReplaced) | Wird aufgerufen, wenn \"mustache\"-Textmarken durch MERGEFIELD-Felder ersetzt werden. |
### tagsReplaced() {#tagsReplaced}
```
public abstract void tagsReplaced()
```


Wird aufgerufen, wenn \"mustache\"-Textmarken durch MERGEFIELD-Felder ersetzt werden.

 **Examples:** 

Zeigt, wie benutzerdefinierte Logik für die Ereignisbehandlung während des Seriendrucks definiert wird.

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

