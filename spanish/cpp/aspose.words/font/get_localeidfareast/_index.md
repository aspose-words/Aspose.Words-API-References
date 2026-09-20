---
title: "Aspose::Words::Font::get_LocaleIdFarEast método"
linktitle: "get_LocaleIdFarEast"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Font::get_LocaleIdFarEast método. Obtiene o establece el identificador de configuración regional (idioma) de los caracteres asiáticos formateados en C++."
type: docs
weight: 24000
url: /es/cpp/aspose.words/font/get_localeidfareast/
---
## Font::get_LocaleIdFarEast method


Obtiene o establece el identificador de configuración regional (idioma) de los caracteres formateados asiáticos.

```cpp
int32_t Aspose::Words::Font::get_LocaleIdFarEast()
```


## Ejemplos



Muestra cómo insertar y formatear texto en un idioma del Lejano Oriente.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Especifique la configuración de fuente que el generador de documentos aplicará a cualquier texto que inserte.
builder->get_Font()->set_Name(u"Courier New");
builder->get_Font()->set_LocaleId(System::MakeObject<System::Globalization::CultureInfo>(u"en-US", false)->get_LCID());

// Nombre equivalentes de \"FarEast\" para nuestra fuente y configuración regional.
// Si el generador inserta caracteres asiáticos con esta configuración de Fuente, entonces cada run que contenga
// estos caracteres los mostrará usando la fuente/configuración regional \"FarEast\" en lugar de la predeterminada.
// Esto podría ser útil cuando una fuente occidental no tiene representaciones ideales para caracteres asiáticos.
builder->get_Font()->set_NameFarEast(u"SimSun");
builder->get_Font()->set_LocaleIdFarEast(System::MakeObject<System::Globalization::CultureInfo>(u"zh-CN", false)->get_LCID());

// Este texto se mostrará en la fuente/configuración regional predeterminada.
builder->Writeln(u"Hello world!");

// Dado que estos son caracteres asiáticos, este run aplicará nuestros equivalentes de fuente/configuración regional \"FarEast\".
builder->Writeln(u"你好世界");

doc->Save(get_ArtifactsDir() + u"Font.FarEast.docx");
```

## Ver también

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
