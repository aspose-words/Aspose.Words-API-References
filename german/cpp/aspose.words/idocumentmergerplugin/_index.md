---
title: "Aspose::Words::IDocumentMergerPlugin interface"
linktitle: "IDocumentMergerPlugin"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::IDocumentMergerPlugin interface. Definiert eine Schnittstelle für ein externes Merge‑Plugin, das PDF‑Dokumente in C++ zusammenführen kann."
type: docs
weight: 76500
url: /de/cpp/aspose.words/idocumentmergerplugin/
---
## IDocumentMergerPlugin interface


Definiert eine Schnittstelle für ein externes Merge‑Plugin, das PDF‑Dokumente zusammenführen kann.

```cpp
class IDocumentMergerPlugin : public virtual System::Object
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Merge](./merge/)(System::SharedPtr\<System::IO::Stream\>, System::ArrayPtr\<System::SharedPtr\<System::IO::Stream\>\>, System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\>) | Führt die angegebenen Eingabe‑PDF‑Dokumente zu einem einzigen Ausgabe‑PDF‑Dokument zusammen, wobei die angegebenen Eingabe‑ und Ausgabeströme verwendet werden. |
| static [Type](./type/)() |  |
## Siehe auch

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
