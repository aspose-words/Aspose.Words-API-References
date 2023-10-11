---
title: IMailMergeDataSource.TableName
second_title: Aspose.Words for .NET API Referansı
description: IMailMergeDataSource mülk. Veri kaynağının adını döndürür.
type: docs
weight: 10
url: /tr/net/aspose.words.mailmerging/imailmergedatasource/tablename/
---
## IMailMergeDataSource.TableName property

Veri kaynağının adını döndürür.

```csharp
public string TableName { get; }
```

### Geri dönüş değeri

Veri kaynağının adı. Veri kaynağının adı yoksa dizeyi boşaltın.

### Notlar

Eğer uyguluyorsanız[`IMailMergeDataSource`](../), bu özellikten data kaynağının adını döndürün.

Aspose.Words bu adı, şablon belgede belirtilen adres-mektup birleştirme bölgesi adıyla eşleştirmek için kullanır. Veri kaynağı adı ile adres-mektup birleştirme bölgesi adı arasındaki karşılaştırma büyük/küçük harfe duyarlı değildir.

### Örnekler

Özel nesne biçimindeki bir veri kaynağıyla adres-mektup birleştirmenin nasıl yürütüleceğini gösterir.

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
/// Uygulamanızdaki "veri varlığı" sınıfına bir örnek.
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
 /// Aspose.Words'e izin vermek için uyguladığınız özel bir adres-mektup birleştirme veri kaynağı
/// Müşteri nesnelerinizdeki posta birleştirme verilerini Microsoft Word belgelerine aktarmak için.
/// </summary>
public class CustomerMailMergeDataSource : IMailMergeDataSource
{
    public CustomerMailMergeDataSource(List<Customer> customers)
    {
        mCustomers = customers;

        // Veri kaynağını başlattığımızda konumu ilk kayıttan önce olmalıdır.
        mRecordIndex = -1;
    }

    /// <summary>
    /// Veri kaynağının adı. Aspose.Words tarafından yalnızca tekrarlanabilir bölgelerle adres-mektup birleştirme yürütülürken kullanılır.
    /// </summary>
    public string TableName
    {
        get { return "Customer"; }
    }

    /// <summary>
    /// Aspose.Words her veri alanı için bir değer elde etmek amacıyla bu yöntemi çağırır.
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
                // Aspose.Words adres-mektup birleştirme motoruna şunu belirtmek için "yanlış" değerini döndürün
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

* interface [IMailMergeDataSource](../)
* ad alanı [Aspose.Words.MailMerging](../../imailmergedatasource/)
* toplantı [Aspose.Words](../../../)


