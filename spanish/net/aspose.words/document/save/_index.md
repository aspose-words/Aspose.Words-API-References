---
title: Document.Save
linktitle: Save
articleTitle: Save
second_title: Aspose.Words para .NET
description: Guarde sus documentos sin esfuerzo con nuestro método de guardado inteligente, que selecciona automáticamente el formato correcto según la extensión del archivo para un almacenamiento perfecto.
type: docs
weight: 750
url: /es/net/aspose.words/document/save/
---
## Save(*string*) {#save_2}

Guarda el documento en un archivo. Determina automáticamente el formato de guardado a partir de la extensión.

```csharp
public SaveOutputParameters Save(string fileName)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| fileName | String | El nombre del documento. Si ya existe un documento con el nombre de archivo especificado , se sobrescribirá. |

### Valor_devuelto

Información adicional que puedes utilizar opcionalmente.

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

### Ver también

* class [SaveOutputParameters](../../../aspose.words.saving/saveoutputparameters/)
* class [Document](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)

---

## Save(*string, [SaveFormat](../../saveformat/)*) {#save_3}

Guarda el documento en un archivo en el formato especificado.

```csharp
public SaveOutputParameters Save(string fileName, SaveFormat saveFormat)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| fileName | String | El nombre del documento. Si ya existe un documento con el nombre de archivo especificado , se sobrescribirá. |
| saveFormat | SaveFormat | El formato en el que guardar el documento. |

### Valor_devuelto

Información adicional que puedes utilizar opcionalmente.

## Ejemplos

Muestra cómo convertir del formato DOCX al HTML.

```csharp
Document doc = new Document(MyDir + "Document.docx");

doc.Save(ArtifactsDir + "Document.ConvertToHtml.html", SaveFormat.Html);
```

### Ver también

* class [SaveOutputParameters](../../../aspose.words.saving/saveoutputparameters/)
* enum [SaveFormat](../../saveformat/)
* class [Document](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)

---

## Save(*string, [SaveOptions](../../../aspose.words.saving/saveoptions/)*) {#save_4}

Guarda el documento en un archivo utilizando las opciones de guardado especificadas.

```csharp
public SaveOutputParameters Save(string fileName, SaveOptions saveOptions)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| fileName | String | El nombre del documento. Si ya existe un documento con el nombre de archivo especificado , se sobrescribirá. |
| saveOptions | SaveOptions | Especifica las opciones que controlan cómo se guarda el documento. Puede ser`nulo`. |

### Valor_devuelto

Información adicional que puedes utilizar opcionalmente.

## Ejemplos

Muestra cómo mejorar la calidad de un documento renderizado con SaveOptions.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Size = 60;
builder.Writeln("Some text.");

SaveOptions options = new ImageSaveOptions(SaveFormat.Jpeg);
doc.Save(ArtifactsDir + "Document.ImageSaveOptions.Default.jpg", options);

options.UseAntiAliasing = true;
options.UseHighQualityRendering = true;

doc.Save(ArtifactsDir + "Document.ImageSaveOptions.HighQuality.jpg", options);
```

Muestra cómo convertir un PDF a .docx y personalizar el proceso de guardado con un objeto SaveOptions.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");

doc.Save(ArtifactsDir + "PDF2Word.ConvertPdfToDocxCustom.pdf");

//Cargamos el documento PDF que acabamos de guardar y lo convertimos a .docx.
Document pdfDoc = new Document(ArtifactsDir + "PDF2Word.ConvertPdfToDocxCustom.pdf");

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions(SaveFormat.Docx);

// Establezca la propiedad "Contraseña" para cifrar el documento guardado con una contraseña.
saveOptions.Password = "MyPassword";

pdfDoc.Save(ArtifactsDir + "PDF2Word.ConvertPdfToDocxCustom.docx", saveOptions);
```

Muestra cómo convertir cada página de un documento en una imagen TIFF independiente.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Page 1.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 2.");
builder.InsertImage(ImageDir + "Logo.jpg");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 3.");

// Crea un objeto "ImageSaveOptions" que podemos pasar al método "Guardar" del documento
// para modificar la forma en que ese método convierte el documento en una imagen.
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);

for (int i = 0; i < doc.PageCount; i++)
{
    // Establezca la propiedad "PageSet" en el número de la primera página desde
    // desde donde comenzar a renderizar el documento.
    options.PageSet = new PageSet(i);
    // Exportar página a 2325x5325 píxeles y 600 dpi.
    options.Resolution = 600;
    options.ImageSize = new Size(2325, 5325);

    doc.Save(ArtifactsDir + $"ImageSaveOptions.PageByPage.{i + 1}.tiff", options);
}
```

Muestra cómo convertir una página de un documento en una imagen JPEG.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Page 1.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 2.");
builder.InsertImage(ImageDir + "Logo.jpg");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 3.");

// Crea un objeto "ImageSaveOptions" que podemos pasar al método "Guardar" del documento
// para modificar la forma en que ese método convierte el documento en una imagen.
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Jpeg);
// Establezca "PageSet" en "1" para seleccionar la segunda página mediante
// el índice basado en cero desde el cual comenzar a renderizar el documento.
options.PageSet = new PageSet(1);

// Cuando guardamos el documento en formato JPEG, Aspose.Words solo renderiza una página.
//Esta imagen contendrá una página a partir de la página dos,
// que será sólo la segunda página del documento original.
doc.Save(ArtifactsDir + "ImageSaveOptions.OnePage.jpg", options);
```

Muestra cómo configurar la compresión al guardar un documento como JPEG.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertImage(ImageDir + "Logo.jpg");

// Crea un objeto "ImageSaveOptions" que podemos pasar al método "Guardar" del documento
// para modificar la forma en que ese método convierte el documento en una imagen.
ImageSaveOptions imageOptions = new ImageSaveOptions(SaveFormat.Jpeg);
// Establezca la propiedad "JpegQuality" en "10" para utilizar una compresión más fuerte al renderizar el documento.
// Esto reducirá el tamaño del archivo del documento, pero la imagen mostrará artefactos de compresión más prominentes.
imageOptions.JpegQuality = 10;
doc.Save(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighCompression.jpg", imageOptions);

// Establezca la propiedad "JpegQuality" en "100" para utilizar una compresión más débil al renderizar el documento.
// Esto mejorará la calidad de la imagen a costa de un mayor tamaño de archivo.
imageOptions.JpegQuality = 100;
doc.Save(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighQuality.jpg", imageOptions);
```

Muestra cómo convertir un documento completo a PDF con tres niveles en el esquema del documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insertar encabezados de niveles 1 al 5.
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;

Assert.True(builder.ParagraphFormat.IsHeading);

builder.Writeln("Heading 1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;

builder.Writeln("Heading 1.1");
builder.Writeln("Heading 1.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading3;

builder.Writeln("Heading 1.2.1");
builder.Writeln("Heading 1.2.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading4;

builder.Writeln("Heading 1.2.2.1");
builder.Writeln("Heading 1.2.2.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading5;

builder.Writeln("Heading 1.2.2.2.1");
builder.Writeln("Heading 1.2.2.2.2");

// Crea un objeto "PdfSaveOptions" que podamos pasar al método "Guardar" del documento
// para modificar la forma en que ese método convierte el documento a .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// El documento PDF de salida contendrá un esquema, que es una tabla de contenidos que enumera los encabezados en el cuerpo del documento.
// Al hacer clic en una entrada de este esquema accederemos a la ubicación de su encabezado respectivo.
// Establezca la propiedad "HeadingsOutlineLevels" en "4" para excluir del esquema todos los encabezados cuyos niveles sean superiores a 4.
options.OutlineOptions.HeadingsOutlineLevels = 4;

// Si una entrada de esquema tiene entradas subsiguientes de un nivel superior entre ella y la siguiente entrada del mismo nivel o de un nivel inferior,
Aparecerá una flecha a la izquierda de la entrada. Esta entrada es la "propietaria" de varias subentradas similares.
// En nuestro documento, las entradas del esquema del quinto nivel de encabezado son subentradas de la segunda entrada del esquema del cuarto nivel.
// las entradas de nivel de encabezado 4º y 5º son subentradas de la segunda entrada de nivel 3, y así sucesivamente.
// En el esquema, podemos hacer clic en la flecha de la entrada "propietario" para contraer/expandir todas sus subentradas.
// Establezca la propiedad "ExpandedOutlineLevels" en "2" para expandir automáticamente todas las entradas de encabezado de nivel 2 y de esquema inferior
// y colapsar todas las entradas de nivel 3 y superiores cuando abrimos el documento.
options.OutlineOptions.ExpandedOutlineLevels = 2;

doc.Save(ArtifactsDir + "PdfSaveOptions.ExpandedOutlineLevels.pdf", options);
```

### Ver también

* class [SaveOutputParameters](../../../aspose.words.saving/saveoutputparameters/)
* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [Document](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)

---

## Save(*Stream, [SaveFormat](../../saveformat/)*) {#save}

Guarda el documento en una secuencia usando el formato especificado.

```csharp
public SaveOutputParameters Save(Stream stream, SaveFormat saveFormat)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| stream | Stream | Transmite dónde guardar el documento. |
| saveFormat | SaveFormat | El formato en el que guardar el documento. |

### Valor_devuelto

Información adicional que puedes utilizar opcionalmente.

## Ejemplos

Muestra cómo guardar un documento en una secuencia.

```csharp
Document doc = new Document(MyDir + "Document.docx");

using (MemoryStream dstStream = new MemoryStream())
{
    doc.Save(dstStream, SaveFormat.Docx);

    // Verifique que el flujo contenga el documento.
    Assert.AreEqual("Hello World!\r\rHello Word!\r\r\rHello World!", new Document(dstStream).GetText().Trim());
}
```

Muestra cómo guardar un documento en una imagen a través de una secuencia y luego leer la imagen desde esa secuencia.

```csharp
Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            builder.Font.Name = "Times New Roman";
            builder.Font.Size = 24;
            builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

            builder.InsertImage(ImageDir + "Logo.jpg");

#if NET461_OR_GREATER || JAVA
            using (MemoryStream stream = new MemoryStream())
            {
                doc.Save(stream, SaveFormat.Bmp);

                stream.Position = 0;

                //Lee la secuencia nuevamente en una imagen.
                using (Image image = Image.FromStream(stream))
                {
                    Assert.AreEqual(ImageFormat.Bmp, image.RawFormat);
                    Assert.AreEqual(816, image.Width);
                    Assert.AreEqual(1056, image.Height);
                }
            }
#elif NET5_0_OR_GREATER
            using (MemoryStream stream = new MemoryStream())
            {
                doc.Save(stream, SaveFormat.Bmp);

                stream.Position = 0;

                SKCodec codec = SKCodec.Create(stream);
                Assert.AreEqual(SKEncodedImageFormat.Bmp, codec.EncodedFormat);

                stream.Position = 0;

                using (SKBitmap image = SKBitmap.Decode(stream))
                {
                    Assert.AreEqual(816, image.Width);
                    Assert.AreEqual(1056, image.Height);
                }
            }
#endif
```

### Ver también

* class [SaveOutputParameters](../../../aspose.words.saving/saveoutputparameters/)
* enum [SaveFormat](../../saveformat/)
* class [Document](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)

---

## Save(*Stream, [SaveOptions](../../../aspose.words.saving/saveoptions/)*) {#save_1}

Guarda el documento en una secuencia utilizando las opciones de guardado especificadas.

```csharp
public SaveOutputParameters Save(Stream stream, SaveOptions saveOptions)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| stream | Stream | Transmite dónde guardar el documento. |
| saveOptions | SaveOptions | Especifica las opciones que controlan cómo se guarda el documento. Puede ser`nulo` . Si esto es`nulo`, el documento se guardará en formato binario DOC. |

### Valor_devuelto

Información adicional que puedes utilizar opcionalmente.

## Ejemplos

Muestra cómo convertir solo algunas de las páginas de un documento a PDF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Page 1.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 2.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 3.");

using (Stream stream = File.Create(ArtifactsDir + "PdfSaveOptions.OnePage.pdf"))
{
    // Crea un objeto "PdfSaveOptions" que podamos pasar al método "Guardar" del documento
    // para modificar la forma en que ese método convierte el documento a .PDF.
    PdfSaveOptions options = new PdfSaveOptions();

    // Establezca "PageIndex" en "1" para representar una parte del documento a partir de la segunda página.
    options.PageSet = new PageSet(1);

    //Este documento contendrá una página a partir de la página dos, que solo contendrá la segunda página.
    doc.Save(stream, options);
}
```

### Ver también

* class [SaveOutputParameters](../../../aspose.words.saving/saveoutputparameters/)
* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [Document](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)

---

## Save(*HttpResponse, string, [ContentDisposition](../../contentdisposition/), [SaveOptions](../../../aspose.words.saving/saveoptions/)*) {#save_5}

Envía el documento al navegador del cliente.

```csharp
public SaveOutputParameters Save(HttpResponse response, string fileName, 
    ContentDisposition contentDisposition, SaveOptions saveOptions)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| response | HttpResponse | Objeto de respuesta donde guardar el documento. |
| fileName | String | El nombre del documento que aparecerá en el navegador del cliente. El nombre no debe contener la ruta. |
| contentDisposition | ContentDisposition | A[`ContentDisposition`](../../contentdisposition/) valor que especifica cómo se presenta el documento en el navegador del cliente. |
| saveOptions | SaveOptions | Especifica las opciones que controlan cómo se guarda el documento. Puede ser`nulo`. |

### Valor_devuelto

Información adicional que puedes utilizar opcionalmente.

## Observaciones

Internamente, este método primero guarda en un flujo de memoria y luego copia en el flujo de respuesta stream porque el flujo de respuesta no admite la búsqueda.

## Ejemplos

Muestra cómo realizar una combinación de correspondencia y luego guardar el documento en el navegador del cliente.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertField(" MERGEFIELD FullName ");
builder.InsertParagraph();
builder.InsertField(" MERGEFIELD Company ");
builder.InsertParagraph();
builder.InsertField(" MERGEFIELD Address ");
builder.InsertParagraph();
builder.InsertField(" MERGEFIELD City ");

doc.MailMerge.Execute(new string[] { "FullName", "Company", "Address", "City" },
    new object[] { "James Bond", "MI5 Headquarters", "Milbank", "London" });

// Envía el documento al navegador del cliente.
//Se lanza porque HttpResponse es nulo en la prueba.
Assert.Throws<ArgumentNullException>(() => doc.Save(response, "Artifacts/MailMerge.ExecuteArray.docx", ContentDisposition.Inline, null));

Necesitaremos cerrar esta respuesta manualmente para asegurarnos de no agregar ningún contenido superfluo al documento después de guardarlo.
Assert.Throws<NullReferenceException>(() => response.End());
```

### Ver también

* class [SaveOutputParameters](../../../aspose.words.saving/saveoutputparameters/)
* enum [ContentDisposition](../../contentdisposition/)
* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [Document](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
