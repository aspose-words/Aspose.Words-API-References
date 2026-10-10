---
title: "Aspose::Words::Saving::IFontSavingCallback Schnittstelle"
linktitle: "IFontSavingCallback"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::IFontSavingCallback Schnittstelle. Implementieren Sie diese Schnittstelle, wenn Sie Benachrichtigungen erhalten und steuern möchten, wie Aspose.Words Schriftarten speichert, wenn ein Dokument im HTML-Format in C++ exportiert wird."
type: docs
weight: 42000
url: /de/cpp/aspose.words.saving/ifontsavingcallback/
---
## IFontSavingCallback interface


Implementieren Sie dieses Interface, wenn Sie Benachrichtigungen erhalten und steuern möchten, wie Aspose.Words Schriftarten beim Exportieren eines Dokuments in das HTML‑Format speichert.

```cpp
class IFontSavingCallback : public virtual System::Object
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| virtual [FontSaving](./fontsaving/)(System::SharedPtr\<Aspose::Words::Saving::FontSavingArgs\>) | Wird aufgerufen, wenn Aspose.Words dabei ist, eine Schriftartressource zu speichern. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## Siehe auch

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
