---
title: Section.ProtectedForForms
linktitle: ProtectedForForms
articleTitle: ProtectedForForms
second_title: 用于 .NET 的 Aspose.Words
description: Section ProtectedForForms 财产. 如果该部分受到表单保护则为真当某个部分受到表单保护时 用户只能在 Microsoft Word 的表单字段中选择和修改文本 在 C#.
type: docs
weight: 60
url: /zh/net/aspose.words/section/protectedforforms/
---
## Section.ProtectedForForms property

如果该部分受到表单保护，则为真。当某个部分受到表单保护时， 用户只能在 Microsoft Word 的表单字段中选择和修改文本。

```csharp
public bool ProtectedForForms { get; set; }
```

## 例子

显示如何关闭部分的保护。

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

// 关闭第一节的写保护。
doc.Sections[0].ProtectedForForms = false;

// 在这个输出文档中，我们将能够自由编辑第一部分，
// 我们只能在第二部分编辑表单域的内容。
doc.Save(ArtifactsDir + "Section.Protect.docx");
```

### 也可以看看

* class [Section](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
