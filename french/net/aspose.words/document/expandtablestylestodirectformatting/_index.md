---
title: Document.ExpandTableStylesToDirectFormatting
linktitle: ExpandTableStylesToDirectFormatting
articleTitle: ExpandTableStylesToDirectFormatting
second_title: Aspose.Words pour .NET
description: Document ExpandTableStylesToDirectFormatting méthode. Convertit le formatage spécifié dans les styles de tableau en formatage direct sur les tableaux du document en C#.
type: docs
weight: 590
url: /fr/net/aspose.words/document/expandtablestylestodirectformatting/
---
## Document.ExpandTableStylesToDirectFormatting method

Convertit le formatage spécifié dans les styles de tableau en formatage direct sur les tableaux du document.

```csharp
public void ExpandTableStylesToDirectFormatting()
```

## Remarques

Cette méthode existe car cette version d'Aspose.Words ne fournit qu'une prise en charge limitée des styles de table (voir ci-dessous). Cette méthode peut être utile lorsque vous chargez un document DOCX ou WordprocessingML contenant des tableaux formatés avec des styles de tableau et que vous devez interroger le formatage des tableaux, cellules, paragraphes ou texte .

Cette version d'Aspose.Words offre une prise en charge limitée des styles de tableau comme suit :

* Les styles de tableau définis dans les documents DOCX ou WordprocessingML sont conservés en tant que tableaux styles lors de l'enregistrement du document au format DOCX ou WordprocessingML.
* Les styles de tableau définis dans les documents DOCX ou WordprocessingML sont automatiquement convertis en formatage direct sur les tableaux lors de l'enregistrement du document dans tout autre format, rendu ou impression.
* Les styles de tableau définis dans les documents DOC sont conservés en tant que styles de tableau lorsque enregistre le document au format DOC uniquement.

## Exemples

Montre comment appliquer les propriétés du style d’un tableau directement aux éléments du tableau.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Hello world!");
builder.EndTable();

TableStyle tableStyle = (TableStyle)doc.Styles.Add(StyleType.Table, "MyTableStyle1");
tableStyle.RowStripe = 3;
tableStyle.CellSpacing = 5;
tableStyle.Shading.BackgroundPatternColor = Color.AntiqueWhite;
tableStyle.Borders.Color = Color.Blue;
tableStyle.Borders.LineStyle = LineStyle.DotDash;

table.Style = tableStyle;

// Cette méthode concerne les propriétés de style de tableau telles que celles que nous avons définies ci-dessus.
doc.ExpandTableStylesToDirectFormatting();

doc.Save(ArtifactsDir + "Document.TableStyleToDirectFormatting.docx");
```

### Voir également

* class [Document](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
