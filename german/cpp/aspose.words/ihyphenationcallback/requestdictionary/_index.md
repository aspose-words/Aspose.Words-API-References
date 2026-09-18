---
title: "Aspose::Words::IHyphenationCallback::RequestDictionary Methode"
linktitle: "RequestDictionary"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::IHyphenationCallback::RequestDictionary Methode. Benachrichtigt die Anwendung, dass das Silbentrennungswörterbuch für die angegebene Sprache nicht gefunden wurde und möglicherweise registriert werden muss. Die Implementierung sollte ein Wörterbuch finden und es mit den RegisterDictionary()-Methoden registrieren. Wenn das Wörterbuch für die angegebene Sprache nicht verfügbar ist, kann die Implementierung weitere Aufrufe für dieselbe Sprache mit RegisterDictionary() und einem Nullwert in C++ abbestellen."
type: docs
weight: 4000
url: /de/cpp/aspose.words/ihyphenationcallback/requestdictionary/
---
## IHyphenationCallback::RequestDictionary method


Benachrichtigt die Anwendung, dass das Silbentrennungswörterbuch für die angegebene Sprache nicht gefunden wurde und möglicherweise registriert werden muss. Die Implementierung sollte ein Wörterbuch finden und es mithilfe der [RegisterDictionary()](../) Methoden registrieren. Wenn das Wörterbuch für die angegebene Sprache nicht verfügbar ist, kann die Implementierung weitere Aufrufe für dieselbe Sprache mit [RegisterDictionary()](../) und dem **null**‑Wert ablehnen.

```cpp
virtual void Aspose::Words::IHyphenationCallback::RequestDictionary(System::String language)=0
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Sprache | System::String | Ein Sprachname, z. B. "en-US". Siehe .NET-Dokumentation für "culture name" und RFC 4646 für Details. |

## Siehe auch

* Interface [IHyphenationCallback](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
