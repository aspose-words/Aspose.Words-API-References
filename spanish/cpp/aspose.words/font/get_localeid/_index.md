---
title: "Método Aspose::Words::Font::get_LocaleId"
linktitle: "get_LocaleId"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Font::get_LocaleId. Obtiene o establece el identificador de configuración regional (idioma) de los caracteres formateados en C++."
type: docs
weight: 22000
url: /es/cpp/aspose.words/font/get_localeid/
---
## Font::get_LocaleId method


Obtiene o establece el identificador de configuración regional (idioma) de los caracteres formateados.

```cpp
int32_t Aspose::Words::Font::get_LocaleId()
```


## Ejemplos



Muestra cómo establecer la configuración regional del texto que estamos añadiendo con un document builder.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Si establecemos la configuración regional de la fuente a inglés e insertamos texto en ruso,
// el corrector ortográfico de la configuración regional inglesa no reconocerá el texto y lo detectará como un error ortográfico.
builder->get_Font()->set_LocaleId(System::MakeObject<System::Globalization::CultureInfo>(u"en-US", false)->get_LCID());
builder->Writeln(u"Привет!");

// Establezca una configuración regional coincidente para el texto que estamos a punto de añadir para aplicar el corrector ortográfico apropiado.
builder->get_Font()->set_LocaleId(System::MakeObject<System::Globalization::CultureInfo>(u"ru-RU", false)->get_LCID());
builder->Writeln(u"Привет!");

doc->Save(get_ArtifactsDir() + u"Font.LocaleId.docx");
```

## Ver también

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
