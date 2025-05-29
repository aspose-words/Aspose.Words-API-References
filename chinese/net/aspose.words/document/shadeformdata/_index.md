---
title: Document.ShadeFormData
linktitle: ShadeFormData
articleTitle: ShadeFormData
second_title: Aspose.Words for .NET
description: 了解如何使用 ShadeFormData 属性通过灰色阴影增强表单可见性，从而改善用户体验和可访问性。
type: docs
weight: 400
url: /zh/net/aspose.words/document/shadeformdata/
---
## Document.ShadeFormData property

指定是否打开表单字段上的灰色阴影。

```csharp
public bool ShadeFormData { get; set; }
```

## 例子

展示如何将灰色阴影应用于表单字段。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Hello world! ");
builder.InsertTextInput("My form field", TextFormFieldType.Regular, "",
    "Text contents of form field, which are shaded in grey by default.", 0);

// 我们可以关闭灰色阴影，这样书签文本就会与其他文本混合在一起。
doc.ShadeFormData = useGreyShading;
doc.Save(ArtifactsDir + "Document.ShadeFormData.docx");
```

### 也可以看看

* class [Document](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
