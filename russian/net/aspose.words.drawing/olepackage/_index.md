---
title: OlePackage Class
linktitle: OlePackage
articleTitle: OlePackage
second_title: Aspose.Words для .NET
description: Изучите класс Aspose.Words.Drawing.OlePackage, чтобы легко управлять свойствами пакета OLE и расширить возможности обработки документов.
type: docs
weight: 1540
url: /ru/net/aspose.words.drawing/olepackage/
---
## OlePackage class

Позволяет получить доступ к свойствам пакета OLE.

Чтобы узнать больше, посетите[Работа с Ole-объектами](https://docs.aspose.com/words/net/working-with-ole-objects/) документальная статья.

```csharp
public class OlePackage
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [DisplayName](../../aspose.words.drawing/olepackage/displayname/) { get; set; } | Возвращает или задает отображаемое имя пакета OLE. |
| [FileName](../../aspose.words.drawing/olepackage/filename/) { get; set; } | Возвращает или задает имя файла пакета OLE. |

## Примечания

Пакет OLE — это устаревший и «недокументированный» способ хранения внедренных объектов, если обработчик OLE неизвестен. Ранние версии Windows, такие как Windows 3.1, 95 и 98, имели приложение Packager.exe, которое можно было использовать для внедрения любого типа данных в документ. Теперь это приложение исключено из Windows, но MS Word и другие приложения по-прежнему используют его для внедрения данных, если обработчик OLE отсутствует или неизвестен.

## Примеры

Показывает, как вставить объект OLE в документ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Объекты OLE позволяют нам открывать другие файлы в локальной файловой системе с помощью другого установленного приложения
// в нашей операционной системе, дважды щелкнув по фигуре, содержащей объект OLE в теле документа.
// В этом случае наш внешний файл будет ZIP-архивом.
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
