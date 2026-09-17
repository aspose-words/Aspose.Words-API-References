---
title: "Constructeur Aspose::Words::Loading::HtmlLoadOptions::HtmlLoadOptions"
linktitle: "HtmlLoadOptions"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Constructeur Aspose::Words::Loading::HtmlLoadOptions::HtmlLoadOptions. Initialise une nouvelle instance de cette classe avec les valeurs par défaut en C++."
type: docs
weight: 2000
url: /fr/cpp/aspose.words.loading/htmlloadoptions/htmlloadoptions/
---
## HtmlLoadOptions::HtmlLoadOptions() constructor


Initialise une nouvelle instance de cette classe avec les valeurs par défaut.

```cpp
Aspose::Words::Loading::HtmlLoadOptions::HtmlLoadOptions()
```


## Exemples



Montre comment prendre en charge les commentaires conditionnels lors du chargement d'un document HTML.
```cpp
auto loadOptions = System::MakeObject<Aspose::Words::Loading::HtmlLoadOptions>();

// Si la valeur est vraie, alors nous prenons en compte le code VML lors de l'analyse du document chargé.
loadOptions->set_SupportVml(supportVml);

// Ce document contient une image JPEG dans les balises "<!--[if gte vml 1]>" ,
// et une image PNG différente dans les balises "<![if !vml]>".
// Si nous définissons le drapeau "SupportVml" sur "true", alors Aspose.Words chargera le JPEG.
// Si nous définissons ce drapeau sur "false", alors Aspose.Words ne chargera que le PNG.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"VML conditional.htm", loadOptions);

if (supportVml)
{
    ASSERT_EQ(Aspose::Words::Drawing::ImageType::Jpeg, (System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true)))->get_ImageData()->get_ImageType());
}
else
{
    ASSERT_EQ(Aspose::Words::Drawing::ImageType::Png, (System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true)))->get_ImageData()->get_ImageType());
}
```

## Voir aussi

* Class [HtmlLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
## HtmlLoadOptions::HtmlLoadOptions(Aspose::Words::LoadFormat, const System::String\&, const System::String\&) constructor


Un raccourci pour initialiser une nouvelle instance de cette classe avec les propriétés définies aux valeurs spécifiées.

```cpp
Aspose::Words::Loading::HtmlLoadOptions::HtmlLoadOptions(Aspose::Words::LoadFormat loadFormat, const System::String &password, const System::String &baseUri)
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
* Class [HtmlLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
## HtmlLoadOptions::HtmlLoadOptions(const System::String\&) constructor


Un raccourci pour initialiser une nouvelle instance de cette classe avec le mot de passe spécifié afin de charger un document chiffré.

```cpp
Aspose::Words::Loading::HtmlLoadOptions::HtmlLoadOptions(const System::String &password)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| password | const System::String\& | Le mot de passe pour ouvrir un document chiffré. Peut être **null** ou une chaîne vide. |

## Exemples



Montre comment chiffrer un document Html, puis l'ouvrir en utilisant un mot de passe.
```cpp
// Créer et signer un document HTML chiffré à partir d'un .docx chiffré.
System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> certificateHolder = Aspose::Words::DigitalSignatures::CertificateHolder::Create(get_MyDir() + u"morzal.pfx", u"aw");

auto signOptions = System::MakeObject<Aspose::Words::DigitalSignatures::SignOptions>();
signOptions->set_Comments(u"Comment");
signOptions->set_SignTime(System::DateTime::get_Now());
signOptions->set_DecryptionPassword(u"docPassword");

System::String inputFileName = get_MyDir() + u"Encrypted.docx";
System::String outputFileName = get_ArtifactsDir() + u"HtmlLoadOptions.EncryptedHtml.html";
Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign(inputFileName, outputFileName, certificateHolder, signOptions);

// Pour charger et lire ce document, nous devrons fournir son déchiffrement
// mot de passe en utilisant un objet HtmlLoadOptions.
auto loadOptions = System::MakeObject<Aspose::Words::Loading::HtmlLoadOptions>(u"docPassword");

ASSERT_EQ(signOptions->get_DecryptionPassword(), loadOptions->get_Password());

auto doc = System::MakeObject<Aspose::Words::Document>(outputFileName, loadOptions);

ASSERT_EQ(u"Test encrypted document.", doc->GetText().Trim());
```

## Voir aussi

* Class [HtmlLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
