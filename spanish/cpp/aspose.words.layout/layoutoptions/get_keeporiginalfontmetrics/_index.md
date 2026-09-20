---
title: "Aspose::Words::Layout::LayoutOptions::get_KeepOriginalFontMetrics método"
linktitle: "get_KeepOriginalFontMetrics"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Layout::LayoutOptions::get_KeepOriginalFontMetrics método. Obtiene o establece una indicación de si se deben usar las métricas de fuente originales después de la sustitución de fuentes. El valor predeterminado es true en C++."
type: docs
weight: 6500
url: /es/cpp/aspose.words.layout/layoutoptions/get_keeporiginalfontmetrics/
---
## LayoutOptions::get_KeepOriginalFontMetrics method


Obtiene o establece una indicación de si se deben usar las métricas de fuente originales después de la sustitución de fuentes. El valor predeterminado es **true**.

```cpp
bool Aspose::Words::Layout::LayoutOptions::get_KeepOriginalFontMetrics() const
```


## Ejemplos



Muestra cómo establecer la propiedad para encontrar la coincidencia más cercana de una fuente faltante entre las fuentes disponibles.
```cpp
// Abre un documento que contiene texto formateado con una fuente que no existe en ninguna de nuestras fuentes.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Missing font.docx");

// Asigna una devolución de llamada para manejar advertencias de sustitución de fuentes.
auto warningCollector = System::MakeObject<Aspose::Words::WarningInfoCollection>();
doc->set_WarningCallback(warningCollector);

// Establezca un nombre de fuente predeterminado y habilite la sustitución de fuentes.
auto fontSettings = System::MakeObject<Aspose::Words::Fonts::FontSettings>();
fontSettings->get_SubstitutionSettings()->get_DefaultFontSubstitution()->set_DefaultFontName(u"Arial");
fontSettings->get_SubstitutionSettings()->get_FontInfoSubstitution()->set_Enabled(true);

// Se deben usar las métricas de la fuente original después de la sustitución de fuentes.
doc->get_LayoutOptions()->set_KeepOriginalFontMetrics(true);

// Obtendremos una advertencia de sustitución de fuentes si guardamos un documento con una fuente faltante.
doc->set_FontSettings(fontSettings);
doc->Save(get_ArtifactsDir() + u"FontSettings.EnableFontSubstitution.pdf");

for (auto&& info : warningCollector)
{
    if (info->get_WarningType() == Aspose::Words::WarningType::FontSubstitution)
    {
        std::cout << info->get_Description() << std::endl;
    }
}
```

## Ver también

* Class [LayoutOptions](../)
* Namespace [Aspose::Words::Layout](../../)
* Library [Aspose.Words for C++](../../../)
