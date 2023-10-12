---
title: DocSaveOptions.AlwaysCompressMetafiles
second_title: Référence de l'API Aspose.Words pour .NET
description: DocSaveOptions propriété. QuandFAUX  les petits métafichiers ne sont pas compressés pour des raisons de performances. La valeur par défaut estvrai  tous les métafichiers sont compressés quelle que soit leur taille.
type: docs
weight: 20
url: /fr/net/aspose.words.saving/docsaveoptions/alwayscompressmetafiles/
---
## DocSaveOptions.AlwaysCompressMetafiles property

Quand`FAUX` , les petits métafichiers ne sont pas compressés pour des raisons de performances. La valeur par défaut est`vrai` , tous les métafichiers sont compressés quelle que soit leur taille.

```csharp
public bool AlwaysCompressMetafiles { get; set; }
```

### Exemples

Montre comment modifier la compression des métafichiers dans un document lors de l'enregistrement.

```csharp
// Ouvrez un document contenant une formule Microsoft Equation 3.0.
Document doc = new Document(MyDir + "Microsoft equation object.docx");

// Lorsque nous enregistrons un document, les métafichiers plus petits ne sont pas compressés pour des raisons de performances.
// Nous pouvons définir un indicateur dans un objet SaveOptions pour compresser chaque métafichier lors de la sauvegarde.
// Certains éditeurs tels que LibreOffice ne peuvent pas lire les métafichiers non compressés.
DocSaveOptions saveOptions = new DocSaveOptions();
saveOptions.AlwaysCompressMetafiles = compressAllMetafiles;

doc.Save(ArtifactsDir + "DocSaveOptions.AlwaysCompressMetafiles.docx", saveOptions);

if (compressAllMetafiles)
    Assert.That(10000, Is.LessThan(new FileInfo(ArtifactsDir + "DocSaveOptions.AlwaysCompressMetafiles.docx").Length));
else
    Assert.That(30000, Is.AtLeast(new FileInfo(ArtifactsDir + "DocSaveOptions.AlwaysCompressMetafiles.docx").Length));
```

### Voir également

* class [DocSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../docsaveoptions/)
* Assemblée [Aspose.Words](../../../)


