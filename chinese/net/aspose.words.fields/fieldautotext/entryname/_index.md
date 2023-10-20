---
title: FieldAutoText.EntryName
linktitle: EntryName
articleTitle: EntryName
second_title: 用于 .NET 的 Aspose.Words
description: FieldAutoText EntryName 财产. 获取或设置自动图文集条目的名称 在 C#.
type: docs
weight: 20
url: /zh/net/aspose.words.fields/fieldautotext/entryname/
---
## FieldAutoText.EntryName property

获取或设置自动图文集条目的名称。

```csharp
public string EntryName { get; set; }
```

## 例子

演示如何显示带有 AUTOTEXT 和 GLOSSARY 字段的构建块。

```csharp
Document doc = new Document();

// 创建词汇表文档并向其添加自动图文集构建块。
doc.GlossaryDocument = new GlossaryDocument();
BuildingBlock buildingBlock = new BuildingBlock(doc.GlossaryDocument);
buildingBlock.Name = "MyBlock";
buildingBlock.Gallery = BuildingBlockGallery.AutoText;
buildingBlock.Category = "General";
buildingBlock.Description = "MyBlock description";
buildingBlock.Behavior = BuildingBlockBehavior.Paragraph;
doc.GlossaryDocument.AppendChild(buildingBlock);

// 创建一个源并将其作为文本添加到我们的构建块中。
Document buildingBlockSource = new Document();
DocumentBuilder buildingBlockSourceBuilder = new DocumentBuilder(buildingBlockSource);
buildingBlockSourceBuilder.Writeln("Hello World!");

Node buildingBlockContent = doc.GlossaryDocument.ImportNode(buildingBlockSource.FirstSection, true);
buildingBlock.AppendChild(buildingBlockContent);

// 设置一个文件，其中包含我们的文档或其附加模板可能不包含的部分。
doc.FieldOptions.BuiltInTemplatesPaths = new[] { MyDir + "Busniess brochure.dotx" };

DocumentBuilder builder = new DocumentBuilder(doc);

// 下面是两种使用字段来显示我们构建块的内容的方法。
// 1 - 使用自动文本字段：
FieldAutoText fieldAutoText = (FieldAutoText)builder.InsertField(FieldType.FieldAutoText, true);
fieldAutoText.EntryName = "MyBlock";

Assert.AreEqual(" AUTOTEXT  MyBlock", fieldAutoText.GetFieldCode());

// 2 - 使用词汇表字段：
FieldGlossary fieldGlossary = (FieldGlossary)builder.InsertField(FieldType.FieldGlossary, true);
fieldGlossary.EntryName = "MyBlock";

Assert.AreEqual(" GLOSSARY  MyBlock", fieldGlossary.GetFieldCode());

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.AUTOTEXT.GLOSSARY.dotx");
```

### 也可以看看

* class [FieldAutoText](../)
* 命名空间 [Aspose.Words.Fields](../../../aspose.words.fields/)
* 部件 [Aspose.Words](../../../)
