---
title: "Aspose::Words::Loading::IDocumentLoadingCallback gränssnitt"
linktitle: "IDocumentLoadingCallback"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Loading::IDocumentLoadingCallback gränssnitt. Implementera detta gränssnitt om du vill ha din egen anpassade metod som anropas under laddning av ett dokument i C++."
type: docs
weight: 10000
url: /sv/cpp/aspose.words.loading/idocumentloadingcallback/
---
## IDocumentLoadingCallback interface


Implementera detta gränssnitt om du vill ha din egen anpassade metod som anropas under dokumentladdning.

```cpp
class IDocumentLoadingCallback : public virtual System::Object
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Notify](./notify/)(System::SharedPtr\<Aspose::Words::Loading::DocumentLoadingArgs\>) | Detta anropas för att meddela dokumentladdningsförloppet. |
| static [Type](./type/)() |  |
## Se även

* Namespace [Aspose::Words::Loading](../)
* Library [Aspose.Words for C++](../../)
