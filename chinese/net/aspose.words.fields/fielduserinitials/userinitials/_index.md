---
title: FieldUserInitials.UserInitials
linktitle: UserInitials
articleTitle: UserInitials
second_title: Aspose.Words for .NET
description: 访问和自定义 FieldUserInitials 属性，轻松管理用户姓名首字母，增强个性化和用户体验。
type: docs
weight: 20
url: /zh/net/aspose.words.fields/fielduserinitials/userinitials/
---
## FieldUserInitials.UserInitials property

获取或设置当前用户的姓名首字母。

```csharp
public string UserInitials { get; set; }
```

## 例子

显示如何使用 USERINITIALS 字段。

```csharp
Document doc = new Document();

// 创建一个 UserInformation 对象并将其设置为我们创建的任何字段的用户信息来源。
UserInformation userInformation = new UserInformation();
userInformation.Initials = "J. D.";
doc.FieldOptions.CurrentUser = userInformation;

// 创建一个 USERINITIALS 字段来显示当前用户的姓名首字母，
// 从我们上面创建的 UserInformation 对象中获取。
DocumentBuilder builder = new DocumentBuilder(doc);
FieldUserInitials fieldUserInitials = (FieldUserInitials)builder.InsertField(FieldType.FieldUserInitials, true);
Assert.AreEqual(userInformation.Initials, fieldUserInitials.Result);

Assert.AreEqual(" USERINITIALS ", fieldUserInitials.GetFieldCode());
Assert.AreEqual("J. D.", fieldUserInitials.Result);

 // 我们可以设置此属性来让我们的字段覆盖当前存储在 UserInformation 对象中的值。
fieldUserInitials.UserInitials = "J. C.";
fieldUserInitials.Update();

Assert.AreEqual(" USERINITIALS  \"J. C.\"", fieldUserInitials.GetFieldCode());
Assert.AreEqual("J. C.", fieldUserInitials.Result);

// 这不会影响 UserInformation 对象中的值。
Assert.AreEqual("J. D.", doc.FieldOptions.CurrentUser.Initials);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.USERINITIALS.docx");
```

### 也可以看看

* class [FieldUserInitials](../)
* 命名空间 [Aspose.Words.Fields](../../../aspose.words.fields/)
* 部件 [Aspose.Words](../../../)
