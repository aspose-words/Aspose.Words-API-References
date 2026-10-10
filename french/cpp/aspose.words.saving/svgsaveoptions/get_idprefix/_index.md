---
title: "Aspose::Words::Saving::SvgSaveOptions::get_IdPrefix méthode"
linktitle: "get_IdPrefix"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::SvgSaveOptions::get_IdPrefix méthode. Spécifie un préfixe qui est ajouté au début de tous les ID d'éléments générés dans le document de sortie. La valeur par défaut est null et aucun préfixe n'est ajouté en C++."
type: docs
weight: 4250
url: /fr/cpp/aspose.words.saving/svgsaveoptions/get_idprefix/
---
## SvgSaveOptions::get_IdPrefix method


Spécifie un préfixe qui est ajouté au début de tous les ID d'éléments générés dans le document de sortie. La valeur par défaut est null et aucun préfixe n'est ajouté.

```cpp
System::String Aspose::Words::Saving::SvgSaveOptions::get_IdPrefix() const
```


## Exemples



Montre comment ajouter un préfixe qui est ajouté au début de tous les ID d'éléments générés (svg).
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Id prefix.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::SvgSaveOptions>();
saveOptions->set_IdPrefix(u"pfx1_");

doc->Save(get_ArtifactsDir() + u"SvgSaveOptions.IdPrefixSvg.html", saveOptions);
```

## Voir aussi

* Class [SvgSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
