---
title: "Aspose::Words::Fields::IFieldUpdatingCallback interfaz"
linktitle: "IFieldUpdatingCallback"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Fields::IFieldUpdatingCallback interfaz. Implementa esta interfaz si deseas que tus propios métodos personalizados sean llamados durante una actualización de campo en C++."
type: docs
weight: 123000
url: /es/cpp/aspose.words.fields/ifieldupdatingcallback/
---
## IFieldUpdatingCallback interface


Implemente esta interfaz si desea que sus propios métodos personalizados se llamen durante la actualización de un campo.

```cpp
class IFieldUpdatingCallback : public virtual System::Object
```

## Métodos

| Método | Descripción |
| --- | --- |
| virtual [FieldUpdated](./fieldupdated/)(System::SharedPtr\<Aspose::Words::Fields::Field\>) | Un método definido por el usuario que se llama justo después de que se actualiza un campo. |
| virtual [FieldUpdating](./fieldupdating/)(System::SharedPtr\<Aspose::Words::Fields::Field\>) | Un método definido por el usuario que se llama justo antes de que se actualice un campo. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## Ver también

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
