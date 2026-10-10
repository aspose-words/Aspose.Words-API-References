---
title: "Méthode Aspose::Words::Style::get_BuiltIn"
linktitle: "get_BuiltIn"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Style::get_BuiltIn. Vrai si ce style fait partie des styles intégrés dans MS Word en C++."
type: docs
weight: 6000
url: /fr/cpp/aspose.words/style/get_builtin/
---
## Style::get_BuiltIn method


Vrai si ce style fait partie des styles intégrés dans MS Word.

```cpp
bool Aspose::Words::Style::get_BuiltIn()
```


## Exemples



Montre comment différencier les styles personnalisés des styles intégrés.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Lorsque nous créons un document avec Microsoft Word, ou de manière programmatique avec Aspose.Words,
// le document sera fourni avec une collection de styles à appliquer à son texte pour modifier son apparence.
// Nous pouvons accéder à ces styles intégrés via la collection "Styles" du document.
// Ces styles auront tous le drapeau "BuiltIn" défini sur "true".
System::SharedPtr<Aspose::Words::Style> style = doc->get_Styles()->idx_get(u"Emphasis");

ASSERT_TRUE(style->get_BuiltIn());

// Créez un style personnalisé et ajoutez-le à la collection.
// Les styles personnalisés comme celui-ci auront le drapeau "BuiltIn" défini sur "false".
style = doc->get_Styles()->Add(Aspose::Words::StyleType::Character, u"MyStyle");
style->get_Font()->set_Color(System::Drawing::Color::get_Navy());
style->get_Font()->set_Name(u"Courier New");

ASSERT_FALSE(style->get_BuiltIn());
```

## Voir aussi

* Class [Style](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
