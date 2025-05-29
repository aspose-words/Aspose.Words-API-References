---
title: LoadOptions.LoadFormat
linktitle: LoadFormat
articleTitle: LoadFormat
second_title: Aspose.Words para .NET
description: Descubra la propiedad LoadOptions LoadFormat para especificar fácilmente los formatos de documento. Optimice la carga con la configuración automática predeterminada para un rendimiento óptimo.
type: docs
weight: 90
url: /es/net/aspose.words.loading/loadoptions/loadformat/
---
## LoadOptions.LoadFormat property

Especifica el formato del documento que se va a cargar. El valor predeterminado esAuto .

```csharp
public LoadFormat LoadFormat { get; set; }
```

## Observaciones

Se recomienda que especifique elAuto Valor y permite que Aspose.Words detecte automáticamente el formato del archivo. Si conoce el formato del documento que va a cargar, puede especificar el formato explícitamente, lo que reducirá ligeramente el tiempo de carga debido a la sobrecarga asociada con la detección automática del formato. Si especifica un formato de carga explícito y resulta ser incorrecto, se invocará la detección automática y se realizará un segundo intento de carga.

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
* class [LoadOptions](../)
* espacio de nombres [Aspose.Words.Loading](../../../aspose.words.loading/)
* asamblea [Aspose.Words](../../../)
