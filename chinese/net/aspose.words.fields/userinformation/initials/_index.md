---
title: UserInformation.Initials
second_title: Aspose.Words for .NET API 参考
description: UserInformation 财产. 获取或设置用户的姓名缩写
type: docs
weight: 40
url: /zh/net/aspose.words.fields/userinformation/initials/
---
## UserInformation.Initials property

获取或设置用户的姓名缩写。

```csharp
public string Initials { get; set; }
```

### 例子

演示如何设置用户详细信息并使用字段显示它们。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 创建一个UserInformation对象，并将其设置为显示用户信息的字段的数据源。
UserInformation userInformation = new UserInformation
{
    Name = "John Doe",
    Initials = "J. D.",
    Address = "123 Main Street"
};
doc.FieldOptions.CurrentUser = userInformation;

// 插入 USERNAME、USERINITIALS 和 USERADDRESS 字段，这些字段显示的值
// 我们上面创建的 UserInformation 对象的相应属性。
Assert.AreEqual(userInformation.Name, builder.InsertField(" USERNAME ").Result);
Assert.AreEqual(userInformation.Initials, builder.InsertField(" USERINITIALS ").Result);
Assert.AreEqual(userInformation.Address, builder.InsertField(" USERADDRESS ").Result);

// 字段选项对象还有一个静态默认用户，所有文档中的字段都可以引用。
UserInformation.DefaultUser.Name = "Default User";
UserInformation.DefaultUser.Initials = "D. U.";
UserInformation.DefaultUser.Address = "One Microsoft Way";
doc.FieldOptions.CurrentUser = UserInformation.DefaultUser;

Assert.AreEqual("Default User", builder.InsertField(" USERNAME ").Result);
Assert.AreEqual("D. U.", builder.InsertField(" USERINITIALS ").Result);
Assert.AreEqual("One Microsoft Way", builder.InsertField(" USERADDRESS ").Result);

doc.UpdateFields();
doc.Save(ArtifactsDir + "FieldOptions.CurrentUser.docx");
```

### 也可以看看

* class [UserInformation](../)
* 命名空间 [Aspose.Words.Fields](../../userinformation/)
* 部件 [Aspose.Words](../../../)


