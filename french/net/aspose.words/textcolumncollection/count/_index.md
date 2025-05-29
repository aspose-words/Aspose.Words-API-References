---
title: TextColumnCollection.Count
linktitle: Count
articleTitle: Count
second_title: Aspose.Words pour .NET
description: Découvrez la propriété TextColumnCollection Count pour accéder facilement au nombre de colonnes dans la section de votre document pour un contrôle de mise en page amélioré.
type: docs
weight: 10
url: /fr/net/aspose.words/textcolumncollection/count/
---
## TextColumnCollection.Count property

Obtient le nombre de colonnes dans la section d'un document.

```csharp
public int Count { get; }
```

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
