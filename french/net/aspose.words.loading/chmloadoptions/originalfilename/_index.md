---
title: ChmLoadOptions.OriginalFileName
second_title: Référence de l'API Aspose.Words pour .NET
description: ChmLoadOptions propriété. Le nom du fichier CHM. La valeur par défaut estnul .
type: docs
weight: 20
url: /fr/net/aspose.words.loading/chmloadoptions/originalfilename/
---
## ChmLoadOptions.OriginalFileName property

Le nom du fichier CHM. La valeur par défaut est`nul` .

```csharp
public string OriginalFileName { get; set; }
```

### Remarques

Les documents CHM peuvent contenir des liens qui font référence au même document par nom de fichier. Aspose.Words prend en charge ces links et utilise normalement[`OriginalFileName`](../../../aspose.words/document/originalfilename/) pour vérifier si le fichier référencé par un link est le fichier en cours de chargement. Si un document est chargé à partir d'un flux, son nom de fichier d'origine doit être spécifié explicitement via cette propriété, car il ne peut pas être déterminé automatiquement.

Si un document CHM est chargé à partir d'un fichier et qu'une valeur non nulle pour cette propriété est spécifiée, la valeur aura priorité sur le nom réel du fichier stocké dans[`OriginalFileName`](../../../aspose.words/document/originalfilename/) .

### Exemples

Montre comment résoudre des URL telles que « ms-its:myfile.chm::/index.htm ».

```csharp
// Notre document contient des URL du type "ms-its:amhelp.chm::....htm", mais il porte un nom différent,
// donc les liens de fichiers ne fonctionnent pas après l'avoir enregistré au format HTML.
// Nous devons définir le nom du fichier d'origine dans 'ChmLoadOptions' pour éviter ce comportement.
ChmLoadOptions loadOptions = new ChmLoadOptions { OriginalFileName = "amhelp.chm" };

Document doc = new Document(new MemoryStream(File.ReadAllBytes(MyDir + "Document with ms-its links.chm")),
    loadOptions);

doc.Save(ArtifactsDir + "ExChmLoadOptions.OriginalFileName.html");
```

### Voir également

* class [ChmLoadOptions](../)
* espace de noms [Aspose.Words.Loading](../../chmloadoptions/)
* Assemblée [Aspose.Words](../../../)


