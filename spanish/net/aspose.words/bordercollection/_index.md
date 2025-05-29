---
title: BorderCollection Class
linktitle: BorderCollection
articleTitle: BorderCollection
second_title: Aspose.Words para .NET
description: Explore Aspose.Words.BorderCollection, su solución ideal para administrar y personalizar objetos Border sin esfuerzo para un mejor formato de documentos.
type: docs
weight: 280
url: /es/net/aspose.words/bordercollection/
---
## BorderCollection class

Una colección de[`Border`](../border/) objetos.

Para obtener más información, visite el[Programación con documentos](https://docs.aspose.com/words/net/programming-with-documents/) Artículo de documentación.

```csharp
public sealed class BorderCollection : IEnumerable<Border>
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [Bottom](../../aspose.words/bordercollection/bottom/) { get; } | Obtiene el borde inferior. |
| [Color](../../aspose.words/bordercollection/color/) { get; set; } | Obtiene o establece el color del borde. |
| [Count](../../aspose.words/bordercollection/count/) { get; } | Obtiene el número de bordes en la colección. |
| [DistanceFromText](../../aspose.words/bordercollection/distancefromtext/) { get; set; } | Obtiene o establece la distancia del borde desde el texto en puntos. |
| [Horizontal](../../aspose.words/bordercollection/horizontal/) { get; } | Obtiene el borde horizontal que se utiliza entre celdas o párrafos conformes. |
| [Item](../../aspose.words/bordercollection/item/) { get; } | Recupera una[`Border`](../border/) objeto por tipo de borde. (2 indexers) |
| [Left](../../aspose.words/bordercollection/left/) { get; } | Obtiene el borde izquierdo. |
| [LineStyle](../../aspose.words/bordercollection/linestyle/) { get; set; } | Obtiene o establece el estilo del borde. |
| [LineWidth](../../aspose.words/bordercollection/linewidth/) { get; set; } | Obtiene o establece el ancho del borde en puntos. |
| [Right](../../aspose.words/bordercollection/right/) { get; } | Obtiene el borde derecho. |
| [Shadow](../../aspose.words/bordercollection/shadow/) { get; set; } | Obtiene o establece un valor que indica si el borde tiene sombra. |
| [Top](../../aspose.words/bordercollection/top/) { get; } | Obtiene el borde superior. |
| [Vertical](../../aspose.words/bordercollection/vertical/) { get; } | Obtiene el borde vertical que se utiliza entre celdas. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [ClearFormatting](../../aspose.words/bordercollection/clearformatting/)() | Elimina todos los bordes de un objeto. |
| [Equals](../../aspose.words/bordercollection/equals/#equals)(*BorderCollection*) | Compara colecciones de bordes. |
| [GetEnumerator](../../aspose.words/bordercollection/getenumerator/)() | Devuelve un objeto enumerador que se puede utilizar para iterar sobre todos los bordes de la colección. |

## Observaciones

Los diferentes elementos del documento tienen diferentes bordes. Por ejemplo,[`ParagraphFormat`](../paragraphformat/) tiene[`Bottom`](./bottom/) ,[`Left`](./left/) ,[`Right`](./right/) y[`Top`](./top/) bordes. Puede especificar un formato diferente para cada borde de forma independiente o enumerar todos los bordes y aplicar el mismo formato.

## Ejemplos

Muestra cómo insertar un párrafo con un borde superior.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Border topBorder = builder.ParagraphFormat.Borders.Top;
topBorder.LineWidth = 4.0d;
topBorder.LineStyle = LineStyle.DashSmallGap;
// Establezca ThemeColor solo cuando se configure LineWidth o LineStyle.
topBorder.ThemeColor = ThemeColor.Accent1;
topBorder.TintAndShade = 0.25d;

builder.Writeln("Text with a top border.");

doc.Save(ArtifactsDir + "Border.ParagraphTopBorder.docx");
```

### Ver también

* class [Border](../border/)
* espacio de nombres [Aspose.Words](../../aspose.words/)
* asamblea [Aspose.Words](../../)
