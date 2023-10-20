---
title: ProtectionType Enum
linktitle: ProtectionType
articleTitle: ProtectionType
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.ProtectionType 枚举. 文档的保护类型 在 C#.
type: docs
weight: 4510
url: /zh/net/aspose.words/protectiontype/
---
## ProtectionType enumeration

文档的保护类型。

```csharp
public enum ProtectionType
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| AllowOnlyComments | `1` | 用户只能修改文档中的评论。 |
| AllowOnlyFormFields | `2` | 用户只能在文档的表单域中输入数据。 |
| AllowOnlyRevisions | `0` | 用户只能在文档中添加修订标记。 |
| ReadOnly | `3` | 不允许更改文档。自 Microsoft Word 2003 起可用。 |
| NoProtection | `-1` | 文档不受保护。 |

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

* 命名空间 [Aspose.Words](../../aspose.words/)
* 部件 [Aspose.Words](../../)
