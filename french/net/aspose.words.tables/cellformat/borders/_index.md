---
title: CellFormat.Borders
linktitle: Borders
articleTitle: Borders
second_title: Aspose.Words pour .NET
description: Découvrez la propriété CellFormat Borders pour accéder et personnaliser les collections de bordures de cellules pour une conception et des fonctionnalités de feuille de calcul améliorées.
type: docs
weight: 10
url: /fr/net/aspose.words.tables/cellformat/borders/
---
## CellFormat.Borders property

Obtient la collection des bordures de la cellule.

```csharp
public BorderCollection Borders { get; }
```

## Exemples

Montre comment combiner les lignes de deux tables en une seule.

```csharp
Document doc = new Document(MyDir + "Tables.docx");

// Vous trouverez ci-dessous deux manières d’obtenir un tableau à partir d’un document.
// 1 - À partir de la collection « Tables » d'un nœud Body :
Table firstTable = doc.FirstSection.Body.Tables[0];

// 2 - Utilisation de la méthode « GetChild » :
Table secondTable = (Table)doc.GetChild(NodeType.Table, 1, true);

// Ajouter toutes les lignes de la table actuelle à la suivante.
while (secondTable.HasChildNodes)
    firstTable.Rows.Add(secondTable.FirstRow);

// Supprimez le conteneur de table vide.
secondTable.Remove();

doc.Save(ArtifactsDir + "Table.CombineTables.docx");
```

### Voir également

* class [BorderCollection](../../../aspose.words/bordercollection/)
* class [CellFormat](../)
* espace de noms [Aspose.Words.Tables](../../../aspose.words.tables/)
* Assemblée [Aspose.Words](../../../)
