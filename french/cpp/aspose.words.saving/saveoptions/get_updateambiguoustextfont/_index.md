---
title: "Méthode Aspose::Words::Saving::SaveOptions::get_UpdateAmbiguousTextFont"
linktitle: "get_UpdateAmbiguousTextFont"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Saving::SaveOptions::get_UpdateAmbiguousTextFont. Détermine si les attributs de police seront modifiés en fonction du code de caractère utilisé en C++."
type: docs
weight: 15500
url: /fr/cpp/aspose.words.saving/saveoptions/get_updateambiguoustextfont/
---
## SaveOptions::get_UpdateAmbiguousTextFont method


Détermine si les attributs de police seront modifiés en fonction du code de caractère utilisé.

```cpp
bool Aspose::Words::Saving::SaveOptions::get_UpdateAmbiguousTextFont() const
```


## Exemples



Montre comment mettre à jour la police pour correspondre au code de caractère utilisé.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Special symbol.docx");
System::SharedPtr<Aspose::Words::Run> run = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0);
std::cout << run->get_Text() << std::endl;
// ฿
std::cout << run->get_Font()->get_Name() << std::endl;
// Arial

auto saveOptions = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>();
saveOptions->set_UpdateAmbiguousTextFont(true);
doc->Save(get_ArtifactsDir() + u"OoxmlSaveOptions.UpdateAmbiguousTextFont.docx", saveOptions);

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"OoxmlSaveOptions.UpdateAmbiguousTextFont.docx");
run = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0);
std::cout << run->get_Text() << std::endl;
// ฿
std::cout << run->get_Font()->get_Name() << std::endl;
// Angsana New
```

## Voir aussi

* Class [SaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
