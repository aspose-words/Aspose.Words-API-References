---
title: MailMerge.Execute
second_title: Aspose.Words for .NET API Referansı
description: MailMerge yöntem. Özel bir veri kaynağından adres mektup birleştirme gerçekleştirir.
type: docs
weight: 180
url: /tr/net/aspose.words.mailmerging/mailmerge/execute/
---
## Execute(IMailMergeDataSource) {#execute}

Özel bir veri kaynağından adres mektup birleştirme gerçekleştirir.

```csharp
public void Execute(IMailMergeDataSource dataSource)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| dataSource | IMailMergeDataSource | Özel adres mektup birleştirme veri kaynağı arabirimini uygulayan bir nesne. |

### Notlar

Belgedeki adres mektup birleştirme alanlarını liste veya karma tablo veya nesneler gibi herhangi bir veri kaynağından gelen değerleriyle doldurmak için bu yöntemi kullanın. Şunu uygulayan your kendi sınıfınızı yazmanız gerekir.[`IMailMergeDataSource`](../../imailmergedatasource/) arayüz.

Bu yöntemi yalnızca şu durumlarda kullanabilirsiniz:[`IsBidiTextSupportedOnUpdate`](../../../aspose.words.fields/fieldoptions/isbiditextsupportedonupdate/)false, yani Sağdan Sola dil (Arapça veya İbranice gibi) uyumluluğuna ihtiyacınız yoktur.

Bu yöntem yok sayarRemoveUnusedRegions seçenek.

### Ayrıca bakınız

* interface [IMailMergeDataSource](../../imailmergedatasource/)
* class [MailMerge](../)
* ad alanı [Aspose.Words.MailMerging](../../mailmerge/)
* toplantı [Aspose.Words](../../../)

---

## Execute(string[], object[]) {#execute_5}

Tek bir kayıt için adres mektup birleştirme işlemi gerçekleştirir.

```csharp
public void Execute(string[] fieldNames, object[] values)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| fieldNames | String[] | Birleştirme alan adları dizisi. Alan adları büyük/küçük harf duyarlı değildir. Belgede bulunmayan bir alan adıyla karşılaşılırsa yok sayılır. |
| values | Object[] | Birleştirme alanlarına eklenecek değerler dizisi. Bu dizideki öğelerin sayısı, fieldNames içindeki öğelerin sayısıyla aynı olmalıdır. |

### Notlar

Belgedeki adres mektup birleştirme alanlarını bir dizi nesneden gelen değerleriyle doldurmak için bu yöntemi kullanın.

Bu yöntem yalnızca bir kayıt için verileri birleştirir. name alan dizisi ve değerler dizisi, tek bir kaydın verilerini temsil eder.

Bu yöntem, adres mektup birleştirme bölgelerini kullanmaz.

Bu yöntem yok sayarRemoveUnusedRegions seçenek.

### Örnekler

Adres mektup birleştirme verileri olarak bir URI'den bir görüntünün bir MERGEFIELD'de nasıl birleştirileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// "Image:" etiketli MERGEFIELD'ler, adres mektup birleştirme sırasında bir resim alacaktır.
// "Image:" etiketindeki iki nokta üst üste işaretinden sonraki dize, bir sütun adına karşılık gelir
// hücreleri görüntü dosyalarının URI'lerini içeren veri kaynağında.
builder.InsertField("MERGEFIELD  Image:logo_FromWeb ");
builder.InsertField("MERGEFIELD  Image:logo_FromFileSystem ");

 // Birleştireceğimiz görüntülerin URI'lerini içeren bir veri kaynağı oluşturun.
// URI, bir resme işaret eden bir web URL'si veya bir resim dosyasının yerel dosya sistemi dosya adı olabilir.
string[] columns = { "logo_FromWeb", "logo_FromFileSystem" };
object[] URIs = { ImageUrl, ImageDir + "Logo.jpg" };

// Tek satırlı bir veri kaynağında adres mektup birleştirme yürütün.
doc.MailMerge.Execute(columns, URIs);

doc.Save(ArtifactsDir + "MailMergeEvent.ImageFromUrl.docx");
```

Adres mektup birleştirmenin nasıl gerçekleştirileceğini ve ardından belgenin istemci tarayıcısına nasıl kaydedileceğini gösterir.

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
Assert.That(() => doc.Save(response, "Artifacts/MailMerge.ExecuteArray.docx", ContentDisposition.Inline, null),
    Throws.TypeOf<ArgumentNullException>()); //HttpResponse testte boş olduğu için atıldı.

// Kaydettikten sonra belgeye gereksiz içerik eklemediğimizden emin olmak için bu yanıtı manuel olarak kapatmamız gerekecek.
Assert.That(() => response.End(), Throws.TypeOf<NullReferenceException>());
```

### Ayrıca bakınız

* class [MailMerge](../)
* ad alanı [Aspose.Words.MailMerging](../../mailmerge/)
* toplantı [Aspose.Words](../../../)

---

## Execute(DataTable) {#execute_2}

Bir DataTable'dan belgeye adres mektup birleştirme gerçekleştirir.

```csharp
public void Execute(DataTable table)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| table | DataTable | Adres mektup birleştirme alanlarına eklenecek verileri içeren tablo. Alan adları büyük/küçük harf duyarlı değildir. Belgede bulunmayan bir alan adıyla karşılaşılırsa, yok sayılır. |

### Notlar

Belgedeki adres mektup birleştirme alanlarını a değerleriyle doldurmak için bu yöntemi kullanın. **Veri tablosu**.

Tablodaki tüm kayıtlar belgede birleştirilir.

Neden olmak için Word belgesindeki SONRAKİ alanını kullanabilirsiniz. **Posta birleştirme** nesneden bir sonraki kayda select  **Veri tablosu** ve birleştirmeye devam edin. Bu, posta etiketleri gibi belgeler oluşturulurken kullanılabilir.

Ne zaman **Posta birleştirme**nesne ana belgenin sonuna ulaşır ve dosyada hala daha fazla satır vardır. **Veri tablosu**, ana belgenin tüm içeriğini kopyalar ve ayırıcı olarak bölüm kesmesi kullanarak hedef belgenin sonuna ekler.

Bu yöntem yok sayarRemoveUnusedRegions seçenek.

### Örnekler

DataTable'daki verilerle adres mektup birleştirmenin nasıl yürütüleceğini gösterir.

```csharp
public void ExecuteDataTable()
{
    DataTable table = new DataTable("Test");
    table.Columns.Add("CustomerName");
    table.Columns.Add("Address");
    table.Rows.Add(new object[] { "Thomas Hardy", "120 Hanover Sq., London" });
    table.Rows.Add(new object[] { "Paolo Accorti", "Via Monte Bianco 34, Torino" });

    // Aşağıda, adres mektup birleştirme için veri kaynağı olarak bir DataTable kullanmanın iki yolu bulunmaktadır.
    // 1 - Tablodaki her satır için bir çıktı adres mektup birleştirme belgesi oluşturmak üzere adres mektup birleştirme için tüm tabloyu kullanın:
    Document doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.WholeTable.docx");

    // 2 - Bir çıktı adres mektup birleştirme belgesi oluşturmak için tablonun bir satırını kullanın:
    doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table.Rows[1]);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.OneRow.docx");
}

/// <summary>
/// Adres mektup birleştirme kaynak belgesi oluşturur.
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

IDataReader'dan belgeye adres mektup birleştirme gerçekleştirir.

```csharp
public void Execute(IDataReader dataReader)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| dataReader | IDataReader | Adres mektup birleştirme işlemi için veri kaynağı. |

### Notlar

Geçebilirsin **SqlDataOkuyucu** veya **OleDbDataOkuyucu** her ikisi de uygulandığı için parametre olarak this yöntemine nesne **IDataOkuyucu** arayüz.

Bu yöntemin adres mektup birleştirme bölgelerini kullanmadığını ve birden çok kayıt için belgesinin tüm belgeyi tekrarlayarak büyüyeceğini unutmayın.

Bu yöntem yok sayarRemoveUnusedRegions seçenek.

### Örnekler

Veri okuyucudan gelen verileri kullanarak adres mektup birleştirmenin nasıl çalıştırılacağını gösterir.

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
// yerel dosya sistemimizde bir bağlantı açın ve bir SQL sorgusu kurun.
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

    // Adres mektup birleştirmemiz için veri kaynağı olacak bir SQL komutu oluşturun.
    // Bu SELECT ifadesinin döndüreceği tablo sütunlarının adları
    // yukarıda yerleştirdiğimiz birleştirme alanlarına karşılık gelmesi gerekecek.
    OdbcCommand command = connection.CreateCommand();
    command.CommandText = query;

    // Bu, komutu çalıştıracak ve verileri okuyucuda saklayacaktır.
    OdbcDataReader reader = command.ExecuteReader(CommandBehavior.CloseConnection);

    // Verileri okuyucudan alın ve adres mektup birleştirmede kullanın.
    doc.MailMerge.Execute(reader);
}

doc.Save(ArtifactsDir + "MailMerge.ExecuteDataReader.docx");
```

### Ayrıca bakınız

* class [MailMerge](../)
* ad alanı [Aspose.Words.MailMerging](../../mailmerge/)
* toplantı [Aspose.Words](../../../)

---

## Execute(DataView) {#execute_3}

Bir DataView'den belgeye adres mektup birleştirme gerçekleştirir.

```csharp
public void Execute(DataView dataView)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| dataView | DataView | Adres mektup birleştirme işlemi için veri kaynağı. |

### Notlar

Bu yöntem, verileri bir **Veri tablosu** ancak then adres mektup birleştirmeden önce bir filtre veya sıralama uygulamanız gerekir.

Bu yöntemin adres mektup birleştirme bölgelerini kullanmadığını ve birden çok kayıt için belgesinin tüm belgeyi tekrarlayarak büyüyeceğini unutmayın.

Bu yöntem yok sayarRemoveUnusedRegions seçenek.

### Örnekler

Bir DataView ile adres mektup birleştirme verilerinin nasıl düzenleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Congratulations ");
builder.InsertField(" MERGEFIELD Name");
builder.Write(" for passing with a grade of ");
builder.InsertField(" MERGEFIELD Grade");

// Adres mektup birleştirmemizin veri kaynağı olacağı bir veri tablosu oluşturun.
DataTable table = new DataTable("ExamResults");
table.Columns.Add("Name");
table.Columns.Add("Grade");
table.Rows.Add(new object[] { "John Doe", "67" });
table.Rows.Add(new object[] { "Jane Doe", "81" });
table.Rows.Add(new object[] { "John Cardholder", "47" });
table.Rows.Add(new object[] { "Joe Bloggs", "75" });

// Veri tablosunun kendisinde değişiklik yapmadan adres mektup birleştirme verilerini değiştirmek için bir veri görünümü kullanabiliriz.
DataView view = new DataView(table);
view.Sort = "Grade DESC";
view.RowFilter = "Grade >= 50";

// Veri görünümümüz, girişleri "Derece" sütunu boyunca azalan düzende sıralar
// ve bu sütunda 50'den küçük değerlere sahip satırları filtreler.
// Çıktı belgesinin üç birleştirme belgesi içermesi için dört satırdan üçü bu ölçütlere uyar.
doc.MailMerge.Execute(view);

doc.Save(ArtifactsDir + "MailMerge.ExecuteDataView.docx");
```

### Ayrıca bakınız

* class [MailMerge](../)
* ad alanı [Aspose.Words.MailMerging](../../mailmerge/)
* toplantı [Aspose.Words](../../../)

---

## Execute(DataRow) {#execute_1}

Bir DataRow'dan belgeye adres mektup birleştirme gerçekleştirir.

```csharp
public void Execute(DataRow row)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| row | DataRow | Adres mektup birleştirme alanlarına eklenecek verileri içeren satır. Alan adları büyük/küçük harf duyarlı değildir. Belgede bulunmayan bir alan adıyla karşılaşılırsa, yok sayılır. |

### Notlar

Belgedeki adres mektup birleştirme alanlarını bir **Veri Satırı**.

Bu yöntem yok sayarRemoveUnusedRegions seçenek.

### Örnekler

DataTable'daki verilerle adres mektup birleştirmenin nasıl yürütüleceğini gösterir.

```csharp
public void ExecuteDataTable()
{
    DataTable table = new DataTable("Test");
    table.Columns.Add("CustomerName");
    table.Columns.Add("Address");
    table.Rows.Add(new object[] { "Thomas Hardy", "120 Hanover Sq., London" });
    table.Rows.Add(new object[] { "Paolo Accorti", "Via Monte Bianco 34, Torino" });

    // Aşağıda, adres mektup birleştirme için veri kaynağı olarak bir DataTable kullanmanın iki yolu bulunmaktadır.
    // 1 - Tablodaki her satır için bir çıktı adres mektup birleştirme belgesi oluşturmak üzere adres mektup birleştirme için tüm tabloyu kullanın:
    Document doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.WholeTable.docx");

    // 2 - Bir çıktı adres mektup birleştirme belgesi oluşturmak için tablonun bir satırını kullanın:
    doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table.Rows[1]);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.OneRow.docx");
}

/// <summary>
/// Adres mektup birleştirme kaynak belgesi oluşturur.
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


