---
title: ViewOptions.DisplayBackgroundShape
linktitle: DisplayBackgroundShape
articleTitle: DisplayBackgroundShape
second_title: Aspose.Words para .NET
description: Descubra la propiedad DisplayBackgroundShape en ViewOptions para mejorar su diseño de impresión con formas de fondo personalizables para una apariencia elegante.
type: docs
weight: 10
url: /es/net/aspose.words.settings/viewoptions/displaybackgroundshape/
---
## ViewOptions.DisplayBackgroundShape property

Controla la visualización de la forma del fondo en la vista de diseño de impresión.

```csharp
public bool DisplayBackgroundShape { get; set; }
```

## Ejemplos

Muestra cómo ocultar/mostrar imágenes de fondo del documento en las opciones de visualización.

```csharp
// Utilice una cadena HTML para crear un nuevo documento con un color de fondo plano.
const string html = 
@"<html>
    <body style='background-color: blue'>
        <p>Hello world!</p>
    </body>
</html>";

Document doc = new Document(new MemoryStream(Encoding.Unicode.GetBytes(html)));

//La fuente del documento tiene un fondo de color plano,
// cuya presencia establecerá el indicador "DisplayBackgroundShape" en "verdadero".
Assert.True(doc.ViewOptions.DisplayBackgroundShape);

// Mantenga "DisplayBackgroundShape" como "verdadero" para que el documento muestre el color de fondo.
// Esto puede afectar algunos colores del texto para mejorar la visibilidad.
// Establezca "DisplayBackgroundShape" en "falso" para no mostrar el color de fondo.
doc.ViewOptions.DisplayBackgroundShape = displayBackgroundShape;

doc.Save(ArtifactsDir + "ViewOptions.DisplayBackgroundShape.docx");
```

### Ver también

* class [ViewOptions](../)
* espacio de nombres [Aspose.Words.Settings](../../../aspose.words.settings/)
* asamblea [Aspose.Words](../../../)
