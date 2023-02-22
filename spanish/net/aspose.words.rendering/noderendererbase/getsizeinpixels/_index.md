---
title: NodeRendererBase.GetSizeInPixels
second_title: Referencia de API de Aspose.Words para .NET
description: NodeRendererBase método. Calcula el tamaño de la forma en píxeles para un factor de zoom y resolución especificados.
type: docs
weight: 60
url: /es/net/aspose.words.rendering/noderendererbase/getsizeinpixels/
---
## GetSizeInPixels(float, float) {#getsizeinpixels}

Calcula el tamaño de la forma en píxeles para un factor de zoom y resolución especificados.

```csharp
public Size GetSizeInPixels(float scale, float dpi)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| scale | Single | El factor de zoom (1.0 es 100%). |
| dpi | Single | La resolución (horizontal y vertical) para convertir de puntos a píxeles (puntos por pulgada). |

### Valor_devuelto

El tamaño de la forma en píxeles.

### Observaciones

Este método convierte[`SizeInPoints`](../sizeinpoints/) en tamaño en píxeles y es útil cuando desea crear un mapa de bits para representar la forma de forma ordenada en el mapa de bits.

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

* class [NodeRendererBase](../)
* espacio de nombres [Aspose.Words.Rendering](../../noderendererbase/)
* asamblea [Aspose.Words](../../../)

---

## GetSizeInPixels(float, float, float) {#getsizeinpixels_1}

Calcula el tamaño de la forma en píxeles para un factor de zoom y resolución especificados.

```csharp
public Size GetSizeInPixels(float scale, float horizontalDpi, float verticalDpi)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| scale | Single | El factor de zoom (1.0 es 100%). |
| horizontalDpi | Single | La resolución horizontal para convertir de puntos a píxeles (puntos por pulgada). |
| verticalDpi | Single | La resolución vertical para convertir de puntos a píxeles (puntos por pulgada). |

### Valor_devuelto

El tamaño de la forma en píxeles.

### Observaciones

Este método convierte[`SizeInPoints`](../sizeinpoints/) en tamaño en píxeles y es útil cuando desea crear un mapa de bits para representar la forma de forma ordenada en el mapa de bits.

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

* class [NodeRendererBase](../)
* espacio de nombres [Aspose.Words.Rendering](../../noderendererbase/)
* asamblea [Aspose.Words](../../../)


