---
title: LoadOptions
linktitle: LoadOptions
articleTitle: LoadOptions
second_title: Aspose.Words para .NET
description: Descubra el constructor LoadOptions, diseñado para inicializar sin esfuerzo una nueva instancia con valores predeterminados para un rendimiento y una eficiencia óptimos.
type: docs
weight: 10
url: /es/net/aspose.words.loading/loadoptions/loadoptions/
---
## LoadOptions() {#constructor}

Inicializa una nueva instancia de esta clase con valores predeterminados.

```csharp
public LoadOptions()
```

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

### Ver también

* class [LoadOptions](../)
* espacio de nombres [Aspose.Words.Loading](../../../aspose.words.loading/)
* asamblea [Aspose.Words](../../../)

---

## LoadOptions(*string*) {#constructor_2}

Un acceso directo para inicializar una nueva instancia de esta clase con la contraseña especificada para cargar un documento cifrado.

```csharp
public LoadOptions(string password)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| password | String | La contraseña para abrir un documento cifrado. Puede ser`nulo` o cadena vacía. |

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

### Ver también

* class [LoadOptions](../)
* espacio de nombres [Aspose.Words.Loading](../../../aspose.words.loading/)
* asamblea [Aspose.Words](../../../)

---

## LoadOptions(*[LoadFormat](../../../aspose.words/loadformat/), string, string*) {#constructor_1}

Un acceso directo para inicializar una nueva instancia de esta clase con propiedades establecidas en los valores especificados.

```csharp
public LoadOptions(LoadFormat loadFormat, string password, string baseUri)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| loadFormat | LoadFormat | El formato del documento que se va a cargar. |
| password | String | La contraseña para abrir un documento cifrado. Puede ser`nulo` o cadena vacía. |
| baseUri | String | La cadena que se usará para convertir las URI relativas en absolutas. Puede ser`nulo` o cadena vacía. |

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

### Ver también

* enum [LoadFormat](../../../aspose.words/loadformat/)
* class [LoadOptions](../)
* espacio de nombres [Aspose.Words.Loading](../../../aspose.words.loading/)
* asamblea [Aspose.Words](../../../)
