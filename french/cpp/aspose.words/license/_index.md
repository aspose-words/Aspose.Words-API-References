---
title: "Aspose::Words::License class"
linktitle: "License"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::License class. Fournit des méthodes pour licencier le composant. Pour en savoir plus, consultez l’article de documentation en C++."
type: docs
weight: 39000
url: /fr/cpp/aspose.words/license/
---
## License class


Fournit des méthodes pour licencier le composant. Pour en savoir plus, consultez l'article de documentation [Licensing and Subscription](https://docs.aspose.com/words/cpp/licensing/).

```cpp
class License : public System::Object
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [License](./license/)() | Initialise une nouvelle instance de cette classe. |
| [SetLicense](./setlicense/)(const System::String\&) | Licence le composant. |
| [SetLicense](./setlicense/)(const System::SharedPtr\<System::IO::Stream\>\&) | Licence le composant. |
| [SetLicense](./setlicense/)(std::basic_istream\<CharType, Traits\>\&) |  |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
