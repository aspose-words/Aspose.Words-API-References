---
title: MailMerge.ExecuteWithRegions
second_title: Référence de l'API Aspose.Words pour .NET
description: MailMerge méthode. Effectue un publipostage à partir dune source de données personnalisée avec des régions de publipostage.
type: docs
weight: 200
url: /fr/net/aspose.words.mailmerging/mailmerge/executewithregions/
---
## ExecuteWithRegions(IMailMergeDataSource) {#executewithregions}

Effectue un publipostage à partir d'une source de données personnalisée avec des régions de publipostage.

```csharp
public void ExecuteWithRegions(IMailMergeDataSource dataSource)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| dataSource | IMailMergeDataSource | Objet qui implémente l'interface de source de données de publipostage personnalisée. |

### Remarques

Utilisez cette méthode pour remplir les champs de fusion et publipostage du document avec des valeurs de n'importe quelle source de données personnalisée telle qu'un fichier XML ou des collections d'objets métier. Vous devez écrire votre propre classe qui implémente le[`IMailMergeDataSource`](../../imailmergedatasource/) interface.

Vous ne pouvez utiliser cette méthode que lorsque[`IsBidiTextSupportedOnUpdate`](../../../aspose.words.fields/fieldoptions/isbiditextsupportedonupdate/)est faux, c'est-à-dire que vous n'avez pas besoin de la compatibilité des langues de droite à gauche (comme l'arabe ou l'hébreu).

### Exemples

Montre comment utiliser les régions de publipostage pour exécuter un publipostage imbriqué.

```csharp
public void CustomDataSource()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Normalement, les champs MERGEFIELD contiennent le nom d'une colonne d'une source de données de publipostage.
    // Au lieu de cela, nous pouvons utiliser les préfixes "TableStart :" et "TableEnd :" pour commencer/terminer une région de publipostage.
    // Chaque région appartiendra à une table dont le nom correspond à la chaîne immédiatement après les deux-points du préfixe.
    builder.InsertField(" MERGEFIELD TableStart:Customers");

    // Ces MERGEFIELDs sont à l'intérieur de la région de publipostage de la table "Clients".
    // Lorsque nous exécutons le publipostage, ce champ recevra les données des lignes d'une source de données nommée "Clients".
    builder.Write("Full name:\t");
    builder.InsertField(" MERGEFIELD FullName ");
    builder.Write("\nAddress:\t");
    builder.InsertField(" MERGEFIELD Address ");
    builder.Write("\nOrders:\n");

    // Crée une deuxième région de fusion et publipostage à l'intérieur de la région extérieure pour une source de données nommée "Orders".
    // Les entrées de données "Commandes" ont une relation plusieurs-à-un avec la source de données "Clients".
    builder.InsertField(" MERGEFIELD TableStart:Orders");

    builder.Write("\tItem name:\t");
    builder.InsertField(" MERGEFIELD Name ");
    builder.Write("\n\tQuantity:\t");
    builder.InsertField(" MERGEFIELD Quantity ");
    builder.InsertParagraph();

    builder.InsertField(" MERGEFIELD TableEnd:Orders");
    builder.InsertField(" MERGEFIELD TableEnd:Customers");

    // Créez des données associées avec des noms qui correspondent à ceux de nos régions de publipostage.
    CustomerList customers = new CustomerList();
    customers.Add(new Customer("Thomas Hardy", "120 Hanover Sq., London"));
    customers.Add(new Customer("Paolo Accorti", "Via Monte Bianco 34, Torino"));

    customers[0].Orders.Add(new Order("Rugby World Cup Cap", 2));
    customers[0].Orders.Add(new Order("Rugby World Cup Ball", 1));
    customers[1].Orders.Add(new Order("Rugby World Cup Guide", 1));

    // Pour effectuer un publipostage à partir de votre source de données, nous devons l'encapsuler dans un objet qui implémente l'interface IMailMergeDataSource.
    CustomerMailMergeDataSource customersDataSource = new CustomerMailMergeDataSource(customers);

    doc.MailMerge.ExecuteWithRegions(customersDataSource);

    doc.Save(ArtifactsDir + "NestedMailMergeCustom.CustomDataSource.docx");
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
        Orders = new List<Order>();
    }

    public string FullName { get; set; }
    public string Address { get; set; }
    public List<Order> Orders { get; set; }
}

/// <summary>
/// Un exemple de collection typée qui contient vos objets "data".
/// </summary>
public class CustomerList : ArrayList
{
    public new Customer this[int index]
    {
        get { return (Customer) base[index]; }
        set { base[index] = value; }
    }
}

/// <summary>
/// Un exemple de classe "entité de données" enfant dans votre application.
/// </summary>
public class Order
{
    public Order(string oName, int oQuantity)
    {
        Name = oName;
        Quantity = oQuantity;
    }

    public string Name { get; set; }
    public int Quantity { get; set; }
}

/// <summary>
/// Une source de données de publipostage personnalisée que vous implémentez pour autoriser Aspose.Words 
/// pour fusionner les données de vos objets Customer dans des documents Microsoft Word.
/// </summary>
public class CustomerMailMergeDataSource : IMailMergeDataSource
{
    public CustomerMailMergeDataSource(CustomerList customers)
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
        get { return "Customers"; }
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
            case "Order":
                fieldValue = mCustomers[mRecordIndex].Orders;
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
        switch (tableName)
        {
            // Obtient la source de données enfant, dont le nom correspond à la région de fusion et publipostage qui utilise ses colonnes.
            case "Orders":
                return new OrderMailMergeDataSource(mCustomers[mRecordIndex].Orders);
            default:
                return null;
        }
    }

    private bool IsEof
    {
        get { return (mRecordIndex >= mCustomers.Count); }
    }

    private readonly CustomerList mCustomers;
    private int mRecordIndex;
}

public class OrderMailMergeDataSource : IMailMergeDataSource
{
    public OrderMailMergeDataSource(List<Order> orders)
    {
        mOrders = orders;

        // Lorsque nous initialisons la source de données, sa position doit être avant le premier enregistrement.
        mRecordIndex = -1;
    }

    /// <summary>
    /// Le nom de la source de données. Utilisé par Aspose.Words uniquement lors de l'exécution d'un publipostage avec des régions répétables.
    /// </summary>
    public string TableName
    {
        get { return "Orders"; }
    }

    /// <summary>
    /// Aspose.Words appelle cette méthode pour obtenir une valeur pour chaque champ de données.
    /// </summary>
    public bool GetValue(string fieldName, out object fieldValue)
    {
        switch (fieldName)
        {
            case "Name":
                fieldValue = mOrders[mRecordIndex].Name;
                return true;
            case "Quantity":
                fieldValue = mOrders[mRecordIndex].Quantity;
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

    /// <summary>
    /// Renvoie null car nous n'avons aucun élément enfant pour ce type d'objet.
    /// </summary>
    public IMailMergeDataSource GetChildDataSource(string tableName)
    {
        return null;
    }

    private bool IsEof
    {
        get { return (mRecordIndex >= mOrders.Count); }
    }

    private readonly List<Order> mOrders;
    private int mRecordIndex;
}
```

### Voir également

* interface [IMailMergeDataSource](../../imailmergedatasource/)
* class [MailMerge](../)
* espace de noms [Aspose.Words.MailMerging](../../mailmerge/)
* Assemblée [Aspose.Words](../../../)

---

## ExecuteWithRegions(IMailMergeDataSourceRoot) {#executewithregions_1}

Effectue un publipostage à partir d'une source de données personnalisée avec des régions de publipostage.

```csharp
public void ExecuteWithRegions(IMailMergeDataSourceRoot dataSourceRoot)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| dataSourceRoot | IMailMergeDataSourceRoot | Objet qui implémente l'interface racine de la source de données de fusion et publipostage personnalisée. |

### Remarques

Utilisez cette méthode pour remplir les champs de fusion et publipostage du document avec des valeurs de n'importe quelle source de données personnalisée telle qu'un fichier XML ou des collections d'objets métier. Vous devez écrire vos propres classes qui implémentent le[`IMailMergeDataSourceRoot`](../../imailmergedatasourceroot/) et[`IMailMergeDataSource`](../../imailmergedatasource/) interfaces.

Vous ne pouvez utiliser cette méthode que lorsque[`IsBidiTextSupportedOnUpdate`](../../../aspose.words.fields/fieldoptions/isbiditextsupportedonupdate/)est faux, c'est-à-dire que vous n'avez pas besoin de la compatibilité des langues de droite à gauche (comme l'arabe ou l'hébreu).

### Exemples

Effectue un publipostage à partir d'une source de données personnalisée avec des données maître-détails.

```csharp
public void CustomDataSourceRoot()
{
    // Crée un document avec deux régions de publipostage nommées "Washington" et "Seattle".
    string[] mailMergeRegions = { "Vancouver", "Seattle" };
    Document doc = CreateSourceDocumentWithMailMergeRegions(mailMergeRegions);

    // Crée deux sources de données pour le publipostage.
    EmployeeList employeesWashingtonBranch = new EmployeeList();
    employeesWashingtonBranch.Add(new Employee("John Doe", "Sales"));
    employeesWashingtonBranch.Add(new Employee("Jane Doe", "Management"));

    EmployeeList employeesSeattleBranch = new EmployeeList();
    employeesSeattleBranch.Add(new Employee("John Cardholder", "Management"));
    employeesSeattleBranch.Add(new Employee("Joe Bloggs", "Sales"));

    // Enregistrez nos sources de données par leur nom dans une racine de source de données.
    // Si nous sommes sur le point d'utiliser cette racine de source de données dans un publipostage avec des régions,
    // le nom enregistré de chaque source doit correspondre au nom d'une région de fusion et publipostage existante dans le document source de fusion et publipostage.
    DataSourceRoot sourceRoot = new DataSourceRoot();
    sourceRoot.RegisterSource(mailMergeRegions[0], new EmployeeListMailMergeSource(employeesWashingtonBranch));
    sourceRoot.RegisterSource(mailMergeRegions[1], new EmployeeListMailMergeSource(employeesSeattleBranch));

    // Étant donné que nous avons des régions de fusion et publipostage consécutives, nous devrions normalement effectuer deux fusions et publipostage.
    // Cependant, une source de publipostage avec une racine de données peut remplir plusieurs régions
    // si la racine contient des tables avec des noms/noms de colonnes correspondants.
    doc.MailMerge.ExecuteWithRegions(sourceRoot);

    doc.Save(ArtifactsDir + "MailMergeCustom.CustomDataSourceRoot.docx");
}

/// <summary>
/// Crée un document qui contient des régions de publipostage consécutives, avec des noms désignés par le tableau d'entrée,
/// pour une table de données des employés.
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
/// Un exemple de classe "entité de données" dans votre application.
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
/// Un exemple de collection typée qui contient vos objets "data".
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
    /// Une implémentation standard pour passer à un enregistrement suivant dans une collection.
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
    /// Le nom de la source de données. Utilisé par Aspose.Words uniquement lors de l'exécution d'un publipostage avec des régions répétables.
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
                // Renvoie "false" au moteur de publipostage Aspose.Words pour signifier
                // que nous n'avons pas trouvé de champ portant ce nom.
                fieldValue = null;
                return false;
        }
    }

    /// <summary>
    /// Les sources de données enfants sont destinées aux publipostages imbriqués.
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

* interface [IMailMergeDataSourceRoot](../../imailmergedatasourceroot/)
* class [MailMerge](../)
* espace de noms [Aspose.Words.MailMerging](../../mailmerge/)
* Assemblée [Aspose.Words](../../../)

---

## ExecuteWithRegions(DataSet) {#executewithregions_2}

Effectue un publipostage à partir d'un DataSet dans un document avec des régions de publipostage.

```csharp
public void ExecuteWithRegions(DataSet dataSet)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| dataSet | DataSet | DataSet qui contient des données à insérer dans les champs de fusion et publipostage. |

### Remarques

Utilisez cette méthode pour effectuer une fusion et publipostage à partir d'une ou plusieurs tables dans des régions de fusion mail répétables dans le document. Les régions de fusion et publipostage à l'intérieur du document augmenteront dynamiquement pour accueillir les enregistrements dans les tables correspondantes.

Chaque table du DataSet doit avoir un nom.

Le document doit avoir des régions de fusion et publipostage définies avec des noms faisant référence aux tables dans le DataSet.

Pour spécifier une région de fusion et publipostage dans le document, vous devez insérer deux champs de fusion et publipostage pour marquer le début et la fin de la région de fusion et publipostage.

Tout le contenu du document qui est inclus dans une région de fusion et publipostage sera automatiquement répété pour chaque enregistrement dans le DataTable.

Pour marquer le début d'une région de fusion et publipostage, insérez un MERGEFIELD avec le nom TableStart:MyTable, où MyTable correspond à l'un des noms de table dans votre DataSet.

Pour marquer la fin de la région de fusion et publipostage, insérez un autre MERGEFIELD avec le nom TableEnd:MyTable.

Pour insérer un MERGEFIELD dans Word, utilisez la commande Insert/Field et sélectionnez MergeField puis tapez le nom du champ.

Les champs TableStart et TableEnd doivent se trouver dans la même section de votre document.

S'ils sont utilisés à l'intérieur d'un tableau, TableStart et TableEnd doivent se trouver dans la même ligne du tableau.

Les régions de fusion et publipostage d'un document doivent être bien formées (il doit toujours y avoir une paire de champs de fusion matching TableStart et TableEnd avec le même nom de table).

### Exemples

Montre comment exécuter un publipostage imbriqué avec deux régions de fusion et deux tables de données.

```csharp
[Test]
public void ExecuteWithRegionsNested()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Normalement, les champs MERGEFIELD contiennent le nom d'une colonne d'une source de données de publipostage.
    // Au lieu de cela, nous pouvons utiliser les préfixes "TableStart :" et "TableEnd :" pour commencer/terminer une région de publipostage.
    // Chaque région appartiendra à une table dont le nom correspond à la chaîne immédiatement après les deux-points du préfixe.
    builder.InsertField(" MERGEFIELD TableStart:Customers");

    // Ce MERGEFIELD se trouve à l'intérieur de la région de publipostage de la table "Clients".
    // Lorsque nous exécutons le publipostage, ce champ recevra les données des lignes d'une source de données nommée "Clients".
    builder.Write("Orders for ");
    builder.InsertField(" MERGEFIELD CustomerName");
    builder.Write(":");

    // Crée des en-têtes de colonne pour une table qui contiendra des valeurs d'une deuxième région interne.
    builder.StartTable();
    builder.InsertCell();
    builder.Write("Item");
    builder.InsertCell();
    builder.Write("Quantity");
    builder.EndRow();

    // Crée une deuxième région de fusion et publipostage à l'intérieur de la région externe pour une table nommée "Orders".
    // La table "Orders" a une relation plusieurs-à-un avec la table "Customers" sur la colonne "CustomerID".
    builder.InsertCell();
    builder.InsertField(" MERGEFIELD TableStart:Orders");
    builder.InsertField(" MERGEFIELD ItemName");
    builder.InsertCell();
    builder.InsertField(" MERGEFIELD Quantity");

    // Fin de la région intérieure, puis fin de la région extérieure. L'ouverture et la fermeture d'une région de publipostage doivent
    // arrive sur la même ligne d'une table.
    builder.InsertField(" MERGEFIELD TableEnd:Orders");
    builder.EndTable();

    builder.InsertField(" MERGEFIELD TableEnd:Customers");

    // Crée un jeu de données qui contient les deux tables avec les noms et relations requis.
    // Chaque document de fusion pour chaque ligne de la table "Clients" de la région de fusion externe effectuera son publipostage sur la table "Commandes".
    // Chaque document de fusion affichera toutes les lignes de cette dernière table dont les valeurs de la colonne "CustomerID" correspondent à la ligne actuelle de la table "Customers".
    DataSet customersAndOrders = CreateDataSet();
    doc.MailMerge.ExecuteWithRegions(customersAndOrders);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteWithRegionsNested.docx");
}

/// <summary>
/// Génère un ensemble de données contenant deux tables de données nommées "Customers" et "Orders", avec une relation un-à-plusieurs sur la colonne "CustomerID".
/// </summary>
private static DataSet CreateDataSet()
{
    DataTable tableCustomers = new DataTable("Customers");
    tableCustomers.Columns.Add("CustomerID");
    tableCustomers.Columns.Add("CustomerName");
    tableCustomers.Rows.Add(new object[] { 1, "John Doe" });
    tableCustomers.Rows.Add(new object[] { 2, "Jane Doe" });

    DataTable tableOrders = new DataTable("Orders");
    tableOrders.Columns.Add("CustomerID");
    tableOrders.Columns.Add("ItemName");
    tableOrders.Columns.Add("Quantity");
    tableOrders.Rows.Add(new object[] { 1, "Hawaiian", 2 });
    tableOrders.Rows.Add(new object[] { 2, "Pepperoni", 1 });
    tableOrders.Rows.Add(new object[] { 2, "Chicago", 1 });

    DataSet dataSet = new DataSet();
    dataSet.Tables.Add(tableCustomers);
    dataSet.Tables.Add(tableOrders);
    dataSet.Relations.Add(tableCustomers.Columns["CustomerID"], tableOrders.Columns["CustomerID"]);

    return dataSet;
}
```

### Voir également

* class [MailMerge](../)
* espace de noms [Aspose.Words.MailMerging](../../mailmerge/)
* Assemblée [Aspose.Words](../../../)

---

## ExecuteWithRegions(DataTable) {#executewithregions_3}

Effectue une fusion et publipostage à partir d'un DataTable dans le document avec des régions de fusion et publipostage.

```csharp
public void ExecuteWithRegions(DataTable dataTable)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| dataTable | DataTable | Source de données pour l'opération de fusion et publipostage. La table doit avoir son **Nom de la table** ensemble de propriétés. |

### Remarques

Le document doit avoir une région de fusion et publipostage définie avec un nom qui correspond à  **DataTable.TableName**.

S'il existe d'autres régions de fusion et publipostage définies dans le document, elles sont laissées intactes. Cela permet d'effectuer plusieurs opérations de fusion et publipostage.

### Exemples

Montre comment formater des cellules lors d'un publipostage.

```csharp
{
    Document doc = new Document(MyDir + "Mail merge destination - Northwind suppliers.docx");

    doc.MailMerge.FieldMergingCallback = new HandleMergeFieldAlternatingRows();

    DataTable dataTable = GetSuppliersDataTable();
    doc.MailMerge.ExecuteWithRegions(dataTable);

    doc.Save(ArtifactsDir + "MailMergeEvent.AlternatingRows.docx");

/// <summary>
/// Formate les lignes du tableau lors d'un publipostage pour alterner entre deux couleurs sur des lignes paires/impaires.
/// </summary>
private class HandleMergeFieldAlternatingRows : IFieldMergingCallback
{
    /// <summary>
    /// Appelé lorsqu'un publipostage fusionne des données dans un MERGEFIELD.
    /// </summary>
    void IFieldMergingCallback.FieldMerging(FieldMergingArgs args)
    {
        if (mBuilder == null)
            mBuilder = new DocumentBuilder(args.Document);

        // Ceci est vrai si nous sommes sur la première colonne, ce qui signifie que nous sommes passés à une nouvelle ligne.
        if (args.FieldName == "CompanyName")
        {
            Color rowColor = IsOdd(mRowIdx) ? Color.FromArgb(213, 227, 235) : Color.FromArgb(242, 242, 242);

            for (int colIdx = 0; colIdx < 4; colIdx++)
            {
                mBuilder.MoveToCell(0, mRowIdx, colIdx, 0);
                mBuilder.CellFormat.Shading.BackgroundPatternColor = rowColor;
            }

            mRowIdx++;
        }
    }

    void IFieldMergingCallback.ImageFieldMerging(ImageFieldMergingArgs args)
    {
        // Ne fais rien.
    }

    private DocumentBuilder mBuilder;
    private int mRowIdx;
}

/// <summary>
/// Fonction nécessaire pour le portage automatique Visual Basic qui renvoie la parité du nombre passé.
/// </summary>
private static bool IsOdd(int value)
{
    return (value / 2 * 2).Equals(value);
}

/// <summary>
/// Crée une source de données de publipostage.
/// </summary>
private static DataTable GetSuppliersDataTable()
{
    DataTable dataTable = new DataTable("Suppliers");
    dataTable.Columns.Add("CompanyName");
    dataTable.Columns.Add("ContactName");
    for (int i = 0; i < 10; i++)
    {
        DataRow datarow = dataTable.NewRow();
        dataTable.Rows.Add(datarow);
        datarow[0] = "Company " + i;
        datarow[1] = "Contact " + i;
    }

    return dataTable;
}
```

Montre comment utiliser des régions pour exécuter deux publipostages distincts dans un seul document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Si nous voulons effectuer deux publipostages consécutifs sur un document tout en prenant des données de deux tables
// liés les uns aux autres de quelque manière que ce soit, nous pouvons séparer les publipostages avec les régions.
// Normalement, les champs MERGEFIELD contiennent le nom d'une colonne d'une source de données de publipostage.
// Au lieu de cela, nous pouvons utiliser les préfixes "TableStart :" et "TableEnd :" pour commencer/terminer une région de publipostage.
// Chaque région appartiendra à une table dont le nom correspond à la chaîne immédiatement après les deux-points du préfixe.
// Ces régions sont séparées pour les données non liées, alors qu'elles peuvent être imbriquées pour les données hiérarchiques.
builder.Writeln("\tCities: ");
builder.InsertField(" MERGEFIELD TableStart:Cities");
builder.InsertField(" MERGEFIELD Name");
builder.InsertField(" MERGEFIELD TableEnd:Cities");
builder.InsertParagraph();

// Les deux champs MERGEFIELD font référence au même nom de colonne, mais les valeurs de chacun proviendront de tables de données différentes.
builder.Writeln("\tFruit: ");
builder.InsertField(" MERGEFIELD TableStart:Fruit");
builder.InsertField(" MERGEFIELD Name");
builder.InsertField(" MERGEFIELD TableEnd:Fruit");

// Crée deux tables de données non liées.
DataTable tableCities = new DataTable("Cities");
tableCities.Columns.Add("Name");
tableCities.Rows.Add(new object[] { "Washington" });
tableCities.Rows.Add(new object[] { "London" });
tableCities.Rows.Add(new object[] { "New York" });

DataTable tableFruit = new DataTable("Fruit");
tableFruit.Columns.Add("Name");
tableFruit.Rows.Add(new object[] { "Cherry" });
tableFruit.Rows.Add(new object[] { "Apple" });
tableFruit.Rows.Add(new object[] { "Watermelon" });
tableFruit.Rows.Add(new object[] { "Banana" });

// Nous devrons exécuter un publipostage par table. Le premier publipostage remplira les MERGEFIELDs
// dans la plage "Villes" en laissant les champs de la plage "Fruit" vides.
doc.MailMerge.ExecuteWithRegions(tableCities);

// Exécute une deuxième fusion pour la table "Fruit", tout en utilisant une vue de données
// pour trier les lignes par ordre croissant sur la colonne "Nom" avant la fusion.
DataView dv = new DataView(tableFruit);
dv.Sort = "Name ASC";
doc.MailMerge.ExecuteWithRegions(dv);

doc.Save(ArtifactsDir + "MailMerge.ExecuteWithRegionsConcurrent.docx");
```

### Voir également

* class [MailMerge](../)
* espace de noms [Aspose.Words.MailMerging](../../mailmerge/)
* Assemblée [Aspose.Words](../../../)

---

## ExecuteWithRegions(DataView) {#executewithregions_4}

Effectue un publipostage à partir d'un DataView dans le document avec des régions de publipostage.

```csharp
public void ExecuteWithRegions(DataView dataView)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| dataView | DataView | Source de données pour l'opération de fusion et publipostage. La table source du **Affichage des données** doit avoir son **Nom de la table** ensemble de propriétés. |

### Remarques

Cette méthode est utile si vous récupérez des données dans un **Tableau de données** mais alors besoin d'appliquer un filtre ou un tri avant le publipostage.

Le document doit avoir une région de fusion et publipostage définie avec un nom qui correspond à  **DataView.Table.TableName**.

S'il existe d'autres régions de fusion et publipostage définies dans le document, elles sont laissées intactes. Cela permet d'effectuer plusieurs opérations de fusion et publipostage.

### Exemples

Montre comment utiliser des régions pour exécuter deux publipostages distincts dans un seul document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Si nous voulons effectuer deux publipostages consécutifs sur un document tout en prenant des données de deux tables
// liés les uns aux autres de quelque manière que ce soit, nous pouvons séparer les publipostages avec les régions.
// Normalement, les champs MERGEFIELD contiennent le nom d'une colonne d'une source de données de publipostage.
// Au lieu de cela, nous pouvons utiliser les préfixes "TableStart :" et "TableEnd :" pour commencer/terminer une région de publipostage.
// Chaque région appartiendra à une table dont le nom correspond à la chaîne immédiatement après les deux-points du préfixe.
// Ces régions sont séparées pour les données non liées, alors qu'elles peuvent être imbriquées pour les données hiérarchiques.
builder.Writeln("\tCities: ");
builder.InsertField(" MERGEFIELD TableStart:Cities");
builder.InsertField(" MERGEFIELD Name");
builder.InsertField(" MERGEFIELD TableEnd:Cities");
builder.InsertParagraph();

// Les deux champs MERGEFIELD font référence au même nom de colonne, mais les valeurs de chacun proviendront de tables de données différentes.
builder.Writeln("\tFruit: ");
builder.InsertField(" MERGEFIELD TableStart:Fruit");
builder.InsertField(" MERGEFIELD Name");
builder.InsertField(" MERGEFIELD TableEnd:Fruit");

// Crée deux tables de données non liées.
DataTable tableCities = new DataTable("Cities");
tableCities.Columns.Add("Name");
tableCities.Rows.Add(new object[] { "Washington" });
tableCities.Rows.Add(new object[] { "London" });
tableCities.Rows.Add(new object[] { "New York" });

DataTable tableFruit = new DataTable("Fruit");
tableFruit.Columns.Add("Name");
tableFruit.Rows.Add(new object[] { "Cherry" });
tableFruit.Rows.Add(new object[] { "Apple" });
tableFruit.Rows.Add(new object[] { "Watermelon" });
tableFruit.Rows.Add(new object[] { "Banana" });

// Nous devrons exécuter un publipostage par table. Le premier publipostage remplira les MERGEFIELDs
// dans la plage "Villes" en laissant les champs de la plage "Fruit" vides.
doc.MailMerge.ExecuteWithRegions(tableCities);

// Exécute une deuxième fusion pour la table "Fruit", tout en utilisant une vue de données
// pour trier les lignes par ordre croissant sur la colonne "Nom" avant la fusion.
DataView dv = new DataView(tableFruit);
dv.Sort = "Name ASC";
doc.MailMerge.ExecuteWithRegions(dv);

doc.Save(ArtifactsDir + "MailMerge.ExecuteWithRegionsConcurrent.docx");
```

### Voir également

* class [MailMerge](../)
* espace de noms [Aspose.Words.MailMerging](../../mailmerge/)
* Assemblée [Aspose.Words](../../../)

---

## ExecuteWithRegions(IDataReader, string) {#executewithregions_5}

Effectue un publipostage depuis IDataReader dans le document avec les régions de publipostage.

```csharp
public void ExecuteWithRegions(IDataReader dataReader, string tableName)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| dataReader | IDataReader | Source des enregistrements de données pour le publipostage, tels que OleDbDataReader ou SqlDataReader. |
| tableName | String | Nom de la région de fusion et publipostage dans le document à remplir. |

### Remarques

Tu peux passer **SqlDataReader** ou **OleDbDataReader** objet dans la méthode this en tant que paramètre car ils ont tous deux implémenté **IDataReader** interface.

### Exemples

Montre comment insérer des images stockées dans un champ BLOB de base de données dans un rapport.

```csharp
public void ImageFromBlob()
{
    Document doc = new Document(MyDir + "Mail merge destination - Northwind employees.docx");

    doc.MailMerge.FieldMergingCallback = new HandleMergeImageFieldFromBlob();

    string connString = $"Provider=Microsoft.Jet.OLEDB.4.0;Data Source={DatabaseDir + "Northwind.mdb"};";
    string query = "SELECT FirstName, LastName, Title, Address, City, Region, Country, PhotoBLOB FROM Employees";

    using (OleDbConnection conn = new OleDbConnection(connString))
    {
        conn.Open();

        // Ouvre le lecteur de données, qui doit être dans un mode qui lit tous les enregistrements à la fois.
        OleDbCommand cmd = new OleDbCommand(query, conn);
        IDataReader dataReader = cmd.ExecuteReader();

        doc.MailMerge.ExecuteWithRegions(dataReader, "Employees");
    }

    doc.Save(ArtifactsDir + "MailMergeEvent.ImageFromBlob.docx");

private class HandleMergeImageFieldFromBlob : IFieldMergingCallback
{
    void IFieldMergingCallback.FieldMerging(FieldMergingArgs args)
    {
        // Ne fais rien.
    }

    /// <summary>
    /// Ceci est appelé lorsqu'un publipostage rencontre un MERGEFIELD dans le document avec une balise "Image :" dans son nom.
    /// </summary>
    void IFieldMergingCallback.ImageFieldMerging(ImageFieldMergingArgs e)
    {
        MemoryStream imageStream = new MemoryStream((byte[])e.FieldValue);
        e.ImageStream = imageStream;
    }
}
```

### Voir également

* class [MailMerge](../)
* espace de noms [Aspose.Words.MailMerging](../../mailmerge/)
* Assemblée [Aspose.Words](../../../)


