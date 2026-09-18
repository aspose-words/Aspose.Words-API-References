---
title: "Aspose::Words::Saving::IDocumentPartSavingCallback Schnittstelle"
linktitle: "IDocumentPartSavingCallback"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::IDocumentPartSavingCallback Schnittstelle. Implementieren Sie diese Schnittstelle, wenn Sie Benachrichtigungen erhalten und steuern möchten, wie Aspose.Words Dokumentteile speichert, wenn ein Dokument in das Html- oder Epub-Format in C++ exportiert wird."
type: docs
weight: 40000
url: /de/cpp/aspose.words.saving/idocumentpartsavingcallback/
---
## IDocumentPartSavingCallback interface


Implementieren Sie diese Schnittstelle, wenn Sie Benachrichtigungen erhalten und steuern möchten, wie Aspose.Words Dokumentteile speichert, wenn ein Dokument in das [Html](../../aspose.words/saveformat/)- oder [Epub](../../aspose.words/saveformat/)-Format exportiert wird.

```cpp
class IDocumentPartSavingCallback : public virtual System::Object
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| virtual [DocumentPartSaving](./documentpartsaving/)(System::SharedPtr\<Aspose::Words::Saving::DocumentPartSavingArgs\>) | Wird aufgerufen, wenn Aspose.Words dabei ist, einen Dokumentteil zu speichern. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## Siehe auch

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
