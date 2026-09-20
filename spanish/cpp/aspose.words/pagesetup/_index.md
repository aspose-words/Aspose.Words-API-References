---
title: "Aspose::Words::PageSetup clase"
linktitle: "PageSetup"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::PageSetup clase. Representa las propiedades de configuración de página de una sección. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 46000
url: /es/cpp/aspose.words/pagesetup/
---
## PageSetup class


Representa las propiedades de configuración de página de una sección. Para obtener más información, visite el artículo de documentación [Working with Sections](https://docs.aspose.com/words/cpp/working-with-sections/).

```cpp
class PageSetup : public Aspose::Words::IBorderAttrSource
```

## Métodos

| Método | Descripción |
| --- | --- |
| [ClearFormatting](./clearformatting/)() | Restablece la configuración de página al tamaño de papel, márgenes y orientación predeterminados. |
| [get_Bidi](./get_bidi/)() | Especifica que esta sección contiene texto bidireccional (scripts complejos). |
| [get_BorderAlwaysInFront](./get_borderalwaysinfront/)() | Especifica dónde se posiciona el borde de la página en relación con los textos y objetos que se intersectan. |
| [get_BorderAppliesTo](./get_borderappliesto/)() | Especifica en qué páginas se imprime el borde de la página. |
| [get_BorderDistanceFrom](./get_borderdistancefrom/)() | Obtiene o establece un valor que indica si el borde de página especificado se mide desde el borde de la página o desde el texto que lo rodea. |
| [get_Borders](./get_borders/)() | Obtiene una colección de los bordes de página. |
| [get_BorderSurroundsFooter](./get_bordersurroundsfooter/)() | Especifica si el borde de página incluye o excluye el pie de página. |
| [get_BorderSurroundsHeader](./get_bordersurroundsheader/)() | Especifica si el borde de página incluye o excluye el encabezado. |
| [get_BottomMargin](./get_bottommargin/)() | Devuelve o establece la distancia (en puntos) entre el borde inferior de la página y el límite inferior del texto del cuerpo. |
| [get_ChapterPageSeparator](./get_chapterpageseparator/)() | Obtiene o establece el carácter separador que aparece entre el número de capítulo y el número de página. |
| [get_CharactersPerLine](./get_charactersperline/)() | Obtiene o establece el número de caracteres por línea en la cuadrícula del documento. |
| [get_DifferentFirstPageHeaderFooter](./get_differentfirstpageheaderfooter/)() | Verdadero si se usa un encabezado o pie de página diferente en la primera página. |
| [get_EndnoteOptions](./get_endnoteoptions/)() | Proporciona opciones que controlan la numeración y la posición de las notas finales en esta sección. |
| [get_FirstPageTray](./get_firstpagetray/)() | Obtiene la bandeja de papel (cajón) que se usará para la primera página de una sección. El valor es específico de la implementación (impresora). |
| [get_FooterDistance](./get_footerdistance/)() | Devuelve o establece la distancia (en puntos) entre el pie de página y el borde inferior de la página. |
| [get_FootnoteOptions](./get_footnoteoptions/)() | Proporciona opciones que controlan la numeración y la posición de las notas al pie en esta sección. |
| [get_Gutter](./get_gutter/)() | Obtiene o establece la cantidad de espacio adicional añadido al margen para la encuadernación del documento. |
| [get_HeaderDistance](./get_headerdistance/)() | Devuelve o establece la distancia (en puntos) entre el encabezado y la parte superior de la página. |
| [get_HeadingLevelForChapter](./get_headinglevelforchapter/)() | Obtiene o establece el estilo de nivel de encabezado que se aplica a los títulos de los capítulos en el documento. |
| [get_LayoutMode](./get_layoutmode/)() | Obtiene o establece el modo de diseño de esta sección. |
| [get_LeftMargin](./get_leftmargin/)() | Devuelve o establece la distancia (en puntos) entre el borde izquierdo de la página y el límite izquierdo del texto del cuerpo. |
| [get_LineNumberCountBy](./get_linenumbercountby/)() | Devuelve o establece el incremento numérico para los números de línea. |
| [get_LineNumberDistanceFromText](./get_linenumberdistancefromtext/)() | Obtiene o establece la distancia entre el borde derecho de los números de línea y el borde izquierdo del documento. |
| [get_LineNumberRestartMode](./get_linenumberrestartmode/)() | Obtiene o establece la forma en que se ejecuta la numeración de líneas, es decir, si se reinicia al comienzo de una nueva página o sección o se ejecuta de forma continua. |
| [get_LinesPerPage](./get_linesperpage/)() | Obtiene o establece el número de líneas por página en la cuadrícula del documento. |
| [get_LineStartingNumber](./get_linestartingnumber/)() | Obtiene o establece el número de línea inicial. |
| [get_Margins](./get_margins/)() | Devuelve o establece los [Márgenes](../margins/) predefinidos de la página. |
| [get_MultiplePages](./get_multiplepages/)() const | Para documentos de varias páginas, obtiene o establece cómo se imprime o renderiza un documento para que pueda encuadernarse como folleto. |
| [get_OddAndEvenPagesHeaderFooter](./get_oddandevenpagesheaderfooter/)() const | Verdadero si el documento tiene encabezados y pies de página diferentes para páginas impares y pares. |
| [get_Orientation](./get_orientation/)() | Devuelve o establece la orientación de la página. |
| [get_OtherPagesTray](./get_otherpagestray/)() | Obtiene la bandeja de papel (cajón) que se usará para todas las páginas excepto la primera de una sección. El valor es específico de la implementación (impresora). |
| [get_PageHeight](./get_pageheight/)() | Devuelve o establece la altura de la página en puntos. |
| [get_PageNumberStyle](./get_pagenumberstyle/)() | Obtiene o establece el formato del número de página. |
| [get_PageStartingNumber](./get_pagestartingnumber/)() | Obtiene o establece el número de página inicial de la sección. |
| [get_PageWidth](./get_pagewidth/)() | Devuelve o establece el ancho de la página en puntos. |
| [get_PaperSize](./get_papersize/)() | Devuelve o establece el tamaño del papel. |
| [get_RestartPageNumbering](./get_restartpagenumbering/)() | True si la numeración de páginas se reinicia al comienzo de la sección. |
| [get_RightMargin](./get_rightmargin/)() | Devuelve o establece la distancia (en puntos) entre el borde derecho de la página y el límite derecho del texto del cuerpo. |
| [get_RtlGutter](./get_rtlgutter/)() | Obtiene o establece si Microsoft Word usa gutters para la sección según un idioma de derecha a izquierda o de izquierda a derecha. |
| [get_SectionStart](./get_sectionstart/)() | Devuelve o establece el tipo de salto de sección para el objeto especificado. |
| [get_SheetsPerBooklet](./get_sheetsperbooklet/)() const | Devuelve o establece el número de páginas que se incluirán en cada folleto. |
| [get_SuppressEndnotes](./get_suppressendnotes/)() | True si las notas al final se imprimen al final de la siguiente sección que no suprime notas al final. Las notas al final suprimidas se imprimen antes de las notas al final en esa sección. |
| [get_TextColumns](./get_textcolumns/)() | Devuelve una colección que representa el conjunto de columnas de texto. |
| [get_TextOrientation](./get_textorientation/)() | Permite especificar [TextOrientation](./get_textorientation/) para toda la página. El valor predeterminado es [Horizontal](../textorientation/) |
| [get_TopMargin](./get_topmargin/)() | Devuelve o establece la distancia (en puntos) entre el borde superior de la página y el límite superior del texto del cuerpo. |
| [get_VerticalAlignment](./get_verticalalignment/)() | Devuelve o establece la alineación vertical del texto en cada página de un documento o sección. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Bidi](./set_bidi/)(bool) | Establecedor de [Aspose::Words::PageSetup::get_Bidi](./get_bidi/). |
| [set_BorderAlwaysInFront](./set_borderalwaysinfront/)(bool) | Establecedor de [Aspose::Words::PageSetup::get_BorderAlwaysInFront](./get_borderalwaysinfront/). |
| [set_BorderAppliesTo](./set_borderappliesto/)(Aspose::Words::PageBorderAppliesTo) | Establecedor de [Aspose::Words::PageSetup::get_BorderAppliesTo](./get_borderappliesto/). |
| [set_BorderDistanceFrom](./set_borderdistancefrom/)(Aspose::Words::PageBorderDistanceFrom) | Establecedor de [Aspose::Words::PageSetup::get_BorderDistanceFrom](./get_borderdistancefrom/). |
| [set_BorderSurroundsFooter](./set_bordersurroundsfooter/)(bool) | Establecedor de [Aspose::Words::PageSetup::get_BorderSurroundsFooter](./get_bordersurroundsfooter/). |
| [set_BorderSurroundsHeader](./set_bordersurroundsheader/)(bool) | Establecedor de [Aspose::Words::PageSetup::get_BorderSurroundsHeader](./get_bordersurroundsheader/). |
| [set_BottomMargin](./set_bottommargin/)(double) | Establecedor de [Aspose::Words::PageSetup::get_BottomMargin](./get_bottommargin/). |
| [set_ChapterPageSeparator](./set_chapterpageseparator/)(Aspose::Words::ChapterPageSeparator) | Establecedor de [Aspose::Words::PageSetup::get_ChapterPageSeparator](./get_chapterpageseparator/). |
| [set_CharactersPerLine](./set_charactersperline/)(int32_t) | Establecedor de [Aspose::Words::PageSetup::get_CharactersPerLine](./get_charactersperline/). |
| [set_DifferentFirstPageHeaderFooter](./set_differentfirstpageheaderfooter/)(bool) | Establecedor de [Aspose::Words::PageSetup::get_DifferentFirstPageHeaderFooter](./get_differentfirstpageheaderfooter/). |
| [set_FirstPageTray](./set_firstpagetray/)(int32_t) | Establece la bandeja de papel (cajón) a usar para la primera página de una sección. El valor es específico de la implementación (impresora). |
| [set_FooterDistance](./set_footerdistance/)(double) | Establecedor de [Aspose::Words::PageSetup::get_FooterDistance](./get_footerdistance/). |
| [set_Gutter](./set_gutter/)(double) | Establecedor de [Aspose::Words::PageSetup::get_Gutter](./get_gutter/). |
| [set_HeaderDistance](./set_headerdistance/)(double) | Establecedor de [Aspose::Words::PageSetup::get_HeaderDistance](./get_headerdistance/). |
| [set_HeadingLevelForChapter](./set_headinglevelforchapter/)(int32_t) | Establecedor de [Aspose::Words::PageSetup::get_HeadingLevelForChapter](./get_headinglevelforchapter/). |
| [set_LayoutMode](./set_layoutmode/)(Aspose::Words::SectionLayoutMode) | Establecedor de [Aspose::Words::PageSetup::get_LayoutMode](./get_layoutmode/). |
| [set_LeftMargin](./set_leftmargin/)(double) | Establecedor de [Aspose::Words::PageSetup::get_LeftMargin](./get_leftmargin/). |
| [set_LineNumberCountBy](./set_linenumbercountby/)(int32_t) | Establecedor de [Aspose::Words::PageSetup::get_LineNumberCountBy](./get_linenumbercountby/). |
| [set_LineNumberDistanceFromText](./set_linenumberdistancefromtext/)(double) | Establecedor de [Aspose::Words::PageSetup::get_LineNumberDistanceFromText](./get_linenumberdistancefromtext/). |
| [set_LineNumberRestartMode](./set_linenumberrestartmode/)(Aspose::Words::LineNumberRestartMode) | Establecedor de [Aspose::Words::PageSetup::get_LineNumberRestartMode](./get_linenumberrestartmode/). |
| [set_LinesPerPage](./set_linesperpage/)(int32_t) | Establecedor de [Aspose::Words::PageSetup::get_LinesPerPage](./get_linesperpage/). |
| [set_LineStartingNumber](./set_linestartingnumber/)(int32_t) | Establecedor de [Aspose::Words::PageSetup::get_LineStartingNumber](./get_linestartingnumber/). |
| [set_Margins](./set_margins/)(Aspose::Words::Margins) | Establecedor de [Aspose::Words::PageSetup::get_Margins](./get_margins/). |
| [set_MultiplePages](./set_multiplepages/)(Aspose::Words::Settings::MultiplePagesType) | Establecedor de [Aspose::Words::PageSetup::get_MultiplePages](./get_multiplepages/). |
| [set_OddAndEvenPagesHeaderFooter](./set_oddandevenpagesheaderfooter/)(bool) | Establecedor de [Aspose::Words::PageSetup::get_OddAndEvenPagesHeaderFooter](./get_oddandevenpagesheaderfooter/). |
| [set_Orientation](./set_orientation/)(Aspose::Words::Orientation) | Establecedor de [Aspose::Words::PageSetup::get_Orientation](./get_orientation/). |
| [set_OtherPagesTray](./set_otherpagestray/)(int32_t) | Establece la bandeja de papel (cajón) que se utilizará para todas las páginas excepto la primera de una sección. El valor es específico de la implementación (impresora). |
| [set_PageHeight](./set_pageheight/)(double) | Establecedor de [Aspose::Words::PageSetup::get_PageHeight](./get_pageheight/). |
| [set_PageNumberStyle](./set_pagenumberstyle/)(Aspose::Words::NumberStyle) | Establecedor de [Aspose::Words::PageSetup::get_PageNumberStyle](./get_pagenumberstyle/). |
| [set_PageStartingNumber](./set_pagestartingnumber/)(int32_t) | Establecedor de [Aspose::Words::PageSetup::get_PageStartingNumber](./get_pagestartingnumber/). |
| [set_PageWidth](./set_pagewidth/)(double) | Establecedor de [Aspose::Words::PageSetup::get_PageWidth](./get_pagewidth/). |
| [set_PaperSize](./set_papersize/)(Aspose::Words::PaperSize) | Establecedor de [Aspose::Words::PageSetup::get_PaperSize](./get_papersize/). |
| [set_RestartPageNumbering](./set_restartpagenumbering/)(bool) | Establecedor de [Aspose::Words::PageSetup::get_RestartPageNumbering](./get_restartpagenumbering/). |
| [set_RightMargin](./set_rightmargin/)(double) | Establecedor de [Aspose::Words::PageSetup::get_RightMargin](./get_rightmargin/). |
| [set_RtlGutter](./set_rtlgutter/)(bool) | Establecedor de [Aspose::Words::PageSetup::get_RtlGutter](./get_rtlgutter/). |
| [set_SectionStart](./set_sectionstart/)(Aspose::Words::SectionStart) | Establecedor de [Aspose::Words::PageSetup::get_SectionStart](./get_sectionstart/). |
| [set_SheetsPerBooklet](./set_sheetsperbooklet/)(int32_t) | Establecedor de [Aspose::Words::PageSetup::get_SheetsPerBooklet](./get_sheetsperbooklet/). |
| [set_SuppressEndnotes](./set_suppressendnotes/)(bool) | True si las notas al final se imprimen al final de la siguiente sección que no suprime notas al final. Las notas al final suprimidas se imprimen antes de las notas al final en esa sección. |
| [set_TextOrientation](./set_textorientation/)(Aspose::Words::TextOrientation) | Establecedor de [Aspose::Words::PageSetup::get_TextOrientation](./get_textorientation/). |
| [set_TopMargin](./set_topmargin/)(double) | Setter para [Aspose::Words::PageSetup::get_TopMargin](./get_topmargin/). |
| [set_VerticalAlignment](./set_verticalalignment/)(Aspose::Words::PageVerticalAlignment) | Setter para [Aspose::Words::PageSetup::get_VerticalAlignment](./get_verticalalignment/). |
| static [Type](./type/)() |  |
## Observaciones


[PageSetup](./) object contains all the page setup attributes of a section (left margin, bottom margin, paper size, and so on) as properties.

## Ejemplos



Muestra cómo aplicar y revertir la configuración de página en secciones de un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Modifique las propiedades de configuración de página de la sección actual del generador y añada texto.
builder->get_PageSetup()->set_Orientation(Aspose::Words::Orientation::Landscape);
builder->get_PageSetup()->set_VerticalAlignment(Aspose::Words::PageVerticalAlignment::Center);
builder->Writeln(u"This is the first section, which landscape oriented with vertically centered text.");

// Si iniciamos una nueva sección usando un generador de documentos,
// heredará las propiedades de configuración de página actuales del generador.
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);

ASSERT_EQ(Aspose::Words::Orientation::Landscape, doc->get_Sections()->idx_get(1)->get_PageSetup()->get_Orientation());
ASSERT_EQ(Aspose::Words::PageVerticalAlignment::Center, doc->get_Sections()->idx_get(1)->get_PageSetup()->get_VerticalAlignment());

// Podemos revertir sus propiedades de configuración de página a sus valores predeterminados usando el método "ClearFormatting".
builder->get_PageSetup()->ClearFormatting();

ASSERT_EQ(Aspose::Words::Orientation::Portrait, doc->get_Sections()->idx_get(1)->get_PageSetup()->get_Orientation());
ASSERT_EQ(Aspose::Words::PageVerticalAlignment::Top, doc->get_Sections()->idx_get(1)->get_PageSetup()->get_VerticalAlignment());

builder->Writeln(u"This is the second section, which is in default Letter paper size, portrait orientation and top alignment.");

doc->Save(get_ArtifactsDir() + u"PageSetup.ClearFormatting.docx");
```

## Ver también

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
