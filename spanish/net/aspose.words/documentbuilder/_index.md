---
title: Class DocumentBuilder
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.DocumentBuilder clase. Proporciona métodos para insertar texto imágenes y otro contenido especificar formato de fuente párrafo y sección.
type: docs
weight: 450
url: /es/net/aspose.words/documentbuilder/
---
## DocumentBuilder class

Proporciona métodos para insertar texto, imágenes y otro contenido, especificar formato de fuente, párrafo y sección.

Para obtener más información, visite el[Descripción general del generador de documentos](https://docs.aspose.com/words/net/document-builder-overview/) artículo de documentación.

```csharp
public class DocumentBuilder
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [DocumentBuilder](documentbuilder/#constructor)() | Inicializa una nueva instancia de esta clase. |
| [DocumentBuilder](documentbuilder/#constructor_1)(Document) | Inicializa una nueva instancia de esta clase. |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [Bold](../../aspose.words/documentbuilder/bold/) { get; set; } | Verdadero si la fuente tiene el formato negrita. |
| [CellFormat](../../aspose.words/documentbuilder/cellformat/) { get; } | Devuelve un objeto que representa las propiedades de formato de celda de la tabla actual. |
| [CurrentNode](../../aspose.words/documentbuilder/currentnode/) { get; } | Obtiene el nodo actualmente seleccionado en este DocumentBuilder. |
| [CurrentParagraph](../../aspose.words/documentbuilder/currentparagraph/) { get; } | Obtiene el párrafo actualmente seleccionado en este`DocumentBuilder` . |
| [CurrentSection](../../aspose.words/documentbuilder/currentsection/) { get; } | Obtiene la sección actualmente seleccionada en este`DocumentBuilder` . |
| [CurrentStory](../../aspose.words/documentbuilder/currentstory/) { get; } | Obtiene la historia actualmente seleccionada en este`DocumentBuilder` . |
| [CurrentStructuredDocumentTag](../../aspose.words/documentbuilder/currentstructureddocumenttag/) { get; } | Obtiene la etiqueta del documento estructurado que está seleccionado actualmente en este`DocumentBuilder` . |
| [Document](../../aspose.words/documentbuilder/document/) { get; set; } | Obtiene o establece el[`Document`](./document/)objeto al que está adjunto este objeto. |
| [Font](../../aspose.words/documentbuilder/font/) { get; } | Devuelve un objeto que representa las propiedades de formato de fuente actuales. |
| [IsAtEndOfParagraph](../../aspose.words/documentbuilder/isatendofparagraph/) { get; } | Devoluciones`verdadero` si el cursor está al final del párrafo actual. |
| [IsAtEndOfStructuredDocumentTag](../../aspose.words/documentbuilder/isatendofstructureddocumenttag/) { get; } | Devoluciones **verdadero** si el cursor está al final de una etiqueta de documento estructurado. |
| [IsAtStartOfParagraph](../../aspose.words/documentbuilder/isatstartofparagraph/) { get; } | Devoluciones`verdadero` si el cursor está al principio del párrafo actual (no hay texto antes del cursor). |
| [Italic](../../aspose.words/documentbuilder/italic/) { get; set; } | Verdadero si la fuente tiene el formato de cursiva. |
| [ListFormat](../../aspose.words/documentbuilder/listformat/) { get; } | Devuelve un objeto que representa las propiedades de formato de la lista actual. |
| [PageSetup](../../aspose.words/documentbuilder/pagesetup/) { get; } | Devuelve un objeto que representa la configuración de página actual y las propiedades de la sección. |
| [ParagraphFormat](../../aspose.words/documentbuilder/paragraphformat/) { get; } | Devuelve un objeto que representa las propiedades de formato del párrafo actual. |
| [RowFormat](../../aspose.words/documentbuilder/rowformat/) { get; } | Devuelve un objeto que representa las propiedades de formato de fila de la tabla actual. |
| [Underline](../../aspose.words/documentbuilder/underline/) { get; set; } | Obtiene/establece el tipo de subrayado para la fuente actual. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [DeleteRow](../../aspose.words/documentbuilder/deleterow/)(int, int) | Elimina una fila de una tabla. |
| [EndBookmark](../../aspose.words/documentbuilder/endbookmark/)(string) | Marca la posición actual en el documento como final del marcador. |
| [EndColumnBookmark](../../aspose.words/documentbuilder/endcolumnbookmark/)(string) | Marca la posición actual en el documento como final de marcador de columna. La posición debe estar en una celda de la tabla. |
| [EndEditableRange](../../aspose.words/documentbuilder/endeditablerange/#endeditablerange)() | Marca la posición actual en el documento como un final de rango editable. |
| [EndEditableRange](../../aspose.words/documentbuilder/endeditablerange/#endeditablerange_1)(EditableRangeStart) | Marca la posición actual en el documento como un final de rango editable. |
| [EndRow](../../aspose.words/documentbuilder/endrow/)() | Finaliza una fila de la tabla en el documento. |
| [EndTable](../../aspose.words/documentbuilder/endtable/)() | Finaliza una tabla en el documento. |
| [InsertBreak](../../aspose.words/documentbuilder/insertbreak/)(BreakType) | Inserta una ruptura del tipo especificado en el documento. |
| [InsertCell](../../aspose.words/documentbuilder/insertcell/)() | Inserta una celda de tabla en el documento. |
| [InsertChart](../../aspose.words/documentbuilder/insertchart/#insertchart_1)(ChartType, double, double) | Inserta un objeto de gráfico en el documento y lo escala al tamaño especificado. |
| [InsertChart](../../aspose.words/documentbuilder/insertchart/#insertchart)(ChartType, RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) | Inserta un objeto de gráfico en el documento y lo escala al tamaño especificado. |
| [InsertCheckBox](../../aspose.words/documentbuilder/insertcheckbox/#insertcheckbox_1)(string, bool, int) | Inserta un campo de formulario de casilla de verificación en la posición actual. |
| [InsertCheckBox](../../aspose.words/documentbuilder/insertcheckbox/#insertcheckbox)(string, bool, bool, int) | Inserta un campo de formulario de casilla de verificación en la posición actual. |
| [InsertComboBox](../../aspose.words/documentbuilder/insertcombobox/)(string, string[], int) | Inserta un campo de formulario de cuadro combinado en la posición actual. |
| [InsertDocument](../../aspose.words/documentbuilder/insertdocument/#insertdocument)(Document, ImportFormatMode) | Inserta un documento en la posición del cursor. |
| [InsertDocument](../../aspose.words/documentbuilder/insertdocument/#insertdocument_1)(Document, ImportFormatMode, ImportFormatOptions) | Inserta un documento en la posición del cursor. |
| [InsertDocumentInline](../../aspose.words/documentbuilder/insertdocumentinline/)(Document, ImportFormatMode, ImportFormatOptions) |  |
| [InsertField](../../aspose.words/documentbuilder/insertfield/#insertfield_1)(string) | Inserta un campo de Word en un documento y actualiza el resultado del campo. |
| [InsertField](../../aspose.words/documentbuilder/insertfield/#insertfield)(FieldType, bool) | Inserta un campo de Word en un documento y, opcionalmente, actualiza el resultado del campo. |
| [InsertField](../../aspose.words/documentbuilder/insertfield/#insertfield_2)(string, string) | Inserta un campo de Word en un documento sin actualizar el resultado del campo. |
| [InsertFootnote](../../aspose.words/documentbuilder/insertfootnote/#insertfootnote)(FootnoteType, string) | Inserta una nota al pie o una nota final en el documento. |
| [InsertFootnote](../../aspose.words/documentbuilder/insertfootnote/#insertfootnote_1)(FootnoteType, string, string) | Inserta una nota al pie o una nota final en el documento. |
| [InsertHorizontalRule](../../aspose.words/documentbuilder/inserthorizontalrule/)() | Inserta una forma de regla horizontal en el documento. |
| [InsertHtml](../../aspose.words/documentbuilder/inserthtml/#inserthtml)(string) | Inserta una cadena HTML en el documento. |
| [InsertHtml](../../aspose.words/documentbuilder/inserthtml/#inserthtml_2)(string, bool) | Inserta una cadena HTML en el documento. |
| [InsertHtml](../../aspose.words/documentbuilder/inserthtml/#inserthtml_1)(string, HtmlInsertOptions) | Inserta una cadena HTML en el documento. Permite especificar opciones adicionales. |
| [InsertHyperlink](../../aspose.words/documentbuilder/inserthyperlink/)(string, string, bool) | Inserta un hipervínculo en el documento. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage)(byte[]) | Inserta una imagen de una matriz de bytes en el documento. La imagen se inserta en línea y a escala del 100%. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_3)(Image) | Inserta una imagen desde un .NETImage objeto en el documento. La imagen se inserta en línea y a escala del 100%. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_6)(Stream) | Inserta una imagen de una secuencia en el documento. La imagen se inserta en línea y a escala del 100%. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_9)(string) | Inserta una imagen de un archivo o URL en el documento. La imagen se inserta en línea y a escala del 100%. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_2)(byte[], double, double) | Inserta una imagen en línea de una matriz de bytes en el documento y la escala al tamaño especificado. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_5)(Image, double, double) | Inserta una imagen en línea desde .NETImage objeto en el documento y lo escala al tamaño especificado. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_8)(Stream, double, double) | Inserta una imagen en línea de una secuencia en el documento y la escala al tamaño especificado. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_11)(string, double, double) | Inserta una imagen en línea de un archivo o URL en el documento y la escala al tamaño especificado. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_1)(byte[], RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) | Inserta una imagen de una matriz de bytes en la posición y el tamaño especificados. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_4)(Image, RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) | Inserta una imagen desde un .NETImage objeto en la posición y tamaño especificados. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_7)(Stream, RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) | Inserta una imagen de una secuencia en la posición y el tamaño especificados. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_10)(string, RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) | Inserta una imagen de un archivo o URL en la posición y tamaño especificados. |
| [InsertNode](../../aspose.words/documentbuilder/insertnode/)(Node) | Inserta un nodo antes del cursor. |
| [InsertOleObject](../../aspose.words/documentbuilder/insertoleobject/#insertoleobject)(Stream, string, bool, Stream) | Inserta un objeto OLE incrustado de una secuencia en el documento. |
| [InsertOleObject](../../aspose.words/documentbuilder/insertoleobject/#insertoleobject_1)(string, bool, bool, Stream) | Inserta un objeto OLE incrustado o vinculado desde un archivo en el documento. Detecta el tipo de objeto OLE usando la extensión de archivo. |
| [InsertOleObject](../../aspose.words/documentbuilder/insertoleobject/#insertoleobject_2)(string, string, bool, bool, Stream) | Inserta un objeto OLE incrustado o vinculado desde un archivo en el documento. Detecta el tipo de objeto OLE utilizando el parámetro progID dado. |
| [InsertOleObjectAsIcon](../../aspose.words/documentbuilder/insertoleobjectasicon/#insertoleobjectasicon)(Stream, string, string, string) | Inserta un objeto OLE incrustado como icono de una secuencia en el documento. Permite especificar el archivo de icono y el título. Detecta el tipo de objeto OLE utilizando el parámetro progID dado. |
| [InsertOleObjectAsIcon](../../aspose.words/documentbuilder/insertoleobjectasicon/#insertoleobjectasicon_1)(string, bool, string, string) | Inserta un objeto OLE incrustado o vinculado como icono en el documento. Permite especificar el archivo de icono y el título. Detecta el tipo de objeto OLE usando la extensión de archivo. |
| [InsertOleObjectAsIcon](../../aspose.words/documentbuilder/insertoleobjectasicon/#insertoleobjectasicon_2)(string, string, bool, string, string) | Inserta un objeto OLE incrustado o vinculado como icono en el documento. Permite especificar el archivo de icono y el título. Detecta el tipo de objeto OLE utilizando el parámetro progID dado. |
| [InsertOnlineVideo](../../aspose.words/documentbuilder/insertonlinevideo/#insertonlinevideo_1)(string, double, double) | Inserta un objeto de vídeo en línea en el documento y lo escala al tamaño especificado. |
| [InsertOnlineVideo](../../aspose.words/documentbuilder/insertonlinevideo/#insertonlinevideo_3)(string, string, byte[], double, double) | Inserta un objeto de vídeo en línea en el documento y lo escala al tamaño especificado. |
| [InsertOnlineVideo](../../aspose.words/documentbuilder/insertonlinevideo/#insertonlinevideo)(string, RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) | Inserta un objeto de vídeo en línea en el documento y lo escala al tamaño especificado. |
| [InsertOnlineVideo](../../aspose.words/documentbuilder/insertonlinevideo/#insertonlinevideo_2)(string, string, byte[], RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) | Inserta un objeto de vídeo en línea en el documento y lo escala al tamaño especificado. |
| [InsertParagraph](../../aspose.words/documentbuilder/insertparagraph/)() | Inserta un salto de párrafo en el documento. |
| [InsertShape](../../aspose.words/documentbuilder/insertshape/#insertshape_1)(ShapeType, double, double) | Inserta una forma en línea con el tipo y tamaño especificados. |
| [InsertShape](../../aspose.words/documentbuilder/insertshape/#insertshape)(ShapeType, RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) | Inserta una forma flotante con una posición, tamaño y tipo de ajuste de texto especificados. |
| [InsertSignatureLine](../../aspose.words/documentbuilder/insertsignatureline/#insertsignatureline)(SignatureLineOptions) | Inserta una línea de firma en la posición actual. |
| [InsertSignatureLine](../../aspose.words/documentbuilder/insertsignatureline/#insertsignatureline_1)(SignatureLineOptions, RelativeHorizontalPosition, double, RelativeVerticalPosition, double, WrapType) | Inserta una línea de firma en la posición especificada. |
| [InsertStyleSeparator](../../aspose.words/documentbuilder/insertstyleseparator/)() | Inserta un separador de estilo en el documento. |
| [InsertTableOfContents](../../aspose.words/documentbuilder/inserttableofcontents/)(string) | Inserta un campo TOC (tabla de contenido) en el documento. |
| [InsertTextInput](../../aspose.words/documentbuilder/inserttextinput/)(string, TextFormFieldType, string, string, int) | Inserta un campo de formulario de texto en la posición actual. |
| [MoveTo](../../aspose.words/documentbuilder/moveto/)(Node) | Mueve el cursor a un nodo en línea o al final de un párrafo. |
| [MoveToBookmark](../../aspose.words/documentbuilder/movetobookmark/#movetobookmark)(string) | Mueve el cursor a un marcador. |
| [MoveToBookmark](../../aspose.words/documentbuilder/movetobookmark/#movetobookmark_1)(string, bool, bool) | Mueve el cursor a un marcador con mayor precisión. |
| [MoveToCell](../../aspose.words/documentbuilder/movetocell/)(int, int, int, int) | Mueve el cursor a una celda de la tabla en la sección actual. |
| [MoveToDocumentEnd](../../aspose.words/documentbuilder/movetodocumentend/)() | Mueve el cursor al final del documento. |
| [MoveToDocumentStart](../../aspose.words/documentbuilder/movetodocumentstart/)() | Mueve el cursor al principio del documento. |
| [MoveToField](../../aspose.words/documentbuilder/movetofield/)(Field, bool) | Mueve el cursor a un campo del documento. |
| [MoveToHeaderFooter](../../aspose.words/documentbuilder/movetoheaderfooter/)(HeaderFooterType) | Mueve el cursor al principio de un encabezado o pie de página en la sección actual. |
| [MoveToMergeField](../../aspose.words/documentbuilder/movetomergefield/#movetomergefield)(string) | Mueve el cursor a una posición justo más allá del campo de combinación especificado y elimina el campo de combinación. |
| [MoveToMergeField](../../aspose.words/documentbuilder/movetomergefield/#movetomergefield_1)(string, bool, bool) | Mueve el campo de combinación al campo de combinación especificado. |
| [MoveToParagraph](../../aspose.words/documentbuilder/movetoparagraph/)(int, int) | Mueve el cursor a un párrafo en la sección actual. |
| [MoveToSection](../../aspose.words/documentbuilder/movetosection/)(int) | Mueve el cursor al principio del cuerpo en una sección especificada. |
| [MoveToStructuredDocumentTag](../../aspose.words/documentbuilder/movetostructureddocumenttag/#movetostructureddocumenttag_1)(int, int) | Mueve el cursor a una etiqueta de documento estructurado en la sección actual. |
| [MoveToStructuredDocumentTag](../../aspose.words/documentbuilder/movetostructureddocumenttag/#movetostructureddocumenttag)(StructuredDocumentTag, int) | Mueve el cursor a la etiqueta del documento estructurado. |
| [PopFont](../../aspose.words/documentbuilder/popfont/)() | Recupera el formato de caracteres previamente guardado en la pila. |
| [PushFont](../../aspose.words/documentbuilder/pushfont/)() | Guarda el formato de caracteres actual en la pila. |
| [StartBookmark](../../aspose.words/documentbuilder/startbookmark/)(string) | Marca la posición actual en el documento como inicio de marcador. |
| [StartColumnBookmark](../../aspose.words/documentbuilder/startcolumnbookmark/)(string) | Marca la posición actual en el documento como inicio de marcador de columna. La posición debe estar en una celda de la tabla. |
| [StartEditableRange](../../aspose.words/documentbuilder/starteditablerange/)() | Marca la posición actual en el documento como un inicio de rango editable. |
| [StartTable](../../aspose.words/documentbuilder/starttable/)() | Inicia una tabla en el documento. |
| [Write](../../aspose.words/documentbuilder/write/)(string) | Inserta una cadena en el documento en la posición de inserción actual. |
| [Writeln](../../aspose.words/documentbuilder/writeln/#writeln)() | Inserta un salto de párrafo en el documento. |
| [Writeln](../../aspose.words/documentbuilder/writeln/#writeln_1)(string) | Inserta una cadena y un salto de párrafo en el documento. |

### Observaciones

`DocumentBuilder` hace que el proceso de construcción de un[`Document`](../document/) más fácil. [`Document`](../document/) es un objeto compuesto que consta de un árbol de nodos y, si bien es posible insertar content nodos directamente en el árbol, requiere una buena comprensión de la estructura del árbol. `DocumentBuilder` es una "fachada" para la compleja estructura de[`Document`](../document/) y permite a insertar contenido y formatear de forma rápida y sencilla.

Crear un`DocumentBuilder` y asociarlo con un[`Document`](../document/).

El`DocumentBuilder` tiene un cursor interno donde se insertará el texto cuando llames[`Write`](./write/) ,[`Writeln`](./writeln/) ,[`InsertBreak`](./insertbreak/) y otros métodos. Puedes navegar por el`DocumentBuilder` cursor a una ubicación diferente en un documento usando varios métodos MoveToXXX.

Utilizar el[`Font`](./font/)propiedad para especificar el formato de caracteres que se aplicará a todo el texto insertado desde la posición actual en el documento en adelante.

Utilizar el[`ParagraphFormat`](./paragraphformat/) propiedad para especificar el formato de párrafo para current y todos los párrafos que se insertarán.

Utilizar el[`PageSetup`](./pagesetup/) propiedad para especificar las propiedades de página y sección para la sección current y todas las secciones que se insertarán.

Utilizar el[`CellFormat`](./cellformat/) y[`RowFormat`](./rowformat/) properties para especificar propiedades de formato para celdas y filas de la tabla. Usuario el[`InsertCell`](./insertcell/) y [`EndRow`](./endrow/) Métodos para construir una tabla.

Tenga en cuenta que[`Font`](./font/) ,[`ParagraphFormat`](./paragraphformat/) y[`PageSetup`](./pagesetup/) Las propiedades se actualizan cada vez que navega a un lugar diferente en el documento para reflejar las propiedades de formato disponibles en la nueva ubicación.

### Ejemplos

Muestra cómo utilizar un generador de documentos para crear una tabla.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inicie la tabla, luego complete la primera fila con dos celdas.
builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, Cell 1.");
builder.InsertCell();
builder.Write("Row 1, Cell 2.");

// Llame al método "EndRow" del constructor para iniciar una nueva fila.
builder.EndRow();
builder.InsertCell();
builder.Write("Row 2, Cell 1.");
builder.InsertCell();
builder.Write("Row 2, Cell 2.");
builder.EndTable();

doc.Save(ArtifactsDir + "DocumentBuilder.CreateTable.docx");
```

Muestra cómo crear encabezados y pies de página en un documento usando DocumentBuilder.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Especifica que queremos encabezados y pies de página diferentes para las primeras páginas, pares e impares.
builder.PageSetup.DifferentFirstPageHeaderFooter = true;
builder.PageSetup.OddAndEvenPagesHeaderFooter = true;

// Cree los encabezados, luego agregue tres páginas al documento para mostrar cada tipo de encabezado.
builder.MoveToHeaderFooter(HeaderFooterType.HeaderFirst);
builder.Write("Header for the first page");
builder.MoveToHeaderFooter(HeaderFooterType.HeaderEven);
builder.Write("Header for even pages");
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Write("Header for all other pages");

builder.MoveToSection(0);
builder.Writeln("Page1");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page2");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page3");

doc.Save(ArtifactsDir + "DocumentBuilder.HeadersAndFooters.docx");
```

Muestra cómo crear una tabla con bordes personalizados.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.StartTable();

// Configurar opciones de formato de tabla para un creador de documentos
// los aplicará a cada fila y celda que agreguemos con ella.
builder.ParagraphFormat.Alignment = ParagraphAlignment.Center;

builder.CellFormat.ClearFormatting();
builder.CellFormat.Width = 150;
builder.CellFormat.VerticalAlignment = CellVerticalAlignment.Center;
builder.CellFormat.Shading.BackgroundPatternColor = Color.GreenYellow;
builder.CellFormat.WrapText = false;
builder.CellFormat.FitText = true;

builder.RowFormat.ClearFormatting();
builder.RowFormat.HeightRule = HeightRule.Exactly;
builder.RowFormat.Height = 50;
builder.RowFormat.Borders.LineStyle = LineStyle.Engrave3D;
builder.RowFormat.Borders.Color = Color.Orange;

builder.InsertCell();
builder.Write("Row 1, Col 1");

builder.InsertCell();
builder.Write("Row 1, Col 2");
builder.EndRow();

// Cambiar el formato lo aplicará a la celda actual,
// y cualquier celda nueva que creemos con el constructor posteriormente.
// Esto no afectará a las celdas que hayamos añadido anteriormente.
builder.CellFormat.Shading.ClearFormatting();

builder.InsertCell();
builder.Write("Row 2, Col 1");

builder.InsertCell();
builder.Write("Row 2, Col 2");

builder.EndRow();

// Aumenta la altura de la fila para que se ajuste al texto vertical.
builder.InsertCell();
builder.RowFormat.Height = 150;
builder.CellFormat.Orientation = TextOrientation.Upward;
builder.Write("Row 3, Col 1");

builder.InsertCell();
builder.CellFormat.Orientation = TextOrientation.Downward;
builder.Write("Row 3, Col 2");

builder.EndRow();
builder.EndTable();

doc.Save(ArtifactsDir + "DocumentBuilder.InsertTable.docx");
```

### Ver también

* espacio de nombres [Aspose.Words](../../aspose.words/)
* asamblea [Aspose.Words](../../)


