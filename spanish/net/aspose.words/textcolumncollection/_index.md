---
title: Class TextColumnCollection
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.TextColumnCollection clase. Una colección deTextColumn objetos que representan todas las columnas de texto en una sección de un documento.
type: docs
weight: 6100
url: /es/net/aspose.words/textcolumncollection/
---
## TextColumnCollection class

Una colección de[`TextColumn`](../textcolumn/) objetos que representan todas las columnas de texto en una sección de un documento.

```csharp
public class TextColumnCollection
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [Count](../../aspose.words/textcolumncollection/count/) { get; } | Obtiene el número de columnas de la sección de un documento. |
| [EvenlySpaced](../../aspose.words/textcolumncollection/evenlyspaced/) { get; set; } | **Verdadero** si las columnas de texto tienen el mismo ancho y están espaciadas uniformemente. |
| [Item](../../aspose.words/textcolumncollection/item/) { get; } | Devuelve una columna de texto en el índice especificado. |
| [LineBetween](../../aspose.words/textcolumncollection/linebetween/) { get; set; } | cuando **verdadero** , agrega una línea vertical entre columnas. |
| [Spacing](../../aspose.words/textcolumncollection/spacing/) { get; set; } | Cuando las columnas están espaciadas uniformemente, obtiene o establece la cantidad de espacio entre cada columna en puntos. |
| [Width](../../aspose.words/textcolumncollection/width/) { get; } | Cuando las columnas están espaciadas uniformemente, obtiene el ancho de las columnas. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [SetCount](../../aspose.words/textcolumncollection/setcount/)(int) | Organiza el texto en el número especificado de columnas de texto. |

### Observaciones

Usar[`SetCount`](./setcount/) para establecer el número de columnas de texto.

Para hacer que todas las columnas tengan el mismo ancho y estén espaciadas uniformemente, configure[`EvenlySpaced`](./evenlyspaced/) a **verdadero** y especifique la cantidad de espacio entre las columnas en[`Spacing`](./spacing/). MS Word will calculará automáticamente el ancho de las columnas.

Si usted tiene **uniformemente espaciados** ajustado a **falso** debe especificar el ancho y el espaciado para cada columna individualmente. Utilice el indexador para acceder a las personas[`TextColumn`](../textcolumn/) objetos.

Cuando utilice anchos de columna personalizados, asegúrese de que la suma de todos los anchos de columna y los espacios entre ellos sea igual al ancho de página menos los márgenes de página izquierdo y derecho.

### Ejemplos

Muestra cómo crear varias columnas espaciadas uniformemente en una sección.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

TextColumnCollection columns = builder.PageSetup.TextColumns;
columns.Spacing = 100;
columns.SetCount(2);

builder.Writeln("Column 1.");
builder.InsertBreak(BreakType.ColumnBreak);
builder.Writeln("Column 2.");

doc.Save(ArtifactsDir + "PageSetup.ColumnsSameWidth.docx");
```

### Ver también

* espacio de nombres [Aspose.Words](../../aspose.words/)
* asamblea [Aspose.Words](../../)


