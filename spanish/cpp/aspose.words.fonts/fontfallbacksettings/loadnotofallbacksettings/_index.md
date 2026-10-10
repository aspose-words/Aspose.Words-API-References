---
title: "Método Aspose::Words::Fonts::FontFallbackSettings::LoadNotoFallbackSettings"
linktitle: "LoadNotoFallbackSettings"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Fonts::FontFallbackSettings::LoadNotoFallbackSettings. Carga configuraciones de sustitución predefinidas que utilizan fuentes Google Noto en C++."
type: docs
weight: 7000
url: /es/cpp/aspose.words.fonts/fontfallbacksettings/loadnotofallbacksettings/
---
## FontFallbackSettings::LoadNotoFallbackSettings method


Carga configuraciones de sustitución predefinidas que utilizan fuentes Google Noto.

```cpp
void Aspose::Words::Fonts::FontFallbackSettings::LoadNotoFallbackSettings()
```


## Ejemplos



Muestra cómo agregar configuraciones de sustitución de fuentes predefinidas para fuentes Google Noto.
```cpp
auto fontSettings = System::MakeObject<Aspose::Words::Fonts::FontSettings>();

// Estas son fuentes gratuitas licenciadas bajo la SIL Open Font License.
// Podemos descargar las fuentes aquí:
// https://www.google.com/get/noto/#sans-lgc
fontSettings->SetFontsFolder(get_FontsDir() + u"Noto", false);

// Tenga en cuenta que las configuraciones predefinidas solo usan fuentes Noto estilo Sans con peso regular.
// Algunas de las fuentes Noto utilizan características tipográficas avanzadas.
// Las fuentes con tipografía avanzada pueden no renderizarse correctamente ya que Aspose.Words actualmente no las admite.
fontSettings->get_FallbackSettings()->LoadNotoFallbackSettings();
fontSettings->get_SubstitutionSettings()->get_FontInfoSubstitution()->set_Enabled(false);
fontSettings->get_SubstitutionSettings()->get_DefaultFontSubstitution()->set_DefaultFontName(u"Noto Sans");

auto doc = System::MakeObject<Aspose::Words::Document>();
doc->set_FontSettings(fontSettings);
```


Muestra cómo cargar configuraciones de sustitución de fuentes predefinidas.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

auto fontSettings = System::MakeObject<Aspose::Words::Fonts::FontSettings>();
doc->set_FontSettings(fontSettings);
System::SharedPtr<Aspose::Words::Fonts::FontFallbackSettings> fontFallbackSettings = fontSettings->get_FallbackSettings();

// Guarde el esquema de fuentes de reserva predeterminado en un documento XML.
// Por ejemplo, uno de los elementos tiene un valor de "0C00-0C7F" para Range y un valor correspondiente "Vani" para FallbackFonts.
// Esto significa que si la fuente que usa algún texto no tiene símbolos para el bloque Unicode 0x0C00-0x0C7F,
// el esquema de reserva utilizará símbolos de la fuente sustituta "Vani".
fontFallbackSettings->Save(get_ArtifactsDir() + u"FontSettings.FallbackSettings.Default.xml");

// A continuación se presentan dos esquemas de reserva de fuentes predefinidos entre los que podemos elegir.
// 1 -  Utilice el esquema predeterminado de Microsoft Office, que es el mismo que el predeterminado:
fontFallbackSettings->LoadMsOfficeFallbackSettings();
fontFallbackSettings->Save(get_ArtifactsDir() + u"FontSettings.FallbackSettings.LoadMsOfficeFallbackSettings.xml");

// 2 -  Utilice el esquema construido a partir de fuentes Google Noto:
fontFallbackSettings->LoadNotoFallbackSettings();
fontFallbackSettings->Save(get_ArtifactsDir() + u"FontSettings.FallbackSettings.LoadNotoFallbackSettings.xml");
```

## Ver también

* Class [FontFallbackSettings](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
