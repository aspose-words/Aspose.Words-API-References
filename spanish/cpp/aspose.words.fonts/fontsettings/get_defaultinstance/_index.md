---
title: "Aspose::Words::Fonts::FontSettings::get_DefaultInstance método"
linktitle: "get_DefaultInstance"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Fonts::FontSettings::get_DefaultInstance método. Configuración de fuentes predeterminada estática en C++."
type: docs
weight: 1000
url: /es/cpp/aspose.words.fonts/fontsettings/get_defaultinstance/
---
## FontSettings::get_DefaultInstance method


Configuración de fuentes predeterminada estática.

```cpp
static System::SharedPtr<Aspose::Words::Fonts::FontSettings> Aspose::Words::Fonts::FontSettings::get_DefaultInstance()
```


## Ejemplos



Muestra cómo configurar la instancia de configuración de fuentes predeterminada.
```cpp
// Configure la instancia de configuración de fuentes predeterminada para usar la fuente "Courier New"
// como sustituto de respaldo cuando intentamos usar una fuente desconocida.
Aspose::Words::Fonts::FontSettings::get_DefaultInstance()->get_SubstitutionSettings()->get_DefaultFontSubstitution()->set_DefaultFontName(u"Courier New");

ASSERT_TRUE(Aspose::Words::Fonts::FontSettings::get_DefaultInstance()->get_SubstitutionSettings()->get_DefaultFontSubstitution()->get_Enabled());

auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Name(u"Non-existent font");
builder->Write(u"Hello world!");

// Este documento no tiene una configuración de FontSettings. Cuando renderizamos el documento,
// la instancia predeterminada de FontSettings resolverá la fuente faltante.
// Aspose.Words usará "Courier New" para renderizar texto que utiliza la fuente desconocida.
ASSERT_TRUE(System::TestTools::IsNull(doc->get_FontSettings()));

doc->Save(get_ArtifactsDir() + u"FontSettings.DefaultFontInstance.pdf");
```

## Ver también

* Class [FontSettings](../)
* Class [FontSettings](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
