---
title: PlainTextDocument.PlainTextDocument
second_title: Referencia de API de Aspose.Words para .NET
description: PlainTextDocument constructor. Crea un documento de texto sin formato a partir de un archivo. Detecta automáticamente el formato de archivo.
type: docs
weight: 10
url: /es/net/aspose.words/plaintextdocument/plaintextdocument/
---
## PlainTextDocument(string) {#constructor_2}

Crea un documento de texto sin formato a partir de un archivo. Detecta automáticamente el formato de archivo.

```csharp
public PlainTextDocument(string fileName)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| fileName | String | Nombre del archivo del que extraer el texto. |

### Excepciones

| excepción | condición |
| --- | --- |
| [UnsupportedFileFormatException](../../unsupportedfileformatexception/) | El formato del documento no se reconoce o no es compatible. |
| [FileCorruptedException](../../filecorruptedexception/) | El documento parece estar dañado y no se puede cargar. |
| Exception | Hay un problema con el documento y debe informarse a los desarrolladores de Aspose.Words. |
| IOException | Hay una excepción de entrada/salida. |
| [IncorrectPasswordException](../../incorrectpasswordexception/) | El documento está encriptado y requiere una contraseña para abrirlo, pero proporcionó una contraseña incorrecta. |
| ArgumentException | El nombre del archivo no puede ser una cadena nula o vacía. |

### Ejemplos

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
* espacio de nombres [Aspose.Words](../../plaintextdocument/)
* asamblea [Aspose.Words](../../../)

---

## PlainTextDocument(string, LoadOptions) {#constructor_3}

Crea un documento de texto sin formato a partir de un archivo. Permite especificar opciones adicionales como una contraseña de cifrado.

```csharp
public PlainTextDocument(string fileName, LoadOptions loadOptions)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| fileName | String | Nombre del archivo del que extraer el texto. |
| loadOptions | LoadOptions | Opciones adicionales para usar al cargar un documento. Puede ser nulo. |

### Excepciones

| excepción | condición |
| --- | --- |
| [UnsupportedFileFormatException](../../unsupportedfileformatexception/) | El formato del documento no se reconoce o no es compatible. |
| [FileCorruptedException](../../filecorruptedexception/) | El documento parece estar dañado y no se puede cargar. |
| Exception | Hay un problema con el documento y debe informarse a los desarrolladores de Aspose.Words. |
| IOException | Hay una excepción de entrada/salida. |
| [IncorrectPasswordException](../../incorrectpasswordexception/) | El documento está encriptado y requiere una contraseña para abrirlo, pero proporcionó una contraseña incorrecta. |
| ArgumentException | El nombre del archivo no puede ser una cadena nula o vacía. |

### Ejemplos

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
* espacio de nombres [Aspose.Words](../../plaintextdocument/)
* asamblea [Aspose.Words](../../../)

---

## PlainTextDocument(Stream) {#constructor}

Crea un documento de texto sin formato a partir de una secuencia. Detecta automáticamente el formato de archivo.

```csharp
public PlainTextDocument(Stream stream)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| stream | Stream | La secuencia de donde extraer el texto. |

### Excepciones

| excepción | condición |
| --- | --- |
| [UnsupportedFileFormatException](../../unsupportedfileformatexception/) | El formato del documento no se reconoce o no es compatible. |
| [FileCorruptedException](../../filecorruptedexception/) | El documento parece estar dañado y no se puede cargar. |
| Exception | Hay un problema con el documento y debe informarse a los desarrolladores de Aspose.Words. |
| IOException | Hay una excepción de entrada/salida. |
| [IncorrectPasswordException](../../incorrectpasswordexception/) | El documento está encriptado y requiere una contraseña para abrirlo, pero proporcionó una contraseña incorrecta. |
| ArgumentNullException | La secuencia no puede ser nula. |
| NotSupportedException | La transmisión no admite la lectura ni la búsqueda. |
| ObjectDisposedException | La corriente es un objeto desechado. |

### Observaciones

El documento debe almacenarse al principio de la secuencia. La secuencia debe admitir el posicionamiento aleatorio.

### Ejemplos

Muestra cómo cargar el contenido de un documento de Microsoft Word en texto sin formato usando stream.

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
* espacio de nombres [Aspose.Words](../../plaintextdocument/)
* asamblea [Aspose.Words](../../../)

---

## PlainTextDocument(Stream, LoadOptions) {#constructor_1}

Crea un documento de texto sin formato a partir de una secuencia. Permite especificar opciones adicionales como una contraseña de cifrado.

```csharp
public PlainTextDocument(Stream stream, LoadOptions loadOptions)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| stream | Stream | La secuencia de donde extraer el texto. |
| loadOptions | LoadOptions | Opciones adicionales para usar al cargar un documento. Puede ser nulo. |

### Excepciones

| excepción | condición |
| --- | --- |
| [UnsupportedFileFormatException](../../unsupportedfileformatexception/) | El formato del documento no se reconoce o no es compatible. |
| [FileCorruptedException](../../filecorruptedexception/) | El documento parece estar dañado y no se puede cargar. |
| Exception | Hay un problema con el documento y debe informarse a los desarrolladores de Aspose.Words. |
| IOException | Hay una excepción de entrada/salida. |
| [IncorrectPasswordException](../../incorrectpasswordexception/) | El documento está encriptado y requiere una contraseña para abrirlo, pero proporcionó una contraseña incorrecta. |
| ArgumentNullException | La secuencia no puede ser nula. |
| NotSupportedException | La transmisión no admite la lectura ni la búsqueda. |
| ObjectDisposedException | La corriente es un objeto desechado. |

### Observaciones

El documento debe almacenarse al principio de la secuencia. La secuencia debe admitir el posicionamiento aleatorio.

### Ejemplos

Muestra cómo cargar el contenido de un documento cifrado de Microsoft Word en texto sin formato mediante flujo.

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
* espacio de nombres [Aspose.Words](../../plaintextdocument/)
* asamblea [Aspose.Words](../../../)


