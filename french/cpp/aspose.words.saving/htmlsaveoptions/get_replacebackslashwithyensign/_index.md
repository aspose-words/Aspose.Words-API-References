---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ReplaceBackslashWithYenSign méthode"
linktitle: "get_ReplaceBackslashWithYenSign"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ReplaceBackslashWithYenSign méthode. Spécifie si les caractères de barre oblique inverse doivent être remplacés par des signes yen. La valeur par défaut est false en C++."
type: docs
weight: 41500
url: /fr/cpp/aspose.words.saving/htmlsaveoptions/get_replacebackslashwithyensign/
---
## HtmlSaveOptions::get_ReplaceBackslashWithYenSign method


Spécifie si les caractères antislash doivent être remplacés par des signes yen. La valeur par défaut est **false**.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ReplaceBackslashWithYenSign() const
```


## Exemples



Montre comment remplacer les caractères de barre oblique inverse par des signes yen (Html).
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Korean backslash symbol.docx");

// Par défaut, Aspose.Words imite le comportement de MS Word et ne remplace pas les caractères de barre oblique inverse par des signes yen dans
// généré des documents HTML. Cependant, les versions précédentes d'Aspose.Words effectuaient de tels remplacements dans certains
// scénarios. Ce drapeau active la compatibilité descendante avec les versions précédentes d'Aspose.Words.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
saveOptions->set_ReplaceBackslashWithYenSign(true);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.ReplaceBackslashWithYenSign.html", saveOptions);
```

## Voir aussi

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
