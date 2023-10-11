---
title: Interface IMailMergeDataSource
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.MailMerging.IMailMergeDataSource arayüz. Nesne listesi gibi özel bir veri kaynağından adresmektup birleştirmeye izin vermek için bu arayüzü uygulayın. Ana detay verileri de desteklenmektedir.
type: docs
weight: 3810
url: /tr/net/aspose.words.mailmerging/imailmergedatasource/
---
## IMailMergeDataSource interface

Nesne listesi gibi özel bir veri kaynağından adres-mektup birleştirmeye izin vermek için bu arayüzü uygulayın. Ana detay verileri de desteklenmektedir.

```csharp
public interface IMailMergeDataSource
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [TableName](../../aspose.words.mailmerging/imailmergedatasource/tablename/) { get; } | Veri kaynağının adını döndürür. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [GetChildDataSource](../../aspose.words.mailmerging/imailmergedatasource/getchilddatasource/)(string) | Aspose.Words adres-mektup birleştirme motoru, iç içe adres-mektup birleştirme bölgesinin başlangıcıyla karşılaştığında bu yöntemi çağırır. |
| [GetValue](../../aspose.words.mailmerging/imailmergedatasource/getvalue/)(string, out object) | Belirtilen alan adı için bir değer döndürür veya`YANLIŞ` alan bulunamazsa. |
| [MoveNext](../../aspose.words.mailmerging/imailmergedatasource/movenext/)() | Veri kaynağındaki bir sonraki kayda ilerler. |

### Notlar

Bir veri kaynağı oluşturulduğunda, BOF'u işaret edecek şekilde başlatılmalıdır (ilk kayıttan önce). Aspose.Words adres-mektup birleştirme motoru,[`MoveNext`](./movenext/) sonraki kayda ilerlemek için and ardından çağırın[`GetValue`](./getvalue/) belgede veya geçerli adres-mektup birleştirme bölgesinde karşılaştığı her birleştirme alanı için.

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

* ad alanı [Aspose.Words.MailMerging](../../aspose.words.mailmerging/)
* toplantı [Aspose.Words](../../)


