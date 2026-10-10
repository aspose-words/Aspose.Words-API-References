---
title: "Aspose::Words::Saving::DocSaveOptions::get_SaveFormat méthode"
linktitle: "get_SaveFormat"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::DocSaveOptions::get_SaveFormat méthode. Spécifie le format dans lequel le document sera enregistré si cet objet d'options de sauvegarde est utilisé. Peut être Doc ou Dot en C++."
type: docs
weight: 5000
url: /fr/cpp/aspose.words.saving/docsaveoptions/get_saveformat/
---
## DocSaveOptions::get_SaveFormat method


Spécifie le format dans lequel le document sera enregistré si cet objet d'options d'enregistrement est utilisé. Peut être [Doc](../../../aspose.words/saveformat/) ou [Dot](../../../aspose.words/saveformat/).

```cpp
Aspose::Words::SaveFormat Aspose::Words::Saving::DocSaveOptions::get_SaveFormat() override
```


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

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [DocSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
