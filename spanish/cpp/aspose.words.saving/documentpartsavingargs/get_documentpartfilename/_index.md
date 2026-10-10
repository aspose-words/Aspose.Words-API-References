---
title: "Método Aspose::Words::Saving::DocumentPartSavingArgs::get_DocumentPartFileName"
linktitle: "get_DocumentPartFileName"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Saving::DocumentPartSavingArgs::get_DocumentPartFileName. Obtiene o establece el nombre de archivo (sin ruta) donde se guardará la parte del documento en C++."
type: docs
weight: 3000
url: /es/cpp/aspose.words.saving/documentpartsavingargs/get_documentpartfilename/
---
## DocumentPartSavingArgs::get_DocumentPartFileName method


Obtiene o establece el nombre de archivo (sin ruta) donde se guardará la parte del documento.

```cpp
System::String Aspose::Words::Saving::DocumentPartSavingArgs::get_DocumentPartFileName() const
```

## Observaciones


Esta propiedad le permite redefinir cómo se generan los nombres de archivo de las partes del documento durante la exportación a HTML o EPUB.

Cuando se invoca la devolución de llamada, esta propiedad contiene el nombre de archivo que fue generado por Aspose.Words. Puede cambiar el valor de esta propiedad para guardar la parte del documento en un archivo diferente. Tenga en cuenta que el nombre de archivo para cada parte debe ser único.

[DocumentPartFileName](./) must contain only the file name without the path. Aspose.Words determines the path for saving using the document file name. If output document file name was not specified, for instance when saving to a stream, this file name is used only for referencing document parts. The same is true when saving to EPUB format.

## Ver también

* Class [DocumentPartSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
