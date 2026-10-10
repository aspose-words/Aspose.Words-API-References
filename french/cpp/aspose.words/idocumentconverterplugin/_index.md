---
title: "interface Aspose::Words::IDocumentConverterPlugin"
linktitle: "IDocumentConverterPlugin"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "interface Aspose::Words::IDocumentConverterPlugin. Définit une interface pour un plugin de conversion externe en C++."
type: docs
weight: 76250
url: /fr/cpp/aspose.words/idocumentconverterplugin/
---
## IDocumentConverterPlugin interface


Définit une interface pour un plug-in de convertisseur externe.

```cpp
class IDocumentConverterPlugin : public virtual System::Object
```

## Méthodes

| Méthode | Description |
| --- | --- |
| virtual [Convert](./convert/)(System::SharedPtr\<System::IO::Stream\>, System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>, System::SharedPtr\<System::IO::Stream\>, System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>) | Convertit le document en utilisant les flux d'entrée et de sortie spécifiés ainsi que les options d'enregistrement. |
| virtual [ConvertToImages](./converttoimages/)(System::SharedPtr\<System::IO::Stream\>, System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>, System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>) | Convertit les pages d'un document depuis le flux d'entrée en un tableau d'images. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## Voir aussi

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
