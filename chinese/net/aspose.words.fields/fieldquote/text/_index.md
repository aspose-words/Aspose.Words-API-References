---
title: FieldQuote.Text
linktitle: Text
articleTitle: Text
second_title: 用于 .NET 的 Aspose.Words
description: FieldQuote Text 财产. 获取或设置要检索的文本 在 C#.
type: docs
weight: 20
url: /zh/net/aspose.words.fields/fieldquote/text/
---
## FieldQuote.Text property

获取或设置要检索的文本。

```csharp
public string Text { get; set; }
```

## 例子

显示使用 QUOTE 字段。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 插入一个 QUOTE 字段，该字段将显示其 Text 属性的值。
FieldQuote field = (FieldQuote)builder.InsertField(FieldType.FieldQuote, true);
field.Text = "\"Quoted text\"";

Assert.AreEqual(" QUOTE  \"\\\"Quoted text\\\"\"", field.GetFieldCode());

// 插入一个 QUOTE 字段并在其中嵌套一个 DATE 字段。
// 每次我们使用 Microsoft Word 打开文档时，DATE 字段都会将其值更新为当前日期。
// 像这样将 DATE 字段嵌套在 QUOTE 字段中将冻结其值
// 到我们创建文档的日期。
builder.Write("\nDocument creation date: ");
field = (FieldQuote)builder.InsertField(FieldType.FieldQuote, true);
builder.MoveTo(field.Separator);
builder.InsertField(FieldType.FieldDate, true);

Assert.AreEqual(" QUOTE \u0013 DATE \u0014" + DateTime.Now.Date.ToShortDateString() + "\u0015", field.GetFieldCode());

// 更新所有字段以显示正确的结果。
doc.UpdateFields();

Assert.AreEqual("\"Quoted text\"", doc.Range.Fields[0].Result);

doc.Save(ArtifactsDir + "Field.QUOTE.docx");
```

### 也可以看看

* class [FieldQuote](../)
* 命名空间 [Aspose.Words.Fields](../../../aspose.words.fields/)
* 部件 [Aspose.Words](../../../)
