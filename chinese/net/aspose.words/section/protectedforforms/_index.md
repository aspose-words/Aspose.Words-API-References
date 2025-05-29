---
title: Section.ProtectedForForms
linktitle: ProtectedForForms
articleTitle: ProtectedForForms
second_title: Aspose.Words for .NET
description: 了解 Microsoft Word 中的 ProtectedForForms 属性如何增强文档安全性，让用户能够轻松地仅编辑指定的表单字段。
type: docs
weight: 60
url: /zh/net/aspose.words/section/protectedforforms/
---
## Section.ProtectedForForms property

如果该部分受表单保护，则为 True。当某个部分受表单保护时， 用户只能在 Microsoft Word 中选择和修改表单域中的文本。

```csharp
public bool ProtectedForForms { get; set; }
```

## 例子

显示如何关闭某个部分的保护。

```csharp
Document doc = new Document();

DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Section 1. Hello world!");
builder.InsertBreak(BreakType.SectionBreakNewPage);

builder.Writeln("Section 2. Hello again!");
builder.Write("Please enter text here: ");
builder.InsertTextInput("TextInput1", TextFormFieldType.Regular, "", "Placeholder text", 0);

// 对文档中的每个部分应用写保护。
doc.Protect(ProtectionType.AllowOnlyFormFields);

// 关闭第一部分的写保护。
doc.Sections[0].ProtectedForForms = false;

// 在此输出文档中，我们将能够自由编辑第一部分，
// 并且我们只能编辑第二部分中的表单字段的内容。
doc.Save(ArtifactsDir + "Section.Protect.docx");
```

### 也可以看看

* class [Section](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
