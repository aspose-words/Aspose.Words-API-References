---
title: Document.ShadeFormData
second_title: Aspose.Words for .NET API 参考
description: Document 财产. 指定是否打开表单字段上的灰色底纹
type: docs
weight: 380
url: /zh/net/aspose.words/document/shadeformdata/
---
## Document.ShadeFormData property

指定是否打开表单字段上的灰色底纹。

```csharp
public bool ShadeFormData { get; set; }
```

### 例子

演示如何将灰色底纹应用到表单字段。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Hello world! ");
builder.InsertTextInput("My form field", TextFormFieldType.Regular, "",
    "Text contents of form field, which are shaded in grey by default.", 0);

// 我们可以关闭灰色阴影，这样加书签的文本就会与其他文本混合在一起。
doc.ShadeFormData = useGreyShading;
doc.Save(ArtifactsDir + "Document.ShadeFormData.docx");
```

### 也可以看看

* class [Document](../)
* 命名空间 [Aspose.Words](../../document/)
* 部件 [Aspose.Words](../../../)


