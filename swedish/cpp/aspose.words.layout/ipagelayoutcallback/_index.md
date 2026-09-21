---
title: "Aspose::Words::Layout::IPageLayoutCallback gränssnitt"
linktitle: "IPageLayoutCallback"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Layout::IPageLayoutCallback gränssnitt. Implementera detta gränssnitt om du vill ha din egen anpassade metod som anropas under byggande och rendering av sidlayoutmodellen i C++."
type: docs
weight: 6000
url: /sv/cpp/aspose.words.layout/ipagelayoutcallback/
---
## IPageLayoutCallback interface


Implementera detta gränssnitt om du vill ha din egen anpassade metod som anropas under byggandet och renderingen av sidlayoutmodellen.

```cpp
class IPageLayoutCallback : public virtual System::Object
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Notify](./notify/)(System::SharedPtr\<Aspose::Words::Layout::PageLayoutCallbackArgs\>) | Detta anropas för att meddela om bygg- och renderingsförloppet för layouten. |
| static [Type](./type/)() |  |
## Anmärkningar


Det primära användningsområdet för detta gränssnitt är att låta applikationskod avbryta byggprocessen.

Det är möjligt att bygga sidlayoutmodellen för endast några få sidor i början av dokumentet, sedan avbryta processen och rendera bara det som redan har byggts.

Observera dock att renderingsresultaten kanske inte matchar vad som skulle ha renderats för varje sida om processen hade slutförts.

Denna teknik kanske inte fungerar för alla dokument eller kan misslyckas helt.

## Se även

* Namespace [Aspose::Words::Layout](../)
* Library [Aspose.Words for C++](../../)
