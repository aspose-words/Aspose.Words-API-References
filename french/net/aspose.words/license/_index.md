---
title: Class License
second_title: Référence de l'API Aspose.Words pour .NET
description: Aspose.Words.License classe. Fournit des méthodes pour obtenir une licence pour le composant.
type: docs
weight: 3420
url: /fr/net/aspose.words/license/
---
## License class

Fournit des méthodes pour obtenir une licence pour le composant.

Pour en savoir plus, visitez le[Licence et abonnement](https://docs.aspose.com/words/net/licensing/) article documentaire.

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
| [SetLicense](../../aspose.words/license/setlicense/#setlicense)(Stream) | Licence pour le composant. |
| [SetLicense](../../aspose.words/license/setlicense/#setlicense_1)(string) | Licence pour le composant. |

### Exemples

Montre comment initialiser une licence pour Aspose.Words à l’aide d’un fichier de licence dans le système de fichiers local.

```csharp
// Définissez la licence de notre produit Aspose.Words en transmettant le nom de fichier du système de fichiers local d'un fichier de licence valide.
string licenseFileName = Path.Combine(LicenseDir, "Aspose.Words.NET.lic");

License license = new License();
license.SetLicense(licenseFileName);

// Créez une copie de notre fichier de licence dans le dossier binaires de notre application.
string licenseCopyFileName = Path.Combine(AssemblyDir, "Aspose.Words.NET.lic");
File.Copy(licenseFileName, licenseCopyFileName);

// Si on passe le nom d'un fichier sans chemin,
// SetLicense recherchera ce fichier dans plusieurs emplacements du système de fichiers local.
// L'un de ces emplacements sera le dossier "bin", qui contient une copie de notre fichier de licence.
license.SetLicense("Aspose.Words.NET.lic");
```

### Voir également

* espace de noms [Aspose.Words](../../aspose.words/)
* Assemblée [Aspose.Words](../../)


