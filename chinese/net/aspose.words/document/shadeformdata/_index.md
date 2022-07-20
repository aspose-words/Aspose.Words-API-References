---
title: ShadeFormData
second_title: Aspose.Words for .NET API 参考
description: 指定是否开启表单域的灰色阴影
type: docs
weight: 360
url: /zh/net/aspose.words/document/shadeformdata/
---
## Document.ShadeFormData property

指定是否开启表单域的灰色阴影。

```csharp
public bool ShadeFormData { get; set; }
```

### 例子

显示如何将灰色阴影应用于表单域。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Hello world! ");
builder.InsertTextInput("My form field", TextFormFieldType.Regular, "",
    "Text contents of form field, which are shaded in grey by default.", 0);

// 我们可以关闭灰色阴影，这样带书签的文本将与其他文本融为一体。
doc.ShadeFormData = useGreyShading;
doc.Save(ArtifactsDir + "Document.ShadeFormData.docx");
```

### 也可以看看

* class [Document](../../document)
* 命名空间 [Aspose.Words](../../document)
* 部件 [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->