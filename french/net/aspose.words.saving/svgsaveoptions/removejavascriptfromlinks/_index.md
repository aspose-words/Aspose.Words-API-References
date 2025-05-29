---
title: SvgSaveOptions.RemoveJavaScriptFromLinks
linktitle: RemoveJavaScriptFromLinks
articleTitle: RemoveJavaScriptFromLinks
second_title: Aspose.Words pour .NET
description: Optimisez vos fichiers SVG avec SvgSaveOptions et supprimez facilement le JavaScript des liens pour un code plus propre. Améliorez les performances et la sécurité grâce à ce paramètre simple !
type: docs
weight: 60
url: /fr/net/aspose.words.saving/svgsaveoptions/removejavascriptfromlinks/
---
## SvgSaveOptions.RemoveJavaScriptFromLinks property

Spécifie si JavaScript sera supprimé des liens. La valeur par défaut est`FAUX` . Si cette option est activée, tous les liens contenant du JavaScript seront remplacés par « javascript:void(0) ».

```csharp
public bool RemoveJavaScriptFromLinks { get; set; }
```

## Exemples

Montre comment supprimer JavaScript des liens (svg).

```csharp
Document doc = new Document(MyDir + "JavaScript in HREF.docx");

SvgSaveOptions saveOptions = new SvgSaveOptions();
saveOptions.RemoveJavaScriptFromLinks = true;

doc.Save(ArtifactsDir + "SvgSaveOptions.RemoveJavaScriptFromLinksSvg.html", saveOptions);
```

### Voir également

* class [SvgSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
