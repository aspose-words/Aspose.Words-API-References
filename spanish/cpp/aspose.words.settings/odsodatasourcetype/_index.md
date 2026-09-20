---
title: "Aspose::Words::Settings::OdsoDataSourceType enum"
linktitle: "OdsoDataSourceType"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Settings::OdsoDataSourceType enum. Especifica el tipo de fuente de datos externa a la que se debe conectar como parte de la información de conexión ODSO en C++."
type: docs
weight: 19000
url: /es/cpp/aspose.words.settings/odsodatasourcetype/
---
## OdsoDataSourceType enum


Especifica el tipo de la fuente de datos externa a la que se conectará como parte de la información de conexión ODSO.

```cpp
enum class OdsoDataSourceType
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Text | 0 | Especifica que un documento dado ha sido conectado a un archivo de texto. Posiblemente wdMergeSubTypeOther. |
| Database | 1 | Especifica que un documento dado ha sido conectado a una base de datos. Posiblemente wdMergeSubTypeAccess. |
| AddressBook | 2 | Especifica que un documento dado ha sido conectado a una libreta de contactos. Posiblemente wdMergeSubTypeOAL. |
| Document1 | 3 | Especifica que un documento dado ha sido conectado a otro formato de documento compatible con la aplicación productora. Posiblemente wdMergeSubTypeOLEDBWord. |
| Document2 | 4 | Especifica que un documento dado ha sido conectado a otro formato de documento compatible con la aplicación productora. Posiblemente wdMergeSubTypeWorks. |
| Native | 5 | Especifica que un documento dado ha sido conectado a otro formato de documento nativo de la aplicación productora. Posiblemente wdMergeSubTypeOLEDBText. |
| Email | 6 | Especifica que un documento dado ha sido conectado a una aplicación de correo electrónico. Posiblemente wdMergeSubTypeOutlook. |
| None | 7 | El tipo de la fuente de datos externa no está especificado. Posiblemente wdMergeSubTypeWord. |
| Legacy | 8 | Especifica que un documento dado ha sido conectado a un formato de documento legado compatible con la aplicación productora. Posiblemente wdMergeSubTypeWord2000. |
| Master | 9 | Especifica que un documento dado ha sido conectado a una fuente de datos que agrega otras fuentes de datos. |
| Default | n/a | Igual a [None](./). |

## Observaciones


La especificación OOXML es muy vaga para este enumerado. Supongo que podría corresponder a la enumeración WdMergeSubType [http://msdn.microsoft.com/en-us/library/bb237801.aspx](http://msdn.microsoft.com/en-us/library/bb237801.aspx).

## Ver también

* Namespace [Aspose::Words::Settings](../)
* Library [Aspose.Words for C++](../../)
