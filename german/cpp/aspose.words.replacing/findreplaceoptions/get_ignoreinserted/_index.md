---
title: "Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreInserted Methode"
linktitle: "get_IgnoreInserted"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreInserted Methode. Gibt einen booleschen Wert zurück oder setzt ihn, der angibt, ob Text innerhalb von Einfügerevisionen ignoriert werden soll. Der Standardwert ist false in C++."
type: docs
weight: 11000
url: /de/cpp/aspose.words.replacing/findreplaceoptions/get_ignoreinserted/
---
## FindReplaceOptions::get_IgnoreInserted method


Liest oder setzt einen booleschen Wert, der angibt, ob Text innerhalb von Einfüge‑Revisionen ignoriert werden soll. Der Standardwert ist **false**.

```cpp
bool Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreInserted() const
```


## Beispiele



Zeigt, wie man Text innerhalb von Einfügerevisionen bei einem Suchen‑und‑Ersetzen‑Vorgang einbezieht oder ignoriert.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Hello world!");

// Beginnen Sie, Revisionen zu verfolgen, und fügen Sie einen Absatz ein. Dieser Absatz wird eine Einfügerevision sein.
doc->StartTrackRevisions(u"John Doe", System::DateTime::get_Now());
builder->Writeln(u"Hello again!");
doc->StopTrackRevisions();

ASSERT_TRUE(doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(1)->get_IsInsertRevision());

// Wir können ein "FindReplaceOptions"‑Objekt verwenden, um den Suchen‑und‑Ersetzen‑Vorgang zu ändern.
auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();

// Setzen Sie das Flag "IgnoreInserted" auf "true", um das Suchen‑und‑Ersetzen
// Vorgang so zu konfigurieren, dass Absätze, die Einfügerevisionen sind, ignoriert werden.
// Setzen Sie das Flag "IgnoreInserted" auf "false", um das Suchen‑und‑Ersetzen
// Vorgang so zu konfigurieren, dass auch nach Text innerhalb von Einfügerevisionen gesucht wird.
options->set_IgnoreInserted(ignoreTextInsideInsertRevisions);

doc->get_Range()->Replace(u"Hello", u"Greetings", options);

ASSERT_EQ(ignoreTextInsideInsertRevisions ? System::String(u"Greetings world!\rHello again!") : System::String(u"Greetings world!\rGreetings again!"), doc->GetText().Trim());
```

## Siehe auch

* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
