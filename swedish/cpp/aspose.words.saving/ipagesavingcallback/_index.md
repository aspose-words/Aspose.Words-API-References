---
title: "Aspose::Words::Saving::IPageSavingCallback gränssnitt"
linktitle: "IPageSavingCallback"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::IPageSavingCallback gränssnitt. Implementera detta gränssnitt om du vill kontrollera hur Aspose.Words sparar separata sidor när du sparar ett dokument till fasta sidformat i C++."
type: docs
weight: 44000
url: /sv/cpp/aspose.words.saving/ipagesavingcallback/
---
## IPageSavingCallback interface


Implementera detta gränssnitt om du vill kontrollera hur Aspose.Words sparar separata sidor när ett dokument sparas till fasta sidformat.

```cpp
class IPageSavingCallback : public virtual System::Object
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [PageSaving](./pagesaving/)(System::SharedPtr\<Aspose::Words::Saving::PageSavingArgs\>) | Kallas när Aspose.Words sparar en separat sida till fasta sidformat. |
| static [Type](./type/)() |  |
## Se även

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
