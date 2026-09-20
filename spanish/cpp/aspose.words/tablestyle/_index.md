---
title: "Clase Aspose::Words::TableStyle"
linktitle: "TableStyle"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Clase Aspose::Words::TableStyle. Representa un estilo de tabla. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 67000
url: /es/cpp/aspose.words/tablestyle/
---
## TableStyle class


Representa un estilo de tabla. Para obtener más información, visite el artículo de documentación [Working with Tables](https://docs.aspose.com/words/cpp/working-with-tables/).

```cpp
class TableStyle : public Aspose::Words::Style,
                   public Aspose::Words::ICellAttrSource,
                   public Aspose::Words::IRowAttrSource,
                   public Aspose::Words::IBorderAttrSource,
                   public Aspose::Words::IShadingAttrSource
```

## Métodos

| Método | Descripción |
| --- | --- |
| [Equals](../style/equals/)(const System::SharedPtr\<Aspose::Words::Style\>\&) | Compara con el estilo especificado. Los Istds de estilos se comparan solo para estilos incorporados. Los valores predeterminados de los estilos no se incluyen en la comparación. El estilo base, el estilo enlazado y el estilo del siguiente párrafo se comparan recursivamente. |
| [get_Aliases](../style/get_aliases/)() | Obtiene todos los alias de este estilo. Si el estilo no tiene alias, se devuelve una matriz vacía de cadenas. |
| [get_Alignment](./get_alignment/)() | Especifica la alineación para el estilo de tabla. |
| [get_AllowBreakAcrossPages](./get_allowbreakacrosspages/)() | Obtiene o establece una bandera que indica si el texto en una fila de tabla puede dividirse a través de un salto de página. |
| [get_AutomaticallyUpdate](../style/get_automaticallyupdate/)() const | Especifica si este estilo se redefine automáticamente según el valor apropiado. |
| [get_BaseStyleName](../style/get_basestylename/)() | Obtiene/establece el nombre del estilo del que se basa este estilo. |
| [get_Borders](./get_borders/)() | Obtiene la colección de bordes de celda predeterminados para el estilo. |
| [get_BottomPadding](./get_bottompadding/)() | Obtiene o establece la cantidad de espacio (en puntos) que se agrega debajo del contenido de las celdas de la tabla. |
| [get_BuiltIn](../style/get_builtin/)() | Verdadero si este estilo es uno de los estilos incorporados en MS Word. |
| [get_CellSpacing](./get_cellspacing/)() | Obtiene o establece la cantidad de espacio (en puntos) entre las celdas. |
| [get_ColumnStripe](./get_columnstripe/)() | Obtiene o establece un número de columnas para incluir en el bandado cuando el estilo especifica bandado de columnas impares/pares. |
| [get_ConditionalStyles](./get_conditionalstyles/)() | Colección de estilos condicionales que pueden definirse para este estilo de tabla. |
| [get_Document](../style/get_document/)() | Obtiene el documento propietario. |
| [get_Font](../style/get_font/)() | Obtiene el formato de caracteres del estilo. |
| [get_IsHeading](../style/get_isheading/)() | Verdadero cuando el estilo es uno de los estilos de encabezado incorporados. |
| [get_IsQuickStyle](../style/get_isquickstyle/)() const | Especifica si este estilo se muestra en la galería rápida de [Style](../style/) dentro de la interfaz de MS Word. |
| [get_LeftIndent](./get_leftindent/)() | Obtiene o establece el valor que representa la sangría izquierda de una tabla. |
| [get_LeftPadding](./get_leftpadding/)() | Obtiene o establece la cantidad de espacio (en puntos) que se agrega a la izquierda del contenido de las celdas de la tabla. |
| [get_LinkedStyleName](../style/get_linkedstylename/)() | Obtiene/establece el nombre del [Style](../style/) vinculado a este. Devuelve una cadena vacía si no hay estilos vinculados. |
| [get_List](../style/get_list/)() | Obtiene la lista que define el formato de este estilo de lista. |
| [get_ListFormat](../style/get_listformat/)() | Proporciona acceso a las propiedades de formato de lista de un estilo de párrafo. |
| [get_Locked](../style/get_locked/)() const | Especifica si este estilo está bloqueado. |
| [get_Name](../style/get_name/)() const | Obtiene o establece el nombre del estilo. |
| [get_NextParagraphStyleName](../style/get_nextparagraphstylename/)() | Obtiene/establece el nombre del estilo que se aplicará automáticamente a un nuevo párrafo insertado después de un párrafo formateado con el estilo especificado. |
| [get_ParagraphFormat](../style/get_paragraphformat/)() | Obtiene el formato de párrafo del estilo. |
| [get_Priority](../style/get_priority/)() const | Obtiene/establece el valor entero que representa la prioridad para ordenar los estilos en el panel de tareas de Estilos. |
| [get_RightPadding](./get_rightpadding/)() | Obtiene o establece la cantidad de espacio (en puntos) que se agrega a la derecha del contenido de las celdas de la tabla. |
| [get_RowStripe](./get_rowstripe/)() | Obtiene o establece un número de filas para incluir en el bandado cuando el estilo especifica bandado de filas impares/pares. |
| [get_SemiHidden](../style/get_semihidden/)() const | Obtiene/establece si el estilo se oculta de la galería de Estilos y del panel de tareas de Estilos. |
| [get_Shading](./get_shading/)() | Obtiene un objeto [Shading](../shading/) que se refiere al formato de sombreado para celdas de tabla. |
| [get_StyleIdentifier](../style/get_styleidentifier/)() const | Obtiene el identificador de estilo independiente de la configuración regional para un estilo incorporado. |
| [get_Styles](../style/get_styles/)() const | Obtiene la colección de estilos a la que pertenece este estilo. |
| [get_TopPadding](./get_toppadding/)() | Obtiene o establece la cantidad de espacio (en puntos) que se agrega encima del contenido de las celdas de la tabla. |
| [get_Type](../style/get_type/)() const | Obtiene el tipo de estilo (párrafo o carácter). |
| [get_UnhideWhenUsed](../style/get_unhidewhenused/)() const | Obtiene/establece si el estilo usado en el documento actual se muestra en la galería de Estilos y en el panel de tareas de Estilos. Verdadero cuando el estilo usado debe mostrarse en la galería de Estilos. |
| [get_VerticalAlignment](./get_verticalalignment/)() | Especifica la alineación vertical para las celdas. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](../style/remove/)() | Elimina el estilo especificado del documento. |
| [set_Alignment](./set_alignment/)(Aspose::Words::Tables::TableAlignment) | Método set para [Aspose::Words::TableStyle::get_Alignment](./get_alignment/). |
| [set_AllowBreakAcrossPages](./set_allowbreakacrosspages/)(bool) | Método set para [Aspose::Words::TableStyle::get_AllowBreakAcrossPages](./get_allowbreakacrosspages/). |
| [set_AutomaticallyUpdate](../style/set_automaticallyupdate/)(bool) | Método set para [Aspose::Words::Style::get_AutomaticallyUpdate](../style/get_automaticallyupdate/). |
| [set_BaseStyleName](../style/set_basestylename/)(const System::String\&) | Método set para [Aspose::Words::Style::get_BaseStyleName](../style/get_basestylename/). |
| [set_BottomPadding](./set_bottompadding/)(double) | Método set para [Aspose::Words::TableStyle::get_BottomPadding](./get_bottompadding/). |
| [set_CellSpacing](./set_cellspacing/)(double) | Método set para [Aspose::Words::TableStyle::get_CellSpacing](./get_cellspacing/). |
| [set_ColumnStripe](./set_columnstripe/)(int32_t) | Método set para [Aspose::Words::TableStyle::get_ColumnStripe](./get_columnstripe/). |
| [set_IsQuickStyle](../style/set_isquickstyle/)(bool) | Método set para [Aspose::Words::Style::get_IsQuickStyle](../style/get_isquickstyle/). |
| [set_LeftIndent](./set_leftindent/)(double) | Método set para [Aspose::Words::TableStyle::get_LeftIndent](./get_leftindent/). |
| [set_LeftPadding](./set_leftpadding/)(double) | Método set para [Aspose::Words::TableStyle::get_LeftPadding](./get_leftpadding/). |
| [set_LinkedStyleName](../style/set_linkedstylename/)(const System::String\&) | Establecedor de [Aspose::Words::Style::get_LinkedStyleName](../style/get_linkedstylename/). |
| [set_Locked](../style/set_locked/)(bool) | Establecedor de [Aspose::Words::Style::get_Locked](../style/get_locked/). |
| [set_Name](../style/set_name/)(const System::String\&) | Establecedor de [Aspose::Words::Style::get_Name](../style/get_name/). |
| [set_NextParagraphStyleName](../style/set_nextparagraphstylename/)(const System::String\&) | Establecedor de [Aspose::Words::Style::get_NextParagraphStyleName](../style/get_nextparagraphstylename/). |
| [set_Priority](../style/set_priority/)(int32_t) | Establecedor de [Aspose::Words::Style::get_Priority](../style/get_priority/). |
| [set_RightPadding](./set_rightpadding/)(double) | Establecedor de [Aspose::Words::TableStyle::get_RightPadding](./get_rightpadding/). |
| [set_RowStripe](./set_rowstripe/)(int32_t) | Establecedor de [Aspose::Words::TableStyle::get_RowStripe](./get_rowstripe/). |
| [set_SemiHidden](../style/set_semihidden/)(bool) | Establecedor de [Aspose::Words::Style::get_SemiHidden](../style/get_semihidden/). |
| [set_TopPadding](./set_toppadding/)(double) | Establecedor de [Aspose::Words::TableStyle::get_TopPadding](./get_toppadding/). |
| [set_UnhideWhenUsed](../style/set_unhidewhenused/)(bool) | Establecedor de [Aspose::Words::Style::get_UnhideWhenUsed](../style/get_unhidewhenused/). |
| [set_VerticalAlignment](./set_verticalalignment/)(Aspose::Words::Tables::CellVerticalAlignment) | Establecedor de [Aspose::Words::TableStyle::get_VerticalAlignment](./get_verticalalignment/). |
| static [Type](./type/)() |  |

## Ejemplos



Muestra cómo crear configuraciones de estilo personalizadas para la tabla.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Name");
builder->InsertCell();
builder->Write(u"مرحبًا");
builder->EndRow();
builder->InsertCell();
builder->InsertCell();
builder->EndTable();

auto tableStyle = System::ExplicitCast<Aspose::Words::TableStyle>(doc->get_Styles()->Add(Aspose::Words::StyleType::Table, u"MyTableStyle1"));
tableStyle->set_AllowBreakAcrossPages(true);
tableStyle->set_CellSpacing(5);
tableStyle->set_BottomPadding(20);
tableStyle->set_LeftPadding(5);
tableStyle->set_RightPadding(10);
tableStyle->set_TopPadding(20);
tableStyle->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_AntiqueWhite());
tableStyle->get_Borders()->set_Color(System::Drawing::Color::get_Blue());
tableStyle->get_Borders()->set_LineStyle(Aspose::Words::LineStyle::DotDash);
tableStyle->set_VerticalAlignment(Aspose::Words::Tables::CellVerticalAlignment::Center);

table->set_Style(tableStyle);

// Establecer las propiedades de estilo de una tabla puede afectar las propiedades de la propia tabla.
ASSERT_FALSE(table->get_Bidi());
ASPOSE_ASSERT_EQ(5.0, table->get_CellSpacing());
ASSERT_EQ(u"MyTableStyle1", table->get_StyleName());

doc->Save(get_ArtifactsDir() + u"Table.TableStyleCreation.docx");
```

## Ver también

* Class [Style](../style/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
