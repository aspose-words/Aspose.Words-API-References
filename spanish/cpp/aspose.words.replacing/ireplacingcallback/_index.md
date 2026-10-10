---
title: "interfaz Aspose::Words::Replacing::IReplacingCallback"
linktitle: "IReplacingCallback"
second_title: "Referencia de API de Aspose.Words para C++"
description: "interfaz Aspose::Words::Replacing::IReplacingCallback. Implemente esta interfaz si desea tener su propio método personalizado llamado durante una operación de buscar y reemplazar en C++."
type: docs
weight: 3000
url: /es/cpp/aspose.words.replacing/ireplacingcallback/
---
## IReplacingCallback interface


Implemente esta interfaz si desea tener su propio método personalizado llamado durante una operación de búsqueda y reemplazo.

```cpp
class IReplacingCallback : public virtual System::Object
```

## Métodos

| Método | Descripción |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Replacing](./replacing/)(System::SharedPtr\<Aspose::Words::Replacing::ReplacingArgs\>) | Un método definido por el usuario que se llama durante una operación de reemplazo para cada coincidencia encontrada justo antes de que se realice un reemplazo. |
| static [Type](./type/)() |  |
## Ver también

* Namespace [Aspose::Words::Replacing](../)
* Library [Aspose.Words for C++](../../)
