---
title: MailMerge.ExecuteADO
linktitle: ExecuteADO
articleTitle: ExecuteADO
second_title: .NET için Aspose.Words
description: MailMerge ExecuteADO yöntemiyle belge oluşturmanızı kolaylaştırın. Verimli, kişiselleştirilmiş çıktı için ADO Kayıt Kümesi verilerini zahmetsizce birleştirin.
type: docs
weight: 190
url: /tr/net/aspose.words.mailmerging/mailmerge/executeado/
---
## MailMerge.ExecuteADO method

ADO Kayıt Kümesi nesnesinden belgeye posta birleştirme gerçekleştirir.

```csharp
public void ExecuteADO(object recordset)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| recordset | Object | ADO Kayıt Kümesi veya Kayıt nesnesi. |

## Notlar

Bu yöntem, Aspose.Words sınıflarını, yönetilmeyen koddan (örneğin, ASP veya Visual Basic 6.0 kullanılarak oluşturulmuş bir uygulama) as COM nesneleri olarak kullanmayı planladığınızda yararlıdır.

Bu yöntem,RemoveUnusedRegions seçenek.

Daha fazla bilgi için açıklamayı inceleyin[`Execute`](../execute/).

## Örnekler

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

ADO veri kümesindeki verilerle posta birleştirmenin nasıl çalıştırılacağını gösterir.

```csharp
public void ExecuteADO()
{
    Document doc = CreateSourceDocADOMailMerge();

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
    const string command = @"SELECT ProductName, QuantityPerUnit, UnitPrice FROM Products";

    ADODB.Recordset recordset = new ADODB.Recordset();
    recordset.Open(command, connection);

    // Posta birleştirmeyi gerçekleştirin ve belgeyi kaydedin.
    doc.MailMerge.ExecuteADO(recordset);
    doc.Save(ArtifactsDir + "MailMerge.ExecuteADO.docx");
}

/// <summary>
/// Boş bir belge oluşturun ve bir posta birleştirme işlemi yürütüldüğünde veri kabul edecek MERGEFIELDS ile doldurun.
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
* ad alanı [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* toplantı [Aspose.Words](../../../)
