---
title: "SaveOutputParameters"
linktitle: "SaveOutputParameters"
second_title: "Aspose.Words per Java"
description: "Questo oggetto viene restituito al chiamante dopo che un documento è stato salvato e contiene informazioni aggiuntive generate o calcolate durante l'operazione di salvataggio in Java."
type: docs
weight: 597
url: /it/java/com.aspose.words/saveoutputparameters/
---

**Inheritance:**
java.lang.Object
```
public class SaveOutputParameters
```

Questo oggetto viene restituito al chiamante dopo che un documento è stato salvato e contiene informazioni aggiuntive generate o calcolate durante l'operazione di salvataggio. Il chiamante può utilizzare o ignorare questo oggetto.

Per saperne di più, visita l'articolo di documentazione [ Save a Document ][Save a Document].

 **Examples:** 

Mostra come accedere ai parametri di output dell'operazione di salvataggio di un documento.

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
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [getContentType()](#getContentType) | Restituisce la stringa Content-Type (Tipo di Media Internet) che identifica il tipo del documento salvato. |
### getContentType() {#getContentType}
```
public String getContentType()
```


Restituisce la stringa Content-Type (Tipo di Media Internet) che identifica il tipo del documento salvato.

 **Examples:** 

Mostra come accedere ai parametri di output dell'operazione di salvataggio di un documento.

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
java.lang.String - La stringa Content-Type (Tipo di Media Internet) che identifica il tipo del documento salvato.
