---
title: UserInformation Class
linktitle: UserInformation
articleTitle: UserInformation
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Fields.UserInformation 类，以有效管理用户详细信息并增强应用程序中的文档处理。
type: docs
weight: 3200
url: /zh/net/aspose.words.fields/userinformation/
---
## UserInformation class

指定有关用户的信息。

要了解更多信息，请访问[使用字段](https://docs.aspose.com/words/net/working-with-fields/)文档文章。

```csharp
public class UserInformation
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [UserInformation](userinformation/)() | 默认构造函数。 |

## 特性

| 姓名 | 描述 |
| --- | --- |
| static [DefaultUser](../../aspose.words.fields/userinformation/defaultuser/) { get; } | 默认用户信息。 |
| [Address](../../aspose.words.fields/userinformation/address/) { get; set; } | 获取或设置用户的邮政地址。 |
| [Initials](../../aspose.words.fields/userinformation/initials/) { get; set; } | 获取或设置用户的姓名首字母。 |
| [Name](../../aspose.words.fields/userinformation/name/) { get; set; } | 获取或设置用户的名称。 |

## 例子

展示如何设置用户详细信息并使用字段显示它们。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 创建一个 UserInformation 对象并将其设置为显示用户信息字段的数据源。
UserInformation userInformation = new UserInformation
{
    Name = "John Doe",
    Initials = "J. D.",
    Address = "123 Main Street"
};
doc.FieldOptions.CurrentUser = userInformation;

// 插入 USERNAME、USERINITIALS 和 USERADDRESS 字段，显示以下值
// 我们上面创建的 UserInformation 对象的各个属性。
Assert.AreEqual(userInformation.Name, builder.InsertField(" USERNAME ").Result);
Assert.AreEqual(userInformation.Initials, builder.InsertField(" USERINITIALS ").Result);
Assert.AreEqual(userInformation.Address, builder.InsertField(" USERADDRESS ").Result);

// 字段选项对象还具有静态默认用户，所有文档中的字段都可以引用。
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

* 命名空间 [Aspose.Words.Fields](../../aspose.words.fields/)
* 部件 [Aspose.Words](../../)
