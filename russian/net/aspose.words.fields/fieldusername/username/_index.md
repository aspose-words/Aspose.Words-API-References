---
title: FieldUserName.UserName
linktitle: UserName
articleTitle: UserName
second_title: Aspose.Words для .NET
description: Управляйте именем текущего пользователя без усилий с помощью свойства FieldUserName. Улучшайте пользовательский опыт и персонализируйте взаимодействия без проблем.
type: docs
weight: 20
url: /ru/net/aspose.words.fields/fieldusername/username/
---
## FieldUserName.UserName property

Указывает или устанавливает имя текущего пользователя.

```csharp
public string UserName { get; set; }
```

## Примеры

Показывает, как использовать поле USERNAME.

```csharp
Document doc = new Document();

// Создаем объект UserInformation и устанавливаем его как источник информации о пользователе для любых полей, которые мы создаем.
UserInformation userInformation = new UserInformation();
userInformation.Name = "John Doe";
doc.FieldOptions.CurrentUser = userInformation;

DocumentBuilder builder = new DocumentBuilder(doc);

// Создаем поле USERNAME для отображения имени текущего пользователя,
// взято из объекта UserInformation, который мы создали выше.
FieldUserName fieldUserName = (FieldUserName)builder.InsertField(FieldType.FieldUserName, true);
Assert.AreEqual(userInformation.Name, fieldUserName.Result);

Assert.AreEqual(" USERNAME ", fieldUserName.GetFieldCode());
Assert.AreEqual("John Doe", fieldUserName.Result);

 // Мы можем задать это свойство, чтобы наше поле переопределяло значение, которое в данный момент хранится в объекте UserInformation.
fieldUserName.UserName = "Jane Doe";
fieldUserName.Update();

Assert.AreEqual(" USERNAME  \"Jane Doe\"", fieldUserName.GetFieldCode());
Assert.AreEqual("Jane Doe", fieldUserName.Result);

// Это не влияет на значение в объекте UserInformation.
Assert.AreEqual("John Doe", doc.FieldOptions.CurrentUser.Name);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.USERNAME.docx");
```

### Смотрите также

* class [FieldUserName](../)
* пространство имен [Aspose.Words.Fields](../../../aspose.words.fields/)
* сборка [Aspose.Words](../../../)
