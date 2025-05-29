---
title: FieldDatabase Class
linktitle: FieldDatabase
articleTitle: FieldDatabase
second_title: Aspose.Words pour .NET
description: Découvrez la classe Aspose.Words.Fields.FieldDatabase pour implémenter efficacement des champs DATABASE dans vos documents. Optimisez l'automatisation de vos documents dès aujourd'hui !
type: docs
weight: 2150
url: /fr/net/aspose.words.fields/fielddatabase/
---
## FieldDatabase class

Implémente le champ DATABASE.

Pour en savoir plus, visitez le[Travailler avec les champs](https://docs.aspose.com/words/net/working-with-fields/) article de documentation.

```csharp
public class FieldDatabase : Field
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [FieldDatabase](fielddatabase/)() | Default_Constructor |

## Propriétés

| Nom | La description |
| --- | --- |
| [Connection](../../aspose.words.fields/fielddatabase/connection/) { get; set; } | Obtient ou définit une connexion aux données. |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Obtient le texte qui représente le résultat du champ affiché. |
| [End](../../aspose.words.fields/field/end/) { get; } | Obtient le nœud qui représente la fin du champ. |
| [FileName](../../aspose.words.fields/fielddatabase/filename/) { get; set; } | Obtient ou définit le chemin complet et le nom du fichier de la base de données |
| [FirstRecord](../../aspose.words.fields/fielddatabase/firstrecord/) { get; set; } | Obtient ou définit le numéro d'enregistrement intégral du premier enregistrement de données à insérer. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Obtient un[`FieldFormat`](../fieldformat/)objet qui fournit un accès typé au formatage du champ. |
| [FormatAttributes](../../aspose.words.fields/fielddatabase/formatattributes/) { get; set; } | Obtient ou définit les attributs du format à appliquer à la table. |
| [InsertHeadings](../../aspose.words.fields/fielddatabase/insertheadings/) { get; set; } | Obtient ou définit s'il faut insérer les noms de champs de la base de données comme en-têtes de colonne dans la table résultante. |
| [InsertOnceOnMailMerge](../../aspose.words.fields/fielddatabase/insertonceonmailmerge/) { get; set; } | Obtient ou définit s'il faut insérer des données au début d'une fusion. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Obtient ou définit si le résultat actuel du champ n'est plus correct (obsolète) en raison d'autres modifications apportées au document. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Obtient ou définit si le champ est verrouillé (ne doit pas recalculer son résultat). |
| [LastRecord](../../aspose.words.fields/fielddatabase/lastrecord/) { get; set; } | Obtient ou définit le numéro d'enregistrement intégral du dernier enregistrement de données à insérer. |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Obtient ou définit le LCID du champ. |
| [Query](../../aspose.words.fields/fielddatabase/query/) { get; set; } | Obtient ou définit un ensemble d'instructions SQL qui interrogent la base de données. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Obtient ou définit le texte qui se trouve entre le séparateur de champ et la fin du champ. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Récupère le nœud représentant le séparateur de champ. Peut être`nul` . |
| [Start](../../aspose.words.fields/field/start/) { get; } | Obtient le nœud qui représente le début du champ. |
| [TableFormat](../../aspose.words.fields/fielddatabase/tableformat/) { get; set; } | Obtient ou définit le format à appliquer au résultat de la requête de base de données. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Obtient le type de champ Microsoft Word. |

## Méthodes

| Nom | La description |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Renvoie le texte entre le début du champ et le séparateur de champ (ou la fin du champ s'il n'y a pas de séparateur). Le code du champ et le résultat du champ des champs enfants sont inclus. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(*bool*) | Renvoie le texte entre le début du champ et le séparateur de champ (ou la fin du champ s'il n'y a pas de séparateur). |
| [Remove](../../aspose.words.fields/field/remove/)() | Supprime le champ du document. Renvoie un nœud immédiatement après le champ. Si la fin du champ est le dernier child de son nœud parent, renvoie son paragraphe parent. Si le champ est déjà supprimé, renvoie`nul` . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Effectue la dissociation du champ. |
| [Update](../../aspose.words.fields/field/update/)() | Effectue la mise à jour du champ. Lève une requête si le champ est déjà en cours de mise à jour. |
| [Update](../../aspose.words.fields/field/update/)(*bool*) | Effectue une mise à jour du champ. L'erreur est générée si le champ est déjà en cours de mise à jour. |

## Remarques

Insère les résultats d'une requête de base de données dans une table WordprocessingML.

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

* class [Field](../field/)
* espace de noms [Aspose.Words.Fields](../../aspose.words.fields/)
* Assemblée [Aspose.Words](../../)
