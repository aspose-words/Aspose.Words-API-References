---
title: "Aspose::Words::IDocumentReaderPlugin interface"
linktitle: "IDocumentReaderPlugin"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::IDocumentReaderPlugin interface. Definisce un'interfaccia per plugin lettori esterni che possono leggere un file in un documento in C++."
type: docs
weight: 77000
url: /it/cpp/aspose.words/idocumentreaderplugin/
---
## IDocumentReaderPlugin interface


Definisce un'interfaccia per plugin lettori esterni che possono leggere un file in un documento.

```cpp
class IDocumentReaderPlugin : public virtual System::Object
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Read](./read/)(System::SharedPtr\<System::IO::Stream\>, System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>, System::SharedPtr\<Aspose::Words::Document\>) | Legge i dati dallo stream specificato nell'istanza [Document](../document/). |
| static [Type](./type/)() |  |
## Vedi anche

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
