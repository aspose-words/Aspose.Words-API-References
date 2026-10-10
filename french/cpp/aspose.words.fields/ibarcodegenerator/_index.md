---
title: "Interface Aspose::Words::Fields::IBarcodeGenerator"
linktitle: "IBarcodeGenerator"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Interface Aspose::Words::Fields::IBarcodeGenerator. Interface publique pour un générateur de code-barres personnalisé. L'implémentation doit être fournie par l'utilisateur en C++."
type: docs
weight: 118000
url: /fr/cpp/aspose.words.fields/ibarcodegenerator/
---
## IBarcodeGenerator interface


Interface publique pour le générateur de code-barres personnalisé. L'implémentation doit être fournie par l'utilisateur.

```cpp
class IBarcodeGenerator : public virtual System::Object
```

## Méthodes

| Méthode | Description |
| --- | --- |
| virtual [GetBarcodeImage](./getbarcodeimage/)(System::SharedPtr\<Aspose::Words::Fields::BarcodeParameters\>) | Générer une image de code-barres en utilisant l'ensemble des paramètres (pour le champ DisplayBarcode). |
| virtual [GetOldBarcodeImage](./getoldbarcodeimage/)(System::SharedPtr\<Aspose::Words::Fields::BarcodeParameters\>) | Générer une image de code-barres en utilisant l'ensemble des paramètres (pour le champ Barcode à l'ancienne). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## Voir aussi

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
