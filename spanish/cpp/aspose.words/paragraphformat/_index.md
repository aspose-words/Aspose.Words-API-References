---
title: "Clase Aspose::Words::ParagraphFormat"
linktitle: "ParagraphFormat"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Clase Aspose::Words::ParagraphFormat. Representa todo el formato de un párrafo. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 49000
url: /es/cpp/aspose.words/paragraphformat/
---
## ParagraphFormat class


Representa todo el formato de un párrafo. Para obtener más información, visite el artículo de documentación [Working with Paragraphs](https://docs.aspose.com/words/cpp/working-with-paragraphs/).

```cpp
class ParagraphFormat : public Aspose::Words::IBorderAttrSource,
                        public Aspose::Words::IShadingAttrSource
```

## Métodos

| Método | Descripción |
| --- | --- |
| [ClearFormatting](./clearformatting/)() | Restablece el formato de párrafo predeterminado. |
| [get_AddSpaceBetweenFarEastAndAlpha](./get_addspacebetweenfareastandalpha/)() | Obtiene o establece una bandera que indica si el espaciado entre caracteres se ajusta automáticamente entre regiones de texto latino y regiones de texto de Asia Oriental en el párrafo actual. |
| [get_AddSpaceBetweenFarEastAndDigit](./get_addspacebetweenfareastanddigit/)() | Obtiene o establece una bandera que indica si el espaciado entre caracteres se ajusta automáticamente entre regiones de números y regiones de texto de Asia Oriental en el párrafo actual. |
| [get_Alignment](./get_alignment/)() | Obtiene o establece la alineación del texto para el párrafo. |
| [get_BaselineAlignment](./get_baselinealignment/)() | Obtiene o establece la posición vertical de las fuentes en una línea. |
| [get_Bidi](./get_bidi/)() | Obtiene o establece si este es un párrafo de derecha a izquierda. |
| [get_Borders](./get_borders/)() | Obtiene la colección de bordes del párrafo. |
| [get_CharacterUnitFirstLineIndent](./get_characterunitfirstlineindent/)() | Obtiene o establece el valor (en caracteres) para la sangría de primera línea o colgante. Use valores positivos para establecer la sangría de primera línea y valores negativos para establecer la sangría colgante. |
| [get_CharacterUnitLeftIndent](./get_characterunitleftindent/)() | Obtiene o establece el valor de sangría izquierda (en caracteres) para los párrafos especificados. |
| [get_CharacterUnitRightIndent](./get_characterunitrightindent/)() | Obtiene o establece el valor de sangría derecha (en caracteres) para los párrafos especificados. |
| [get_DropCapPosition](./get_dropcapposition/)() | Obtiene o establece la posición para un texto de inicial mayúscula. |
| [get_FarEastLineBreakControl](./get_fareastlinebreakcontrol/)() | Obtiene o establece una bandera que indica si se aplican las reglas de salto de línea de Asia Oriental al párrafo actual. |
| [get_FirstLineIndent](./get_firstlineindent/)() | Obtiene o establece el valor (en puntos) para una sangría de primera línea o colgante. Use valores positivos para establecer la sangría de primera línea y valores negativos para establecer la sangría colgante. |
| [get_HangingPunctuation](./get_hangingpunctuation/)() | Obtiene o establece una bandera que indica si la puntuación colgante está habilitada para el párrafo actual. |
| [get_IsHeading](./get_isheading/)() | Verdadero cuando el estilo del párrafo es uno de los estilos de encabezado incorporados. |
| [get_IsListItem](./get_islistitem/)() | Verdadero cuando el párrafo es un elemento de una lista con viñetas o numerada. |
| [get_KeepTogether](./get_keeptogether/)() | Verdadero si todas las líneas del párrafo deben permanecer en la misma página. |
| [get_KeepWithNext](./get_keepwithnext/)() | Verdadero si el párrafo debe permanecer en la misma página que el párrafo que le sigue. |
| [get_LeftIndent](./get_leftindent/)() | Obtiene o establece el valor (en puntos) que representa la sangría izquierda para el párrafo. |
| [get_LineSpacing](./get_linespacing/)() | Obtiene o establece el interlineado (en puntos) para el párrafo. |
| [get_LineSpacingRule](./get_linespacingrule/)() | Obtiene o establece el interlineado para el párrafo. |
| [get_LinesToDrop](./get_linestodrop/)() | Obtiene o establece el número de líneas del texto del párrafo usadas para calcular la altura de la inicial mayúscula. |
| [get_LineUnitAfter](./get_lineunitafter/)() | Obtiene o establece la cantidad de espacio (en líneas de cuadrícula) después de los párrafos. |
| [get_LineUnitBefore](./get_lineunitbefore/)() | Obtiene o establece la cantidad de espacio (en líneas de cuadrícula) antes de los párrafos. |
| [get_MirrorIndents](./get_mirrorindents/)() | Obtiene o establece una bandera que indica si las sangrías izquierda y derecha tienen la misma anchura. |
| [get_NoSpaceBetweenParagraphsOfSameStyle](./get_nospacebetweenparagraphsofsamestyle/)() | Cuando **true**, [SpaceBefore](./get_spacebefore/) y [SpaceAfter](./get_spaceafter/) serán ignorados entre los párrafos del mismo estilo. |
| [get_OutlineLevel](./get_outlinelevel/)() | Especifica el nivel de esquema del párrafo en el documento. |
| [get_PageBreakBefore](./get_pagebreakbefore/)() | Verdadero si se fuerza un salto de página antes del párrafo. |
| [get_RightIndent](./get_rightindent/)() | Obtiene o establece el valor (en puntos) que representa la sangría derecha del párrafo. |
| [get_Shading](./get_shading/)() | Devuelve un objeto [Shading](../shading/) que se refiere al formato de sombreado del párrafo. |
| [get_SnapToGrid](./get_snaptogrid/)() | Especifica si el párrafo actual debe usar la configuración de líneas de cuadrícula del documento por página al organizar el contenido en el párrafo. |
| [get_SpaceAfter](./get_spaceafter/)() | Obtiene o establece la cantidad de espacio (en puntos) después del párrafo. |
| [get_SpaceAfterAuto](./get_spaceafterauto/)() | True si la cantidad de espacio después del párrafo se establece automáticamente. |
| [get_SpaceBefore](./get_spacebefore/)() | Obtiene o establece la cantidad de espacio (en puntos) antes del párrafo. |
| [get_SpaceBeforeAuto](./get_spacebeforeauto/)() | True si la cantidad de espacio antes del párrafo se establece automáticamente. |
| [get_Style](./get_style/)() | Obtiene o establece el estilo de párrafo aplicado a este formato. |
| [get_StyleIdentifier](./get_styleidentifier/)() | Obtiene o establece el identificador de estilo independiente de la configuración regional del estilo de párrafo aplicado a este formato. |
| [get_StyleName](./get_stylename/)() | Obtiene o establece el nombre del estilo de párrafo aplicado a este formato. |
| [get_SuppressAutoHyphens](./get_suppressautohyphens/)() | Especifica si el párrafo actual debe estar exento de cualquier guionización que se aplique en la configuración del documento. |
| [get_SuppressLineNumbers](./get_suppresslinenumbers/)() | Especifica si las líneas del párrafo actual deben estar exentas de la numeración de líneas que se aplica en la sección principal. |
| [get_TabStops](./get_tabstops/)() | Obtiene la colección de tabulaciones personalizadas definidas para este objeto. |
| [get_WidowControl](./get_widowcontrol/)() | True si la primera y la última línea del párrafo deben permanecer en la misma página que el resto del párrafo. |
| [get_WordWrap](./get_wordwrap/)() | Si esta propiedad es **false**, el texto latino en medio de una palabra puede dividirse en el párrafo actual. De lo contrario, el texto latino se divide por palabras completas. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AddSpaceBetweenFarEastAndAlpha](./set_addspacebetweenfareastandalpha/)(bool) | Establecedor para [Aspose::Words::ParagraphFormat::get_AddSpaceBetweenFarEastAndAlpha](./get_addspacebetweenfareastandalpha/). |
| [set_AddSpaceBetweenFarEastAndDigit](./set_addspacebetweenfareastanddigit/)(bool) | Establecedor para [Aspose::Words::ParagraphFormat::get_AddSpaceBetweenFarEastAndDigit](./get_addspacebetweenfareastanddigit/). |
| [set_Alignment](./set_alignment/)(Aspose::Words::ParagraphAlignment) | Establecedor para [Aspose::Words::ParagraphFormat::get_Alignment](./get_alignment/). |
| [set_BaselineAlignment](./set_baselinealignment/)(Aspose::Words::BaselineAlignment) | Establecedor para [Aspose::Words::ParagraphFormat::get_BaselineAlignment](./get_baselinealignment/). |
| [set_Bidi](./set_bidi/)(bool) | Establecedor para [Aspose::Words::ParagraphFormat::get_Bidi](./get_bidi/). |
| [set_CharacterUnitFirstLineIndent](./set_characterunitfirstlineindent/)(double) | Establecedor para [Aspose::Words::ParagraphFormat::get_CharacterUnitFirstLineIndent](./get_characterunitfirstlineindent/). |
| [set_CharacterUnitLeftIndent](./set_characterunitleftindent/)(double) | Establecedor para [Aspose::Words::ParagraphFormat::get_CharacterUnitLeftIndent](./get_characterunitleftindent/). |
| [set_CharacterUnitRightIndent](./set_characterunitrightindent/)(double) | Establecedor para [Aspose::Words::ParagraphFormat::get_CharacterUnitRightIndent](./get_characterunitrightindent/). |
| [set_DropCapPosition](./set_dropcapposition/)(Aspose::Words::DropCapPosition) | Establecedor para [Aspose::Words::ParagraphFormat::get_DropCapPosition](./get_dropcapposition/). |
| [set_FarEastLineBreakControl](./set_fareastlinebreakcontrol/)(bool) | Establecedor para [Aspose::Words::ParagraphFormat::get_FarEastLineBreakControl](./get_fareastlinebreakcontrol/). |
| [set_FirstLineIndent](./set_firstlineindent/)(double) | Método setter para [Aspose::Words::ParagraphFormat::get_FirstLineIndent](./get_firstlineindent/). |
| [set_HangingPunctuation](./set_hangingpunctuation/)(bool) | Método setter para [Aspose::Words::ParagraphFormat::get_HangingPunctuation](./get_hangingpunctuation/). |
| [set_KeepTogether](./set_keeptogether/)(bool) | Método setter para [Aspose::Words::ParagraphFormat::get_KeepTogether](./get_keeptogether/). |
| [set_KeepWithNext](./set_keepwithnext/)(bool) | Método setter para [Aspose::Words::ParagraphFormat::get_KeepWithNext](./get_keepwithnext/). |
| [set_LeftIndent](./set_leftindent/)(double) | Método setter para [Aspose::Words::ParagraphFormat::get_LeftIndent](./get_leftindent/). |
| [set_LineSpacing](./set_linespacing/)(double) | Método setter para [Aspose::Words::ParagraphFormat::get_LineSpacing](./get_linespacing/). |
| [set_LineSpacingRule](./set_linespacingrule/)(Aspose::Words::LineSpacingRule) | Método setter para [Aspose::Words::ParagraphFormat::get_LineSpacingRule](./get_linespacingrule/). |
| [set_LinesToDrop](./set_linestodrop/)(int32_t) | Método setter para [Aspose::Words::ParagraphFormat::get_LinesToDrop](./get_linestodrop/). |
| [set_LineUnitAfter](./set_lineunitafter/)(double) | Método setter para [Aspose::Words::ParagraphFormat::get_LineUnitAfter](./get_lineunitafter/). |
| [set_LineUnitBefore](./set_lineunitbefore/)(double) | Método setter para [Aspose::Words::ParagraphFormat::get_LineUnitBefore](./get_lineunitbefore/). |
| [set_MirrorIndents](./set_mirrorindents/)(bool) | Método setter para [Aspose::Words::ParagraphFormat::get_MirrorIndents](./get_mirrorindents/). |
| [set_NoSpaceBetweenParagraphsOfSameStyle](./set_nospacebetweenparagraphsofsamestyle/)(bool) | Método setter para [Aspose::Words::ParagraphFormat::get_NoSpaceBetweenParagraphsOfSameStyle](./get_nospacebetweenparagraphsofsamestyle/). |
| [set_OutlineLevel](./set_outlinelevel/)(Aspose::Words::OutlineLevel) | Método setter para [Aspose::Words::ParagraphFormat::get_OutlineLevel](./get_outlinelevel/). |
| [set_PageBreakBefore](./set_pagebreakbefore/)(bool) | Método setter para [Aspose::Words::ParagraphFormat::get_PageBreakBefore](./get_pagebreakbefore/). |
| [set_RightIndent](./set_rightindent/)(double) | Método setter para [Aspose::Words::ParagraphFormat::get_RightIndent](./get_rightindent/). |
| [set_SnapToGrid](./set_snaptogrid/)(bool) | Método setter para [Aspose::Words::ParagraphFormat::get_SnapToGrid](./get_snaptogrid/). |
| [set_SpaceAfter](./set_spaceafter/)(double) | Método setter para [Aspose::Words::ParagraphFormat::get_SpaceAfter](./get_spaceafter/). |
| [set_SpaceAfterAuto](./set_spaceafterauto/)(bool) | Método setter para [Aspose::Words::ParagraphFormat::get_SpaceAfterAuto](./get_spaceafterauto/). |
| [set_SpaceBefore](./set_spacebefore/)(double) | Método setter para [Aspose::Words::ParagraphFormat::get_SpaceBefore](./get_spacebefore/). |
| [set_SpaceBeforeAuto](./set_spacebeforeauto/)(bool) | Método setter para [Aspose::Words::ParagraphFormat::get_SpaceBeforeAuto](./get_spacebeforeauto/). |
| [set_Style](./set_style/)(const System::SharedPtr\<Aspose::Words::Style\>\&) | Método setter para [Aspose::Words::ParagraphFormat::get_Style](./get_style/). |
| [set_StyleIdentifier](./set_styleidentifier/)(Aspose::Words::StyleIdentifier) | Método setter para [Aspose::Words::ParagraphFormat::get_StyleIdentifier](./get_styleidentifier/). |
| [set_StyleName](./set_stylename/)(const System::String\&) | Método setter para [Aspose::Words::ParagraphFormat::get_StyleName](./get_stylename/). |
| [set_SuppressAutoHyphens](./set_suppressautohyphens/)(bool) | Método setter para [Aspose::Words::ParagraphFormat::get_SuppressAutoHyphens](./get_suppressautohyphens/). |
| [set_SuppressLineNumbers](./set_suppresslinenumbers/)(bool) | Método setter para [Aspose::Words::ParagraphFormat::get_SuppressLineNumbers](./get_suppresslinenumbers/). |
| [set_WidowControl](./set_widowcontrol/)(bool) | Establecedor para [Aspose::Words::ParagraphFormat::get_WidowControl](./get_widowcontrol/). |
| [set_WordWrap](./set_wordwrap/)(bool) | Establecedor para [Aspose::Words::ParagraphFormat::get_WordWrap](./get_wordwrap/). |
| static [Type](./type/)() |  |

## Ejemplos



Muestra cómo construir un documento Aspose.Words manualmente.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Un documento en blanco contiene una sección, un cuerpo y un párrafo.
// Llame al método "RemoveAllChildren" para eliminar todos esos nodos,
// y termine con un nodo de documento sin hijos.
doc->RemoveAllChildren();

// Este documento ahora no tiene nodos hijos compuestos a los que podamos añadir contenido.
// Si deseamos editarlo, necesitaremos volver a poblar su colección de nodos.
// Primero, cree una nueva sección y luego añádala como hijo al nodo raíz del documento.
auto section = System::MakeObject<Aspose::Words::Section>(doc);
doc->AppendChild<System::SharedPtr<Aspose::Words::Section>>(section);

// Establezca algunas propiedades de configuración de página para la sección.
section->get_PageSetup()->set_SectionStart(Aspose::Words::SectionStart::NewPage);
section->get_PageSetup()->set_PaperSize(Aspose::Words::PaperSize::Letter);

// Una sección necesita un cuerpo, que contendrá y mostrará todo su contenido
// en la página entre el encabezado y el pie de página de la sección.
auto body = System::MakeObject<Aspose::Words::Body>(doc);
section->AppendChild<System::SharedPtr<Aspose::Words::Body>>(body);

// Crea un párrafo, establece algunas propiedades de formato y luego añádelo como hijo al cuerpo.
auto para = System::MakeObject<Aspose::Words::Paragraph>(doc);

para->get_ParagraphFormat()->set_StyleName(u"Heading 1");
para->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);

body->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(para);

// Finalmente, agrega contenido al documento. Crea un run,
// establece su apariencia y contenido, y luego añádelo como hijo al párrafo.
auto run = System::MakeObject<Aspose::Words::Run>(doc);
run->set_Text(u"Hello World!");
run->get_Font()->set_Color(System::Drawing::Color::get_Red());
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

ASSERT_EQ(u"Hello World!", doc->GetText().Trim());

doc->Save(get_ArtifactsDir() + u"Section.CreateManually.docx");
```

## Ver también

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
