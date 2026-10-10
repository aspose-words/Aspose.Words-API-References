---
title: "Enum Aspose::Words::WarningType"
linktitle: "WarningType"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Enum Aspose::Words::WarningType. Especifica el tipo de advertencia que emite Aspose.Words durante la carga o guardado de documentos en C++."
type: docs
weight: 129000
url: /es/cpp/aspose.words/warningtype/
---
## WarningType enum


Especifica el tipo de advertencia que emite Aspose.Words durante la carga o guardado del documento.

```cpp
enum class WarningType
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| DataLossCategory | 255 | Algún texto/caracter/imagen u otros datos faltarán ya sea del árbol del documento después de la carga, o del documento creado después del guardado. |
| DataLoss | 1 | Pérdida de datos genérica, sin código específico. |
| MajorFormattingLossCategory | 65280 | El documento resultante o una ubicación particular en él podría verse sustancialmente diferente comparado con el documento original. |
| MajorFormattingLoss | 256 | Pérdida mayor de formato genérica, sin código específico. |
| MinorFormattingLossCategory | 16711680 | El documento resultante o una ubicación particular en él podría verse algo diferente comparado con el documento original. |
| MinorFormattingLoss | 65536 | Pérdida menor de formato genérica, sin código específico. |
| FontSubstitution | 131072 | [Font](../font/) ha sido sustituido. |
| FontEmbedding | 262144 | Pérdida de información de fuentes incrustadas durante el guardado del documento. |
| UnexpectedContentCategory | 251658240 | Algunos contenidos del documento fuente no pudieron ser reconocidos (es decir, no son compatibles), lo que puede o no causar problemas o resultar en pérdida de datos/formato. |
| UnexpectedContent | 16777216 | Contenido inesperado genérico, sin código específico. |
| Sugerencia | 268435456 | Advierte de un posible problema o sugiere una mejora. |


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
