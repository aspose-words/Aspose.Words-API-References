---
title: FieldUserInitials.UserInitials
linktitle: UserInitials
articleTitle: UserInitials
second_title: Aspose.Words для .NET
description: Получите доступ к свойству FieldUserInitials и настройте его, чтобы легко управлять инициалами пользователей, улучшая персонализацию и пользовательский опыт.
type: docs
weight: 20
url: /ru/net/aspose.words.fields/fielduserinitials/userinitials/
---
## FieldUserInitials.UserInitials property

Получает или задает инициалы текущего пользователя.

```csharp
public string UserInitials { get; set; }
```

## Примеры

Показывает, как использовать поле USERINITIALS.

```csharp
Document doc = new Document();

// Создаем объект UserInformation и устанавливаем его как источник информации о пользователе для любых полей, которые мы создаем.
UserInformation userInformation = new UserInformation();
userInformation.Initials = "J. D.";
doc.FieldOptions.CurrentUser = userInformation;

// Создаем поле USERINITIALS для отображения инициалов текущего пользователя,
// взято из объекта UserInformation, который мы создали выше.
DocumentBuilder builder = new DocumentBuilder(doc);
FieldUserInitials fieldUserInitials = (FieldUserInitials)builder.InsertField(FieldType.FieldUserInitials, true);
Assert.AreEqual(userInformation.Initials, fieldUserInitials.Result);

Assert.AreEqual(" USERINITIALS ", fieldUserInitials.GetFieldCode());
Assert.AreEqual("J. D.", fieldUserInitials.Result);

 // Мы можем задать это свойство, чтобы наше поле переопределяло значение, которое в данный момент хранится в объекте UserInformation.
fieldUserInitials.UserInitials = "J. C.";
fieldUserInitials.Update();

Assert.AreEqual(" USERINITIALS  \"J. C.\"", fieldUserInitials.GetFieldCode());
Assert.AreEqual("J. C.", fieldUserInitials.Result);

// Это не влияет на значение в объекте UserInformation.
Assert.AreEqual("J. D.", doc.FieldOptions.CurrentUser.Initials);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.USERINITIALS.docx");
```

### Смотрите также

* class [FieldUserInitials](../)
* пространство имен [Aspose.Words.Fields](../../../aspose.words.fields/)
* сборка [Aspose.Words](../../../)
