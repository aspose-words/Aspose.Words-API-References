---
title: "Aspose::Words::Document::UnlinkFields method"
linktitle: "UnlinkFields"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Document::UnlinkFields method. Scollega i campi in tutto il documento in C++."
type: docs
weight: 94000
url: /it/cpp/aspose.words/document/unlinkfields/
---
## Document::UnlinkFields method


Scollega i campi in tutto il documento.

```cpp
void Aspose::Words::Document::UnlinkFields()
```

## Note


Sostituisce tutti i campi in tutto il documento con i loro risultati più recenti.

Per scollegare i campi in una parte specifica del documento, usa [UnlinkFields](../../range/unlinkfields/).

## Esempi



Mostra come scollegare tutti i campi nel documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Linked fields.docx");

doc->UnlinkFields();
```

## Vedi anche

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
