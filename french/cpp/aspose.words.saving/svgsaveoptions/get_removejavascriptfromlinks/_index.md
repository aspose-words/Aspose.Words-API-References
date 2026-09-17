---
title: "Méthode Aspose::Words::Saving::SvgSaveOptions::get_RemoveJavaScriptFromLinks"
linktitle: "get_RemoveJavaScriptFromLinks"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Saving::SvgSaveOptions::get_RemoveJavaScriptFromLinks. Indique si le JavaScript sera supprimé des liens. La valeur par défaut est false. Si cette option est activée, tous les liens contenant du JavaScript seront remplacés par \"javascript:void(0)\" en C++."
type: docs
weight: 4750
url: /fr/cpp/aspose.words.saving/svgsaveoptions/get_removejavascriptfromlinks/
---
## SvgSaveOptions::get_RemoveJavaScriptFromLinks method


Spécifie si le JavaScript sera supprimé des liens. La valeur par défaut est **false**. Si cette option est activée, tous les liens contenant du JavaScript seront remplacés par "javascript:void(0)".

```cpp
bool Aspose::Words::Saving::SvgSaveOptions::get_RemoveJavaScriptFromLinks() const
```


## Exemples



Montre comment supprimer le JavaScript des liens (svg).
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"JavaScript in HREF.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::SvgSaveOptions>();
saveOptions->set_RemoveJavaScriptFromLinks(true);

doc->Save(get_ArtifactsDir() + u"SvgSaveOptions.RemoveJavaScriptFromLinksSvg.html", saveOptions);
```

## Voir aussi

* Class [SvgSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
