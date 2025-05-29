---
title: DocumentBuilder.InsertStyleSeparator
linktitle: InsertStyleSeparator
articleTitle: InsertStyleSeparator
second_title: Aspose.Words pour .NET
description: Améliorez vos documents avec la méthode InsertStyleSeparator de DocumentBuilder, en ajoutant sans effort des séparateurs de style pour une mise en forme et une organisation améliorées.
type: docs
weight: 490
url: /fr/net/aspose.words/documentbuilder/insertstyleseparator/
---
## DocumentBuilder.InsertStyleSeparator method

Insère un séparateur de style dans le document.

```csharp
public void InsertStyleSeparator()
```

## Remarques

Cette méthode permet d'appliquer des styles de paragraphe différents à deux parties différentes d'une ligne de texte.

## Exemples

Montre comment travailler avec les séparateurs de style.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Chaque paragraphe ne peut avoir qu'un seul style.
// La méthode InsertStyleSeparator nous permet de contourner cette limitation.
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;
builder.Write("This text is in a Heading style. ");
builder.InsertStyleSeparator();

Style paraStyle = builder.Document.Styles.Add(StyleType.Paragraph, "MyParaStyle");
paraStyle.Font.Bold = false;
paraStyle.Font.Size = 8;
paraStyle.Font.Name = "Arial";

builder.ParagraphFormat.StyleName = paraStyle.Name;
builder.Write("This text is in a custom style. ");

// L'appel de la méthode InsertStyleSeparator crée un autre paragraphe,
// qui peut avoir un style différent du précédent. Il n'y aura pas de coupure entre les paragraphes.
// Le texte dans le document de sortie ressemblera à un paragraphe avec deux styles.
Assert.AreEqual(2, doc.FirstSection.Body.Paragraphs.Count);
Assert.AreEqual("Heading 1", doc.FirstSection.Body.Paragraphs[0].ParagraphFormat.Style.Name);
Assert.AreEqual("MyParaStyle", doc.FirstSection.Body.Paragraphs[1].ParagraphFormat.Style.Name);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertStyleSeparator.docx");
```

### Voir également

* class [DocumentBuilder](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
