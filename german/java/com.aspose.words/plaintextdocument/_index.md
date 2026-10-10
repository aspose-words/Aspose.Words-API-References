---
title: "PlainTextDocument"
linktitle: "PlainTextDocument"
second_title: "Aspose.Words für Java"
description: "Ermöglicht das Extrahieren einer Nur-Text-Darstellung des Dokumentinhalts in Java."
type: docs
weight: 549
url: /de/java/com.aspose.words/plaintextdocument/
---

**Inheritance:**
java.lang.Object
```
public class PlainTextDocument
```

Ermöglicht das Extrahieren einer Nur‑Text‑Darstellung des Inhalts des Dokuments.

Um mehr zu erfahren, besuchen Sie den Dokumentationsartikel [ Working with Text Document ][Working with Text Document].

 **Examples:** 

Zeigt, wie man den Inhalt eines Microsoft Word-Dokuments im Nur-Text-Format lädt.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world!");

 doc.save(getArtifactsDir() + "PlainTextDocument.Load.docx");

 PlainTextDocument plaintext = new PlainTextDocument(getArtifactsDir() + "PlainTextDocument.Load.docx");

 Assert.assertEquals("Hello world!", plaintext.getText().trim());
 
```


[Working with Text Document]: https://docs.aspose.com/words/java/working-with-text-document/
## Konstruktoren

| Konstruktor | Beschreibung |
| --- | --- |
| [PlainTextDocument(String fileName)](#PlainTextDocument-java.lang.String) | Erstellt ein Nur-Text-Dokument aus einer Datei. |
| [PlainTextDocument(String fileName, LoadOptions loadOptions)](#PlainTextDocument-java.lang.String-com.aspose.words.LoadOptions) | Erstellt ein Nur-Text-Dokument aus einer Datei. |
| [PlainTextDocument(InputStream stream)](#PlainTextDocument-java.io.InputStream) | Initialisiert eine neue Instanz dieser Klasse. |
| [PlainTextDocument(InputStream stream, LoadOptions loadOptions)](#PlainTextDocument-java.io.InputStream-com.aspose.words.LoadOptions) | Initialisiert eine neue Instanz dieser Klasse. |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [getBuiltInDocumentProperties()](#getBuiltInDocumentProperties) | Liefert [getBuiltInDocumentProperties()](../../com.aspose.words/plaintextdocument/\#getBuiltInDocumentProperties) des Dokuments. |
| [getCustomDocumentProperties()](#getCustomDocumentProperties) | Liefert [getCustomDocumentProperties()](../../com.aspose.words/plaintextdocument/\#getCustomDocumentProperties) des Dokuments. |
| [getText()](#getText) | Liefert den Textinhalt des Dokuments, zusammengefügt als Zeichenkette. |
### PlainTextDocument(String fileName) {#PlainTextDocument-java.lang.String}
```
public PlainTextDocument(String fileName)
```


Erstellt ein Nur-Text-Dokument aus einer Datei. Erkennt das Dateiformat automatisch.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fileName | java.lang.String | Name der Datei, aus der der Text extrahiert werden soll. |

### PlainTextDocument(String fileName, LoadOptions loadOptions) {#PlainTextDocument-java.lang.String-com.aspose.words.LoadOptions}
```
public PlainTextDocument(String fileName, LoadOptions loadOptions)
```


Erstellt ein Nur-Text-Dokument aus einer Datei. Ermöglicht die Angabe zusätzlicher Optionen wie ein Verschlüsselungspasswort.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fileName | java.lang.String | Name der Datei, aus der der Text extrahiert werden soll. |
| loadOptions | [LoadOptions](../../com.aspose.words/loadoptions/) | Zusätzliche Optionen, die beim Laden eines Dokuments verwendet werden können. Kann null sein. |

### PlainTextDocument(InputStream stream) {#PlainTextDocument-java.io.InputStream}
```
public PlainTextDocument(InputStream stream)
```


Initialisiert eine neue Instanz dieser Klasse.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| stream | java.io.InputStream |  |

### PlainTextDocument(InputStream stream, LoadOptions loadOptions) {#PlainTextDocument-java.io.InputStream-com.aspose.words.LoadOptions}
```
public PlainTextDocument(InputStream stream, LoadOptions loadOptions)
```


Initialisiert eine neue Instanz dieser Klasse.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| stream | java.io.InputStream |  |
| loadOptions | [LoadOptions](../../com.aspose.words/loadoptions/) |  |

### getBuiltInDocumentProperties() {#getBuiltInDocumentProperties}
```
public BuiltInDocumentProperties getBuiltInDocumentProperties()
```


Liefert [getBuiltInDocumentProperties()](../../com.aspose.words/plaintextdocument/\#getBuiltInDocumentProperties) des Dokuments.

 **Examples:** 

Zeigt, wie der Inhalt eines Microsoft Word-Dokuments im Klartext geladen und anschließend auf die integrierten Eigenschaften des Originaldokuments zugegriffen wird.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Hello world!");
 doc.getBuiltInDocumentProperties().setAuthor("John Doe");

 doc.save(getArtifactsDir() + "PlainTextDocument.BuiltInProperties.docx");

 PlainTextDocument plaintext = new PlainTextDocument(getArtifactsDir() + "PlainTextDocument.BuiltInProperties.docx");

 Assert.assertEquals("Hello world!", plaintext.getText().trim());
 Assert.assertEquals("John Doe", plaintext.getBuiltInDocumentProperties().getAuthor());
 
```

**Returns:**
[BuiltInDocumentProperties](../../com.aspose.words/builtindocumentproperties/) - [getBuiltInDocumentProperties()](../../com.aspose.words/plaintextdocument/\#getBuiltInDocumentProperties) of the document.
### getCustomDocumentProperties() {#getCustomDocumentProperties}
```
public CustomDocumentProperties getCustomDocumentProperties()
```


Liefert [getCustomDocumentProperties()](../../com.aspose.words/plaintextdocument/\#getCustomDocumentProperties) des Dokuments.

 **Examples:** 

Zeigt, wie der Inhalt eines Microsoft Word-Dokuments im Klartext geladen und anschließend auf die benutzerdefinierten Eigenschaften des Originaldokuments zugegriffen wird.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Hello world!");
 doc.getCustomDocumentProperties().add("Location of writing", "123 Main St, London, UK");

 doc.save(getArtifactsDir() + "PlainTextDocument.CustomDocumentProperties.docx");

 PlainTextDocument plaintext = new PlainTextDocument(getArtifactsDir() + "PlainTextDocument.CustomDocumentProperties.docx");

 Assert.assertEquals("Hello world!", plaintext.getText().trim());
 Assert.assertEquals("123 Main St, London, UK", plaintext.getCustomDocumentProperties().get("Location of writing").getValue());
 
```

**Returns:**
[CustomDocumentProperties](../../com.aspose.words/customdocumentproperties/) - [getCustomDocumentProperties()](../../com.aspose.words/plaintextdocument/\#getCustomDocumentProperties) of the document.
### getText() {#getText}
```
public String getText()
```


Liefert den Textinhalt des Dokuments, zusammengefügt als Zeichenkette.

 **Examples:** 

Zeigt, wie man den Inhalt eines Microsoft Word-Dokuments im Nur-Text-Format lädt.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world!");

 doc.save(getArtifactsDir() + "PlainTextDocument.Load.docx");

 PlainTextDocument plaintext = new PlainTextDocument(getArtifactsDir() + "PlainTextDocument.Load.docx");

 Assert.assertEquals("Hello world!", plaintext.getText().trim());
 
```

**Returns:**
java.lang.String – Textlicher Inhalt des Dokuments, als Zeichenkette verkettet.
