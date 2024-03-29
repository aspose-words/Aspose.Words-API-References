---
title: IMailMergeDataSource.TableName
linktitle: TableName
articleTitle: TableName
second_title: Aspose.Words pour .NET
description: IMailMergeDataSource TableName propriété. Renvoie le nom de la source de données en C#.
type: docs
weight: 10
url: /fr/net/aspose.words.mailmerging/imailmergedatasource/tablename/
---
## IMailMergeDataSource.TableName property

Renvoie le nom de la source de données.

```csharp
public string TableName { get; }
```

### Return_Value

Le nom de la source de données. Chaîne vide si la source de données n'a pas de nom.

## Remarques

Si vous mettez en œuvre[`IMailMergeDataSource`](../), renvoie le nom de la source data de cette propriété.

Aspose.Words utilise ce nom pour correspondre au nom de région de publipostage spécifié dans le document modèle. La comparaison entre le nom de la source de données et le nom de la région de publipostage n'est pas sensible à la casse.

## Exemples

Montre comment exécuter un publipostage avec une source de données sous la forme d'un objet personnalisé.

```csharp
public void CustomDataSource()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);
    builder.InsertField(" MERGEFIELD FullName ");
    builder.InsertParagraph();
    builder.InsertField(" MERGEFIELD Address ");

    List<Customer> customers = new List<Customer>
    {
        new Customer("Thomas Hardy", "120 Hanover Sq., London"),
        new Customer("Paolo Accorti", "Via Monte Bianco 34, Torino")
    };

     // Pour utiliser un objet personnalisé comme source de données, il doit implémenter l'interface IMailMergeDataSource.
    CustomerMailMergeDataSource dataSource = new CustomerMailMergeDataSource(customers);

    doc.MailMerge.Execute(dataSource);

    doc.Save(ArtifactsDir + "MailMergeCustom.CustomDataSource.docx");
}

/// <summary>
/// Un exemple de classe "entité de données" dans votre application.
/// </summary>
public class Customer
{
    public Customer(string aFullName, string anAddress)
    {
        FullName = aFullName;
        Address = anAddress;
    }

    public string FullName { get; set; }
    public string Address { get; set; }
}

/// <summary>
 /// Une source de données de publipostage personnalisée que vous implémentez pour autoriser Aspose.Words
/// pour fusionner les données de vos objets Client dans des documents Microsoft Word.
/// </summary>
public class CustomerMailMergeDataSource : IMailMergeDataSource
{
    public CustomerMailMergeDataSource(List<Customer> customers)
    {
        mCustomers = customers;

        // Lorsque nous initialisons la source de données, sa position doit être avant le premier enregistrement.
        mRecordIndex = -1;
    }

    /// <summary>
    /// Le nom de la source de données. Utilisé par Aspose.Words uniquement lors de l’exécution d’un publipostage avec des régions répétables.
    /// </summary>
    public string TableName
    {
        get { return "Customer"; }
    }

    /// <summary>
    /// Aspose.Words appelle cette méthode pour obtenir une valeur pour chaque champ de données.
    /// </summary>
    public bool GetValue(string fieldName, out object fieldValue)
    {
        switch (fieldName)
        {
            case "FullName":
                fieldValue = mCustomers[mRecordIndex].FullName;
                return true;
            case "Address":
                fieldValue = mCustomers[mRecordIndex].Address;
                return true;
            default:
                // Renvoie "false" au moteur de publipostage Aspose.Words pour signifier
                // que nous n'avons pas trouvé de champ portant ce nom.
                fieldValue = null;
                return false;
        }
    }

    /// <summary>
    /// Une implémentation standard pour passer à un enregistrement suivant dans une collection.
    /// </summary>
    public bool MoveNext()
    {
        if (!IsEof)
            mRecordIndex++;

        return !IsEof;
    }

    public IMailMergeDataSource GetChildDataSource(string tableName)
    {
        return null;
    }

    private bool IsEof
    {
        get { return (mRecordIndex >= mCustomers.Count); }
    }

    private readonly List<Customer> mCustomers;
    private int mRecordIndex;
}
```

### Voir également

* interface [IMailMergeDataSource](../)
* espace de noms [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* Assemblée [Aspose.Words](../../../)
