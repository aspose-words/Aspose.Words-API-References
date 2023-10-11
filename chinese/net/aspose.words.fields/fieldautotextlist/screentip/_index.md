---
title: FieldAutoTextList.ScreenTip
second_title: Aspose.Words for .NET API 参考
description: FieldAutoTextList 财产. 获取或设置要显示的屏幕提示文本
type: docs
weight: 40
url: /zh/net/aspose.words.fields/fieldautotextlist/screentip/
---
## FieldAutoTextList.ScreenTip property

获取或设置要显示的屏幕提示文本。

```csharp
public string ScreenTip { get; set; }
```

### 例子

演示如何使用 AUTOTEXTLIST 字段从自动图文集条目列表中进行选择。

```csharp
public void FieldAutoTextList()
{
    Document doc = new Document();

    // 创建一个词汇表文档并用自动文本条目填充它。
    doc.GlossaryDocument = new GlossaryDocument();
    AppendAutoTextEntry(doc.GlossaryDocument, "AutoText 1", "Contents of AutoText 1");
    AppendAutoTextEntry(doc.GlossaryDocument, "AutoText 2", "Contents of AutoText 2");
    AppendAutoTextEntry(doc.GlossaryDocument, "AutoText 3", "Contents of AutoText 3");

    DocumentBuilder builder = new DocumentBuilder(doc);

    // 创建一个 AUTOTEXTLIST 字段并设置该字段将在 Microsoft Word 中显示的文本。
    // 设置文本以提示用户右键单击该字段以选择自动图文集构建块，
    // 该字段将显示其内容。
    FieldAutoTextList field = (FieldAutoTextList)builder.InsertField(FieldType.FieldAutoTextList, true);
    field.EntryName = "Right click here to select an AutoText block";
    field.ListStyle = "Heading 1";
    field.ScreenTip = "Hover tip text for AutoTextList goes here";

    Assert.AreEqual(" AUTOTEXTLIST  \"Right click here to select an AutoText block\" " +
                    "\\s \"Heading 1\" " +
                    "\\t \"Hover tip text for AutoTextList goes here\"", field.GetFieldCode());

    doc.Save(ArtifactsDir + "Field.AUTOTEXTLIST.dotx");
}

/// <summary>
/// 创建自动图文集类型构建块并将其添加到术语表文档中。
/// </summary>
private static void AppendAutoTextEntry(GlossaryDocument glossaryDoc, string name, string contents)
{
    BuildingBlock buildingBlock = new BuildingBlock(glossaryDoc);
    buildingBlock.Name = name;
    buildingBlock.Gallery = BuildingBlockGallery.AutoText;
    buildingBlock.Category = "General";
    buildingBlock.Behavior = BuildingBlockBehavior.Paragraph;

    Section section = new Section(glossaryDoc);
    section.AppendChild(new Body(glossaryDoc));
    section.Body.AppendParagraph(contents);
    buildingBlock.AppendChild(section);

    glossaryDoc.AppendChild(buildingBlock);
}
```

### 也可以看看

* class [FieldAutoTextList](../)
* 命名空间 [Aspose.Words.Fields](../../fieldautotextlist/)
* 部件 [Aspose.Words](../../../)


