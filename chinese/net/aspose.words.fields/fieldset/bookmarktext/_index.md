---
title: FieldSet.BookmarkText
linktitle: BookmarkText
articleTitle: BookmarkText
second_title: Aspose.Words for .NET
description: 了解如何轻松管理 FieldSet BookmarkText 属性以自定义和增强您的书签，从而实现更好的组织和可访问性。
type: docs
weight: 30
url: /zh/net/aspose.words.fields/fieldset/bookmarktext/
---
## FieldSet.BookmarkText property

获取或设置书签的新文本。

```csharp
public string BookmarkText { get; set; }
```

## 例子

展示如何使用 SET 字段创建书签文本，然后使用 REF 字段将其显示在文档中。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

 // 使用 SET 字段命名书签文本。
// 该字段指的是“书签”，而不是文本中出现的书签结构，而是一个命名变量。
FieldSet fieldSet = (FieldSet)builder.InsertField(FieldType.FieldSet, false);
fieldSet.BookmarkName = "MyBookmark";
fieldSet.BookmarkText = "Hello world!";
fieldSet.Update();

Assert.AreEqual(" SET  MyBookmark \"Hello world!\"", fieldSet.GetFieldCode());

// 在 REF 字段中按名称引用书签并显示其内容。
FieldRef fieldRef = (FieldRef)builder.InsertField(FieldType.FieldRef, true);
fieldRef.BookmarkName = "MyBookmark";
fieldRef.Update();

Assert.AreEqual(" REF  MyBookmark", fieldRef.GetFieldCode());
Assert.AreEqual("Hello world!", fieldRef.Result);

doc.Save(ArtifactsDir + "Field.SET.REF.docx");
```

### 也可以看看

* class [FieldSet](../)
* 命名空间 [Aspose.Words.Fields](../../../aspose.words.fields/)
* 部件 [Aspose.Words](../../../)
