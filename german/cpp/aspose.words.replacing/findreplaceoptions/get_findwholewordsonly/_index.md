---
title: "Aspose::Words::Replacing::FindReplaceOptions::get_FindWholeWordsOnly Methode"
linktitle: "get_FindWholeWordsOnly"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Replacing::FindReplaceOptions::get_FindWholeWordsOnly Methode. True gibt an, dass oldValue ein eigenständiges Wort sein muss in C++."
type: docs
weight: 6000
url: /de/cpp/aspose.words.replacing/findreplaceoptions/get_findwholewordsonly/
---
## FindReplaceOptions::get_FindWholeWordsOnly method


True gibt an, dass oldValue ein eigenständiges Wort sein muss.

```cpp
bool Aspose::Words::Replacing::FindReplaceOptions::get_FindWholeWordsOnly() const
```


## Beispiele



Zeigt, wie man eigenständige wort‑nur‑Suchen‑und‑Ersetzen‑Operationen umschaltet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Jackson will meet you in Jacksonville.");

// Wir können ein "FindReplaceOptions"‑Objekt verwenden, um den Suchen‑und‑Ersetzen‑Vorgang zu ändern.
auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();

// Setzen Sie das Flag "FindWholeWordsOnly" auf "true", um den gefundenen Text zu ersetzen, wenn er nicht Teil eines anderen Wortes ist.
// Setzen Sie das Flag "FindWholeWordsOnly" auf "false", um allen Text zu ersetzen, unabhängig von seiner Umgebung.
options->set_FindWholeWordsOnly(findWholeWordsOnly);

doc->get_Range()->Replace(u"Jackson", u"Louis", options);

ASSERT_EQ(findWholeWordsOnly ? System::String(u"Louis will meet you in Jacksonville.") : System::String(u"Louis will meet you in Louisville."), doc->GetText().Trim());
```

## Siehe auch

* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
