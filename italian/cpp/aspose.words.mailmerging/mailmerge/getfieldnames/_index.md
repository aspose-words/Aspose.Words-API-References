---
title: "Metodo Aspose::Words::MailMerging::MailMerge::GetFieldNames"
linktitle: "GetFieldNames"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::MailMerging::MailMerge::GetFieldNames. Restituisce una raccolta di nomi di campi di mail merge disponibili nel documento in C++."
type: docs
weight: 21000
url: /it/cpp/aspose.words.mailmerging/mailmerge/getfieldnames/
---
## MailMerge::GetFieldNames method


Restituisce una raccolta di nomi di campi di mail merge disponibili nel documento.

```cpp
System::ArrayPtr<System::String> Aspose::Words::MailMerging::MailMerge::GetFieldNames()
```

## Note


Restituisce i nomi completi dei campi di merge includendo il prefisso opzionale. Non elimina i nomi di campo duplicati.

Un nuovo array di stringhe viene creato ad ogni chiamata.

Include i nomi di campo \"mustache\" se [UseNonMergeFields](../get_usenonmergefields/) è **true**.
## Vedi anche

* Class [MailMerge](../)
* Namespace [Aspose::Words::MailMerging](../../)
* Library [Aspose.Words for C++](../../../)
