---
title: "Aspose::Words::Saving::FontSavingArgs::get_IsSubsettingNeeded método"
linktitle: "get_IsSubsettingNeeded"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Saving::FontSavingArgs::get_IsSubsettingNeeded. Permite especificar si la fuente actual se subestablecerá antes de exportarse como un recurso de fuente en C++."
type: docs
weight: 8000
url: /es/cpp/aspose.words.saving/fontsavingargs/get_issubsettingneeded/
---
## FontSavingArgs::get_IsSubsettingNeeded method


Permite especificar si la fuente actual se subestablecerá antes de exportarse como un recurso de fuente.

```cpp
bool Aspose::Words::Saving::FontSavingArgs::get_IsSubsettingNeeded() const
```

## Observaciones


[Fonts](../../../aspose.words.fonts/) can be exported as complete original font files or subsetted to include only the characters that are used in the document. Subsetting allows to reduce the resulting font resource size.

Por defecto, Aspose.Words decide si realizar o no el subestablecimiento comparando el tamaño del archivo de fuente original con el especificado en [FontResourcesSubsettingSizeThreshold](../../htmlsaveoptions/get_fontresourcessubsettingsizethreshold/). Puede anular este comportamiento para fuentes individuales estableciendo la propiedad [IsSubsettingNeeded](./).
## Ver también

* Class [FontSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
