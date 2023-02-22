---
title: MailMerge.ExecuteADO
second_title: Référence de l'API Aspose.Words pour .NET
description: MailMerge méthode. Effectue une fusion et publipostage à partir dun objet ADO Recordset dans le document.
type: docs
weight: 190
url: /fr/net/aspose.words.mailmerging/mailmerge/executeado/
---
## MailMerge.ExecuteADO method

Effectue une fusion et publipostage à partir d'un objet ADO Recordset dans le document.

```csharp
public void ExecuteADO(object recordset)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| recordset | Object | Jeu d'enregistrements ADO ou objet Record. |

### Remarques

Cette méthode est utile lorsque vous avez l'intention d'utiliser les classes Aspose.Words en tant qu'objets COM à partir de code non managé, comme une application créée à l'aide de ASP ou de Visual Basic 6.0.

Cette méthode ignore lesRemoveUnusedRegions option.

Pour plus d'informations, consultez la description de MailMerge.Execute(DataTable).

### Exemples

```csharp
[VBScript]

Dim RS
Set RS = CreateObject("ADODB.Recordset")
RS.Open _
    "SELECT TOP 50 * FROM Customers ORDER BY Country, CompanyName", _
    "Provider=Microsoft.Jet.OLEDB.4.0;Data Source=Northwind.mdb"

Dim License
Set License = CreateObject("Aspose.Words.License")
License.SetLicense "C:\MyPath\MyLicense.lic"

Dim Helper
Set Helper = CreateObject("Aspose.Words.ComHelper")
Dim Doc
Set Doc = Helper.Open("CustomerLabels.doc")

Doc.MailMerge.ExecuteADO RS
Doc.Save "C:\MyPath\CustomerLabels Out VBScript.doc"
```

Montre comment exécuter un publipostage avec les données d'un jeu de données ADO.

```csharp
public void ExecuteADO()
{
    Document doc = CreateSourceDocADOMailMerge();

    // Pour travailler avec les DataSets ADO, nous devrons ajouter une référence à la bibliothèque Microsoft ActiveX Data Objects,
    // qui est inclus dans la distribution .NET et stocké dans "adodb.dll".
    ADODB.Connection connection = new ADODB.Connection();

    // Crée une chaîne de connexion qui pointe vers le fichier de base de données "Northwind"
    // dans notre système de fichiers local et ouvrez une connexion.
    string connectionString = @"Provider=Microsoft.Jet.OLEDB.4.0;Data Source=" + DatabaseDir + "Northwind.mdb";
    connection.Open(connectionString);

    // Remplir notre DataSet en exécutant une commande SQL sur notre base de données.
    // Les noms des colonnes de la table résultat devront correspondre
    // aux valeurs des MERGEFIELDS qui accueilleront nos données.
    const string command = @"SELECT ProductName, QuantityPerUnit, UnitPrice FROM Products";

    ADODB.Recordset recordset = new ADODB.Recordset();
    recordset.Open(command, connection);

    // Exécute le publipostage et enregistre le document.
    doc.MailMerge.ExecuteADO(recordset);
    doc.Save(ArtifactsDir + "MailMerge.ExecuteADO.docx");
}

/// <summary>
/// Créez un document vierge et remplissez-le avec MERGEFIELDS qui acceptera les données lors de l'exécution d'un publipostage.
/// </summary>
private static Document CreateSourceDocADOMailMerge()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.Write("Product:\t");
    builder.InsertField(" MERGEFIELD ProductName");
    builder.Writeln();
    builder.InsertField(" MERGEFIELD QuantityPerUnit");
    builder.Write(" for $");
    builder.InsertField(" MERGEFIELD UnitPrice");

    return doc;
}
```

### Voir également

* class [MailMerge](../)
* espace de noms [Aspose.Words.MailMerging](../../mailmerge/)
* Assemblée [Aspose.Words](../../../)


