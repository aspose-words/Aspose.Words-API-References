---
title: "SaveOutputParameters"
linktitle: "SaveOutputParameters"
second_title: "Aspose.Words pour Java"
description: "Cet objet est renvoyé à l'appelant après l'enregistrement d'un document et contient des informations supplémentaires qui ont été générées ou calculées pendant l'opération d'enregistrement en Java."
type: docs
weight: 597
url: /fr/java/com.aspose.words/saveoutputparameters/
---

**Inheritance:**
java.lang.Object
```
public class SaveOutputParameters
```

Cet objet est renvoyé à l'appelant après l'enregistrement d'un document et contient des informations supplémentaires qui ont été générées ou calculées pendant l'opération d'enregistrement. L'appelant peut utiliser ou ignorer cet objet.

Pour en savoir plus, consultez l'article de documentation [ Save a Document ][Save a Document].

 **Examples:** 

Montre comment accéder aux paramètres de sortie de l'opération d'enregistrement d'un document.

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
## Méthodes

| Méthode | Description |
| --- | --- |
| [getContentType()](#getContentType) | Renvoie la chaîne Content-Type (type de média Internet) qui identifie le type du document enregistré. |
### getContentType() {#getContentType}
```
public String getContentType()
```


Renvoie la chaîne Content-Type (type de média Internet) qui identifie le type du document enregistré.

 **Examples:** 

Montre comment accéder aux paramètres de sortie de l'opération d'enregistrement d'un document.

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
java.lang.String - La chaîne Content-Type (type de média Internet) qui identifie le type du document enregistré.
