---
title: "Aspose::Words::IRevisionCriteria interface"
linktitle: "IRevisionCriteria"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::IRevisionCriteria interface. Implementera detta gränssnitt om du vill kontrollera när en viss Revision ska accepteras/avvisas eller inte av metoderna Accept()/Reject() i C++."
type: docs
weight: 79500
url: /sv/cpp/aspose.words/irevisioncriteria/
---
## IRevisionCriteria interface


Implementera detta gränssnitt om du vill kontrollera när en viss [Revision](../revision/) ska accepteras/avvisas eller inte av [Accept]()(../)/[Reject]()(../) metoderna.

```cpp
class IRevisionCriteria : public virtual System::Object
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [IsMatch](./ismatch/)(System::SharedPtr\<Aspose::Words::Revision\>) | Kontrollerar om den angivna *revisionen* matchar kriterierna eller inte. |
| static [Type](./type/)() |  |
## Se även

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
