---
title: HtmlSaveOptions.ReplaceBackslashWithYenSign
linktitle: ReplaceBackslashWithYenSign
articleTitle: ReplaceBackslashWithYenSign
second_title: Aspose.Words pour .NET
description: Découvrez comment la propriété HtmlSaveOptions ReplaceBackslashWithYenSign améliore votre sortie HTML en convertissant les barres obliques inverses en signes yen. Valeur par défaut  false.
type: docs
weight: 420
url: /fr/net/aspose.words.saving/htmlsaveoptions/replacebackslashwithyensign/
---
## HtmlSaveOptions.ReplaceBackslashWithYenSign property

Spécifie si les caractères de barre oblique inverse doivent être remplacés par des signes yen. La valeur par défaut est`FAUX` .

```csharp
public bool ReplaceBackslashWithYenSign { get; set; }
```

## Remarques

Par défaut, Aspose.Words imite le comportement de MS Word et ne remplace pas les barres obliques inverses par des signes yen dans les documents HTML générés. Cependant, les versions précédentes d'Aspose.Words effectuaient de tels remplacements dans certains cas. Cet indicateur assure la rétrocompatibilité avec les versions précédentes d'Aspose.Words.

## Exemples

Montre comment remplacer les caractères barre oblique inverse par des signes yen (Html).

```csharp
Document doc = new Document(MyDir + "Korean backslash symbol.docx");

// Par défaut, Aspose.Words imite le comportement de MS Word et ne remplace pas les barres obliques inverses par des signes yen dans
// documents HTML générés. Cependant, les versions précédentes d'Aspose.Words effectuaient de tels remplacements dans certains cas.
// scénarios. Cet indicateur permet la compatibilité descendante avec les versions précédentes d'Aspose.Words.
HtmlSaveOptions saveOptions = new HtmlSaveOptions();
saveOptions.ReplaceBackslashWithYenSign = true;

doc.Save(ArtifactsDir + "HtmlSaveOptions.ReplaceBackslashWithYenSign.html", saveOptions);
```

### Voir également

* class [HtmlSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
