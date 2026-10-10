---
title: "Aspose::Words::Loading::LoadOptions::LoadOptions constructeur"
linktitle: "LoadOptions"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Loading::LoadOptions::LoadOptions constructeur. Initialise une nouvelle instance de cette classe avec des valeurs par défaut en C++."
type: docs
weight: 2000
url: /fr/cpp/aspose.words.loading/loadoptions/loadoptions/
---
## LoadOptions::LoadOptions() constructor


Initialise une nouvelle instance de cette classe avec les valeurs par défaut.

```cpp
Aspose::Words::Loading::LoadOptions::LoadOptions()
```


## Exemples



Montre comment ouvrir un document HTML avec des images depuis un flux en utilisant une URI de base.
```cpp
{
    System::SharedPtr<System::IO::Stream> stream = System::IO::File::OpenRead(get_MyDir() + u"Document.html");
    // Passez l'URI du dossier de base lors du chargement.
    // afin que toutes les images avec des URI relatifs dans le document HTML puissent être trouvées.
    auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
    loadOptions->set_BaseUri(get_ImageDir());

    auto doc = System::MakeObject<Aspose::Words::Document>(stream, loadOptions);

    // Vérifiez que la première forme du document contient une image valide.
    auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));

    ASSERT_TRUE(shape->get_IsImage());
    ASSERT_FALSE(System::TestTools::IsNull(shape->get_ImageData()->get_ImageBytes()));
    ASSERT_NEAR(32.0, Aspose::Words::ConvertUtil::PointToPixel(shape->get_Width()), 0.01);
    ASSERT_NEAR(32.0, Aspose::Words::ConvertUtil::PointToPixel(shape->get_Height()), 0.01);
}
```

## Voir aussi

* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
## LoadOptions::LoadOptions(Aspose::Words::LoadFormat, const System::String\&, const System::String\&) constructor


Un raccourci pour initialiser une nouvelle instance de cette classe avec les propriétés définies aux valeurs spécifiées.

```cpp
Aspose::Words::Loading::LoadOptions::LoadOptions(Aspose::Words::LoadFormat loadFormat, const System::String &password, const System::String &baseUri)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| loadFormat | Aspose::Words::LoadFormat | Le format du document à charger. |
| password | const System::String\& | Le mot de passe pour ouvrir un document chiffré. Peut être **null** ou une chaîne vide. |
| baseUri | const System::String\& | La chaîne qui sera utilisée pour résoudre les URI relatives en absolues. Peut être **null** ou une chaîne vide. |

## Exemples



Montre comment spécifier une URI de base lors de l'ouverture d'un document html.
```cpp
// Supposons que nous voulions charger un document .html contenant une image liée par une URI relative
// alors que l'image se trouve à un autre emplacement. Dans ce cas, nous devrons résoudre l'URI relative en une URI absolue.
// Nous pouvons fournir une URI de base en utilisant un objet HtmlLoadOptions.
auto loadOptions = System::MakeObject<Aspose::Words::Loading::HtmlLoadOptions>(Aspose::Words::LoadFormat::Html, u"", get_ImageDir());

ASSERT_EQ(Aspose::Words::LoadFormat::Html, loadOptions->get_LoadFormat());

auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Missing image.html", loadOptions);

// Bien que l'image était cassée dans le .html d'entrée, notre URI de base personnalisée nous a aidés à réparer le lien.
auto imageShape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->idx_get(0));
ASSERT_TRUE(imageShape->get_IsImage());

// Ce document de sortie affichera l'image qui manquait.
doc->Save(get_ArtifactsDir() + u"HtmlLoadOptions.BaseUri.docx");
```

## Voir aussi

* Enum [LoadFormat](../../../aspose.words/loadformat/)
* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
## LoadOptions::LoadOptions(const System::String\&) constructor


Un raccourci pour initialiser une nouvelle instance de cette classe avec le mot de passe spécifié afin de charger un document chiffré.

```cpp
Aspose::Words::Loading::LoadOptions::LoadOptions(const System::String &password)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| password | const System::String\& | Le mot de passe pour ouvrir un document chiffré. Peut être **null** ou une chaîne vide. |

## Exemples



Montre comment charger un document Microsoft Word chiffré.
```cpp
System::SharedPtr<Aspose::Words::Document> doc;

// Aspose.Words lève une exception si nous essayons d'ouvrir un document chiffré sans son mot de passe.
ASSERT_THROW(static_cast<std::function<void()>>([&doc]() -> void
{
    doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Encrypted.docx");
})(), Aspose::Words::IncorrectPasswordException);

// Lors du chargement d'un tel document, le mot de passe est passé au constructeur du document à l'aide d'un objet LoadOptions.
auto options = System::MakeObject<Aspose::Words::Loading::LoadOptions>(u"docPassword");

// Il existe deux façons de charger un document chiffré avec un objet LoadOptions.
// 1 -  Chargez le document depuis le système de fichiers local par nom de fichier :
doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Encrypted.docx", options);

// 2 -  Chargez le document depuis un flux :
{
    System::SharedPtr<System::IO::Stream> stream = System::IO::File::OpenRead(get_MyDir() + u"Encrypted.docx");
    doc = System::MakeObject<Aspose::Words::Document>(stream, options);
}
```

## Voir aussi

* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
