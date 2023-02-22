---
title: IMailMergeDataSource.GetChildDataSource
second_title: Référence de l'API Aspose.Words pour .NET
description: IMailMergeDataSource méthode. Le moteur de publipostage Aspose.Words appelle cette méthode lorsquil rencontre le début dune région de publipostage imbriquée.
type: docs
weight: 20
url: /fr/net/aspose.words.mailmerging/imailmergedatasource/getchilddatasource/
---
## IMailMergeDataSource.GetChildDataSource method

Le moteur de publipostage Aspose.Words appelle cette méthode lorsqu'il rencontre le début d'une région de publipostage imbriquée.

```csharp
public IMailMergeDataSource GetChildDataSource(string tableName)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| tableName | String | Le nom de la région de fusion et publipostage tel qu'il est spécifié dans le modèle de document. Insensible à la casse. |

### Return_Value

Un objet de source de données qui donnera accès aux enregistrements de données de la table spécifiée.

### Remarques

Lorsque les moteurs de publipostage Aspose.Words remplissent une région de publipostage avec des données et rencontrent le début d'une région de publipostage nested sous la forme de MERGEFIELD TableStart:TableName, il appelle`GetChildDataSource` sur l'objet source de données current . Votre implémentation doit renvoyer un nouvel objet de source de données qui donnera accès aux enregistrements child de l'enregistrement parent actuel. Aspose.Words utilisera la source de données renvoyée pour remplir la région de publipostage imbriquée.

Vous trouverez ci-dessous les règles que la mise en œuvre de`GetChildDataSource` doit suivre.

Si la table représentée par cet objet de source de données a une table enfant (détail) associée avec le nom spécifié, , votre implémentation doit alors renvoyer un nouveau[`IMailMergeDataSource`](../) objet qui fournira access aux enregistrements enfants de l'enregistrement actuel. Un exemple de ceci est la relation Orders / OrderDetails. Supposons que le courant[`IMailMergeDataSource`](../) object représente la table Commandes et possède un enregistrement de commande en cours. Ensuite, Aspose.Words rencontre "MERGEFIELD TableStart:OrderDetails" dans le document et appelle`GetChildDataSource` . Vous devez créer et retourner un[`IMailMergeDataSource`](../) objet qui permettra à Aspose.Words d'accéder à l'enregistrement OrderDetails pour la commande en cours.

Si cet objet de source de données n'a pas de relation avec la table avec le nom spécifié, alors vous devez return a[`IMailMergeDataSource`](../)objet qui donnera accès à tous les enregistrements de la table spécifiée.

Si une table portant le nom spécifié n'existe pas, votre implémentation doit renvoyer`nul` .

### Exemples

Montre comment exécuter un publipostage avec une source de données sous la forme d'un objet personnalisé.

```csharp
public void CustomDataSource()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);
    builder.InsertField(" MERGEFIELD FullName ");
    builder.InsertParagraph();
    builder.InsertField(" MERGEFIELD Address ");

    List<Customer> customers = new List<Customer>();
    customers.Add(new Customer("Thomas Hardy", "120 Hanover Sq., London"));
    customers.Add(new Customer("Paolo Accorti", "Via Monte Bianco 34, Torino"));

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
/// pour fusionner les données de vos objets Customer dans des documents Microsoft Word.
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
    /// Le nom de la source de données. Utilisé par Aspose.Words uniquement lors de l'exécution d'un publipostage avec des régions répétables.
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
* espace de noms [Aspose.Words.MailMerging](../../imailmergedatasource/)
* Assemblée [Aspose.Words](../../../)


