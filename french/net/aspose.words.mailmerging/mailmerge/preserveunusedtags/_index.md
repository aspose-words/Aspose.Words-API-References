---
title: MailMerge.PreserveUnusedTags
linktitle: PreserveUnusedTags
articleTitle: PreserveUnusedTags
second_title: Aspose.Words pour .NET
description: MailMerge PreserveUnusedTags propriété. Obtient ou définit une valeur indiquant si les balises moustache inutilisées doivent être conservées en C#.
type: docs
weight: 80
url: /fr/net/aspose.words.mailmerging/mailmerge/preserveunusedtags/
---
## MailMerge.PreserveUnusedTags property

Obtient ou définit une valeur indiquant si les balises "moustache" inutilisées doivent être conservées.

```csharp
public bool PreserveUnusedTags { get; set; }
```

## Remarques

La valeur par défaut est`FAUX` .

## Exemples

Montre comment conserver l’apparence des balises de publipostage alternatives qui restent inutilisées lors d’un publipostage.

```csharp
public void PreserveUnusedTags(bool preserveUnusedTags)
{
    Document doc = CreateSourceDocWithAlternativeMergeFields();
    DataTable dataTable = CreateSourceTablePreserveUnusedTags();

     // Par défaut, un publipostage place les données de chaque ligne d'une table dans des MERGEFIELD, qui nomment les colonnes de cette table.
    // Notre document ne contient pas de tels champs, mais il contient des balises de texte en clair entourées d'accolades.
    // Si nous définissons le flag "PreserveUnusedTags" sur "true", nous pourrions traiter ces balises comme des MERGEFIELD
    // pour permettre à notre publipostage d'insérer des données de la source de données au niveau de ces balises.
    // Si on met le flag "PreserveUnusedTags" à "false",
    // le publipostage convertira ces balises en MERGEFIELD et les laissera vides.
    doc.MailMerge.PreserveUnusedTags = preserveUnusedTags;
    doc.MailMerge.Execute(dataTable);

    doc.Save(ArtifactsDir + "MailMerge.PreserveUnusedTags.docx");

    // Notre document possède une balise pour une colonne nommée "Colonne2", qui n'existe pas dans le tableau.
    // Si on met le flag "PreserveUnusedTags" à "false", then the mail merge will convert this tag into a MERGEFIELD.
    Assert.AreEqual(doc.GetText().Contains("{{ Column2 }}"), preserveUnusedTags);

    if (preserveUnusedTags)
        Assert.AreEqual(0, doc.Range.Fields.Count(f => f.Type == FieldType.FieldMergeField));
    else
        Assert.AreEqual(1, doc.Range.Fields.Count(f => f.Type == FieldType.FieldMergeField));
}

/// <summary>
/// Créez un document et ajoutez deux balises de texte en clair qui peuvent agir comme MERGEFIELD lors d'un publipostage.
/// </summary>
private static Document CreateSourceDocWithAlternativeMergeFields()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.Writeln("{{ Column1 }}");
    builder.Writeln("{{ Column2 }}");

    // Nos balises s'enregistreront en tant que destinations pour les données de publipostage uniquement si nous définissons cela sur true.
    doc.MailMerge.UseNonMergeFields = true;

    return doc;
}

/// <summary>
/// Créez un tableau de données simple avec une colonne.
/// </summary>
private static DataTable CreateSourceTablePreserveUnusedTags()
{
    DataTable dataTable = new DataTable("MyTable");
    dataTable.Columns.Add("Column1");
    dataTable.Rows.Add(new object[] { "Value1" });

    return dataTable;
}
```

### Voir également

* property [UseNonMergeFields](../usenonmergefields/)
* class [MailMerge](../)
* espace de noms [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* Assemblée [Aspose.Words](../../../)
