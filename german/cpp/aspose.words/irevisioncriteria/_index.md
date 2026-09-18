---
title: "Aspose::Words::IRevisionCriteria interface"
linktitle: "IRevisionCriteria"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::IRevisionCriteria interface. Implementieren Sie dieses Interface, wenn Sie steuern möchten, wann bestimmte Revisionen von den Methoden Accept()/Reject() in C++ akzeptiert/abgelehnt werden sollen oder nicht."
type: docs
weight: 79500
url: /de/cpp/aspose.words/irevisioncriteria/
---
## IRevisionCriteria interface


Implementieren Sie dieses Interface, wenn Sie steuern möchten, wann bestimmte [Revision](../revision/) von den [Accept()](../)/[Reject()](../) Methoden akzeptiert/abgelehnt werden soll oder nicht.

```cpp
class IRevisionCriteria : public virtual System::Object
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [IsMatch](./ismatch/)(System::SharedPtr\<Aspose::Words::Revision\>) | Überprüft, ob die angegebene *revision* den Kriterien entspricht oder nicht. |
| static [Type](./type/)() |  |
## Siehe auch

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
