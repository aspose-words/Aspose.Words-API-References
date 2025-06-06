---
title: MappedDataFieldCollection.ContainsKey
linktitle: ContainsKey
articleTitle: ContainsKey
second_title: Aspose.Words pour .NET
description: Découvrez si un mappage de champ de document spécifique existe dans MappedDataFieldCollection grâce à la méthode ContainsKey. Simplifiez la gestion des données !
type: docs
weight: 50
url: /fr/net/aspose.words.mailmerging/mappeddatafieldcollection/containskey/
---
## MappedDataFieldCollection.ContainsKey method

Détermine si un mappage du champ spécifié dans le document existe dans la collection.

```csharp
public bool ContainsKey(string documentFieldName)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| documentFieldName | String | Nom sensible à la casse du champ de publipostage dans le document. |

### Return_Value

`vrai`si l'élément est trouvé dans la collection ; sinon,`FAUX`.

## Exemples

Montre comment mapper des colonnes de données et des MERGEFIELD avec des noms différents afin que les données soient transférées entre eux lors d'un publipostage.

```csharp
public void MappedDataFieldCollection()
{
    Document doc = CreateSourceDocMappedDataFields();
    DataTable dataTable = CreateSourceTableMappedDataFields();

    // La table a une colonne nommée « Colonne2 », mais il n'y a pas de MERGEFIELD portant ce nom.
    // Nous avons également un MERGEFIELD nommé « Column3 », mais la source de données n'a pas de colonne portant ce nom.
    // Si les données de « Colonne 2 » conviennent au MERGEFIELD « Colonne 3 »,
    // nous pouvons mapper ce nom de colonne au MERGEFIELD dans la paire clé/valeur « MappedDataFields ».
    MappedDataFieldCollection mappedDataFields = doc.MailMerge.MappedDataFields;

    // Nous pouvons lier un nom de colonne de source de données à un nom MERGEFIELD comme celui-ci.
    mappedDataFields.Add("MergeFieldName", "DataSourceColumnName");

    // Liez la colonne de source de données nommée « Colonne2 » aux MERGEFIELD nommés « Colonne3 ».
    mappedDataFields.Add("Column3", "Column2");

    // Le nom MERGEFIELD est la « clé » du nom de colonne de source de données respectif « valeur ».
    Assert.AreEqual("DataSourceColumnName", mappedDataFields["MergeFieldName"]);
    Assert.True(mappedDataFields.ContainsKey("MergeFieldName"));
    Assert.True(mappedDataFields.ContainsValue("DataSourceColumnName"));

    // Maintenant, si nous exécutons cette fusion, les MERGEFIELD « Colonne 3 » prendront les données de la « Colonne 2 » de la table.
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
/// Créez un document avec 2 MERGEFIELD, dont l'un n'a pas de
/// colonne correspondante dans le tableau de données de la méthode ci-dessous.
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
/// Créez une table de données avec 2 colonnes, dont une sans
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

* class [MappedDataFieldCollection](../)
* espace de noms [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* Assemblée [Aspose.Words](../../../)
