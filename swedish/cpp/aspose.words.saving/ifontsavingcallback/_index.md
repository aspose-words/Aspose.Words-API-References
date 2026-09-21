---
title: "Aspose::Words::Saving::IFontSavingCallback interface"
linktitle: "IFontSavingCallback"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::IFontSavingCallback interface. Implementera detta gränssnitt om du vill få notifikationer och kontrollera hur Aspose.Words sparar teckensnitt när du exporterar ett dokument till HTML-format i C++."
type: docs
weight: 42000
url: /sv/cpp/aspose.words.saving/ifontsavingcallback/
---
## IFontSavingCallback interface


Implementera detta gränssnitt om du vill få meddelanden och kontrollera hur Aspose.Words sparar teckensnitt när ett dokument exporteras till HTML-format.

```cpp
class IFontSavingCallback : public virtual System::Object
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| virtual [FontSaving](./fontsaving/)(System::SharedPtr\<Aspose::Words::Saving::FontSavingArgs\>) | Kallas när Aspose.Words håller på att spara en teckensnittresurs. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## Se även

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
