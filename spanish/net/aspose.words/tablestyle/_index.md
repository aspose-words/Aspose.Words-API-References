---
title: TableStyle Class
linktitle: TableStyle
articleTitle: TableStyle
second_title: Aspose.Words para .NET
description: Descubre la clase Aspose.Words.TableStyle para crear y personalizar estilos de tabla impactantes en tus documentos. ¡Mejora tu formato fácilmente!
type: docs
weight: 7070
url: /es/net/aspose.words/tablestyle/
---
## TableStyle class

Representa un estilo de tabla.

Para obtener más información, visite el[Trabajar con tablas](https://docs.aspose.com/words/net/working-with-tables/) Artículo de documentación.

```csharp
public class TableStyle : Style
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [Aliases](../../aspose.words/style/aliases/) { get; } | Obtiene todos los alias de este estilo. Si el estilo no tiene alias, se devuelve una matriz de cadenas vacía. |
| [Alignment](../../aspose.words/tablestyle/alignment/) { get; set; } | Especifica la alineación para el estilo de tabla. |
| [AllowBreakAcrossPages](../../aspose.words/tablestyle/allowbreakacrosspages/) { get; set; } | Obtiene o establece un indicador que indica si se permite que el texto de una fila de tabla se divida en un salto de página. |
| [AutomaticallyUpdate](../../aspose.words/style/automaticallyupdate/) { get; set; } | Especifica si este estilo se redefine automáticamente en función del valor apropiado. |
| [BaseStyleName](../../aspose.words/style/basestylename/) { get; set; } | Obtiene/establece el nombre del estilo en el que se basa este estilo. |
| [Bidi](../../aspose.words/tablestyle/bidi/) { get; set; } | Obtiene o establece si este es un estilo para una tabla de derecha a izquierda. |
| [Borders](../../aspose.words/tablestyle/borders/) { get; } | Obtiene la colección de bordes de celda predeterminados para el estilo. |
| [BottomPadding](../../aspose.words/tablestyle/bottompadding/) { get; set; } | Obtiene o establece la cantidad de espacio (en puntos) que se agregará debajo del contenido de las celdas de la tabla. |
| [BuiltIn](../../aspose.words/style/builtin/) { get; } | Verdadero si este estilo es uno de los estilos integrados en MS Word. |
| [CellSpacing](../../aspose.words/tablestyle/cellspacing/) { get; set; } | Obtiene o establece la cantidad de espacio (en puntos) entre las celdas. |
| [ColumnStripe](../../aspose.words/tablestyle/columnstripe/) { get; set; } | Obtiene o establece una cantidad de columnas para incluir en las bandas cuando el estilo especifica bandas de columnas pares/impares. |
| [ConditionalStyles](../../aspose.words/tablestyle/conditionalstyles/) { get; } | Colección de estilos condicionales que se pueden definir para este estilo de tabla. |
| [Document](../../aspose.words/style/document/) { get; } | Obtiene el documento del propietario. |
| [Font](../../aspose.words/style/font/) { get; } | Obtiene el formato de carácter del estilo. |
| [IsHeading](../../aspose.words/style/isheading/) { get; } | Verdadero cuando el estilo es uno de los estilos de título integrados. |
| [IsQuickStyle](../../aspose.words/style/isquickstyle/) { get; set; } | Especifica si este estilo se muestra en la galería de estilos rápidos dentro de la interfaz de usuario de MS Word. |
| [LeftIndent](../../aspose.words/tablestyle/leftindent/) { get; set; } | Obtiene o establece el valor que representa la sangría izquierda de una tabla. |
| [LeftPadding](../../aspose.words/tablestyle/leftpadding/) { get; set; } | Obtiene o establece la cantidad de espacio (en puntos) que se agregará a la izquierda del contenido de las celdas de la tabla. |
| [LinkedStyleName](../../aspose.words/style/linkedstylename/) { get; set; } | Obtiene/establece el nombre del[`Style`](../style/) Vinculado a este. Devuelve una cadena vacía si no hay estilos vinculados. |
| [List](../../aspose.words/style/list/) { get; } | Obtiene la lista que define el formato de este estilo de lista. |
| [ListFormat](../../aspose.words/style/listformat/) { get; } | Proporciona acceso a las propiedades de formato de lista de un estilo de párrafo. |
| [Locked](../../aspose.words/style/locked/) { get; set; } | Especifica si este estilo está bloqueado. |
| [Name](../../aspose.words/style/name/) { get; set; } | Obtiene o establece el nombre del estilo. |
| [NextParagraphStyleName](../../aspose.words/style/nextparagraphstylename/) { get; set; } | Obtiene/establece el nombre del estilo que se aplicará automáticamente a un nuevo párrafo insertado después de un párrafo formateado con el estilo especificado. |
| [ParagraphFormat](../../aspose.words/style/paragraphformat/) { get; } | Obtiene el formato de párrafo del estilo. |
| [Priority](../../aspose.words/style/priority/) { get; set; } | Obtiene/establece el valor entero que representa la prioridad para ordenar los estilos en el panel de tareas Estilos. |
| [RightPadding](../../aspose.words/tablestyle/rightpadding/) { get; set; } | Obtiene o establece la cantidad de espacio (en puntos) que se agregará a la derecha del contenido de las celdas de la tabla. |
| [RowStripe](../../aspose.words/tablestyle/rowstripe/) { get; set; } | Obtiene o establece una cantidad de filas para incluir en las bandas cuando el estilo especifica bandas de filas pares/impares. |
| [SemiHidden](../../aspose.words/style/semihidden/) { get; set; } | Obtiene/establece si el estilo se oculta en la galería de Estilos y en el panel de tareas Estilos. |
| [Shading](../../aspose.words/tablestyle/shading/) { get; } | Obtiene un[`Shading`](../shading/) objeto que hace referencia al formato de sombreado para celdas de tabla. |
| [StyleIdentifier](../../aspose.words/style/styleidentifier/) { get; } | Obtiene el identificador de estilo independiente de la configuración regional para un estilo integrado. |
| [Styles](../../aspose.words/style/styles/) { get; } | Obtiene la colección de estilos a la que pertenece este estilo. |
| [TopPadding](../../aspose.words/tablestyle/toppadding/) { get; set; } | Obtiene o establece la cantidad de espacio (en puntos) que se agregará sobre el contenido de las celdas de la tabla. |
| [Type](../../aspose.words/style/type/) { get; } | Obtiene el tipo de estilo (párrafo o carácter). |
| [UnhideWhenUsed](../../aspose.words/style/unhidewhenused/) { get; set; } | Obtiene/establece si el estilo usado en el documento actual se muestra en la galería de Estilos y en el panel de tareas Estilos. Verdadero cuando el estilo usado debe mostrarse en la galería de Estilos. |
| [VerticalAlignment](../../aspose.words/tablestyle/verticalalignment/) { get; set; } | Especifica la alineación vertical de las celdas. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [Equals](../../aspose.words/style/equals/)(*[Style](../style/)*) | Se compara con el estilo especificado. Los estilos predeterminados se comparan solo para estilos integrados. Los estilos predeterminados no se incluyen en la comparación. El estilo base, el estilo vinculado y el estilo del siguiente párrafo se comparan de forma recursiva. |
| [Remove](../../aspose.words/style/remove/)() | Elimina el estilo especificado del documento. |

## Ejemplos

Muestra cómo crear configuraciones de estilo personalizadas para la tabla.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Name");
builder.InsertCell();
builder.Write("مرحبًا");
builder.EndRow();
builder.InsertCell();
builder.InsertCell();
builder.EndTable();

TableStyle tableStyle = (TableStyle)doc.Styles.Add(StyleType.Table, "MyTableStyle1");
tableStyle.AllowBreakAcrossPages = true;
tableStyle.Bidi = true;
tableStyle.CellSpacing = 5;
tableStyle.BottomPadding = 20;
tableStyle.LeftPadding = 5;
tableStyle.RightPadding = 10;
tableStyle.TopPadding = 20;
tableStyle.Shading.BackgroundPatternColor = Color.AntiqueWhite;
tableStyle.Borders.Color = Color.Blue;
tableStyle.Borders.LineStyle = LineStyle.DotDash;
tableStyle.VerticalAlignment = CellVerticalAlignment.Center;

table.Style = tableStyle;

// Establecer las propiedades de estilo de una tabla puede afectar las propiedades de la tabla misma.
Assert.True(table.Bidi);
Assert.AreEqual(5.0d, table.CellSpacing);
Assert.AreEqual("MyTableStyle1", table.StyleName);

doc.Save(ArtifactsDir + "Table.TableStyleCreation.docx");
```

### Ver también

* class [Style](../style/)
* espacio de nombres [Aspose.Words](../../aspose.words/)
* asamblea [Aspose.Words](../../)
