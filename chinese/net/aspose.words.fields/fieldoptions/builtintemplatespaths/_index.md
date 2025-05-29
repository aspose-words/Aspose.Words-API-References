---
title: FieldOptions.BuiltInTemplatesPaths
linktitle: BuiltInTemplatesPaths
articleTitle: BuiltInTemplatesPaths
second_title: Aspose.Words for .NET
description: 了解如何使用 FieldOptions BuiltInTemplatesPaths 属性管理 MS Word 内置模板路径，以实现无缝文档创建。
type: docs
weight: 30
url: /zh/net/aspose.words.fields/fieldoptions/builtintemplatespaths/
---
## FieldOptions.BuiltInTemplatesPaths property

获取或设置 MS Word 内置模板的路径。

```csharp
public string[] BuiltInTemplatesPaths { get; set; }
```

## 评论

此属性由[`FieldAutoText`](../../fieldautotext/)和[`FieldGlossary`](../../fieldglossary/)字段，如果在[`AttachedTemplate`](../../../aspose.words/document/attachedtemplate/)模板。

默认情况下，MS Word 将内置模板存储在 c:\Users\&lt;用户名&gt;\AppData\Roaming\Microsoft\Document Building Blocks\1033\16\Built-In Building Blocks.dotx 和 C:\Users\&lt;用户名&gt;\AppData\Roaming\Microsoft\Templates\Normal.dotm 文件中。

## 例子

展示如何显示带有 AUTOTEXT 和 GLOSSARY 字段的构建块。

```csharp
Document doc = new Document();

// 创建一个词汇表文档并向其中添加自动图文集构建块。
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

// 设置一个包含我们的文档或其附加模板可能不包含的部分的文件。
doc.FieldOptions.BuiltInTemplatesPaths = new[] { MyDir + "Busniess brochure.dotx" };

DocumentBuilder builder = new DocumentBuilder(doc);

// 下面是两种使用字段显示我们的构建块内容的方法。
// 1 - 使用 AUTOTEXT 字段：
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
* 命名空间 [Aspose.Words.Fields](../../../aspose.words.fields/)
* 部件 [Aspose.Words](../../../)
