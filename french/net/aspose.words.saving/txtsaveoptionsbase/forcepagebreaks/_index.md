---
title: TxtSaveOptionsBase.ForcePageBreaks
linktitle: ForcePageBreaks
articleTitle: ForcePageBreaks
second_title: Aspose.Words pour .NET
description: TxtSaveOptionsBase ForcePageBreaks propriété. Permet de préciser si les sauts de page doivent être conservés lors de lexport en C#.
type: docs
weight: 30
url: /fr/net/aspose.words.saving/txtsaveoptionsbase/forcepagebreaks/
---
## TxtSaveOptionsBase.ForcePageBreaks property

Permet de préciser si les sauts de page doivent être conservés lors de l'export.

La valeur par défaut est`FAUX`.

```csharp
public bool ForcePageBreaks { get; set; }
```

## Remarques

La propriété affecte uniquement les sauts de page insérés explicitement dans un document. Il n'est pas lié aux sauts de page que MS Word insère automatiquement à la fin de chaque page.

## Exemples

Montre comment spécifier s’il faut conserver les sauts de page lors de l’exportation d’un document en texte brut.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Page 1");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 2");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 3");

// Crée un objet "TxtSaveOptions", que l'on peut passer au "Save" du document
// Méthode pour modifier la façon dont nous enregistrons le document en texte brut.
TxtSaveOptions saveOptions = new TxtSaveOptions();

// Les objets "Document" Aspose.Words ont des sauts de page, tout comme les documents Microsoft Word.
// Les formats de sauvegarde tels que ".txt" constituent un corps de texte continu sans sauts de page.
// Définissez la propriété "ForcePageBreaks" sur "true" pour conserver tous les sauts de page sous la forme de caractères '\f'.
// Définissez la propriété "ForcePageBreaks" sur "false" pour ignorer tous les sauts de page.
saveOptions.ForcePageBreaks = forcePageBreaks;

doc.Save(ArtifactsDir + "TxtSaveOptions.PageBreaks.txt", saveOptions);

// Si nous chargeons un document en texte brut avec des sauts de page,
// l'objet "Document" les utilisera pour diviser le corps en pages.
doc = new Document(ArtifactsDir + "TxtSaveOptions.PageBreaks.txt");

Assert.AreEqual(forcePageBreaks ? 3 : 1, doc.PageCount);
```

### Voir également

* class [TxtSaveOptionsBase](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
