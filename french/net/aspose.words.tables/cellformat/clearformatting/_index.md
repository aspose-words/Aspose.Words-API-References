---
title: CellFormat.ClearFormatting
linktitle: ClearFormatting
articleTitle: ClearFormatting
second_title: Aspose.Words pour .NET
description: CellFormat ClearFormatting méthode. Réinitialise le formatage de cellule par défaut. Ne modifie pas la largeur de la cellule en C#.
type: docs
weight: 150
url: /fr/net/aspose.words.tables/cellformat/clearformatting/
---
## CellFormat.ClearFormatting method

Réinitialise le formatage de cellule par défaut. Ne modifie pas la largeur de la cellule.

```csharp
public void ClearFormatting()
```

## Exemples

Montre comment combiner les lignes de deux tables en une seule.

```csharp
Document doc = new Document(MyDir + "Tables.docx");

// Vous trouverez ci-dessous deux manières d'obtenir un tableau à partir d'un document.
// 1 - Depuis la collection "Tables" d'un nœud Body :
Table firstTable = doc.FirstSection.Body.Tables[0];

// 2 - Utilisation de la méthode "GetChild" :
Table secondTable = (Table)doc.GetChild(NodeType.Table, 1, true);

// Ajoute toutes les lignes de la table actuelle à la suivante.
while (secondTable.HasChildNodes)
    firstTable.Rows.Add(secondTable.FirstRow);

// Supprime le conteneur de table vide.
secondTable.Remove();

doc.Save(ArtifactsDir + "Table.CombineTables.docx");
```

### Voir également

* class [CellFormat](../)
* espace de noms [Aspose.Words.Tables](../../../aspose.words.tables/)
* Assemblée [Aspose.Words](../../../)
