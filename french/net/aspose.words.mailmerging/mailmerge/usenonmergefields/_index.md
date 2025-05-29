---
title: MailMerge.UseNonMergeFields
linktitle: UseNonMergeFields
articleTitle: UseNonMergeFields
second_title: Aspose.Words pour .NET
description: Exploitez toute la puissance du publipostage ! Utilisez la propriété UseNonMergeFields pour enrichir vos documents en les fusionnant facilement avec différents types de champs.
type: docs
weight: 150
url: /fr/net/aspose.words.mailmerging/mailmerge/usenonmergefields/
---
## MailMerge.UseNonMergeFields property

Quand`vrai` , spécifie qu'en plus des champs MERGEFIELD, le publipostage est effectué dans certains autres types de champs et également dans les balises "{{fieldName}}".

```csharp
public bool UseNonMergeFields { get; set; }
```

## Remarques

Normalement, le publipostage s'effectue uniquement dans les champs MERGEFIELD, mais plusieurs clients ont créé leur reporting à partir d'autres champs et ont ainsi généré de nombreux documents. Afin de simplifier la migration (et parce que cette approche était utilisée indépendamment par plusieurs clients), la possibilité de fusionner avec d'autres champs a été introduite.

Quand`UseNonMergeFields` est réglé sur`vrai`Aspose.Words effectuera un publipostage dans les champs suivants :

MERGEFIELD Nom du champ

MACROBUTTON NOM MACRO Nom du champ

SI 0 = 0 "{FieldName}" ""

De plus, lorsque`UseNonMergeFields` est réglé sur`vrai`Aspose.Words effectuera un publipostage dans les balises texte "{{fieldName}}". Il ne s'agit pas de champs, mais simplement de balises texte.

## Exemples

Montre comment conserver l'apparence des balises de publipostage alternatives qui ne sont pas utilisées lors d'un publipostage.

```csharp
public void PreserveUnusedTags(bool preserveUnusedTags)
{
    Document doc = CreateSourceDocWithAlternativeMergeFields();
    DataTable dataTable = CreateSourceTablePreserveUnusedTags();

     // Par défaut, un publipostage place les données de chaque ligne d'une table dans des MERGEFIELD, qui nomment les colonnes de cette table.
    // Notre document ne contient pas de tels champs, mais il contient des balises de texte brut entourées d'accolades.
    // Si nous définissons l'indicateur « PreserveUnusedTags » sur « true », nous pourrions traiter ces balises comme des MERGEFIELD
    // pour permettre à notre publipostage d'insérer des données de la source de données à ces balises.
    // Si nous définissons l'indicateur « PreserveUnusedTags » sur « false »,
    // le publipostage convertira ces balises en MERGEFIELD et les laissera vides.
    doc.MailMerge.PreserveUnusedTags = preserveUnusedTags;
    doc.MailMerge.Execute(dataTable);

    doc.Save(ArtifactsDir + "MailMerge.PreserveUnusedTags.docx");

    // Notre document a une balise pour une colonne nommée « Colonne2 », qui n'existe pas dans la table.
    // Si nous définissons l'indicateur « PreserveUnusedTags » sur « false », then the mail merge will convert this tag into a MERGEFIELD.
    Assert.AreEqual(doc.GetText().Contains("{{ Column2 }}"), preserveUnusedTags);

    if (preserveUnusedTags)
        Assert.AreEqual(0, doc.Range.Fields.Count(f => f.Type == FieldType.FieldMergeField));
    else
        Assert.AreEqual(1, doc.Range.Fields.Count(f => f.Type == FieldType.FieldMergeField));
}

/// <summary>
/// Créez un document et ajoutez deux balises de texte brut qui peuvent agir comme MERGEFIELD lors d'un publipostage.
/// </summary>
private static Document CreateSourceDocWithAlternativeMergeFields()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.Writeln("{{ Column1 }}");
    builder.Writeln("{{ Column2 }}");

    // Nos balises seront enregistrées comme destinations pour les données de publipostage uniquement si nous définissons cette option sur true.
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

* class [MailMerge](../)
* espace de noms [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* Assemblée [Aspose.Words](../../../)
