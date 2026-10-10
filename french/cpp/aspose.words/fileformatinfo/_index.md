---
title: "Aspose::Words::FileFormatInfo classe"
linktitle: "FileFormatInfo"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::FileFormatInfo classe. Contient les données renvoyées par les méthodes de détection du format de document de FileFormatUtil. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 27000
url: /fr/cpp/aspose.words/fileformatinfo/
---
## FileFormatInfo class


Contient les données renvoyées par les méthodes de détection du format de document de [FileFormatUtil](../fileformatutil/). Pour en savoir plus, consultez l'article de documentation [Detect File Format and Check Format Compatibility](https://docs.aspose.com/words/cpp/detect-file-format-and-check-format-compatibility/).

```cpp
class FileFormatInfo : public System::Object
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [get_Encoding](./get_encoding/)() const | Obtient l'encodage détecté si applicable au format du document actuel. Pour le moment, il ne détecte l'encodage que pour les documents HTML. |
| [get_HasDigitalSignature](./get_hasdigitalsignature/)() const | Renvoie **true** si ce document contient une signature numérique. Cette propriété indique simplement qu'une signature numérique est présente sur un document, mais elle ne précise pas si la signature est valide ou non. |
| [get_HasMacros](./get_hasmacros/)() const | Renvoie **true** si ce document contient des macros VBA. |
| [get_IsEncrypted](./get_isencrypted/)() const | Renvoie **true** si le document est chiffré et nécessite un mot de passe pour être ouvert. |
| [get_LoadFormat](./get_loadformat/)() const | Obtient le format de document détecté. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## Remarques


Vous ne créez pas d'instances de cette classe directement. Les objets de cette classe sont renvoyés par les méthodes [DetectFileFormat()](../).

## Exemples



Montre comment utiliser la classe [FileFormatUtil](../fileformatutil/) pour détecter le format du document et le chiffrement.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Configurez un objet SaveOptions pour chiffrer le document
// avec un mot de passe lors de l'enregistrement, puis enregistrez le document.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::OdtSaveOptions>(Aspose::Words::SaveFormat::Odt);
saveOptions->set_Password(u"MyPassword");

doc->Save(get_ArtifactsDir() + u"File.DetectDocumentEncryption.odt", saveOptions);

// Vérifiez le type de fichier de notre document ainsi que son état de chiffrement.
System::SharedPtr<Aspose::Words::FileFormatInfo> info = Aspose::Words::FileFormatUtil::DetectFileFormat(get_ArtifactsDir() + u"File.DetectDocumentEncryption.odt");

ASSERT_EQ(u".odt", Aspose::Words::FileFormatUtil::LoadFormatToExtension(info->get_LoadFormat()));
ASSERT_TRUE(info->get_IsEncrypted());
```


Montre comment utiliser la classe [FileFormatUtil](../fileformatutil/) pour détecter le format du document et la présence de signatures numériques.
```cpp
// Utilisez une instance de FileFormatInfo pour vérifier qu'un document n'est pas signé numériquement.
System::SharedPtr<Aspose::Words::FileFormatInfo> info = Aspose::Words::FileFormatUtil::DetectFileFormat(get_MyDir() + u"Document.docx");

ASSERT_EQ(u".docx", Aspose::Words::FileFormatUtil::LoadFormatToExtension(info->get_LoadFormat()));
ASSERT_FALSE(info->get_HasDigitalSignature());

System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> certificateHolder = Aspose::Words::DigitalSignatures::CertificateHolder::Create(get_MyDir() + u"morzal.pfx", u"aw", nullptr);
auto signOptions = System::MakeObject<Aspose::Words::DigitalSignatures::SignOptions>();
signOptions->set_SignTime(System::DateTime::get_Now());
Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign(get_MyDir() + u"Document.docx", get_ArtifactsDir() + u"File.DetectDigitalSignatures.docx", certificateHolder, signOptions);

// Utilisez une nouvelle FileFormatInstance pour confirmer qu'il est signé.
info = Aspose::Words::FileFormatUtil::DetectFileFormat(get_ArtifactsDir() + u"File.DetectDigitalSignatures.docx");

ASSERT_TRUE(info->get_HasDigitalSignature());

// Nous pouvons charger et accéder aux signatures d'un document signé dans une collection comme celle-ci.
ASSERT_EQ(1, Aspose::Words::DigitalSignatures::DigitalSignatureUtil::LoadSignatures(get_ArtifactsDir() + u"File.DetectDigitalSignatures.docx")->get_Count());
```

## Voir aussi

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
