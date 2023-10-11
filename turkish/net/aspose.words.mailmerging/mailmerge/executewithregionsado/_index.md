---
title: MailMerge.ExecuteWithRegionsADO
second_title: Aspose.Words for .NET API Referansı
description: MailMerge yöntem. Bir ADO Recordset nesnesinden adresmektup birleştirme bölgelerine sahip belgeye adresmektup birleştirme gerçekleştirir.
type: docs
weight: 210
url: /tr/net/aspose.words.mailmerging/mailmerge/executewithregionsado/
---
## MailMerge.ExecuteWithRegionsADO method

Bir ADO Recordset nesnesinden adres-mektup birleştirme bölgelerine sahip belgeye adres-mektup birleştirme gerçekleştirir.

```csharp
public void ExecuteWithRegionsADO(object recordset, string tableName)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| recordset | Object | ADO Kayıt Kümesi veya Kayıt nesnesi. |
| tableName | String | Doldurulacak belgedeki adres-mektup birleştirme bölgesinin adı. |

### Notlar

Bu yöntem, Aspose.Words sınıflarını as COM nesnelerini, örneğin ASP veya Visual Basic 6.0 kullanılarak oluşturulan bir uygulama gibi yönetilmeyen koddan kullanmayı planladığınızda kullanışlıdır.

Daha fazla bilgi için açıklamasına bakın[`ExecuteWithRegions`](../executewithregions/).

### Örnekler

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

Bir ADO veri kümesindeki verilerle derlenen, birden çok bölgeyle adres-mektup birleştirmenin nasıl çalıştırılacağını gösterir.

```csharp
public void ExecuteWithRegionsADO()
{
    Document doc = CreateSourceDocADOMailMergeWithRegions();

    // ADO DataSets ile çalışmak için Microsoft ActiveX Data Objects kütüphanesine bir referans eklememiz gerekecek,
    // .NET dağıtımına dahil edilir ve "adodb.dll" dosyasında saklanır.
    ADODB.Connection connection = new ADODB.Connection();

    // "Northwind" veritabanı dosyasına işaret eden bir bağlantı dizesi oluşturun
    // yerel dosya sistemimizde bir bağlantı açın.
    string connectionString = @"Provider=Microsoft.ACE.OLEDB.12.0;Data Source=" + DatabaseDir + "Northwind.accdb";
    connection.Open(connectionString);

    // Veritabanımız üzerinde bir SQL komutu çalıştırarak DataSet'imizi dolduruyoruz.
    // Sonuç tablosundaki sütunların adlarının eşleşmesi gerekecek
    // MERGEFIELDS'in verilerimizi barındıracak değerlerine.
    string command = "SELECT FirstName, LastName, City FROM Employees";

    ADODB.Recordset recordset = new ADODB.Recordset();
    recordset.Open(command, connection);

    // MERGEFIELDS'i kayıt kümesindeki verilerle doldurarak yalnızca ilk bölgede adres-mektup birleştirme çalıştırın.
    doc.MailMerge.ExecuteWithRegionsADO(recordset, "MergeRegion1");

    // Kayıt kümesini kapatın ve başka bir SQL sorgusundan gelen verilerle yeniden açın.
    command = "SELECT * FROM Customers";

    recordset.Close();
    recordset.Open(command, connection);

    // İkinci bölgede ikinci bir adres-mektup birleştirme çalıştırın ve belgeyi kaydedin.
    doc.MailMerge.ExecuteWithRegionsADO(recordset, "MergeRegion2");

    doc.Save(ArtifactsDir + "MailMerge.ExecuteWithRegionsADO.docx");

}

/// <summary>
/// İki adres-mektup birleştirme bölgesine sahip bir belge oluşturun.
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
* ad alanı [Aspose.Words.MailMerging](../../mailmerge/)
* toplantı [Aspose.Words](../../../)


