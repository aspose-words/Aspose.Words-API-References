---
title: IMailMergeDataSource
second_title: Aspose.Words for .NET API Referansı
description: Nesne listesi gibi özel bir veri kaynağından adres mektup birleştirmeye izin vermek için bu arabirimi uygulayın. Ana ayrıntı verileri de desteklenir.
type: docs
weight: 3590
url: /tr/net/aspose.words.mailmerging/imailmergedatasource/
---
## IMailMergeDataSource interface

Nesne listesi gibi özel bir veri kaynağından adres mektup birleştirmeye izin vermek için bu arabirimi uygulayın. Ana ayrıntı verileri de desteklenir.

```csharp
public interface IMailMergeDataSource
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [TableName](../../aspose.words.mailmerging/imailmergedatasource/tablename) { get; } | Veri kaynağının adını döndürür. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [GetChildDataSource](../../aspose.words.mailmerging/imailmergedatasource/getchilddatasource)(string) | Aspose.Words adres mektup birleştirme motoru, iç içe bir adres mektup birleştirme bölgesinin başlangıcıyla karşılaştığında bu yöntemi çağırır. |
| [GetValue](../../aspose.words.mailmerging/imailmergedatasource/getvalue)(string, out object) | Belirtilen alan adı için bir değer döndürür veya alan bulunamazsa false döndürür. |
| [MoveNext](../../aspose.words.mailmerging/imailmergedatasource/movenext)() | Veri kaynağındaki bir sonraki kayda ilerler. |

### Notlar

Bir veri kaynağı oluşturulduğunda, BOF'a işaret edecek şekilde başlatılmalıdır (ilk kayıttan önce). Aspose.Words adres mektup birleştirme motoru çalıştırılacaktır.[`MoveNext`](./movenext) sonraki kayda ilerlemek için and ve ardından çağırmak için[`GetValue`](./getvalue) belgede veya geçerli adres mektup birleştirme bölgesinde karşılaştığı her birleştirme alanı için.

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

* ad alanı [Aspose.Words.MailMerging](../../aspose.words.mailmerging)
* toplantı [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
