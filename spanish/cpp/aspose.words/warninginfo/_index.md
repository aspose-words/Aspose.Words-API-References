---
title: "Clase Aspose::Words::WarningInfo"
linktitle: "WarningInfo"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Clase Aspose::Words::WarningInfo. Contiene información sobre una advertencia que Aspose.Words emitió durante la carga o guardado del documento. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 74000
url: /es/cpp/aspose.words/warninginfo/
---
## WarningInfo class


Contiene información sobre una advertencia que Aspose.Words emitió durante la carga o guardado del documento. Para obtener más información, visite el artículo de documentación [Programming with Documents](https://docs.aspose.com/words/cpp/programming-with-documents/).

```cpp
class WarningInfo : public System::Object
```

## Métodos

| Método | Descripción |
| --- | --- |
| [get_Description](./get_description/)() const | Devuelve la descripción de la advertencia. |
| [get_Source](./get_source/)() const | Devuelve el origen de la advertencia. |
| [get_WarningType](./get_warningtype/)() const | Devuelve el tipo de la advertencia. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## Observaciones


No crea instancias de esta clase. Los objetos de esta clase son creados y pasados por Aspose.Words al método [Warning()](../iwarningcallback/warning/).

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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
