---
title: TextColumnCollection.SetCount
linktitle: SetCount
articleTitle: SetCount
second_title: Aspose.Words pour .NET
description: Optimisez votre mise en page avec la méthode TextColumnCollection SetCount, en organisant sans effort le texte dans le nombre de colonnes souhaité pour une meilleure lisibilité.
type: docs
weight: 70
url: /fr/net/aspose.words/textcolumncollection/setcount/
---
## TextColumnCollection.SetCount method

Organise le texte dans le nombre spécifié de colonnes de texte.

```csharp
public void SetCount(int newCount)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| newCount | Int32 | Le nombre de colonnes dans lesquelles le texte doit être organisé. |

## Remarques

Quand[`EvenlySpaced`](../evenlyspaced/) est`FAUX` et vous augmentez le nombre de colonnes, nouveau[`TextColumn`](../../textcolumn/) les objets sont créés avec une largeur et un espacement nuls. Vous devez définir la largeur et l'espacement des nouvelles colonnes.

## Exemples

Montre comment créer plusieurs colonnes régulièrement espacées dans une section.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

TextColumnCollection columns = builder.PageSetup.TextColumns;
columns.Spacing = 100;
columns.SetCount(2);

builder.Writeln("Column 1.");
builder.InsertBreak(BreakType.ColumnBreak);
builder.Writeln("Column 2.");

doc.Save(ArtifactsDir + "PageSetup.ColumnsSameWidth.docx");
```

### Voir également

* class [TextColumnCollection](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
