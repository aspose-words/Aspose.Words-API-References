---
title: GetChildDataSource
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words adres mektup birleştirme motoru iç içe bir adres mektup birleştirme bölgesinin başlangıcıyla karşılaştığında bu yöntemi çağırır.
type: docs
weight: 20
url: /tr/net/aspose.words.mailmerging/imailmergedatasource/getchilddatasource/
---
## IMailMergeDataSource.GetChildDataSource method

Aspose.Words adres mektup birleştirme motoru, iç içe bir adres mektup birleştirme bölgesinin başlangıcıyla karşılaştığında bu yöntemi çağırır.

```csharp
public IMailMergeDataSource GetChildDataSource(string tableName)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| tableName | String | Şablon belgesinde belirtilen adres mektup birleştirme bölgesinin adı. Büyük/küçük harfe duyarsız. |

### Geri dönüş değeri

Belirtilen tablonun veri kayıtlarına erişim sağlayacak bir veri kaynağı nesnesi.

### Notlar

Aspose.Words adres mektup birleştirme motorları bir adres mektup birleştirme bölgesini verilerle doldurduğunda ve MERGEFIELD TableStart:TableName biçiminde bir iç içe adres mektup birleştirme bölgesinin başlangıcıyla karşılaştığında,`GetChildDataSource` current veri kaynağı nesnesinde. Uygulamanızın, geçerli üst kaydın child kayıtlarına erişim sağlayacak yeni bir veri kaynağı nesnesi döndürmesi gerekiyor. Aspose.Words, iç içe adres mektup birleştirme bölgesini doldurmak için döndürülen veri kaynağını kullanır.

Aşağıda, uygulamanın`GetChildDataSource` takip etmelisin.

Bu veri kaynağı nesnesi tarafından temsil edilen tablo, belirtilen ada sahip ilgili bir alt (detay) tabloya sahipse, o zaman uygulamanızın yeni bir tablo döndürmesi gerekir.[`IMailMergeDataSource`](../../imailmergedatasource) geçerli kaydın alt kayıtlarına erişim sağlayacak nesne. Buna bir örnek Orders / OrderDetails ilişkisidir. Diyelim ki mevcut[`IMailMergeDataSource`](../../imailmergedatasource) object , Siparişler tablosunu temsil eder ve güncel bir sipariş kaydına sahiptir. Ardından, Aspose.Words belgede "MERGEFIELD TableStart:OrderDetails" ile karşılaşır ve onu çağırır`GetChildDataSource` . oluşturmanız ve döndürmeniz gerekir.[`IMailMergeDataSource`](../../imailmergedatasource) Aspose.Words'ün mevcut sipariş için OrderDetails kaydına erişmesini sağlayacak nesnesi.

Bu veri kaynağı nesnesinin belirtilen ada sahip tabloyla bir ilişkisi yoksa, o zaman a döndürmeniz gerekir.[`IMailMergeDataSource`](../../imailmergedatasource)belirtilen tablonun tüm kayıtlarına erişim sağlayacak nesne.

Belirtilen ada sahip bir tablo yoksa, uygulamanız geri dönmelidir`hükümsüz` .

### Örnekler

Özel nesne biçimindeki bir veri kaynağıyla adres mektup birleştirmenin nasıl yürütüleceğini gösterir.

```csharp
public void CustomDataSource()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);
    builder.InsertField(" MERGEFIELD FullName ");
    builder.InsertParagraph();
    builder.InsertField(" MERGEFIELD Address ");

    List<Customer> customers = new List<Customer>();
    customers.Add(new Customer("Thomas Hardy", "120 Hanover Sq., London"));
    customers.Add(new Customer("Paolo Accorti", "Via Monte Bianco 34, Torino"));

    // Özel bir nesneyi veri kaynağı olarak kullanmak için IMailMergeDataSource arabirimini uygulaması gerekir. 
    CustomerMailMergeDataSource dataSource = new CustomerMailMergeDataSource(customers);

    doc.MailMerge.Execute(dataSource);

    doc.Save(ArtifactsDir + "MailMergeCustom.CustomDataSource.docx");
}

/// <summary>
/// Uygulamanızda bir "veri varlığı" sınıfı örneği.
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
/// Aspose.Words'e izin vermek için uyguladığınız özel bir adres mektup birleştirme veri kaynağı 
/// Müşteri nesnelerinizden Microsoft Word belgelerine adres mektup birleştirme verileri.
/// </summary>
public class CustomerMailMergeDataSource : IMailMergeDataSource
{
    public CustomerMailMergeDataSource(List<Customer> customers)
    {
        mCustomers = customers;

        // Veri kaynağını başlattığımızda, konumu ilk kayıttan önce olmalıdır.
        mRecordIndex = -1;
    }

    /// <summary>
    /// Veri kaynağının adı. Aspose.Words tarafından yalnızca tekrarlanabilir bölgelerle adres mektup birleştirme yürütülürken kullanılır.
    /// </summary>
    public string TableName
    {
        get { return "Customer"; }
    }

    /// <summary>
    /// Aspose.Words, her veri alanı için bir değer almak için bu yöntemi çağırır.
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
                // Belirtmek için Aspose.Words adres mektup birleştirme motoruna "false" döndür
                // bu isimde bir alan bulamadık.
                fieldValue = null;
                return false;
        }
    }

    /// <summary>
    /// Koleksiyondaki bir sonraki kayda geçmek için standart bir uygulama.
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

* interface [IMailMergeDataSource](../../imailmergedatasource)
* ad alanı [Aspose.Words.MailMerging](../../imailmergedatasource)
* toplantı [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
