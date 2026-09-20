---
title: "Método Aspose::Words::EditableRange::get_SingleUser"
linktitle: "get_SingleUser"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::EditableRange::get_SingleUser. Devuelve o establece el usuario único para el rango editable en C++."
type: docs
weight: 6000
url: /es/cpp/aspose.words/editablerange/get_singleuser/
---
## EditableRange::get_SingleUser method


Devuelve o establece el usuario único para el rango editable.

```cpp
System::String Aspose::Words::EditableRange::get_SingleUser()
```

## Observaciones


Este editor puede almacenarse en una de las siguientes formas:

DOMAIN\\Username - para usuarios cuyo acceso será autenticado usando las credenciales de dominio del usuario actual.

user@domain.com - para usuarios cuyo acceso será autenticado usando la dirección de correo electrónico del usuario como credenciales.

user - para usuarios cuyo acceso será autenticado usando las credenciales de la máquina del usuario actual.

El usuario único y el grupo de editores no pueden establecerse simultáneamente para el rango editable específico; si se establece uno, el otro se borrará.
## Ver también

* Class [EditableRange](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
