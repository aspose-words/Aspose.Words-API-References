---
title: IFieldUpdatingCallback.FieldUpdated
second_title: Aspose.Words for .NET API 参考
description: IFieldUpdatingCallback 方法. 在字段更新后立即调用的用户定义方法
type: docs
weight: 10
url: /zh/net/aspose.words.fields/ifieldupdatingcallback/fieldupdated/
---
## IFieldUpdatingCallback.FieldUpdated method

在字段更新后立即调用的用户定义方法。

```csharp
public void FieldUpdated(Field field)
```

### 例子

展示如何在字段更新期间使用回调方法。

```csharp
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
/// 如果您想在字段更新期间调用自己的自定义方法，请实现此接口。
/// </summary>
public class FieldUpdatingCallback : IFieldUpdatingCallback
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

    public IList<string> FieldUpdatedCalls { get; }
}
```

### 也可以看看

* class [Field](../../field/)
* interface [IFieldUpdatingCallback](../)
* 命名空间 [Aspose.Words.Fields](../../ifieldupdatingcallback/)
* 部件 [Aspose.Words](../../../)


