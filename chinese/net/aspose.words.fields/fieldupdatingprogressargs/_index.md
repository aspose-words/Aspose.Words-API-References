---
title: FieldUpdatingProgressArgs Class
linktitle: FieldUpdatingProgressArgs
articleTitle: FieldUpdatingProgressArgs
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Fields.FieldUpdatingProgressArgs 类，它通过提供字段进度的实时更新来增强文档自动化。
type: docs
weight: 2980
url: /zh/net/aspose.words.fields/fieldupdatingprogressargs/
---
## FieldUpdatingProgressArgs class

为字段更新进度事件提供数据。

```csharp
public sealed class FieldUpdatingProgressArgs
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [TotalFieldsCount](../../aspose.words.fields/fieldupdatingprogressargs/totalfieldscount/) { get; } | 获取要更新的字段总数。 |
| [UpdateCompleted](../../aspose.words.fields/fieldupdatingprogressargs/updatecompleted/) { get; } | 获取字段更新是否完成的值。 |
| [UpdatedFieldsCount](../../aspose.words.fields/fieldupdatingprogressargs/updatedfieldscount/) { get; } | 获取更新字段的数量。 |

## 例子

展示如何在字段更新期间使用回调方法。

```csharp
public void FieldUpdatingCallbackTest()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.InsertField(" DATE \\@ \"dddd, d MMMM yyyy\" ");
    builder.InsertField(" TIME ");
    builder.InsertField(" REVNUM ");
    builder.InsertField(" AUTHOR  \"John Doe\" ");
    builder.InsertField(" SUBJECT \"My Subject\" ");
    builder.InsertField(" QUOTE \"Hello world!\" ");

    FieldUpdatingCallback callback = new FieldUpdatingCallback();
    doc.FieldOptions.FieldUpdatingCallback = callback;

    doc.UpdateFields();

    Assert.True(callback.FieldUpdatedCalls.Contains("Updating John Doe"));
}

/// <summary>
/// 如果您希望在字段更新期间调用自己的自定义方法，请实现此接口。
/// </summary>
public class FieldUpdatingCallback : IFieldUpdatingCallback, IFieldUpdatingProgressCallback
{
    public FieldUpdatingCallback()
    {
        FieldUpdatedCalls = new List<string>();
    }

    /// <summary>
    /// 在字段更新之前调用的用户定义方法。
    /// </summary>
    void IFieldUpdatingCallback.FieldUpdating(Field field)
    {
        if (field.Type == FieldType.FieldAuthor)
        {
            FieldAuthor fieldAuthor = (FieldAuthor) field;
            fieldAuthor.AuthorName = "Updating John Doe";
        }
    }

    /// <summary>
    /// 在字段更新后立即调用的用户定义方法。
    /// </summary>
    void IFieldUpdatingCallback.FieldUpdated(Field field)
    {
        FieldUpdatedCalls.Add(field.Result);
    }

    void IFieldUpdatingProgressCallback.Notify(FieldUpdatingProgressArgs args)
    {
        Console.WriteLine($"{args.UpdateCompleted}/{args.TotalFieldsCount}");
        Console.WriteLine($"{args.UpdatedFieldsCount}");
    }

    public IList<string> FieldUpdatedCalls { get; }
}
```

### 也可以看看

* 命名空间 [Aspose.Words.Fields](../../aspose.words.fields/)
* 部件 [Aspose.Words](../../)
