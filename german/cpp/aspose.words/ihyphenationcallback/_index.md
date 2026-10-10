---
title: "Aspose::Words::IHyphenationCallback Schnittstelle"
linktitle: "IHyphenationCallback"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::IHyphenationCallback Schnittstelle. Implementiert von Klassen, die Silbentrennungswörterbücher in C++ registrieren können."
type: docs
weight: 78000
url: /de/cpp/aspose.words/ihyphenationcallback/
---
## IHyphenationCallback interface


Wird von Klassen implementiert, die Silbentrennungs‑Wörterbücher registrieren können.

```cpp
class IHyphenationCallback : public virtual System::Object
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [RequestDictionary](./requestdictionary/)(System::String) | Benachrichtigt die Anwendung, dass das Silbentrennungswörterbuch für die angegebene Sprache nicht gefunden wurde und möglicherweise registriert werden muss. Die Implementierung sollte ein Wörterbuch finden und es mithilfe der [RegisterDictionary()](../) Methoden registrieren. Wenn das Wörterbuch für die angegebene Sprache nicht verfügbar ist, kann die Implementierung weitere Aufrufe für dieselbe Sprache mit [RegisterDictionary()](../) und dem **null**‑Wert ablehnen. |
| static [Type](./type/)() |  |
## Siehe auch

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
