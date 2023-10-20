---
title: DocumentSecurity Enum
linktitle: DocumentSecurity
articleTitle: DocumentSecurity
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.Properties.DocumentSecurity 枚举. 用作Securityproperty. 将文档的安全级别指定为数值 在 C#.
type: docs
weight: 4490
url: /zh/net/aspose.words.properties/documentsecurity/
---
## DocumentSecurity enumeration

用作[`Security`](../builtindocumentproperties/security/)property. 将文档的安全级别指定为数值。

```csharp
[Flags]
public enum DocumentSecurity
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| None | `0` | 该属性没有指定安全状态。 |
| PasswordProtected | `1` | 该文档受密码保护。 （迄今为止在文档中从未见过注释）. |
| ReadOnlyRecommended | `2` | 如果可能，以只读方式打开文档，但可以覆盖该设置。 |
| ReadOnlyEnforced | `4` | 始终以只读方式打开的文档。 |
| ReadOnlyExceptAnnotations | `8` | 除注释外始终以只读方式打开的文档。 |

## 例子

演示如何使用文档属性来显示文档的安全级别。

```csharp
Document doc = new Document();

Assert.AreEqual(DocumentSecurity.None, doc.BuiltInDocumentProperties.Security);

// 如果我们将文档配置为只读，它将使用“Security”内置属性显示此状态。
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

//“安全”是一个描述性属性。我们可以手动编辑它的值。
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
