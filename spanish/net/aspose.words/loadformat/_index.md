---
title: LoadFormat Enum
linktitle: LoadFormat
articleTitle: LoadFormat
second_title: Aspose.Words para .NET
description: Descubra la enumeración Aspose.Words.LoadFormat, que define formatos de documentos para una carga perfecta y una compatibilidad mejorada en sus aplicaciones.
type: docs
weight: 4000
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
| Auto | `0` | Indica a Aspose.Words que reconozca el formato automáticamente. |
| MsWorks | `8` | Documento de Microsoft Works 8. |
| Doc | `10` | Documento de Microsoft Word 95 o Word 97 - 2003. |
| Dot | `11` | Plantilla de Microsoft Word 95 o Word 97 - 2003. |
| DocPreWord60 | `12` | El documento está en formato anterior a Word 95. Aspose.Words actualmente no admite la carga de dichos documentos. |
| Docx | `20` | Documento WordprocessingML de Office Open XML (sin macros). |
| Docm | `21` | Documento con macros habilitadas para WordprocessingML de Office Open XML. |
| Dotx | `22` | Plantilla WordprocessingML de Office Open XML (sin macros). |
| Dotm | `23` | Plantilla habilitada para macros de Office Open XML WordprocessingML. |
| FlatOpc | `24` | Office Open XML WordprocessingML se almacena en un archivo XML plano en lugar de un paquete ZIP. |
| FlatOpcMacroEnabled | `25` | Documento habilitado para macros de Office Open XML WordprocessingML almacenado en un archivo XML plano en lugar de un paquete ZIP. |
| FlatOpcTemplate | `26` | Plantilla WordprocessingML de Office Open XML (sin macros) almacenada en un archivo XML plano en lugar de un paquete ZIP. |
| FlatOpcTemplateMacroEnabled | `27` | Plantilla habilitada para macros de Office Open XML WordprocessingML almacenada en un archivo XML plano en lugar de un paquete ZIP. |
| Rtf | `30` | Formato RTF. |
| WordML | `31` | Formato WordprocessingML de Microsoft Word 2003. |
| Html | `50` | Formato HTML. |
| Mhtml | `51` | Formato MHTML (archivo web). |
| Mobi | `52` | Formato MOBI. Utilizado por los lectores MobiPocket y Amazon Kindle. |
| Chm | `53` | Formato CHM (Ayuda HTML compilada). |
| Azw3 | `54` | Formato AZW3. Usado por lectores Kindle de Amazon. |
| Epub | `55` | Formato EPUB. |
| Odt | `60` | Documento de texto ODF. |
| Ott | `61` | Plantilla de documento de texto ODF. |
| Text | `62` | Texto sin formato. |
| Markdown | `63` | Documento de texto Markdown. |
| Pdf | `64` | Documento PDF. |
| Xml | `65` | Documento XML. |
| Unknown | `255` | Formato no reconocido, no puede ser cargado por Aspose.Words. |

## Ejemplos

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

Muestra cómo especificar una URI base al abrir un documento html.

```csharp
// Supongamos que queremos cargar un documento .html que contiene una imagen vinculada por una URI relativa
// mientras la imagen esté en una ubicación diferente. En ese caso, necesitaremos convertir la URI relativa en una absoluta.
 // Podemos proporcionar una URI base utilizando un objeto HtmlLoadOptions.
HtmlLoadOptions loadOptions = new HtmlLoadOptions(LoadFormat.Html, "", ImageDir);

Assert.AreEqual(LoadFormat.Html, loadOptions.LoadFormat);

Document doc = new Document(MyDir + "Missing image.html", loadOptions);

// Aunque la imagen estaba rota en el .html de entrada, nuestra URI base personalizada nos ayudó a reparar el enlace.
Shape imageShape = (Shape)doc.GetChildNodes(NodeType.Shape, true)[0];
Assert.True(imageShape.IsImage);

//Este documento de salida mostrará la imagen que faltaba.
doc.Save(ArtifactsDir + "HtmlLoadOptions.BaseUri.docx");
```

Muestra cómo utilizar los métodos FileFormatUtil para detectar el formato de un documento.

```csharp
// Cargue un documento desde un archivo al que le falta una extensión de archivo y luego detecte su formato de archivo.
using (FileStream docStream = File.OpenRead(MyDir + "Word document with missing file extension"))
{
    FileFormatInfo info = FileFormatUtil.DetectFileFormat(docStream);
    LoadFormat loadFormat = info.LoadFormat;

    Assert.AreEqual(LoadFormat.Doc, loadFormat);

    // A continuación se muestran dos métodos para convertir un LoadFormat a su SaveFormat correspondiente.
    // 1 - Obtenga la cadena de extensión de archivo para LoadFormat, luego obtenga el SaveFormat correspondiente de esa cadena:
    string fileExtension = FileFormatUtil.LoadFormatToExtension(loadFormat);
    SaveFormat saveFormat = FileFormatUtil.ExtensionToSaveFormat(fileExtension);

    // 2 - Convierte el LoadFormat directamente a su SaveFormat:
    saveFormat = FileFormatUtil.LoadFormatToSaveFormat(loadFormat);

    // Cargue un documento desde la secuencia y luego guárdelo en la extensión de archivo detectada automáticamente.
    Document doc = new Document(docStream);

    Assert.AreEqual(".doc", FileFormatUtil.SaveFormatToExtension(saveFormat));

    doc.Save(ArtifactsDir + "File.SaveToDetectedFileFormat" + FileFormatUtil.SaveFormatToExtension(saveFormat));
}
```

### Ver también

* espacio de nombres [Aspose.Words](../../aspose.words/)
* asamblea [Aspose.Words](../../)
