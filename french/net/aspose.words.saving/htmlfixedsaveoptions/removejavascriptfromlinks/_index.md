---
title: HtmlFixedSaveOptions.RemoveJavaScriptFromLinks
linktitle: RemoveJavaScriptFromLinks
articleTitle: RemoveJavaScriptFromLinks
second_title: Aspose.Words pour .NET
description: Optimisez votre code HTML avec la fonctionnalité HtmlFixedSaveOptions RemoveJavaScriptFromLinks. Améliorez la sécurité en supprimant facilement le JavaScript des liens.
type: docs
weight: 140
url: /fr/net/aspose.words.saving/htmlfixedsaveoptions/removejavascriptfromlinks/
---
## HtmlFixedSaveOptions.RemoveJavaScriptFromLinks property

Spécifie si JavaScript sera supprimé des liens. La valeur par défaut est`FAUX` .

```csharp
public bool RemoveJavaScriptFromLinks { get; set; }
```

## Remarques

Si cette option est activée, tous les liens contenant du JavaScript (par exemple, ceux dont l'attribut href contient « javascript: ») seront remplacés par « javascript:void(0) ». Cela permet d'éviter des risques de sécurité potentiels, comme les attaques XSS.

## Exemples

Montre comment supprimer JavaScript des liens.

```csharp
Document doc = new Document(MyDir + "JavaScript in HREF.docx");

HtmlSaveOptions saveOptions = new HtmlSaveOptions();
saveOptions.RemoveJavaScriptFromLinks = true;

doc.Save(ArtifactsDir + "HtmlSaveOptions.RemoveJavaScriptFromLinks.html", saveOptions);
```

Montre comment supprimer JavaScript des liens pour les documents HTML fixes.

```csharp
Document doc = new Document(MyDir + "JavaScript in HREF.docx");

HtmlFixedSaveOptions saveOptions = new HtmlFixedSaveOptions();
saveOptions.RemoveJavaScriptFromLinks = true;

doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.RemoveJavaScriptFromLinks.html", saveOptions);
```

### Voir également

* class [HtmlFixedSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
