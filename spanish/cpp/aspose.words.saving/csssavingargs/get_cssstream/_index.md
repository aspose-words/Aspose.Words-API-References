---
title: "Aspose::Words::Saving::CssSavingArgs::get_CssStream método"
linktitle: "get_CssStream"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Saving::CssSavingArgs::get_CssStream método. Permite especificar el flujo donde se guardará la información CSS en C++."
type: docs
weight: 2000
url: /es/cpp/aspose.words.saving/csssavingargs/get_cssstream/
---
## CssSavingArgs::get_CssStream method


Permite especificar el flujo donde se guardará la información CSS.

```cpp
System::SharedPtr<System::IO::Stream> Aspose::Words::Saving::CssSavingArgs::get_CssStream() const
```

## Observaciones


Esta propiedad le permite guardar la información CSS en un flujo.

El valor predeterminado es **null**. Esta propiedad no suprime el guardado de la información CSS en un archivo ni la incrustación en el documento HTML. Para suprimir la exportación de CSS use la propiedad [IsExportNeeded](../get_isexportneeded/).

Al usar [ICssSavingCallback](../../icsssavingcallback/) no puede sustituir CSS por otro. Está destinado solo a guardar CSS en un flujo.

## Ver también

* Class [CssSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
