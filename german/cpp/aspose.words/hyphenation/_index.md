---
title: "Aspose::Words::Hyphenation‑Klasse"
linktitle: "Silbentrennung"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Hyphenation‑Klasse. Stellt Methoden zur Arbeit mit Silbentrennungs‑Wörterbüchern bereit. Diese Wörterbücher geben vor, wo Wörter einer bestimmten Sprache getrennt werden können. Weitere Informationen finden Sie im Dokumentationsartikel zu C++."
type: docs
weight: 33000
url: /de/cpp/aspose.words/hyphenation/
---
## Hyphenation class


Stellt Methoden zum Arbeiten mit Silbentrennungswörterbüchern bereit. Diese Wörterbücher geben vor, wo Wörter einer bestimmten Sprache getrennt werden können. Um mehr zu erfahren, besuchen Sie den Dokumentationsartikel [Working with Hyphenation](https://docs.aspose.com/words/cpp/working-with-hyphenation/).

```cpp
class Hyphenation
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| static [get_Callback](./get_callback/)() | Ruft die Callback‑Schnittstelle ab, die zum Anfordern von Wörterbüchern verwendet wird, wenn das Seitenlayout des Dokuments erstellt wird. Dies ermöglicht das verzögerte Laden von Wörterbüchern, was bei der Verarbeitung von Dokumenten in vielen Sprachen nützlich sein kann. |
| static [get_WarningCallback](./get_warningcallback/)() | Aufgerufen beim Laden von Silbentrennungs‑Mustern, wenn ein Problem erkannt wird, das zu einem Verlust der Formattreue führen könnte. |
| [Hyphenation](./hyphenation/)() |  |
| static [IsDictionaryRegistered](./isdictionaryregistered/)(const System::String\&) | Gibt **false** zurück, wenn für die angegebene Sprache kein Wörterbuch registriert ist oder das registrierte Wörterbuch Null ist, andernfalls **true**. |
| static [RegisterDictionary](./registerdictionary/)(const System::String\&, const System::SharedPtr\<System::IO::Stream\>\&) | Registriert und lädt ein Silbentrennungs‑Wörterbuch für die angegebene Sprache aus einem Stream. Wirft eine Ausnahme, wenn das Wörterbuch nicht gelesen werden kann oder ein ungültiges Format hat. |
| static [RegisterDictionary](./registerdictionary/)(const System::String\&, const System::String\&) | Registriert und lädt ein Silbentrennungs‑Wörterbuch für die angegebene Sprache aus einer Datei. Wirft eine Ausnahme, wenn das Wörterbuch nicht gelesen werden kann oder ein ungültiges Format hat. Diese Methode kann auch verwendet werden, um ein Null‑Wörterbuch zu registrieren, damit [Callback](./get_callback/) nicht wiederholt für dieselbe Sprache aufgerufen wird. |
| static [RegisterDictionary](./registerdictionary/)(System::String, std::basic_istream\<CharType, Traits\>\&) |  |
| static [set_Callback](./set_callback/)(const System::SharedPtr\<Aspose::Words::IHyphenationCallback\>\&) | Legt die Callback-Schnittstelle fest, die zum Anfordern von Wörterbüchern verwendet wird, wenn das Seitenlayout des Dokuments erstellt wird. Dies ermöglicht ein verzögertes Laden von Wörterbüchern, was bei der Verarbeitung von Dokumenten in vielen Sprachen nützlich sein kann. |
| static [set_WarningCallback](./set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | Aufgerufen beim Laden von Silbentrennungs‑Mustern, wenn ein Problem erkannt wird, das zu einem Verlust der Formattreue führen könnte. |
| static [UnregisterDictionary](./unregisterdictionary/)(const System::String\&) | Meldet ein Silbentrennungswörterbuch für die angegebene Sprache ab. Dies unterscheidet sich vom Registrieren eines Null-Wörterbuchs. Das Abmelden eines Wörterbuchs aktiviert den Callback für die angegebene Sprache. |
## Siehe auch

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
