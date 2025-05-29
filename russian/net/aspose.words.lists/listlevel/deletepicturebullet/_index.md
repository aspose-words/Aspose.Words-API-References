---
title: ListLevel.DeletePictureBullet
linktitle: DeletePictureBullet
articleTitle: DeletePictureBullet
second_title: Aspose.Words для .NET
description: Легко удаляйте маркеры изображений из текущего уровня списка с помощью метода ListLevel DeletePictureBullet. Упростите форматирование документов сегодня!
type: docs
weight: 160
url: /ru/net/aspose.words.lists/listlevel/deletepicturebullet/
---
## ListLevel.DeletePictureBullet method

Удаляет маркер изображения для текущего уровня списка.

```csharp
public void DeletePictureBullet()
```

## Примечания

После удаления будет показан маркер по умолчанию.

## Примеры

Показывает, как установить пользовательский значок изображения для меток элементов списка.

```csharp
Document doc = new Document();

List list = doc.Lists.Add(ListTemplate.BulletCircle);

// Создаем маркер-картинку для текущего уровня списка и устанавливаем изображение из локальной файловой системы
// как значок, который будут отображать маркеры для этого уровня списка.
list.ListLevels[0].CreatePictureBullet();
list.ListLevels[0].ImageData.SetImage(ImageDir + "Logo icon.ico");

Assert.IsTrue(list.ListLevels[0].ImageData.HasImage);

DocumentBuilder builder = new DocumentBuilder(doc);

builder.ListFormat.List = list;
builder.Writeln("Hello world!");
builder.Write("Hello again!");

doc.Save(ArtifactsDir + "Lists.CreatePictureBullet.docx");

list.ListLevels[0].DeletePictureBullet();

Assert.IsNull(list.ListLevels[0].ImageData);
```

### Смотрите также

* class [ListLevel](../)
* пространство имен [Aspose.Words.Lists](../../../aspose.words.lists/)
* сборка [Aspose.Words](../../../)
