---
title: ListLevel.CreatePictureBullet
linktitle: CreatePictureBullet
articleTitle: CreatePictureBullet
second_title: Aspose.Words for .NET
description: 探索 ListLevel CreatePictureBullet 方法，轻松使用自定义图片项目符号增强列表，增加视觉吸引力和清晰度。
type: docs
weight: 150
url: /zh/net/aspose.words.lists/listlevel/createpicturebullet/
---
## ListLevel.CreatePictureBullet method

为当前列表级别创建图片项目符号形状。

```csharp
public void CreatePictureBullet()
```

## 评论

请注意，[`NumberStyle`](../numberstyle/)将设置为Bulletand [`NumberFormat`](../numberformat/)到“\xF0B7”以正确显示图片项目符号。 红十字图像将在创建时设置为图片项目符号图像。 要更改它请使用[`ImageData`](../imagedata/)。

## 例子

展示如何为列表项标签设置自定义图像图标。

```csharp
Document doc = new Document();

List list = doc.Lists.Add(ListTemplate.BulletCircle);

// 为当前列表级别创建图片项目符号，并从本地文件系统设置图像
// 作为此列表级别的项目符号将显示的图标。
list.ListLevels[0].CreatePictureBullet();
list.ListLevels[0].ImageData.SetImage(ImageDir + "Logo icon.ico");

Assert.IsTrue(list.ListLevels[0].ImageData.HasImage);

DocumentBuilder builder = new DocumentBuilder(doc);

builder.ListFormat.List = list;
builder.Writeln("Hello world!");
builder.Write("Hello again!");

doc.Save(ArtifactsDir + "Lists.CreatePictureBullet.docx");

list.ListLevels[0].DeletePictureBullet();

Assert.IsNull(list.ListLevels[0].ImageData);
```

### 也可以看看

* class [ListLevel](../)
* 命名空间 [Aspose.Words.Lists](../../../aspose.words.lists/)
* 部件 [Aspose.Words](../../../)
