---
title: License Class
linktitle: License
articleTitle: License
second_title: Aspose.Words pour .NET
description: Exploitez tout le potentiel d'Aspose.Words grâce à notre classe de licences. Gérez facilement vos licences pour un traitement fluide des documents et des fonctionnalités améliorées.
type: docs
weight: 3870
url: /fr/net/aspose.words/license/
---
## License class

Fournit des méthodes pour obtenir une licence pour le composant.

Pour en savoir plus, visitez le[Licences et abonnements](https://docs.aspose.com/words/net/licensing/) article de documentation.

```csharp
public class License
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [License](license/)() | Initialise une nouvelle instance de cette classe. |

## Méthodes

| Nom | La description |
| --- | --- |
| [SetLicense](../../aspose.words/license/setlicense/#setlicense)(*Stream*) | Licence le composant. |
| [SetLicense](../../aspose.words/license/setlicense/#setlicense_1)(*string*) | Licence le composant. |

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

* espace de noms [Aspose.Words](../../aspose.words/)
* Assemblée [Aspose.Words](../../)
