---
title: "Aspose::Words::MailMerging::IFieldMergingCallback gränssnitt"
linktitle: "IFieldMergingCallback"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::MailMerging::IFieldMergingCallback gränssnitt. Implementera detta gränssnitt om du vill kontrollera hur data infogas i sammanslagningsfält under en kopplad utskriftsoperation i C++."
type: docs
weight: 7000
url: /sv/cpp/aspose.words.mailmerging/ifieldmergingcallback/
---
## IFieldMergingCallback interface


Implementera detta gränssnitt om du vill kontrollera hur data infogas i sammanslagningsfält under en mail merge‑operation.

```cpp
class IFieldMergingCallback : public virtual System::Object
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| virtual [FieldMerging](./fieldmerging/)(System::SharedPtr\<Aspose::Words::MailMerging::FieldMergingArgs\>) | Kallas när Aspose.Words‑motor för kopplad utskrift är på väg att infoga data i ett sammanslagningsfält i dokumentet. |
| [GetType](./gettype/)() const override |  |
| virtual [ImageFieldMerging](./imagefieldmerging/)(System::SharedPtr\<Aspose::Words::MailMerging::ImageFieldMergingArgs\>) | Kallas när Aspose.Words‑motor för kopplad utskrift är på väg att infoga en bild i ett sammanslagningsfält. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## Se även

* Namespace [Aspose::Words::MailMerging](../)
* Library [Aspose.Words for C++](../../)
