---
title: NodeRendererBase.GetBoundsInPixels
linktitle: GetBoundsInPixels
articleTitle: GetBoundsInPixels
second_title: Aspose.Words para .NET
description: Descubra el método NodeRendererBase GetBoundsInPixels para calcular con precisión las dimensiones de la forma en píxeles según el zoom y la resolución para una mayor precisión.
type: docs
weight: 40
url: /es/net/aspose.words.rendering/noderendererbase/getboundsinpixels/
---
## GetBoundsInPixels(*float, float*) {#getboundsinpixels}

Calcula los límites de la forma en píxeles para un factor de zoom y una resolución especificados.

```csharp
public Rectangle GetBoundsInPixels(float scale, float dpi)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| scale | Single | El factor de zoom (1.0 es 100%). |
| dpi | Single | La resolución (horizontal y vertical) para convertir de puntos a píxeles (puntos por pulgada). |

### Valor_devuelto

El cuadro delimitador real (tal como se muestra en la página) de la forma en píxeles.

## Observaciones

Este método convierte[`BoundsInPoints`](../boundsinpoints/) en rectángulo en píxeles.

## Ejemplos

Muestra cómo medir y escalar formas.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

OfficeMath officeMath = (OfficeMath)doc.GetChild(NodeType.OfficeMath, 0, true);
OfficeMathRenderer renderer = new OfficeMathRenderer(officeMath);

// Verificar el tamaño de la imagen que el objeto OfficeMath creará cuando lo rendericemos.
Assert.AreEqual(122.0f, renderer.SizeInPoints.Width, 0.25f);
Assert.AreEqual(13.0f, renderer.SizeInPoints.Height, 0.15f);

Assert.AreEqual(122.0f, renderer.BoundsInPoints.Width, 0.25f);
Assert.AreEqual(13.0f, renderer.BoundsInPoints.Height, 0.15f);

// Las formas con partes transparentes pueden contener valores diferentes en las propiedades "OpaqueBoundsInPoints".
Assert.AreEqual(122.0f, renderer.OpaqueBoundsInPoints.Width, 0.25f);
Assert.AreEqual(14.2f, renderer.OpaqueBoundsInPoints.Height, 0.1f);

// Obtenga el tamaño de la forma en píxeles, con escala lineal a un DPI específico.
Rectangle bounds = renderer.GetBoundsInPixels(1.0f, 96.0f);

Assert.AreEqual(163, bounds.Width);
Assert.AreEqual(18, bounds.Height);

// Obtenga el tamaño de la forma en píxeles, pero con un DPI diferente para las dimensiones horizontales y verticales.
bounds = renderer.GetBoundsInPixels(1.0f, 96.0f, 150.0f);
Assert.AreEqual(163, bounds.Width);
Assert.AreEqual(27, bounds.Height);

// Los límites opacos también pueden variar aquí.
bounds = renderer.GetOpaqueBoundsInPixels(1.0f, 96.0f);

Assert.AreEqual(163, bounds.Width);
Assert.AreEqual(19, bounds.Height);

bounds = renderer.GetOpaqueBoundsInPixels(1.0f, 96.0f, 150.0f);

Assert.AreEqual(163, bounds.Width);
Assert.AreEqual(29, bounds.Height);
```

### Ver también

* class [NodeRendererBase](../)
* espacio de nombres [Aspose.Words.Rendering](../../../aspose.words.rendering/)
* asamblea [Aspose.Words](../../../)

---

## GetBoundsInPixels(*float, float, float*) {#getboundsinpixels_1}

Calcula los límites de la forma en píxeles para un factor de zoom y una resolución especificados.

```csharp
public Rectangle GetBoundsInPixels(float scale, float horizontalDpi, float verticalDpi)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| scale | Single | El factor de zoom (1.0 es 100%). |
| horizontalDpi | Single | La resolución horizontal para convertir de puntos a píxeles (puntos por pulgada). |
| verticalDpi | Single | La resolución vertical para convertir de puntos a píxeles (puntos por pulgada). |

### Valor_devuelto

El cuadro delimitador real (tal como se muestra en la página) de la forma en píxeles.

## Observaciones

Este método convierte[`BoundsInPoints`](../boundsinpoints/) en rectángulo en píxeles.

## Ejemplos

Muestra cómo medir y escalar formas.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

OfficeMath officeMath = (OfficeMath)doc.GetChild(NodeType.OfficeMath, 0, true);
OfficeMathRenderer renderer = new OfficeMathRenderer(officeMath);

// Verificar el tamaño de la imagen que el objeto OfficeMath creará cuando lo rendericemos.
Assert.AreEqual(122.0f, renderer.SizeInPoints.Width, 0.25f);
Assert.AreEqual(13.0f, renderer.SizeInPoints.Height, 0.15f);

Assert.AreEqual(122.0f, renderer.BoundsInPoints.Width, 0.25f);
Assert.AreEqual(13.0f, renderer.BoundsInPoints.Height, 0.15f);

// Las formas con partes transparentes pueden contener valores diferentes en las propiedades "OpaqueBoundsInPoints".
Assert.AreEqual(122.0f, renderer.OpaqueBoundsInPoints.Width, 0.25f);
Assert.AreEqual(14.2f, renderer.OpaqueBoundsInPoints.Height, 0.1f);

// Obtenga el tamaño de la forma en píxeles, con escala lineal a un DPI específico.
Rectangle bounds = renderer.GetBoundsInPixels(1.0f, 96.0f);

Assert.AreEqual(163, bounds.Width);
Assert.AreEqual(18, bounds.Height);

// Obtenga el tamaño de la forma en píxeles, pero con un DPI diferente para las dimensiones horizontales y verticales.
bounds = renderer.GetBoundsInPixels(1.0f, 96.0f, 150.0f);
Assert.AreEqual(163, bounds.Width);
Assert.AreEqual(27, bounds.Height);

// Los límites opacos también pueden variar aquí.
bounds = renderer.GetOpaqueBoundsInPixels(1.0f, 96.0f);

Assert.AreEqual(163, bounds.Width);
Assert.AreEqual(19, bounds.Height);

bounds = renderer.GetOpaqueBoundsInPixels(1.0f, 96.0f, 150.0f);

Assert.AreEqual(163, bounds.Width);
Assert.AreEqual(29, bounds.Height);
```

### Ver también

* class [NodeRendererBase](../)
* espacio de nombres [Aspose.Words.Rendering](../../../aspose.words.rendering/)
* asamblea [Aspose.Words](../../../)
