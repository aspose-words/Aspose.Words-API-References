---
title: "Aspose::Words::IDocumentMergerPlugin interface"
linktitle: "IDocumentMergerPlugin"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::IDocumentMergerPlugin interface. Definisce un'interfaccia per plugin di fusione esterni che possono unire documenti PDF in C++."
type: docs
weight: 76500
url: /it/cpp/aspose.words/idocumentmergerplugin/
---
## IDocumentMergerPlugin interface


Definisce un'interfaccia per plugin di fusione esterno che può unire documenti Pdf.

```cpp
class IDocumentMergerPlugin : public virtual System::Object
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Merge](./merge/)(System::SharedPtr\<System::IO::Stream\>, System::ArrayPtr\<System::SharedPtr\<System::IO::Stream\>\>, System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\>) | Unisce i documenti PDF di input forniti in un unico documento PDF di output utilizzando i flussi di input e output specificati. |
| static [Type](./type/)() |  |
## Vedi anche

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
