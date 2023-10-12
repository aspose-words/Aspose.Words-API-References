---
title: Interface IFieldUpdatingCallback
second_title: Aspose.Words for .NET API 参考
description: Aspose.Words.Fields.IFieldUpdatingCallback 界面. 如果您想在字段更新期间调用自己的自定义方法请实现此接口
type: docs
weight: 2720
url: /zh/net/aspose.words.fields/ifieldupdatingcallback/
---
## IFieldUpdatingCallback interface

如果您想在字段更新期间调用自己的自定义方法，请实现此接口。

```csharp
public interface IFieldUpdatingCallback
```

## 方法

| 姓名 | 描述 |
| --- | --- |
| [FieldUpdated](../../aspose.words.fields/ifieldupdatingcallback/fieldupdated/)(Field) | 更新字段后立即调用的用户定义方法。 |
| [FieldUpdating](../../aspose.words.fields/ifieldupdatingcallback/fieldupdating/)(Field) | 在更新字段之前调用的用户定义方法。 |

### 例子

演示如何在字段更新期间使用回调方法。

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
/// 如果您想在字段更新期间调用您自己的自定义方法，请实现此接口。
/// </summary>
public class FieldUpdatingCallback : IFieldUpdatingCallback, IFieldUpdatingProgressCallback
{
    public FieldUpdatingCallback()
    {
        FieldUpdatedCalls = new List<string>();
    }

    /// <summary>
    /// 在更新字段之前调用的用户定义方法。
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
    /// 更新字段后调用的用户定义方法。
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


