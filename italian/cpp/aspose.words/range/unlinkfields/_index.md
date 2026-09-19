---
title: "Aspose::Words::Range::UnlinkFields metodo"
linktitle: "UnlinkFields"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Range::UnlinkFields metodo. Scollega i campi in questo intervallo in C++."
type: docs
weight: 14000
url: /it/cpp/aspose.words/range/unlinkfields/
---
## Range::UnlinkFields method


Scollega i campi in questo intervallo.

```cpp
void Aspose::Words::Range::UnlinkFields()
```

## Note


Sostituisce tutti i campi in questo intervallo con i loro risultati più recenti.

Per scollegare i campi nell'intero documento utilizzare [UnlinkFields](./).

## Esempi



Mostra come scollegare tutti i campi in un intervallo.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Linked fields.docx");

auto newSection = System::ExplicitCast<Aspose::Words::Section>(System::ExplicitCast<Aspose::Words::Node>(doc->get_Sections()->idx_get(0))->Clone(true));
doc->get_Sections()->Add(newSection);

doc->get_Sections()->idx_get(1)->get_Range()->UnlinkFields();
```

## Vedi anche

* Class [Range](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
