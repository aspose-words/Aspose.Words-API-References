---
title: LoadOptions.LoadFormat
linktitle: LoadFormat
articleTitle: LoadFormat
second_title: Aspose.Words para .NET
description: LoadOptions LoadFormat propiedad. Especifica el formato del documento que se cargará. El valor predeterminado esAuto  en C#.
type: docs
weight: 90
url: /es/net/aspose.words.loading/loadoptions/loadformat/
---
## LoadOptions.LoadFormat property

Especifica el formato del documento que se cargará. El valor predeterminado esAuto .

```csharp
public LoadFormat LoadFormat { get; set; }
```

## Observaciones

Se recomienda especificar elAuto value y permita que Aspose.Words detecte el formato del archivo automáticamente. Si conoce el formato del documento que está a punto de cargar, puede especificar format explícitamente y esto reducirá ligeramente el tiempo de carga debido a la sobrecarga asociada con la detección automática del formato. Si especifica un formato de carga explícito, se activará Si resulta incorrecto, se invocará la detección automática y se realizará un segundo intento de cargar el archivo.

## Ejemplos

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
* espacio de nombres [Aspose.Words.Loading](../../../aspose.words.loading/)
* asamblea [Aspose.Words](../../../)
