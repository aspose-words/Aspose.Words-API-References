---
title: "Aspose::Words::Saving::HtmlFixedSaveOptions::get_RemoveJavaScriptFromLinks méthode"
linktitle: "get_RemoveJavaScriptFromLinks"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::HtmlFixedSaveOptions::get_RemoveJavaScriptFromLinks méthode. Spécifie si le JavaScript sera supprimé des liens. La valeur par défaut est false en C++."
type: docs
weight: 13500
url: /fr/cpp/aspose.words.saving/htmlfixedsaveoptions/get_removejavascriptfromlinks/
---
## HtmlFixedSaveOptions::get_RemoveJavaScriptFromLinks method


Spécifie si le JavaScript sera supprimé des liens. La valeur par défaut est **false**.

```cpp
bool Aspose::Words::Saving::HtmlFixedSaveOptions::get_RemoveJavaScriptFromLinks() const
```


## Exemples



Montre comment supprimer le JavaScript des liens pour les documents HTML à page fixe.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"JavaScript in HREF.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::HtmlFixedSaveOptions>();
saveOptions->set_RemoveJavaScriptFromLinks(true);

doc->Save(get_ArtifactsDir() + u"HtmlFixedSaveOptions.RemoveJavaScriptFromLinks.html", saveOptions);
```


Montre comment supprimer le JavaScript des liens.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"JavaScript in HREF.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
saveOptions->set_RemoveJavaScriptFromLinks(true);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.RemoveJavaScriptFromLinks.html", saveOptions);
```

## Voir aussi

* Class [HtmlFixedSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
