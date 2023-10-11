---
title: FieldOptions.BuiltInTemplatesPaths
second_title: Aspose.Words for .NET API 参考
description: FieldOptions 财产. 获取或设置 MS Word 内置模板的路径
type: docs
weight: 30
url: /zh/net/aspose.words.fields/fieldoptions/builtintemplatespaths/
---
## FieldOptions.BuiltInTemplatesPaths property

获取或设置 MS Word 内置模板的路径。

```csharp
public string[] BuiltInTemplatesPaths { get; set; }
```

### 评论

该属性由[`FieldAutoText`](../../fieldautotext/)和[`FieldGlossary`](../../fieldglossary/)字段，如果在中找不到引用的自动文本条目[`AttachedTemplate`](../../../aspose.words/document/attachedtemplate/)模板。

默认情况下，MS Word 将内置模板存储在 c:\Users\&lt;用户名&gt;\AppData\Roaming\Microsoft\Document Building Blocks\1033\16\Built-In Building Blocks.dotx and C:\Users\&lt;用户名&gt;\ AppData\Roaming\Microsoft\Templates\Normal.dotm 文件。

### 例子

演示如何显示带有自动文本和词汇表字段的构建块。

```csharp
Document doc = new Document();

// 创建词汇表文档并向其中添加自动图文集构建块。
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

// 下面是使用字段来显示构建块内容的两种方法。
// 1 - 使用自动文本字段：
FieldAutoText fieldAutoText = (FieldAutoText)builder.InsertField(FieldType.FieldAutoText, true);
fieldAutoText.EntryName = "MyBlock";

Assert.AreEqual(" AUTOTEXT  MyBlock", fieldAutoText.GetFieldCode());

// 2 - 使用 GLOSSARY 字段：
FieldGlossary fieldGlossary = (FieldGlossary)builder.InsertField(FieldType.FieldGlossary, true);
fieldGlossary.EntryName = "MyBlock";

Assert.AreEqual(" GLOSSARY  MyBlock", fieldGlossary.GetFieldCode());

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.AUTOTEXT.GLOSSARY.dotx");
```

### 也可以看看

* class [FieldOptions](../)
* 命名空间 [Aspose.Words.Fields](../../fieldoptions/)
* 部件 [Aspose.Words](../../../)


