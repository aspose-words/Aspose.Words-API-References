---
title: "Aspose::Words::Replacing::IReplacingCallback interface"
linktitle: "IReplacingCallback"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Replacing::IReplacingCallback‑gränssnitt. Implementera detta gränssnitt om du vill ha din egen anpassade metod som anropas under en sök‑och‑ersätt‑operation i C++."
type: docs
weight: 3000
url: /sv/cpp/aspose.words.replacing/ireplacingcallback/
---
## IReplacingCallback interface


Implementera detta gränssnitt om du vill ha din egen anpassade metod som anropas under en sök‑och‑ersätt‑operation.

```cpp
class IReplacingCallback : public virtual System::Object
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Replacing](./replacing/)(System::SharedPtr\<Aspose::Words::Replacing::ReplacingArgs\>) | En användardefinierad metod som anropas under en ersättningsoperation för varje matchning som hittas precis innan en ersättning görs. |
| static [Type](./type/)() |  |
## Se även

* Namespace [Aspose::Words::Replacing](../)
* Library [Aspose.Words for C++](../../)
