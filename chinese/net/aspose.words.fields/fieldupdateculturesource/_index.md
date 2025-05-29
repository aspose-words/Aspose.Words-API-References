---
title: FieldUpdateCultureSource Enum
linktitle: FieldUpdateCultureSource
articleTitle: FieldUpdateCultureSource
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Fields.FieldUpdateCultureSource。使用可自定义的文化设置控制字段更新，以增强文档准确性。
type: docs
weight: 2970
url: /zh/net/aspose.words.fields/fieldupdateculturesource/
---
## FieldUpdateCultureSource enumeration

表示在字段更新期间使用什么文化。

```csharp
public enum FieldUpdateCultureSource
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| CurrentThread | `0` | 使用当前执行线程的文化来更新字段。 |
| FieldCode | `1` | 使用通过语言设置在字段格式属性中指定的文化。 |

## 例子

展示如何在字段更新或邮件合并期间指定用于日期格式化的文化来源。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 插入两个具有德语语言环境的合并字段。
builder.Font.LocaleId = new CultureInfo("de-DE").LCID;
builder.InsertField("MERGEFIELD Date1 \\@ \"dddd, d MMMM yyyy\"");
builder.Write(" - ");
builder.InsertField("MERGEFIELD Date2 \\@ \"dddd, d MMMM yyyy\"");

// 在变量中保存其原始值后，将当前文化设置为美国英语。
CultureInfo currentCulture = Thread.CurrentThread.CurrentCulture;
Thread.CurrentThread.CurrentCulture = new CultureInfo("en-US");

// 此次合并将使用当前线程的文化来格式化日期，即美国英语。
doc.MailMerge.Execute(new[] { "Date1" }, new object[] { new DateTime(2020, 1, 01) });

// 配置下一次合并，从字段代码中获取其文化值。该文化值将为“德语”。
doc.FieldOptions.FieldUpdateCultureSource = FieldUpdateCultureSource.FieldCode;
doc.MailMerge.Execute(new[] { "Date2" }, new object[] { new DateTime(2020, 1, 01) });

// 第一个合并结果包含英文格式的日期，而第二个合并结果包含德文格式的日期。
Assert.AreEqual("Wednesday, 1 January 2020 - Mittwoch, 1 Januar 2020", doc.Range.Text.Trim());

// 恢复线程的原始文化。
Thread.CurrentThread.CurrentCulture = currentCulture;
```

### 也可以看看

* 命名空间 [Aspose.Words.Fields](../../aspose.words.fields/)
* 部件 [Aspose.Words](../../)
