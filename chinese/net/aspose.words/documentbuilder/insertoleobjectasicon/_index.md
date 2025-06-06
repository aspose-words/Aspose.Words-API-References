---
title: DocumentBuilder.InsertOleObjectAsIcon
linktitle: InsertOleObjectAsIcon
articleTitle: InsertOleObjectAsIcon
second_title: Aspose.Words for .NET
description: 使用 DocumentBuilder 轻松将 OLE 对象作为图标插入文档。自定义图标和标题，确保无缝集成。
type: docs
weight: 430
url: /zh/net/aspose.words/documentbuilder/insertoleobjectasicon/
---
## InsertOleObjectAsIcon(*string, bool, string, string*) {#insertoleobjectasicon_1}

将嵌入或链接的 OLE 对象作为图标插入文档。 允许指定图标文件和标题。使用文件扩展名检测 OLE 对象类型。

```csharp
public Shape InsertOleObjectAsIcon(string fileName, bool isLinked, string iconFile, 
    string iconCaption)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| fileName | String | 文件的完整路径。 |
| isLinked | Boolean | 如果`真的`然后插入链接的 OLE 对象，否则插入嵌入的 OLE 对象。 |
| iconFile | String | ICO 文件的完整路径。如果值为`无效的`，Aspose.Words 将使用预定义的图像。 |
| iconCaption | String | 图标标题。如果值为`无效的`，Aspose.Words 将使用文件名. |

### 返回值

包含 Ole 对象的形状节点并插入到当前 Builder 位置。

## 例子

展示如何将 OLE 对象插入文档。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// OLE 对象是我们本地文件系统中的文件的链接，可以由其他已安装的应用程序打开。
// 双击这些形状将启动应用程序，然后使用它打开链接的对象。
// 有三种使用 InsertOleObject 方法插入这些形状并配置其外观的方法。
// 1 - 从本地文件系统获取的图像：
using (FileStream imageStream = new FileStream(ImageDir + "Logo.jpg", FileMode.Open))
{
    // 如果省略“presentation”并设置“asIcon”，则此重载方法选择
    // 根据文件扩展名选择图标并使用文件名作为图标标题。
    builder.InsertOleObject(MyDir + "Spreadsheet.xlsx", false, false, imageStream); 
}

// 如果省略“presentation”并设置“asIcon”，则此重载方法选择
// 根据“progId”的图标并使用文件名作为图标标题。
// 2 - 基于将打开对象的应用程序的图标：
builder.InsertOleObject(MyDir + "Spreadsheet.xlsx", "Excel.Sheet", false, true, null);

// 如果省略“iconFile”和“iconCaption”，则此重载方法选择
// 根据“progId”的图标并使用预定义的图标标题。
// 3 - 来自本地文件系统的 32 x 32 像素或更小的图像图标，带有自定义标题：
builder.InsertOleObjectAsIcon(MyDir + "Presentation.pptx", false, ImageDir + "Logo icon.ico",
    "Double click to view presentation!");

doc.Save(ArtifactsDir + "DocumentBuilder.InsertOleObject.docx");
```

### 也可以看看

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)

---

## InsertOleObjectAsIcon(*string, string, bool, string, string*) {#insertoleobjectasicon_2}

将嵌入或链接的 OLE 对象作为图标插入文档。 允许指定图标文件和标题。使用给定的 progID 参数检测 OLE 对象类型。

```csharp
public Shape InsertOleObjectAsIcon(string fileName, string progId, bool isLinked, string iconFile, 
    string iconCaption)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| fileName | String | 文件的完整路径。 |
| progId | String | OLE 对象的 ProgId。 |
| isLinked | Boolean | 如果`真的`然后插入链接的 OLE 对象，否则插入嵌入的 OLE 对象。 |
| iconFile | String | ICO 文件的完整路径。如果值为`无效的`，Aspose.Words 将使用预定义的图像。 |
| iconCaption | String | 图标标题。如果值为`无效的`，Aspose.Words 将使用文件名. |

### 返回值

包含 Ole 对象的形状节点并插入到当前 Builder 位置。

## 例子

展示如何将嵌入或链接的 OLE 对象作为图标插入到文档中。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 如果省略“iconFile”和“iconCaption”，则此重载方法选择
// 根据“progId”的图标并使用文件名作为图标标题。
builder.InsertOleObjectAsIcon(MyDir + "Presentation.pptx", "Package", false, ImageDir + "Logo icon.ico", "My embedded file");

builder.InsertBreak(BreakType.LineBreak);

using (FileStream stream = new FileStream(MyDir + "Presentation.pptx", FileMode.Open))
{
    // 如果省略“iconFile”和“iconCaption”，则此重载方法选择
    // 根据文件扩展名选择图标并使用文件名作为图标标题。
    Shape shape = builder.InsertOleObjectAsIcon(stream, "PowerPoint.Application", ImageDir + "Logo icon.ico",
        "My embedded file stream");

    OlePackage setOlePackage = shape.OleFormat.OlePackage;
    setOlePackage.FileName = "Presentation.pptx";
    setOlePackage.DisplayName = "Presentation.pptx";
}

doc.Save(ArtifactsDir + "DocumentBuilder.InsertOleObjectAsIcon.docx");
```

### 也可以看看

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)

---

## InsertOleObjectAsIcon(*Stream, string, string, string*) {#insertoleobjectasicon}

将嵌入的 OLE 对象作为图标从流插入文档。 允许指定图标文件和标题。使用给定的 progID 参数检测 OLE 对象类型。

```csharp
public Shape InsertOleObjectAsIcon(Stream stream, string progId, string iconFile, 
    string iconCaption)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| stream | Stream | 包含应用程序数据的流。 |
| progId | String | OLE 对象的 ProgId。 |
| iconFile | String | ICO 文件的完整路径。如果值为`无效的`，Aspose.Words 将使用预定义的图像。 |
| iconCaption | String | 图标标题。如果值为`无效的` ，Aspose.Words 将使用预定义的图标标题。 |

### 返回值

包含 Ole 对象的形状节点并插入到当前 Builder 位置。

## 例子

展示如何将嵌入或链接的 OLE 对象作为图标插入到文档中。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 如果省略“iconFile”和“iconCaption”，则此重载方法选择
// 根据“progId”的图标并使用文件名作为图标标题。
builder.InsertOleObjectAsIcon(MyDir + "Presentation.pptx", "Package", false, ImageDir + "Logo icon.ico", "My embedded file");

builder.InsertBreak(BreakType.LineBreak);

using (FileStream stream = new FileStream(MyDir + "Presentation.pptx", FileMode.Open))
{
    // 如果省略“iconFile”和“iconCaption”，则此重载方法选择
    // 根据文件扩展名选择图标并使用文件名作为图标标题。
    Shape shape = builder.InsertOleObjectAsIcon(stream, "PowerPoint.Application", ImageDir + "Logo icon.ico",
        "My embedded file stream");

    OlePackage setOlePackage = shape.OleFormat.OlePackage;
    setOlePackage.FileName = "Presentation.pptx";
    setOlePackage.DisplayName = "Presentation.pptx";
}

doc.Save(ArtifactsDir + "DocumentBuilder.InsertOleObjectAsIcon.docx");
```

### 也可以看看

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
