---
title: OleFormat.SuggestedExtension
second_title: Справочник по API Aspose.Words для .NET
description: OleFormat свойство. Получает расширение файла предложенное для текущего внедренного объекта если вы хотите сохранить его в файл.
type: docs
weight: 120
url: /ru/net/aspose.words.drawing/oleformat/suggestedextension/
---
## OleFormat.SuggestedExtension property

Получает расширение файла, предложенное для текущего внедренного объекта, если вы хотите сохранить его в файл.

```csharp
public string SuggestedExtension { get; }
```

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


