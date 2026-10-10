---
title: "Méthode Aspose::Words::Saving::DocSaveOptions::get_Password"
linktitle: "get_Password"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Saving::DocSaveOptions::get_Password. Obtient/definit un mot de passe pour chiffrer le document en utilisant la méthode de chiffrement RC4 en C++."
type: docs
weight: 4000
url: /fr/cpp/aspose.words.saving/docsaveoptions/get_password/
---
## DocSaveOptions::get_Password method


Obtient/definit un mot de passe pour chiffrer le document en utilisant la méthode de chiffrement RC4.

```cpp
System::String Aspose::Words::Saving::DocSaveOptions::get_Password() const
```

## Remarques


Afin d'enregistrer le document sans chiffrement, cette propriété doit être **null** ou une chaîne vide.

## Exemples



Montre comment définir les options d'enregistrement pour les anciens formats Microsoft Word.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Write(u"Hello world!");

auto options = System::MakeObject<Aspose::Words::Saving::DocSaveOptions>(Aspose::Words::SaveFormat::Doc);

// Définissez un mot de passe qui protégera le chargement du document par Microsoft Word ou Aspose.Words.
// Notez que cela n'encrypte pas le contenu du document de quelque manière que ce soit.
options->set_Password(u"MyPassword");

// Si le document contient un bordereau d'acheminement, nous pouvons le conserver lors de l'enregistrement en définissant ce drapeau sur true.
options->set_SaveRoutingSlip(true);

doc->Save(get_ArtifactsDir() + u"DocSaveOptions.SaveAsDoc.doc", options);

// Pour pouvoir charger le document,
// nous devrons appliquer le mot de passe que nous avons spécifié dans l'objet DocSaveOptions dans un objet LoadOptions.
ASSERT_THROW(static_cast<std::function<void()>>([&doc]() -> void
{
    doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"DocSaveOptions.SaveAsDoc.doc");
})(), Aspose::Words::IncorrectPasswordException);

auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>(u"MyPassword");
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"DocSaveOptions.SaveAsDoc.doc", loadOptions);

ASSERT_EQ(u"Hello world!", doc->GetText().Trim());
```

## Voir aussi

* Class [DocSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
