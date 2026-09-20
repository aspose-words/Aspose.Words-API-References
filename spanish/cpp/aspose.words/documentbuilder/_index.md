---
title: "Aspose::Words::DocumentBuilder clase"
linktitle: "DocumentBuilder"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::DocumentBuilder clase. Proporciona métodos para insertar texto, imágenes y otro contenido, especificar la fuente, el formato de párrafo y de sección. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 22000
url: /es/cpp/aspose.words/documentbuilder/
---
## DocumentBuilder class


Proporciona métodos para insertar texto, imágenes y otro contenido, especificar la fuente, el formato de párrafo y de sección. Para obtener más información, visite el artículo de documentación [Document Builder Overview](https://docs.aspose.com/words/cpp/document-builder-overview/).

```cpp
class DocumentBuilder : public Aspose::Words::IRunAttrSource,
                        public Aspose::Words::IParaAttrSource,
                        public Aspose::Words::IRowAttrSource,
                        public Aspose::Words::ICellAttrSource
```

## Métodos

| Método | Descripción |
| --- | --- |
| [DeleteRow](./deleterow/)(int32_t, int32_t) | Elimina una fila de una tabla. |
| [DocumentBuilder](./documentbuilder/)() | Inicializa una nueva instancia de esta clase. |
| [DocumentBuilder](./documentbuilder/)(const System::SharedPtr\<Aspose::Words::DocumentBuilderOptions\>\&) | Inicializa una nueva instancia de esta clase. |
| [DocumentBuilder](./documentbuilder/)(const System::SharedPtr\<Aspose::Words::Document\>\&) | Inicializa una nueva instancia de esta clase. |
| [DocumentBuilder](./documentbuilder/)(const System::SharedPtr\<Aspose::Words::Document\>\&, const System::SharedPtr\<Aspose::Words::DocumentBuilderOptions\>\&) | Inicializa una nueva instancia de esta clase. |
| [EndBookmark](./endbookmark/)(const System::String\&) | Marca la posición actual en el documento como el final de un marcador. |
| [EndColumnBookmark](./endcolumnbookmark/)(const System::String\&) | Marca la posición actual en el documento como el final de un marcador de columna. La posición debe estar en una celda de tabla. |
| [EndEditableRange](./endeditablerange/)() | Marca la posición actual en el documento como el final de un rango editable. |
| [EndEditableRange](./endeditablerange/)(const System::SharedPtr\<Aspose::Words::EditableRangeStart\>\&) | Marca la posición actual en el documento como el final de un rango editable. |
| [EndRow](./endrow/)() | Finaliza una fila de tabla en el documento. |
| [EndTable](./endtable/)() | Finaliza una tabla en el documento. |
| [get_Bold](./get_bold/)() | Verdadero si la fuente está formateada en negrita. |
| [get_CellFormat](./get_cellformat/)() | Devuelve un objeto que representa las propiedades de formato de la celda de tabla actual. |
| [get_CurrentNode](./get_currentnode/)() | Obtiene el nodo que está actualmente seleccionado en este [DocumentBuilder](./). |
| [get_CurrentParagraph](./get_currentparagraph/)() | Obtiene el párrafo que está actualmente seleccionado en este [DocumentBuilder](./). |
| [get_CurrentSection](./get_currentsection/)() | Obtiene la sección que está actualmente seleccionada en este [DocumentBuilder](./). |
| [get_CurrentStory](./get_currentstory/)() | Obtiene la historia que está actualmente seleccionada en este [DocumentBuilder](./). |
| [get_CurrentStructuredDocumentTag](./get_currentstructureddocumenttag/)() | Obtiene la etiqueta de documento estructurado que está actualmente seleccionada en este [DocumentBuilder](./). |
| [get_Document](./get_document/)() const | Obtiene o establece el objeto [Document](./get_document/) al que está adjunto este objeto. |
| [get_Font](./get_font/)() | Devuelve un objeto que representa las propiedades de formato de fuente actuales. |
| [get_IsAtEndOfParagraph](./get_isatendofparagraph/)() | Devuelve **true** si el cursor está al final del párrafo actual. |
| [get_IsAtEndOfStructuredDocumentTag](./get_isatendofstructureddocumenttag/)() | Devuelve **true** si el cursor está al final de una etiqueta de documento estructurado. |
| [get_IsAtStartOfParagraph](./get_isatstartofparagraph/)() | Devuelve **true** si el cursor está al principio del párrafo actual (no hay texto antes del cursor). |
| [get_Italic](./get_italic/)() | True si la fuente está formateada en cursiva. |
| [get_ListFormat](./get_listformat/)() | Devuelve un objeto que representa las propiedades de formato de lista actuales. |
| [get_PageSetup](./get_pagesetup/)() | Devuelve un objeto que representa la configuración de página y las propiedades de sección actuales. |
| [get_ParagraphFormat](./get_paragraphformat/)() | Devuelve un objeto que representa las propiedades de formato de párrafo actuales. |
| [get_RowFormat](./get_rowformat/)() | Devuelve un objeto que representa las propiedades de formato de fila de tabla actuales. |
| [get_Underline](./get_underline/)() | Obtiene/establece el tipo de subrayado para la fuente actual. |
| [GetType](./gettype/)() const override |  |
| [InsertBreak](./insertbreak/)(Aspose::Words::BreakType) | Inserta un salto del tipo especificado en el documento. |
| [InsertCell](./insertcell/)() | Inserta una celda de tabla en el documento. |
| [InsertChart](./insertchart/)(Aspose::Words::Drawing::Charts::ChartType, double, double) | Inserta un objeto de gráfico en el documento y lo escala al tamaño especificado. |
| [InsertChart](./insertchart/)(Aspose::Words::Drawing::Charts::ChartType, double, double, Aspose::Words::Drawing::Charts::ChartStyle) | Inserta un objeto de gráfico en el documento y lo escala al tamaño especificado. |
| [InsertChart](./insertchart/)(Aspose::Words::Drawing::Charts::ChartType, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) | Inserta un objeto de gráfico en el documento y lo escala al tamaño especificado. |
| [InsertChart](./insertchart/)(Aspose::Words::Drawing::Charts::ChartType, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType, Aspose::Words::Drawing::Charts::ChartStyle) | Inserta un objeto de gráfico en el documento y lo escala al tamaño especificado. |
| [InsertCheckBox](./insertcheckbox/)(const System::String\&, bool, int32_t) | Inserta un campo de formulario de casilla de verificación en la posición actual. |
| [InsertCheckBox](./insertcheckbox/)(const System::String\&, bool, bool, int32_t) | Inserta un campo de formulario de casilla de verificación en la posición actual. |
| [InsertComboBox](./insertcombobox/)(const System::String\&, const System::ArrayPtr\<System::String\>\&, int32_t) | Inserta un campo de formulario de cuadro combinado en la posición actual. |
| [InsertDocument](./insertdocument/)(const System::SharedPtr\<Aspose::Words::Document\>\&, Aspose::Words::ImportFormatMode) | Inserta un documento en la posición del cursor. |
| [InsertDocument](./insertdocument/)(const System::SharedPtr\<Aspose::Words::Document\>\&, Aspose::Words::ImportFormatMode, const System::SharedPtr\<Aspose::Words::ImportFormatOptions\>\&) | Inserta un documento en la posición del cursor. |
| [InsertDocumentInline](./insertdocumentinline/)(const System::SharedPtr\<Aspose::Words::Document\>\&, Aspose::Words::ImportFormatMode, const System::SharedPtr\<Aspose::Words::ImportFormatOptions\>\&) | Inserta un documento en línea en la posición del cursor. |
| [InsertField](./insertfield/)(Aspose::Words::Fields::FieldType, bool) | Inserta un campo de Word en un documento y opcionalmente actualiza el resultado del campo. |
| [InsertField](./insertfield/)(const System::String\&) | Inserta un campo de Word en un documento y actualiza el resultado del campo. |
| [InsertField](./insertfield/)(const System::String\&, const System::String\&) | Inserta un campo de Word en un documento sin actualizar el resultado del campo. |
| [InsertFootnote](./insertfootnote/)(Aspose::Words::Notes::FootnoteType, const System::String\&) | Inserta una nota al pie o una nota final en el documento. |
| [InsertFootnote](./insertfootnote/)(Aspose::Words::Notes::FootnoteType, const System::String\&, const System::String\&) | Inserta una nota al pie o una nota final en el documento. |
| [InsertForms2OleControl](./insertforms2olecontrol/)(const System::SharedPtr\<Aspose::Words::Drawing::Ole::Forms2OleControl\>\&) | Inserta el objeto [Forms2OleControl](../) en la posición actual. |
| [InsertGroupShape](./insertgroupshape/)(const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Drawing::ShapeBase\>\>\&) | Agrupa las formas pasadas como parámetro en un nuevo nodo GroupShape que se inserta en la posición actual. |
| [InsertGroupShape](./insertgroupshape/)(double, double, double, double, const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Drawing::ShapeBase\>\>\&) | Agrupa las formas pasadas como parámetro en un nuevo nodo GroupShape del tamaño especificado que se inserta en la posición especificada. |
| [InsertHorizontalRule](./inserthorizontalrule/)() | Inserta una forma de regla horizontal en el documento. |
| [InsertHtml](./inserthtml/)(const System::String\&) | Inserta una cadena HTML en el documento. |
| [InsertHtml](./inserthtml/)(const System::String\&, bool) | Inserta una cadena HTML en el documento. |
| [InsertHtml](./inserthtml/)(const System::String\&, Aspose::Words::HtmlInsertOptions) | Inserta una cadena HTML en el documento. Permite especificar opciones adicionales. |
| [InsertHyperlink](./inserthyperlink/)(const System::String\&, const System::String\&, bool) | Inserta un hipervínculo en el documento. |
| [InsertImage](./insertimage/)(const System::SharedPtr\<System::Drawing::Image\>\&) | Inserta una imagen desde un objeto **Image** en el documento. La imagen se inserta en línea y al 100 % de escala. |
| [InsertImage](./insertimage/)(const System::String\&) | Inserta una imagen desde un archivo o URL en el documento. La imagen se inserta en línea y al 100 % de escala. |
| [InsertImage](./insertimage/)(const System::SharedPtr\<System::IO::Stream\>\&) | Inserta una imagen desde un flujo en el documento. La imagen se inserta en línea y al 100 % de escala. |
| [InsertImage](./insertimage/)(const System::ArrayPtr\<uint8_t\>\&) | Inserta una imagen desde una matriz de bytes en el documento. La imagen se inserta en línea y al 100 % de escala. |
| [InsertImage](./insertimage/)(const System::SharedPtr\<System::Drawing::Image\>\&, double, double) | Inserta una imagen en línea desde un objeto **Image** en el documento y la escala al tamaño especificado. |
| [InsertImage](./insertimage/)(const System::String\&, double, double) | Inserta una imagen en línea desde un archivo o URL en el documento y la escala al tamaño especificado. |
| [InsertImage](./insertimage/)(const System::SharedPtr\<System::IO::Stream\>\&, double, double) | Inserta una imagen en línea desde un flujo en el documento y la escala al tamaño especificado. |
| [InsertImage](./insertimage/)(const System::ArrayPtr\<uint8_t\>\&, double, double) | Inserta una imagen en línea desde una matriz de bytes en el documento y la escala al tamaño especificado. |
| [InsertImage](./insertimage/)(const System::SharedPtr\<System::Drawing::Image\>\&, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) | Inserta una imagen desde un objeto **Image** en la posición y tamaño especificados. |
| [InsertImage](./insertimage/)(const System::String\&, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) | Inserta una imagen desde un archivo o URL en la posición y tamaño especificados. |
| [InsertImage](./insertimage/)(const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) | Inserta una imagen desde un flujo en la posición y tamaño especificados. |
| [InsertImage](./insertimage/)(const System::ArrayPtr\<uint8_t\>\&, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) | Inserta una imagen desde una matriz de bytes en la posición y tamaño especificados. |
| [InsertImage](./insertimage/)(std::basic_istream\<CharType, Traits\>\&) |  |
| [InsertImage](./insertimage/)(std::basic_istream\<CharType, Traits\>\&, double, double) |  |
| [InsertImage](./insertimage/)(std::basic_istream\<CharType, Traits\>\&, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) |  |
| [InsertNode](./insertnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Inserta un nodo antes del cursor. |
| [InsertOleObject](./insertoleobject/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::String\&, bool, const System::SharedPtr\<System::IO::Stream\>\&) | Inserta un objeto OLE incrustado desde un flujo en el documento. |
| [InsertOleObject](./insertoleobject/)(const System::String\&, bool, bool, const System::SharedPtr\<System::IO::Stream\>\&) | Inserta un objeto OLE incrustado o vinculado desde un archivo en el documento. Detecta el tipo de objeto OLE usando la extensión del archivo. |
| [InsertOleObject](./insertoleobject/)(const System::String\&, const System::String\&, bool, bool, const System::SharedPtr\<System::IO::Stream\>\&) | Inserta un objeto OLE incrustado o vinculado desde un archivo en el documento. Detecta el tipo de objeto OLE usando el parámetro progID proporcionado. |
| [InsertOleObject](./insertoleobject/)(std::basic_istream\<CharType, Traits\>\&, System::String, bool, std::basic_istream\<CharType, Traits\>\&) |  |
| [InsertOleObject](./insertoleobject/)(System::String, bool, bool, std::basic_istream\<CharType, Traits\>\&) |  |
| [InsertOleObject](./insertoleobject/)(System::String, System::String, bool, bool, std::basic_istream\<CharType, Traits\>\&) |  |
| [InsertOleObjectAsIcon](./insertoleobjectasicon/)(const System::String\&, bool, const System::String\&, const System::String\&) | Inserta un objeto OLE incrustado o vinculado como ícono en el documento. Permite especificar el archivo de ícono y el título. Detecta el tipo de objeto OLE usando la extensión del archivo. |
| [InsertOleObjectAsIcon](./insertoleobjectasicon/)(const System::String\&, const System::String\&, bool, const System::String\&, const System::String\&) | Inserta un objeto OLE incrustado o vinculado como ícono en el documento. Permite especificar el archivo de ícono y el título. Detecta el tipo de objeto OLE usando el parámetro progID proporcionado. |
| [InsertOleObjectAsIcon](./insertoleobjectasicon/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::String\&, const System::String\&, const System::String\&) | Inserta un objeto OLE incrustado como ícono desde un flujo en el documento. Permite especificar el archivo de ícono y el título. Detecta el tipo de objeto OLE usando el parámetro progID proporcionado. |
| [InsertOleObjectAsIcon](./insertoleobjectasicon/)(std::basic_istream\<CharType, Traits\>\&, System::String, System::String, System::String) |  |
| [InsertOnlineVideo](./insertonlinevideo/)(const System::String\&, double, double) | Inserta un objeto de video en línea en el documento y lo escala al tamaño especificado. |
| [InsertOnlineVideo](./insertonlinevideo/)(const System::String\&, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) | Inserta un objeto de video en línea en el documento y lo escala al tamaño especificado. |
| [InsertOnlineVideo](./insertonlinevideo/)(const System::String\&, const System::String\&, const System::ArrayPtr\<uint8_t\>\&, double, double) | Inserta un objeto de video en línea en el documento y lo escala al tamaño especificado. |
| [InsertOnlineVideo](./insertonlinevideo/)(const System::String\&, const System::String\&, const System::ArrayPtr\<uint8_t\>\&, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) | Inserta un objeto de video en línea en el documento y lo escala al tamaño especificado. |
| [InsertParagraph](./insertparagraph/)() | Inserta un salto de párrafo en el documento. |
| [InsertShape](./insertshape/)(Aspose::Words::Drawing::ShapeType, double, double) | Inserta una forma en línea con el tipo y tamaño especificados. |
| [InsertShape](./insertshape/)(Aspose::Words::Drawing::ShapeType, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) | Inserta una forma flotante libre con la posición, tamaño y tipo de ajuste de texto especificados. |
| [InsertSignatureLine](./insertsignatureline/)(const System::SharedPtr\<Aspose::Words::SignatureLineOptions\>\&) | Inserta una línea de firma en la posición actual. |
| [InsertSignatureLine](./insertsignatureline/)(const System::SharedPtr\<Aspose::Words::SignatureLineOptions\>\&, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, Aspose::Words::Drawing::WrapType) | Inserta una línea de firma en la posición especificada. |
| [InsertStructuredDocumentTag](./insertstructureddocumenttag/)(Aspose::Words::Markup::SdtType) | Inserta un [StructuredDocumentTag](../../aspose.words.markup/structureddocumenttag/) en el documento. |
| [InsertStyleSeparator](./insertstyleseparator/)() | Inserta un separador de estilo en el documento. |
| [InsertTableOfContents](./inserttableofcontents/)(const System::String\&) | Inserta un campo TOC (tabla de contenido) en el documento. |
| [InsertTextInput](./inserttextinput/)(const System::String\&, Aspose::Words::Fields::TextFormFieldType, const System::String\&, const System::String\&, int32_t) | Inserta un campo de formulario de texto en la posición actual. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [MoveTo](./moveto/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Mueve el cursor a un nodo en línea o al final de un párrafo. |
| [MoveToBookmark](./movetobookmark/)(const System::String\&) | Mueve el cursor a un marcador. |
| [MoveToBookmark](./movetobookmark/)(const System::String\&, bool, bool) | Mueve el cursor a un marcador con mayor precisión. |
| [MoveToCell](./movetocell/)(int32_t, int32_t, int32_t, int32_t) | Mueve el cursor a una celda de tabla en la sección actual. |
| [MoveToDocumentEnd](./movetodocumentend/)() | Mueve el cursor al final del documento. |
| [MoveToDocumentStart](./movetodocumentstart/)() | Mueve el cursor al comienzo del documento. |
| [MoveToField](./movetofield/)(const System::SharedPtr\<Aspose::Words::Fields::Field\>\&, bool) | Mueve el cursor a un campo en el documento. |
| [MoveToHeaderFooter](./movetoheaderfooter/)(Aspose::Words::HeaderFooterType) | Mueve el cursor al comienzo de un encabezado o pie de página en la sección actual. |
| [MoveToMergeField](./movetomergefield/)(const System::String\&) | Mueve el cursor a una posición justo después del campo de combinación especificado y elimina el campo de combinación. |
| [MoveToMergeField](./movetomergefield/)(const System::String\&, bool, bool) | Mueve el campo de combinación al campo de combinación especificado. |
| [MoveToParagraph](./movetoparagraph/)(int32_t, int32_t) | Mueve el cursor a un párrafo en la sección actual. |
| [MoveToSection](./movetosection/)(int32_t) | Mueve el cursor al comienzo del cuerpo en una sección especificada. |
| [MoveToStructuredDocumentTag](./movetostructureddocumenttag/)(int32_t, int32_t) | Mueve el cursor a una etiqueta de documento estructurado en la sección actual. |
| [MoveToStructuredDocumentTag](./movetostructureddocumenttag/)(const System::SharedPtr\<Aspose::Words::Markup::StructuredDocumentTag\>\&, int32_t) | Mueve el cursor a la etiqueta de documento estructurado. |
| [PopFont](./popfont/)() | Recupera el formato de carácter guardado previamente en la pila. |
| [PushFont](./pushfont/)() | Guarda el formato de carácter actual en la pila. |
| [set_Bold](./set_bold/)(bool) | Setter para [Aspose::Words::DocumentBuilder::get_Bold](./get_bold/). |
| [set_Document](./set_document/)(const System::SharedPtr\<Aspose::Words::Document\>\&) | Setter para [Aspose::Words::DocumentBuilder::get_Document](./get_document/). |
| [set_Italic](./set_italic/)(bool) | Setter para [Aspose::Words::DocumentBuilder::get_Italic](./get_italic/). |
| [set_Underline](./set_underline/)(Aspose::Words::Underline) | Establecedor para [Aspose::Words::DocumentBuilder::get_Underline](./get_underline/). |
| [StartBookmark](./startbookmark/)(const System::String\&) | Marca la posición actual en el documento como el inicio de un marcador. |
| [StartColumnBookmark](./startcolumnbookmark/)(const System::String\&) | Marca la posición actual en el documento como el inicio de un marcador de columna. La posición debe estar en una celda de tabla. |
| [StartEditableRange](./starteditablerange/)() | Marca la posición actual en el documento como el inicio de un rango editable. |
| [StartTable](./starttable/)() | Inicia una tabla en el documento. |
| static [Type](./type/)() |  |
| [Write](./write/)(const System::String\&) | Inserta una cadena en el documento en la posición de inserción actual. |
| [Writeln](./writeln/)(const System::String\&) | Inserta una cadena y un salto de párrafo en el documento. |
| [Writeln](./writeln/)() | Inserta un salto de párrafo en el documento. |
## Observaciones


[DocumentBuilder](./) makes the process of building a [Document](../document/) easier. [Document](../document/) is a composite object consisting of a tree of nodes and while inserting content nodes directly into the tree is possible, it requires good understanding of the tree structure. [DocumentBuilder](./) is a "facade" for the complex structure of [Document](../document/) and allows to insert content and formatting quickly and easily.

Crea un [DocumentBuilder](./) y asócialo con un [Document](../document/).

El [DocumentBuilder](./) tiene un cursor interno donde se insertará el texto cuando llames a [Write()](../), [Writeln()](../), [InsertBreak()](./insertbreak/) y otros métodos. Puedes navegar el cursor del [DocumentBuilder](./) a una ubicación diferente en un documento usando varios métodos MoveToXXX.

Utiliza la propiedad [Font](./get_font/) para especificar el formato de caracteres que se aplicará a todo el texto insertado desde la posición actual en el documento en adelante.

Utiliza la propiedad [ParagraphFormat](./get_paragraphformat/) para especificar el formato de párrafo para el actual y todos los párrafos que se insertarán.

Utiliza la propiedad [PageSetup](./get_pagesetup/) para especificar las propiedades de página y sección para la sección actual y todas las secciones que se insertarán.

Utiliza las propiedades [CellFormat](./get_cellformat/) y [RowFormat](./get_rowformat/) para especificar las propiedades de formato de celdas y filas de tabla. Usa los métodos [InsertCell](./insertcell/) y [EndRow](./endrow/) para construir una tabla.

Ten en cuenta que las propiedades [Font](./get_font/), [ParagraphFormat](./get_paragraphformat/) y [PageSetup](./get_pagesetup/) se actualizan cada vez que navegas a un lugar diferente en el documento para reflejar las propiedades de formato disponibles en la nueva ubicación.

## Ejemplos



Muestra cómo crear una tabla con bordes personalizados.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->StartTable();

// Configuración de opciones de formato de tabla para un DocumentBuilder
// se aplicarán a cada fila y celda que añadamos con él.
builder->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);

builder->get_CellFormat()->ClearFormatting();
builder->get_CellFormat()->set_Width(150);
builder->get_CellFormat()->set_VerticalAlignment(Aspose::Words::Tables::CellVerticalAlignment::Center);
builder->get_CellFormat()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_GreenYellow());
builder->get_CellFormat()->set_WrapText(false);
builder->get_CellFormat()->set_FitText(true);

builder->get_RowFormat()->ClearFormatting();
builder->get_RowFormat()->set_HeightRule(Aspose::Words::HeightRule::Exactly);
builder->get_RowFormat()->set_Height(50);
builder->get_RowFormat()->get_Borders()->set_LineStyle(Aspose::Words::LineStyle::Engrave3D);
builder->get_RowFormat()->get_Borders()->set_Color(System::Drawing::Color::get_Orange());

builder->InsertCell();
builder->Write(u"Row 1, Col 1");

builder->InsertCell();
builder->Write(u"Row 1, Col 2");
builder->EndRow();

// Cambiar el formato lo aplicará a la celda actual,
// y a cualquier celda nueva que creemos con el constructor posteriormente.
// Esto no afectará a las celdas que hemos añadido previamente.
builder->get_CellFormat()->get_Shading()->ClearFormatting();

builder->InsertCell();
builder->Write(u"Row 2, Col 1");

builder->InsertCell();
builder->Write(u"Row 2, Col 2");

builder->EndRow();

// Aumenta la altura de la fila para ajustar el texto vertical.
builder->InsertCell();
builder->get_RowFormat()->set_Height(150);
builder->get_CellFormat()->set_Orientation(Aspose::Words::TextOrientation::Upward);
builder->Write(u"Row 3, Col 1");

builder->InsertCell();
builder->get_CellFormat()->set_Orientation(Aspose::Words::TextOrientation::Downward);
builder->Write(u"Row 3, Col 2");

builder->EndRow();
builder->EndTable();

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertTable.docx");
```


Muestra cómo usar un DocumentBuilder para crear una tabla.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Inicia la tabla, luego rellena la primera fila con dos celdas.
builder->StartTable();
builder->InsertCell();
builder->Write(u"Row 1, Cell 1.");
builder->InsertCell();
builder->Write(u"Row 1, Cell 2.");

// Llama al método "EndRow" del constructor para iniciar una nueva fila.
builder->EndRow();
builder->InsertCell();
builder->Write(u"Row 2, Cell 1.");
builder->InsertCell();
builder->Write(u"Row 2, Cell 2.");
builder->EndTable();

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.CreateTable.docx");
```

## Ver también

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
