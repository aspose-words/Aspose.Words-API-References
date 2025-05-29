---
title: ChmLoadOptions
linktitle: ChmLoadOptions
articleTitle: ChmLoadOptions
second_title: Aspose.Words pour .NET
description: Découvrez le constructeur ChmLoadOptions pour une initialisation fluide. Définissez facilement des valeurs par défaut et améliorez les performances de votre application dès aujourd'hui !
type: docs
weight: 10
url: /fr/net/aspose.words.loading/chmloadoptions/chmloadoptions/
---
## ChmLoadOptions constructor

Initialise une nouvelle instance de cette classe avec les valeurs par défaut.

```csharp
public ChmLoadOptions()
```

## Exemples

Montre comment résoudre des URL telles que « ms-its:myfile.chm::/index.htm ».

```csharp
// Notre document contient des URL telles que « ms-its:amhelp.chm::....htm », mais il a un nom différent,
// donc les liens de fichiers ne fonctionnent pas après l'avoir enregistré au format HTML.
// Nous devons définir le nom de fichier d'origine dans 'ChmLoadOptions' pour éviter ce comportement.
ChmLoadOptions loadOptions = new ChmLoadOptions { OriginalFileName = "amhelp.chm" };

Document doc = new Document(new MemoryStream(File.ReadAllBytes(MyDir + "Document with ms-its links.chm")),
    loadOptions);

doc.Save(ArtifactsDir + "ExChmLoadOptions.OriginalFileName.html");
```

### Voir également

* class [ChmLoadOptions](../)
* espace de noms [Aspose.Words.Loading](../../../aspose.words.loading/)
* Assemblée [Aspose.Words](../../../)
