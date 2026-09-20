---
title: "Aspose::Words::EditorType enumeración"
linktitle: "EditorType"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::EditorType enumeración. Especifica el conjunto de alias posibles (o grupos de edición) que pueden usarse como alias para determinar si el usuario actual podrá editar un rango único definido por un rango editable dentro de un documento en C++."
type: docs
weight: 88000
url: /es/cpp/aspose.words/editortype/
---
## EditorType enum


Especifica el conjunto de alias posibles (o grupos de edición) que pueden usarse como alias para determinar si al usuario actual se le permite editar un rango único definido por un rango editable dentro de un documento.

```cpp
enum class EditorType
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| No especificado | 0 | Indica que el tipo de editor no está especificado. |
| Administradores | 1 | Especifica que los usuarios asociados al grupo Administradores podrán editar rangos editables usando este tipo de edición cuando la protección del documento está habilitada. |
| Colaboradores | 2 | Especifica que los usuarios asociados al grupo Colaboradores podrán editar rangos editables usando este tipo de edición cuando la protección del documento está habilitada. |
| Actual | 3 | Especifica que los usuarios asociados al grupo Actual podrán editar rangos editables usando este tipo de edición cuando la protección del documento está habilitada. |
| Editores | 4 | Especifica que los usuarios asociados al grupo Editores podrán editar rangos editables usando este tipo de edición cuando la protección del documento está habilitada. |
| Todos | 5 | Especifica que todos los usuarios que abran el documento podrán editar rangos editables usando este tipo de edición cuando la protección del documento está habilitada. |
| None | 6 | Especifica que ninguno de los usuarios que abran el documento podrá editar rangos editables usando este tipo de edición cuando la protección del documento está habilitada. |
| Propietarios | 7 | Especifica que los usuarios asociados al grupo Owners podrán editar rangos editables usando este tipo de edición cuando la protección del documento está habilitada. |
| Default | n/a | Lo mismo que [Unspecified](./). |

## Ver también

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
