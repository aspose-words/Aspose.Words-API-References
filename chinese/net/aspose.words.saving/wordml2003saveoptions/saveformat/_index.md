---
title: WordML2003SaveOptions.SaveFormat
linktitle: SaveFormat
articleTitle: SaveFormat
second_title: Aspose.Words for .NET
description: 了解 WordML2003SaveOptions 的 SaveFormat 属性如何定义文档保存格式。确保您的文件与 WordML 无缝兼容！
type: docs
weight: 20
url: /zh/net/aspose.words.saving/wordml2003saveoptions/saveformat/
---
## WordML2003SaveOptions.SaveFormat property

指定如果使用此保存选项对象，文档将以哪种格式保存。 只能是WordML.

```csharp
public override SaveFormat SaveFormat { get; set; }
```

## 例子

显示如何管理输出文档的原始内容。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// 创建一个“WordML2003SaveOptions”对象以传递给文档的“Save”方法
// 修改我们将文档保存为 WordML 保存格式的方式。
WordML2003SaveOptions options = new WordML2003SaveOptions();

Assert.AreEqual(SaveFormat.WordML, options.SaveFormat);

// 将“PrettyFormat”属性设置为“true”以应用制表符缩进和
// 换行符使输出文档的原始内容更易于阅读。
// 将“PrettyFormat”属性设置为“false”以将文档的原始内容保存在文本的一个连续主体中。
options.PrettyFormat = prettyFormat;

doc.Save(ArtifactsDir + "WordML2003SaveOptions.PrettyFormat.xml", options);

string fileContents = File.ReadAllText(ArtifactsDir + "WordML2003SaveOptions.PrettyFormat.xml");
string newLine = Environment.NewLine;

if (prettyFormat)
    Assert.True(fileContents.Contains(
        $"<o:DocumentProperties>{newLine}\t\t" +
            $"<o:Revision>1</o:Revision>{newLine}\t\t" +
            $"<o:TotalTime>0</o:TotalTime>{newLine}\t\t" +
            $"<o:Pages>1</o:Pages>{newLine}\t\t" +
            $"<o:Words>0</o:Words>{newLine}\t\t" +
            $"<o:Characters>0</o:Characters>{newLine}\t\t" +
            $"<o:Lines>1</o:Lines>{newLine}\t\t" +
            $"<o:Paragraphs>1</o:Paragraphs>{newLine}\t\t" +
            $"<o:CharactersWithSpaces>0</o:CharactersWithSpaces>{newLine}\t\t" +
            $"<o:Version>11.5606</o:Version>{newLine}\t" +
        "</o:DocumentProperties>"));
else
    Assert.True(fileContents.Contains(
        "<o:DocumentProperties><o:Revision>1</o:Revision><o:TotalTime>0</o:TotalTime><o:Pages>1</o:Pages>" +
        "<o:Words>0</o:Words><o:Characters>0</o:Characters><o:Lines>1</o:Lines><o:Paragraphs>1</o:Paragraphs>" +
        "<o:CharactersWithSpaces>0</o:CharactersWithSpaces><o:Version>11.5606</o:Version></o:DocumentProperties>"));
```

### 也可以看看

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [WordML2003SaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
