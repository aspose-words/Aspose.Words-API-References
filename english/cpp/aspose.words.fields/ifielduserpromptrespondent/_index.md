---
title: Aspose::Words::Fields::IFieldUserPromptRespondent interface
linktitle: IFieldUserPromptRespondent
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fields::IFieldUserPromptRespondent interface. Represents the respondent to user prompts during field update in C++.'
type: docs
weight: 125000
url: /cpp/aspose.words.fields/ifielduserpromptrespondent/
---
## IFieldUserPromptRespondent interface


Represents the respondent to user prompts during field update.

```cpp
class IFieldUserPromptRespondent : public virtual System::Object
```

## Methods

| Method | Description |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Respond](./respond/)(System::String, System::String) | When implemented, returns a response from the user on prompting. Your implementation should return **null** to indicate that the user has not responded to the prompt (i.e. the user has pressed the Cancel button in the prompt window). |
| static [Type](./type/)() |  |
## See Also

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
