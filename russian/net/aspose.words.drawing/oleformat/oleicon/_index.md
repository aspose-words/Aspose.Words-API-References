---
title: OleFormat.OleIcon
linktitle: OleIcon
articleTitle: OleIcon
second_title: Aspose.Words для .NET
description: Откройте для себя свойство OleFormat OleIcon, управляйте отображением объектов OLE в виде значков или контента для улучшения пользовательского опыта и бесшовной интеграции в ваши приложения.
type: docs
weight: 70
url: /ru/net/aspose.words.drawing/oleformat/oleicon/
---
## OleFormat.OleIcon property

Получает аспект рисования объекта OLE. Когда`истинный` объект OLE отображается как значок. Когда`ЛОЖЬ` , объект OLE отображается как content.

```csharp
public bool OleIcon { get; }
```

## Примечания

Aspose.Words не позволяет устанавливать это свойство, чтобы избежать путаницы. Если бы вы могли изменить аспект рисования в Aspose.Words, Microsoft Word все равно отображал бы объект OLE в его оригинальном аспекте рисования, пока вы не отредактируете или не обновите объект OLE в Microsoft Word.

## Примеры

Показывает, как вставлять связанные и несвязанные объекты OLE.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Внедряем рисунок Microsoft Visio в документ как объект OLE.
builder.InsertOleObject(ImageDir + "Microsoft Visio drawing.vsd", "Package", false, false, null);

// Вставляем ссылку на файл в локальной файловой системе и отображаем ее в виде значка.
builder.InsertOleObject(ImageDir + "Microsoft Visio drawing.vsd", "Package", true, true, null);

// Вставка объектов OLE создает фигуры, хранящие эти объекты.
Shape[] shapes = doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>().ToArray();

Assert.AreEqual(2, shapes.Length);
Assert.AreEqual(2, shapes.Count(s => s.ShapeType == ShapeType.OleObject));

// Если фигура содержит объект OLE, у нее будет допустимое свойство "OleFormat",
// который мы можем использовать для проверки некоторых аспектов формы.
OleFormat oleFormat = shapes[0].OleFormat;

Assert.AreEqual(false, oleFormat.IsLink);
Assert.AreEqual(false, oleFormat.OleIcon);

oleFormat = shapes[1].OleFormat;

Assert.AreEqual(true, oleFormat.IsLink);
Assert.AreEqual(true, oleFormat.OleIcon);

Assert.True(oleFormat.SourceFullName.EndsWith(@"Images" + Path.DirectorySeparatorChar + "Microsoft Visio drawing.vsd"));
Assert.AreEqual("", oleFormat.SourceItem);

Assert.AreEqual("Microsoft Visio drawing.vsd", oleFormat.IconCaption);

doc.Save(ArtifactsDir + "Shape.OleLinks.docx");

// Если объект содержит данные OLE, мы можем получить к нему доступ с помощью потока.
using (MemoryStream stream = oleFormat.GetOleEntry("\x0001CompObj"))
{
    byte[] oleEntryBytes = stream.ToArray();
    Assert.AreEqual(76, oleEntryBytes.Length);
}
```

### Смотрите также

* class [OleFormat](../)
* пространство имен [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* сборка [Aspose.Words](../../../)
