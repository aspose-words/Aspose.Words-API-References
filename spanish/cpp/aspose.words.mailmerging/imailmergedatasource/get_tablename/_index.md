---
title: "Método Aspose::Words::MailMerging::IMailMergeDataSource::get_TableName"
linktitle: "get_TableName"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::MailMerging::IMailMergeDataSource::get_TableName. Devuelve el nombre de la fuente de datos en C++."
type: docs
weight: 2000
url: /es/cpp/aspose.words.mailmerging/imailmergedatasource/get_tablename/
---
## IMailMergeDataSource::get_TableName method


Devuelve el nombre de la fuente de datos.

```cpp
virtual System::String Aspose::Words::MailMerging::IMailMergeDataSource::get_TableName()=0
```


### ReturnValue

El nombre de la fuente de datos. Cadena vacía si la fuente de datos no tiene nombre.
## Observaciones


Si está implementando [IMailMergeDataSource](../), devuelva el nombre de la fuente de datos desde esta propiedad.

Aspose.Words utiliza este nombre para compararlo con el nombre de la región de combinación de correspondencia especificado en el documento plantilla. La comparación entre el nombre de la fuente de datos y el nombre de la región de combinación de correspondencia no distingue entre mayúsculas y minúsculas.

## Ver también

* Interface [IMailMergeDataSource](../)
* Namespace [Aspose::Words::MailMerging](../../)
* Library [Aspose.Words for C++](../../../)
