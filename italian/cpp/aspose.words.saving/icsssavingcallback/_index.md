---
title: "interfaccia Aspose::Words::Saving::ICssSavingCallback"
linktitle: "ICssSavingCallback"
second_title: "Riferimento API Aspose.Words per C++"
description: "interfaccia Aspose::Words::Saving::ICssSavingCallback. Implementa questa interfaccia se desideri controllare come Aspose.Words salva il CSS (Cascading Style Sheet) quando si salva un documento in HTML in C++."
type: docs
weight: 39000
url: /it/cpp/aspose.words.saving/icsssavingcallback/
---
## ICssSavingCallback interface


Implementa questa interfaccia se desideri controllare come Aspose.Words salva il CSS (Cascading [Style](../../aspose.words/style/) Sheet) quando si salva un documento in HTML.

```cpp
class ICssSavingCallback : public virtual System::Object
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| virtual [CssSaving](./csssaving/)(System::SharedPtr\<Aspose::Words::Saving::CssSavingArgs\>) | Chiamato quando Aspose.Words salva un CSS (a cascata [Style](../../aspose.words/style/) Foglio). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## Vedi anche

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
