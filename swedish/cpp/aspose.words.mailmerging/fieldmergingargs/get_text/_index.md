---
title: "Aspose::Words::MailMerging::FieldMergingArgs::get_Text metod"
linktitle: "get_Text"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::MailMerging::FieldMergingArgs::get_Text metod. Hämtar eller anger texten som kommer att infogas i dokumentet för det aktuella sammanslagningsfältet i C++."
type: docs
weight: 2000
url: /sv/cpp/aspose.words.mailmerging/fieldmergingargs/get_text/
---
## FieldMergingArgs::get_Text method


Hämtar eller anger texten som kommer att infogas i dokumentet för det aktuella sammanslagningsfältet.

```cpp
System::String Aspose::Words::MailMerging::FieldMergingArgs::get_Text() const
```

## Anmärkningar


När din händelsehanterare anropas, sätts denna egenskap till **null**.

Om du lämnar Text som **null**, kommer mailmerge-motorn att infoga [FieldValue](../../fieldmergingargsbase/get_fieldvalue/) i stället för sammanslagningsfältet.

Om du sätter Text till en sträng (inklusive tom), kommer strängen att infogas i dokumentet i stället för sammanslagningsfältet.
## Se även

* Class [FieldMergingArgs](../)
* Namespace [Aspose::Words::MailMerging](../../)
* Library [Aspose.Words for C++](../../../)
