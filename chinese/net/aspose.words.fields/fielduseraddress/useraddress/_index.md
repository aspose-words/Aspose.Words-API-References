---
title: FieldUserAddress.UserAddress
linktitle: UserAddress
articleTitle: UserAddress
second_title: Aspose.Words for .NET
description: 使用 FieldUserAddress 属性轻松管理用户邮政地址。轻松检索和更新当前用户信息，提升用户体验。
type: docs
weight: 20
url: /zh/net/aspose.words.fields/fielduseraddress/useraddress/
---
## FieldUserAddress.UserAddress property

获取或设置当前用户的邮政地址。

```csharp
public string UserAddress { get; set; }
```

## 例子

展示如何使用 USERADDRESS 字段。

```csharp
Document doc = new Document();

// 创建一个 UserInformation 对象并将其设置为我们创建的任何字段的用户信息来源。
UserInformation userInformation = new UserInformation();
userInformation.Address = "123 Main Street";
doc.FieldOptions.CurrentUser = userInformation;

// 创建一个 USERADDRESS 字段来显示当前用户的地址，
// 从我们上面创建的 UserInformation 对象中获取。
DocumentBuilder builder = new DocumentBuilder(doc);
FieldUserAddress fieldUserAddress = (FieldUserAddress)builder.InsertField(FieldType.FieldUserAddress, true);
Assert.AreEqual(" USERADDRESS ", fieldUserAddress.GetFieldCode());
Assert.AreEqual("123 Main Street", fieldUserAddress.Result);

// 我们可以设置此属性来让我们的字段覆盖当前存储在 UserInformation 对象中的值。
fieldUserAddress.UserAddress = "456 North Road";
fieldUserAddress.Update();

Assert.AreEqual(" USERADDRESS  \"456 North Road\"", fieldUserAddress.GetFieldCode());
Assert.AreEqual("456 North Road", fieldUserAddress.Result);

// 这不会影响 UserInformation 对象中的值。
Assert.AreEqual("123 Main Street", doc.FieldOptions.CurrentUser.Address);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.USERADDRESS.docx");
```

### 也可以看看

* class [FieldUserAddress](../)
* 命名空间 [Aspose.Words.Fields](../../../aspose.words.fields/)
* 部件 [Aspose.Words](../../../)
