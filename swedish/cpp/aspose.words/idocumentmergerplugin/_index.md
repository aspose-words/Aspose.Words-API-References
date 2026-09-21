---
title: "Aspose::Words::IDocumentMergerPlugin interface"
linktitle: "IDocumentMergerPlugin"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::IDocumentMergerPlugin interface. Definierar ett gränssnitt för extern sammanslagnings‑plugin som kan slå ihop PDF‑dokument i C++."
type: docs
weight: 76500
url: /sv/cpp/aspose.words/idocumentmergerplugin/
---
## IDocumentMergerPlugin interface


Definierar ett gränssnitt för ett externt sammanslagnings-plugin som kan slå samman Pdf-dokument.

```cpp
class IDocumentMergerPlugin : public virtual System::Object
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Merge](./merge/)(System::SharedPtr\<System::IO::Stream\>, System::ArrayPtr\<System::SharedPtr\<System::IO::Stream\>\>, System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\>) | Slår ihop de angivna inmatnings‑PDF‑dokumenten till ett enda utmatnings‑PDF‑dokument med hjälp av specificerade in‑ och utströmar. |
| static [Type](./type/)() |  |
## Se även

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
