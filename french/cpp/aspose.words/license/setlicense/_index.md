---
title: "Aspose::Words::License::SetLicense méthode"
linktitle: "SetLicense"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::License::SetLicense méthode. Licence le composant en C++."
type: docs
weight: 5000
url: /fr/cpp/aspose.words/license/setlicense/
---
## License::SetLicense(const System::SharedPtr\<System::IO::Stream\>\&) method


Licence le composant.

```cpp
void Aspose::Words::License::SetLicense(const System::SharedPtr<System::IO::Stream> &stream)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| flux | const System::SharedPtr\<System::IO::Stream\>\& | Un flux qui contient la licence. |
## Remarques


Utilisez cette méthode pour charger une licence depuis un flux.

## Exemples



Montre comment initialiser une licence pour Aspose.Words depuis un flux.
```cpp
System::String testLicenseFileName = u"Aspose.Words.Cpp.lic";
// Définissez la licence de notre produit Aspose.Words en passant un flux contenant un fichier de licence valide dans notre système de fichiers local.
{
    System::SharedPtr<System::IO::Stream> myStream = System::IO::File::OpenRead(System::IO::Path::Combine(get_LicenseDir(), testLicenseFileName));
    auto license = System::MakeObject<Aspose::Words::License>();
    license->SetLicense(myStream);
}
```

## Voir aussi

* Class [License](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## License::SetLicense(const System::String\&) method


Licence le composant.

```cpp
void Aspose::Words::License::SetLicense(const System::String &licenseName)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| licenseName | const System::String\& | Peut être un nom de fichier complet ou court. Utilisez une chaîne vide pour passer en mode d'évaluation. |
## Remarques


Essaie de trouver la licence aux emplacements suivants:

1. Chemin explicite.
1. Le dossier qui contient la bibliothèque Aspose.Words.
1. Le dossier qui contient l'application du client.



## Exemples



Montre comment initialiser une licence pour Aspose.Words en utilisant un fichier de licence dans le système de fichiers local.
```cpp
System::String testLicenseFileName = u"Aspose.Words.Cpp.lic";

// Définissez la licence de notre produit Aspose.Words en passant le nom de fichier du système de fichiers local d’un fichier de licence valide.
System::String licenseFileName = System::IO::Path::Combine(get_LicenseDir(), testLicenseFileName);

auto license = System::MakeObject<Aspose::Words::License>();
license->SetLicense(licenseFileName);

// Créez une copie de notre fichier de licence dans le dossier des binaires de notre application.
System::String licenseCopyFileName = System::IO::Path::Combine(get_AssemblyDir(), testLicenseFileName);
System::IO::File::Copy(licenseFileName, licenseCopyFileName);

// Si nous transmettons le nom d’un fichier sans chemin,
// la méthode SetLicense recherchera plusieurs emplacements du système de fichiers locaux pour ce fichier.
// L'un de ces emplacements sera le dossier "bin", qui contient une copie de notre fichier de licence.
license->SetLicense(testLicenseFileName);
```

## Voir aussi

* Class [License](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## License::SetLicense(std::basic_istream\<CharType, Traits\>\&) method




```cpp
template<typename CharType,typename Traits> void Aspose::Words::License::SetLicense(std::basic_istream<CharType, Traits> &stream)
```

## Voir aussi

* Class [License](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
