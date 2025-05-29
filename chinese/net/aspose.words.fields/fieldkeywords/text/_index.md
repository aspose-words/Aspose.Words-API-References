---
title: FieldKeywords.Text
linktitle: Text
articleTitle: Text
second_title: Aspose.Words for .NET
description: 轻松管理您的 FieldKeywords！访问并自定义关键字文本，以获得最佳 SEO 效果并增强可见性。
type: docs
weight: 20
url: /zh/net/aspose.words.fields/fieldkeywords/text/
---
## FieldKeywords.Text property

获取或设置关键字的文本。

```csharp
public string Text { get; set; }
```

## 例子

显示插入 KEYWORDS 字段。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 在文件资源管理器中添加一些关键字，也称为“标签”。
doc.BuiltInDocumentProperties.Keywords = "Keyword1, Keyword2";

// KEYWORDS 字段显示此属性的值。
FieldKeywords field = (FieldKeywords)builder.InsertField(FieldType.FieldKeyword, true);
field.Update();

Assert.AreEqual(" KEYWORDS ", field.GetFieldCode());
Assert.AreEqual("Keyword1, Keyword2", field.Result);

// 为字段的 Text 属性设置一个值，
// 然后更新字段也会用新值覆盖相应的内置属性。
field.Text = "OverridingKeyword";
field.Update();

Assert.AreEqual(" KEYWORDS  OverridingKeyword", field.GetFieldCode());
Assert.AreEqual("OverridingKeyword", field.Result);
Assert.AreEqual("OverridingKeyword", doc.BuiltInDocumentProperties.Keywords);

doc.Save(ArtifactsDir + "Field.KEYWORDS.docx");
```

### 也可以看看

* class [FieldKeywords](../)
* 命名空间 [Aspose.Words.Fields](../../../aspose.words.fields/)
* 部件 [Aspose.Words](../../../)
