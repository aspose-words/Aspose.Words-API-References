---
title: "SaveOutputParameters"
linktitle: "SaveOutputParameters"
second_title: "Aspose.Words para Java"
description: "Este objeto se devuelve al llamador después de que se guarda un documento y contiene información adicional que se ha generado o calculado durante la operación de guardado en Java."
type: docs
weight: 597
url: /es/java/com.aspose.words/saveoutputparameters/
---

**Inheritance:**
java.lang.Object
```
public class SaveOutputParameters
```

Este objeto se devuelve al llamador después de que se guarda un documento y contiene información adicional que se ha generado o calculado durante la operación de guardado. El llamador puede usar o ignorar este objeto.

Para obtener más información, visite el artículo de documentación [ Save a Document ][Save a Document].

 **Examples:** 

Muestra cómo acceder a los parámetros de salida de la operación de guardado de un documento.

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
## Métodos

| Método | Descripción |
| --- | --- |
| [getContentType()](#getContentType) | Devuelve la cadena Content-Type (Tipo de medio de Internet) que identifica el tipo del documento guardado. |
### getContentType() {#getContentType}
```
public String getContentType()
```


Devuelve la cadena Content-Type (Tipo de medio de Internet) que identifica el tipo del documento guardado.

 **Examples:** 

Muestra cómo acceder a los parámetros de salida de la operación de guardado de un documento.

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
java.lang.String - La cadena Content-Type (Tipo de medio de Internet) que identifica el tipo del documento guardado.
