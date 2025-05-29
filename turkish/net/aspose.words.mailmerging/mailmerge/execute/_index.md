---
title: MailMerge.Execute
linktitle: Execute
articleTitle: Execute
second_title: .NET için Aspose.Words
description: MailMerge Execute yöntemi ile postalama sürecinizi kolaylaştırın ve kişiselleştirilmiş iletişim için özel kaynaklardan gelen verileri zahmetsizce birleştirin.
type: docs
weight: 180
url: /tr/net/aspose.words.mailmerging/mailmerge/execute/
---
## Execute(*[IMailMergeDataSource](../../imailmergedatasource/)*) {#execute}

Özel bir veri kaynağından posta birleştirme gerçekleştirir.

```csharp
public void Execute(IMailMergeDataSource dataSource)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| dataSource | IMailMergeDataSource | Özel posta birleştirme veri kaynağı arayüzünü uygulayan bir nesne. |

## Notlar

Bu yöntemi, belgedeki posta birleştirme alanlarını bir liste veya karma tablo veya nesneler gibi herhangi bir veri kaynağından gelen değerlerle doldurmak için kullanın. Bunu uygulayan kendi sınıfınızı yazmanız gerekir.[`IMailMergeDataSource`](../../imailmergedatasource/) arayüz.

Bu yöntemi yalnızca şu durumlarda kullanabilirsiniz:[`IsBidiTextSupportedOnUpdate`](../../../aspose.words.fields/fieldoptions/isbiditextsupportedonupdate/) dır`YANLIŞ`, yani Sağdan Sola dil (örneğin Arapça veya İbranice) uyumluluğuna ihtiyacınız yok.

Bu yöntem,RemoveUnusedRegions seçenek.

## Örnekler

Özel bir nesne biçiminde bir veri kaynağıyla posta birleştirmenin nasıl gerçekleştirileceğini gösterir.

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

     // Özel bir nesneyi veri kaynağı olarak kullanmak için IMailMergeDataSource arayüzünü uygulaması gerekir.
    CustomerMailMergeDataSource dataSource = new CustomerMailMergeDataSource(customers);

    doc.MailMerge.Execute(dataSource);

    doc.Save(ArtifactsDir + "MailMergeCustom.CustomDataSource.docx");
}

/// <summary>
/// Uygulamanızdaki "veri varlığı" sınıfının bir örneği.
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
 /// Aspose.Words'e izin vermek için uyguladığınız özel bir posta birleştirme veri kaynağı
/// Müşteri nesnelerinizdeki verileri Microsoft Word belgelerine birleştirmek için.
/// </summary>
public class CustomerMailMergeDataSource : IMailMergeDataSource
{
    public CustomerMailMergeDataSource(List<Customer> customers)
    {
        mCustomers = customers;

        // Veri kaynağını başlattığımızda, konumunun ilk kayıttan önce olması gerekir.
        mRecordIndex = -1;
    }

    /// <summary>
    /// Veri kaynağının adı. Aspose.Words tarafından yalnızca tekrarlanabilir bölgelerle posta birleştirme işlemi yürütülürken kullanılır.
    /// </summary>
    public string TableName
    {
        get { return "Customer"; }
    }

    /// <summary>
    /// Aspose.Words her veri alanı için bir değer almak amacıyla bu metodu çağırır.
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
                // Aspose.Words posta birleştirme motoruna "false" değerini döndürerek belirtin
                // Bu isimde bir alan bulamadık.
                fieldValue = null;
                return false;
        }
    }

    /// <summary>
    /// Bir koleksiyondaki bir sonraki kayda geçmek için standart bir uygulama.
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

### Ayrıca bakınız

* interface [IMailMergeDataSource](../../imailmergedatasource/)
* class [MailMerge](../)
* ad alanı [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* toplantı [Aspose.Words](../../../)

---

## Execute(*string[], object[]*) {#execute_5}

Tek bir kayıt için bir posta birleştirme işlemi gerçekleştirir.

```csharp
public void Execute(string[] fieldNames, object[] values)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| fieldNames | String[] | Birleştirme alanı adları dizisi. Alan adları büyük/küçük harfe duyarlı değildir. Belgede bulunmayan bir alan adıyla karşılaşılırsa, bu ad yoksayılır. |
| values | Object[] | Birleştirme alanlarına eklenecek değer dizisi. Bu dizideki öğe sayısı, dizideki öğe sayısıyla aynı olmalıdır.*fieldNames*. |

## Notlar

Belgedeki birleştirme alanlarını nesnelerden oluşan bir dizi olan değerleriyle doldurmak için bu yöntemi kullanın.

Bu yöntem yalnızca bir kayıt için verileri birleştirir. Alan adları dizisi ve değerler dizisi tek bir kaydın verilerini temsil eder.

Bu yöntem posta birleştirme bölgelerini kullanmaz.

Bu yöntem,RemoveUnusedRegions seçenek.

## Örnekler

Bir URI'den gelen bir görüntünün birleştirme postası verisi olarak bir MERGEFIELD'a nasıl birleştirileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// "Image:" etiketli MERGEFIELD'lar, posta birleştirme sırasında bir resim alacaktır.
// "Image:" etiketindeki iki noktadan sonraki dize bir sütun adına karşılık gelir
// Hücreleri resim dosyalarının URI'lerini içeren veri kaynağında.
builder.InsertField("MERGEFIELD  Image:logo_FromWeb ");
builder.InsertField("MERGEFIELD  Image:logo_FromFileSystem ");

 // Birleştireceğimiz resimlerin URI'lerini içeren bir veri kaynağı oluşturun.
// Bir URI, bir görüntüye işaret eden bir web URL'si veya bir görüntü dosyasının yerel dosya sistemi dosya adı olabilir.
string[] columns = { "logo_FromWeb", "logo_FromFileSystem" };
object[] URIs = { ImageUrl, ImageDir + "Logo.jpg" };

// Tek satırdan oluşan bir veri kaynağında posta birleştirme işlemini gerçekleştir.
doc.MailMerge.Execute(columns, URIs);

doc.Save(ArtifactsDir + "MailMergeEvent.ImageFromUrl.docx");
```

Posta birleştirmenin nasıl gerçekleştirileceğini ve ardından belgenin istemci tarayıcısına nasıl kaydedileceğini gösterir.

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

// Belgeyi istemci tarayıcısına gönder.
//Testte HttpResponse boş olduğu için atıldı.
Assert.Throws<ArgumentNullException>(() => doc.Save(response, "Artifacts/MailMerge.ExecuteArray.docx", ContentDisposition.Inline, null));

// Kaydedildikten sonra belgeye gereksiz içerik eklememek için bu yanıtı manuel olarak kapatmamız gerekecek.
Assert.Throws<NullReferenceException>(() => response.End());
```

### Ayrıca bakınız

* class [MailMerge](../)
* ad alanı [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* toplantı [Aspose.Words](../../../)

---

## Execute(*DataTable*) {#execute_2}

Bir DataTable'dan belgeye posta birleştirme işlemini gerçekleştirir.

```csharp
public void Execute(DataTable table)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| table | DataTable | Posta birleştirme alanlarına eklenecek verileri içeren tablo. Alan adları büyük/küçük harfe duyarlı değildir. Belgede bulunmayan bir alan adıyla karşılaşıldığında, bu ad yoksayılır. |

## Notlar

Belgedeki birleştirme alanlarını a değerleriyle doldurmak için bu yöntemi kullanın**Veri Tablosu**.

Tablodaki tüm kayıtlar belgeye birleştirilir.

Word belgesinde NEXT alanını kullanarak[`MailMerge`](../) select sonraki kaydı seçmek için nesne**Veri Tablosu** ve birleştirmeye devam edin. Bu, posta etiketleri gibi belgeler oluştururken kullanılabilir.

Ne zaman[`MailMerge`](../) nesne ana belgenin sonuna ulaşır ve hala daha fazla satır vardır**Veri Tablosu**ana belgenin tüm içeriğini kopyalar ve ayırıcı olarak section kesmesini kullanarak hedef belgenin sonuna ekler.

Bu yöntem,RemoveUnusedRegions seçenek.

## Örnekler

DataTable'daki verilerle posta birleştirme işleminin nasıl gerçekleştirileceğini gösterir.

```csharp
public void ExecuteDataTable()
{
    DataTable table = new DataTable("Test");
    table.Columns.Add("CustomerName");
    table.Columns.Add("Address");
    table.Rows.Add(new object[] { "Thomas Hardy", "120 Hanover Sq., London" });
    table.Rows.Add(new object[] { "Paolo Accorti", "Via Monte Bianco 34, Torino" });

    // Aşağıda bir posta birleştirme için veri kaynağı olarak DataTable kullanmanın iki yolu bulunmaktadır.
    // 1 - Tablonun tamamını kullanarak, tablodaki her satır için tek bir çıktı birleştirme belgesi oluşturun:
    Document doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.WholeTable.docx");

    // 2 - Tablonun bir satırını kullanarak tek bir çıktı birleştirme belgesi oluşturun:
    doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table.Rows[1]);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.OneRow.docx");
}

/// <summary>
/// Bir posta birleştirme kaynak belgesi oluşturur.
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

### Ayrıca bakınız

* class [MailMerge](../)
* ad alanı [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* toplantı [Aspose.Words](../../../)

---

## Execute(*IDataReader*) {#execute_4}

Posta birleştirme işlemini gerçekleştirir**IDataOkuyucu** belgeye.

```csharp
public void Execute(IDataReader dataReader)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| dataReader | IDataReader | Posta birleştirme işlemi için veri kaynağı. |

## Notlar

Geçebilirsin**SqlDataOkuyucu** veya**OleDbVeriOkuyucu**nesneyi this yöntemine parametre olarak eklediler çünkü ikisi de uygulandı**IDataOkuyucu** arayüz.

Bu yöntemin birleştirme bölgelerini kullanmadığını ve birden fazla kayıt için the belgesinin tüm belgeyi tekrarlayarak büyüyeceğini unutmayın.

Bu yöntem,RemoveUnusedRegions seçenek.

## Örnekler

Veri okuyucusundan gelen verileri kullanarak posta birleştirmenin nasıl çalıştırılacağını gösterir.

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

// "Northwind" veritabanı dosyasına işaret eden bir bağlantı dizesi oluşturun
// yerel dosya sistemimizde bir bağlantı açın ve bir SQL sorgusu ayarlayın.
string connectionString = @"Provider = Microsoft.ACE.OLEDB.12.0; Data Source=" + DatabaseDir + "Northwind.accdb";
string query =
    @"SELECT Products.ProductName, Suppliers.CompanyName, Products.QuantityPerUnit, Products.UnitPrice
    FROM Products 
    INNER JOIN Suppliers 
    ON Products.SupplierID = Suppliers.SupplierID";

using (OleDbConnection connection = new OleDbConnection(connectionString))
{
    // Posta birleştirme işlemimiz için veri kaynağı olacak bir SQL komutu oluşturun.
    // Bu SELECT ifadesinin döndüreceği tablonun sütunlarının adları
    // yukarıda yerleştirdiğimiz birleştirme alanlarına karşılık gelmesi gerekecektir.
    OleDbCommand command = new OleDbCommand(query, connection);
    command.CommandText = query;
    try
    {
        connection.Open();
        using (OleDbDataReader reader = command.ExecuteReader())
        {
            // Okuyucudan verileri al ve posta birleştirmede kullan.
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

### Ayrıca bakınız

* class [MailMerge](../)
* ad alanı [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* toplantı [Aspose.Words](../../../)

---

## Execute(*DataView*) {#execute_3}

Bir e-posta birleştirme işlemini gerçekleştirir**VeriGörünümü** belgeye.

```csharp
public void Execute(DataView dataView)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| dataView | DataView | Posta birleştirme işlemi için veri kaynağı. |

## Notlar

Bu yöntem, verileri bir**Veri Tablosu** ancak then birleştirmeden önce bir filtre veya sıralama uygulamanız gerekir.

Bu yöntemin birleştirme bölgelerini kullanmadığını ve birden fazla kayıt için the belgesinin tüm belgeyi tekrarlayarak büyüyeceğini unutmayın.

Bu yöntem,RemoveUnusedRegions seçenek.

## Örnekler

Bir DataView ile posta birleştirme verilerinin nasıl düzenleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Congratulations ");
builder.InsertField(" MERGEFIELD Name");
builder.Write(" for passing with a grade of ");
builder.InsertField(" MERGEFIELD Grade");

// Posta birleştirmemizin veri alacağı bir veri tablosu oluşturun.
DataTable table = new DataTable("ExamResults");
table.Columns.Add("Name");
table.Columns.Add("Grade");
table.Rows.Add(new object[] { "John Doe", "67" });
table.Rows.Add(new object[] { "Jane Doe", "81" });
table.Rows.Add(new object[] { "John Cardholder", "47" });
table.Rows.Add(new object[] { "Joe Bloggs", "75" });

// Veri tablosunda değişiklik yapmadan, posta birleştirme verilerini değiştirmek için bir veri görünümü kullanabiliriz.
DataView view = new DataView(table);
view.Sort = "Grade DESC";
view.RowFilter = "Grade >= 50";

// Veri görünümümüz, girdileri "Sınıf" sütunu boyunca azalan düzende sıralar
// ve o sütunda değeri 50'den küçük olan satırları filtreler.
// Dört satırdan üçü bu ölçütlere uyduğundan çıktı belgesi üç birleştirme belgesi içerecektir.
doc.MailMerge.Execute(view);

doc.Save(ArtifactsDir + "MailMerge.ExecuteDataView.docx");
```

### Ayrıca bakınız

* class [MailMerge](../)
* ad alanı [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* toplantı [Aspose.Words](../../../)

---

## Execute(*DataRow*) {#execute_1}

Bir e-posta birleştirme işlemini gerçekleştirir**Veri Satırı** belgeye.

```csharp
public void Execute(DataRow row)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| row | DataRow | Posta birleştirme alanlarına eklenecek verileri içeren satır. Alan adları büyük/küçük harfe duyarlı değildir. Belgede bulunmayan bir alan adıyla karşılaşıldığında, bu ad yoksayılır. |

## Notlar

Belgedeki birleştirme alanlarını bir e-posta adresinden gelen değerlerle doldurmak için bu yöntemi kullanın.**Veri Satırı**.

Bu yöntem,RemoveUnusedRegions seçenek.

## Örnekler

DataTable'daki verilerle posta birleştirme işleminin nasıl gerçekleştirileceğini gösterir.

```csharp
public void ExecuteDataTable()
{
    DataTable table = new DataTable("Test");
    table.Columns.Add("CustomerName");
    table.Columns.Add("Address");
    table.Rows.Add(new object[] { "Thomas Hardy", "120 Hanover Sq., London" });
    table.Rows.Add(new object[] { "Paolo Accorti", "Via Monte Bianco 34, Torino" });

    // Aşağıda bir posta birleştirme için veri kaynağı olarak DataTable kullanmanın iki yolu bulunmaktadır.
    // 1 - Tablonun tamamını kullanarak, tablodaki her satır için tek bir çıktı birleştirme belgesi oluşturun:
    Document doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.WholeTable.docx");

    // 2 - Tablonun bir satırını kullanarak tek bir çıktı birleştirme belgesi oluşturun:
    doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table.Rows[1]);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.OneRow.docx");
}

/// <summary>
/// Bir posta birleştirme kaynak belgesi oluşturur.
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

### Ayrıca bakınız

* class [MailMerge](../)
* ad alanı [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* toplantı [Aspose.Words](../../../)
