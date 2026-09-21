---
title: "Aspose::Words::Fields::IFieldUserPromptRespondent gränssnitt"
linktitle: "IFieldUserPromptRespondent"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fields::IFieldUserPromptRespondent gränssnitt. Representerar svararen på användarpromptar under fältuppdatering i C++."
type: docs
weight: 125000
url: /sv/cpp/aspose.words.fields/ifielduserpromptrespondent/
---
## IFieldUserPromptRespondent interface


Representerar svararen på användarpromptar under fältuppdatering.

```cpp
class IFieldUserPromptRespondent : public virtual System::Object
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Respond](./respond/)(System::String, System::String) | När den implementeras returnerar den ett svar från användaren vid prompt. Din implementation bör returnera **null** för att indikera att användaren inte har svarat på prompten (dvs. att användaren har tryckt på Avbryt‑knappen i promptfönstret). |
| static [Type](./type/)() |  |
## Se även

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
