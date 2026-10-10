---
title: "Méthode Aspose::Words::Saving::HtmlFixedSaveOptions::get_IdPrefix"
linktitle: "get_IdPrefix"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Saving::HtmlFixedSaveOptions::get_IdPrefix. Spécifie un préfixe qui est ajouté au début de tous les ID d'éléments générés dans le document de sortie. La valeur par défaut est null et aucun préfixe n'est ajouté en C++."
type: docs
weight: 10500
url: /fr/cpp/aspose.words.saving/htmlfixedsaveoptions/get_idprefix/
---
## HtmlFixedSaveOptions::get_IdPrefix method


Spécifie un préfixe qui est ajouté au début de tous les ID d'éléments générés dans le document de sortie. La valeur par défaut est null et aucun préfixe n'est ajouté.

```cpp
System::String Aspose::Words::Saving::HtmlFixedSaveOptions::get_IdPrefix() const
```


## Exemples



Montre comment ajouter un préfixe qui est ajouté au début de tous les ID d'éléments générés.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Id prefix.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::HtmlFixedSaveOptions>();
saveOptions->set_IdPrefix(u"pfx1_");

doc->Save(get_ArtifactsDir() + u"HtmlFixedSaveOptions.IdPrefix.html", saveOptions);
```

## Voir aussi

* Class [HtmlFixedSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
