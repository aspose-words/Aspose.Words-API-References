---
title: DocSaveOptions.SavePictureBullet
linktitle: SavePictureBullet
articleTitle: SavePictureBullet
second_title: Aspose.Words for .NET
description: 了解 DocSaveOptions 的 SavePictureBullet 属性如何增强您的文档输出效果。轻松控制 PictureBullet 数据保存，获得最佳效果。
type: docs
weight: 60
url: /zh/net/aspose.words.saving/docsaveoptions/savepicturebullet/
---
## DocSaveOptions.SavePictureBullet property

当`错误的` ，PictureBullet 数据未保存到输出文档。 默认值为`真的`.

```csharp
public bool SavePictureBullet { get; set; }
```

## 评论

该选项是为 Word 97 提供的，它无法正确处理 PictureBullet 数据。 要删除 PictureBullet 数据，请将该选项设置为“false”。

## 例子

展示如何在保存时从文档中省略 PictureBullet 数据。

```csharp
Document doc = new Document(MyDir + "Image bullet points.docx");
// 某些文字处理器（例如 Microsoft Word 97）与 PictureBullet 数据不兼容。
// 通过在 SaveOptions 对象中设置一个标志，
// 我们可以在保存时将所有图像项目符号转换为普通项目符号。
DocSaveOptions saveOptions = new DocSaveOptions(SaveFormat.Doc);
saveOptions.SavePictureBullet = false;

doc.Save(ArtifactsDir + "DocSaveOptions.PictureBullets.doc", saveOptions);
```

### 也可以看看

* class [DocSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
