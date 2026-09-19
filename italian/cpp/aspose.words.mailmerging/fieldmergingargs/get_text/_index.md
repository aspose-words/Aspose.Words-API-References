---
title: "Metodo get_Text di Aspose::Words::MailMerging::FieldMergingArgs"
linktitle: "get_Text"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo get_Text di Aspose::Words::MailMerging::FieldMergingArgs. Ottiene o imposta il testo che verrà inserito nel documento per il campo di unione corrente in C++."
type: docs
weight: 2000
url: /it/cpp/aspose.words.mailmerging/fieldmergingargs/get_text/
---
## FieldMergingArgs::get_Text method


Ottiene o imposta il testo che sarà inserito nel documento per il campo di unione corrente.

```cpp
System::String Aspose::Words::MailMerging::FieldMergingArgs::get_Text() const
```

## Note


Quando il tuo gestore di eventi viene chiamato, questa proprietà è impostata su **null**.

Se lasci Text impostato su **null**, il motore di unione di posta inserirà [FieldValue](../../fieldmergingargsbase/get_fieldvalue/) al posto del campo di unione.

Se imposti Text su qualsiasi stringa (inclusa quella vuota), la stringa verrà inserita nel documento al posto del campo di unione.
## Vedi anche

* Class [FieldMergingArgs](../)
* Namespace [Aspose::Words::MailMerging](../../)
* Library [Aspose.Words for C++](../../../)
