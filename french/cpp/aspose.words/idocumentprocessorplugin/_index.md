---
title: "Interface Aspose::Words::IDocumentProcessorPlugin"
linktitle: "IDocumentProcessorPlugin"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Interface Aspose::Words::IDocumentProcessorPlugin. Définit une interface pour un plugin de traitement de documents externe en C++."
type: docs
weight: 76750
url: /fr/cpp/aspose.words/idocumentprocessorplugin/
---
## IDocumentProcessorPlugin interface


Définit une interface pour un plug-in de traitement de document externe.

```cpp
class IDocumentProcessorPlugin : public virtual System::Object
```

## Méthodes

| Méthode | Description |
| --- | --- |
| virtual [Append](./append/)(System::SharedPtr\<System::IO::Stream\>, System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>) | Ajoutez le document en le chargeant avec les options de chargement spécifiées. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Load](./load/)(System::SharedPtr\<System::IO::Stream\>, System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>) | Chargez le document en utilisant les options de chargement spécifiées. |
| virtual [Save](./save/)(System::SharedPtr\<System::IO::Stream\>, System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>) | Enregistrez le document chargé par la méthode [Load()](./load/) dans le flux de sortie en utilisant les options d'enregistrement spécifiées. |
| virtual [SetImageWatermark](./setimagewatermark/)(System::SharedPtr\<System::IO::Stream\>, System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>) | Ajoute un filigrane d'image sur chaque page du document chargé par la méthode [Load()](./load/). |
| virtual [SetTextWatermark](./settextwatermark/)(System::String, System::SharedPtr\<Aspose::Words::TextWatermarkOptions\>) | Ajoute un filigrane de texte sur chaque page du document chargé par la méthode [Load()](./load/). |
| virtual [ToDocument](./todocument/)() | Analyse le document chargé par la méthode [Load()](./load/) en un objet [Document](../document/). |
| virtual [ToPages](./topages/)(System::SharedPtr\<Aspose::Words::Saving::FixedPageSaveOptions\>) | Enregistre chaque page du document chargé par la méthode [Load()](./load/) en utilisant les options d'enregistrement de page fixe spécifiées. |
| static [Type](./type/)() |  |
## Voir aussi

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
