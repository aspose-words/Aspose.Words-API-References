---
title: MailMerge.Execute
linktitle: Execute
articleTitle: Execute
second_title: Aspose.Words pour .NET
description: Optimisez votre processus de mailing avec la méthode MailMerge Execute, en fusionnant sans effort les données provenant de sources personnalisées pour une communication personnalisée.
type: docs
weight: 180
url: /fr/net/aspose.words.mailmerging/mailmerge/execute/
---
## Execute(*[IMailMergeDataSource](../../imailmergedatasource/)*) {#execute}

Effectue un publipostage à partir d'une source de données personnalisée.

```csharp
public void Execute(IMailMergeDataSource dataSource)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| dataSource | IMailMergeDataSource | Un objet qui implémente l'interface de source de données de publipostage personnalisée. |

## Remarques

Utilisez cette méthode pour remplir les champs de publipostage du document avec des valeurs provenant de n'importe quelle source de données, telle qu'une liste, une table de hachage ou des objets. Vous devez écrire votre propre classe implémentant la méthode.[`IMailMergeDataSource`](../../imailmergedatasource/) interface.

Vous ne pouvez utiliser cette méthode que lorsque[`IsBidiTextSupportedOnUpdate`](../../../aspose.words.fields/fieldoptions/isbiditextsupportedonupdate/) est`FAUX`, c'est-à-dire que vous n'avez pas besoin de compatibilité avec les langues de droite à gauche (comme l'arabe ou l'hébreu).

Cette méthode ignore leRemoveUnusedRegions option.

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
/// Un exemple de classe « entité de données » dans votre application.
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
    /// Nom de la source de données. Utilisé par Aspose.Words uniquement lors d'un publipostage avec des régions répétables.
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
                // Renvoyer « false » au moteur de publipostage Aspose.Words pour signifier
                // que nous n'avons pas pu trouver de champ avec ce nom.
                fieldValue = null;
                return false;
        }
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

* interface [IMailMergeDataSource](../../imailmergedatasource/)
* class [MailMerge](../)
* espace de noms [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* Assemblée [Aspose.Words](../../../)

---

## Execute(*string[], object[]*) {#execute_5}

Effectue une opération de publipostage pour un seul enregistrement.

```csharp
public void Execute(string[] fieldNames, object[] values)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| fieldNames | String[] | Tableau de noms de champs de fusion. Les noms de champs ne sont pas sensibles à la casse. Si un nom de champ introuvable dans le document est rencontré, il est ignoré. |
| values | Object[] | Tableau de valeurs à insérer dans les champs de fusion. Le nombre d'éléments dans ce tableau doit être le même que le nombre d'éléments dans*fieldNames*. |

## Remarques

Utilisez cette méthode pour remplir les champs de publipostage du document avec des valeurs de un tableau d'objets.

Cette méthode fusionne les données d'un seul enregistrement. Le tableau de noms de champs (names ) et le tableau de valeurs représentent les données d'un seul enregistrement.

Cette méthode n'utilise pas de régions de publipostage.

Cette méthode ignore leRemoveUnusedRegions option.

## Exemples

Montre comment fusionner une image à partir d'un URI en tant que données de publipostage dans un MERGEFIELD.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Les MERGEFIELD avec les balises « Image : » recevront une image lors d'un publipostage.
// La chaîne après les deux points dans la balise « Image : » correspond à un nom de colonne
// dans la source de données dont les cellules contiennent les URI des fichiers image.
builder.InsertField("MERGEFIELD  Image:logo_FromWeb ");
builder.InsertField("MERGEFIELD  Image:logo_FromFileSystem ");

 // Créez une source de données contenant les URI des images que nous allons fusionner.
// Un URI peut être une URL Web qui pointe vers une image ou un nom de fichier de système de fichiers local d'un fichier image.
string[] columns = { "logo_FromWeb", "logo_FromFileSystem" };
object[] URIs = { ImageUrl, ImageDir + "Logo.jpg" };

// Exécuter un publipostage sur une source de données avec une seule ligne.
doc.MailMerge.Execute(columns, URIs);

doc.Save(ArtifactsDir + "MailMergeEvent.ImageFromUrl.docx");
```

Montre comment effectuer un publipostage, puis enregistrer le document dans le navigateur client.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertField(" MERGEFIELD FullName ");
builder.InsertParagraph();
builder.InsertField(" MERGEFIELD Company ");
builder.InsertParagraph();
builder.InsertField(" MERGEFIELD Address ");
builder.InsertParagraph();
builder.InsertField(" MERGEFIELD City ");

doc.MailMerge.Execute(new string[] { "FullName", "Company", "Address", "City" },
    new object[] { "James Bond", "MI5 Headquarters", "Milbank", "London" });

// Envoyer le document au navigateur client.
//Lancé car HttpResponse est nul dans le test.
Assert.Throws<ArgumentNullException>(() => doc.Save(response, "Artifacts/MailMerge.ExecuteArray.docx", ContentDisposition.Inline, null));

// Nous devrons fermer cette réponse manuellement pour nous assurer que nous n'ajoutons aucun contenu superflu au document après l'enregistrement.
Assert.Throws<NullReferenceException>(() => response.End());
```

### Voir également

* class [MailMerge](../)
* espace de noms [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* Assemblée [Aspose.Words](../../../)

---

## Execute(*DataTable*) {#execute_2}

Effectue un publipostage à partir d'un DataTable vers le document.

```csharp
public void Execute(DataTable table)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| table | DataTable | Tableau contenant des données à insérer dans les champs de publipostage. Les noms de champs ne sont pas sensibles à la casse. Si un nom de champ introuvable dans le document est rencontré, il est ignoré. |

## Remarques

Utilisez cette méthode pour remplir les champs de publipostage du document avec les valeurs de a **Table de données**.

Tous les enregistrements de la table sont fusionnés dans le document.

Vous pouvez utiliser le champ SUIVANT dans le document Word pour provoquer[`MailMerge`](../) objet pour sélectionner l'enregistrement suivant à partir de**Table de données** et continuer la fusion. Cela peut être utilisé lors de la création de documents tels que des étiquettes de publipostage.

Quand[`MailMerge`](../) l'objet atteint la fin du document principal et il y a encore more lignes dans le**Table de données**il copie l'intégralité du contenu du document principal et l'ajoute à la fin du document de destination en utilisant un saut de section comme séparateur.

Cette méthode ignore leRemoveUnusedRegions option.

## Exemples

Montre comment exécuter un publipostage avec des données provenant d'un DataTable.

```csharp
public void ExecuteDataTable()
{
    DataTable table = new DataTable("Test");
    table.Columns.Add("CustomerName");
    table.Columns.Add("Address");
    table.Rows.Add(new object[] { "Thomas Hardy", "120 Hanover Sq., London" });
    table.Rows.Add(new object[] { "Paolo Accorti", "Via Monte Bianco 34, Torino" });

    // Vous trouverez ci-dessous deux manières d'utiliser un DataTable comme source de données pour un publipostage.
    // 1 - Utilisez la table entière pour le publipostage afin de créer un document de publipostage de sortie pour chaque ligne de la table :
    Document doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.WholeTable.docx");

    // 2 - Utilisez une ligne du tableau pour créer un document de publipostage de sortie :
    doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table.Rows[1]);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.OneRow.docx");
}

/// <summary>
/// Crée un document source de publipostage.
/// </summary>
private static Document CreateSourceDocExecuteDataTable()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.InsertField(" MERGEFIELD CustomerName ");
    builder.InsertParagraph();
    builder.InsertField(" MERGEFIELD Address ");

    return doc;
}
```

### Voir également

* class [MailMerge](../)
* espace de noms [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* Assemblée [Aspose.Words](../../../)

---

## Execute(*IDataReader*) {#execute_4}

Effectue le publipostage à partir de**IDataReader** dans le document.

```csharp
public void Execute(IDataReader dataReader)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| dataReader | IDataReader | Source de données pour l'opération de publipostage. |

## Remarques

Tu peux passer**SqlDataReader** ou**Lecteur de données OleDb**objet dans la méthode this en tant que paramètre car ils ont tous deux été implémentés**IDataReader** interface.

Notez que cette méthode n'utilise pas de régions de fusion et de publipostage et que pour plusieurs enregistrements, le document the s'agrandira en répétant l'intégralité du document.

Cette méthode ignore leRemoveUnusedRegions option.

## Exemples

Montre comment exécuter un publipostage à l'aide de données provenant d'un lecteur de données.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Product:\t");
builder.InsertField(" MERGEFIELD ProductName");
builder.Write("\nSupplier:\t");
builder.InsertField(" MERGEFIELD CompanyName");
builder.Writeln();
builder.InsertField(" MERGEFIELD QuantityPerUnit");
builder.Write(" for $");
builder.InsertField(" MERGEFIELD UnitPrice");

// Créer une chaîne de connexion qui pointe vers le fichier de base de données « Northwind »
// dans notre système de fichiers local, ouvrez une connexion et configurez une requête SQL.
string connectionString = @"Provider = Microsoft.ACE.OLEDB.12.0; Data Source=" + DatabaseDir + "Northwind.accdb";
string query =
    @"SELECT Products.ProductName, Suppliers.CompanyName, Products.QuantityPerUnit, Products.UnitPrice
    FROM Products 
    INNER JOIN Suppliers 
    ON Products.SupplierID = Suppliers.SupplierID";

using (OleDbConnection connection = new OleDbConnection(connectionString))
{
    // Créez une commande SQL qui fournira des données pour notre publipostage.
    // Les noms des colonnes de la table que cette instruction SELECT renverra
    // devra correspondre aux champs de fusion que nous avons placés ci-dessus.
    OleDbCommand command = new OleDbCommand(query, connection);
    command.CommandText = query;
    try
    {
        connection.Open();
        using (OleDbDataReader reader = command.ExecuteReader())
        {
            // Prenez les données du lecteur et utilisez-les dans le publipostage.
            doc.MailMerge.Execute(reader);
        }
    }
    catch (Exception ex)
    {
        Console.WriteLine(ex.Message);
    }
}

doc.Save(ArtifactsDir + "MailMerge.ExecuteDataReader.docx");
```

### Voir également

* class [MailMerge](../)
* espace de noms [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* Assemblée [Aspose.Words](../../../)

---

## Execute(*DataView*) {#execute_3}

Effectue le publipostage à partir d'un**Vue des données** dans le document.

```csharp
public void Execute(DataView dataView)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| dataView | DataView | Source de données pour l'opération de publipostage. |

## Remarques

Cette méthode est utile si vous récupérez des données dans un**Table de données** mais alors il faut appliquer un filtre ou un tri avant le publipostage.

Notez que cette méthode n'utilise pas de régions de fusion et de publipostage et que pour plusieurs enregistrements, le document the s'agrandira en répétant l'intégralité du document.

Cette méthode ignore leRemoveUnusedRegions option.

## Exemples

Montre comment modifier les données de publipostage avec un DataView.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Congratulations ");
builder.InsertField(" MERGEFIELD Name");
builder.Write(" for passing with a grade of ");
builder.InsertField(" MERGEFIELD Grade");

// Créez une table de données à partir de laquelle notre publipostage s'approvisionnera en données.
DataTable table = new DataTable("ExamResults");
table.Columns.Add("Name");
table.Columns.Add("Grade");
table.Rows.Add(new object[] { "John Doe", "67" });
table.Rows.Add(new object[] { "Jane Doe", "81" });
table.Rows.Add(new object[] { "John Cardholder", "47" });
table.Rows.Add(new object[] { "Joe Bloggs", "75" });

// Nous pouvons utiliser une vue de données pour modifier les données de publipostage sans apporter de modifications à la table de données elle-même.
DataView view = new DataView(table);
view.Sort = "Grade DESC";
view.RowFilter = "Grade >= 50";

// Notre vue de données trie les entrées par ordre décroissant le long de la colonne « Note »
// et filtre les lignes avec des valeurs inférieures à 50 sur cette colonne.
// Trois des quatre lignes correspondent à ces critères, de sorte que le document de sortie contiendra trois documents de fusion.
doc.MailMerge.Execute(view);

doc.Save(ArtifactsDir + "MailMerge.ExecuteDataView.docx");
```

### Voir également

* class [MailMerge](../)
* espace de noms [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* Assemblée [Aspose.Words](../../../)

---

## Execute(*DataRow*) {#execute_1}

Effectue le publipostage à partir d'un**Ligne de données** dans le document.

```csharp
public void Execute(DataRow row)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| row | DataRow | Ligne contenant les données à insérer dans les champs de publipostage. Les noms de champs ne sont pas sensibles à la casse. Si un nom de champ introuvable dans le document est rencontré, il est ignoré. |

## Remarques

Utilisez cette méthode pour remplir les champs de publipostage du document avec des valeurs provenant d'un**Ligne de données**.

Cette méthode ignore leRemoveUnusedRegions option.

## Exemples

Montre comment exécuter un publipostage avec des données provenant d'un DataTable.

```csharp
public void ExecuteDataTable()
{
    DataTable table = new DataTable("Test");
    table.Columns.Add("CustomerName");
    table.Columns.Add("Address");
    table.Rows.Add(new object[] { "Thomas Hardy", "120 Hanover Sq., London" });
    table.Rows.Add(new object[] { "Paolo Accorti", "Via Monte Bianco 34, Torino" });

    // Vous trouverez ci-dessous deux manières d'utiliser un DataTable comme source de données pour un publipostage.
    // 1 - Utilisez la table entière pour le publipostage afin de créer un document de publipostage de sortie pour chaque ligne de la table :
    Document doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.WholeTable.docx");

    // 2 - Utilisez une ligne du tableau pour créer un document de publipostage de sortie :
    doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table.Rows[1]);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.OneRow.docx");
}

/// <summary>
/// Crée un document source de publipostage.
/// </summary>
private static Document CreateSourceDocExecuteDataTable()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.InsertField(" MERGEFIELD CustomerName ");
    builder.InsertParagraph();
    builder.InsertField(" MERGEFIELD Address ");

    return doc;
}
```

### Voir également

* class [MailMerge](../)
* espace de noms [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* Assemblée [Aspose.Words](../../../)
