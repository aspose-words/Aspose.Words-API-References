---
title: HtmlLoadOptions
linktitle: HtmlLoadOptions
articleTitle: HtmlLoadOptions
second_title: Aspose.Words para .NET
description: Descubra el constructor HtmlLoadOptions, diseñado para inicializar sin esfuerzo instancias con configuraciones predeterminadas para un desarrollo web perfecto.
type: docs
weight: 10
url: /es/net/aspose.words.loading/htmlloadoptions/htmlloadoptions/
---
## HtmlLoadOptions() {#constructor}

Inicializa una nueva instancia de esta clase con valores predeterminados.

```csharp
public HtmlLoadOptions()
```

## Ejemplos

Muestra cómo admitir comentarios condicionales al cargar un documento HTML.

```csharp
HtmlLoadOptions loadOptions = new HtmlLoadOptions();

// Si el valor es verdadero, tomamos en cuenta el código VML al analizar el documento cargado.
loadOptions.SupportVml = supportVml;

// Este documento contiene una imagen JPEG dentro de las etiquetas "<!--[if gte vml 1]>",
// y una imagen PNG diferente dentro de las etiquetas "<![if !vml]>".
// Si establecemos el indicador "SupportVml" en "verdadero", entonces Aspose.Words cargará el JPEG.
// Si establecemos esta bandera como "falso", entonces Aspose.Words solo cargará el PNG.
Document doc = new Document(MyDir + "VML conditional.htm", loadOptions);

if (supportVml)
    Assert.AreEqual(ImageType.Jpeg, ((Shape)doc.GetChild(NodeType.Shape, 0, true)).ImageData.ImageType);
else
    Assert.AreEqual(ImageType.Png, ((Shape)doc.GetChild(NodeType.Shape, 0, true)).ImageData.ImageType);
```

### Ver también

* class [HtmlLoadOptions](../)
* espacio de nombres [Aspose.Words.Loading](../../../aspose.words.loading/)
* asamblea [Aspose.Words](../../../)

---

## HtmlLoadOptions(*string*) {#constructor_2}

Un acceso directo para inicializar una nueva instancia de esta clase con la contraseña especificada para cargar un documento cifrado.

```csharp
public HtmlLoadOptions(string password)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| password | String | La contraseña para abrir un documento cifrado. Puede ser`nulo` o cadena vacía. |

## Ejemplos

Muestra cómo cifrar un documento HTML y luego abrirlo usando una contraseña.

```csharp
// Cree y firme un documento HTML cifrado a partir de un .docx cifrado.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");

SignOptions signOptions = new SignOptions
{
    Comments = "Comment",
    SignTime = DateTime.Now,
    DecryptionPassword = "docPassword"
};

string inputFileName = MyDir + "Encrypted.docx";
string outputFileName = ArtifactsDir + "HtmlLoadOptions.EncryptedHtml.html";
DigitalSignatureUtil.Sign(inputFileName, outputFileName, certificateHolder, signOptions);

// Para cargar y leer este documento, necesitaremos pasar su descifrado
// contraseña utilizando un objeto HtmlLoadOptions.
HtmlLoadOptions loadOptions = new HtmlLoadOptions("docPassword");

Assert.AreEqual(signOptions.DecryptionPassword, loadOptions.Password);

Document doc = new Document(outputFileName, loadOptions);

Assert.AreEqual("Test encrypted document.", doc.GetText().Trim());
```

### Ver también

* class [HtmlLoadOptions](../)
* espacio de nombres [Aspose.Words.Loading](../../../aspose.words.loading/)
* asamblea [Aspose.Words](../../../)

---

## HtmlLoadOptions(*[LoadFormat](../../../aspose.words/loadformat/), string, string*) {#constructor_1}

Un acceso directo para inicializar una nueva instancia de esta clase con propiedades establecidas en los valores especificados.

```csharp
public HtmlLoadOptions(LoadFormat loadFormat, string password, string baseUri)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| loadFormat | LoadFormat | El formato del documento que se va a cargar. |
| password | String | La contraseña para abrir un documento cifrado. Puede ser`nulo` o cadena vacía. |
| baseUri | String | La cadena que se usará para convertir las URI relativas en absolutas. Puede ser`nulo` o cadena vacía. |

## Ejemplos

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
* class [HtmlLoadOptions](../)
* espacio de nombres [Aspose.Words.Loading](../../../aspose.words.loading/)
* asamblea [Aspose.Words](../../../)
