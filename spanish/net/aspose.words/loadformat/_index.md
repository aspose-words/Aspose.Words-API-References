---
title: LoadFormat
second_title: Referencia de API de Aspose.Words para .NET
description: Indica el formato del documento que se va a cargar.
type: docs
weight: 3350
url: /es/net/aspose.words/loadformat/
---
## LoadFormat enumeration

Indica el formato del documento que se va a cargar.

```csharp
public enum LoadFormat
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Auto | `0` | Le indica a Aspose.Words que reconozca el formato automáticamente. |
| Doc | `10` | Documento de Microsoft Word 95 o Word 97 - 2003. |
| Dot | `11` | Plantilla de Microsoft Word 95 o Word 97 - 2003. |
| DocPreWord60 | `12` | El documento está en formato anterior a Word 95. Aspose.Words actualmente no admite la carga de dichos documentos. |
| Docx | `20` | Documento Office Open XML WordprocessingML (sin macros). |
| Docm | `21` | Documento de Office Open XML WordprocessingML habilitado para macros. |
| Dotx | `22` | Plantilla Office Open XML WordprocessingML (sin macros). |
| Dotm | `23` | Plantilla de Office Open XML WordprocessingML habilitada para macros. |
| FlatOpc | `24` | Office Open XML WordprocessingML almacenado en un archivo XML sin formato en lugar de un paquete ZIP. |
| FlatOpcMacroEnabled | `25` | Documento Office Open XML WordprocessingML habilitado para macros almacenado en un archivo XML sin formato en lugar de un paquete ZIP. |
| FlatOpcTemplate | `26` | Plantilla Office Open XML WordprocessingML (sin macros) almacenada en un archivo XML sin formato en lugar de un paquete ZIP. |
| FlatOpcTemplateMacroEnabled | `27` | Plantilla de Office Open XML WordprocessingML habilitada para macros almacenada en un archivo XML sin formato en lugar de un paquete ZIP. |
| Rtf | `30` | Formato RTF. |
| WordML | `31` | formato Microsoft Word 2003 WordprocessingML. |
| Html | `50` | formato HTML. |
| Mhtml | `51` | formato MHTML (archivo web). |
| Mobi | `52` | Formato MOBI. Utilizado por el lector MobiPocket y los lectores Kindle de Amazon. |
| Chm | `53` | Formato CHM (Ayuda HTML compilada). |
| Azw3 | `54` | Formato AZW3. Usado por los lectores Kindle de Amazon. |
| Epub | `55` | Formato EPUB. |
| Odt | `60` | Documento de texto ODF. |
| Ott | `61` | Plantilla de documento de texto ODF. |
| Text | `62` | Texto sin formato. |
| Markdown | `63` | Documento de texto Markdown. |
| Pdf | `64` | Documento pdf. |
| Xml | `65` | Documento XML. |
| Unknown | `255` | Formato no reconocido, Aspose.Words no lo puede cargar. |

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

Muestra cómo especificar un URI base al abrir un documento html.

```csharp
// Supongamos que queremos cargar un documento .html que contiene una imagen enlazada por una URI relativa
// mientras la imagen está en una ubicación diferente. En ese caso, necesitaremos convertir el URI relativo en uno absoluto.
  // Podemos proporcionar un URI base usando un objeto HtmlLoadOptions.
HtmlLoadOptions loadOptions = new HtmlLoadOptions(LoadFormat.Html, "", ImageDir);

Assert.AreEqual(LoadFormat.Html, loadOptions.LoadFormat);

Document doc = new Document(MyDir + "Missing image.html", loadOptions);

// Si bien la imagen se rompió en el .html de entrada, nuestro URI base personalizado nos ayudó a reparar el enlace.
Shape imageShape = (Shape)doc.GetChildNodes(NodeType.Shape, true)[0];
Assert.True(imageShape.IsImage);

// Este documento de salida mostrará la imagen que faltaba.
doc.Save(ArtifactsDir + "HtmlLoadOptions.BaseUri.docx");
```

Muestra cómo usar los métodos FileFormatUtil para detectar el formato de un documento.

```csharp
// Cargue un documento de un archivo al que le falta una extensión de archivo y luego detecte su formato de archivo.
using (FileStream docStream = File.OpenRead(MyDir + "Word document with missing file extension"))
{
    FileFormatInfo info = FileFormatUtil.DetectFileFormat(docStream);
    LoadFormat loadFormat = info.LoadFormat;

    Assert.AreEqual(LoadFormat.Doc, loadFormat);

    // A continuación se muestran dos métodos para convertir un LoadFormat a su SaveFormat correspondiente.
    // 1 - Obtenga la cadena de extensión de archivo para LoadFormat, luego obtenga el SaveFormat correspondiente de esa cadena:
    string fileExtension = FileFormatUtil.LoadFormatToExtension(loadFormat);
    SaveFormat saveFormat = FileFormatUtil.ExtensionToSaveFormat(fileExtension);

    // 2 - Convertir el LoadFormat directamente a su SaveFormat:
    saveFormat = FileFormatUtil.LoadFormatToSaveFormat(loadFormat);

    // Cargue un documento de la secuencia y luego guárdelo en la extensión de archivo detectada automáticamente.
    Document doc = new Document(docStream);

    Assert.AreEqual(".doc", FileFormatUtil.SaveFormatToExtension(saveFormat));

    doc.Save(ArtifactsDir + "File.SaveToDetectedFileFormat" + FileFormatUtil.SaveFormatToExtension(saveFormat));
}
```

### Ver también

* espacio de nombres [Aspose.Words](../../aspose.words/)
* asamblea [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
