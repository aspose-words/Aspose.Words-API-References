---
title: DocumentBuilder Class
linktitle: DocumentBuilder
articleTitle: DocumentBuilder
second_title: Aspose.Words para .NET
description: Descubra la clase Aspose.Words.DocumentBuilder: su solución para insertar sin esfuerzo texto, imágenes y elementos de formato en documentos.
type: docs
weight: 660
url: /es/net/aspose.words/documentbuilder/
---
## DocumentBuilder class

Proporciona métodos para insertar texto, imágenes y otro contenido, especificar fuente, párrafo y formato de sección.

Para obtener más información, visite el[Descripción general del generador de documentos](https://docs.aspose.com/words/net/document-builder-overview/) Artículo de documentación.

```csharp
public class DocumentBuilder
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [DocumentBuilder](documentbuilder/#constructor)() | Inicializa una nueva instancia de esta clase. |
| [DocumentBuilder](documentbuilder/#constructor_1)(*[Document](../document/)*) | Inicializa una nueva instancia de esta clase. |
| [DocumentBuilder](documentbuilder/#constructor_3)(*[DocumentBuilderOptions](../documentbuilderoptions/)*) | Inicializa una nueva instancia de esta clase. |
| [DocumentBuilder](documentbuilder/#constructor_2)(*[Document](../document/), [DocumentBuilderOptions](../documentbuilderoptions/)*) | Inicializa una nueva instancia de esta clase. |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [Bold](../../aspose.words/documentbuilder/bold/) { get; set; } | Verdadero si la fuente está formateada en negrita. |
| [CellFormat](../../aspose.words/documentbuilder/cellformat/) { get; } | Devuelve un objeto que representa las propiedades de formato de celda de la tabla actual. |
| [CurrentNode](../../aspose.words/documentbuilder/currentnode/) { get; } | Obtiene el nodo que está seleccionado actualmente en este DocumentBuilder. |
| [CurrentParagraph](../../aspose.words/documentbuilder/currentparagraph/) { get; } | Obtiene el párrafo que está seleccionado actualmente en este`DocumentBuilder` . |
| [CurrentSection](../../aspose.words/documentbuilder/currentsection/) { get; } | Obtiene la sección que está seleccionada actualmente en este`DocumentBuilder` . |
| [CurrentStory](../../aspose.words/documentbuilder/currentstory/) { get; } | Obtiene la historia que está seleccionada actualmente en este`DocumentBuilder` . |
| [CurrentStructuredDocumentTag](../../aspose.words/documentbuilder/currentstructureddocumenttag/) { get; } | Obtiene la etiqueta del documento estructurado que está seleccionada actualmente en este`DocumentBuilder` . |
| [Document](../../aspose.words/documentbuilder/document/) { get; set; } | Obtiene o establece el[`Document`](./document/) objeto al que está adjunto este objeto. |
| [Font](../../aspose.words/documentbuilder/font/) { get; } | Devuelve un objeto que representa las propiedades de formato de fuente actuales. |
| [IsAtEndOfParagraph](../../aspose.words/documentbuilder/isatendofparagraph/) { get; } | Devuelve`verdadero` si el cursor está al final del párrafo actual. |
| [IsAtEndOfStructuredDocumentTag](../../aspose.words/documentbuilder/isatendofstructureddocumenttag/) { get; } | Devuelve**verdadero** si el cursor está al final de una etiqueta de documento estructurado. |
| [IsAtStartOfParagraph](../../aspose.words/documentbuilder/isatstartofparagraph/) { get; } | Devuelve`verdadero`si el cursor está al principio del párrafo actual (no hay texto antes del cursor). |
| [Italic](../../aspose.words/documentbuilder/italic/) { get; set; } | Verdadero si la fuente está formateada como cursiva. |
| [ListFormat](../../aspose.words/documentbuilder/listformat/) { get; } | Devuelve un objeto que representa las propiedades de formato de lista actuales. |
| [PageSetup](../../aspose.words/documentbuilder/pagesetup/) { get; } | Devuelve un objeto que representa la configuración de la página actual y las propiedades de la sección. |
| [ParagraphFormat](../../aspose.words/documentbuilder/paragraphformat/) { get; } | Devuelve un objeto que representa las propiedades de formato de párrafo actuales. |
| [RowFormat](../../aspose.words/documentbuilder/rowformat/) { get; } | Devuelve un objeto que representa las propiedades de formato de fila de la tabla actual. |
| [Underline](../../aspose.words/documentbuilder/underline/) { get; set; } | Obtiene/establece el tipo de subrayado para la fuente actual. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [DeleteRow](../../aspose.words/documentbuilder/deleterow/)(*int, int*) | Elimina una fila de una tabla. |
| [EndBookmark](../../aspose.words/documentbuilder/endbookmark/)(*string*) | Marca la posición actual en el documento como un marcador final. |
| [EndColumnBookmark](../../aspose.words/documentbuilder/endcolumnbookmark/)(*string*) | Marca la posición actual en el documento como final de marcador de columna. La posición debe estar en una celda de tabla. |
| [EndEditableRange](../../aspose.words/documentbuilder/endeditablerange/#endeditablerange)() | Marca la posición actual en el documento como un final de rango editable. |
| [EndEditableRange](../../aspose.words/documentbuilder/endeditablerange/#endeditablerange_1)(*[EditableRangeStart](../editablerangestart/)*) | Marca la posición actual en el documento como un final de rango editable. |
| [EndRow](../../aspose.words/documentbuilder/endrow/)() | Finaliza una fila de la tabla en el documento. |
| [EndTable](../../aspose.words/documentbuilder/endtable/)() | Finaliza una tabla en el documento. |
| [InsertBreak](../../aspose.words/documentbuilder/insertbreak/)(*[BreakType](../breaktype/)*) | Inserta un salto del tipo especificado en el documento. |
| [InsertCell](../../aspose.words/documentbuilder/insertcell/)() | Inserta una celda de tabla en el documento. |
| [InsertChart](../../aspose.words/documentbuilder/insertchart/#insertchart_2)(*[ChartType](../../aspose.words.drawing.charts/charttype/), double, double*) | Inserta un objeto de gráfico en el documento y lo escala al tamaño especificado. |
| [InsertChart](../../aspose.words/documentbuilder/insertchart/#insertchart_3)(*[ChartType](../../aspose.words.drawing.charts/charttype/), double, double, [ChartStyle](../../aspose.words.drawing.charts/chartstyle/)*) | Inserta un objeto de gráfico en el documento y lo escala al tamaño especificado. |
| [InsertChart](../../aspose.words/documentbuilder/insertchart/#insertchart)(*[ChartType](../../aspose.words.drawing.charts/charttype/), [RelativeHorizontalPosition](../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../aspose.words.drawing/relativeverticalposition/), double, double, double, [WrapType](../../aspose.words.drawing/wraptype/)*) | Inserta un objeto de gráfico en el documento y lo escala al tamaño especificado. |
| [InsertChart](../../aspose.words/documentbuilder/insertchart/#insertchart_1)(*[ChartType](../../aspose.words.drawing.charts/charttype/), [RelativeHorizontalPosition](../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../aspose.words.drawing/relativeverticalposition/), double, double, double, [WrapType](../../aspose.words.drawing/wraptype/), [ChartStyle](../../aspose.words.drawing.charts/chartstyle/)*) | Inserta un objeto de gráfico en el documento y lo escala al tamaño especificado. |
| [InsertCheckBox](../../aspose.words/documentbuilder/insertcheckbox/#insertcheckbox_1)(*string, bool, int*) | Inserta un campo de formulario de casilla de verificación en la posición actual. |
| [InsertCheckBox](../../aspose.words/documentbuilder/insertcheckbox/#insertcheckbox)(*string, bool, bool, int*) | Inserta un campo de formulario de casilla de verificación en la posición actual. |
| [InsertComboBox](../../aspose.words/documentbuilder/insertcombobox/)(*string, string[], int*) | Inserta un campo de formulario de cuadro combinado en la posición actual. |
| [InsertDocument](../../aspose.words/documentbuilder/insertdocument/#insertdocument)(*[Document](../document/), [ImportFormatMode](../importformatmode/)*) | Inserta un documento en la posición del cursor. |
| [InsertDocument](../../aspose.words/documentbuilder/insertdocument/#insertdocument_1)(*[Document](../document/), [ImportFormatMode](../importformatmode/), [ImportFormatOptions](../importformatoptions/)*) | Inserta un documento en la posición del cursor. |
| [InsertDocumentInline](../../aspose.words/documentbuilder/insertdocumentinline/)(*[Document](../document/), [ImportFormatMode](../importformatmode/), [ImportFormatOptions](../importformatoptions/)*) | Inserta un documento en línea en la posición del cursor. |
| [InsertField](../../aspose.words/documentbuilder/insertfield/#insertfield_1)(*string*) | Inserta un campo de Word en un documento y actualiza el resultado del campo. |
| [InsertField](../../aspose.words/documentbuilder/insertfield/#insertfield)(*[FieldType](../../aspose.words.fields/fieldtype/), bool*) | Inserta un campo de Word en un documento y, opcionalmente, actualiza el resultado del campo. |
| [InsertField](../../aspose.words/documentbuilder/insertfield/#insertfield_2)(*string, string*) | Inserta un campo de Word en un documento sin actualizar el resultado del campo. |
| [InsertFootnote](../../aspose.words/documentbuilder/insertfootnote/#insertfootnote)(*[FootnoteType](../../aspose.words.notes/footnotetype/), string*) | Inserta una nota al pie o una nota final en el documento. |
| [InsertFootnote](../../aspose.words/documentbuilder/insertfootnote/#insertfootnote_1)(*[FootnoteType](../../aspose.words.notes/footnotetype/), string, string*) | Inserta una nota al pie o una nota final en el documento. |
| [InsertForms2OleControl](../../aspose.words/documentbuilder/insertforms2olecontrol/)(*[Forms2OleControl](../../aspose.words.drawing.ole/forms2olecontrol/)*) | Inserciones[`Forms2OleControl`](../../aspose.words.drawing.ole/forms2olecontrol/) objeto en la posición actual. |
| [InsertGroupShape](../../aspose.words/documentbuilder/insertgroupshape/#insertgroupshape)(*params ShapeBase[]*) | Agrupa las formas pasadas como parámetro en un nuevo nodo GroupShape que se inserta en la posición actual. |
| [InsertGroupShape](../../aspose.words/documentbuilder/insertgroupshape/#insertgroupshape_1)(*double, double, double, double, params ShapeBase[]*) | Agrupa las formas pasadas como parámetro en un nuevo nodo GroupShape del tamaño especificado que se inserta en la posición especificada. |
| [InsertHorizontalRule](../../aspose.words/documentbuilder/inserthorizontalrule/)() | Inserta una forma de regla horizontal en el documento. |
| [InsertHtml](../../aspose.words/documentbuilder/inserthtml/#inserthtml)(*string*) | Inserta una cadena HTML en el documento. |
| [InsertHtml](../../aspose.words/documentbuilder/inserthtml/#inserthtml_2)(*string, bool*) | Inserta una cadena HTML en el documento. |
| [InsertHtml](../../aspose.words/documentbuilder/inserthtml/#inserthtml_1)(*string, [HtmlInsertOptions](../htmlinsertoptions/)*) | Inserta una cadena HTML en el documento. Permite especificar opciones adicionales. |
| [InsertHyperlink](../../aspose.words/documentbuilder/inserthyperlink/)(*string, string, bool*) | Inserta un hipervínculo en el documento. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage)(*byte[]*) | Inserta una imagen de una matriz de bytes en el documento. La imagen se inserta en línea y a una escala del 100%. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_3)(*Image*) | Inserta una imagen desde un .NETImage Objeto en el documento. La imagen se inserta en línea y a escala del 100 %. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_6)(*Stream*) | Inserta una imagen de una secuencia en el documento. La imagen se inserta en línea y a una escala del 100%. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_9)(*string*) | Inserta una imagen desde un archivo o URL en el documento. La imagen se inserta en línea y a una escala del 100%. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_2)(*byte[], double, double*) | Inserta una imagen en línea desde una matriz de bytes en el documento y la escala al tamaño especificado. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_5)(*Image, double, double*) | Inserta una imagen en línea desde un .NETImage objeto en el documento y lo escala al tamaño especificado. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_8)(*Stream, double, double*) | Inserta una imagen en línea desde una secuencia en el documento y la escala al tamaño especificado. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_11)(*string, double, double*) | Inserta una imagen en línea desde un archivo o URL en el documento y la escala al tamaño especificado. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_1)(*byte[], [RelativeHorizontalPosition](../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../aspose.words.drawing/relativeverticalposition/), double, double, double, [WrapType](../../aspose.words.drawing/wraptype/)*) | Inserta una imagen de una matriz de bytes en la posición y tamaño especificados. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_4)(*Image, [RelativeHorizontalPosition](../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../aspose.words.drawing/relativeverticalposition/), double, double, double, [WrapType](../../aspose.words.drawing/wraptype/)*) | Inserta una imagen desde un .NETImage objeto en la posición y tamaño especificados. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_7)(*Stream, [RelativeHorizontalPosition](../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../aspose.words.drawing/relativeverticalposition/), double, double, double, [WrapType](../../aspose.words.drawing/wraptype/)*) | Inserta una imagen desde una secuencia en la posición y tamaño especificados. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_10)(*string, [RelativeHorizontalPosition](../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../aspose.words.drawing/relativeverticalposition/), double, double, double, [WrapType](../../aspose.words.drawing/wraptype/)*) | Inserta una imagen desde un archivo o URL en la posición y tamaño especificados. |
| [InsertNode](../../aspose.words/documentbuilder/insertnode/)(*[Node](../node/)*) | Inserta un nodo antes del cursor. |
| [InsertOleObject](../../aspose.words/documentbuilder/insertoleobject/#insertoleobject)(*Stream, string, bool, Stream*) | Inserta un objeto OLE incrustado desde una secuencia en el documento. |
| [InsertOleObject](../../aspose.words/documentbuilder/insertoleobject/#insertoleobject_1)(*string, bool, bool, Stream*) | Inserta un objeto OLE incrustado o vinculado desde un archivo en el documento. Detecta el tipo de objeto OLE mediante la extensión del archivo. |
| [InsertOleObject](../../aspose.words/documentbuilder/insertoleobject/#insertoleobject_2)(*string, string, bool, bool, Stream*) | Inserta un objeto OLE incrustado o vinculado desde un archivo en el documento. Detecta el tipo de objeto OLE mediante el parámetro progID especificado. |
| [InsertOleObjectAsIcon](../../aspose.words/documentbuilder/insertoleobjectasicon/#insertoleobjectasicon)(*Stream, string, string, string*) | Inserta un objeto OLE incrustado como icono desde una secuencia en el documento. Permite especificar el archivo y el título del icono. Detecta el tipo de objeto OLE mediante el parámetro progID especificado. |
| [InsertOleObjectAsIcon](../../aspose.words/documentbuilder/insertoleobjectasicon/#insertoleobjectasicon_1)(*string, bool, string, string*) | Inserta un objeto OLE incrustado o vinculado como icono en el documento. Permite especificar el archivo y el título del icono. Detecta el tipo de objeto OLE mediante la extensión del archivo. |
| [InsertOleObjectAsIcon](../../aspose.words/documentbuilder/insertoleobjectasicon/#insertoleobjectasicon_2)(*string, string, bool, string, string*) | Inserta un objeto OLE incrustado o vinculado como icono en el documento. Permite especificar el archivo y el título del icono. Detecta el tipo de objeto OLE mediante el parámetro progID especificado. |
| [InsertOnlineVideo](../../aspose.words/documentbuilder/insertonlinevideo/#insertonlinevideo_1)(*string, double, double*) | Inserta un objeto de vídeo en línea en el documento y lo escala al tamaño especificado. |
| [InsertOnlineVideo](../../aspose.words/documentbuilder/insertonlinevideo/#insertonlinevideo_3)(*string, string, byte[], double, double*) | Inserta un objeto de vídeo en línea en el documento y lo escala al tamaño especificado. |
| [InsertOnlineVideo](../../aspose.words/documentbuilder/insertonlinevideo/#insertonlinevideo)(*string, [RelativeHorizontalPosition](../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../aspose.words.drawing/relativeverticalposition/), double, double, double, [WrapType](../../aspose.words.drawing/wraptype/)*) | Inserta un objeto de vídeo en línea en el documento y lo escala al tamaño especificado. |
| [InsertOnlineVideo](../../aspose.words/documentbuilder/insertonlinevideo/#insertonlinevideo_2)(*string, string, byte[], [RelativeHorizontalPosition](../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../aspose.words.drawing/relativeverticalposition/), double, double, double, [WrapType](../../aspose.words.drawing/wraptype/)*) | Inserta un objeto de vídeo en línea en el documento y lo escala al tamaño especificado. |
| [InsertParagraph](../../aspose.words/documentbuilder/insertparagraph/)() | Inserta un salto de párrafo en el documento. |
| [InsertShape](../../aspose.words/documentbuilder/insertshape/#insertshape_1)(*[ShapeType](../../aspose.words.drawing/shapetype/), double, double*) | Inserta una forma en línea con el tipo y tamaño especificados. |
| [InsertShape](../../aspose.words/documentbuilder/insertshape/#insertshape)(*[ShapeType](../../aspose.words.drawing/shapetype/), [RelativeHorizontalPosition](../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../aspose.words.drawing/relativeverticalposition/), double, double, double, [WrapType](../../aspose.words.drawing/wraptype/)*) | Inserta una forma flotante con la posición, el tamaño y el tipo de ajuste de texto especificados. |
| [InsertSignatureLine](../../aspose.words/documentbuilder/insertsignatureline/#insertsignatureline)(*[SignatureLineOptions](../signaturelineoptions/)*) | Inserta una línea de firma en la posición actual. |
| [InsertSignatureLine](../../aspose.words/documentbuilder/insertsignatureline/#insertsignatureline_1)(*[SignatureLineOptions](../signaturelineoptions/), [RelativeHorizontalPosition](../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../aspose.words.drawing/relativeverticalposition/), double, [WrapType](../../aspose.words.drawing/wraptype/)*) | Inserta una línea de firma en la posición especificada. |
| [InsertStructuredDocumentTag](../../aspose.words/documentbuilder/insertstructureddocumenttag/)(*[SdtType](../../aspose.words.markup/sdttype/)*) | Inserta un[`StructuredDocumentTag`](../../aspose.words.markup/structureddocumenttag/) en el documento. |
| [InsertStyleSeparator](../../aspose.words/documentbuilder/insertstyleseparator/)() | Inserta un separador de estilo en el documento. |
| [InsertTableOfContents](../../aspose.words/documentbuilder/inserttableofcontents/)(*string*) | Inserta un campo TOC (tabla de contenidos) en el documento. |
| [InsertTextInput](../../aspose.words/documentbuilder/inserttextinput/)(*string, [TextFormFieldType](../../aspose.words.fields/textformfieldtype/), string, string, int*) | Inserta un campo de formulario de texto en la posición actual. |
| [MoveTo](../../aspose.words/documentbuilder/moveto/)(*[Node](../node/)*) | Mueve el cursor a un nodo en línea o al final de un párrafo. |
| [MoveToBookmark](../../aspose.words/documentbuilder/movetobookmark/#movetobookmark)(*string*) | Mueve el cursor a un marcador. |
| [MoveToBookmark](../../aspose.words/documentbuilder/movetobookmark/#movetobookmark_1)(*string, bool, bool*) | Mueve el cursor a un marcador con mayor precisión. |
| [MoveToCell](../../aspose.words/documentbuilder/movetocell/)(*int, int, int, int*) | Mueve el cursor a una celda de la tabla en la sección actual. |
| [MoveToDocumentEnd](../../aspose.words/documentbuilder/movetodocumentend/)() | Mueve el cursor al final del documento. |
| [MoveToDocumentStart](../../aspose.words/documentbuilder/movetodocumentstart/)() | Mueve el cursor al principio del documento. |
| [MoveToField](../../aspose.words/documentbuilder/movetofield/)(*[Field](../../aspose.words.fields/field/), bool*) | Mueve el cursor a un campo en el documento. |
| [MoveToHeaderFooter](../../aspose.words/documentbuilder/movetoheaderfooter/)(*[HeaderFooterType](../headerfootertype/)*) | Mueve el cursor al comienzo de un encabezado o pie de página en la sección actual. |
| [MoveToMergeField](../../aspose.words/documentbuilder/movetomergefield/#movetomergefield)(*string*) | Mueve el cursor a una posición justo más allá del campo de combinación especificado y elimina el campo de combinación. |
| [MoveToMergeField](../../aspose.words/documentbuilder/movetomergefield/#movetomergefield_1)(*string, bool, bool*) | Mueve el campo de combinación al campo de combinación especificado. |
| [MoveToParagraph](../../aspose.words/documentbuilder/movetoparagraph/)(*int, int*) | Mueve el cursor a un párrafo en la sección actual. |
| [MoveToSection](../../aspose.words/documentbuilder/movetosection/)(*int*) | Mueve el cursor al principio del cuerpo en una sección especificada. |
| [MoveToStructuredDocumentTag](../../aspose.words/documentbuilder/movetostructureddocumenttag/#movetostructureddocumenttag_1)(*int, int*) | Mueve el cursor a una etiqueta de documento estructurado en la sección actual. |
| [MoveToStructuredDocumentTag](../../aspose.words/documentbuilder/movetostructureddocumenttag/#movetostructureddocumenttag)(*[StructuredDocumentTag](../../aspose.words.markup/structureddocumenttag/), int*) | Mueve el cursor a la etiqueta del documento estructurado. |
| [PopFont](../../aspose.words/documentbuilder/popfont/)() | Recupera el formato de carácter previamente guardado en la pila. |
| [PushFont](../../aspose.words/documentbuilder/pushfont/)() | Guarda el formato de carácter actual en la pila. |
| [StartBookmark](../../aspose.words/documentbuilder/startbookmark/)(*string*) | Marca la posición actual en el documento como inicio de marcador. |
| [StartColumnBookmark](../../aspose.words/documentbuilder/startcolumnbookmark/)(*string*) | Marca la posición actual en el documento como inicio de marcador de columna. La posición debe estar en una celda de tabla. |
| [StartEditableRange](../../aspose.words/documentbuilder/starteditablerange/)() | Marca la posición actual en el documento como inicio de rango editable. |
| [StartTable](../../aspose.words/documentbuilder/starttable/)() | Inicia una tabla en el documento. |
| [Write](../../aspose.words/documentbuilder/write/)(*string*) | Inserta una cadena en el documento en la posición de inserción actual. |
| [Writeln](../../aspose.words/documentbuilder/writeln/#writeln)() | Inserta un salto de párrafo en el documento. |
| [Writeln](../../aspose.words/documentbuilder/writeln/#writeln_1)(*string*) | Inserta una cadena y un salto de párrafo en el documento. |

## Observaciones

`DocumentBuilder` hace que el proceso de construcción de una[`Document`](../document/) más fácil. [`Document`](../document/) es un objeto compuesto que consiste en un árbol de nodos y, si bien es posible insertar nodos content directamente en el árbol, se requiere una buena comprensión de la estructura del árbol. `DocumentBuilder` es una "fachada" para la compleja estructura de[`Document`](../document/) y permite a insertar contenido y formato de forma rápida y sencilla.

Crear una`DocumentBuilder` y asociarlo con un[`Document`](../document/).

El`DocumentBuilder` tiene un cursor interno donde se insertará el texto cuando llames[`Write`](./write/) ,[`Writeln`](./writeln/) ,[`InsertBreak`](./insertbreak/) y otros métodos. Puedes navegar por el`DocumentBuilder` cursor a una ubicación diferente en un documento usando varios métodos MoveToXXX.

Utilice el[`Font`](./font/) propiedad para especificar el formato de caracteres que se aplicará a todo el texto insertado desde la posición actual en el documento en adelante.

Utilice el[`ParagraphFormat`](./paragraphformat/) propiedad para especificar el formato de párrafo para current y todos los párrafos que se insertarán.

Utilice el[`PageSetup`](./pagesetup/) propiedad para especificar las propiedades de página y sección para la sección current y todas las secciones que se insertarán.

Utilice el[`CellFormat`](./cellformat/) y[`RowFormat`](./rowformat/) Propiedades para especificar las propiedades de formato x000d_ para celdas y filas de la tabla. Utilice[`InsertCell`](./insertcell/) y [`EndRow`](./endrow/) métodos para construir una tabla.

Tenga en cuenta que[`Font`](./font/) ,[`ParagraphFormat`](./paragraphformat/) y[`PageSetup`](./pagesetup/) Las propiedades se actualizan cada vez que navega a un lugar diferente en el documento para reflejar las propiedades de formato disponibles en la nueva ubicación.

## Ejemplos

Muestra cómo utilizar un generador de documentos para crear una tabla.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inicie la tabla y luego rellene la primera fila con dos celdas.
builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, Cell 1.");
builder.InsertCell();
builder.Write("Row 1, Cell 2.");

// Llame al método "EndRow" del constructor para comenzar una nueva fila.
builder.EndRow();
builder.InsertCell();
builder.Write("Row 2, Cell 1.");
builder.InsertCell();
builder.Write("Row 2, Cell 2.");
builder.EndTable();

doc.Save(ArtifactsDir + "DocumentBuilder.CreateTable.docx");
```

Muestra cómo crear encabezados y pies de página en un documento utilizando DocumentBuilder.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Especificamos que queremos encabezados y pies de página diferentes para la primera página, páginas pares e impares.
builder.PageSetup.DifferentFirstPageHeaderFooter = true;
builder.PageSetup.OddAndEvenPagesHeaderFooter = true;

// Cree los encabezados y luego agregue tres páginas al documento para mostrar cada tipo de encabezado.
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

// Configuración de opciones de formato de tabla para un generador de documentos
// los aplicará a cada fila y celda que agreguemos.
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

//Cambiar el formato se aplicará a la celda actual,
// y cualquier celda nueva que creemos con el constructor posteriormente.
//Esto no afectará las celdas que hemos agregado previamente.
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
