---
title: FieldMacroButton.MacroName
linktitle: MacroName
articleTitle: MacroName
second_title: Aspose.Words for .NET
description: 发现 FieldMacroButton MacroName 属性，轻松管理和自定义您的宏或命令，以增强功能和效率。
type: docs
weight: 30
url: /zh/net/aspose.words.fields/fieldmacrobutton/macroname/
---
## FieldMacroButton.MacroName property

获取或设置要运行的宏或命令的名称。

```csharp
public string MacroName { get; set; }
```

## 例子

展示如何使用 MACROBUTTON 字段来允许我们通过单击来运行文档的宏。

```csharp
Document doc = new Document(MyDir + "Macro.docm");
DocumentBuilder builder = new DocumentBuilder(doc);

Assert.IsTrue(doc.HasMacros);

// 插入一个 MACROBUTTON 字段，并在 MacroName 属性中按名称引用文档的某个宏。
FieldMacroButton field = (FieldMacroButton)builder.InsertField(FieldType.FieldMacroButton, true);
field.MacroName = "MyMacro";
field.DisplayText = "Double click to run macro: " + field.MacroName;

Assert.AreEqual(" MACROBUTTON  MyMacro Double click to run macro: MyMacro", field.GetFieldCode());

// 使用该属性引用“ViewZoom200”，这是 Microsoft Word 附带的宏。
// 我们可以通过“查看”->“宏”（下拉菜单）->“查看宏”找到所有其他宏。
// 在该菜单中，从“宏：”下拉菜单中选择“Word 命令”。
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
