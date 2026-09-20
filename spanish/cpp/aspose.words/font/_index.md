---
title: "Aspose::Words::Font class"
linktitle: "Fuente"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Font class. Contiene atributos de fuente (nombre de fuente, tamaño de fuente, color, etc.) para un objeto. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 29000
url: /es/cpp/aspose.words/font/
---
## Font class


Contiene atributos de fuente (nombre de fuente, tamaño de fuente, color, etc.) para un objeto. Para obtener más información, visite el artículo de documentación [Working with Fonts](https://docs.aspose.com/words/cpp/working-with-fonts/).

```cpp
class Font : public Aspose::Words::IBorderAttrSource,
             public Aspose::Words::IShadingAttrSource,
             public Aspose::Words::Drawing::Core::IFillable
```

## Métodos

| Método | Descripción |
| --- | --- |
| [ClearFormatting](./clearformatting/)() | Restablece el formato de fuente predeterminado. |
| [get_AllCaps](./get_allcaps/)() | Verdadero si la fuente está formateada en mayúsculas. |
| [get_AutoColor](./get_autocolor/)() | Devuelve el color calculado actual del texto (negro o blanco) que se usará para 'auto color'. Si el color no es 'auto', entonces devuelve [Color](./get_color/). |
| [get_Bidi](./get_bidi/)() | Especifica si el contenido de esta ejecución debe tener características de derecha a izquierda. |
| [get_Bold](./get_bold/)() | Verdadero si la fuente está formateada en negrita. |
| [get_BoldBi](./get_boldbi/)() | Verdadero si el texto de derecha a izquierda está formateado en negrita. |
| [get_Border](./get_border/)() | Devuelve un objeto [Border](../border/) que especifica el borde para la fuente. |
| [get_Color](./get_color/)() | Obtiene o establece el color de la fuente. |
| [get_ComplexScript](./get_complexscript/)() | Especifica si el contenido de esta ejecución debe tratarse como texto de escritura compleja sin importar sus valores de caracteres Unicode al determinar el formato de esta ejecución. |
| [get_DoubleStrikeThrough](./get_doublestrikethrough/)() | Verdadero si la fuente está formateada con doble tachado. |
| [get_Emboss](./get_emboss/)() | Verdadero si la fuente está formateada como relieve. |
| [get_EmphasisMark](./get_emphasismark/)() | Obtiene o establece la marca de énfasis aplicada a este formato. |
| [get_Engrave](./get_engrave/)() | Verdadero si la fuente está formateada como grabado. |
| [get_Fill](./get_fill/)() | Obtiene el formato de relleno para la [Font](./). |
| [get_Hidden](./get_hidden/)() | Verdadero si la fuente está formateada como texto oculto. |
| [get_HighlightColor](./get_highlightcolor/)() | Obtiene o establece el color de resaltado (marcador). |
| [get_Italic](./get_italic/)() | True si la fuente está formateada en cursiva. |
| [get_ItalicBi](./get_italicbi/)() | Verdadero si el texto de derecha a izquierda está formateado en cursiva. |
| [get_Kerning](./get_kerning/)() | Obtiene o establece el tamaño de fuente a partir del cual comienza el kerning. |
| [get_LineSpacing](./get_linespacing/)() | Devuelve el interlineado de esta fuente (en puntos). |
| [get_LocaleId](./get_localeid/)() | Obtiene o establece el identificador de configuración regional (idioma) de los caracteres formateados. |
| [get_LocaleIdBi](./get_localeidbi/)() | Obtiene o establece el identificador de configuración regional (idioma) de los caracteres formateados de derecha a izquierda. |
| [get_LocaleIdFarEast](./get_localeidfareast/)() | Obtiene o establece el identificador de configuración regional (idioma) de los caracteres formateados asiáticos. |
| [get_Name](./get_name/)() | Obtiene o establece el nombre de la fuente. |
| [get_NameAscii](./get_nameascii/)() | Devuelve o establece la fuente utilizada para texto latino (caracteres con códigos de carácter de 0 (cero) a 127). |
| [get_NameBi](./get_namebi/)() | Devuelve o establece el nombre de la fuente en un documento de idioma de derecha a izquierda. |
| [get_NameFarEast](./get_namefareast/)() | Devuelve o establece un nombre de fuente de Asia Oriental. |
| [get_NameOther](./get_nameother/)() | Devuelve o establece la fuente utilizada para los caracteres con códigos de carácter de 128 a 255. |
| [get_NoProofing](./get_noproofing/)() | True cuando los caracteres formateados no deben revisarse ortográficamente. |
| [get_NumberSpacing](./get_numberspacing/)() | Obtiene o establece el tipo de espaciado del número que se muestra. |
| [get_Outline](./get_outline/)() | True si la fuente está formateada como contorno. |
| [get_Position](./get_position/)() | Obtiene o establece la posición del texto (en puntos) relativa a la línea base. Un número positivo eleva el texto, y un número negativo lo baja. |
| [get_Scaling](./get_scaling/)() | Obtiene o establece la escala de ancho de carácter en porcentaje. |
| [get_Shading](./get_shading/)() | Devuelve un objeto [Shading](../shading/) que se refiere al formato de sombreado para la fuente. |
| [get_Shadow](./get_shadow/)() | True si la fuente está formateada como sombreada. |
| [get_Size](./get_size/)() | Obtiene o establece el tamaño de la fuente en puntos. |
| [get_SizeBi](./get_sizebi/)() | Obtiene o establece el tamaño de la fuente en puntos utilizado en un documento de derecha a izquierda. |
| [get_SmallCaps](./get_smallcaps/)() | True si la fuente está formateada como letras capitales pequeñas. |
| [get_SnapToGrid](./get_snaptogrid/)() | Especifica si la fuente actual debe usar la configuración de caracteres por línea de la cuadrícula del documento al maquetar. |
| [get_Spacing](./get_spacing/)() | Devuelve o establece el espaciado (en puntos) entre caracteres. |
| [get_StrikeThrough](./get_strikethrough/)() | True si la fuente está formateada como texto tachado. |
| [get_Style](./get_style/)() | Obtiene o establece el estilo de carácter aplicado a este formato. |
| [get_StyleIdentifier](./get_styleidentifier/)() | Obtiene o establece el identificador de estilo independiente de la configuración regional del estilo de carácter aplicado a este formato. |
| [get_StyleName](./get_stylename/)() | Obtiene o establece el nombre del estilo de carácter aplicado a este formato. |
| [get_Subscript](./get_subscript/)() | True si la fuente está formateada como subíndice. |
| [get_Superscript](./get_superscript/)() | True si la fuente está formateada como superíndice. |
| [get_TextEffect](./get_texteffect/)() | Obtiene o establece el efecto de animación de la fuente. |
| [get_ThemeColor](./get_themecolor/)() | Obtiene o establece el color del tema en el esquema de colores aplicado que está asociado con este objeto [Font](./). |
| [get_ThemeFont](./get_themefont/)() | Obtiene o establece la fuente del tema en el esquema de fuentes aplicado que está asociado con este objeto [Font](./). |
| [get_ThemeFontAscii](./get_themefontascii/)() | Obtiene o establece la fuente del tema utilizada para texto latino (caracteres con códigos de carácter de 0 (cero) a 127) en el esquema de fuentes aplicado que está asociado con este objeto [Font](./). |
| [get_ThemeFontBi](./get_themefontbi/)() | Obtiene o establece la fuente del tema en el esquema de fuentes aplicado que está asociado con este objeto [Font](./) en un documento de idioma de derecha a izquierda. |
| [get_ThemeFontFarEast](./get_themefontfareast/)() | Obtiene o establece la fuente del tema de Asia Oriental en el esquema de fuentes aplicado que está asociado con este objeto [Font](./). |
| [get_ThemeFontOther](./get_themefontother/)() | Obtiene o establece la fuente de tema utilizada para los caracteres con códigos de carácter de 128 a 255 en el esquema de fuentes aplicado que está asociado con este objeto [Font](./). |
| [get_TintAndShade](./get_tintandshade/)() | Obtiene o establece un valor doble que aclara u oscurece un color. |
| [get_Underline](./get_underline/)() | Obtiene o establece el tipo de subrayado aplicado a la fuente. |
| [get_UnderlineColor](./get_underlinecolor/)() | Obtiene o establece el color del subrayado aplicado a la fuente. |
| [GetType](./gettype/)() const override |  |
| [HasDmlEffect](./hasdmleffect/)(Aspose::Words::TextDmlEffect) | Comprueba si se aplica un efecto de texto DrawingML particular. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AllCaps](./set_allcaps/)(bool) | Establecedor para [Aspose::Words::Font::get_AllCaps](./get_allcaps/). |
| [set_Bidi](./set_bidi/)(bool) | Establecedor para [Aspose::Words::Font::get_Bidi](./get_bidi/). |
| [set_Bold](./set_bold/)(bool) | Establecedor para [Aspose::Words::Font::get_Bold](./get_bold/). |
| [set_BoldBi](./set_boldbi/)(bool) | Establecedor para [Aspose::Words::Font::get_BoldBi](./get_boldbi/). |
| [set_Color](./set_color/)(System::Drawing::Color) | Establecedor para [Aspose::Words::Font::get_Color](./get_color/). |
| [set_ComplexScript](./set_complexscript/)(bool) | Establecedor para [Aspose::Words::Font::get_ComplexScript](./get_complexscript/). |
| [set_DoubleStrikeThrough](./set_doublestrikethrough/)(bool) | Establecedor para [Aspose::Words::Font::get_DoubleStrikeThrough](./get_doublestrikethrough/). |
| [set_Emboss](./set_emboss/)(bool) | Establecedor para [Aspose::Words::Font::get_Emboss](./get_emboss/). |
| [set_EmphasisMark](./set_emphasismark/)(Aspose::Words::EmphasisMark) | Establecedor para [Aspose::Words::Font::get_EmphasisMark](./get_emphasismark/). |
| [set_Engrave](./set_engrave/)(bool) | Establecedor para [Aspose::Words::Font::get_Engrave](./get_engrave/). |
| [set_Hidden](./set_hidden/)(bool) | Establecedor para [Aspose::Words::Font::get_Hidden](./get_hidden/). |
| [set_HighlightColor](./set_highlightcolor/)(System::Drawing::Color) | Establecedor para [Aspose::Words::Font::get_HighlightColor](./get_highlightcolor/). |
| [set_Italic](./set_italic/)(bool) | Establecedor para [Aspose::Words::Font::get_Italic](./get_italic/). |
| [set_ItalicBi](./set_italicbi/)(bool) | Establecedor para [Aspose::Words::Font::get_ItalicBi](./get_italicbi/). |
| [set_Kerning](./set_kerning/)(double) | Establecedor para [Aspose::Words::Font::get_Kerning](./get_kerning/). |
| [set_LocaleId](./set_localeid/)(int32_t) | Establecedor para [Aspose::Words::Font::get_LocaleId](./get_localeid/). |
| [set_LocaleIdBi](./set_localeidbi/)(int32_t) | Establecedor para [Aspose::Words::Font::get_LocaleIdBi](./get_localeidbi/). |
| [set_LocaleIdFarEast](./set_localeidfareast/)(int32_t) | Establecedor para [Aspose::Words::Font::get_LocaleIdFarEast](./get_localeidfareast/). |
| [set_Name](./set_name/)(const System::String\&) | Establecedor para [Aspose::Words::Font::get_Name](./get_name/). |
| [set_NameAscii](./set_nameascii/)(const System::String\&) | Establecedor para [Aspose::Words::Font::get_NameAscii](./get_nameascii/). |
| [set_NameBi](./set_namebi/)(const System::String\&) | Establecedor para [Aspose::Words::Font::get_NameBi](./get_namebi/). |
| [set_NameFarEast](./set_namefareast/)(const System::String\&) | Establecedor de [Aspose::Words::Font::get_NameFarEast](./get_namefareast/). |
| [set_NameOther](./set_nameother/)(const System::String\&) | Establecedor de [Aspose::Words::Font::get_NameOther](./get_nameother/). |
| [set_NoProofing](./set_noproofing/)(bool) | Establecedor de [Aspose::Words::Font::get_NoProofing](./get_noproofing/). |
| [set_NumberSpacing](./set_numberspacing/)(Aspose::Words::NumSpacing) | Establecedor de [Aspose::Words::Font::get_NumberSpacing](./get_numberspacing/). |
| [set_Outline](./set_outline/)(bool) | Establecedor de [Aspose::Words::Font::get_Outline](./get_outline/). |
| [set_Position](./set_position/)(double) | Establecedor de [Aspose::Words::Font::get_Position](./get_position/). |
| [set_Scaling](./set_scaling/)(int32_t) | Establecedor de [Aspose::Words::Font::get_Scaling](./get_scaling/). |
| [set_Shadow](./set_shadow/)(bool) | Establecedor de [Aspose::Words::Font::get_Shadow](./get_shadow/). |
| [set_Size](./set_size/)(double) | Establecedor de [Aspose::Words::Font::get_Size](./get_size/). |
| [set_SizeBi](./set_sizebi/)(double) | Establecedor de [Aspose::Words::Font::get_SizeBi](./get_sizebi/). |
| [set_SmallCaps](./set_smallcaps/)(bool) | Establecedor de [Aspose::Words::Font::get_SmallCaps](./get_smallcaps/). |
| [set_SnapToGrid](./set_snaptogrid/)(bool) | Especifica si la fuente actual debe usar la configuración de caracteres por línea de la cuadrícula del documento al maquetar. |
| [set_Spacing](./set_spacing/)(double) | Establecedor de [Aspose::Words::Font::get_Spacing](./get_spacing/). |
| [set_StrikeThrough](./set_strikethrough/)(bool) | Establecedor de [Aspose::Words::Font::get_StrikeThrough](./get_strikethrough/). |
| [set_Style](./set_style/)(const System::SharedPtr\<Aspose::Words::Style\>\&) | Establecedor de [Aspose::Words::Font::get_Style](./get_style/). |
| [set_StyleIdentifier](./set_styleidentifier/)(Aspose::Words::StyleIdentifier) | Establecedor de [Aspose::Words::Font::get_StyleIdentifier](./get_styleidentifier/). |
| [set_StyleName](./set_stylename/)(const System::String\&) | Establecedor de [Aspose::Words::Font::get_StyleName](./get_stylename/). |
| [set_Subscript](./set_subscript/)(bool) | Establecedor de [Aspose::Words::Font::get_Subscript](./get_subscript/). |
| [set_Superscript](./set_superscript/)(bool) | Establecedor de [Aspose::Words::Font::get_Superscript](./get_superscript/). |
| [set_TextEffect](./set_texteffect/)(Aspose::Words::TextEffect) | Establecedor de [Aspose::Words::Font::get_TextEffect](./get_texteffect/). |
| [set_ThemeColor](./set_themecolor/)(Aspose::Words::Themes::ThemeColor) | Establecedor de [Aspose::Words::Font::get_ThemeColor](./get_themecolor/). |
| [set_ThemeFont](./set_themefont/)(Aspose::Words::Themes::ThemeFont) | Establecedor de [Aspose::Words::Font::get_ThemeFont](./get_themefont/). |
| [set_ThemeFontAscii](./set_themefontascii/)(Aspose::Words::Themes::ThemeFont) | Establecedor de [Aspose::Words::Font::get_ThemeFontAscii](./get_themefontascii/). |
| [set_ThemeFontBi](./set_themefontbi/)(Aspose::Words::Themes::ThemeFont) | Establecedor de [Aspose::Words::Font::get_ThemeFontBi](./get_themefontbi/). |
| [set_ThemeFontFarEast](./set_themefontfareast/)(Aspose::Words::Themes::ThemeFont) | Establecedor de [Aspose::Words::Font::get_ThemeFontFarEast](./get_themefontfareast/). |
| [set_ThemeFontOther](./set_themefontother/)(Aspose::Words::Themes::ThemeFont) | Establecedor de [Aspose::Words::Font::get_ThemeFontOther](./get_themefontother/). |
| [set_TintAndShade](./set_tintandshade/)(double) | Método set para [Aspose::Words::Font::get_TintAndShade](./get_tintandshade/). |
| [set_Underline](./set_underline/)(Aspose::Words::Underline) | Método set para [Aspose::Words::Font::get_Underline](./get_underline/). |
| [set_UnderlineColor](./set_underlinecolor/)(System::Drawing::Color) | Método set para [Aspose::Words::Font::get_UnderlineColor](./get_underlinecolor/). |
| static [Type](./type/)() |  |
## Observaciones


No crea instancias de la clase [Font](./) directamente. Simplemente usa [Font](./) para acceder a las propiedades de fuente de los distintos objetos, como [Run](../run/), [Paragraph](../paragraph/), [Style](../style/) y [DocumentBuilder](../documentbuilder/).

## Ejemplos



Muestra cómo insertar una cadena rodeada por un borde en un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->get_Border()->set_Color(System::Drawing::Color::get_Green());
builder->get_Font()->get_Border()->set_LineWidth(2.5);
builder->get_Font()->get_Border()->set_LineStyle(Aspose::Words::LineStyle::DashDotStroker);

builder->Write(u"Text surrounded by green border.");

doc->Save(get_ArtifactsDir() + u"Border.FontBorder.docx");
```


Muestra cómo formatear una corrida de texto usando su propiedad de fuente.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto run = System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!");

System::SharedPtr<Aspose::Words::Font> font = run->get_Font();
font->set_Name(u"Courier New");
font->set_Size(36);
font->set_HighlightColor(System::Drawing::Color::get_Yellow());

doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);
doc->Save(get_ArtifactsDir() + u"Font.CreateFormattedRun.docx");
```


Muestra cómo crear y usar un estilo de párrafo con formato de lista.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Crea un estilo de párrafo personalizado.
System::SharedPtr<Aspose::Words::Style> style = doc->get_Styles()->Add(Aspose::Words::StyleType::Paragraph, u"MyStyle1");
style->get_Font()->set_Size(24);
style->get_Font()->set_Name(u"Verdana");
style->get_ParagraphFormat()->set_SpaceAfter(12);

// Crea una lista y asegura que los párrafos que usan este estilo utilicen esta lista.
style->get_ListFormat()->set_List(doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::BulletDefault));
style->get_ListFormat()->set_ListLevelNumber(0);

// Aplica el estilo de párrafo al párrafo actual del generador de documentos y luego agrega algo de texto.
builder->get_ParagraphFormat()->set_Style(style);
builder->Writeln(u"Hello World: MyStyle1, bulleted list.");

// Cambie el estilo del document builder a uno que no tenga formato de lista y escriba otro párrafo.
builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Normal"));
builder->Writeln(u"Hello World: Normal.");

builder->get_Document()->Save(get_ArtifactsDir() + u"Styles.ParagraphStyleBulletedList.docx");
```

## Ver también

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
