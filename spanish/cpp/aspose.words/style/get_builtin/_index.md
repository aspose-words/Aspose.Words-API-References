---
title: "Método Aspose::Words::Style::get_BuiltIn"
linktitle: "get_BuiltIn"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Style::get_BuiltIn. True si este estilo es uno de los estilos incorporados en MS Word en C++."
type: docs
weight: 6000
url: /es/cpp/aspose.words/style/get_builtin/
---
## Style::get_BuiltIn method


Verdadero si este estilo es uno de los estilos incorporados en MS Word.

```cpp
bool Aspose::Words::Style::get_BuiltIn()
```


## Ejemplos



Muestra cómo diferenciar estilos personalizados de estilos incorporados.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Cuando creamos un documento usando Microsoft Word, o programáticamente usando Aspose.Words,
// el documento vendrá con una colección de estilos para aplicar a su texto y modificar su apariencia.
// Podemos acceder a estos estilos incorporados a través de la colección "Styles" del documento.
// Todos estos estilos tendrán la bandera "BuiltIn" establecida en "true".
System::SharedPtr<Aspose::Words::Style> style = doc->get_Styles()->idx_get(u"Emphasis");

ASSERT_TRUE(style->get_BuiltIn());

// Cree un estilo personalizado y agréguelo a la colección.
// Los estilos personalizados como este tendrán la bandera "BuiltIn" establecida en "false".
style = doc->get_Styles()->Add(Aspose::Words::StyleType::Character, u"MyStyle");
style->get_Font()->set_Color(System::Drawing::Color::get_Navy());
style->get_Font()->set_Name(u"Courier New");

ASSERT_FALSE(style->get_BuiltIn());
```

## Ver también

* Class [Style](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
