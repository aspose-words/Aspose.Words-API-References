---
title: TextColumnCollection.Spacing
second_title: Référence de l'API Aspose.Words pour .NET
description: TextColumnCollection propriété. Lorsque les colonnes sont régulièrement espacées obtient ou définit la quantité despace entre chaque colonne en points.
type: docs
weight: 50
url: /fr/net/aspose.words/textcolumncollection/spacing/
---
## TextColumnCollection.Spacing property

Lorsque les colonnes sont régulièrement espacées, obtient ou définit la quantité d'espace entre chaque colonne en points.

```csharp
public double Spacing { get; set; }
```

### Remarques

N'a d'effet que lorsque[`EvenlySpaced`](../evenlyspaced/) est réglé sur **vrai** .

### Exemples

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
* espace de noms [Aspose.Words](../../textcolumncollection/)
* Assemblée [Aspose.Words](../../../)


