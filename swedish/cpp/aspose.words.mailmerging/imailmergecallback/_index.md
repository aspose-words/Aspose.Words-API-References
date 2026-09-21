---
title: "Aspose::Words::MailMerging::IMailMergeCallback interface"
linktitle: "IMailMergeCallback"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::MailMerging::IMailMergeCallback interface. Implementera detta gränssnitt om du vill ta emot aviseringar medan kopplad sammanslagning utförs i C++."
type: docs
weight: 8000
url: /sv/cpp/aspose.words.mailmerging/imailmergecallback/
---
## IMailMergeCallback interface


Implementera detta gränssnitt om du vill ta emot aviseringar medan mail merge utförs.

```cpp
class IMailMergeCallback : public virtual System::Object
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [TagsReplaced](./tagsreplaced/)() | Kallas när "mustache"‑texttaggar ersätts med MERGEFIELD‑fält. |
| static [Type](./type/)() |  |
## Se även

* Namespace [Aspose::Words::MailMerging](../)
* Library [Aspose.Words for C++](../../)
