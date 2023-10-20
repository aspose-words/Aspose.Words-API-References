---
title: OlePackage.FileName
linktitle: FileName
articleTitle: FileName
second_title: Aspose.Words для .NET
description: OlePackage FileName свойство. Получает или задает имя файла пакета OLE на С#.
type: docs
weight: 20
url: /ru/net/aspose.words.drawing/olepackage/filename/
---
## OlePackage.FileName property

Получает или задает имя файла пакета OLE.

```csharp
public string FileName { get; set; }
```

## Примеры

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

* class [OlePackage](../)
* пространство имен [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* сборка [Aspose.Words](../../../)
