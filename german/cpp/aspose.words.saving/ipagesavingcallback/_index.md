---
title: "Aspose::Words::Saving::IPageSavingCallback Schnittstelle"
linktitle: "IPageSavingCallback"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::IPageSavingCallback Schnittstelle. Implementieren Sie diese Schnittstelle, wenn Sie steuern möchten, wie Aspose.Words separate Seiten speichert, wenn ein Dokument in feste Seitenformate in C++ gespeichert wird."
type: docs
weight: 44000
url: /de/cpp/aspose.words.saving/ipagesavingcallback/
---
## IPageSavingCallback interface


Implementieren Sie dieses Interface, wenn Sie steuern möchten, wie Aspose.Words einzelne Seiten speichert, wenn ein Dokument in feste Seitenformate gespeichert wird.

```cpp
class IPageSavingCallback : public virtual System::Object
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [PageSaving](./pagesaving/)(System::SharedPtr\<Aspose::Words::Saving::PageSavingArgs\>) | Wird aufgerufen, wenn Aspose.Words eine separate Seite in feste Seitenformate speichert. |
| static [Type](./type/)() |  |
## Siehe auch

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
