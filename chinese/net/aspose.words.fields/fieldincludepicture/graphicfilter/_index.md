---
title: FieldIncludePicture.GraphicFilter
linktitle: GraphicFilter
articleTitle: GraphicFilter
second_title: Aspose.Words for .NET
description: 发现 FieldIncludePicture GraphicFilter 属性，轻松管理图形格式过滤器，实现项目中的无缝图像集成。
type: docs
weight: 20
url: /zh/net/aspose.words.fields/fieldincludepicture/graphicfilter/
---
## FieldIncludePicture.GraphicFilter property

获取或设置要插入的图形格式的过滤器的名称。

```csharp
public string GraphicFilter { get; set; }
```

## 例子

展示如何使用 IMPORT 和 INCLUDEPICTURE 字段插入图像。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 下面是两种类似的字段类型，我们可以用它们来显示从本地文件系统链接的图像。
// 1 - INCLUDEPICTURE 字段：
FieldIncludePicture fieldIncludePicture = (FieldIncludePicture)builder.InsertField(FieldType.FieldIncludePicture, true);
fieldIncludePicture.SourceFullName = ImageDir + "Transparent background logo.png";

Assert.True(Regex.Match(fieldIncludePicture.GetFieldCode(), " INCLUDEPICTURE  .*").Success);

// 应用 PNG32.FLT 过滤器。
fieldIncludePicture.GraphicFilter = "PNG32";
fieldIncludePicture.IsLinked = true;
fieldIncludePicture.ResizeHorizontally = true;
fieldIncludePicture.ResizeVertically = true;

// 2 - IMPORT 字段：
FieldImport fieldImport = (FieldImport)builder.InsertField(FieldType.FieldImport, true);
fieldImport.SourceFullName = ImageDir + "Transparent background logo.png";
fieldImport.GraphicFilter = "PNG32";
fieldImport.IsLinked = true;

Assert.True(Regex.Match(fieldImport.GetFieldCode(), " IMPORT  .* \\\\c PNG32 \\\\d").Success);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.IMPORT.INCLUDEPICTURE.docx");
```

### 也可以看看

* class [FieldIncludePicture](../)
* 命名空间 [Aspose.Words.Fields](../../../aspose.words.fields/)
* 部件 [Aspose.Words](../../../)
