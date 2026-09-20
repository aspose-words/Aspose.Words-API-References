---
title: "Método Aspose::Words::MailMerging::IMailMergeDataSource::GetChildDataSource"
linktitle: "GetChildDataSource"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::MailMerging::IMailMergeDataSource::GetChildDataSource. El motor de combinación de correspondencia de Aspose.Words invoca este método cuando encuentra el inicio de una región de combinación de correspondencia anidada en C++."
type: docs
weight: 3000
url: /es/cpp/aspose.words.mailmerging/imailmergedatasource/getchilddatasource/
---
## IMailMergeDataSource::GetChildDataSource method


El motor de combinación de correspondencia Aspose.Words invoca este método cuando encuentra el inicio de una región de combinación de correspondencia anidada.

```cpp
virtual System::SharedPtr<Aspose::Words::MailMerging::IMailMergeDataSource> Aspose::Words::MailMerging::IMailMergeDataSource::GetChildDataSource(System::String tableName)=0
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| tableName | System::String | El nombre de la región de combinación de correspondencia tal como se especifica en el documento plantilla. No distingue entre mayúsculas y minúsculas. |

### ReturnValue

Un objeto de fuente de datos que proporcionará acceso a los registros de datos de la tabla especificada.
## Observaciones


Cuando los motores de combinación de correspondencia de Aspose.Words rellenan una región de combinación de correspondencia con datos y encuentran el inicio de una región de combinación de correspondencia anidada en forma de MERGEFIELD TableStart:TableName, invocan [GetChildDataSource()](./) en el objeto de fuente de datos actual. Su implementación debe devolver un nuevo objeto de fuente de datos que proporcione acceso a los registros hijos del registro padre actual. Aspose.Words utilizará la fuente de datos devuelta para rellenar la región de combinación de correspondencia anidada.

A continuación se presentan las reglas que debe seguir la implementación de [GetChildDataSource()](./).

Si la tabla representada por este objeto de fuente de datos tiene una tabla hija (detalle) relacionada con el nombre especificado, entonces su implementación debe devolver un nuevo objeto [IMailMergeDataSource](../) que proporcione acceso a los registros hijos del registro actual. Un ejemplo de esto es la relación Orders / OrderDetails. Supongamos que el objeto [IMailMergeDataSource](../) actual representa la tabla Orders y tiene un registro de pedido actual. A continuación, Aspose.Words encuentra "MERGEFIELD TableStart:OrderDetails" en el documento e invoca [GetChildDataSource()](./). Necesita crear y devolver un objeto [IMailMergeDataSource](../) que permita a Aspose.Words acceder al registro OrderDetails del pedido actual.

Si este objeto de fuente de datos no tiene una relación con la tabla cuyo nombre se especificó, entonces debe devolver un objeto [IMailMergeDataSource](../) que proporcione acceso a todos los registros de la tabla especificada.

Si una tabla con el nombre especificado no existe, su implementación debe devolver **null**.

## Ver también

* Interface [IMailMergeDataSource](../)
* Interface [IMailMergeDataSource](../)
* Namespace [Aspose::Words::MailMerging](../../)
* Library [Aspose.Words for C++](../../../)
