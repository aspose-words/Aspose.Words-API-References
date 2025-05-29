---
title: DocumentSecurity Enum
linktitle: DocumentSecurity
articleTitle: DocumentSecurity
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.DocumentSecurity 枚举，增强文档的安全性。轻松指定和管理安全级别，实现最佳保护。
type: docs
weight: 5220
url: /zh/net/aspose.words.properties/documentsecurity/
---
## DocumentSecurity enumeration

用作[`Security`](../builtindocumentproperties/security/)属性。 以数值形式指定文档的安全级别。

```csharp
[Flags]
public enum DocumentSecurity
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| None | `0` | 该属性未指定任何安全状态。 |
| PasswordProtected | `1` | 该文档受密码保护。（迄今为止，文档中从未出现过此信息。） |
| ReadOnlyRecommended | `2` | 如果可能，文档将以只读方式打开，但该设置可以被覆盖。 |
| ReadOnlyEnforced | `4` | 文档始终以只读方式打开。 |
| ReadOnlyExceptAnnotations | `8` | 除注释外，文档始终以只读方式打开。 |

## 例子

展示如何使用文档属性来显示文档的安全级别。

```csharp
Document doc = new Document();

Assert.AreEqual(DocumentSecurity.None, doc.BuiltInDocumentProperties.Security);

// 如果我们将文档配置为只读，它将使用“安全”内置属性显示此状态。
doc.WriteProtection.ReadOnlyRecommended = true;
doc.Save(ArtifactsDir + "DocumentProperties.Security.ReadOnlyRecommended.docx");

Assert.AreEqual(DocumentSecurity.ReadOnlyRecommended, 
    new Document(ArtifactsDir + "DocumentProperties.Security.ReadOnlyRecommended.docx").BuiltInDocumentProperties.Security);

// 对文档进行写保护，然后验证其安全级别。
doc = new Document();

Assert.False(doc.WriteProtection.IsWriteProtected);

doc.WriteProtection.SetPassword("MyPassword");

Assert.True(doc.WriteProtection.ValidatePassword("MyPassword"));
Assert.True(doc.WriteProtection.IsWriteProtected);

doc.Save(ArtifactsDir + "DocumentProperties.Security.ReadOnlyEnforced.docx");

Assert.AreEqual(DocumentSecurity.ReadOnlyEnforced,
    new Document(ArtifactsDir + "DocumentProperties.Security.ReadOnlyEnforced.docx").BuiltInDocumentProperties.Security);

//“Security”是一个描述性属性。我们可以手动编辑它的值。
doc = new Document();

doc.Protect(ProtectionType.AllowOnlyComments, "MyPassword");
doc.BuiltInDocumentProperties.Security = DocumentSecurity.ReadOnlyExceptAnnotations;
doc.Save(ArtifactsDir + "DocumentProperties.Security.ReadOnlyExceptAnnotations.docx");

Assert.AreEqual(DocumentSecurity.ReadOnlyExceptAnnotations,
    new Document(ArtifactsDir + "DocumentProperties.Security.ReadOnlyExceptAnnotations.docx").BuiltInDocumentProperties.Security);
```

### 也可以看看

* 命名空间 [Aspose.Words.Properties](../../aspose.words.properties/)
* 部件 [Aspose.Words](../../)
