---
title: FieldMacroButton.DisplayText
linktitle: DisplayText
articleTitle: DisplayText
second_title: 用于 .NET 的 Aspose.Words
description: FieldMacroButton DisplayText 财产. 获取或设置显示为选择运行宏或命令的按钮的文本 在 C#.
type: docs
weight: 20
url: /zh/net/aspose.words.fields/fieldmacrobutton/displaytext/
---
## FieldMacroButton.DisplayText property

获取或设置显示为选择运行宏或命令的“按钮”的文本。

```csharp
public string DisplayText { get; set; }
```

## 例子

演示如何使用 MACROBUTTON 字段来允许我们通过单击来运行文档的宏。

```csharp
Document doc = new Document(MyDir + "Macro.docm");
DocumentBuilder builder = new DocumentBuilder(doc);

Assert.IsTrue(doc.HasMacros);

// 插入 MACROBUTTON 字段，并按 MacroName 属性中的名称引用文档的宏之一。
FieldMacroButton field = (FieldMacroButton)builder.InsertField(FieldType.FieldMacroButton, true);
field.MacroName = "MyMacro";
field.DisplayText = "Double click to run macro: " + field.MacroName;

Assert.AreEqual(" MACROBUTTON  MyMacro Double click to run macro: MyMacro", field.GetFieldCode());

// 使用该属性引用“ViewZoom200”，这是 Microsoft Word 附带的宏。
// 我们可以通过 View -> 找到所有其他宏宏（下拉菜单）->查看宏。
// 在该菜单中，从“宏位于：”下拉列表中选择“Word 命令”。
// 如果我们的文档包含与库存宏同名的自定义宏，
// 我们的宏将是 MACROBUTTON 字段运行的宏。
builder.InsertParagraph();
field = (FieldMacroButton)builder.InsertField(FieldType.FieldMacroButton, true);
field.MacroName = "ViewZoom200";
field.DisplayText = "Run " + field.MacroName;

Assert.AreEqual(" MACROBUTTON  ViewZoom200 Run ViewZoom200", field.GetFieldCode());

// 将文档保存为启用宏的文档类型。
doc.Save(ArtifactsDir + "Field.MACROBUTTON.docm");
```

### 也可以看看

* class [FieldMacroButton](../)
* 命名空间 [Aspose.Words.Fields](../../../aspose.words.fields/)
* 部件 [Aspose.Words](../../../)
