---
title: IMailMergeDataSourceRoot.GetDataSource
linktitle: GetDataSource
articleTitle: GetDataSource
second_title: Aspose.Words pour .NET
description: Bénéficiez d'un publipostage fluide avec Aspose.Words ! Découvrez comment la méthode IMailMergeDataSourceRoot GetDataSource optimise l'automatisation de vos documents.
type: docs
weight: 10
url: /fr/net/aspose.words.mailmerging/imailmergedatasourceroot/getdatasource/
---
## IMailMergeDataSourceRoot.GetDataSource method

Le moteur de publipostage Aspose.Words appelle cette méthode lorsqu'il rencontre le début d'une région de publipostage de niveau supérieur.

```csharp
public IMailMergeDataSource GetDataSource(string tableName)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| tableName | String | Nom de la zone de publipostage tel que spécifié dans le modèle de document. Non sensible à la casse. |

### Return_Value

Un objet source de données qui fournira l’accès aux enregistrements de données de la table spécifiée.

## Remarques

Lorsque les moteurs de publipostage Aspose.Words remplissent un document avec des données et rencontrent MERGEFIELD TableStart:TableName, , ils appellent`GetDataSource` sur cet objet. Votre implémentation doit renvoyer un nouvel objet source de données. Aspose.Words utilisera la source de données renvoyée pour remplir la zone de publipostage.

Si une source de données (table) avec le nom spécifié n'existe pas, votre implémentation doit renvoyer`nul` .

## Exemples

Effectue un publipostage à partir d'une source de données personnalisée avec des données maître-détails.

```csharp
public void CustomDataSourceRoot()
{
    // Créez un document avec deux régions de publipostage nommées « Washington » et « Seattle ».
    string[] mailMergeRegions = { "Vancouver", "Seattle" };
    Document doc = CreateSourceDocumentWithMailMergeRegions(mailMergeRegions);

    // Créez deux sources de données pour le publipostage.
    EmployeeList employeesWashingtonBranch = new EmployeeList();
    employeesWashingtonBranch.Add(new Employee("John Doe", "Sales"));
    employeesWashingtonBranch.Add(new Employee("Jane Doe", "Management"));

    EmployeeList employeesSeattleBranch = new EmployeeList();
    employeesSeattleBranch.Add(new Employee("John Cardholder", "Management"));
    employeesSeattleBranch.Add(new Employee("Joe Bloggs", "Sales"));

    // Enregistrez nos sources de données par nom dans une racine de source de données.
    // Si nous sommes sur le point d'utiliser cette racine de source de données dans un publipostage avec des régions,
    // le nom enregistré de chaque source doit correspondre au nom d'une région de publipostage existante dans le document source de publipostage.
    DataSourceRoot sourceRoot = new DataSourceRoot();
    sourceRoot.RegisterSource(mailMergeRegions[0], new EmployeeListMailMergeSource(employeesWashingtonBranch));
    sourceRoot.RegisterSource(mailMergeRegions[1], new EmployeeListMailMergeSource(employeesSeattleBranch));

    // Étant donné que nous avons des régions de publipostage consécutives, nous devrions normalement effectuer deux publipostages.
    // Cependant, une source de publipostage avec une racine de données peut remplir plusieurs régions
    // si la racine contient des tables avec des noms/noms de colonnes correspondants.
    doc.MailMerge.ExecuteWithRegions(sourceRoot);

    doc.Save(ArtifactsDir + "MailMergeCustom.CustomDataSourceRoot.docx");
}

/// <summary>
/// Créez un document contenant des régions de publipostage consécutives, avec des noms désignés par le tableau d'entrée,
/// pour un tableau de données des employés.
/// </summary>
private static Document CreateSourceDocumentWithMailMergeRegions(string[] regions)
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    foreach (string s in regions)
    {
        builder.Writeln("\n" + s + " branch: ");
        builder.InsertField(" MERGEFIELD TableStart:" + s);
        builder.InsertField(" MERGEFIELD FullName");
        builder.Write(", ");
        builder.InsertField(" MERGEFIELD Department");
        builder.InsertField(" MERGEFIELD TableEnd:" + s);
    }

    return doc;
}

/// <summary>
/// Un exemple de classe « entité de données » dans votre application.
/// </summary>
private class Employee
{
    public Employee(string aFullName, string aDepartment)
    {
        FullName = aFullName;
        Department = aDepartment;
    }

    public string FullName { get; }
    public string Department { get; }
}

/// <summary>
/// Un exemple de collection typée qui contient vos objets « données ».
/// </summary>
private class EmployeeList : ArrayList
{
    public new Employee this[int index]
    {
        get { return (Employee)base[index]; }
        set { base[index] = value; }
    }
}

/// <summary>
/// Racine de la source de données qui peut être transmise directement dans un publipostage qui peut enregistrer et contenir de nombreuses sources de données enfants.
/// Ces sources doivent toutes implémenter IMailMergeDataSource, et sont enregistrées et différenciées par un nom
/// qui correspond à une région de publipostage qui lira les données respectives.
/// </summary>
private class DataSourceRoot : IMailMergeDataSourceRoot
{
    public IMailMergeDataSource GetDataSource(string tableName)
    {
        EmployeeListMailMergeSource source = mSources[tableName];
        source.Reset();
        return mSources[tableName];
    }

    public void RegisterSource(string sourceName, EmployeeListMailMergeSource source)
    {
        mSources.Add(sourceName, source);
    }

    private readonly Dictionary<string, EmployeeListMailMergeSource> mSources = new Dictionary<string, EmployeeListMailMergeSource>();
}

/// <summary>
/// Source de données de publipostage personnalisée.
/// </summary>
private class EmployeeListMailMergeSource : IMailMergeDataSource
{
    public EmployeeListMailMergeSource(EmployeeList employees)
    {
        mEmployees = employees;
        mRecordIndex = -1;
    }

    /// <summary>
    /// Une implémentation standard pour passer à l'enregistrement suivant dans une collection.
    /// </summary>
    public bool MoveNext()
    {
        if (!IsEof)
            mRecordIndex++;

        return !IsEof;
    }

    private bool IsEof
    {
        get { return (mRecordIndex >= mEmployees.Count); }
    }

    public void Reset()
    {
        mRecordIndex = -1;
    }

    /// <summary>
    /// Nom de la source de données. Utilisé par Aspose.Words uniquement lors d'un publipostage avec des régions répétables.
    /// </summary>
    public string TableName
    {
        get { return "Employees"; }
    }

    /// <summary>
    /// Aspose.Words appelle cette méthode pour obtenir une valeur pour chaque champ de données.
    /// </summary>
    public bool GetValue(string fieldName, out object fieldValue)
    {
        switch (fieldName)
        {
            case "FullName":
                fieldValue = mEmployees[mRecordIndex].FullName;
                return true;
            case "Department":
                fieldValue = mEmployees[mRecordIndex].Department;
                return true;
            default:
                // Renvoyer « false » au moteur de publipostage Aspose.Words pour signifier
                // que nous n'avons pas pu trouver de champ avec ce nom.
                fieldValue = null;
                return false;
        }
    }

    /// <summary>
    /// Les sources de données enfants sont destinées aux fusions de courrier imbriquées.
    /// </summary>
    public IMailMergeDataSource GetChildDataSource(string tableName)
    {
        throw new System.NotImplementedException();
    }

    private readonly EmployeeList mEmployees;
    private int mRecordIndex;
}
```

### Voir également

* interface [IMailMergeDataSource](../../imailmergedatasource/)
* interface [IMailMergeDataSourceRoot](../)
* espace de noms [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* Assemblée [Aspose.Words](../../../)
