---
title: "IMailMergeCallback"
linktitle: "IMailMergeCallback"
second_title: "Aspose.Words para Java"
description: "Implemente esta interfaz si desea recibir notificaciones mientras se realiza la combinación de correspondencia en Java."
type: docs
weight: 775
url: /es/java/com.aspose.words/imailmergecallback/
---
```
public interface IMailMergeCallback
```

Implemente esta interfaz si desea recibir notificaciones mientras se realiza la combinación de correspondencia.

 **Examples:** 

Muestra cómo definir lógica personalizada para manejar eventos durante la combinación de correspondencia.

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
## Métodos

| Método | Descripción |
| --- | --- |
| [tagsReplaced()](#tagsReplaced) | Se llama cuando las etiquetas de texto "mustache" se reemplazan con campos MERGEFIELD. |
### tagsReplaced() {#tagsReplaced}
```
public abstract void tagsReplaced()
```


Se llama cuando las etiquetas de texto "mustache" se reemplazan con campos MERGEFIELD.

 **Examples:** 

Muestra cómo definir lógica personalizada para manejar eventos durante la combinación de correspondencia.

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

