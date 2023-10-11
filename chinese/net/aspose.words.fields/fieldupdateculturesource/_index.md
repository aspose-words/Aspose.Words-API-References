---
title: Enum FieldUpdateCultureSource
second_title: Aspose.Words for .NET API 参考
description: Aspose.Words.Fields.FieldUpdateCultureSource 枚举. 指示字段更新期间使用的区域性
type: docs
weight: 2560
url: /zh/net/aspose.words.fields/fieldupdateculturesource/
---
## FieldUpdateCultureSource enumeration

指示字段更新期间使用的区域性。

```csharp
public enum FieldUpdateCultureSource
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| CurrentThread | `0` | 当前执行线程的区域性用于更新字段。 |
| FieldCode | `1` | 使用通过语言设置在字段格式属性中指定的区域性。 |

### 例子

演示如何在字段更新或邮件合并期间指定用于日期格式设置的区域性来源。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 插入两个具有德语区域设置的合并字段。
builder.Font.LocaleId = new CultureInfo("de-DE").LCID;
builder.InsertField("MERGEFIELD Date1 \\@ \"dddd, d MMMM yyyy\"");
builder.Write(" - ");
builder.InsertField("MERGEFIELD Date2 \\@ \"dddd, d MMMM yyyy\"");

// 在变量中保留其原始值后，将当前区域性设置为美国英语。
CultureInfo currentCulture = Thread.CurrentThread.CurrentCulture;
Thread.CurrentThread.CurrentCulture = new CultureInfo("en-US");

// 此合并将使用当前线程的区域性来格式化日期，美国英语。
doc.MailMerge.Execute(new[] { "Date1" }, new object[] { new DateTime(2020, 1, 01) });

// 配置下一个合并以从字段代码中获取其区域性值。这种文化的价值将是德国的。
doc.FieldOptions.FieldUpdateCultureSource = FieldUpdateCultureSource.FieldCode;
doc.MailMerge.Execute(new[] { "Date2" }, new object[] { new DateTime(2020, 1, 01) });

// 第一个合并结果包含英语格式的日期，而第二个则包含德语格式的日期。
Assert.AreEqual("Wednesday, 1 January 2020 - Mittwoch, 1 Januar 2020", doc.Range.Text.Trim());

// 恢复线程的原始文化。
Thread.CurrentThread.CurrentCulture = currentCulture;
```

### 也可以看看

* 命名空间 [Aspose.Words.Fields](../../aspose.words.fields/)
* 部件 [Aspose.Words](../../)


