---
title: OleFormat.SourceFullName
linktitle: SourceFullName
articleTitle: SourceFullName
second_title: Aspose.Words для .NET
description: Откройте для себя свойство OleFormat SourceFullName, легко управляйте путем и именем исходного файла связанного OLE-объекта для бесшовной интеграции.
type: docs
weight: 100
url: /ru/net/aspose.words.drawing/oleformat/sourcefullname/
---
## OleFormat.SourceFullName property

Возвращает или задает путь и имя исходного файла для связанного объекта OLE.

```csharp
public string SourceFullName { get; set; }
```

## Примечания

Значение по умолчанию — пустая строка.

Если`SourceFullName` не является пустой строкой, объект OLE связан.

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
