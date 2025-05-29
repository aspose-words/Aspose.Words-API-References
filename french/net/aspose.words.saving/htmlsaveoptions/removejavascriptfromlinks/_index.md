---
title: HtmlSaveOptions.RemoveJavaScriptFromLinks
linktitle: RemoveJavaScriptFromLinks
articleTitle: RemoveJavaScriptFromLinks
second_title: Aspose.Words pour .NET
description: Optimisez votre contenu Web avec HtmlSaveOptions pour supprimer facilement JavaScript des liens, améliorant ainsi les performances et l'expérience utilisateur.
type: docs
weight: 410
url: /fr/net/aspose.words.saving/htmlsaveoptions/removejavascriptfromlinks/
---
## HtmlSaveOptions.RemoveJavaScriptFromLinks property

Spécifie si JavaScript sera supprimé des liens. La valeur par défaut est`FAUX` .

```csharp
public bool RemoveJavaScriptFromLinks { get; set; }
```

## Remarques

Si cette option est activée, tous les liens contenant du JavaScript (par exemple, ceux dont l'attribut href contient « javascript: ») seront remplacés par « javascript:void(0) ». Cela permet d'éviter des risques de sécurité potentiels, comme les attaques XSS.

### Voir également

* class [HtmlSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
