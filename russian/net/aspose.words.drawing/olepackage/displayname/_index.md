---
title: OlePackage.DisplayName
linktitle: DisplayName
articleTitle: DisplayName
second_title: Aspose.Words для .NET
description: Откройте для себя свойство OlePackage DisplayName для простого управления отображаемыми именами пакетов OLE. Улучшите организацию данных с помощью этой ключевой функции.
type: docs
weight: 10
url: /ru/net/aspose.words.drawing/olepackage/displayname/
---
## OlePackage.DisplayName property

Возвращает или задает отображаемое имя пакета OLE.

```csharp
public string DisplayName { get; set; }
```

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

* class [OlePackage](../)
* пространство имен [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* сборка [Aspose.Words](../../../)
