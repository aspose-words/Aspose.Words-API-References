---
title: OlePackage
second_title: Справочник по API Aspose.Words для .NET
description: Предоставить доступ кOlePackageaspose.words.drawing/olepackage если объект OLE является пакетом OLE. В противном случае возвращает null.
type: docs
weight: 80
url: /ru/net/aspose.words.drawing/oleformat/olepackage/
---
## OleFormat.OlePackage property

Предоставить доступ к[`OlePackage`](../../olepackage) если объект OLE является пакетом OLE. В противном случае возвращает null.

```csharp
public OlePackage OlePackage { get; }
```

### Примечания

OLE Package — это устаревшая технология, позволяющая оборачивать любой формат файла, отсутствующий в реестре OLE системы Windows, в универсальный пакет, позволяющий встраивать в документ практически все, что угодно. См.[`OlePackage`](../../olepackage)введите для получения дополнительной информации.

### Примеры

Показывает, как вставить объект OLE в документ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Объекты OLE позволяют нам открывать другие файлы в локальной файловой системе с помощью другого установленного приложения
// в нашей операционной системе, дважды щелкнув фигуру, содержащую объект OLE в теле документа.
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

* class [OlePackage](../../olepackage)
* class [OleFormat](../../oleformat)
* пространство имен [Aspose.Words.Drawing](../../oleformat)
* сборка [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->