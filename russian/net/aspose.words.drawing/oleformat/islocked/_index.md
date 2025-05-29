---
title: OleFormat.IsLocked
linktitle: IsLocked
articleTitle: IsLocked
second_title: Aspose.Words для .NET
description: Откройте для себя свойство OleFormat IsLocked, управляйте связями объектов OLE и повышайте целостность данных, предотвращая нежелательные обновления. Узнайте больше прямо сейчас!
type: docs
weight: 50
url: /ru/net/aspose.words.drawing/oleformat/islocked/
---
## OleFormat.IsLocked property

Указывает, заблокирована ли ссылка на объект OLE от обновлений.

```csharp
public bool IsLocked { get; set; }
```

## Примечания

Значение по умолчанию:`ЛОЖЬ`.

## Примеры

Показывает, как извлекать встроенные OLE-объекты в файлы.

```csharp
Document doc = new Document(MyDir + "OLE spreadsheet.docm");
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

// Объект OLE в первой форме — это электронная таблица Microsoft Excel.
OleFormat oleFormat = shape.OleFormat;

Assert.AreEqual("Excel.Sheet.12", oleFormat.ProgId);

// Наш объект не обновляется автоматически и не заблокирован от обновлений.
Assert.False(oleFormat.AutoUpdate);
Assert.AreEqual(false, oleFormat.IsLocked);

// Если мы планируем сохранить объект OLE в файл в локальной файловой системе,
// мы можем использовать свойство "SuggestedExtension", чтобы определить, какое расширение файла применить к файлу.
Assert.AreEqual(".xlsx", oleFormat.SuggestedExtension);

// Ниже приведены два способа сохранения объекта OLE в файл в локальной файловой системе.
// 1 - Сохранить через поток:
using (FileStream fs = new FileStream(ArtifactsDir + "OLE spreadsheet extracted via stream" + oleFormat.SuggestedExtension, FileMode.Create))
{
    oleFormat.Save(fs);
}

// 2 - Сохранить его непосредственно в файле:
oleFormat.Save(ArtifactsDir + "OLE spreadsheet saved directly" + oleFormat.SuggestedExtension);
```

### Смотрите также

* class [OleFormat](../)
* пространство имен [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* сборка [Aspose.Words](../../../)
