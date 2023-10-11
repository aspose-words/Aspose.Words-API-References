---
title: MailMerge.ExecuteADO
second_title: Aspose.Words for .NET API Referansı
description: MailMerge yöntem. Bir ADO Recordset nesnesinden belgeye adresmektup birleştirme gerçekleştirir.
type: docs
weight: 190
url: /tr/net/aspose.words.mailmerging/mailmerge/executeado/
---
## MailMerge.ExecuteADO method

Bir ADO Recordset nesnesinden belgeye adres-mektup birleştirme gerçekleştirir.

```csharp
public void ExecuteADO(object recordset)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| recordset | Object | ADO Kayıt Kümesi veya Kayıt nesnesi. |

### Notlar

Bu yöntem, Aspose.Words sınıflarını as COM nesnelerini, örneğin ASP veya Visual Basic 6.0 kullanılarak oluşturulan bir uygulama gibi yönetilmeyen koddan kullanmayı planladığınızda kullanışlıdır.

Bu yöntem göz ardı edilirRemoveUnusedRegions seçenek.

Daha fazla bilgi için açıklamasına bakın[`Execute`](../execute/).

### Örnekler

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

ADO veri kümesindeki verilerle adres-mektup birleştirmenin nasıl çalıştırılacağını gösterir.

```csharp
public void ExecuteADO()
{
    Document doc = CreateSourceDocADOMailMerge();

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
    const string command = @"SELECT ProductName, QuantityPerUnit, UnitPrice FROM Products";

    ADODB.Recordset recordset = new ADODB.Recordset();
    recordset.Open(command, connection);

    // Adres-mektup birleştirmeyi yürütün ve belgeyi kaydedin.
    doc.MailMerge.ExecuteADO(recordset);
    doc.Save(ArtifactsDir + "MailMerge.ExecuteADO.docx");
}

/// <summary>
/// Boş bir belge oluşturun ve bunu, adres-mektup birleştirme yürütüldüğünde verileri kabul edecek MERGEFIELDS ile doldurun.
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

### Ayrıca bakınız

* class [MailMerge](../)
* ad alanı [Aspose.Words.MailMerging](../../mailmerge/)
* toplantı [Aspose.Words](../../../)


