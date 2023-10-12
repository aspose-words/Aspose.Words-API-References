---
title: HtmlLoadOptions.HtmlLoadOptions
second_title: Referencia de API de Aspose.Words para .NET
description: HtmlLoadOptions constructor. Inicializa una nueva instancia de esta clase con valores predeterminados.
type: docs
weight: 10
url: /es/net/aspose.words.loading/htmlloadoptions/htmlloadoptions/
---
## HtmlLoadOptions() {#constructor}

Inicializa una nueva instancia de esta clase con valores predeterminados.

```csharp
public HtmlLoadOptions()
```

### Ejemplos

Muestra cómo admitir comentarios condicionales al cargar un documento HTML.

```csharp
HtmlLoadOptions loadOptions = new HtmlLoadOptions();

// Si el valor es verdadero, tomamos en cuenta el código VML al analizar el documento cargado.
loadOptions.SupportVml = supportVml;

// Este documento contiene una imagen JPEG dentro de "<!--[if gte vml 1]>" etiquetas,
// y una imagen PNG diferente dentro de "<![if !vml]>" etiquetas.
// Si configuramos el indicador "SupportVml" en "true", Aspose.Words cargará el JPEG.
// Si configuramos este indicador en "falso", entonces Aspose.Words solo cargará el PNG.
Document doc = new Document(MyDir + "VML conditional.htm", loadOptions);

if (supportVml)
    Assert.AreEqual(ImageType.Jpeg, ((Shape)doc.GetChild(NodeType.Shape, 0, true)).ImageData.ImageType);
else
    Assert.AreEqual(ImageType.Png, ((Shape)doc.GetChild(NodeType.Shape, 0, true)).ImageData.ImageType);
```

### Ver también

* class [HtmlLoadOptions](../)
* espacio de nombres [Aspose.Words.Loading](../../htmlloadoptions/)
* asamblea [Aspose.Words](../../../)

---

## HtmlLoadOptions(string) {#constructor_2}

Un acceso directo para inicializar una nueva instancia de esta clase con la contraseña especificada para cargar un documento cifrado.

```csharp
public HtmlLoadOptions(string password)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| password | String | La contraseña para abrir un documento cifrado. Puede ser`nulo` o cadena vacía. |

### Ejemplos

Muestra cómo cifrar un documento HTML y luego abrirlo usando una contraseña.

```csharp
// Crea y firma un documento HTML cifrado a partir de un .docx cifrado.
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
// contraseña usando un objeto HtmlLoadOptions.
HtmlLoadOptions loadOptions = new HtmlLoadOptions("docPassword");

Assert.AreEqual(signOptions.DecryptionPassword, loadOptions.Password);

Document doc = new Document(outputFileName, loadOptions);

Assert.AreEqual("Test encrypted document.", doc.GetText().Trim());
```

### Ver también

* class [HtmlLoadOptions](../)
* espacio de nombres [Aspose.Words.Loading](../../htmlloadoptions/)
* asamblea [Aspose.Words](../../../)

---

## HtmlLoadOptions(LoadFormat, string, string) {#constructor_1}

Un acceso directo para inicializar una nueva instancia de esta clase con propiedades establecidas en los valores especificados.

```csharp
public HtmlLoadOptions(LoadFormat loadFormat, string password, string baseUri)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| loadFormat | LoadFormat | El formato del documento que se va a cargar. |
| password | String | La contraseña para abrir un documento cifrado. Puede ser`nulo` o cadena vacía. |
| baseUri | String | La cadena que se utilizará para resolver los URI relativos a absolutos. Puede ser`nulo` o cadena vacía. |

### Ejemplos

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
* class [HtmlLoadOptions](../)
* espacio de nombres [Aspose.Words.Loading](../../htmlloadoptions/)
* asamblea [Aspose.Words](../../../)


