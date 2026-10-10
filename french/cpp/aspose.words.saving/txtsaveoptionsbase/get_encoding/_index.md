---
title: "Méthode Aspose::Words::Saving::TxtSaveOptionsBase::get_Encoding"
linktitle: "get_Encoding"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Saving::TxtSaveOptionsBase::get_Encoding. Spécifie l'encodage à utiliser lors de l'exportation aux formats texte. La valeur par défaut est Encoding.UTF8 en C++."
type: docs
weight: 3000
url: /fr/cpp/aspose.words.saving/txtsaveoptionsbase/get_encoding/
---
## TxtSaveOptionsBase::get_Encoding method


Spécifie l'encodage à utiliser lors de l'exportation dans des formats texte. La valeur par défaut est **Encoding.UTF8**.

```cpp
System::SharedPtr<System::Text::Encoding> Aspose::Words::Saving::TxtSaveOptionsBase::get_Encoding() const
```


## Exemples



Montre comment définir l'encodage pour un document de sortie .txt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Ajoutez du texte contenant des caractères en dehors du jeu de caractères ASCII.
builder->Write(u"À È Ì Ò Ù.");

// Créez un objet "TxtSaveOptions" que nous pouvons passer à la méthode "Save" du document
// pour modifier la façon dont nous enregistrons le document en texte brut.
auto txtSaveOptions = System::MakeObject<Aspose::Words::Saving::TxtSaveOptions>();

// Vérifiez que la propriété "Encoding" contient l'encodage approprié pour le contenu de notre document.
ASPOSE_ASSERT_EQ(System::Text::Encoding::get_UTF8(), txtSaveOptions->get_Encoding());

doc->Save(get_ArtifactsDir() + u"TxtSaveOptions.Encoding.UTF8.txt", txtSaveOptions);

System::String docText = System::Text::Encoding::get_UTF8()->GetString(System::IO::File::ReadAllBytes(get_ArtifactsDir() + u"TxtSaveOptions.Encoding.UTF8.txt"));

ASSERT_EQ(u"\ufeffÀ È Ì Ò Ù.\r\n", docText);

// L'utilisation d'un encodage inadapté peut entraîner une perte du contenu du document.
txtSaveOptions->set_Encoding(System::Text::Encoding::get_ASCII());
doc->Save(get_ArtifactsDir() + u"TxtSaveOptions.Encoding.ASCII.txt", txtSaveOptions);
docText = System::Text::Encoding::get_ASCII()->GetString(System::IO::File::ReadAllBytes(get_ArtifactsDir() + u"TxtSaveOptions.Encoding.ASCII.txt"));

ASSERT_EQ(u"? ? ? ? ?.\r\n", docText);
```

## Voir aussi

* Class [TxtSaveOptionsBase](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
