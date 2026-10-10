---
title: "PlainTextDocument"
linktitle: "PlainTextDocument"
second_title: "Aspose.Words para Java"
description: "Permite extraer la representación de texto plano del contenido del documento en Java."
type: docs
weight: 549
url: /es/java/com.aspose.words/plaintextdocument/
---

**Inheritance:**
java.lang.Object
```
public class PlainTextDocument
```

Permite extraer una representación de texto plano del contenido del documento.

Para obtener más información, visite el artículo de documentación [ Working with Text Document ][Working with Text Document].

 **Examples:** 

Muestra cómo cargar el contenido de un documento Microsoft Word en texto plano.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world!");

 doc.save(getArtifactsDir() + "PlainTextDocument.Load.docx");

 PlainTextDocument plaintext = new PlainTextDocument(getArtifactsDir() + "PlainTextDocument.Load.docx");

 Assert.assertEquals("Hello world!", plaintext.getText().trim());
 
```


[Working with Text Document]: https://docs.aspose.com/words/java/working-with-text-document/
## Constructores

| Constructor | Descripción |
| --- | --- |
| [PlainTextDocument(String fileName)](#PlainTextDocument-java.lang.String) | Crea un documento de texto plano a partir de un archivo. |
| [PlainTextDocument(String fileName, LoadOptions loadOptions)](#PlainTextDocument-java.lang.String-com.aspose.words.LoadOptions) | Crea un documento de texto plano a partir de un archivo. |
| [PlainTextDocument(InputStream stream)](#PlainTextDocument-java.io.InputStream) | Inicializa una nueva instancia de esta clase. |
| [PlainTextDocument(InputStream stream, LoadOptions loadOptions)](#PlainTextDocument-java.io.InputStream-com.aspose.words.LoadOptions) | Inicializa una nueva instancia de esta clase. |
## Métodos

| Método | Descripción |
| --- | --- |
| [getBuiltInDocumentProperties()](#getBuiltInDocumentProperties) | Obtiene [getBuiltInDocumentProperties()](../../com.aspose.words/plaintextdocument/\#getBuiltInDocumentProperties) del documento. |
| [getCustomDocumentProperties()](#getCustomDocumentProperties) | Obtiene [getCustomDocumentProperties()](../../com.aspose.words/plaintextdocument/\#getCustomDocumentProperties) del documento. |
| [getText()](#getText) | Obtiene el contenido textual del documento concatenado como una cadena. |
### PlainTextDocument(String fileName) {#PlainTextDocument-java.lang.String}
```
public PlainTextDocument(String fileName)
```


Crea un documento de texto plano a partir de un archivo. Detecta automáticamente el formato del archivo.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| fileName | java.lang.String | Nombre del archivo del cual extraer el texto. |

### PlainTextDocument(String fileName, LoadOptions loadOptions) {#PlainTextDocument-java.lang.String-com.aspose.words.LoadOptions}
```
public PlainTextDocument(String fileName, LoadOptions loadOptions)
```


Crea un documento de texto plano a partir de un archivo. Permite especificar opciones adicionales como una contraseña de cifrado.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| fileName | java.lang.String | Nombre del archivo del cual extraer el texto. |
| loadOptions | [LoadOptions](../../com.aspose.words/loadoptions/) | Opciones adicionales para usar al cargar un documento. Puede ser null. |

### PlainTextDocument(InputStream stream) {#PlainTextDocument-java.io.InputStream}
```
public PlainTextDocument(InputStream stream)
```


Inicializa una nueva instancia de esta clase.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| stream | java.io.InputStream |  |

### PlainTextDocument(InputStream stream, LoadOptions loadOptions) {#PlainTextDocument-java.io.InputStream-com.aspose.words.LoadOptions}
```
public PlainTextDocument(InputStream stream, LoadOptions loadOptions)
```


Inicializa una nueva instancia de esta clase.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| stream | java.io.InputStream |  |
| loadOptions | [LoadOptions](../../com.aspose.words/loadoptions/) |  |

### getBuiltInDocumentProperties() {#getBuiltInDocumentProperties}
```
public BuiltInDocumentProperties getBuiltInDocumentProperties()
```


Obtiene [getBuiltInDocumentProperties()](../../com.aspose.words/plaintextdocument/\#getBuiltInDocumentProperties) del documento.

 **Examples:** 

Muestra cómo cargar el contenido de un documento Microsoft Word en texto plano y luego acceder a las propiedades integradas del documento original.

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


Obtiene [getCustomDocumentProperties()](../../com.aspose.words/plaintextdocument/\#getCustomDocumentProperties) del documento.

 **Examples:** 

Muestra cómo cargar el contenido de un documento Microsoft Word en texto plano y luego acceder a las propiedades personalizadas del documento original.

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


Obtiene el contenido textual del documento concatenado como una cadena.

 **Examples:** 

Muestra cómo cargar el contenido de un documento Microsoft Word en texto plano.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world!");

 doc.save(getArtifactsDir() + "PlainTextDocument.Load.docx");

 PlainTextDocument plaintext = new PlainTextDocument(getArtifactsDir() + "PlainTextDocument.Load.docx");

 Assert.assertEquals("Hello world!", plaintext.getText().trim());
 
```

**Returns:**
java.lang.String - Contenido textual del documento concatenado como una cadena.
