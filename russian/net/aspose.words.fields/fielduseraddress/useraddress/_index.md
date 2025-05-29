---
title: FieldUserAddress.UserAddress
linktitle: UserAddress
articleTitle: UserAddress
second_title: Aspose.Words для .NET
description: Управляйте почтовыми адресами пользователей без усилий с помощью свойства FieldUserAddress. Легко извлекайте и обновляйте информацию о текущем пользователе для улучшения опыта.
type: docs
weight: 20
url: /ru/net/aspose.words.fields/fielduseraddress/useraddress/
---
## FieldUserAddress.UserAddress property

Возвращает или задает почтовый адрес текущего пользователя.

```csharp
public string UserAddress { get; set; }
```

## Примеры

Показывает, как использовать поле USERADDRESS.

```csharp
Document doc = new Document();

// Создаем объект UserInformation и устанавливаем его как источник информации о пользователе для любых полей, которые мы создаем.
UserInformation userInformation = new UserInformation();
userInformation.Address = "123 Main Street";
doc.FieldOptions.CurrentUser = userInformation;

// Создаем поле USERADDRESS для отображения адреса текущего пользователя,
// взято из объекта UserInformation, который мы создали выше.
DocumentBuilder builder = new DocumentBuilder(doc);
FieldUserAddress fieldUserAddress = (FieldUserAddress)builder.InsertField(FieldType.FieldUserAddress, true);
Assert.AreEqual(" USERADDRESS ", fieldUserAddress.GetFieldCode());
Assert.AreEqual("123 Main Street", fieldUserAddress.Result);

// Мы можем задать это свойство, чтобы наше поле переопределяло значение, которое в данный момент хранится в объекте UserInformation.
fieldUserAddress.UserAddress = "456 North Road";
fieldUserAddress.Update();

Assert.AreEqual(" USERADDRESS  \"456 North Road\"", fieldUserAddress.GetFieldCode());
Assert.AreEqual("456 North Road", fieldUserAddress.Result);

// Это не влияет на значение в объекте UserInformation.
Assert.AreEqual("123 Main Street", doc.FieldOptions.CurrentUser.Address);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.USERADDRESS.docx");
```

### Смотрите также

* class [FieldUserAddress](../)
* пространство имен [Aspose.Words.Fields](../../../aspose.words.fields/)
* сборка [Aspose.Words](../../../)
