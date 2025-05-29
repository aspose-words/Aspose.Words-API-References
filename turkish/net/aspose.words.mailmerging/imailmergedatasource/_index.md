---
title: IMailMergeDataSource Interface
linktitle: IMailMergeDataSource
articleTitle: IMailMergeDataSource
second_title: .NET için Aspose.Words
description: Aspose.Words.MailMerging.IMailMergeDataSource ile güçlü e-posta birleştirmenin kilidini açın. Sorunsuz belge otomasyonu için özel veri kaynaklarını zahmetsizce bağlayın.
type: docs
weight: 4500
url: /tr/net/aspose.words.mailmerging/imailmergedatasource/
---
## IMailMergeDataSource interface

Nesnelerin listesi gibi özel bir veri kaynağından posta birleştirmeye izin vermek için bu arayüzü uygulayın. Ana-ayrıntılı veriler de desteklenir.

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
| [GetChildDataSource](../../aspose.words.mailmerging/imailmergedatasource/getchilddatasource/)(*string*) | Aspose.Words posta birleştirme motoru, iç içe geçmiş bir posta birleştirme bölgesinin başlangıcıyla karşılaştığında bu yöntemi çağırır. |
| [GetValue](../../aspose.words.mailmerging/imailmergedatasource/getvalue/)(*string, out object*) | Belirtilen alan adı için bir değer döndürür veya`YANLIŞ` alan bulunamazsa. |
| [MoveNext](../../aspose.words.mailmerging/imailmergedatasource/movenext/)() | Veri kaynağındaki bir sonraki kayda ilerler. |

## Notlar

Bir veri kaynağı oluşturulduğunda, BOF'u (ilk kayıttan önce) işaret edecek şekilde başlatılmalıdır. Aspose.Words posta birleştirme motoru çağrılacaktır[`MoveNext`](./movenext/) bir sonraki kayda geçmek için ve ardından çağır[`GetValue`](./getvalue/) belgede veya geçerli posta birleştirme bölgesinde karşılaştığı her birleştirme alanı için.

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

* ad alanı [Aspose.Words.MailMerging](../../aspose.words.mailmerging/)
* toplantı [Aspose.Words](../../)
