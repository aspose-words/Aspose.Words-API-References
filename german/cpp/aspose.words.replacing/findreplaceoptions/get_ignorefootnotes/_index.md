---
title: "Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreFootnotes Methode"
linktitle: "get_IgnoreFootnotes"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreFootnotes Methode. Gibt einen booleschen Wert zurück oder setzt ihn, der angibt, ob Fußnoten ignoriert werden sollen. Der Standardwert ist false in C++."
type: docs
weight: 10000
url: /de/cpp/aspose.words.replacing/findreplaceoptions/get_ignorefootnotes/
---
## FindReplaceOptions::get_IgnoreFootnotes method


Liest oder setzt einen booleschen Wert, der angibt, ob Fußnoten ignoriert werden sollen. Der Standardwert ist **false**.

```cpp
bool Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreFootnotes() const
```


## Beispiele



Zeigt, wie man Fußnoten während einer Suchen‑und‑Ersetzen‑Operation ignoriert.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit.");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Lorem ipsum dolor sit amet, consectetur adipiscing elit.");

builder->InsertParagraph();

builder->Write(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit.");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Lorem ipsum dolor sit amet, consectetur adipiscing elit.");

// Setzen Sie das Flag "IgnoreFootnotes" auf "true", um die Suchen‑und‑Ersetzen‑Operation zu erhalten
// Operation, um Text innerhalb von Fußnoten zu ignorieren.
// Setzen Sie das Flag "IgnoreFootnotes" auf "false", um die Suchen‑und‑Ersetzen‑Operation zu erhalten
// Operation, um auch nach Text innerhalb von Fußnoten zu suchen.
auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();
options->set_IgnoreFootnotes(isIgnoreFootnotes);
doc->get_Range()->Replace(u"Lorem ipsum", u"Replaced Lorem ipsum", options);
```

## Siehe auch

* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
