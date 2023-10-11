---
title: Fill.SetImage
second_title: Aspose.Words for .NET API 参考
description: Fill 方法. 将填充类型更改为单个图像
type: docs
weight: 250
url: /zh/net/aspose.words.drawing/fill/setimage/
---
## SetImage(string) {#setimage_2}

将填充类型更改为单个图像。

```csharp
public void SetImage(string fileName)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| fileName | String | 图像文件的路径。 |

### 例子

演示如何将形状填充类型设置为图像。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 设置图像有多种方法。
Shape shape = builder.InsertShape(ShapeType.Rectangle, 80, 80);
// 1 - 使用本地系统文件名：
shape.Fill.SetImage(ImageDir + "Logo.jpg");
doc.Save(ArtifactsDir + "Shape.FillImage.FileName.docx");

// 2 - 将文件加载到字节数组中：
shape.Fill.SetImage(File.ReadAllBytes(ImageDir + "Logo.jpg"));
doc.Save(ArtifactsDir + "Shape.FillImage.ByteArray.docx");

// 3 - 来自流：
using (FileStream stream = new FileStream(ImageDir + "Logo.jpg", FileMode.Open))
    shape.Fill.SetImage(stream);
doc.Save(ArtifactsDir + "Shape.FillImage.Stream.docx");
```

### 也可以看看

* class [Fill](../)
* 命名空间 [Aspose.Words.Drawing](../../fill/)
* 部件 [Aspose.Words](../../../)

---

## SetImage(Stream) {#setimage_1}

将填充类型更改为单个图像。

```csharp
public void SetImage(Stream stream)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| stream | Stream | 包含图像字节的流。 |

### 也可以看看

* class [Fill](../)
* 命名空间 [Aspose.Words.Drawing](../../fill/)
* 部件 [Aspose.Words](../../../)

---

## SetImage(byte[]) {#setimage}

将填充类型更改为单个图像。

```csharp
public void SetImage(byte[] imageBytes)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| imageBytes | Byte[] | 图像字节数组。 |

### 也可以看看

* class [Fill](../)
* 命名空间 [Aspose.Words.Drawing](../../fill/)
* 部件 [Aspose.Words](../../../)


