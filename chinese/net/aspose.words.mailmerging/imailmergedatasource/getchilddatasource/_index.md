---
title: IMailMergeDataSource.GetChildDataSource
linktitle: GetChildDataSource
articleTitle: GetChildDataSource
second_title: 用于 .NET 的 Aspose.Words
description: IMailMergeDataSource GetChildDataSource 方法. Aspose.Words 邮件合并引擎在遇到嵌套邮件合并区域的开头时调用此方法 在 C#.
type: docs
weight: 20
url: /zh/net/aspose.words.mailmerging/imailmergedatasource/getchilddatasource/
---
## IMailMergeDataSource.GetChildDataSource method

Aspose.Words 邮件合并引擎在遇到嵌套邮件合并区域的开头时调用此方法。

```csharp
public IMailMergeDataSource GetChildDataSource(string tableName)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| tableName | String | 模板文档中指定的邮件合并区域的名称。不区分大小写。 |

### 返回值

将提供对指定表的数据记录的访问的数据源对象。

## 评论

当 Aspose.Words 邮件合并引擎用数据填充邮件合并区域并遇到 MERGEFIELD TableStart:TableName 形式的nested 邮件合并区域的开头时，它会调用`GetChildDataSource`在 current 数据源对象上。您的实现需要返回一个新的数据源对象，该对象将提供对当前父记录的 child 记录的访问。 Aspose.Words 将使用返回的数据源填充嵌套邮件合并区域。

下面是执行的规则`GetChildDataSource`必须遵循.

如果此数据源对象表示的表具有指定名称的相关子（详细信息）表， 那么您的实现需要返回一个新的[`IMailMergeDataSource`](../)将为当前记录的子记录提供 access 的对象。 的一个示例是 Orders / OrderDetails 关系。我们假设当前[`IMailMergeDataSource`](../)object 表示订单表，它有当前订单记录。接下来，Aspose.Words 在文档中遇到“MERGEFIELD TableStart:OrderDetails” 并调用`GetChildDataSource`。您需要创建并返回一个[`IMailMergeDataSource`](../) 对象将允许 Aspose.Words 访问当前订单的 OrderDetails 记录。

如果此数据源对象与指定名称的表没有关系，则需要返回 a[`IMailMergeDataSource`](../)将提供对指定表的所有记录的访问的对象。

如果指定名称的表不存在，您的实现应该返回`无效的`.

## 例子

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
* 命名空间 [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* 部件 [Aspose.Words](../../../)
