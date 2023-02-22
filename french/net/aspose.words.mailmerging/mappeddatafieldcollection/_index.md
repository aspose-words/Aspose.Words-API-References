---
title: Class MappedDataFieldCollection
second_title: Référence de l'API Aspose.Words pour .NET
description: Aspose.Words.MailMerging.MappedDataFieldCollection classe. Permet de mapper automatiquement les noms des champs de votre source de données et les noms des champs de fusion et publipostage du document.
type: docs
weight: 3650
url: /fr/net/aspose.words.mailmerging/mappeddatafieldcollection/
---
## MappedDataFieldCollection class

Permet de mapper automatiquement les noms des champs de votre source de données et les noms des champs de fusion et publipostage du document.

```csharp
public class MappedDataFieldCollection : IEnumerable<KeyValuePair<string, string>>
```

## Propriétés

| Nom | La description |
| --- | --- |
| [Count](../../aspose.words.mailmerging/mappeddatafieldcollection/count/) { get; } | Obtient le nombre d'éléments contenus dans la collection. |
| [Item](../../aspose.words.mailmerging/mappeddatafieldcollection/item/) { get; set; } | Obtient ou définit le nom du champ dans la source de données associée au champ de publipostage spécifié. |

## Méthodes

| Nom | La description |
| --- | --- |
| [Add](../../aspose.words.mailmerging/mappeddatafieldcollection/add/)(string, string) | Ajoute un nouveau mappage de champ. |
| [Clear](../../aspose.words.mailmerging/mappeddatafieldcollection/clear/)() | Supprime tous les éléments de la collection. |
| [ContainsKey](../../aspose.words.mailmerging/mappeddatafieldcollection/containskey/)(string) | Détermine si un mappage du champ spécifié dans le document existe dans la collection. |
| [ContainsValue](../../aspose.words.mailmerging/mappeddatafieldcollection/containsvalue/)(string) | Détermine si un mappage du champ spécifié dans la source de données existe dans la collection. |
| [GetEnumerator](../../aspose.words.mailmerging/mappeddatafieldcollection/getenumerator/)() | Renvoie un objet énumérateur de dictionnaire qui peut être utilisé pour itérer sur tous les éléments de la collection. |
| [Remove](../../aspose.words.mailmerging/mappeddatafieldcollection/remove/)(string) | Supprime un mappage de champ. |

### Remarques

Ceci est implémenté comme une collection de clés de chaîne dans des valeurs de chaîne. Les clés sont les noms des champs de fusion et publipostage dans le document et les values sont les noms des champs de votre source de données.

### Exemples

Montre comment mapper des colonnes de données et des MERGEFIELD avec des noms différents afin que les données soient transférées entre eux lors d'un publipostage.

```csharp
public void MappedDataFieldCollection()
{
    Document doc = CreateSourceDocMappedDataFields();
    DataTable dataTable = CreateSourceTableMappedDataFields();

    // La table a une colonne nommée "Column2", mais il n'y a pas de MERGEFIELD avec ce nom.
    // De plus, nous avons un MERGEFIELD nommé "Column3", mais la source de données n'a pas de colonne portant ce nom.
    // Si les données de "Column2" conviennent au MERGEFIELD "Column3",
    // nous pouvons mapper ce nom de colonne au MERGEFIELD dans la paire clé/valeur "MappedDataFields".
    MappedDataFieldCollection mappedDataFields = doc.MailMerge.MappedDataFields;

    // Nous pouvons lier un nom de colonne de source de données à un nom MERGEFIELD comme celui-ci.
    mappedDataFields.Add("MergeFieldName", "DataSourceColumnName");

    // Liez la colonne de la source de données nommée "Column2" aux MERGEFIELDs nommés "Column3".
    mappedDataFields.Add("Column3", "Column2");

    // Le nom MERGEFIELD est la "clé" du nom de colonne de source de données respectif "valeur".
    Assert.AreEqual("DataSourceColumnName", mappedDataFields["MergeFieldName"]);
    Assert.True(mappedDataFields.ContainsKey("MergeFieldName"));
    Assert.True(mappedDataFields.ContainsValue("DataSourceColumnName"));

    // Maintenant, si nous exécutons ce publipostage, les MERGEFIELD "Column3" prendront les données de "Column2" de la table.
    doc.MailMerge.Execute(dataTable);

    doc.Save(ArtifactsDir + "MailMerge.MappedDataFieldCollection.docx");

    // Nous pouvons parcourir les éléments de cette collection.
    Assert.AreEqual(2, mappedDataFields.Count);

    using (IEnumerator<KeyValuePair<string, string>> enumerator = mappedDataFields.GetEnumerator())
        while (enumerator.MoveNext())
            Console.WriteLine(
                $"Column named {enumerator.Current.Value} is mapped to MERGEFIELDs named {enumerator.Current.Key}");

    // Nous pouvons également supprimer des éléments de la collection.
    mappedDataFields.Remove("MergeFieldName");

    Assert.False(mappedDataFields.ContainsKey("MergeFieldName"));
    Assert.False(mappedDataFields.ContainsValue("DataSourceColumnName"));

    mappedDataFields.Clear();

    Assert.AreEqual(0, mappedDataFields.Count);
}

/// <summary>
/// Créer un document avec 2 MERGEFIELDs, dont l'un n'a pas de
/// colonne correspondante dans la table de données de la méthode ci-dessous.
/// </summary>
private static Document CreateSourceDocMappedDataFields()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.InsertField(" MERGEFIELD Column1");
    builder.Write(", ");
    builder.InsertField(" MERGEFIELD Column3");

    return doc;
}

/// <summary>
/// Créer un tableau de données avec 2 colonnes, dont une n'a pas de
/// MERGEFIELD correspondant dans le document source de la méthode ci-dessus.
/// </summary>
private static DataTable CreateSourceTableMappedDataFields()
{
    DataTable dataTable = new DataTable("MyTable");
    dataTable.Columns.Add("Column1");
    dataTable.Columns.Add("Column2");
    dataTable.Rows.Add(new object[] { "Value1", "Value2" });

    return dataTable;
}
```

### Voir également

* espace de noms [Aspose.Words.MailMerging](../../aspose.words.mailmerging/)
* Assemblée [Aspose.Words](../../)


