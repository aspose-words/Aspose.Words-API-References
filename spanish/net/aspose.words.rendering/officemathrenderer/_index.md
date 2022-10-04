---
title: OfficeMathRenderer
second_title: Referencia de API de Aspose.Words para .NET
description: Proporciona métodos para representar a un individuoOfficeMath../aspose.words.math/officemath/ a una imagen rasterizada o vectorial o a un objeto Graphics.
type: docs
weight: 4300
url: /es/net/aspose.words.rendering/officemathrenderer/
---
## OfficeMathRenderer class

Proporciona métodos para representar a un individuo[`OfficeMath`](../../aspose.words.math/officemath/) a una imagen rasterizada o vectorial o a un objeto Graphics.

```csharp
public class OfficeMathRenderer : NodeRendererBase
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [OfficeMathRenderer](officemathrenderer/)(OfficeMath) | Inicializa una nueva instancia de esta clase. |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [BoundsInPoints](../../aspose.words.rendering/noderendererbase/boundsinpoints/) { get; } | Obtiene los límites reales de la forma en puntos. |
| [OpaqueBoundsInPoints](../../aspose.words.rendering/noderendererbase/opaqueboundsinpoints/) { get; } | Obtiene los límites opacos de la forma en puntos. |
| [SizeInPoints](../../aspose.words.rendering/noderendererbase/sizeinpoints/) { get; } | Obtiene el tamaño real de la forma en puntos. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [GetBoundsInPixels](../../aspose.words.rendering/noderendererbase/getboundsinpixels/)(float, float) | Calcula los límites de la forma en píxeles para un factor de zoom y una resolución específicos. |
| [GetBoundsInPixels](../../aspose.words.rendering/noderendererbase/getboundsinpixels/)(float, float, float) | Calcula los límites de la forma en píxeles para un factor de zoom y una resolución específicos. |
| [GetOpaqueBoundsInPixels](../../aspose.words.rendering/noderendererbase/getopaqueboundsinpixels/)(float, float) | Calcula los límites opacos de la forma en píxeles para un factor de zoom y una resolución específicos. |
| [GetOpaqueBoundsInPixels](../../aspose.words.rendering/noderendererbase/getopaqueboundsinpixels/)(float, float, float) | Calcula los límites opacos de la forma en píxeles para un factor de zoom y una resolución específicos. |
| [GetSizeInPixels](../../aspose.words.rendering/noderendererbase/getsizeinpixels/)(float, float) | Calcula el tamaño de la forma en píxeles para un factor de zoom y resolución especificados. |
| [GetSizeInPixels](../../aspose.words.rendering/noderendererbase/getsizeinpixels/)(float, float, float) | Calcula el tamaño de la forma en píxeles para un factor de zoom y resolución especificados. |
| [RenderToScale](../../aspose.words.rendering/noderendererbase/rendertoscale/)(Graphics, float, float, float) | Convierte la forma en unGraphics objeto a una escala especificada. |
| [RenderToSize](../../aspose.words.rendering/noderendererbase/rendertosize/)(Graphics, float, float, float, float) | Convierte la forma en unGraphics objeto a un tamaño especificado. |
| [Save](../../aspose.words.rendering/noderendererbase/save/)(Stream, ImageSaveOptions) | Representa la forma en una imagen y la guarda en una secuencia. |
| [Save](../../aspose.words.rendering/noderendererbase/save/)(string, ImageSaveOptions) | Representa la forma en una imagen y la guarda en un archivo. |

### Ejemplos

Muestra cómo medir y escalar formas.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

OfficeMath officeMath = (OfficeMath)doc.GetChild(NodeType.OfficeMath, 0, true);
OfficeMathRenderer renderer = new OfficeMathRenderer(officeMath);

// Verificar el tamaño de la imagen que creará el objeto OfficeMath cuando lo representemos.
Assert.AreEqual(119.0f, renderer.SizeInPoints.Width, 0.2f);
Assert.AreEqual(13.0f, renderer.SizeInPoints.Height, 0.1f);

Assert.AreEqual(119.0f, renderer.BoundsInPoints.Width, 0.2f);
Assert.AreEqual(13.0f, renderer.BoundsInPoints.Height, 0.1f);

// Las formas con partes transparentes pueden contener diferentes valores en las propiedades "OpaqueBoundsInPoints".
Assert.AreEqual(119.0f, renderer.OpaqueBoundsInPoints.Width, 0.2f);
Assert.AreEqual(14.2f, renderer.OpaqueBoundsInPoints.Height, 0.1f);

// Obtener el tamaño de la forma en píxeles, con escalado lineal a un DPI específico.
Rectangle bounds = renderer.GetBoundsInPixels(1.0f, 96.0f);

Assert.AreEqual(159, bounds.Width);
Assert.AreEqual(18, bounds.Height);

// Obtenga el tamaño de la forma en píxeles, pero con un DPI diferente para las dimensiones horizontal y vertical.
bounds = renderer.GetBoundsInPixels(1.0f, 96.0f, 150.0f);
Assert.AreEqual(159, bounds.Width);
Assert.AreEqual(28, bounds.Height);

// Los límites opacos también pueden variar aquí.
bounds = renderer.GetOpaqueBoundsInPixels(1.0f, 96.0f);

Assert.AreEqual(159, bounds.Width);
Assert.AreEqual(18, bounds.Height);

bounds = renderer.GetOpaqueBoundsInPixels(1.0f, 96.0f, 150.0f);

Assert.AreEqual(159, bounds.Width);
Assert.AreEqual(30, bounds.Height);
```

### Ver también

* class [NodeRendererBase](../noderendererbase/)
* espacio de nombres [Aspose.Words.Rendering](../../aspose.words.rendering/)
* asamblea [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
