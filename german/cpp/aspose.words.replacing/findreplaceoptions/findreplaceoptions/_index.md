---
title: "Aspose::Words::Replacing::FindReplaceOptions::FindReplaceOptions Konstruktor"
linktitle: "FindReplaceOptions"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Replacing::FindReplaceOptions::FindReplaceOptions‑Konstruktor. Initialisiert eine neue Instanz der FindReplaceOptions‑Klasse mit den Standardeinstellungen in C++."
type: docs
weight: 2000
url: /de/cpp/aspose.words.replacing/findreplaceoptions/findreplaceoptions/
---
## FindReplaceOptions::FindReplaceOptions() constructor


Initialisiert eine neue Instanz der [FindReplaceOptions](../)‑Klasse mit den Standardeinstellungen.

```cpp
Aspose::Words::Replacing::FindReplaceOptions::FindReplaceOptions()
```


## Beispiele



Zeigt, wie man Substitutionen innerhalb von Ersetzungsmustern erkennt und verwendet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Jason gave money to Paul.");

auto regex = System::MakeObject<System::Text::RegularExpressions::Regex>(u"([A-z]+) gave money to ([A-z]+)");

auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();
options->set_UseSubstitutions(true);

// Die Verwendung des Legacy‑Modus unterstützt viele erweiterte Funktionen nicht, daher müssen wir ihn auf 'false' setzen.
options->set_LegacyMode(false);

doc->get_Range()->Replace(regex, u"$2 took money from $1", options);

ASSERT_EQ(doc->GetText(), u"Paul took money from Jason.\f");
```

## Siehe auch

* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
## FindReplaceOptions::FindReplaceOptions(Aspose::Words::Replacing::FindReplaceDirection) constructor


Initialisiert eine neue Instanz der [FindReplaceOptions](../)‑Klasse mit der angegebenen Richtung.

```cpp
Aspose::Words::Replacing::FindReplaceOptions::FindReplaceOptions(Aspose::Words::Replacing::FindReplaceDirection direction)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Richtung | Aspose::Words::Replacing::FindReplaceDirection | Die Richtung des Such‑ und Ersetzungsvorgangs. |

## Siehe auch

* Enum [FindReplaceDirection](../../findreplacedirection/)
* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
## FindReplaceOptions::FindReplaceOptions(Aspose::Words::Replacing::FindReplaceDirection, const System::SharedPtr\<Aspose::Words::Replacing::IReplacingCallback\>\&) constructor


Initialisiert eine neue Instanz der [FindReplaceOptions](../)‑Klasse mit der angegebenen Richtung und dem Ersetzungs‑Callback.

```cpp
Aspose::Words::Replacing::FindReplaceOptions::FindReplaceOptions(Aspose::Words::Replacing::FindReplaceDirection direction, const System::SharedPtr<Aspose::Words::Replacing::IReplacingCallback> &replacingCallback)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Richtung | Aspose::Words::Replacing::FindReplaceDirection | Die Richtung des Such‑ und Ersetzungsvorgangs. |
| replacingCallback | const System::SharedPtr\<Aspose::Words::Replacing::IReplacingCallback\>\& | Der Callback, der zum Ersetzen des gefundenen Textes verwendet wird. |

## Siehe auch

* Enum [FindReplaceDirection](../../findreplacedirection/)
* Interface [IReplacingCallback](../../ireplacingcallback/)
* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
## FindReplaceOptions::FindReplaceOptions(const System::SharedPtr\<Aspose::Words::Replacing::IReplacingCallback\>\&) constructor


Initialisiert eine neue Instanz der [FindReplaceOptions](../)‑Klasse mit dem angegebenen Ersetzungs‑Callback.

```cpp
Aspose::Words::Replacing::FindReplaceOptions::FindReplaceOptions(const System::SharedPtr<Aspose::Words::Replacing::IReplacingCallback> &replacingCallback)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| replacingCallback | const System::SharedPtr\<Aspose::Words::Replacing::IReplacingCallback\>\& | Der Callback, der zum Ersetzen des gefundenen Textes verwendet wird. |

## Siehe auch

* Interface [IReplacingCallback](../../ireplacingcallback/)
* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
