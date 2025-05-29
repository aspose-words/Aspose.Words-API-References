---
title: PlainTextDocument
linktitle: PlainTextDocument
articleTitle: PlainTextDocument
second_title: Aspose.Words para .NET
description: Crea fácilmente documentos de texto plano con nuestro constructor PlainTextDocument. ¡Disfruta de la detección automática del formato de archivo para una integración perfecta!
type: docs
weight: 10
url: /es/net/aspose.words/plaintextdocument/plaintextdocument/
---
## PlainTextDocument(*string*) {#constructor_2}

Crea un documento de texto sin formato a partir de un archivo. Detecta automáticamente el formato del archivo.

```csharp
public PlainTextDocument(string fileName)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| fileName | String | Nombre del archivo del cual extraer el texto. |

### Excepciones

| excepción | condición |
| --- | --- |
| [UnsupportedFileFormatException](../../unsupportedfileformatexception/) | El formato del documento no es reconocido o no es compatible. |
| [FileCorruptedException](../../filecorruptedexception/) | El documento parece estar dañado y no se puede cargar. |
| Exception | Hay un problema con el documento y debe informarse a los desarrolladores de Aspose.Words. |
| IOException | Hay una excepción de entrada/salida. |
| [IncorrectPasswordException](../../incorrectpasswordexception/) | El documento está encriptado y requiere una contraseña para abrirlo, pero usted proporcionó una contraseña incorrecta. |
| ArgumentException | El nombre del archivo no puede ser una cadena nula o vacía. |

## Ejemplos

Muestra cómo cargar el contenido de un documento de Microsoft Word en texto sin formato.

```csharp
Document doc = new Document(); 
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

doc.Save(ArtifactsDir + "PlainTextDocument.Load.docx");

PlainTextDocument plaintext = new PlainTextDocument(ArtifactsDir + "PlainTextDocument.Load.docx");

Assert.AreEqual("Hello world!", plaintext.Text.Trim());
```

### Ver también

* class [PlainTextDocument](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)

---

## PlainTextDocument(*string, [LoadOptions](../../../aspose.words.loading/loadoptions/)*) {#constructor_3}

Crea un documento de texto sin formato a partir de un archivo. Permite especificar opciones adicionales, como una contraseña de cifrado.

```csharp
public PlainTextDocument(string fileName, LoadOptions loadOptions)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| fileName | String | Nombre del archivo del cual extraer el texto. |
| loadOptions | LoadOptions | Opciones adicionales para usar al cargar un documento. Puede ser`nulo`. |

### Excepciones

| excepción | condición |
| --- | --- |
| [UnsupportedFileFormatException](../../unsupportedfileformatexception/) | El formato del documento no es reconocido o no es compatible. |
| [FileCorruptedException](../../filecorruptedexception/) | El documento parece estar dañado y no se puede cargar. |
| Exception | Hay un problema con el documento y debe informarse a los desarrolladores de Aspose.Words. |
| IOException | Hay una excepción de entrada/salida. |
| [IncorrectPasswordException](../../incorrectpasswordexception/) | El documento está encriptado y requiere una contraseña para abrirlo, pero usted proporcionó una contraseña incorrecta. |
| ArgumentException | El nombre del archivo no puede ser una cadena nula o vacía. |

## Ejemplos

Muestra cómo cargar el contenido de un documento cifrado de Microsoft Word en texto sin formato.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
saveOptions.Password = "MyPassword";

doc.Save(ArtifactsDir + "PlainTextDocument.LoadEncrypted.docx", saveOptions);

LoadOptions loadOptions = new LoadOptions();
loadOptions.Password = "MyPassword";

PlainTextDocument plaintext = new PlainTextDocument(ArtifactsDir + "PlainTextDocument.LoadEncrypted.docx", loadOptions);

Assert.AreEqual("Hello world!", plaintext.Text.Trim());
```

### Ver también

* class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* class [PlainTextDocument](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)

---

## PlainTextDocument(*Stream*) {#constructor}

Crea un documento de texto sin formato a partir de una secuencia. Detecta automáticamente el formato del archivo.

```csharp
public PlainTextDocument(Stream stream)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| stream | Stream | La secuencia de donde extraer el texto. |

### Excepciones

| excepción | condición |
| --- | --- |
| [UnsupportedFileFormatException](../../unsupportedfileformatexception/) | El formato del documento no es reconocido o no es compatible. |
| [FileCorruptedException](../../filecorruptedexception/) | El documento parece estar dañado y no se puede cargar. |
| Exception | Hay un problema con el documento y debe informarse a los desarrolladores de Aspose.Words. |
| IOException | Hay una excepción de entrada/salida. |
| [IncorrectPasswordException](../../incorrectpasswordexception/) | El documento está encriptado y requiere una contraseña para abrirlo, pero usted proporcionó una contraseña incorrecta. |
| ArgumentNullException | El flujo no puede ser nulo. |
| NotSupportedException | El stream no admite ni lectura ni búsqueda. |
| ObjectDisposedException | El arroyo es un objeto dispuesto. |

## Observaciones

El documento debe almacenarse al inicio de la secuencia. La secuencia debe permitir posicionamiento aleatorio.

## Ejemplos

Muestra cómo cargar el contenido de un documento de Microsoft Word en texto simple mediante secuencias.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");
doc.Save(ArtifactsDir + "PlainTextDocument.LoadFromStream.docx");

using (FileStream stream = new FileStream(ArtifactsDir + "PlainTextDocument.LoadFromStream.docx", FileMode.Open))
{
    PlainTextDocument plaintext = new PlainTextDocument(stream);

    Assert.AreEqual("Hello world!", plaintext.Text.Trim());
}
```

### Ver también

* class [PlainTextDocument](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)

---

## PlainTextDocument(*Stream, [LoadOptions](../../../aspose.words.loading/loadoptions/)*) {#constructor_1}

Crea un documento de texto sin formato a partir de una secuencia. Permite especificar opciones adicionales, como una contraseña de cifrado.

```csharp
public PlainTextDocument(Stream stream, LoadOptions loadOptions)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| stream | Stream | La secuencia de donde extraer el texto. |
| loadOptions | LoadOptions | Opciones adicionales para usar al cargar un documento. Puede ser`nulo`. |

### Excepciones

| excepción | condición |
| --- | --- |
| [UnsupportedFileFormatException](../../unsupportedfileformatexception/) | El formato del documento no es reconocido o no es compatible. |
| [FileCorruptedException](../../filecorruptedexception/) | El documento parece estar dañado y no se puede cargar. |
| Exception | Hay un problema con el documento y debe informarse a los desarrolladores de Aspose.Words. |
| IOException | Hay una excepción de entrada/salida. |
| [IncorrectPasswordException](../../incorrectpasswordexception/) | El documento está encriptado y requiere una contraseña para abrirlo, pero usted proporcionó una contraseña incorrecta. |
| ArgumentNullException | El flujo no puede ser nulo. |
| NotSupportedException | El stream no admite ni lectura ni búsqueda. |
| ObjectDisposedException | El arroyo es un objeto dispuesto. |

## Observaciones

El documento debe almacenarse al inicio de la secuencia. La secuencia debe permitir posicionamiento aleatorio.

## Ejemplos

Muestra cómo cargar el contenido de un documento cifrado de Microsoft Word en texto simple mediante secuencias.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
saveOptions.Password = "MyPassword";

doc.Save(ArtifactsDir + "PlainTextDocument.LoadFromStreamWithOptions.docx", saveOptions);

LoadOptions loadOptions = new LoadOptions();
loadOptions.Password = "MyPassword";

using (FileStream stream = new FileStream(ArtifactsDir + "PlainTextDocument.LoadFromStreamWithOptions.docx", FileMode.Open))
{
    PlainTextDocument plaintext = new PlainTextDocument(stream, loadOptions);

    Assert.AreEqual("Hello world!", plaintext.Text.Trim());
}
```

### Ver también

* class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* class [PlainTextDocument](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
