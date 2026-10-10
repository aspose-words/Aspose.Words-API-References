---
title: "Schnittstelle Aspose::Words::Saving::ICssSavingCallback"
linktitle: "ICssSavingCallback"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::ICssSavingCallback Schnittstelle. Implementieren Sie diese Schnittstelle, wenn Sie steuern möchten, wie Aspose.Words CSS (Cascading Style Sheet) beim Speichern eines Dokuments als HTML in C++ speichert."
type: docs
weight: 39000
url: /de/cpp/aspose.words.saving/icsssavingcallback/
---
## ICssSavingCallback interface


Implementieren Sie diese Schnittstelle, wenn Sie steuern möchten, wie Aspose.Words CSS (Cascading [Style](../../aspose.words/style/) Sheet) beim Speichern eines Dokuments als HTML speichert.

```cpp
class ICssSavingCallback : public virtual System::Object
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| virtual [CssSaving](./csssaving/)(System::SharedPtr\<Aspose::Words::Saving::CssSavingArgs\>) | Wird aufgerufen, wenn Aspose.Words ein CSS (Cascading [Style](../../aspose.words/style/) Sheet) speichert. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## Siehe auch

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
