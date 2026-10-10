---
title: "Aspose::Words::IDocumentReaderPlugin interface"
linktitle: "IDocumentReaderPlugin"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::IDocumentReaderPlugin interface. Définit une interface pour des plug‑ins de lecture externes pouvant lire un fichier dans un document en C++."
type: docs
weight: 77000
url: /fr/cpp/aspose.words/idocumentreaderplugin/
---
## IDocumentReaderPlugin interface


Définit une interface pour des plug-ins de lecture externes capables de lire un fichier dans un document.

```cpp
class IDocumentReaderPlugin : public virtual System::Object
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Read](./read/)(System::SharedPtr\<System::IO::Stream\>, System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>, System::SharedPtr\<Aspose::Words::Document\>) | Lit les données du flux spécifié dans l’instance [Document](../document/). |
| static [Type](./type/)() |  |
## Voir aussi

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
