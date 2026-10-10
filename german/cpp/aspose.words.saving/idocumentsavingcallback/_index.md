---
title: "Aspose::Words::Saving::IDocumentSavingCallback Schnittstelle"
linktitle: "IDocumentSavingCallback"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::IDocumentSavingCallback Schnittstelle. Implementieren Sie diese Schnittstelle, wenn Sie Ihre eigene benutzerdefinierte Methode während des Speicherns eines Dokuments in C++ aufrufen lassen möchten."
type: docs
weight: 41000
url: /de/cpp/aspose.words.saving/idocumentsavingcallback/
---
## IDocumentSavingCallback interface


Implementieren Sie dieses Interface, wenn Sie eine eigene benutzerdefinierte Methode während des Speicherns eines Dokuments aufrufen lassen möchten.

```cpp
class IDocumentSavingCallback : public virtual System::Object
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Notify](./notify/)(System::SharedPtr\<Aspose::Words::Saving::DocumentSavingArgs\>) | Dies wird aufgerufen, um über den Fortschritt des Dokumentenspeicherns zu benachrichtigen. |
| static [Type](./type/)() |  |
## Siehe auch

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
