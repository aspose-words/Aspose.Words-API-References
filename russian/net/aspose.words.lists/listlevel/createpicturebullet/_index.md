---
title: ListLevel.CreatePictureBullet
linktitle: CreatePictureBullet
articleTitle: CreatePictureBullet
second_title: Aspose.Words для .NET
description: Откройте для себя метод ListLevel CreatePictureBullet, который позволит вам легко дополнить свои списки пользовательскими маркерами изображений, добавив им визуальной привлекательности и ясности.
type: docs
weight: 150
url: /ru/net/aspose.words.lists/listlevel/createpicturebullet/
---
## ListLevel.CreatePictureBullet method

Создает форму маркера изображения для текущего уровня списка.

```csharp
public void CreatePictureBullet()
```

## Примечания

Пожалуйста, обрати внимание,[`NumberStyle`](../numberstyle/) будет установлен наBullet и [`NumberFormat`](../numberformat/) на "\xF0B7" для правильного отображения маркера изображения. Изображение красного креста будет установлено в качестве маркера изображения при создании. Чтобы изменить его, используйте[`ImageData`](../imagedata/).

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
