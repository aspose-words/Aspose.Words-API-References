---
title: ShadowFormat Class
linktitle: ShadowFormat
articleTitle: ShadowFormat
second_title: Aspose.Words para .NET
description: Descubra Aspose.Words.Drawing.ShadowFormat para mejorar los efectos de sombra de objetos. Mejore el diseño de sus documentos con opciones personalizables de formato de sombra.
type: docs
weight: 1620
url: /es/net/aspose.words.drawing/shadowformat/
---
## ShadowFormat class

Representa el formato de sombra para un objeto.

Para obtener más información, visite el[Trabajar con elementos gráficos](https://docs.aspose.com/words/net/working-with-graphic-elements/) Artículo de documentación.

```csharp
public class ShadowFormat
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [Color](../../aspose.words.drawing/shadowformat/color/) { get; } | Obtiene unColor objeto que representa el color de la sombra. El valor predeterminado esBlack . |
| [Type](../../aspose.words.drawing/shadowformat/type/) { get; set; } | Obtiene o establece el valor especificado[`ShadowType`](../shadowtype/) para ShadowFormat. |
| [Visible](../../aspose.words.drawing/shadowformat/visible/) { get; } | Devuelve`verdadero` si el formato aplicado a esta instancia es visible. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [Clear](../../aspose.words.drawing/shadowformat/clear/)() | Borra el formato de la sombra. |

## Ejemplos

Muestra cómo obtener el color de la sombra.

```csharp
Document doc = new Document(MyDir + "Shadow color.docx");
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
ShadowFormat shadowFormat = shape.ShadowFormat;

Assert.AreEqual(Color.Red.ToArgb(), shadowFormat.Color.ToArgb());
Assert.AreEqual(ShadowType.ShadowMixed, shadowFormat.Type);
```

### Ver también

* espacio de nombres [Aspose.Words.Drawing](../../aspose.words.drawing/)
* asamblea [Aspose.Words](../../)
