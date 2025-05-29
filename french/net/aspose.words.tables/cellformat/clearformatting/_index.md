---
title: CellFormat.ClearFormatting
linktitle: ClearFormatting
articleTitle: ClearFormatting
second_title: Aspose.Words pour .NET
description: Découvrez la méthode CellFormat ClearFormatting pour réinitialiser facilement les styles de cellule par défaut sans modifier leur largeur. Améliorez l'efficacité de votre tableur !
type: docs
weight: 160
url: /fr/net/aspose.words.tables/cellformat/clearformatting/
---
## CellFormat.ClearFormatting method

Rétablit la mise en forme par défaut de la cellule. Ne modifie pas la largeur de la cellule.

```csharp
public void ClearFormatting()
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

* class [CellFormat](../)
* espace de noms [Aspose.Words.Tables](../../../aspose.words.tables/)
* Assemblée [Aspose.Words](../../../)
