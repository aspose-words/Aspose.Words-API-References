---
title: "Método Aspose::Words::DocumentBase::get_WarningCallback"
linktitle: "get_WarningCallback"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::DocumentBase::get_WarningCallback. Se llama durante varios procedimientos de procesamiento de documentos cuando se detecta un problema que podría resultar en pérdida de datos o de fidelidad de formato en C++."
type: docs
weight: 10000
url: /es/cpp/aspose.words/documentbase/get_warningcallback/
---
## DocumentBase::get_WarningCallback method


Se llama durante varios procedimientos de procesamiento de documentos cuando se detecta un problema que podría resultar en pérdida de fidelidad de datos o formato.

```cpp
System::SharedPtr<Aspose::Words::IWarningCallback> Aspose::Words::DocumentBase::get_WarningCallback() const
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

* Interface [IWarningCallback](../../iwarningcallback/)
* Class [DocumentBase](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
