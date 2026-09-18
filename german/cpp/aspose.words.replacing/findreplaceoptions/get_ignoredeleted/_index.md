---
title: "Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreDeleted Methode"
linktitle: "get_IgnoreDeleted"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreDeleted Methode. Gibt einen booleschen Wert zurück oder setzt ihn, der angibt, ob Text innerhalb von Löschrevisionen ignoriert werden soll. Der Standardwert ist false in C++."
type: docs
weight: 7000
url: /de/cpp/aspose.words.replacing/findreplaceoptions/get_ignoredeleted/
---
## FindReplaceOptions::get_IgnoreDeleted method


Liest oder setzt einen booleschen Wert, der angibt, ob Text innerhalb von Löschrevisionen ignoriert werden soll. Der Standardwert ist **false**.

```cpp
bool Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreDeleted() const
```


## Beispiele



Zeigt, wie man Text innerhalb von Löschrevisionen während einer Suchen‑und‑Ersetzen‑Operation einbezieht oder ignoriert.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Hello world!");
builder->Writeln(u"Hello again!");

// Beginnen Sie mit der Verfolgung von Revisionen und entfernen Sie den zweiten Absatz, wodurch eine Löschrevision erstellt wird.
// Dieser Absatz bleibt im Dokument, bis wir die Löschrevision akzeptieren.
doc->StartTrackRevisions(u"John Doe", System::DateTime::get_Now());
doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(1)->Remove();
doc->StopTrackRevisions();

ASSERT_TRUE(doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(1)->get_IsDeleteRevision());

// Wir können ein "FindReplaceOptions"-Objekt verwenden, um den Suchen‑und‑Ersetzen‑Vorgang zu ändern.
auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();

// Setzen Sie das "IgnoreDeleted"‑Flag auf "true", um den Suchen‑und‑Ersetzen‑Vorgang zu erhalten.
// Operation, um Absätze zu ignorieren, die Löschrevisionen sind.
// Setzen Sie das "IgnoreDeleted"‑Flag auf "false", um den Suchen‑und‑Ersetzen‑Vorgang zu erhalten.
// Operation, um auch nach Text innerhalb von Löschrevisionen zu suchen.
options->set_IgnoreDeleted(ignoreTextInsideDeleteRevisions);

doc->get_Range()->Replace(u"Hello", u"Greetings", options);

ASSERT_EQ(ignoreTextInsideDeleteRevisions ? System::String(u"Greetings world!\rHello again!") : System::String(u"Greetings world!\rGreetings again!"), doc->GetText().Trim());
```

## Siehe auch

* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
