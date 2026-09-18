---
title: "Aspose::Words::Loading::IDocumentLoadingCallback Schnittstelle"
linktitle: "IDocumentLoadingCallback"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Loading::IDocumentLoadingCallback Schnittstelle. Implementieren Sie diese Schnittstelle, wenn Sie eine eigene benutzerdefinierte Methode während des Ladens eines Dokuments in C++ aufrufen möchten."
type: docs
weight: 10000
url: /de/cpp/aspose.words.loading/idocumentloadingcallback/
---
## IDocumentLoadingCallback interface


Implementieren Sie diese Schnittstelle, wenn Sie eine eigene benutzerdefinierte Methode während des Ladens eines Dokuments aufrufen möchten.

```cpp
class IDocumentLoadingCallback : public virtual System::Object
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Notify](./notify/)(System::SharedPtr\<Aspose::Words::Loading::DocumentLoadingArgs\>) | Dies wird aufgerufen, um über den Fortschritt des Dokumentladens zu benachrichtigen. |
| static [Type](./type/)() |  |
## Siehe auch

* Namespace [Aspose::Words::Loading](../)
* Library [Aspose.Words for C++](../../)
