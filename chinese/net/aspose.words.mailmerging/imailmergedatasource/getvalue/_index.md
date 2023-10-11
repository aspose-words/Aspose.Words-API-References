---
title: IMailMergeDataSource.GetValue
second_title: Aspose.Words for .NET API 参考
description: IMailMergeDataSource 方法. 返回指定字段名称的值或错误的如果未找到该字段.
type: docs
weight: 30
url: /zh/net/aspose.words.mailmerging/imailmergedatasource/getvalue/
---
## IMailMergeDataSource.GetValue method

返回指定字段名称的值或`错误的`如果未找到该字段.

```csharp
public bool GetValue(string fieldName, out object fieldValue)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| fieldName | String | 数据字段的名称。 |
| fieldValue | Object& | 返回字段值。 |

### 返回值

`真的`如果找到值。

### 例子

演示如何使用自定义对象形式的数据源执行邮件合并。

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

     // 要使用自定义对象作为数据源，它必须实现 IMailMergeDataSource 接口。
    CustomerMailMergeDataSource dataSource = new CustomerMailMergeDataSource(customers);

    doc.MailMerge.Execute(dataSource);

    doc.Save(ArtifactsDir + "MailMergeCustom.CustomDataSource.docx");
}

/// <summary>
/// 应用程序中“数据实体”类的示例。
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
 /// 您实现的自定义邮件合并数据源以允许 Aspose.Words
/// 将客户对象中的数据通过邮件合并到 Microsoft Word 文档中。
/// </summary>
public class CustomerMailMergeDataSource : IMailMergeDataSource
{
    public CustomerMailMergeDataSource(List<Customer> customers)
    {
        mCustomers = customers;

        // 当我们初始化数据源时，它的位置必须在第一条记录之前。
        mRecordIndex = -1;
    }

    /// <summary>
    /// 数据源的名称。仅在对可重复区域执行邮件合并时由 Aspose.Words 使用。
    /// </summary>
    public string TableName
    {
        get { return "Customer"; }
    }

    /// <summary>
    /// Aspose.Words 调用此方法来获取每个数据字段的值。
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
                // 返回“false”给Aspose.Words邮件合并引擎来表示
                // 我们找不到具有该名称的字段。
                fieldValue = null;
                return false;
        }
    }

    /// <summary>
    /// 移动到集合中下一条记录的标准实现。
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

### 也可以看看

* interface [IMailMergeDataSource](../)
* 命名空间 [Aspose.Words.MailMerging](../../imailmergedatasource/)
* 部件 [Aspose.Words](../../../)


