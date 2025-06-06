---
title: IMailMergeDataSource Interface
linktitle: IMailMergeDataSource
articleTitle: IMailMergeDataSource
second_title: Aspose.Words for .NET
description: 使用 Aspose.Words.MailMerging.IMailMergeDataSource 解锁强大的邮件合并功能。轻松连接自定义数据源，实现无缝文档自动化。
type: docs
weight: 4500
url: /zh/net/aspose.words.mailmerging/imailmergedatasource/
---
## IMailMergeDataSource interface

实现此接口，允许从自定义数据源（例如对象列表）进行邮件合并。主从数据也受支持。

```csharp
public interface IMailMergeDataSource
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [TableName](../../aspose.words.mailmerging/imailmergedatasource/tablename/) { get; } | 返回数据源的名称。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [GetChildDataSource](../../aspose.words.mailmerging/imailmergedatasource/getchilddatasource/)(*string*) | Aspose.Words 邮件合并引擎在遇到嵌套邮件合并区域的开头时调用此方法。 |
| [GetValue](../../aspose.words.mailmerging/imailmergedatasource/getvalue/)(*string, out object*) | 返回指定字段名称的值或`错误的`如果未找到该字段。 |
| [MoveNext](../../aspose.words.mailmerging/imailmergedatasource/movenext/)() | 前进到数据源中的下一记录。 |

## 评论

创建数据源时，应将其初始化为指向 BOF（在第一条记录之前）。 Aspose.Words 邮件合并引擎将调用[`MoveNext`](./movenext/)前进到下一记录 and 然后调用[`GetValue`](./getvalue/)对于文档或当前邮件合并区域中遇到的每个合并字段。

## 例子

展示如何以自定义对象的形式执行与数据源的邮件合并。

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
/// 您的应用程序中“数据实体”类的示例。
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
 /// 您实现的自定义邮件合并数据源，以允许 Aspose.Words
/// 将客户对象中的数据通过邮件合并到 Microsoft Word 文档中。
/// </summary>
public class CustomerMailMergeDataSource : IMailMergeDataSource
{
    public CustomerMailMergeDataSource(List<Customer> customers)
    {
        mCustomers = customers;

        // 当我们初始化数据源时，它的位置必须在第一个记录之前。
        mRecordIndex = -1;
    }

    /// <summary>
    /// 数据源的名称。仅在执行可重复区域的邮件合并时由 Aspose.Words 使用。
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
                // 返回“false”给 Aspose.Words 邮件合并引擎以表示
                // 我们找不到具有此名称的字段。
                fieldValue = null;
                return false;
        }
    }

    /// <summary>
    /// 移动到集合中的下一个记录的标准实现。
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

* 命名空间 [Aspose.Words.MailMerging](../../aspose.words.mailmerging/)
* 部件 [Aspose.Words](../../)
