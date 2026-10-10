---
title: "Aspose::Words::MailMerging::IMailMergeDataSourceRoot::GetDataSource método"
linktitle: "GetDataSource"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::MailMerging::IMailMergeDataSourceRoot::GetDataSource método. El motor de combinación de correspondencia de Aspose.Words invoca este método cuando encuentra el inicio de una región de combinación de correspondencia de nivel superior en C++."
type: docs
weight: 2000
url: /es/cpp/aspose.words.mailmerging/imailmergedatasourceroot/getdatasource/
---
## IMailMergeDataSourceRoot::GetDataSource method


El motor de combinación de correspondencia de Aspose.Words invoca este método cuando encuentra el inicio de una región de combinación de nivel superior.

```cpp
virtual System::SharedPtr<Aspose::Words::MailMerging::IMailMergeDataSource> Aspose::Words::MailMerging::IMailMergeDataSourceRoot::GetDataSource(System::String tableName)=0
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| tableName | System::String | El nombre de la región de combinación de correspondencia tal como se especifica en el documento plantilla. No distingue entre mayúsculas y minúsculas. |

### ReturnValue

Un objeto de fuente de datos que proporcionará acceso a los registros de datos de la tabla especificada.
## Observaciones


Cuando los motores de combinación de correspondencia de Aspose.Words rellenan un documento con datos y encuentran MERGEFIELD TableStart:TableName, invocan [GetDataSource()](./) en este objeto. Su implementación debe devolver un nuevo objeto de origen de datos. Aspose.Words usará el origen de datos devuelto para rellenar la región de combinación de correspondencia.

Si no existe un origen de datos (tabla) con el nombre especificado, su implementación debe devolver **null**.

## Ver también

* Interface [IMailMergeDataSource](../../imailmergedatasource/)
* Interface [IMailMergeDataSourceRoot](../)
* Namespace [Aspose::Words::MailMerging](../../)
* Library [Aspose.Words for C++](../../../)
