---
title: PageSetup.TextColumns
second_title: Référence de l'API Aspose.Words pour .NET
description: PageSetup propriété. Renvoie une collection qui représente lensemble des colonnes de texte.
type: docs
weight: 420
url: /fr/net/aspose.words/pagesetup/textcolumns/
---
## PageSetup.TextColumns property

Renvoie une collection qui représente l'ensemble des colonnes de texte.

```csharp
public TextColumnCollection TextColumns { get; }
```

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

* class [TextColumnCollection](../../textcolumncollection/)
* class [PageSetup](../)
* espace de noms [Aspose.Words](../../pagesetup/)
* Assemblée [Aspose.Words](../../../)


