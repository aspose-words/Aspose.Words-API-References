---
title: LoadOptions.LoadOptions
second_title: Referencia de API de Aspose.Words para .NET
description: LoadOptions constructor. Inicializa una nueva instancia de esta clase con valores predeterminados.
type: docs
weight: 10
url: /es/net/aspose.words.loading/loadoptions/loadoptions/
---
## LoadOptions() {#constructor}

Inicializa una nueva instancia de esta clase con valores predeterminados.

```csharp
public LoadOptions()
```

### Ejemplos

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

### Ver también

* class [LoadOptions](../)
* espacio de nombres [Aspose.Words.Loading](../../loadoptions/)
* asamblea [Aspose.Words](../../../)

---

## LoadOptions(string) {#constructor_2}

Un acceso directo para inicializar una nueva instancia de esta clase con la contraseña especificada para cargar un documento cifrado.

```csharp
public LoadOptions(string password)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| password | String | La contraseña para abrir un documento cifrado. Puede ser`nulo` o cadena vacía. |

### Ejemplos

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

* class [LoadOptions](../)
* espacio de nombres [Aspose.Words.Loading](../../loadoptions/)
* asamblea [Aspose.Words](../../../)

---

## LoadOptions(LoadFormat, string, string) {#constructor_1}

Un acceso directo para inicializar una nueva instancia de esta clase con propiedades establecidas en los valores especificados.

```csharp
public LoadOptions(LoadFormat loadFormat, string password, string baseUri)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| loadFormat | LoadFormat | El formato del documento que se va a cargar. |
| password | String | La contraseña para abrir un documento cifrado. Puede ser`nulo` o cadena vacía. |
| baseUri | String | La cadena que se utilizará para resolver los URI relativos a absolutos. Puede ser`nulo` o cadena vacía. |

### Ejemplos

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

Muestra cómo especificar un URI base al abrir un documento html.

```csharp
// Supongamos que queremos cargar un documento .html que contiene una imagen vinculada por un URI relativo
// mientras la imagen está en una ubicación diferente. En ese caso, necesitaremos resolver el URI relativo en uno absoluto.
 // Podemos proporcionar un URI base usando un objeto HtmlLoadOptions.
HtmlLoadOptions loadOptions = new HtmlLoadOptions(LoadFormat.Html, "", ImageDir);

Assert.AreEqual(LoadFormat.Html, loadOptions.LoadFormat);

Document doc = new Document(MyDir + "Missing image.html", loadOptions);

// Si bien la imagen estaba rota en el .html de entrada, nuestro URI base personalizado nos ayudó a reparar el enlace.
Shape imageShape = (Shape)doc.GetChildNodes(NodeType.Shape, true)[0];
Assert.True(imageShape.IsImage);

// Este documento de salida mostrará la imagen que faltaba.
doc.Save(ArtifactsDir + "HtmlLoadOptions.BaseUri.docx");
```

### Ver también

* enum [LoadFormat](../../../aspose.words/loadformat/)
* class [LoadOptions](../)
* espacio de nombres [Aspose.Words.Loading](../../loadoptions/)
* asamblea [Aspose.Words](../../../)


