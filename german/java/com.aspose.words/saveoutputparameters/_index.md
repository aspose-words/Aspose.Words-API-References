---
title: "SaveOutputParameters"
linktitle: "SaveOutputParameters"
second_title: "Aspose.Words für Java"
description: "Dieses Objekt wird an den Aufrufer zurückgegeben, nachdem ein Dokument gespeichert wurde, und enthält zusätzliche Informationen, die während des Speichervorgangs in Java erzeugt oder berechnet wurden."
type: docs
weight: 597
url: /de/java/com.aspose.words/saveoutputparameters/
---

**Inheritance:**
java.lang.Object
```
public class SaveOutputParameters
```

Dieses Objekt wird an den Aufrufer zurückgegeben, nachdem ein Dokument gespeichert wurde, und enthält zusätzliche Informationen, die während des Speichervorgangs erzeugt oder berechnet wurden. Der Aufrufer kann dieses Objekt verwenden oder ignorieren.

Um mehr zu erfahren, besuchen Sie den [ Save a Document ][Save a Document] Dokumentationsartikel.

 **Examples:** 

Zeigt, wie man auf die Ausgabparameter eines Dokumentenspeichervorgangs zugreift.

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
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [getContentType()](#getContentType) | Gibt die Content-Type-Zeichenkette (Internet Media Type) zurück, die den Typ des gespeicherten Dokuments identifiziert. |
### getContentType() {#getContentType}
```
public String getContentType()
```


Gibt die Content-Type-Zeichenkette (Internet Media Type) zurück, die den Typ des gespeicherten Dokuments identifiziert.

 **Examples:** 

Zeigt, wie man auf die Ausgabparameter eines Dokumentenspeichervorgangs zugreift.

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
java.lang.String - Die Content-Type-Zeichenkette (Internet Media Type), die den Typ des gespeicherten Dokuments identifiziert.
