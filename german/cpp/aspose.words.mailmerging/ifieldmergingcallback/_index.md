---
title: "Aspose::Words::MailMerging::IFieldMergingCallback Schnittstelle"
linktitle: "IFieldMergingCallback"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::MailMerging::IFieldMergingCallback Schnittstelle. Implementieren Sie diese Schnittstelle, wenn Sie steuern möchten, wie Daten während einer Seriendruck‑Operation in C++ in Merge‑Felder eingefügt werden."
type: docs
weight: 7000
url: /de/cpp/aspose.words.mailmerging/ifieldmergingcallback/
---
## IFieldMergingCallback interface


Implementieren Sie dieses Interface, wenn Sie steuern möchten, wie Daten während eines Seriendruckvorgangs in Merge-Felder eingefügt werden.

```cpp
class IFieldMergingCallback : public virtual System::Object
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| virtual [FieldMerging](./fieldmerging/)(System::SharedPtr\<Aspose::Words::MailMerging::FieldMergingArgs\>) | Wird aufgerufen, wenn die Aspose.Words Seriendruck‑Engine Daten in ein Merge‑Feld im Dokument einfügen soll. |
| [GetType](./gettype/)() const override |  |
| virtual [ImageFieldMerging](./imagefieldmerging/)(System::SharedPtr\<Aspose::Words::MailMerging::ImageFieldMergingArgs\>) | Wird aufgerufen, wenn die Aspose.Words-Mail-Merge-Engine dabei ist, ein Bild in ein Zusammenführungsfeld einzufügen. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## Siehe auch

* Namespace [Aspose::Words::MailMerging](../)
* Library [Aspose.Words for C++](../../)
