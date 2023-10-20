---
title: Document
linktitle: Document
articleTitle: Document
second_title: Aspose.Words para .NET
description: Document constructor. Crea un documento de Word en blanco en C#.
type: docs
weight: 10
url: /es/net/aspose.words/document/document/
---
## Document() {#constructor}

Crea un documento de Word en blanco.

```csharp
public Document()
```

## Observaciones

El tamaño del papel del documento es Carta de forma predeterminada. Si desea cambiar la configuración de la página, use [`PageSetup`](../../section/pagesetup/).

Después de la creación, puedes usar[`DocumentBuilder`](../../documentbuilder/) para agregar contenido al documento fácilmente.

## Ejemplos

Muestra cómo dar formato a una serie de texto usando su propiedad de fuente.

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
// Hay dos formas de crear un objeto Documento usando Aspose.Words.
// 1 - Crea un documento en blanco:
Document doc = new Document();

// Los nuevos objetos de documento vienen por defecto con el conjunto mínimo de nodos
// requerido para comenzar a agregar contenido como texto y formas: una sección, un cuerpo y un párrafo.
doc.FirstSection.Body.FirstParagraph.AppendChild(new Run(doc, "Hello world!"));

// 2 - Cargar un documento que existe en el sistema de archivos local:
doc = new Document(MyDir + "Document.docx");

// Los documentos cargados tendrán contenidos a los que podremos acceder y editar.
Assert.AreEqual("Hello World!", doc.FirstSection.Body.FirstParagraph.GetText().Trim());

// Algunas operaciones que deben realizarse durante la carga, como usar una contraseña para descifrar un documento,
// se puede hacer pasando un objeto LoadOptions al cargar el documento.
doc = new Document(MyDir + "Encrypted.docx", new LoadOptions("docPassword"));

Assert.AreEqual("Test encrypted document.", doc.FirstSection.Body.FirstParagraph.GetText().Trim());
```

### Ver también

* class [Document](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)

---

## Document(*string*) {#constructor_3}

Abre un documento existente desde un archivo. Detecta automáticamente el formato del archivo.

```csharp
public Document(string fileName)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| fileName | String | Nombre del archivo del documento a abrir. |

### Excepciones

| excepción | condición |
| --- | --- |
| [UnsupportedFileFormatException](../../unsupportedfileformatexception/) | El formato del documento no se reconoce o no se admite. |
| [FileCorruptedException](../../filecorruptedexception/) | El documento parece estar dañado y no se puede cargar. |
| Exception | Hay un problema con el documento y se debe informar a los desarrolladores de Aspose.Words. |
| IOException | Hay una excepción de entrada/salida. |
| [IncorrectPasswordException](../../incorrectpasswordexception/) | El documento está cifrado y requiere una contraseña para abrirse, pero usted proporcionó una contraseña incorrecta. |
| ArgumentException | El nombre del archivo no puede ser una cadena nula o vacía. |

## Ejemplos

Muestra cómo abrir un documento y convertirlo a .PDF.

```csharp
Document doc = new Document(MyDir + "Document.docx");

doc.Save(ArtifactsDir + "Document.ConvertToPdf.pdf");
```

Muestra cómo convertir un PDF a .docx.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Hello world!");

doc.Save(ArtifactsDir + "PDF2Word.ConvertPdfToDocx.pdf");

// Carga el documento PDF que acabamos de guardar y conviértelo a .docx.
Document pdfDoc = new Document(ArtifactsDir + "PDF2Word.ConvertPdfToDocx.pdf");

pdfDoc.Save(ArtifactsDir + "PDF2Word.ConvertPdfToDocx.docx");
```

Muestra cómo cargar un PDF.

```csharp
Aspose.Words.Document doc = new Aspose.Words.Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Hello world!");

doc.Save(ArtifactsDir + "PDF2Word.LoadPdf.pdf");

// A continuación se muestran dos formas de cargar documentos PDF utilizando los productos Aspose.
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
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)

---

## Document(*string, [LoadOptions](../../../aspose.words.loading/loadoptions/)*) {#constructor_4}

Abre un documento existente desde un archivo. Permite especificar opciones adicionales como una contraseña de cifrado.

```csharp
public Document(string fileName, LoadOptions loadOptions)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| fileName | String | Nombre del archivo del documento a abrir. |
| loadOptions | LoadOptions | Opciones adicionales para usar al cargar un documento. Puede ser`nulo`. |

### Excepciones

| excepción | condición |
| --- | --- |
| [UnsupportedFileFormatException](../../unsupportedfileformatexception/) | El formato del documento no se reconoce o no se admite. |
| [FileCorruptedException](../../filecorruptedexception/) | El documento parece estar dañado y no se puede cargar. |
| Exception | Hay un problema con el documento y se debe informar a los desarrolladores de Aspose.Words. |
| IOException | Hay una excepción de entrada/salida. |
| [IncorrectPasswordException](../../incorrectpasswordexception/) | El documento está cifrado y requiere una contraseña para abrirse, pero usted proporcionó una contraseña incorrecta. |
| ArgumentException | El nombre del archivo no puede ser una cadena nula o vacía. |

## Ejemplos

Muestra cómo cargar un documento cifrado de Microsoft Word.

```csharp
Document doc;

// Aspose.Words lanza una excepción si intentamos abrir un documento cifrado sin su contraseña.
Assert.Throws<IncorrectPasswordException>(() => doc = new Document(MyDir + "Encrypted.docx"));

// Al cargar dicho documento, la contraseña se pasa al constructor del documento mediante un objeto LoadOptions.
LoadOptions options = new LoadOptions("docPassword");

// Hay dos formas de cargar un documento cifrado con un objeto LoadOptions.
// 1 - Carga el documento desde el sistema de archivos local por nombre de archivo:
doc = new Document(MyDir + "Encrypted.docx", options);
// 2 - Cargar el documento desde una secuencia:
using (Stream stream = File.OpenRead(MyDir + "Encrypted.docx"))
{
    doc = new Document(stream, options);
}
```

Muestra cómo crear y cargar documentos.

```csharp
// Hay dos formas de crear un objeto Documento usando Aspose.Words.
// 1 - Crea un documento en blanco:
Document doc = new Document();

// Los nuevos objetos de documento vienen por defecto con el conjunto mínimo de nodos
// requerido para comenzar a agregar contenido como texto y formas: una sección, un cuerpo y un párrafo.
doc.FirstSection.Body.FirstParagraph.AppendChild(new Run(doc, "Hello world!"));

// 2 - Cargar un documento que existe en el sistema de archivos local:
doc = new Document(MyDir + "Document.docx");

// Los documentos cargados tendrán contenidos a los que podremos acceder y editar.
Assert.AreEqual("Hello World!", doc.FirstSection.Body.FirstParagraph.GetText().Trim());

// Algunas operaciones que deben realizarse durante la carga, como usar una contraseña para descifrar un documento,
// se puede hacer pasando un objeto LoadOptions al cargar el documento.
doc = new Document(MyDir + "Encrypted.docx", new LoadOptions("docPassword"));

Assert.AreEqual("Test encrypted document.", doc.FirstSection.Body.FirstParagraph.GetText().Trim());
```

### Ver también

* class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* class [Document](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)

---

## Document(*Stream*) {#constructor_1}

Abre un documento existente desde una secuencia. Detecta automáticamente el formato del archivo.

```csharp
public Document(Stream stream)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| stream | Stream | Transmita desde dónde cargar el documento. |

### Excepciones

| excepción | condición |
| --- | --- |
| [UnsupportedFileFormatException](../../unsupportedfileformatexception/) | El formato del documento no se reconoce o no se admite. |
| [FileCorruptedException](../../filecorruptedexception/) | El documento parece estar dañado y no se puede cargar. |
| Exception | Hay un problema con el documento y se debe informar a los desarrolladores de Aspose.Words. |
| IOException | Hay una excepción de entrada/salida. |
| [IncorrectPasswordException](../../incorrectpasswordexception/) | El documento está cifrado y requiere una contraseña para abrirse, pero usted proporcionó una contraseña incorrecta. |
| ArgumentNullException | La secuencia no puede ser nula. |
| NotSupportedException | La transmisión no admite lectura ni búsqueda. |
| ObjectDisposedException | El arroyo es un objeto desechado. |

## Observaciones

El documento debe almacenarse al comienzo de la secuencia. La transmisión debe admitir el posicionamiento aleatorio.

## Ejemplos

Muestra cómo cargar un documento usando una secuencia.

```csharp
using (Stream stream = File.OpenRead(MyDir + "Document.docx"))
{
    Document doc = new Document(stream);

    Assert.AreEqual("Hello World!\r\rHello Word!\r\r\rHello World!", doc.GetText().Trim());
}
```

Muestra cómo cargar un documento desde una URL.

```csharp
// Crea una URL que apunte a un documento de Microsoft Word.
const string url = "https://filesamples.com/samples/document/docx/sample3.docx";

// Descargue el documento en una matriz de bytes, luego cargue esa matriz en un documento usando un flujo de memoria.
using (HttpClient webClient = new HttpClient())
{
    byte[] dataBytes = await webClient.GetByteArrayAsync(url);

    using (MemoryStream byteStream = new MemoryStream(dataBytes))
    {
        Document doc = new Document(byteStream);

        // En esta etapa, podemos leer y editar el contenido del documento y luego guardarlo en el sistema de archivos local.
        Assert.AreEqual("There are eight section headings in this document. At the beginning, \"Sample Document\" is a level 1 heading. " +
            "The main section headings, such as \"Headings\" and \"Lists\" are level 2 headings. " +
            "The Tables section contains two sub-headings, \"Simple Table\" and \"Complex Table,\" which are both level 3 headings.",                         
            doc.FirstSection.Body.Paragraphs[3].GetText().Trim());

        doc.Save(ArtifactsDir + "Document.LoadFromWeb.docx");
    }
}
```

### Ver también

* class [Document](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)

---

## Document(*Stream, [LoadOptions](../../../aspose.words.loading/loadoptions/)*) {#constructor_2}

Abre un documento existente desde una secuencia. Permite especificar opciones adicionales como una contraseña de cifrado.

```csharp
public Document(Stream stream, LoadOptions loadOptions)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| stream | Stream | La secuencia desde donde cargar el documento. |
| loadOptions | LoadOptions | Opciones adicionales para usar al cargar un documento. Puede ser`nulo`. |

### Excepciones

| excepción | condición |
| --- | --- |
| [UnsupportedFileFormatException](../../unsupportedfileformatexception/) | El formato del documento no se reconoce o no se admite. |
| [FileCorruptedException](../../filecorruptedexception/) | El documento parece estar dañado y no se puede cargar. |
| Exception | Hay un problema con el documento y se debe informar a los desarrolladores de Aspose.Words. |
| IOException | Hay una excepción de entrada/salida. |
| [IncorrectPasswordException](../../incorrectpasswordexception/) | El documento está cifrado y requiere una contraseña para abrirse, pero usted proporcionó una contraseña incorrecta. |
| ArgumentNullException | La secuencia no puede ser nula. |
| NotSupportedException | La transmisión no admite lectura ni búsqueda. |
| ObjectDisposedException | El arroyo es un objeto desechado. |

## Observaciones

El documento debe almacenarse al comienzo de la secuencia. La transmisión debe admitir el posicionamiento aleatorio.

## Ejemplos

Muestra cómo abrir un documento HTML con imágenes de una secuencia utilizando un URI base.

```csharp
using (Stream stream = File.OpenRead(MyDir + "Document.html"))
{
    // Pasa el URI de la carpeta base mientras la cargas
    // para que se puedan encontrar todas las imágenes con URI relativos en el documento HTML.
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

Muestra cómo guardar una página web como un archivo .docx.

```csharp
const string url = "https://www.aspose.com/";

using (HttpClient client = new HttpClient()) 
{
    var bytes = await client.GetByteArrayAsync(url);
    using (MemoryStream stream = new MemoryStream(bytes))
    {
        // La URL se utiliza nuevamente como baseUri para garantizar que las rutas de imagen relativas se recuperen correctamente.
        LoadOptions options = new LoadOptions(LoadFormat.Html, "", url);

        // Carga el documento HTML desde la secuencia y pasa el objeto LoadOptions.
        Document doc = new Document(stream, options);

        // En esta etapa, podemos leer y editar el contenido del documento y luego guardarlo en el sistema de archivos local.
        doc.Save(ArtifactsDir + "Document.InsertHtmlFromWebPage.docx");
    }
}
```

Muestra cómo cargar un documento cifrado de Microsoft Word.

```csharp
Document doc;

// Aspose.Words lanza una excepción si intentamos abrir un documento cifrado sin su contraseña.
Assert.Throws<IncorrectPasswordException>(() => doc = new Document(MyDir + "Encrypted.docx"));

// Al cargar dicho documento, la contraseña se pasa al constructor del documento mediante un objeto LoadOptions.
LoadOptions options = new LoadOptions("docPassword");

// Hay dos formas de cargar un documento cifrado con un objeto LoadOptions.
// 1 - Carga el documento desde el sistema de archivos local por nombre de archivo:
doc = new Document(MyDir + "Encrypted.docx", options);
// 2 - Cargar el documento desde una secuencia:
using (Stream stream = File.OpenRead(MyDir + "Encrypted.docx"))
{
    doc = new Document(stream, options);
}
```

### Ver también

* class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* class [Document](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
