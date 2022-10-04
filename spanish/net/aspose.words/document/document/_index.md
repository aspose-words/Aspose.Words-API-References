---
title: Document
second_title: Referencia de API de Aspose.Words para .NET
description: Crea un documento de Word en blanco.
type: docs
weight: 10
url: /es/net/aspose.words/document/document/
---
## Document() {#constructor}

Crea un documento de Word en blanco.

```csharp
public Document()
```

### Observaciones

El tamaño de papel del documento es Carta de forma predeterminada. Si desea cambiar la configuración de la página, use [`Sección.Configuración de página`](../../section/pagesetup/).

Después de la creación, puede utilizar[`DocumentBuilder`](../../documentbuilder/) para agregar contenido del documento fácilmente.

### Ejemplos

Muestra cómo dar formato a una tirada de texto utilizando su propiedad de fuente.

```csharp
Document doc = new Document();
Run run = new Run(doc, "Hello world!");

Aspose.Words.Font font = run.Font;
font.Name = "Courier New";
font.Size = 36;
font.HighlightColor = Color.Yellow;

doc.FirstSection.Body.FirstParagraph.AppendChild(run);
doc.Save(ArtifactsDir + "Font.CreateFormattedRun.docx");
```

Muestra cómo crear y cargar documentos.

```csharp
// Hay dos formas de crear un objeto Documento utilizando Aspose.Words.
// 1 - Crea un documento en blanco:
Document doc = new Document();

// Los objetos New Document por defecto vienen con el conjunto mínimo de nodos
// requerido para comenzar a agregar contenido como texto y formas: una sección, un cuerpo y un párrafo.
doc.FirstSection.Body.FirstParagraph.AppendChild(new Run(doc, "Hello world!"));

// 2 - Carga un documento que existe en el sistema de archivos local:
doc = new Document(MyDir + "Document.docx");

// Los documentos cargados tendrán contenidos a los que podemos acceder y editar.
Assert.AreEqual("Hello World!", doc.FirstSection.Body.FirstParagraph.GetText().Trim());

// Algunas operaciones que deben ocurrir durante la carga, como usar una contraseña para descifrar un documento,
// se puede hacer pasando un objeto LoadOptions al cargar el documento.
doc = new Document(MyDir + "Encrypted.docx", new LoadOptions("docPassword"));

Assert.AreEqual("Test encrypted document.", doc.FirstSection.Body.FirstParagraph.GetText().Trim());
```

### Ver también

* class [Document](../)
* espacio de nombres [Aspose.Words](../../document/)
* asamblea [Aspose.Words](../../../)

---

## Document(string) {#constructor_3}

Abre un documento existente de un archivo. Detecta automáticamente el formato de archivo.

```csharp
public Document(string fileName)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| fileName | String | Nombre de archivo del documento a abrir. |

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

Muestra cómo abrir un documento y convertirlo a .PDF.

```csharp
Document doc = new Document(MyDir + "Document.docx");

doc.Save(ArtifactsDir + "Document.ConvertToPdf.pdf");
```

Muestra cómo convertir un PDF a un .docx.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Hello world!");

doc.Save(ArtifactsDir + "PDF2Word.ConvertPdfToDocx.pdf");

// Cargue el documento PDF que acabamos de guardar y conviértalo a .docx.
Document pdfDoc = new Document(ArtifactsDir + "PDF2Word.ConvertPdfToDocx.pdf");

pdfDoc.Save(ArtifactsDir + "PDF2Word.ConvertPdfToDocx.docx");
```

Muestra cómo cargar un PDF.

```csharp
Aspose.Words.Document doc = new Aspose.Words.Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Hello world!");

doc.Save(ArtifactsDir + "PDF2Word.LoadPdf.pdf");

// A continuación se muestran dos formas de cargar documentos PDF utilizando productos Aspose.
// 1 - Cargar como documento Aspose.Words:
Aspose.Words.Document asposeWordsDoc = new Aspose.Words.Document(ArtifactsDir + "PDF2Word.LoadPdf.pdf");

Assert.AreEqual("Hello world!", asposeWordsDoc.GetText().Trim());

// 2 - Cargar como documento Aspose.Pdf:
Aspose.Pdf.Document asposePdfDoc = new Aspose.Pdf.Document(ArtifactsDir + "PDF2Word.LoadPdf.pdf");

TextFragmentAbsorber textFragmentAbsorber = new TextFragmentAbsorber();
asposePdfDoc.Pages.Accept(textFragmentAbsorber);

Assert.AreEqual("Hello world!", textFragmentAbsorber.Text.Trim());
```

### Ver también

* class [Document](../)
* espacio de nombres [Aspose.Words](../../document/)
* asamblea [Aspose.Words](../../../)

---

## Document(string, LoadOptions) {#constructor_4}

Abre un documento existente de un archivo. Permite especificar opciones adicionales como una contraseña de cifrado.

```csharp
public Document(string fileName, LoadOptions loadOptions)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| fileName | String | Nombre de archivo del documento a abrir. |
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

Muestra cómo cargar un documento cifrado de Microsoft Word.

```csharp
Document doc;

// Aspose.Words lanza una excepción si intentamos abrir un documento encriptado sin su contraseña.
Assert.Throws<IncorrectPasswordException>(() => doc = new Document(MyDir + "Encrypted.docx"));

// Al cargar un documento de este tipo, la contraseña se pasa al constructor del documento mediante un objeto LoadOptions.
LoadOptions options = new LoadOptions("docPassword");

// Hay dos formas de cargar un documento cifrado con un objeto LoadOptions.
// 1 - Cargar el documento desde el sistema de archivos local por nombre de archivo:
doc = new Document(MyDir + "Encrypted.docx", options);
// 2 - Cargar el documento desde un stream:
using (Stream stream = File.OpenRead(MyDir + "Encrypted.docx"))
{
    doc = new Document(stream, options);
```

Muestra cómo crear y cargar documentos.

```csharp
// Hay dos formas de crear un objeto Documento utilizando Aspose.Words.
// 1 - Crea un documento en blanco:
Document doc = new Document();

// Los objetos New Document por defecto vienen con el conjunto mínimo de nodos
// requerido para comenzar a agregar contenido como texto y formas: una sección, un cuerpo y un párrafo.
doc.FirstSection.Body.FirstParagraph.AppendChild(new Run(doc, "Hello world!"));

// 2 - Carga un documento que existe en el sistema de archivos local:
doc = new Document(MyDir + "Document.docx");

// Los documentos cargados tendrán contenidos a los que podemos acceder y editar.
Assert.AreEqual("Hello World!", doc.FirstSection.Body.FirstParagraph.GetText().Trim());

// Algunas operaciones que deben ocurrir durante la carga, como usar una contraseña para descifrar un documento,
// se puede hacer pasando un objeto LoadOptions al cargar el documento.
doc = new Document(MyDir + "Encrypted.docx", new LoadOptions("docPassword"));

Assert.AreEqual("Test encrypted document.", doc.FirstSection.Body.FirstParagraph.GetText().Trim());
```

### Ver también

* class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* class [Document](../)
* espacio de nombres [Aspose.Words](../../document/)
* asamblea [Aspose.Words](../../../)

---

## Document(Stream) {#constructor_1}

Abre un documento existente de una secuencia. Detecta automáticamente el formato de archivo.

```csharp
public Document(Stream stream)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| stream | Stream | Transmitir desde dónde cargar el documento. |

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

Muestra cómo cargar un documento utilizando una secuencia.

```csharp
using (Stream stream = File.OpenRead(MyDir + "Document.docx"))
{
    Document doc = new Document(stream);

    Assert.AreEqual("Hello World!\r\rHello Word!\r\r\rHello World!", doc.GetText().Trim());
}
```

Muestra cómo cargar un documento desde una URL.

```csharp
// Crear una URL que apunte a un documento de Microsoft Word.
const string url = "https://omextemplates.content.office.net/support/templates/en-us/tf16402488.dotx";

// Descargue el documento en una matriz de bytes, luego cargue esa matriz en un documento usando un flujo de memoria.
using (WebClient webClient = new WebClient())
{
    byte[] dataBytes = webClient.DownloadData(url);

    using (MemoryStream byteStream = new MemoryStream(dataBytes))
    {
        Document doc = new Document(byteStream);

        // En esta etapa, podemos leer y editar el contenido del documento y luego guardarlo en el sistema de archivos local.
        Assert.AreEqual("Use this section to highlight your relevant passions, activities, and how you like to give back. " +
                        "It’s good to include Leadership and volunteer experiences here. " +
                        "Or show off important extras like publications, certifications, languages and more.",
            doc.FirstSection.Body.Paragraphs[4].GetText().Trim());

        doc.Save(ArtifactsDir + "Document.LoadFromWeb.docx");
    }
}
```

### Ver también

* class [Document](../)
* espacio de nombres [Aspose.Words](../../document/)
* asamblea [Aspose.Words](../../../)

---

## Document(Stream, LoadOptions) {#constructor_2}

Abre un documento existente de una secuencia. Permite especificar opciones adicionales como una contraseña de cifrado.

```csharp
public Document(Stream stream, LoadOptions loadOptions)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| stream | Stream | El flujo desde donde cargar el documento. |
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

Muestra cómo guardar una página web como un archivo .docx.

```csharp
const string url = "http://www.aspose.com/";

using (WebClient client = new WebClient()) 
{ 
    using (MemoryStream stream = new MemoryStream(client.DownloadData(url)))
    {
        // La URL se usa nuevamente como baseUri para garantizar que las rutas de imagen relativas se recuperen correctamente.
        LoadOptions options = new LoadOptions(LoadFormat.Html, "", url);

        // Cargue el documento HTML desde la secuencia y pase el objeto LoadOptions.
        Document doc = new Document(stream, options);

        // En esta etapa, podemos leer y editar el contenido del documento y luego guardarlo en el sistema de archivos local.
        doc.Save(ArtifactsDir + "Document.InsertHtmlFromWebPage.docx");
    }
}
```

Muestra cómo abrir un documento HTML con imágenes de una transmisión usando un URI base.

```csharp
using (Stream stream = File.OpenRead(MyDir + "Document.html"))
{
    // Pasar la URI de la carpeta base mientras se carga
    // para que se puedan encontrar todas las imágenes con URI relativas en el documento HTML.
    LoadOptions loadOptions = new LoadOptions();
    loadOptions.BaseUri = ImageDir;

    Document doc = new Document(stream, loadOptions);

    // Verifica que la primera forma del documento contenga una imagen válida.
    Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

    Assert.IsTrue(shape.IsImage);
    Assert.IsNotNull(shape.ImageData.ImageBytes);
    Assert.AreEqual(32.0, ConvertUtil.PointToPixel(shape.Width), 0.01);
    Assert.AreEqual(32.0, ConvertUtil.PointToPixel(shape.Height), 0.01);
}
```

Muestra cómo cargar un documento cifrado de Microsoft Word.

```csharp
Document doc;

// Aspose.Words lanza una excepción si intentamos abrir un documento encriptado sin su contraseña.
Assert.Throws<IncorrectPasswordException>(() => doc = new Document(MyDir + "Encrypted.docx"));

// Al cargar un documento de este tipo, la contraseña se pasa al constructor del documento mediante un objeto LoadOptions.
LoadOptions options = new LoadOptions("docPassword");

// Hay dos formas de cargar un documento cifrado con un objeto LoadOptions.
// 1 - Cargar el documento desde el sistema de archivos local por nombre de archivo:
doc = new Document(MyDir + "Encrypted.docx", options);
// 2 - Cargar el documento desde un stream:
using (Stream stream = File.OpenRead(MyDir + "Encrypted.docx"))
{
    doc = new Document(stream, options);
```

### Ver también

* class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* class [Document](../)
* espacio de nombres [Aspose.Words](../../document/)
* asamblea [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
