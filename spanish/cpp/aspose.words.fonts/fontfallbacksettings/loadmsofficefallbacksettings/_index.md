---
title: "Aspose::Words::Fonts::FontFallbackSettings::LoadMsOfficeFallbackSettings método"
linktitle: "LoadMsOfficeFallbackSettings"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Fonts::FontFallbackSettings::LoadMsOfficeFallbackSettings método. Carga configuraciones de reserva predefinidas que imitan la reserva de Microsoft Word y utiliza fuentes de Microsoft Office en C++."
type: docs
weight: 6000
url: /es/cpp/aspose.words.fonts/fontfallbacksettings/loadmsofficefallbacksettings/
---
## FontFallbackSettings::LoadMsOfficeFallbackSettings method


Carga configuraciones de sustitución predefinidas que imitan la sustitución de Microsoft Word y utilizan fuentes de Microsoft Office.

```cpp
void Aspose::Words::Fonts::FontFallbackSettings::LoadMsOfficeFallbackSettings()
```


## Ejemplos



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
