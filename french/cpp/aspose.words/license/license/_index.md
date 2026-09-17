---
title: "Aspose::Words::License::License constructeur"
linktitle: "License"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::License::License constructeur. Initialise une nouvelle instance de cette classe en C++."
type: docs
weight: 2000
url: /fr/cpp/aspose.words/license/license/
---
## License::License constructor


Initialise une nouvelle instance de cette classe.

```cpp
Aspose::Words::License::License()
```


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
