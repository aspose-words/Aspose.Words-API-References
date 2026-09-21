---
title: "Aspose::Words::IDocumentReaderPlugin interface"
linktitle: "IDocumentReaderPlugin"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::IDocumentReaderPlugin interface. Definierar ett gränssnitt för externa läs‑plugin‑moduler som kan läsa in en fil till ett dokument i C++."
type: docs
weight: 77000
url: /sv/cpp/aspose.words/idocumentreaderplugin/
---
## IDocumentReaderPlugin interface


Definierar ett gränssnitt för externa läs-plugin-moduler som kan läsa in en fil i ett dokument.

```cpp
class IDocumentReaderPlugin : public virtual System::Object
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Read](./read/)(System::SharedPtr\<System::IO::Stream\>, System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>, System::SharedPtr\<Aspose::Words::Document\>) | Läser data från den specificerade strömmen till [Document](../document/)‑instansen. |
| static [Type](./type/)() |  |
## Se även

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
