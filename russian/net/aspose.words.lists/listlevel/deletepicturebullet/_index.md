---
title: ListLevel.DeletePictureBullet
second_title: Справочник по API Aspose.Words для .NET
description: ListLevel метод. Удаляет маркер изображения для текущего уровня списка.
type: docs
weight: 160
url: /ru/net/aspose.words.lists/listlevel/deletepicturebullet/
---
## ListLevel.DeletePictureBullet method

Удаляет маркер изображения для текущего уровня списка.

```csharp
public void DeletePictureBullet()
```

### Примечания

Пуля по умолчанию будет отображаться после удаления.

### Примеры

Показывает, как установить пользовательский значок изображения для меток элементов списка.

```csharp
Document doc = new Document();

List list = doc.Lists.Add(ListTemplate.BulletCircle);

// Создаем маркер изображения для текущего уровня списка и устанавливаем изображение из локальной файловой системы
// в качестве значка, который будут отображать маркеры для этого уровня списка.
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
* пространство имен [Aspose.Words.Lists](../../listlevel/)
* сборка [Aspose.Words](../../../)


