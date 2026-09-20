---
title: "Aspose::Words::Fields::IFieldUserPromptRespondent::Respond método"
linktitle: "Respond"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Fields::IFieldUserPromptRespondent::Respond método. Cuando se implementa, devuelve una respuesta del usuario al solicitarla. Su implementación debe devolver null para indicar que el usuario no ha respondido al aviso (es decir, que el usuario ha pulsado el botón Cancelar en la ventana del aviso) en C++."
type: docs
weight: 4000
url: /es/cpp/aspose.words.fields/ifielduserpromptrespondent/respond/
---
## IFieldUserPromptRespondent::Respond method


Cuando se implementa, devuelve una respuesta del usuario al solicitar. Su implementación debe devolver **null** para indicar que el usuario no ha respondido al mensaje (es decir, el usuario ha pulsado el botón Cancelar en la ventana del mensaje).

```cpp
virtual System::String Aspose::Words::Fields::IFieldUserPromptRespondent::Respond(System::String promptText, System::String defaultResponse)=0
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| promptText | System::String | Texto del aviso (es decir, título de la ventana del aviso). |
| defaultResponse | System::String | Respuesta predeterminada del usuario (es decir, valor inicial contenido en la ventana del aviso). |

### ReturnValue

Respuesta del usuario (es decir, valor confirmado contenido en la ventana del aviso).

## Ver también

* Interface [IFieldUserPromptRespondent](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
