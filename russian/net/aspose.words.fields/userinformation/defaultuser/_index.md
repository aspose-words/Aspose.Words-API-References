---
title: UserInformation.DefaultUser
linktitle: DefaultUser
articleTitle: DefaultUser
second_title: Aspose.Words для .NET
description: Откройте для себя свойство DefaultUser для бесшовного управления пользовательской информацией. Повысьте эффективность своего приложения с помощью наших простых в использовании функций!
type: docs
weight: 20
url: /ru/net/aspose.words.fields/userinformation/defaultuser/
---
## UserInformation.DefaultUser property

Информация о пользователе по умолчанию.

```csharp
public static UserInformation DefaultUser { get; }
```

## Примечания

Используйте[`CurrentUser`](../../fieldoptions/currentuser/) свойство для указания информации о пользователе для одного документа.

## Примеры

Показывает, как задать данные пользователя и отобразить их с помощью полей.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Создайте объект UserInformation и установите его в качестве источника данных для полей, отображающих информацию о пользователе.
UserInformation userInformation = new UserInformation
{
    Name = "John Doe",
    Initials = "J. D.",
    Address = "123 Main Street"
};
doc.FieldOptions.CurrentUser = userInformation;

// Вставьте поля USERNAME, USERINITIALS и USERADDRESS, которые отображают значения
 // соответствующие свойства объекта UserInformation, который мы создали выше.
Assert.AreEqual(userInformation.Name, builder.InsertField(" USERNAME ").Result);
Assert.AreEqual(userInformation.Initials, builder.InsertField(" USERINITIALS ").Result);
Assert.AreEqual(userInformation.Address, builder.InsertField(" USERADDRESS ").Result);

// Объект параметров поля также имеет статического пользователя по умолчанию, на которого могут ссылаться поля из всех документов.
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

### Смотрите также

* class [UserInformation](../)
* пространство имен [Aspose.Words.Fields](../../../aspose.words.fields/)
* сборка [Aspose.Words](../../../)
