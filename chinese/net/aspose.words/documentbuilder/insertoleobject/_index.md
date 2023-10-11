---
title: DocumentBuilder.InsertOleObject
second_title: Aspose.Words for .NET API 参考
description: DocumentBuilder 方法. 将嵌入的 OLE 对象从流插入到文档中
type: docs
weight: 400
url: /zh/net/aspose.words/documentbuilder/insertoleobject/
---
## InsertOleObject(Stream, string, bool, Stream) {#insertoleobject}

将嵌入的 OLE 对象从流插入到文档中。

```csharp
public Shape InsertOleObject(Stream stream, string progId, bool asIcon, Stream presentation)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| stream | Stream | 包含应用程序数据的流。 |
| progId | String | OLE 对象的编程标识符。 |
| asIcon | Boolean | 指定要插入的 OLE 对象的图标模式或普通模式。 |
| presentation | Stream | OLE 对象的图像表示。如果值为`无效的`Aspose.Words 将使用预定义图像之一。 |

### 返回值

包含 Ole 对象并插入到当前 Builder 位置的形状节点。

### 例子

演示如何使用文档生成器在文档中嵌入 OLE 对象。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 从本地文件系统插入 Microsoft Excel 电子表格
// 进入文档，同时保持其默认外观。
using (Stream spreadsheetStream = File.Open(MyDir + "Spreadsheet.xlsx", FileMode.Open))
{
    builder.Writeln("Spreadsheet Ole object:");
    // 如果省略 'presentation' 并设置 'asIcon'，则此重载方法选择
    // 根据“progId”的图标并使用预定义的图标标题。
    builder.InsertOleObject(spreadsheetStream, "OleObject.xlsx", false, null);
}

// 将 Microsoft Powerpoint 演示文稿作为 OLE 对象插入。
// 这次，它将有一个从网络下载的图像作为图标。
using (Stream powerpointStream = File.Open(MyDir + "Presentation.pptx", FileMode.Open))
{
    using (HttpClient httpClient = new HttpClient())
    {
        byte[] imgBytes = File.ReadAllBytes(ImageDir + "Logo.jpg");

        using (MemoryStream imageStream = new MemoryStream(imgBytes))
        {
            builder.InsertParagraph();
            builder.Writeln("Powerpoint Ole object:");
            builder.InsertOleObject(powerpointStream, "OleObject.pptx", true, imageStream);
        }
    }
}

// 在 Microsoft Word 中双击这些对象以打开
// 使用各自应用程序的链接文件。
doc.Save(ArtifactsDir + "DocumentBuilder.InsertOleObjects.docx");
```

### 也可以看看

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* 命名空间 [Aspose.Words](../../documentbuilder/)
* 部件 [Aspose.Words](../../../)

---

## InsertOleObject(string, bool, bool, Stream) {#insertoleobject_1}

将嵌入或链接的 OLE 对象从文件插入到文档中。使用文件扩展名检测 OLE 对象类型。

```csharp
public Shape InsertOleObject(string fileName, bool isLinked, bool asIcon, Stream presentation)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| fileName | String | 文件的完整路径。 |
| isLinked | Boolean | 如果`真的`然后插入链接的 OLE 对象，否则插入嵌入的 OLE 对象。 |
| asIcon | Boolean | 指定要插入的 OLE 对象的图标模式或普通模式。 |
| presentation | Stream | OLE 对象的图像表示。如果值为`无效的`Aspose.Words 将使用预定义图像之一。 |

### 返回值

包含 Ole 对象并插入到当前 Builder 位置的形状节点。

### 例子

演示如何将 OLE 对象插入到文档中。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// OLE 对象是本地文件系统中文件的链接，可以由其他已安装的应用程序打开。
// 双击这些形状将启动应用程序，然后使用它打开链接的对象。
// 使用InsertOleObject 方法插入这些形状并配置其外观的方法有3 种。
// 1 - 从本地文件系统获取的图像：
using (FileStream imageStream = new FileStream(ImageDir + "Logo.jpg", FileMode.Open))
{
    // 如果省略 'presentation' 并设置 'asIcon'，则此重载方法选择
    // 根据文件扩展名的图标，并使用文件名作为图标标题。
    builder.InsertOleObject(MyDir + "Spreadsheet.xlsx", false, false, imageStream); 
}

// 如果省略 'presentation' 并设置 'asIcon'，则此重载方法选择
// 根据“progId”的图标并使用图标标题的文件名。
// 2 - 基于将打开对象的应用程序的图标：
builder.InsertOleObject(MyDir + "Spreadsheet.xlsx", "Excel.Sheet", false, true, null);

// 如果省略 'iconFile' 和 'iconCaption'，则此重载方法选择
// 根据“progId”的图标并使用预定义的图标标题。
// 3 - 本地文件系统中 32 x 32 像素或更小的图像图标，带有自定义标题：
builder.InsertOleObjectAsIcon(MyDir + "Presentation.pptx", false, ImageDir + "Logo icon.ico",
    "Double click to view presentation!");

doc.Save(ArtifactsDir + "DocumentBuilder.InsertOleObject.docx");
```

### 也可以看看

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* 命名空间 [Aspose.Words](../../documentbuilder/)
* 部件 [Aspose.Words](../../../)

---

## InsertOleObject(string, string, bool, bool, Stream) {#insertoleobject_2}

将嵌入或链接的 OLE 对象从文件插入到文档中。使用给定的 progID 参数检测 OLE 对象类型。

```csharp
public Shape InsertOleObject(string fileName, string progId, bool isLinked, bool asIcon, 
    Stream presentation)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| fileName | String | 文件的完整路径。 |
| progId | String | OLE 对象的 ProgId。 |
| isLinked | Boolean | 如果`真的`然后插入链接的 OLE 对象，否则插入嵌入的 OLE 对象。 |
| asIcon | Boolean | 指定要插入的 OLE 对象的图标模式或普通模式。 |
| presentation | Stream | OLE 对象的图像表示。如果值为`无效的`Aspose.Words 将使用预定义图像之一。 |

### 返回值

包含 Ole 对象并插入到当前 Builder 位置的形状节点。

### 例子

演示如何将 OLE 对象插入到文档中。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// OLE 对象是本地文件系统中文件的链接，可以由其他已安装的应用程序打开。
// 双击这些形状将启动应用程序，然后使用它打开链接的对象。
// 使用InsertOleObject 方法插入这些形状并配置其外观的方法有3 种。
// 1 - 从本地文件系统获取的图像：
using (FileStream imageStream = new FileStream(ImageDir + "Logo.jpg", FileMode.Open))
{
    // 如果省略 'presentation' 并设置 'asIcon'，则此重载方法选择
    // 根据文件扩展名的图标，并使用文件名作为图标标题。
    builder.InsertOleObject(MyDir + "Spreadsheet.xlsx", false, false, imageStream); 
}

// 如果省略 'presentation' 并设置 'asIcon'，则此重载方法选择
// 根据“progId”的图标并使用图标标题的文件名。
// 2 - 基于将打开对象的应用程序的图标：
builder.InsertOleObject(MyDir + "Spreadsheet.xlsx", "Excel.Sheet", false, true, null);

// 如果省略 'iconFile' 和 'iconCaption'，则此重载方法选择
// 根据“progId”的图标并使用预定义的图标标题。
// 3 - 本地文件系统中 32 x 32 像素或更小的图像图标，带有自定义标题：
builder.InsertOleObjectAsIcon(MyDir + "Presentation.pptx", false, ImageDir + "Logo icon.ico",
    "Double click to view presentation!");

doc.Save(ArtifactsDir + "DocumentBuilder.InsertOleObject.docx");
```

### 也可以看看

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* 命名空间 [Aspose.Words](../../documentbuilder/)
* 部件 [Aspose.Words](../../../)


