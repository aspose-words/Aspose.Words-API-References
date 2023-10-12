---
title: FieldOptions.PreProcessCulture
second_title: Aspose.Words for .NET API 参考
description: FieldOptions 财产. 获取或设置区域性以预处理字段值
type: docs
weight: 170
url: /zh/net/aspose.words.fields/fieldoptions/preprocessculture/
---
## FieldOptions.PreProcessCulture property

获取或设置区域性以预处理字段值。

```csharp
public CultureInfo PreProcessCulture { get; set; }
```

### 评论

目前该属性仅影响[`FieldDocProperty`](../../fielddocproperty/)场地。

默认值为`无效的` 。当该属性设置为`无效的`， 这[`FieldDocProperty`](../../fielddocproperty/)字段的值是 preprocessed ，其区域性由[`FieldUpdateCultureSource`](../fieldupdateculturesource/)财产。

### 例子

演示如何设置预处理区域性。

```csharp
Document doc = new Document(MyDir + "Document.docx");
DocumentBuilder builder = new DocumentBuilder(doc);

// 设置区域性，某些字段将根据该区域性来格式化其显示值。
doc.FieldOptions.PreProcessCulture = new CultureInfo("de-DE");

Field field = builder.InsertField(" DOCPROPERTY CreateTime");

// DOCPROPERTY 字段将显示根据预处理区域性格式化的结果
// 我们已设置为德语。该字段将使用“dd.mm.yyyy hh:mm”格式显示日期/时间。
Assert.IsTrue(Regex.Match(field.Result, @"\d{2}[.]\d{2}[.]\d{4} \d{2}[:]\d{2}").Success);

doc.FieldOptions.PreProcessCulture = CultureInfo.InvariantCulture;
field.Update();

// 切换到固定区域性后，DOCPROPERTY 字段将使用“mm/dd/yyyy hh:mm”格式。
Assert.IsTrue(Regex.Match(field.Result, @"\d{2}[/]\d{2}[/]\d{4} \d{2}[:]\d{2}").Success);
```

### 也可以看看

* class [FieldOptions](../)
* 命名空间 [Aspose.Words.Fields](../../fieldoptions/)
* 部件 [Aspose.Words](../../../)


