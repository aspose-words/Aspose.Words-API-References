---
title: Class OlePackage
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.Drawing.OlePackage сорт. Разрешает доступ к свойствам пакета OLE.
type: docs
weight: 1160
url: /ru/net/aspose.words.drawing/olepackage/
---
## OlePackage class

Разрешает доступ к свойствам пакета OLE.

Чтобы узнать больше, посетите[Работа с объектами Ole](https://docs.aspose.com/words/net/working-with-ole-objects/) статья документации.

```csharp
public class OlePackage
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [DisplayName](../../aspose.words.drawing/olepackage/displayname/) { get; set; } | Получает или задает отображаемое имя пакета OLE. |
| [FileName](../../aspose.words.drawing/olepackage/filename/) { get; set; } | Получает или задает имя файла пакета OLE. |

### Примечания

Пакет OLE — это устаревший и «недокументированный» способ хранения встроенного объекта, если обработчик OLE неизвестен. Ранние версии Windows, такие как Windows 3.1, 95 и 98, имели приложение Packager.exe, которое можно было использовать для встраивания данных любого типа в документ. . Теперь это приложение исключено из Windows, но MS Word и другие приложения по-прежнему используют его для встраивания данных, если обработчик OLE отсутствует или неизвестен.

### Примеры

Показывает, как вставить объект OLE в документ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Объекты OLE позволяют нам открывать другие файлы в локальной файловой системе с помощью другого установленного приложения
// в нашей операционной системе, дважды щелкнув фигуру, содержащую объект OLE в теле документа.
// В данном случае наш внешний файл будет ZIP-архивом.
byte[] zipFileBytes = File.ReadAllBytes(DatabaseDir + "cat001.zip");

using (MemoryStream stream = new MemoryStream(zipFileBytes))
{
    Shape shape = builder.InsertOleObject(stream, "Package", true, null);

    shape.OleFormat.OlePackage.FileName = "Package file name.zip";
    shape.OleFormat.OlePackage.DisplayName = "Package display name.zip";
}

doc.Save(ArtifactsDir + "Shape.InsertOlePackage.docx");
```

### Смотрите также

* пространство имен [Aspose.Words.Drawing](../../aspose.words.drawing/)
* сборка [Aspose.Words](../../)


