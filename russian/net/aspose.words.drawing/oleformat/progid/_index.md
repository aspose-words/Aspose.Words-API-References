---
title: OleFormat.ProgId
linktitle: ProgId
articleTitle: ProgId
second_title: Aspose.Words для .NET
description: OleFormat ProgId свойство. Получает или задает ProgID объекта OLE на С#.
type: docs
weight: 90
url: /ru/net/aspose.words.drawing/oleformat/progid/
---
## OleFormat.ProgId property

Получает или задает ProgID объекта OLE.

```csharp
public string ProgId { get; set; }
```

## Примечания

Свойство ProgID не всегда присутствует в документах Microsoft Word, и на него нельзя полагаться.

Не может быть`нулевой`.

Значение по умолчанию — пустая строка.

## Примеры

Показывает, как извлечь внедренные объекты OLE в файлы.

```csharp
Document doc = new Document(MyDir + "OLE spreadsheet.docm");
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

// Объект OLE в первой фигуре — это электронная таблица Microsoft Excel.
OleFormat oleFormat = shape.OleFormat;

Assert.AreEqual("Excel.Sheet.12", oleFormat.ProgId);

// Наш объект не является ни автоматически обновляемым, ни заблокированным от обновлений.
Assert.False(oleFormat.AutoUpdate);
Assert.AreEqual(false, oleFormat.IsLocked);

// Если мы планируем сохранить объект OLE в файл в локальной файловой системе,
// мы можем использовать свойство «SuggestedExtension», чтобы определить, какое расширение файла применить к файлу.
Assert.AreEqual(".xlsx", oleFormat.SuggestedExtension);

// Ниже приведены два способа сохранения объекта OLE в файл локальной файловой системы.
// 1 - Сохранить через поток:
using (FileStream fs = new FileStream(ArtifactsDir + "OLE spreadsheet extracted via stream" + oleFormat.SuggestedExtension, FileMode.Create))
{
    oleFormat.Save(fs);
}

// 2 - Сохраняем непосредственно в файл:
oleFormat.Save(ArtifactsDir + "OLE spreadsheet saved directly" + oleFormat.SuggestedExtension);
```

### Смотрите также

* class [OleFormat](../)
* пространство имен [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* сборка [Aspose.Words](../../../)
