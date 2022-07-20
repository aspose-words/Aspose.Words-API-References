---
title: Execute
second_title: Référence de l'API Aspose.Words pour .NET
description: Effectue un publipostage à partir dune source de données personnalisée.
type: docs
weight: 180
url: /fr/net/aspose.words.mailmerging/mailmerge/execute/
---
## Execute(IMailMergeDataSource) {#execute}

Effectue un publipostage à partir d'une source de données personnalisée.

```csharp
public void Execute(IMailMergeDataSource dataSource)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| dataSource | IMailMergeDataSource | Objet qui implémente l'interface de source de données de publipostage personnalisée. |

### Remarques

Utilisez cette méthode pour remplir les champs de fusion et publipostage du document avec des valeurs de n'importe quelle source de données telle qu'une liste, une table de hachage ou des objets. Vous devez écrire votre propre classe qui implémente le[`IMailMergeDataSource`](../../imailmergedatasource) interface.

Vous ne pouvez utiliser cette méthode que lorsque[`IsBidiTextSupportedOnUpdate`](../../../aspose.words.fields/fieldoptions/isbiditextsupportedonupdate)est faux, c'est-à-dire que vous n'avez pas besoin de la compatibilité des langues de droite à gauche (comme l'arabe ou l'hébreu).

Cette méthode ignore lesRemoveUnusedRegions option.

### Voir également

* interface [IMailMergeDataSource](../../imailmergedatasource)
* class [MailMerge](../../mailmerge)
* espace de noms [Aspose.Words.MailMerging](../../mailmerge)
* Assemblée [Aspose.Words](../../../)

---

## Execute(string[], object[]) {#execute_5}

Effectue une opération de fusion et publipostage pour un seul enregistrement.

```csharp
public void Execute(string[] fieldNames, object[] values)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| fieldNames | String[] | Tableau de noms de champs de fusion. Les noms de champ ne sont pas sensibles à la casse. Si un nom de champ introuvable dans le document est rencontré, il est ignoré. |
| values | Object[] | Tableau de valeurs à insérer dans les champs de fusion. Le nombre d'éléments dans ce tableau doit être le même que le nombre d'éléments dans fieldNames. |

### Remarques

Utilisez cette méthode pour remplir les champs de fusion et publipostage du document avec des valeurs provenant de un tableau d'objets.

Cette méthode fusionne les données d'un seul enregistrement. Le tableau de noms de champs et le tableau de valeurs représentent les données d'un seul enregistrement.

Cette méthode n'utilise pas les régions de fusion et publipostage.

Cette méthode ignore lesRemoveUnusedRegions option.

### Exemples

Montre comment fusionner une image à partir d'un URI en tant que données de fusion et publipostage dans un MERGEFIELD.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Les CHAMPS DE FUSION avec des balises "Image :" recevront une image lors d'un publipostage.
// La chaîne après les deux-points dans la balise "Image :" correspond à un nom de colonne
// dans la source de données dont les cellules contiennent les URI des fichiers image.
builder.InsertField("MERGEFIELD  Image:logo_FromWeb ");
builder.InsertField("MERGEFIELD  Image:logo_FromFileSystem ");

 // Crée une source de données qui contient les URI des images que nous allons fusionner.
// Un URI peut être une URL Web qui pointe vers une image, ou un nom de fichier du système de fichiers local d'un fichier image.
string[] columns = { "logo_FromWeb", "logo_FromFileSystem" };
object[] URIs = { ImageUrl, ImageDir + "Logo.jpg" };

// Exécute un publipostage sur une source de données avec une ligne.
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

// Envoie le document au navigateur client.
Assert.That(() => doc.Save(response, "Artifacts/MailMerge.ExecuteArray.docx", ContentDisposition.Inline, null),
    Throws.TypeOf<ArgumentNullException>()); //Lancé car HttpResponse est nul dans le test.

// Nous devrons fermer cette réponse manuellement pour nous assurer de ne pas ajouter de contenu superflu au document après l'enregistrement.
Assert.That(() => response.End(), Throws.TypeOf<NullReferenceException>());
```

### Voir également

* class [MailMerge](../../mailmerge)
* espace de noms [Aspose.Words.MailMerging](../../mailmerge)
* Assemblée [Aspose.Words](../../../)

---

## Execute(DataTable) {#execute_2}

Effectue une fusion et publipostage à partir d'un DataTable dans le document.

```csharp
public void Execute(DataTable table)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| table | DataTable | Table qui contient des données à insérer dans les champs de fusion et publipostage. Les noms de champ ne sont pas sensibles à la casse. Si un nom de champ introuvable dans le document est rencontré, il est ignoré. |

### Remarques

Utilisez cette méthode pour remplir les champs de fusion et publipostage du document avec des valeurs de a  **Tableau de données**.

Tous les enregistrements de la table sont fusionnés dans le document.

Vous pouvez utiliser le champ NEXT dans le document Word pour provoquer **Publipostage** objet pour select enregistrement suivant de la **Tableau de données** et continuer la fusion. Cela peut être utilisé lors de la création de documents tels que des étiquettes de publipostage.

Lorsque **Publipostage**l'objet atteint la fin du document principal et il y a encore more lignes dans le **Tableau de données**, il copie tout le contenu de le document principal et l'ajoute à la fin du document de destination en utilisant une rupture section comme séparateur.

Cette méthode ignore lesRemoveUnusedRegions option.

### Exemples

Montre comment exécuter un publipostage avec les données d'un DataTable.

```csharp
public void ExecuteDataTable()
{
    DataTable table = new DataTable("Test");
    table.Columns.Add("CustomerName");
    table.Columns.Add("Address");
    table.Rows.Add(new object[] { "Thomas Hardy", "120 Hanover Sq., London" });
    table.Rows.Add(new object[] { "Paolo Accorti", "Via Monte Bianco 34, Torino" });

    // Vous trouverez ci-dessous deux manières d'utiliser un DataTable comme source de données pour un publipostage.
    // 1 - Utiliser le tableau entier pour le publipostage afin de créer un document de publipostage de sortie pour chaque ligne du tableau :
    Document doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.WholeTable.docx");

    // 2 - Utilisez une ligne du tableau pour créer un document de publipostage de sortie :
    doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table.Rows[1]);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.OneRow.docx");
}

/// <summary>
/// Crée un document source de fusion et publipostage.
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

* class [MailMerge](../../mailmerge)
* espace de noms [Aspose.Words.MailMerging](../../mailmerge)
* Assemblée [Aspose.Words](../../../)

---

## Execute(IDataReader) {#execute_4}

Effectue une fusion et publipostage depuis IDataReader dans le document.

```csharp
public void Execute(IDataReader dataReader)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| dataReader | IDataReader | Source de données pour l'opération de fusion et publipostage. |

### Remarques

Tu peux passer **SqlDataReader** ou **OleDbDataReader** objet dans la méthode this en tant que paramètre car ils ont tous deux implémenté **IDataReader** interface.

Notez que cette méthode n'utilise pas les régions de fusion et publipostage et pour plusieurs enregistrements, le document the augmentera en répétant l'intégralité du document.

Cette méthode ignore lesRemoveUnusedRegions option.

### Exemples

Montre comment exécuter un publipostage à l'aide des données d'un lecteur de données.

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

// Crée une chaîne de connexion qui pointe vers le fichier de base de données "Northwind"
// dans notre système de fichiers local, ouvrez une connexion et configurez une requête SQL.
string connectionString = @"Driver={Microsoft Access Driver (*.mdb)};Dbq=" + DatabaseDir + "Northwind.mdb";
string query = 
    @"SELECT Products.ProductName, Suppliers.CompanyName, Products.QuantityPerUnit, {fn ROUND(Products.UnitPrice,2)} as UnitPrice
    FROM Products 
    INNER JOIN Suppliers 
    ON Products.SupplierID = Suppliers.SupplierID";

using (OdbcConnection connection = new OdbcConnection())
{
    connection.ConnectionString = connectionString;
    connection.Open();

    // Créez une commande SQL qui fournira des données pour notre publipostage.
    // Les noms des colonnes de la table que cette instruction SELECT renverra
    // devra correspondre aux champs de fusion que nous avons placés ci-dessus.
    OdbcCommand command = connection.CreateCommand();
    command.CommandText = query;

    // Cela exécutera la commande et stockera les données dans le lecteur.
    OdbcDataReader reader = command.ExecuteReader(CommandBehavior.CloseConnection);

    // Prend les données du lecteur et les utilise dans le publipostage.
    doc.MailMerge.Execute(reader);
}

doc.Save(ArtifactsDir + "MailMerge.ExecuteDataReader.docx");
```

### Voir également

* class [MailMerge](../../mailmerge)
* espace de noms [Aspose.Words.MailMerging](../../mailmerge)
* Assemblée [Aspose.Words](../../../)

---

## Execute(DataView) {#execute_3}

Effectue un publipostage à partir d'un DataView dans le document.

```csharp
public void Execute(DataView dataView)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| dataView | DataView | Source de données pour l'opération de fusion et publipostage. |

### Remarques

Cette méthode est utile si vous récupérez des données dans un **Tableau de données** mais alors besoin d'appliquer un filtre ou un tri avant le publipostage.

Notez que cette méthode n'utilise pas les régions de fusion et publipostage et pour plusieurs enregistrements, le document the augmentera en répétant l'intégralité du document.

Cette méthode ignore lesRemoveUnusedRegions option.

### Exemples

Montre comment modifier les données de fusion et publipostage avec un DataView.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Congratulations ");
builder.InsertField(" MERGEFIELD Name");
builder.Write(" for passing with a grade of ");
builder.InsertField(" MERGEFIELD Grade");

// Crée une table de données à partir de laquelle notre fusion et publipostage puisera les données.
DataTable table = new DataTable("ExamResults");
table.Columns.Add("Name");
table.Columns.Add("Grade");
table.Rows.Add(new object[] { "John Doe", "67" });
table.Rows.Add(new object[] { "Jane Doe", "81" });
table.Rows.Add(new object[] { "John Cardholder", "47" });
table.Rows.Add(new object[] { "Joe Bloggs", "75" });

// Nous pouvons utiliser une vue de données pour modifier les données de fusion et publipostage sans apporter de modifications à la table de données elle-même.
DataView view = new DataView(table);
view.Sort = "Grade DESC";
view.RowFilter = "Grade >= 50";

// Notre vue de données trie les entrées par ordre décroissant le long de la colonne "Note"
// et filtre les lignes avec des valeurs inférieures à 50 sur cette colonne.
// Trois des quatre lignes correspondent à ces critères de sorte que le document de sortie contiendra trois documents de fusion.
doc.MailMerge.Execute(view);

doc.Save(ArtifactsDir + "MailMerge.ExecuteDataView.docx");
```

### Voir également

* class [MailMerge](../../mailmerge)
* espace de noms [Aspose.Words.MailMerging](../../mailmerge)
* Assemblée [Aspose.Words](../../../)

---

## Execute(DataRow) {#execute_1}

Effectue un publipostage à partir d'un DataRow dans le document.

```csharp
public void Execute(DataRow row)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| row | DataRow | Ligne contenant des données à insérer dans les champs de fusion et publipostage. Les noms de champ ne sont pas sensibles à la casse. Si un nom de champ introuvable dans le document est rencontré, il est ignoré. |

### Remarques

Utilisez cette méthode pour remplir les champs de fusion et publipostage du document avec des valeurs d'un **Ligne de données**.

Cette méthode ignore lesRemoveUnusedRegions option.

### Exemples

Montre comment exécuter un publipostage avec les données d'un DataTable.

```csharp
public void ExecuteDataTable()
{
    DataTable table = new DataTable("Test");
    table.Columns.Add("CustomerName");
    table.Columns.Add("Address");
    table.Rows.Add(new object[] { "Thomas Hardy", "120 Hanover Sq., London" });
    table.Rows.Add(new object[] { "Paolo Accorti", "Via Monte Bianco 34, Torino" });

    // Vous trouverez ci-dessous deux manières d'utiliser un DataTable comme source de données pour un publipostage.
    // 1 - Utiliser le tableau entier pour le publipostage afin de créer un document de publipostage de sortie pour chaque ligne du tableau :
    Document doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.WholeTable.docx");

    // 2 - Utilisez une ligne du tableau pour créer un document de publipostage de sortie :
    doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table.Rows[1]);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.OneRow.docx");
}

/// <summary>
/// Crée un document source de fusion et publipostage.
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

* class [MailMerge](../../mailmerge)
* espace de noms [Aspose.Words.MailMerging](../../mailmerge)
* Assemblée [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
