---
title: "Aspose::Words::MailMerging::FieldMergingArgs class"
linktitle: "FieldMergingArgs"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::MailMerging::FieldMergingArgs class. Tillhandahåller data för MergeField‑händelsen. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 1000
url: /sv/cpp/aspose.words.mailmerging/fieldmergingargs/
---
## FieldMergingArgs class


Tillhandahåller data för **MergeField**‑händelsen. För att lära dig mer, besök dokumentationsartikeln [Mail Merge and Reporting](https://docs.aspose.com/words/cpp/mail-merge-and-reporting/).

```cpp
class FieldMergingArgs : public Aspose::Words::MailMerging::FieldMergingArgsBase
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [get_Document](../fieldmergingargsbase/get_document/)() const | Returnerar [Document](../fieldmergingargsbase/get_document/)‑objektet för vilket kopplad sammanslagning utförs. |
| [get_DocumentFieldName](../fieldmergingargsbase/get_documentfieldname/)() const | Hämtar namnet på sammanslagningsfältet enligt vad som anges i dokumentet. |
| [get_Field](../fieldmergingargsbase/get_field/)() const | Hämtar objektet som representerar det aktuella sammanslagningsfältet. |
| [get_FieldName](../fieldmergingargsbase/get_fieldname/)() const | Hämtar namnet på sammanslagningsfältet i datakällan. |
| [get_FieldValue](../fieldmergingargsbase/get_fieldvalue/)() const | Hämtar värdet på fältet från datakällan. |
| [get_RecordIndex](../fieldmergingargsbase/get_recordindex/)() const | Hämtar det nollbaserade indexet för posten som slås samman. |
| [get_TableName](../fieldmergingargsbase/get_tablename/)() const | Hämtar namnet på datatabellen för den aktuella sammanslagningsoperationen eller en tom sträng om namnet inte är tillgängligt. |
| [get_Text](./get_text/)() const | Hämtar eller anger texten som kommer att infogas i dokumentet för det aktuella sammanslagningsfältet. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_FieldValue](../fieldmergingargsbase/set_fieldvalue/)(const System::SharedPtr\<System::Object\>\&) | Ställer in värdet för fältet från datakällan. |
| [set_Text](./set_text/)(const System::String\&) | Sättare för [Aspose::Words::MailMerging::FieldMergingArgs::get_Text](./get_text/). |
| static [Type](./type/)() |  |
## Anmärkningar


Händelsen **MergeField** inträffar under kopplad sammanslagning när ett enkelt sammanslagningsfält påträffas i dokumentet. Du kan svara på denna händelse för att returnera text som kopplad sammanslagningsmotor ska infoga i dokumentet.

## Se även

* Class [FieldMergingArgsBase](../fieldmergingargsbase/)
* Namespace [Aspose::Words::MailMerging](../)
* Library [Aspose.Words for C++](../../)
