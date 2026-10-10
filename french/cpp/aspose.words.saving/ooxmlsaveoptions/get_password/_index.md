---
title: "Aspose::Words::Saving::OoxmlSaveOptions::get_Password méthode"
linktitle: "get_Password"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::OoxmlSaveOptions::get_Password méthode. Obtient/definit un mot de passe pour chiffrer le document en utilisant l'algorithme de chiffrement standard ECMA376 en C++."
type: docs
weight: 6000
url: /fr/cpp/aspose.words.saving/ooxmlsaveoptions/get_password/
---
## OoxmlSaveOptions::get_Password method


Obtient/définit un mot de passe pour chiffrer le document en utilisant l'algorithme de chiffrement ECMA376 Standard.

```cpp
System::String Aspose::Words::Saving::OoxmlSaveOptions::get_Password() const
```

## Remarques


Afin d'enregistrer le document sans chiffrement, cette propriété doit être **null** ou une chaîne vide.

## Exemples



Montre comment créer un document Office Open XML chiffré par mot de passe.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>();
saveOptions->set_Password(u"MyPassword");

doc->Save(get_ArtifactsDir() + u"OoxmlSaveOptions.Password.docx", saveOptions);

// Nous ne pourrons pas ouvrir ce document avec Microsoft Word ou
// Aspose.Words sans fournir le mot de passe correct.
ASSERT_THROW(static_cast<std::function<void()>>([&doc]() -> void
{
    doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"OoxmlSaveOptions.Password.docx");
})(), Aspose::Words::IncorrectPasswordException);

// Ouvrez le document chiffré en transmettant le mot de passe correct dans un objet LoadOptions.
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"OoxmlSaveOptions.Password.docx", System::MakeObject<Aspose::Words::Loading::LoadOptions>(u"MyPassword"));

ASSERT_EQ(u"Hello world!", doc->GetText().Trim());
```

## Voir aussi

* Class [OoxmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
