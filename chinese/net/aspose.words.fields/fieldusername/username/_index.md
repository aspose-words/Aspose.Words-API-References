---
title: FieldUserName.UserName
linktitle: UserName
articleTitle: UserName
second_title: Aspose.Words for .NET
description: 使用 FieldUserName 属性轻松管理当前用户的名称。增强用户体验并无缝个性化交互。
type: docs
weight: 20
url: /zh/net/aspose.words.fields/fieldusername/username/
---
## FieldUserName.UserName property

手势或设置当前用户的名称。

```csharp
public string UserName { get; set; }
```

## 例子

显示如何使用 USERNAME 字段。

```csharp
Document doc = new Document();

// 创建一个 UserInformation 对象并将其设置为我们创建的任何字段的用户信息来源。
UserInformation userInformation = new UserInformation();
userInformation.Name = "John Doe";
doc.FieldOptions.CurrentUser = userInformation;

DocumentBuilder builder = new DocumentBuilder(doc);

// 创建一个 USERNAME 字段来显示当前用户的名称，
// 从我们上面创建的 UserInformation 对象中获取。
FieldUserName fieldUserName = (FieldUserName)builder.InsertField(FieldType.FieldUserName, true);
Assert.AreEqual(userInformation.Name, fieldUserName.Result);

Assert.AreEqual(" USERNAME ", fieldUserName.GetFieldCode());
Assert.AreEqual("John Doe", fieldUserName.Result);

 // 我们可以设置此属性来让我们的字段覆盖当前存储在 UserInformation 对象中的值。
fieldUserName.UserName = "Jane Doe";
fieldUserName.Update();

Assert.AreEqual(" USERNAME  \"Jane Doe\"", fieldUserName.GetFieldCode());
Assert.AreEqual("Jane Doe", fieldUserName.Result);

// 这不会影响 UserInformation 对象中的值。
Assert.AreEqual("John Doe", doc.FieldOptions.CurrentUser.Name);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.USERNAME.docx");
```

### 也可以看看

* class [FieldUserName](../)
* 命名空间 [Aspose.Words.Fields](../../../aspose.words.fields/)
* 部件 [Aspose.Words](../../../)
