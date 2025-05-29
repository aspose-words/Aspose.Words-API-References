---
title: ListLevel.DeletePictureBullet
linktitle: DeletePictureBullet
articleTitle: DeletePictureBullet
second_title: Aspose.Words for .NET
description: 使用 ListLevel DeletePictureBullet 方法，轻松从当前列表层级移除图片项目符号。立即简化您的文档格式！
type: docs
weight: 160
url: /zh/net/aspose.words.lists/listlevel/deletepicturebullet/
---
## ListLevel.DeletePictureBullet method

删除当前列表级别的图片项目符号。

```csharp
public void DeletePictureBullet()
```

## 评论

删除后将显示默认项目符号。

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
