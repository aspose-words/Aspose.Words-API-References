---
title: MailMerge.ExecuteWithRegionsADO
linktitle: ExecuteWithRegionsADO
articleTitle: ExecuteWithRegionsADO
second_title: .NET için Aspose.Words
description: MailMerge ExecuteWithRegionsADO yöntemiyle belge oluşturmanızı kolaylaştırın. Kişiselleştirilmiş sonuçlar için ADO Kayıt Kümesi verilerini zahmetsizce birleştirin.
type: docs
weight: 210
url: /tr/net/aspose.words.mailmerging/mailmerge/executewithregionsado/
---
## MailMerge.ExecuteWithRegionsADO method

ADO Kayıt Kümesi nesnesinden belgeye posta birleştirme işlemini posta birleştirme bölgeleriyle gerçekleştirir.

```csharp
public void ExecuteWithRegionsADO(object recordset, string tableName)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| recordset | Object | ADO Kayıt Kümesi veya Kayıt nesnesi. |
| tableName | String | Doldurulacak belgedeki posta birleştirme bölgesinin adı. |

## Notlar

Bu yöntem, Aspose.Words sınıflarını, yönetilmeyen koddan (örneğin, ASP veya Visual Basic 6.0 kullanılarak oluşturulmuş bir uygulama) as COM nesneleri olarak kullanmayı planladığınızda yararlıdır.

Daha fazla bilgi için açıklamayı inceleyin[`ExecuteWithRegions`](../executewithregions/).

## Örnekler

```csharp
[VBScript]

Dim RS
Set RS = CreateObject("ADODB.Recordset")
RS.Open _
    "SELECT * FROM AsposeWordOrderDetails WHERE OrderId = 10444 ORDER BY ProductID", _
    "Provider=Microsoft.Jet.OLEDB.4.0;Data Source=Northwind.mdb"

Dim Helper
Set Helper = CreateObject("Aspose.Words.ComHelper")

Dim Doc
Set Doc = Helper.Open("Invoice.doc")

Doc.MailMerge.ExecuteWithRegionsADO RS, "OrderDetails"
Doc.Save "Invoice Out VBScript.doc"
```

ADO veri kümesinden derlenen verilerle birden fazla bölgeyle posta birleştirmenin nasıl çalıştırılacağını gösterir.

```csharp
public void ExecuteWithRegionsADO()
{
    Document doc = CreateSourceDocADOMailMergeWithRegions();

    // ADO DataSet'lerle çalışmak için Microsoft ActiveX Data Objects kitaplığına bir başvuru eklememiz gerekecek,
    // .NET dağıtımına dahil olan ve "adodb.dll" içinde saklanan.
    ADODB.Connection connection = new ADODB.Connection();

    // "Northwind" veritabanı dosyasına işaret eden bir bağlantı dizesi oluşturun
    // yerel dosya sistemimizde bir bağlantı açalım.
    string connectionString = @"Provider=Microsoft.ACE.OLEDB.12.0;Data Source=" + DatabaseDir + "Northwind.accdb";
    connection.Open(connectionString);

    // Veritabanımızda bir SQL komutu çalıştırarak DataSet'imizi dolduralım.
    // Sonuç tablosundaki sütunların adlarının eşleşmesi gerekecektir
    // Verilerimizi barındıracak MERGEFIELDS değerlerine.
    string command = "SELECT FirstName, LastName, City FROM Employees";

    ADODB.Recordset recordset = new ADODB.Recordset();
    recordset.Open(command, connection);

    // Sadece ilk bölgede bir posta birleştirme çalıştır ve MERGEFIELDS'ını kayıt kümesindeki verilerle doldur.
    doc.MailMerge.ExecuteWithRegionsADO(recordset, "MergeRegion1");

    // Kayıt kümesini kapatın ve başka bir SQL sorgusundan gelen verilerle yeniden açın.
    command = "SELECT * FROM Customers";

    recordset.Close();
    recordset.Open(command, connection);

    // İkinci bölgede ikinci bir posta birleştirme işlemi gerçekleştirin ve belgeyi kaydedin.
    doc.MailMerge.ExecuteWithRegionsADO(recordset, "MergeRegion2");

    doc.Save(ArtifactsDir + "MailMerge.ExecuteWithRegionsADO.docx");

}

/// <summary>
/// İki birleştirme bölgesi olan bir belge oluşturun.
/// </summary>
private static Document CreateSourceDocADOMailMergeWithRegions()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.Writeln("\tEmployees: ");
    builder.InsertField(" MERGEFIELD TableStart:MergeRegion1");
    builder.InsertField(" MERGEFIELD FirstName");
    builder.Write(", ");
    builder.InsertField(" MERGEFIELD LastName");
    builder.Write(", ");
    builder.InsertField(" MERGEFIELD City");
    builder.InsertField(" MERGEFIELD TableEnd:MergeRegion1");
    builder.InsertParagraph();

    builder.Writeln("\tCustomers: ");
    builder.InsertField(" MERGEFIELD TableStart:MergeRegion2");
    builder.InsertField(" MERGEFIELD ContactName");
    builder.Write(", ");
    builder.InsertField(" MERGEFIELD Address");
    builder.Write(", ");
    builder.InsertField(" MERGEFIELD City");
    builder.InsertField(" MERGEFIELD TableEnd:MergeRegion2");

    return doc;
}
```

### Ayrıca bakınız

* class [MailMerge](../)
* ad alanı [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* toplantı [Aspose.Words](../../../)
