---
title: "PlainTextDocument"
linktitle: "PlainTextDocument"
second_title: "Aspose.Words pour Java"
description: "Permet d'extraire la représentation en texte brut du contenu du document en Java."
type: docs
weight: 549
url: /fr/java/com.aspose.words/plaintextdocument/
---

**Inheritance:**
java.lang.Object
```
public class PlainTextDocument
```

Permet d'extraire la représentation en texte brut du contenu du document.

Pour en savoir plus, consultez l'article de documentation [ Working with Text Document ][Working with Text Document].

 **Examples:** 

Montre comment charger le contenu d'un document Microsoft Word en texte brut.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world!");

 doc.save(getArtifactsDir() + "PlainTextDocument.Load.docx");

 PlainTextDocument plaintext = new PlainTextDocument(getArtifactsDir() + "PlainTextDocument.Load.docx");

 Assert.assertEquals("Hello world!", plaintext.getText().trim());
 
```


[Working with Text Document]: https://docs.aspose.com/words/java/working-with-text-document/
## Constructors

| Constructor | Description |
| --- | --- |
| [PlainTextDocument(String fileName)](#PlainTextDocument-java.lang.String) | Crée un document texte brut à partir d'un fichier. |
| [PlainTextDocument(String fileName, LoadOptions loadOptions)](#PlainTextDocument-java.lang.String-com.aspose.words.LoadOptions) | Crée un document texte brut à partir d'un fichier. |
| [PlainTextDocument(InputStream stream)](#PlainTextDocument-java.io.InputStream) | Initialise une nouvelle instance de cette classe. |
| [PlainTextDocument(InputStream stream, LoadOptions loadOptions)](#PlainTextDocument-java.io.InputStream-com.aspose.words.LoadOptions) | Initialise une nouvelle instance de cette classe. |
## Méthodes

| Méthode | Description |
| --- | --- |
| [getBuiltInDocumentProperties()](#getBuiltInDocumentProperties) | Obtient [getBuiltInDocumentProperties()](../../com.aspose.words/plaintextdocument/\#getBuiltInDocumentProperties) du document. |
| [getCustomDocumentProperties()](#getCustomDocumentProperties) | Obtient [getCustomDocumentProperties()](../../com.aspose.words/plaintextdocument/\#getCustomDocumentProperties) du document. |
| [getText()](#getText) | Obtient le contenu textuel du document concaténé sous forme de chaîne. |
### PlainTextDocument(String fileName) {#PlainTextDocument-java.lang.String}
```
public PlainTextDocument(String fileName)
```


Crée un document texte brut à partir d'un fichier. Détecte automatiquement le format du fichier.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| fileName | java.lang.String | Nom du fichier dont le texte doit être extrait. |

### PlainTextDocument(String fileName, LoadOptions loadOptions) {#PlainTextDocument-java.lang.String-com.aspose.words.LoadOptions}
```
public PlainTextDocument(String fileName, LoadOptions loadOptions)
```


Crée un document texte brut à partir d'un fichier. Permet de spécifier des options supplémentaires telles qu'un mot de passe de chiffrement.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| fileName | java.lang.String | Nom du fichier dont le texte doit être extrait. |
| loadOptions | [LoadOptions](../../com.aspose.words/loadoptions/) | Options supplémentaires à utiliser lors du chargement d'un document. Peut être null. |

### PlainTextDocument(InputStream stream) {#PlainTextDocument-java.io.InputStream}
```
public PlainTextDocument(InputStream stream)
```


Initialise une nouvelle instance de cette classe.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| stream | java.io.InputStream |  |

### PlainTextDocument(InputStream stream, LoadOptions loadOptions) {#PlainTextDocument-java.io.InputStream-com.aspose.words.LoadOptions}
```
public PlainTextDocument(InputStream stream, LoadOptions loadOptions)
```


Initialise une nouvelle instance de cette classe.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| stream | java.io.InputStream |  |
| loadOptions | [LoadOptions](../../com.aspose.words/loadoptions/) |  |

### getBuiltInDocumentProperties() {#getBuiltInDocumentProperties}
```
public BuiltInDocumentProperties getBuiltInDocumentProperties()
```


Obtient [getBuiltInDocumentProperties()](../../com.aspose.words/plaintextdocument/\#getBuiltInDocumentProperties) du document.

 **Examples:** 

Montre comment charger le contenu d'un document Microsoft Word en texte brut puis accéder aux propriétés intégrées du document original.

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


Obtient [getCustomDocumentProperties()](../../com.aspose.words/plaintextdocument/\#getCustomDocumentProperties) du document.

 **Examples:** 

Montre comment charger le contenu d'un document Microsoft Word en texte brut, puis accéder aux propriétés personnalisées du document original.

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


Obtient le contenu textuel du document concaténé sous forme de chaîne.

 **Examples:** 

Montre comment charger le contenu d'un document Microsoft Word en texte brut.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world!");

 doc.save(getArtifactsDir() + "PlainTextDocument.Load.docx");

 PlainTextDocument plaintext = new PlainTextDocument(getArtifactsDir() + "PlainTextDocument.Load.docx");

 Assert.assertEquals("Hello world!", plaintext.getText().trim());
 
```

**Returns:**
java.lang.String - Contenu textuel du document concaténé sous forme de chaîne.
