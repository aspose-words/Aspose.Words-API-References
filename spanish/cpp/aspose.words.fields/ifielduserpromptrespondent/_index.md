---
title: "Aspose::Words::Fields::IFieldUserPromptRespondent interface"
linktitle: "IFieldUserPromptRespondent"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Fields::IFieldUserPromptRespondent interface. Representa al respondedor de los mensajes al usuario durante la actualización de campos en C++."
type: docs
weight: 125000
url: /es/cpp/aspose.words.fields/ifielduserpromptrespondent/
---
## IFieldUserPromptRespondent interface


Representa al respondedor de los mensajes al usuario durante la actualización del campo.

```cpp
class IFieldUserPromptRespondent : public virtual System::Object
```

## Métodos

| Método | Descripción |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Respond](./respond/)(System::String, System::String) | Cuando se implementa, devuelve una respuesta del usuario al solicitar. Su implementación debe devolver **null** para indicar que el usuario no ha respondido al mensaje (es decir, el usuario ha pulsado el botón Cancelar en la ventana del mensaje). |
| static [Type](./type/)() |  |
## Ver también

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
