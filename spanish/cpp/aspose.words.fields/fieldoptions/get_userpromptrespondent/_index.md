---
title: "Aspose::Words::Fields::FieldOptions::get_UserPromptRespondent método"
linktitle: "get_UserPromptRespondent"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Fields::FieldOptions::get_UserPromptRespondent método. Obtiene o establece el respondente a los avisos de usuario durante la actualización de campos en C++."
type: docs
weight: 22000
url: /es/cpp/aspose.words.fields/fieldoptions/get_userpromptrespondent/
---
## FieldOptions::get_UserPromptRespondent method


Obtiene o establece el respondedor a los mensajes del usuario durante la actualización del campo.

```cpp
const System::SharedPtr<Aspose::Words::Fields::IFieldUserPromptRespondent> & Aspose::Words::Fields::FieldOptions::get_UserPromptRespondent() const
```

## Observaciones


Si el valor de esta propiedad se establece en **null**, los campos que requieren respuesta del usuario al solicitarla (como [FieldAsk](../../fieldask/) o [FieldFillIn](../../fieldfillin/)) no se actualizan.

El valor predeterminado es **null**.
## Ver también

* Interface [IFieldUserPromptRespondent](../../ifielduserpromptrespondent/)
* Class [FieldOptions](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
