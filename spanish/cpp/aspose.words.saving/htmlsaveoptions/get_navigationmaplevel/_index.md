---
title: "Método Aspose::Words::Saving::HtmlSaveOptions::get_NavigationMapLevel"
linktitle: "get_NavigationMapLevel"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Saving::HtmlSaveOptions::get_NavigationMapLevel. Especifica el nivel máximo de encabezados que se incluyen en el mapa de navegación al exportar a formatos EPUB, MOBI o AZW3. El valor predeterminado es %3 en C++."
type: docs
weight: 40500
url: /es/cpp/aspose.words.saving/htmlsaveoptions/get_navigationmaplevel/
---
## HtmlSaveOptions::get_NavigationMapLevel method


Especifica el nivel máximo de encabezados poblados en el mapa de navegación al exportar a los formatos EPUB, MOBI o AZW3. El valor predeterminado es **%3**.

```cpp
int32_t Aspose::Words::Saving::HtmlSaveOptions::get_NavigationMapLevel() const
```

## Observaciones


El mapa de navegación permite a los agentes de usuario proporcionar una forma fácil de navegar a través de la estructura del documento. Normalmente los puntos de navegación corresponden a los encabezados del documento. Para poblar los encabezados hasta el nivel **N**, asigna este valor a [NavigationMapLevel](./).

Por defecto, se poblan tres niveles de encabezados: párrafos con los estilos **Heading 1**, **Heading 2** y **Heading 3**. Puedes establecer esta propiedad a un valor entre 1 y 9 para solicitar el nivel máximo correspondiente. Configurarla en cero reducirá el mapa de navegación solo a la raíz del documento o a las raíces de las partes del documento.

## Ejemplos



Muestra cómo generar la tabla de contenido para documentos Azw3.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Big document.docx");

auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>(Aspose::Words::SaveFormat::Azw3);
options->set_NavigationMapLevel(2);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.CreateAZW3Toc.azw3", options);
```


Muestra cómo generar la tabla de contenido para documentos Mobi.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Big document.docx");

auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>(Aspose::Words::SaveFormat::Mobi);
options->set_NavigationMapLevel(5);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.CreateMobiToc.mobi", options);
```

## Ver también

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
