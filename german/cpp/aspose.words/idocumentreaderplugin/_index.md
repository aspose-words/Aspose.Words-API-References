---
title: "Aspose::Words::IDocumentReaderPlugin interface"
linktitle: "IDocumentReaderPlugin"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::IDocumentReaderPlugin interface. Definiert eine Schnittstelle für externe Lese‑Plugins, die eine Datei in ein Dokument in C++ einlesen können."
type: docs
weight: 77000
url: /de/cpp/aspose.words/idocumentreaderplugin/
---
## IDocumentReaderPlugin interface


Definiert eine Schnittstelle für externe Reader‑Plugins, die eine Datei in ein Dokument einlesen können.

```cpp
class IDocumentReaderPlugin : public virtual System::Object
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Read](./read/)(System::SharedPtr\<System::IO::Stream\>, System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>, System::SharedPtr\<Aspose::Words::Document\>) | Liest die Daten aus dem angegebenen Stream in die [Document](../document/) Instanz. |
| static [Type](./type/)() |  |
## Siehe auch

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
