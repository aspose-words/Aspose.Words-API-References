---
title: "Aspose::Words::IDocumentMergerPlugin interface"
linktitle: "IDocumentMergerPlugin"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::IDocumentMergerPlugin interface. Définit une interface pour un plug‑in de fusion externe pouvant fusionner des documents PDF en C++."
type: docs
weight: 76500
url: /fr/cpp/aspose.words/idocumentmergerplugin/
---
## IDocumentMergerPlugin interface


Définit une interface pour un plug-in de fusion externe capable de fusionner des documents Pdf.

```cpp
class IDocumentMergerPlugin : public virtual System::Object
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Merge](./merge/)(System::SharedPtr\<System::IO::Stream\>, System::ArrayPtr\<System::SharedPtr\<System::IO::Stream\>\>, System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\>) | Fusionne les documents PDF d’entrée fournis en un seul document PDF de sortie en utilisant les flux d’entrée et de sortie spécifiés. |
| static [Type](./type/)() |  |
## Voir aussi

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
