---
title: FieldDatabase.InsertOnceOnMailMerge
linktitle: InsertOnceOnMailMerge
articleTitle: InsertOnceOnMailMerge
second_title: Aspose.Words pour .NET
description: Découvrez comment la propriété InsertOnceOnMailMerge dans FieldDatabase améliore la fusion de vos données en permettant une insertion transparente au début des fusions.
type: docs
weight: 70
url: /fr/net/aspose.words.fields/fielddatabase/insertonceonmailmerge/
---
## FieldDatabase.InsertOnceOnMailMerge property

Obtient ou définit s'il faut insérer des données au début d'une fusion.

```csharp
public bool InsertOnceOnMailMerge { get; set; }
```

## Exemples

Montre comment extraire des données d'une base de données et les insérer en tant que champ dans un document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Ce champ DATABASE exécutera une requête sur une base de données et affichera le résultat dans une table.
FieldDatabase field = (FieldDatabase)builder.InsertField(FieldType.FieldDatabase, true);
field.FileName = DatabaseDir + "Northwind.accdb";
field.Connection = "Provider=Microsoft.ACE.OLEDB.12.0";
field.Query = "SELECT * FROM [Products]";

Assert.AreEqual($" DATABASE  \\d {DatabaseDir.Replace("\\", "\\\\") + "Northwind.accdb"} \\c Provider=Microsoft.ACE.OLEDB.12.0 \\s \"SELECT * FROM [Products]\"", field.GetFieldCode());

// Insérez un autre champ de BASE DE DONNÉES avec une requête plus complexe qui trie tous les produits par ordre décroissant en fonction des ventes brutes.
field = (FieldDatabase)builder.InsertField(FieldType.FieldDatabase, true);
field.FileName = DatabaseDir + "Northwind.accdb";
field.Connection = "Provider=Microsoft.ACE.OLEDB.12.0";
field.Query =
    "SELECT [Products].ProductName, FORMAT(SUM([Order Details].UnitPrice * (1 - [Order Details].Discount) * [Order Details].Quantity), 'Currency') AS GrossSales " +
    "FROM([Products] " +
    "LEFT JOIN[Order Details] ON[Products].[ProductID] = [Order Details].[ProductID]) " +
    "GROUP BY[Products].ProductName " +
    "ORDER BY SUM([Order Details].UnitPrice* (1 - [Order Details].Discount) * [Order Details].Quantity) DESC";

// Ces propriétés ont la même fonction que les clauses LIMIT et TOP.
// Configurez-les pour afficher uniquement les lignes 1 à 10 du résultat de la requête dans la table du champ.
field.FirstRecord = "1";
field.LastRecord = "10";

// Cette propriété correspond à l'index du format que nous souhaitons utiliser pour notre tableau. La liste des formats de tableau se trouve dans le menu « Format automatique de tableau… ».
// qui apparaît lorsque nous créons un champ BASE DE DONNÉES dans Microsoft Word. L'index n° 10 correspond au format « Colorful 3 ».
field.TableFormat = "10";

// La propriété FormatAttribute est une représentation sous forme de chaîne d'un entier qui stocke plusieurs indicateurs.
// Nous pouvons appliquer partiellement le format vers lequel pointe la propriété TableFormat en définissant différents indicateurs dans cette propriété.
// Le nombre que nous utilisons est la somme d'une combinaison de valeurs correspondant à différents aspects du style du tableau.
// 63 représente 1 (bordures) + 2 (ombrage) + 4 (police) + 8 (couleur) + 16 (ajustement automatique) + 32 (lignes d'en-tête).
field.FormatAttributes = "63";
field.InsertHeadings = true;
field.InsertOnceOnMailMerge = true;

doc.FieldOptions.FieldDatabaseProvider = new OleDbFieldDatabaseProvider();
doc.UpdateFields();

doc.Save(ArtifactsDir + "Field.DATABASE.docx");
```

### Voir également

* class [FieldDatabase](../)
* espace de noms [Aspose.Words.Fields](../../../aspose.words.fields/)
* Assemblée [Aspose.Words](../../../)
