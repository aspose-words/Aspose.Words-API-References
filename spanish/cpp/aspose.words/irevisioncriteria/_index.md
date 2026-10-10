---
title: "Aspose::Words::IRevisionCriteria interface"
linktitle: "IRevisionCriteria"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::IRevisionCriteria interface. Implemente esta interfaz si desea controlar cuándo cierta Revisión debe ser aceptada/rechazada o no mediante los métodos Accept()/Reject() en C++."
type: docs
weight: 79500
url: /es/cpp/aspose.words/irevisioncriteria/
---
## IRevisionCriteria interface


Implemente esta interfaz si desea controlar cuándo cierta [Revision](../revision/) debe ser aceptada/rechazada o no mediante los métodos [Accept()](../)/[Reject()](../).

```cpp
class IRevisionCriteria : public virtual System::Object
```

## Métodos

| Método | Descripción |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [IsMatch](./ismatch/)(System::SharedPtr\<Aspose::Words::Revision\>) | Comprueba si la *revision* especificada coincide o no con los criterios. |
| static [Type](./type/)() |  |
## Ver también

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
