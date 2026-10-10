---
title: "Aspose::Words::Saving::IDocumentSavingCallback interface"
linktitle: "IDocumentSavingCallback"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::IDocumentSavingCallback interface. Implementera detta gränssnitt om du vill ha din egen anpassade metod som anropas under sparandet av ett dokument i C++."
type: docs
weight: 41000
url: /sv/cpp/aspose.words.saving/idocumentsavingcallback/
---
## IDocumentSavingCallback interface


Implementera detta gränssnitt om du vill ha din egen anpassade metod som anropas under sparandet av ett dokument.

```cpp
class IDocumentSavingCallback : public virtual System::Object
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Notify](./notify/)(System::SharedPtr\<Aspose::Words::Saving::DocumentSavingArgs\>) | Detta anropas för att meddela dokumentets sparningsförlopp. |
| static [Type](./type/)() |  |
## Se även

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
