---
title: FieldOptions.CurrentUser
second_title: Справочник по API Aspose.Words для .NET
description: FieldOptions свойство. Получает или задает информацию о текущем пользователе.
type: docs
weight: 50
url: /ru/net/aspose.words.fields/fieldoptions/currentuser/
---
## FieldOptions.CurrentUser property

Получает или задает информацию о текущем пользователе.

```csharp
public UserInformation CurrentUser { get; set; }
```

### Примеры

Показывает, как задать сведения о пользователе и отобразить их с помощью полей.

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

// Вставляем поля USERNAME, USERINITIALS и USERADDRESS, которые отображают значения
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

* class [UserInformation](../../userinformation/)
* class [FieldOptions](../)
* пространство имен [Aspose.Words.Fields](../../fieldoptions/)
* сборка [Aspose.Words](../../../)


