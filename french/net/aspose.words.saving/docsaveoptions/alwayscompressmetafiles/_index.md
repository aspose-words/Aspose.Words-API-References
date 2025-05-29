---
title: DocSaveOptions.AlwaysCompressMetafiles
linktitle: AlwaysCompressMetafiles
articleTitle: AlwaysCompressMetafiles
second_title: Aspose.Words pour .NET
description: Optimisez la gestion de vos documents grâce à la propriété AlwaysCompressMetafiles. Améliorez vos performances en contrôlant la compression des métafichiers pour plus d'efficacité.
type: docs
weight: 20
url: /fr/net/aspose.words.saving/docsaveoptions/alwayscompressmetafiles/
---
## DocSaveOptions.AlwaysCompressMetafiles property

Quand`FAUX` , les petits métafichiers ne sont pas compressés pour des raisons de performances. La valeur par défaut est`vrai` , tous les métafichiers sont compressés quelle que soit leur taille.

```csharp
public bool AlwaysCompressMetafiles { get; set; }
```

## Exemples

Montre comment modifier la compression des métafichiers dans un document lors de l'enregistrement.

```csharp
// Ouvrez un document contenant une formule Microsoft Equation 3.0.
Document doc = new Document(MyDir + "Microsoft equation object.docx");

// Lorsque nous enregistrons un document, les métafichiers plus petits ne sont pas compressés pour des raisons de performances.
// Nous pouvons définir un indicateur dans un objet SaveOptions pour compresser chaque métafichier lors de l'enregistrement.
// Certains éditeurs tels que LibreOffice ne peuvent pas lire les métafichiers non compressés.
DocSaveOptions saveOptions = new DocSaveOptions();
saveOptions.AlwaysCompressMetafiles = compressAllMetafiles;

doc.Save(ArtifactsDir + "DocSaveOptions.AlwaysCompressMetafiles.docx", saveOptions);
```

### Voir également

* class [DocSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
