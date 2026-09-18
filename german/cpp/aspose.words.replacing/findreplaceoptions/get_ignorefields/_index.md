---
title: "Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreFields method"
linktitle: "get_IgnoreFields"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreFields method. Gibt einen booleschen Wert zurück oder setzt ihn, der angibt, ob Text innerhalb von Feldern ignoriert werden soll. Der Standardwert ist false in C++."
type: docs
weight: 9000
url: /de/cpp/aspose.words.replacing/findreplaceoptions/get_ignorefields/
---
## FindReplaceOptions::get_IgnoreFields method


Liest oder setzt einen booleschen Wert, der angibt, ob Text innerhalb von Feldern ignoriert werden soll. Der Standardwert ist **false**.

```cpp
bool Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreFields() const
```

## Hinweise


Diese Option betrifft das gesamte Feld (alle Knoten zwischen [FieldStart](../../../aspose.words/nodetype/) und [FieldEnd](../../../aspose.words/nodetype/)).

Um nur Feldcodes zu ignorieren, verwenden Sie bitte die entsprechende Option [IgnoreFieldCodes](../get_ignorefieldcodes/).

## Beispiele



Zeigt, wie man Text innerhalb von Feldern ignoriert.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Hello world!");
builder->InsertField(u"QUOTE", u"Hello again!");

// Wir können ein "FindReplaceOptions"‑Objekt verwenden, um den Suchen‑und‑Ersetzen‑Vorgang zu ändern.
auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();

// Setzen Sie das "IgnoreFields"‑Flag auf "true", um den Suchen‑und‑Ersetzen‑Vorgang zu erhalten.
// Operation, um Text innerhalb von Feldern zu ignorieren.
// Setzen Sie das "IgnoreFields"‑Flag auf "false", um den Suchen‑und‑Ersetzen‑Vorgang zu erhalten.
// Operation, um auch nach Text innerhalb von Feldern zu suchen.
options->set_IgnoreFields(ignoreTextInsideFields);

doc->get_Range()->Replace(u"Hello", u"Greetings", options);

ASSERT_EQ(ignoreTextInsideFields ? System::String(u"Greetings world!\r\u0013QUOTE\u0014Hello again!\u0015") : System::String(u"Greetings world!\r\u0013QUOTE\u0014Greetings again!\u0015"), doc->GetText().Trim());
```

## Siehe auch

* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
