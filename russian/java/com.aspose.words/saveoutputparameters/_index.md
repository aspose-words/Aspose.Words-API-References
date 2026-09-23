---
title: "SaveOutputParameters"
linktitle: "SaveOutputParameters"
second_title: "Aspose.Words для Java"
description: "Этот объект возвращается вызывающему после сохранения документа и содержит дополнительную информацию, которая была сгенерирована или вычислена во время операции сохранения в Java."
type: docs
weight: 597
url: /ru/java/com.aspose.words/saveoutputparameters/
---

**Inheritance:**
java.lang.Object
```
public class SaveOutputParameters
```

Этот объект возвращается вызывающему после сохранения документа и содержит дополнительную информацию, которая была сгенерирована или вычислена во время операции сохранения. Вызывающий может использовать этот объект или игнорировать его.

Чтобы узнать больше, посетите статью документации [ Save a Document ][Save a Document].

 **Examples:** 

Показывает, как получить доступ к параметрам вывода операции сохранения документа.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world!");

 // After we save a document, we can access the Internet Media Type (MIME type) of the newly created output document.
 SaveOutputParameters parameters = doc.save(getArtifactsDir() + "Document.SaveOutputParameters.doc");

 Assert.assertEquals("application/msword", parameters.getContentType());

 // This property changes depending on the save format.
 parameters = doc.save(getArtifactsDir() + "Document.SaveOutputParameters.pdf");

 Assert.assertEquals("application/pdf", parameters.getContentType());
 
```


[Save a Document]: https://docs.aspose.com/words/java/save-a-document/
## Методы

| Метод | Описание |
| --- | --- |
| [getContentType()](#getContentType) | Возвращает строку Content-Type (тип интернет‑медиа), которая определяет тип сохранённого документа. |
### getContentType() {#getContentType}
```
public String getContentType()
```


Возвращает строку Content-Type (тип интернет‑медиа), которая определяет тип сохранённого документа.

 **Examples:** 

Показывает, как получить доступ к параметрам вывода операции сохранения документа.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world!");

 // After we save a document, we can access the Internet Media Type (MIME type) of the newly created output document.
 SaveOutputParameters parameters = doc.save(getArtifactsDir() + "Document.SaveOutputParameters.doc");

 Assert.assertEquals("application/msword", parameters.getContentType());

 // This property changes depending on the save format.
 parameters = doc.save(getArtifactsDir() + "Document.SaveOutputParameters.pdf");

 Assert.assertEquals("application/pdf", parameters.getContentType());
 
```

**Returns:**
java.lang.String — строка Content-Type (тип интернет‑медиа), которая определяет тип сохранённого документа.
