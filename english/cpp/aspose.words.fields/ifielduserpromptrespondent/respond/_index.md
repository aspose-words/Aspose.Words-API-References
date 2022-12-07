---
title: Respond
second_title: Aspose.Words for C++ API Reference
description: When implemented, returns a response from the user on prompting. Your implementation should return null to indicate that the user has not responded to the prompt (i.e. the user has pressed the Cancel button in the prompt window).
type: docs
weight: 40
url: /cpp/aspose.words.fields/ifielduserpromptrespondent/respond/
---
## IFieldUserPromptRespondent::Respond method


When implemented, returns a response from the user on prompting. Your implementation should return **null** to indicate that the user has not responded to the prompt (i.e. the user has pressed the Cancel button in the prompt window).

```cpp
virtual System::String Aspose::Words::Fields::IFieldUserPromptRespondent::Respond(System::String promptText, System::String defaultResponse)=0
```


| Parameter | Type | Description |
| --- | --- | --- |
| promptText | System::String | Prompt text (i.e. title of the prompt window). |
| defaultResponse | System::String | Default user response (i.e. initial value contained in the prompt window). |

### ReturnValue

User response (i.e. confirmed value contained in the prompt window).

## See Also

* Interface [IFieldUserPromptRespondent](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words](../../../)
