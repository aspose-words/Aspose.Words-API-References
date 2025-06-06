---
title: License.SetLicense
linktitle: SetLicense
articleTitle: SetLicense
second_title: Aspose.Words pour .NET
description: Obtenez facilement des licences pour vos composants grâce à notre méthode SetLicense. Exploitez toutes les fonctionnalités et optimisez le potentiel de votre projet dès aujourd'hui !
type: docs
weight: 20
url: /fr/net/aspose.words/license/setlicense/
---
## SetLicense(*string*) {#setlicense_1}

Licence le composant.

```csharp
public void SetLicense(string licenseName)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| licenseName | String | Peut être un nom de fichier complet ou court ou le nom d'une ressource intégrée. Utilisez une chaîne vide pour passer en mode d'évaluation. |

## Remarques

Essaie de trouver la licence aux emplacements suivants :

1. Chemin explicite.

2. Le dossier contenant l’assemblage du composant Aspose.

3. Le dossier qui contient l'assembly appelant du client.

4. Le dossier qui contient l'assemblage d'entrée (démarrage).

5. Une ressource intégrée dans l'assembly appelant du client.

**Note:**Sur le .NET Compact Framework, essaie de trouver la licence uniquement à ces emplacements :

1. Chemin explicite.

2. Une ressource intégrée dans l'assembly appelant du client.

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

---

## SetLicense(*Stream*) {#setlicense}

Licence le composant.

```csharp
public void SetLicense(Stream stream)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| stream | Stream | Un flux qui contient la licence. |

## Remarques

Utilisez cette méthode pour charger une licence à partir d’un flux.

## Exemples

Montre comment initialiser une licence pour Aspose.Words à partir d'un flux.

```csharp
// Définissez la licence de notre produit Aspose.Words en transmettant un flux pour un fichier de licence valide dans notre système de fichiers local.
using (Stream myStream = File.OpenRead(Path.Combine(LicenseDir, "Aspose.Words.NET.lic")))
{
    License license = new License();
    license.SetLicense(myStream);
}
```

### Voir également

* class [License](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
