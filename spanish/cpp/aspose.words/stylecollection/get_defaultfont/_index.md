---
title: "Aspose::Words::StyleCollection::get_DefaultFont método"
linktitle: "get_DefaultFont"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::StyleCollection::get_DefaultFont método. Obtiene el formato de texto predeterminado del documento en C++."
type: docs
weight: 6000
url: /es/cpp/aspose.words/stylecollection/get_defaultfont/
---
## StyleCollection::get_DefaultFont method


Obtiene el formato de texto predeterminado del documento.

```cpp
System::SharedPtr<Aspose::Words::Font> Aspose::Words::StyleCollection::get_DefaultFont()
```

## Observaciones


Ten en cuenta que los valores predeterminados a nivel de documento se introdujeron en Microsoft Word 2007 y solo son compatibles totalmente con los formatos OOXML ([Docx](../../loadformat/)). Los formatos de documento anteriores tienen soporte limitado para esta característica y solo se pueden almacenar los nombres de fuentes.

## Ejemplos



Muestra cómo agregar un [Style](../../style/) a la colección de estilos de un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

System::SharedPtr<Aspose::Words::StyleCollection> styles = doc->get_Styles();
// Establezca los parámetros predeterminados para los nuevos estilos que luego podamos agregar a esta colección.
styles->get_DefaultFont()->set_Name(u"Courier New");
// Si añadimos un estilo de "StyleType.Paragraph", la colección aplicará los valores de
// su propiedad "DefaultParagraphFormat" a la propiedad "ParagraphFormat" del estilo.
styles->get_DefaultParagraphFormat()->set_FirstLineIndent(15.0);
// Añade un estilo y luego verifica que tiene la configuración predeterminada.
styles->Add(Aspose::Words::StyleType::Paragraph, u"MyStyle");

ASSERT_EQ(u"Courier New", styles->idx_get(4)->get_Font()->get_Name());
ASPOSE_ASSERT_EQ(15.0, styles->idx_get(u"MyStyle")->get_ParagraphFormat()->get_FirstLineIndent());
```

## Ver también

* Class [Font](../../font/)
* Class [StyleCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
