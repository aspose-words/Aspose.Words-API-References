---
title: OleFormat.ProgId
second_title: Справочник по API Aspose.Words для .NET
description: OleFormat свойство. Получает или задает ProgID объекта OLE.
type: docs
weight: 90
url: /ru/net/aspose.words.drawing/oleformat/progid/
---
## OleFormat.ProgId property

Получает или задает ProgID объекта OLE.

```csharp
public string ProgId { get; set; }
```

### Примечания

Свойство ProgID не всегда присутствует в документах Microsoft Word, и на него нельзя полагаться.

Не может быть нулевым.

Значение по умолчанию — пустая строка.

### Примеры

Показывает, как извлекать встроенные объекты OLE в файлы.

```csharp
Document doc = new Document(MyDir + "OLE spreadsheet.docm");
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

// Объект OLE в первой фигуре — это электронная таблица Microsoft Excel.
OleFormat oleFormat = shape.OleFormat;

Assert.AreEqual("Excel.Sheet.12", oleFormat.ProgId);

// Наш объект не обновляется автоматически и не заблокирован от обновлений.
Assert.False(oleFormat.AutoUpdate);
Assert.AreEqual(false, oleFormat.IsLocked);

// Если мы планируем сохранить объект OLE в файл в локальной файловой системе,
// мы можем использовать свойство "SuggestedExtension", чтобы определить, какое расширение файла применить к файлу.
Assert.AreEqual(".xlsx", oleFormat.SuggestedExtension);

// Ниже приведены два способа сохранения объекта OLE в файл в локальной файловой системе.
// 1 - Сохраняем через поток:
using (FileStream fs = new FileStream(ArtifactsDir + "OLE spreadsheet extracted via stream" + oleFormat.SuggestedExtension, FileMode.Create))
{
    oleFormat.Save(fs);
}

// 2 - Сохраните его прямо в имя файла:
oleFormat.Save(ArtifactsDir + "OLE spreadsheet saved directly" + oleFormat.SuggestedExtension);
```

### Смотрите также

* class [OleFormat](../)
* пространство имен [Aspose.Words.Drawing](../../oleformat/)
* сборка [Aspose.Words](../../../)


