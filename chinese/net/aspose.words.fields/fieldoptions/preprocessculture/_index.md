---
title: FieldOptions.PreProcessCulture
linktitle: PreProcessCulture
articleTitle: PreProcessCulture
second_title: Aspose.Words for .NET
description: 了解 FieldOptions PreProcessCulture 如何通过自定义字段值文化来增强数据处理，从而提高准确性和效率。
type: docs
weight: 170
url: /zh/net/aspose.words.fields/fieldoptions/preprocessculture/
---
## FieldOptions.PreProcessCulture property

获取或设置文化以预处理字段值。

```csharp
public CultureInfo PreProcessCulture { get; set; }
```

## 评论

目前此属性仅影响[`FieldDocProperty`](../../fielddocproperty/)场地。

默认值为`无效的` 。当此属性设置为`无效的`， 这[`FieldDocProperty`](../../fielddocproperty/)字段的值是 preprocessed ，其文化由[`FieldUpdateCultureSource`](../fieldupdateculturesource/)财产。

## 例子

展示如何设置预处理文化。

```csharp
Document doc = new Document(MyDir + "Document.docx");
DocumentBuilder builder = new DocumentBuilder(doc);

// 设置某些字段将根据其格式化其显示值的文化。
doc.FieldOptions.PreProcessCulture = new CultureInfo("de-DE");

Field field = builder.InsertField(" DOCPROPERTY CreateTime");

// DOCPROPERTY 字段将根据预处理文化显示其格式化的结果
// 我们已设置为德语。该字段将使用“dd.mm.yyyy hh:mm”格式显示日期/时间。
Assert.IsTrue(Regex.Match(field.Result, @"\d{2}[.]\d{2}[.]\d{4} \d{2}[:]\d{2}").Success);

doc.FieldOptions.PreProcessCulture = CultureInfo.InvariantCulture;
field.Update();

// 切换到不变文化后，DOCPROPERTY 字段将使用“mm/dd/yyyy hh:mm”格式。
Assert.IsTrue(Regex.Match(field.Result, @"\d{2}[/]\d{2}[/]\d{4} \d{2}[:]\d{2}").Success);
```

### 也可以看看

* class [FieldOptions](../)
* 命名空间 [Aspose.Words.Fields](../../../aspose.words.fields/)
* 部件 [Aspose.Words](../../../)
