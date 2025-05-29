---
title: IMailMergeDataSource.GetChildDataSource
linktitle: GetChildDataSource
articleTitle: GetChildDataSource
second_title: .NET için Aspose.Words
description: IMailMergeDataSource GetChildDataSource yönteminin, iç içe geçmiş bölgeleri sorunsuz bir şekilde yöneterek Aspose.Words posta birleştirmeyi nasıl geliştirdiğini keşfedin.
type: docs
weight: 20
url: /tr/net/aspose.words.mailmerging/imailmergedatasource/getchilddatasource/
---
## IMailMergeDataSource.GetChildDataSource method

Aspose.Words posta birleştirme motoru, iç içe geçmiş bir posta birleştirme bölgesinin başlangıcıyla karşılaştığında bu yöntemi çağırır.

```csharp
public IMailMergeDataSource GetChildDataSource(string tableName)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| tableName | String | Şablon belgesinde belirtilen posta birleştirme bölgesinin adı. Büyük/küçük harfe duyarlı değildir. |

### Geri dönüş değeri

Belirtilen tablonun veri kayıtlarına erişim sağlayacak bir veri kaynağı nesnesi.

## Notlar

Aspose.Words posta birleştirme motorları bir posta birleştirme bölgesini verilerle doldurduğunda ve MERGEFIELD TableStart:TableName biçiminde iç içe geçmiş bir posta birleştirme bölgesinin başlangıcıyla karşılaştığında,`GetChildDataSource` current veri kaynağı nesnesinde. Uygulamanızın, geçerli üst kaydın child kayıtlarına erişim sağlayacak yeni bir veri kaynağı nesnesi döndürmesi gerekir. Aspose.Words, iç içe geçmiş posta birleştirme bölgesini doldurmak için döndürülen veri kaynağını kullanır.

Aşağıda, uygulamanın kuralları yer almaktadır.`GetChildDataSource` Takip etmelisin.

Bu veri kaynağı nesnesi tarafından temsil edilen tablonun belirtilen adla ilişkili bir alt (ayrıntı) tablosu varsa, uygulamanızın yeni bir değer döndürmesi gerekir.[`IMailMergeDataSource`](../) Geçerli kaydın alt kayıtlarına erişim sağlayacak nesne. Bunun bir örneği Orders / OrderDetails ilişkisidir. Geçerli kaydın alt kayıtlarına erişim sağlayacak nesne. Bunun bir örneği Orders / OrderDetails ilişkisidir.[`IMailMergeDataSource`](../) object Orders tablosunu temsil eder ve geçerli bir sipariş kaydına sahiptir. Sonra, Aspose.Words belgede "MERGEFIELD TableStart:OrderDetails" ile karşılaşır ve çağırır`GetChildDataSource` Bir tane oluşturmanız ve döndürmeniz gerekiyor[`IMailMergeDataSource`](../) Aspose.Words'ün geçerli sipariş için OrderDetails kaydına erişmesine izin verecek nesnesi.

Bu veri kaynağı nesnesinin belirtilen ada sahip tabloyla bir ilişkisi yoksa, return a[`IMailMergeDataSource`](../)belirtilen tablonun tüm kayıtlarına erişim sağlayacak nesne.

Belirtilen ada sahip bir tablo yoksa, uygulamanız şunu döndürmelidir:`hükümsüz` .

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

* interface [IMailMergeDataSource](../)
* ad alanı [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* toplantı [Aspose.Words](../../../)
