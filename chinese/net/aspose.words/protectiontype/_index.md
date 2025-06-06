---
title: ProtectionType Enum
linktitle: ProtectionType
articleTitle: ProtectionType
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.ProtectionType 枚举，实现强大的文档安全保护。立即使用可自定义的保护选项增强您的文档安全！
type: docs
weight: 5240
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
| AllowOnlyComments | `1` | 用户只能修改文档中的注释。 |
| AllowOnlyFormFields | `2` | 用户只能在文档的表单字段中输入数据。 |
| AllowOnlyRevisions | `0` | 用户只能向文档添加修订标记。 |
| ReadOnly | `3` | 不允许对文档进行任何更改。Microsoft Word 2003 及更高版本可用。 |
| NoProtection | `-1` | 该文档未受保护。 |

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

* 命名空间 [Aspose.Words](../../aspose.words/)
* 部件 [Aspose.Words](../../)
