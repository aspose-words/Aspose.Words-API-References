---
title: "Aspose::Words::Font::get_NumberSpacing méthode"
linktitle: "get_NumberSpacing"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Font::get_NumberSpacing méthode. Obtient ou définit le type d'espacement du chiffre affiché en C++."
type: docs
weight: 30500
url: /fr/cpp/aspose.words/font/get_numberspacing/
---
## Font::get_NumberSpacing method


Obtient ou définit le type d'espacement du chiffre affiché.

```cpp
Aspose::Words::NumSpacing Aspose::Words::Font::get_NumberSpacing()
```


## Exemples



Montre comment définir le type d'espacement du chiffre.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Cet effet n'est pris en charge que dans les versions récentes de MS Word.
doc->get_CompatibilityOptions()->OptimizeFor(Aspose::Words::Settings::MsWordVersion::Word2019);

builder->Write(u"1 ");
builder->Write(u"This is an example");

System::SharedPtr<Aspose::Words::Run> run = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0);
if (run->get_Font()->get_NumberSpacing() == Aspose::Words::NumSpacing::Default)
{
    run->get_Font()->set_NumberSpacing(Aspose::Words::NumSpacing::Proportional);
}

doc->Save(get_ArtifactsDir() + u"Fonts.NumberSpacing.docx");
```

## Voir aussi

* Enum [NumSpacing](../../numspacing/)
* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
