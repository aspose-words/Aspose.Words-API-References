---
title: "Aspose::Words::MailMerging::MailMerge::get_UseNonMergeFields method"
linktitle: "get_UseNonMergeFields"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::MailMerging::MailMerge::get_UseNonMergeFields method. Quando è true, specifica che, oltre ai campi MERGEFIELD, la mail merge viene eseguita su altri tipi di campi e anche sui tag \"{{fieldName}}\" in C++."
type: docs
weight: 19000
url: /it/cpp/aspose.words.mailmerging/mailmerge/get_usenonmergefields/
---
## MailMerge::get_UseNonMergeFields method


Quando **true**, specifica che, oltre ai campi MERGEFIELD, l'unione della posta viene eseguita su altri tipi di campi e anche sui tag "{{fieldName}}".

```cpp
bool Aspose::Words::MailMerging::MailMerge::get_UseNonMergeFields() const
```

## Note


Normalmente, l'unione di stampa viene eseguita solo sui campi MERGEFIELD, ma diversi clienti hanno costruito i loro report utilizzando altri campi e hanno creato molti documenti in questo modo. Per semplificare la migrazione (e perché questo approccio è stato utilizzato in modo indipendente da diversi clienti) è stata introdotta la possibilità di eseguire l'unione di stampa in altri campi.

Quando [UseNonMergeFields](./) è impostato su **true**, Aspose.Words eseguirà l'unione di stampa nei seguenti campi:

MERGEFIELD FieldName

MACROBUTTON NOMACRO FieldName

IF 0 = 0 "{FieldName}" ""

Inoltre, quando [UseNonMergeFields](./) è impostato su **true**, Aspose.Words eseguirà l'unione di stampa nei tag di testo "{{fieldName}}". Questi non sono campi, ma solo tag di testo.
## Vedi anche

* Class [MailMerge](../)
* Namespace [Aspose::Words::MailMerging](../../)
* Library [Aspose.Words for C++](../../../)
