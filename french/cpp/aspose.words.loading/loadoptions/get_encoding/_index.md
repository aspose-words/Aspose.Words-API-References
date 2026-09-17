---
title: "Méthode Aspose::Words::Loading::LoadOptions::get_Encoding"
linktitle: "get_Encoding"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Loading::LoadOptions::get_Encoding. Obtient ou définit l'encodage qui sera utilisé pour charger un document HTML, TXT ou CHM si l'encodage n'est pas spécifié dans le document. Peut être null. La valeur par défaut est null en C++."
type: docs
weight: 6000
url: /fr/cpp/aspose.words.loading/loadoptions/get_encoding/
---
## LoadOptions::get_Encoding method


Obtient ou définit l'encodage qui sera utilisé pour charger un document HTML, TXT ou CHM si l'encodage n'est pas spécifié dans le document. Peut être **null**. La valeur par défaut est **null**.

```cpp
System::SharedPtr<System::Text::Encoding> Aspose::Words::Loading::LoadOptions::get_Encoding() const
```

## Remarques


Cette propriété n'est utilisée que lors du chargement de documents HTML, TXT ou CHM.

Si l'encodage n'est pas spécifié dans le document et que cette propriété est **null**, le système tentera de détecter automatiquement l'encodage.

## Exemples



Montre comment définir l'encodage avec lequel ouvrir un document.
```cpp
auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
loadOptions->set_Encoding(System::Text::Encoding::get_ASCII());

// Chargez le document en passant l'objet LoadOptions, puis vérifiez le contenu du document.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"English text.txt", loadOptions);

ASSERT_TRUE(doc->ToString(Aspose::Words::SaveFormat::Text).Contains(u"This is a sample text in English."));
```

## Voir aussi

* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
