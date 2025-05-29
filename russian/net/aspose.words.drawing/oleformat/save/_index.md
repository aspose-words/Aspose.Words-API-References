---
title: OleFormat.Save
linktitle: Save
articleTitle: Save
second_title: Aspose.Words для .NET
description: Откройте для себя метод OleFormat Save для эффективного хранения данных встроенных объектов в выбранном вами потоке. Улучшите управление данными с легкостью!
type: docs
weight: 160
url: /ru/net/aspose.words.drawing/oleformat/save/
---
## Save(*Stream*) {#save}

Сохраняет данные внедренного объекта в указанный поток.

```csharp
public void Save(Stream stream)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| stream | Stream | Где сохранить данные объекта. |

### Исключения

| исключение | условие |
| --- | --- |
| InvalidOperationException | Вызывается при попытке сохранить связанный объект. |

## Примечания

Ответственность за утилизацию потока лежит на вызывающем абоненте.

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

---

## Save(*string*) {#save_1}

Сохраняет данные внедренного объекта в файл с указанным именем.

```csharp
public void Save(string fileName)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| fileName | String | Имя файла для сохранения данных объекта OLE. |

### Исключения

| исключение | условие |
| --- | --- |
| InvalidOperationException | Вызывается при попытке сохранить связанный объект. |

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
