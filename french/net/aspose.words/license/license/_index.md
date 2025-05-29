---
title: License
linktitle: License
articleTitle: License
second_title: Aspose.Words pour .NET
description: Créez et gérez facilement vos licences grâce à notre classe constructeur. Simplifiez votre processus de gestion des licences et gagnez en efficacité dès aujourd'hui !
type: docs
weight: 10
url: /fr/net/aspose.words/license/license/
---
## License constructor

Initialise une nouvelle instance de cette classe.

```csharp
public License()
```

## Exemples

Montre comment initialiser une licence pour Aspose.Words à l'aide d'un fichier de licence dans le système de fichiers local.

```csharp
// Définissez la licence de notre produit Aspose.Words en transmettant le nom de fichier du système de fichiers local d'un fichier de licence valide.
string licenseFileName = Path.Combine(LicenseDir, "Aspose.Words.NET.lic");

License license = new License();
license.SetLicense(licenseFileName);

// Créez une copie de notre fichier de licence dans le dossier binaires de notre application.
string licenseCopyFileName = Path.Combine(AssemblyDir, "Aspose.Words.NET.lic");
File.Copy(licenseFileName, licenseCopyFileName);

// Si nous passons le nom d'un fichier sans chemin,
// SetLicense recherchera plusieurs emplacements du système de fichiers local pour ce fichier.
// L’un de ces emplacements sera le dossier « bin », qui contient une copie de notre fichier de licence.
license.SetLicense("Aspose.Words.NET.lic");
```

### Voir également

* class [License](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
