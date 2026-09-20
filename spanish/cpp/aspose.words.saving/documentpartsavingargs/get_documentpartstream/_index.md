---
title: "Aspose::Words::Saving::DocumentPartSavingArgs::get_DocumentPartStream método"
linktitle: "get_DocumentPartStream"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Saving::DocumentPartSavingArgs::get_DocumentPartStream método. Permite especificar el flujo donde la parte del documento se guardará en C++."
type: docs
weight: 4000
url: /es/cpp/aspose.words.saving/documentpartsavingargs/get_documentpartstream/
---
## DocumentPartSavingArgs::get_DocumentPartStream method


Permite especificar el flujo donde se guardará la parte del documento.

```cpp
System::SharedPtr<System::IO::Stream> Aspose::Words::Saving::DocumentPartSavingArgs::get_DocumentPartStream() const
```

## Observaciones


Esta propiedad le permite guardar partes del documento en flujos en lugar de archivos durante la exportación HTML.

El valor predeterminado es **null**. Cuando esta propiedad es **null**, la parte del documento se guardará en un archivo especificado en la propiedad [DocumentPartFileName](../get_documentpartfilename/).

Cuando se solicita guardar en un flujo en formato HTML mediante [Save()](../) o [Save()](../) y la primera parte del documento está a punto de guardarse, Aspose.Words sugiere aquí el flujo de salida principal pasado inicialmente por el llamador.

Al guardar en formato EPUB, que es un formato contenedor basado en HTML, no se puede especificar [DocumentPartStream](./) porque todas las partes subsidiarias se encapsularán en un único paquete de salida.

## Ver también

* Class [DocumentPartSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
