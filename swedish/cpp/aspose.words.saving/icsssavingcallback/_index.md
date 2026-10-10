---
title: "Aspose::Words::Saving::ICssSavingCallback gränssnitt"
linktitle: "ICssSavingCallback"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::ICssSavingCallback gränssnitt. Implementera detta gränssnitt om du vill kontrollera hur Aspose.Words sparar CSS (Cascading Style Sheet) när du sparar ett dokument till HTML i C++."
type: docs
weight: 39000
url: /sv/cpp/aspose.words.saving/icsssavingcallback/
---
## ICssSavingCallback interface


Implementera detta gränssnitt om du vill kontrollera hur Aspose.Words sparar CSS (Cascading [Style](../../aspose.words/style/) Sheet) när du sparar ett dokument till HTML.

```cpp
class ICssSavingCallback : public virtual System::Object
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| virtual [CssSaving](./csssaving/)(System::SharedPtr\<Aspose::Words::Saving::CssSavingArgs\>) | Kallas när Aspose.Words sparar en CSS (Cascading [Style](../../aspose.words/style/) Sheet). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## Se även

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
