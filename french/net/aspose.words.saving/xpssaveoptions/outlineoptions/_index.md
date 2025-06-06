---
title: XpsSaveOptions.OutlineOptions
linktitle: OutlineOptions
articleTitle: OutlineOptions
second_title: Aspose.Words pour .NET
description: Découvrez la propriété OutlineOptions de XpsSaveOptions pour personnaliser les paramètres de plan de votre document pour une organisation et une présentation améliorées.
type: docs
weight: 30
url: /fr/net/aspose.words.saving/xpssaveoptions/outlineoptions/
---
## XpsSaveOptions.OutlineOptions property

Permet de spécifier les options de contour.

```csharp
public OutlineOptions OutlineOptions { get; }
```

## Remarques

Noter que[`ExpandedOutlineLevels`](../../outlineoptions/expandedoutlinelevels/) l'option ne fonctionnera pas lors de l'enregistrement au format XPS.

## Exemples

Montre comment limiter le niveau des titres qui apparaîtront dans le plan d'un document XPS enregistré.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insérer des titres pouvant servir d'entrées de table des matières de niveaux 1, 2, puis 3.
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;

Assert.True(builder.ParagraphFormat.IsHeading);

builder.Writeln("Heading 1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;

builder.Writeln("Heading 1.1");
builder.Writeln("Heading 1.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading3;

builder.Writeln("Heading 1.2.1");
builder.Writeln("Heading 1.2.2");

// Créez un objet « XpsSaveOptions » que nous pouvons transmettre à la méthode « Save » du document
// pour modifier la façon dont cette méthode convertit le document en .XPS.
XpsSaveOptions saveOptions = new XpsSaveOptions();

Assert.AreEqual(SaveFormat.Xps, saveOptions.SaveFormat);

// Le document XPS de sortie contiendra un plan, une table des matières qui répertorie les titres dans le corps du document.
// Cliquer sur une entrée dans ce plan nous amènera à l'emplacement de son titre respectif.
// Définissez la propriété « HeadingsOutlineLevels » sur « 2 » pour exclure tous les titres dont les niveaux sont supérieurs à 2 du plan.
// Les deux derniers titres que nous avons insérés ci-dessus n'apparaîtront pas.
saveOptions.OutlineOptions.HeadingsOutlineLevels = 2;

doc.Save(ArtifactsDir + "XpsSaveOptions.OutlineLevels.xps", saveOptions);
```

### Voir également

* class [OutlineOptions](../../outlineoptions/)
* class [XpsSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
