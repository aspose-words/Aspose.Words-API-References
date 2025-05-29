---
title: OleFormat.OlePackage
linktitle: OlePackage
articleTitle: OlePackage
second_title: Aspose.Words для .NET
description: Получите доступ к свойствам OlePackage для объектов OLE без усилий. Получите бесшовную интеграцию с пакетами OLE и улучшите свои возможности обработки данных.
type: docs
weight: 80
url: /ru/net/aspose.words.drawing/oleformat/olepackage/
---
## OleFormat.OlePackage property

Предоставить доступ к[`OlePackage`](../../olepackage/) если объект OLE является пакетом OLE. Возвращает`нулевой` в противном случае.

```csharp
public OlePackage OlePackage { get; }
```

## Примечания

OLE Package — это устаревшая технология, которая позволяет упаковать любой формат файла, отсутствующий в реестре OLE системы Windows, в универсальный пакет, позволяющий встраивать в документ практически все, что угодно. См.[`OlePackage`](../../olepackage/) для получения дополнительной информации введите .

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

* class [OlePackage](../../olepackage/)
* class [OleFormat](../)
* пространство имен [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* сборка [Aspose.Words](../../../)
