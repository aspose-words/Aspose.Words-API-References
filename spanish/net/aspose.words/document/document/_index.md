---
title: Document
linktitle: Document
articleTitle: Document
second_title: Aspose.Words para .NET
description: Crea fácilmente documentos de Word en blanco con nuestro constructor de documentos intuitivo. ¡Optimiza tu proceso de escritura hoy mismo!
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

Se recupera un documento en blanco de los recursos y, de forma predeterminada, el documento resultante se parece más al creado porWord2007. Este documento en blanco contiene una tabla de fuentes predeterminadas, estilos predeterminados mínimos y estilos latentes.

[`OptimizeFor`](../../../aspose.words.settings/compatibilityoptions/optimizefor/) Este método se puede utilizar para optimizar el contenido del documento, así como el comportamiento predeterminado de Aspose.Words para una versión particular de MS Word.

El tamaño de papel del documento predeterminado es Carta. Si desea cambiar la configuración de página, use [`PageSetup`](../../section/pagesetup/).

Después de la creación, puedes utilizar[`DocumentBuilder`](../../documentbuilder/) para agregar contenido al documento fácilmente.

## Ejemplos

Muestra cómo formatear una serie de texto utilizando su propiedad de fuente.

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

Muestra cómo crear un documento simple.

```csharp
Document doc = new Document();

// Los nuevos objetos de documento vienen por defecto con el conjunto mínimo de nodos
// necesario para comenzar a agregar contenido como texto y formas: una Sección, un Cuerpo y un Párrafo.
doc.AppendChild(new Section(doc))
    .AppendChild(new Body(doc))
    .AppendChild(new Paragraph(doc))
    .AppendChild(new Run(doc, "Hello world!"));
```

Muestra cómo crear y cargar documentos.

```csharp
// Hay dos formas de crear un objeto Documento usando Aspose.Words.
// 1 - Crear un documento en blanco:
Document doc = new Document();

// Los nuevos objetos de documento vienen por defecto con el conjunto mínimo de nodos
// necesario para comenzar a agregar contenido como texto y formas: una Sección, un Cuerpo y un Párrafo.
doc.FirstSection.Body.FirstParagraph.AppendChild(new Run(doc, "Hello world!"));

// 2 - Cargar un documento que existe en el sistema de archivos local:
doc = new Document(MyDir + "Document.docx");

//Los documentos cargados tendrán contenidos a los que podremos acceder y editar.
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
| [UnsupportedFileFormatException](../../unsupportedfileformatexception/) | El formato del documento no es reconocido o no es compatible. |
| [FileCorruptedException](../../filecorruptedexception/) | El documento parece estar dañado y no se puede cargar. |
| Exception | Hay un problema con el documento y debe informarse a los desarrolladores de Aspose.Words. |
| IOException | Hay una excepción de entrada/salida. |
| [IncorrectPasswordException](../../incorrectpasswordexception/) | El documento está encriptado y requiere una contraseña para abrirlo, pero usted proporcionó una contraseña incorrecta. |
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

//Cargamos el documento PDF que acabamos de guardar y lo convertimos a .docx.
Document pdfDoc = new Document(ArtifactsDir + "PDF2Word.ConvertPdfToDocx.pdf");

pdfDoc.Save(ArtifactsDir + "PDF2Word.ConvertPdfToDocx.docx");
```

Muestra cómo cargar un PDF.

```csharp
Document doc = new Aspose.Words.Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Hello world!");

doc.Save(ArtifactsDir + "PDF2Word.LoadPdf.pdf");

A continuación se muestran dos formas de cargar documentos PDF utilizando productos Aspose.
// 1 - Cargar como un documento Aspose.Words:
Document asposeWordsDoc = new Document(ArtifactsDir + "PDF2Word.LoadPdf.pdf");

Assert.AreEqual("Hello world!", asposeWordsDoc.GetText().Trim());

// 2 - Cargar como un documento Aspose.Pdf:
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

Abre un documento existente desde un archivo. Permite especificar opciones adicionales, como una contraseña de cifrado.

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
| [UnsupportedFileFormatException](../../unsupportedfileformatexception/) | El formato del documento no es reconocido o no es compatible. |
| [FileCorruptedException](../../filecorruptedexception/) | El documento parece estar dañado y no se puede cargar. |
| Exception | Hay un problema con el documento y debe informarse a los desarrolladores de Aspose.Words. |
| IOException | Hay una excepción de entrada/salida. |
| [IncorrectPasswordException](../../incorrectpasswordexception/) | El documento está encriptado y requiere una contraseña para abrirlo, pero usted proporcionó una contraseña incorrecta. |
| ArgumentException | El nombre del archivo no puede ser una cadena nula o vacía. |

## Ejemplos

Muestra cómo cargar un documento de Microsoft Word cifrado.

```csharp
Document doc;

// Aspose.Words lanza una excepción si intentamos abrir un documento cifrado sin su contraseña.
Assert.Throws<IncorrectPasswordException>(() => doc = new Document(MyDir + "Encrypted.docx"));

// Al cargar dicho documento, la contraseña se pasa al constructor del documento mediante un objeto LoadOptions.
LoadOptions options = new LoadOptions("docPassword");

// Hay dos formas de cargar un documento cifrado con un objeto LoadOptions.
// 1 - Cargar el documento desde el sistema de archivos local por nombre de archivo:
doc = new Document(MyDir + "Encrypted.docx", options);
// 2 - Cargar el documento desde un stream:
using (Stream stream = File.OpenRead(MyDir + "Encrypted.docx"))
{
    doc = new Document(stream, options);
}
```

Muestra cómo crear y cargar documentos.

```csharp
// Hay dos formas de crear un objeto Documento usando Aspose.Words.
// 1 - Crear un documento en blanco:
Document doc = new Document();

// Los nuevos objetos de documento vienen por defecto con el conjunto mínimo de nodos
// necesario para comenzar a agregar contenido como texto y formas: una Sección, un Cuerpo y un Párrafo.
doc.FirstSection.Body.FirstParagraph.AppendChild(new Run(doc, "Hello world!"));

// 2 - Cargar un documento que existe en el sistema de archivos local:
doc = new Document(MyDir + "Document.docx");

//Los documentos cargados tendrán contenidos a los que podremos acceder y editar.
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
| stream | Stream | Transmite desde donde cargar el documento. |

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

Muestra cómo cargar un documento mediante una secuencia.

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

// Descargue el documento en una matriz de bytes y luego cargue esa matriz en un documento usando un flujo de memoria.
using (WebClient webClient = new WebClient())
{
    byte[] dataBytes = webClient.DownloadData(url);

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

Abre un documento existente desde una secuencia. Permite especificar opciones adicionales, como una contraseña de cifrado.

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

Muestra cómo abrir un documento HTML con imágenes desde una transmisión usando una URI base.

```csharp
using (Stream stream = File.OpenRead(MyDir + "Document.html"))
{
    // Pasar la URI de la carpeta base mientras se carga
    // para que se puedan encontrar todas las imágenes con URI relativas en el documento HTML.
    LoadOptions loadOptions = new LoadOptions();
    loadOptions.BaseUri = ImageDir;

    Document doc = new Document(stream, loadOptions);

    // Verifique que la primera forma del documento contenga una imagen válida.
    Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

    Assert.IsTrue(shape.IsImage);
    Assert.IsNotNull(shape.ImageData.ImageBytes);
    Assert.AreEqual(32.0, ConvertUtil.PointToPixel(shape.Width), 0.01);
    Assert.AreEqual(32.0, ConvertUtil.PointToPixel(shape.Height), 0.01);
}
```

Muestra cómo guardar una página web como un archivo .docx.

```csharp
const string url = "https://productos.aspose.com/palabras/";

using (WebClient client = new WebClient())
{
    var bytes = client.DownloadData(url);
    using (MemoryStream stream = new MemoryStream(bytes))
    {
        // La URL se utiliza nuevamente como baseUri para garantizar que todas las rutas de imágenes relativas se recuperen correctamente.
        LoadOptions options = new LoadOptions(LoadFormat.Html, "", url);

        // Cargue el documento HTML desde el stream y pase el objeto LoadOptions.
        Document doc = new Document(stream, options);

        // En esta etapa, podemos leer y editar el contenido del documento y luego guardarlo en el sistema de archivos local.
        doc.Save(ArtifactsDir + "Document.InsertHtmlFromWebPage.docx");
    }
}
```

Muestra cómo cargar un documento de Microsoft Word cifrado.

```csharp
Document doc;

// Aspose.Words lanza una excepción si intentamos abrir un documento cifrado sin su contraseña.
Assert.Throws<IncorrectPasswordException>(() => doc = new Document(MyDir + "Encrypted.docx"));

// Al cargar dicho documento, la contraseña se pasa al constructor del documento mediante un objeto LoadOptions.
LoadOptions options = new LoadOptions("docPassword");

// Hay dos formas de cargar un documento cifrado con un objeto LoadOptions.
// 1 - Cargar el documento desde el sistema de archivos local por nombre de archivo:
doc = new Document(MyDir + "Encrypted.docx", options);
// 2 - Cargar el documento desde un stream:
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
