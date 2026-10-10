---
title: "Aspose::Words::Fields::IFieldUserPromptRespondent::Respond-metoden"
linktitle: "Respond"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fields::IFieldUserPromptRespondent::Respond-metoden. När den implementeras returnerar den ett svar från användaren vid en prompt. Din implementation bör returnera null för att indikera att användaren inte har svarat på prompten (dvs. att användaren har tryckt på Avbryt‑knappen i promptfönstret) i C++."
type: docs
weight: 4000
url: /sv/cpp/aspose.words.fields/ifielduserpromptrespondent/respond/
---
## IFieldUserPromptRespondent::Respond method


När den implementeras returnerar den ett svar från användaren vid prompt. Din implementation bör returnera **null** för att indikera att användaren inte har svarat på prompten (dvs. att användaren har tryckt på Avbryt‑knappen i promptfönstret).

```cpp
virtual System::String Aspose::Words::Fields::IFieldUserPromptRespondent::Respond(System::String promptText, System::String defaultResponse)=0
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| promptText | System::String | Prompt‑text (dvs. titeln på prompt‑fönstret). |
| defaultResponse | System::String | Standardanvändarsvar (dvs. initialvärdet som finns i prompt‑fönstret). |

### ReturnValue

Användarsvar (dvs. bekräftat värde som finns i prompt‑fönstret).

## Se även

* Interface [IFieldUserPromptRespondent](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
