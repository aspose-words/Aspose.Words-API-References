---
title: "Método Aspose::Words::Saving::DocumentPartSavingArgs::get_KeepDocumentPartStreamOpen"
linktitle: "get_KeepDocumentPartStreamOpen"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Saving::DocumentPartSavingArgs::get_KeepDocumentPartStreamOpen. Especifica si Aspose.Words debe mantener el flujo abierto o cerrarlo después de guardar una parte del documento en C++."
type: docs
weight: 5000
url: /es/cpp/aspose.words.saving/documentpartsavingargs/get_keepdocumentpartstreamopen/
---
## DocumentPartSavingArgs::get_KeepDocumentPartStreamOpen method


Especifica si Aspose.Words debe mantener el flujo abierto o cerrarlo después de guardar una parte del documento.

```cpp
bool Aspose::Words::Saving::DocumentPartSavingArgs::get_KeepDocumentPartStreamOpen() const
```

## Observaciones


El valor predeterminado es **false** y Aspose.Words cerrará el flujo que proporcionó en la propiedad [DocumentPartStream](../get_documentpartstream/) después de escribir una parte del documento en él. Especifique **true** para mantener el flujo abierto. Tenga en cuenta que el flujo de salida principal proporcionado en la llamada a [Save()](../) o [Save()](../) nunca será cerrado por Aspose.Words incluso si [KeepDocumentPartStreamOpen](./) está configurado en **false**.

## Ver también

* Class [DocumentPartSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
