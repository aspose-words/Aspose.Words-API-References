---
title: MailMerge.Execute
second_title: Aspose.Words for .NET API Referansı
description: MailMerge yöntem. Özel bir veri kaynağından adresmektup birleştirme gerçekleştirir.
type: docs
weight: 180
url: /tr/net/aspose.words.mailmerging/mailmerge/execute/
---
## Execute(IMailMergeDataSource) {#execute}

Özel bir veri kaynağından adres-mektup birleştirme gerçekleştirir.

```csharp
public void Execute(IMailMergeDataSource dataSource)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| dataSource | IMailMergeDataSource | Özel adres-mektup birleştirme veri kaynağı arayüzünü uygulayan bir nesne. |

### Notlar

Belgedeki adres-mektup birleştirme alanlarını liste, karma tablosu veya nesneler gibi herhangi bir veri kaynağından değerleri ile doldurmak için bu yöntemi kullanın. Bunu uygulayan your kendi sınıfını yazmanız gerekir.[`IMailMergeDataSource`](../../imailmergedatasource/) arayüz.

Bu yöntemi yalnızca şu durumlarda kullanabilirsiniz:[`IsBidiTextSupportedOnUpdate`](../../../aspose.words.fields/fieldoptions/isbiditextsupportedonupdate/) dır-dir`YANLIŞ`, yani Sağdan Sola dil (Arapça veya İbranice gibi) uyumluluğuna ihtiyacınız yoktur.

Bu yöntem göz ardı edilirRemoveUnusedRegions seçenek.

### Ayrıca bakınız

* interface [IMailMergeDataSource](../../imailmergedatasource/)
* class [MailMerge](../)
* ad alanı [Aspose.Words.MailMerging](../../mailmerge/)
* toplantı [Aspose.Words](../../../)

---

## Execute(string[], object[]) {#execute_5}

Tek bir kayıt için adres-mektup birleştirme işlemi gerçekleştirir.

```csharp
public void Execute(string[] fieldNames, object[] values)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| fieldNames | String[] | Birleştirme alanı adları dizisi. Alan adları büyük/küçük harfe duyarlı değildir. Belgede bulunmayan bir alan adıyla karşılaşılırsa dikkate alınmaz. |
| values | Object[] | Birleştirme alanlarına eklenecek değerler dizisi. Bu dizideki öğe sayısı, dizideki öğe sayısıyla aynı olmalıdır*fieldNames*. |

### Notlar

Belgedeki adres-mektup birleştirme alanlarını bir nesne dizisinden değerleri ile doldurmak için bu yöntemi kullanın.

Bu yöntem yalnızca bir kayda ait verileri birleştirir. name alan dizisi ve değerler dizisi tek bir kaydın verilerini temsil eder.

Bu yöntem adres-mektup birleştirme bölgelerini kullanmaz.

Bu yöntem göz ardı edilirRemoveUnusedRegions seçenek.

### Örnekler

URI'deki bir görüntünün adres-mektup birleştirme verileri olarak MERGEFIELD'a nasıl birleştirileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// "Resim:" etiketli MERGEFIELD'ler, adres-mektup birleştirme sırasında bir resim alacaktır.
// "Resim:" etiketindeki iki nokta üst üste işaretinden sonraki dize, bir sütun adına karşılık gelir
// hücreleri görüntü dosyalarının URI'lerini içeren veri kaynağında.
builder.InsertField("MERGEFIELD  Image:logo_FromWeb ");
builder.InsertField("MERGEFIELD  Image:logo_FromFileSystem ");

 // Birleştireceğimiz görsellerin URI'lerini içeren bir veri kaynağı oluşturun.
// URI, bir görsele işaret eden bir web URL'si veya bir görsel dosyasının yerel dosya sistemi dosya adı olabilir.
string[] columns = { "logo_FromWeb", "logo_FromFileSystem" };
object[] URIs = { ImageUrl, ImageDir + "Logo.jpg" };

// Tek satırlı bir veri kaynağında adres-mektup birleştirme gerçekleştirin.
doc.MailMerge.Execute(columns, URIs);

doc.Save(ArtifactsDir + "MailMergeEvent.ImageFromUrl.docx");
```

Adres-mektup birleştirmenin nasıl gerçekleştirileceğini ve ardından belgenin istemci tarayıcısına nasıl kaydedileceğini gösterir.

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

// Belgeyi istemci tarayıcısına gönderin.
Assert.That(() => doc.Save(response, "Artifacts/MailMerge.ExecuteArray.docx", ContentDisposition.Inline, null),
    Throws.TypeOf<ArgumentNullException>()); //HttpResponse testte null olduğundan atıldı.

// Kaydettikten sonra belgeye gereksiz içerik eklemediğimizden emin olmak için bu yanıtı manuel olarak kapatmamız gerekecek.
Assert.That(() => response.End(), Throws.TypeOf<NullReferenceException>());
```

### Ayrıca bakınız

* class [MailMerge](../)
* ad alanı [Aspose.Words.MailMerging](../../mailmerge/)
* toplantı [Aspose.Words](../../../)

---

## Execute(DataTable) {#execute_2}

DataTable'dan belgeye adres-mektup birleştirme gerçekleştirir.

```csharp
public void Execute(DataTable table)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| table | DataTable | Adres-mektup birleştirme alanlarına eklenecek verileri içeren tablo. Alan adları büyük/küçük harfe duyarlı değildir. Belgede bulunmayan bir alan adıyla karşılaşılırsa dikkate alınmaz. |

### Notlar

Belgedeki adres-mektup birleştirme alanlarını a değerleri ile doldurmak için bu yöntemi kullanın. **Veri tablosu**.

Tablodaki tüm kayıtlar belgede birleştirilir.

Bunun için Word belgesindeki NEXT alanını kullanabilirsiniz.[`MailMerge`](../) sonraki kaydın seçilmesi nesnesi **Veri tablosu** ve birleştirmeye devam edin. Bu, posta etiketleri gibi belgeler oluştururken kullanılabilir.

Ne zaman[`MailMerge`](../) nesne ana belgenin sonuna ulaştığında hala more satırları var **Veri tablosu**, ana belgenin içeriğinin tamamını kopyalar ve ayırıcı olarak bir bölüm sonu kullanarak bunu hedef belgenin sonuna ekler.

Bu yöntem göz ardı edilirRemoveUnusedRegions seçenek.

### Örnekler

DataTable'daki verilerle adres-mektup birleştirmenin nasıl yürütüleceğini gösterir.

```csharp
public void ExecuteDataTable()
{
    DataTable table = new DataTable("Test");
    table.Columns.Add("CustomerName");
    table.Columns.Add("Address");
    table.Rows.Add(new object[] { "Thomas Hardy", "120 Hanover Sq., London" });
    table.Rows.Add(new object[] { "Paolo Accorti", "Via Monte Bianco 34, Torino" });

    // Aşağıda, adres-mektup birleştirme için veri kaynağı olarak DataTable'ı kullanmanın iki yolu verilmiştir.
    // 1 - Tablodaki her satır için bir çıktı adres-mektup birleştirme belgesi oluşturmak amacıyla adres-mektup birleştirme için tablonun tamamını kullanın:
    Document doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.WholeTable.docx");

    // 2 - Bir çıktı adres-mektup birleştirme belgesi oluşturmak için tablonun bir satırını kullanın:
    doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table.Rows[1]);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.OneRow.docx");
}

/// <summary>
/// Adres-mektup birleştirme kaynak belgesi oluşturur.
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
* ad alanı [Aspose.Words.MailMerging](../../mailmerge/)
* toplantı [Aspose.Words](../../../)

---

## Execute(IDataReader) {#execute_4}

Adres-mektup birleştirmeyi şuradan gerçekleştirir: **IDataReader** belgeye.

```csharp
public void Execute(IDataReader dataReader)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| dataReader | IDataReader | Adres-mektup birleştirme işlemi için veri kaynağı. |

### Notlar

Geçebilirsin **SqlDataReader** veya **OleDbDataReader** this yöntemine parametre olarak itiraz edin çünkü ikisi de uygulandı **IDataReader** arayüz.

Bu yöntemin adres-mektup birleştirme bölgelerini kullanmadığını ve birden fazla kayıt için the belgesinin tüm belgeyi tekrarlayarak büyüyeceğini unutmayın.

Bu yöntem göz ardı edilirRemoveUnusedRegions seçenek.

### Örnekler

Veri okuyucudan alınan verileri kullanarak adres-mektup birleştirmenin nasıl çalıştırılacağını gösterir.

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
// yerel dosya sistemimizde bir bağlantı açın ve bir SQL sorgusu oluşturun.
string connectionString = @"Provider = Microsoft.ACE.OLEDB.12.0; Data Source=" + DatabaseDir + "Northwind.accdb";
string query =
    @"SELECT Products.ProductName, Suppliers.CompanyName, Products.QuantityPerUnit, Products.UnitPrice
    FROM Products 
    INNER JOIN Suppliers 
    ON Products.SupplierID = Suppliers.SupplierID";

using (OleDbConnection connection = new OleDbConnection(connectionString))
{
    // Adres-mektup birleştirmemiz için veri kaynağı olacak bir SQL komutu oluşturun.
    // Bu SELECT ifadesinin döndüreceği tablo sütunlarının adları
    // yukarıda yerleştirdiğimiz birleştirme alanlarına karşılık gelmeli.
    OleDbCommand command = new OleDbCommand(query, connection);
    command.CommandText = query;
    try
    {                    
        connection.Open();                 
        using (OleDbDataReader reader = command.ExecuteReader())
        {
            // Verileri okuyucudan alın ve adres-mektup birleştirmede kullanın.
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
* ad alanı [Aspose.Words.MailMerging](../../mailmerge/)
* toplantı [Aspose.Words](../../../)

---

## Execute(DataView) {#execute_3}

Adres-mektup birleştirmeyi bir adresten gerçekleştirir. **Veri görünümü** belgeye.

```csharp
public void Execute(DataView dataView)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| dataView | DataView | Adres-mektup birleştirme işlemi için veri kaynağı. |

### Notlar

Bu yöntem, verileri bir dosyaya alırsanız kullanışlıdır. **Veri tablosu** ancak Then adres-mektup birleştirmeden önce bir filtre uygulamanız veya sıralamanız gerekir.

Bu yöntemin adres-mektup birleştirme bölgelerini kullanmadığını ve birden fazla kayıt için the belgesinin tüm belgeyi tekrarlayarak büyüyeceğini unutmayın.

Bu yöntem göz ardı edilirRemoveUnusedRegions seçenek.

### Örnekler

DataView ile adres-mektup birleştirme verilerinin nasıl düzenleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Congratulations ");
builder.InsertField(" MERGEFIELD Name");
builder.Write(" for passing with a grade of ");
builder.InsertField(" MERGEFIELD Grade");

// Adres-mektup birleştirmemizin veri kaynağı olacağı bir veri tablosu oluşturun.
DataTable table = new DataTable("ExamResults");
table.Columns.Add("Name");
table.Columns.Add("Grade");
table.Rows.Add(new object[] { "John Doe", "67" });
table.Rows.Add(new object[] { "Jane Doe", "81" });
table.Rows.Add(new object[] { "John Cardholder", "47" });
table.Rows.Add(new object[] { "Joe Bloggs", "75" });

// Veri tablosunun kendisinde değişiklik yapmadan adres-mektup birleştirme verilerini değiştirmek için veri görünümünü kullanabiliriz.
DataView view = new DataView(table);
view.Sort = "Grade DESC";
view.RowFilter = "Grade >= 50";

// Veri görünümümüz, girişleri "Not" sütunu boyunca azalan düzende sıralar
// ve o sütundaki değeri 50'den küçük olan satırları filtreler.
// Dört satırdan üçü bu kriterlere uyuyor, böylece çıktı belgesi üç birleştirme belgesi içerecek.
doc.MailMerge.Execute(view);

doc.Save(ArtifactsDir + "MailMerge.ExecuteDataView.docx");
```

### Ayrıca bakınız

* class [MailMerge](../)
* ad alanı [Aspose.Words.MailMerging](../../mailmerge/)
* toplantı [Aspose.Words](../../../)

---

## Execute(DataRow) {#execute_1}

Adres-mektup birleştirmeyi bir adresten gerçekleştirir. **Veri Satırı** belgeye.

```csharp
public void Execute(DataRow row)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| row | DataRow | Adres-mektup birleştirme alanlarına eklenecek verileri içeren satır. Alan adları büyük/küçük harfe duyarlı değildir. Belgede bulunmayan bir alan adıyla karşılaşılırsa dikkate alınmaz. |

### Notlar

Belgedeki adres-mektup birleştirme alanlarını bir adresten gelen değerlerle doldurmak için bu yöntemi kullanın. **Veri Satırı**.

Bu yöntem göz ardı edilirRemoveUnusedRegions seçenek.

### Örnekler

DataTable'daki verilerle adres-mektup birleştirmenin nasıl yürütüleceğini gösterir.

```csharp
public void ExecuteDataTable()
{
    DataTable table = new DataTable("Test");
    table.Columns.Add("CustomerName");
    table.Columns.Add("Address");
    table.Rows.Add(new object[] { "Thomas Hardy", "120 Hanover Sq., London" });
    table.Rows.Add(new object[] { "Paolo Accorti", "Via Monte Bianco 34, Torino" });

    // Aşağıda, adres-mektup birleştirme için veri kaynağı olarak DataTable'ı kullanmanın iki yolu verilmiştir.
    // 1 - Tablodaki her satır için bir çıktı adres-mektup birleştirme belgesi oluşturmak amacıyla adres-mektup birleştirme için tablonun tamamını kullanın:
    Document doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.WholeTable.docx");

    // 2 - Bir çıktı adres-mektup birleştirme belgesi oluşturmak için tablonun bir satırını kullanın:
    doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table.Rows[1]);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.OneRow.docx");
}

/// <summary>
/// Adres-mektup birleştirme kaynak belgesi oluşturur.
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
* ad alanı [Aspose.Words.MailMerging](../../mailmerge/)
* toplantı [Aspose.Words](../../../)


