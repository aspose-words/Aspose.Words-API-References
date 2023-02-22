---
title: UserInformation.Name
second_title: Aspose.Words for .NET API 参考
description: UserInformation 财产. 获取或设置用户名
type: docs
weight: 50
url: /zh/net/aspose.words.fields/userinformation/name/
---
## UserInformation.Name property

获取或设置用户名。

```csharp
public string Name { get; set; }
```

### 例子

显示如何设置用户详细信息，并使用字段显示它们。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 创建一个 UserInformation 对象，并将其设置为显示用户信息的字段的数据源。
UserInformation userInformation = new UserInformation
{
    Name = "John Doe",
    Initials = "J. D.",
    Address = "123 Main Street"
};
doc.FieldOptions.CurrentUser = userInformation;

// 插入 USERNAME、USERINITIALS 和 USERADDRESS 字段，它们显示的值
// 我们在上面创建的 UserInformation 对象的各个属性。 
Assert.AreEqual(userInformation.Name, builder.InsertField(" USERNAME ").Result);
Assert.AreEqual(userInformation.Initials, builder.InsertField(" USERINITIALS ").Result);
Assert.AreEqual(userInformation.Address, builder.InsertField(" USERADDRESS ").Result);

// 字段选项对象还有一个静态默认用户，所有文档的字段都可以引用。
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


