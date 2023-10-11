---
title: FieldIncludePicture.IsLinked
second_title: Aspose.Words for .NET API 参考
description: FieldIncludePicture 财产. 获取或设置是否通过不随文档存储图形数据来减小文件大小
type: docs
weight: 30
url: /zh/net/aspose.words.fields/fieldincludepicture/islinked/
---
## FieldIncludePicture.IsLinked property

获取或设置是否通过不随文档存储图形数据来减小文件大小。

```csharp
public bool IsLinked { get; set; }
```

### 例子

演示如何使用 IMPORT 和 INCLUDEPICTURE 字段插入图像。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 下面是两个类似的字段类型，我们可以使用它们来显示从本地文件系统链接的图像。
// 1 - INCLUDEPICTURE 字段：
FieldIncludePicture fieldIncludePicture = (FieldIncludePicture)builder.InsertField(FieldType.FieldIncludePicture, true);
fieldIncludePicture.SourceFullName = ImageDir + "Transparent background logo.png";

Assert.True(Regex.Match(fieldIncludePicture.GetFieldCode(), " INCLUDEPICTURE  .*").Success);

// 应用 PNG32.FLT 过滤器。
fieldIncludePicture.GraphicFilter = "PNG32";
fieldIncludePicture.IsLinked = true;
fieldIncludePicture.ResizeHorizontally = true;
fieldIncludePicture.ResizeVertically = true;

// 2 - 导入字段：
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
* 命名空间 [Aspose.Words.Fields](../../fieldincludepicture/)
* 部件 [Aspose.Words](../../../)


