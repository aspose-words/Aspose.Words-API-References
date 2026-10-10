---
title: "Aspose::Words::MailMerging::IMailMergeCallback interface"
linktitle: "IMailMergeCallback"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::MailMerging::IMailMergeCallback Schnittstelle. Implementieren Sie diese Schnittstelle, wenn Sie Benachrichtigungen erhalten möchten, während der Seriendruck in C++ ausgeführt wird."
type: docs
weight: 8000
url: /de/cpp/aspose.words.mailmerging/imailmergecallback/
---
## IMailMergeCallback interface


Implementieren Sie dieses Interface, wenn Sie Benachrichtigungen erhalten möchten, während ein Seriendruck durchgeführt wird.

```cpp
class IMailMergeCallback : public virtual System::Object
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [TagsReplaced](./tagsreplaced/)() | Wird aufgerufen, wenn "mustache"-Text-Tags durch MERGEFIELD-Felder ersetzt werden. |
| static [Type](./type/)() |  |
## Siehe auch

* Namespace [Aspose::Words::MailMerging](../)
* Library [Aspose.Words for C++](../../)
