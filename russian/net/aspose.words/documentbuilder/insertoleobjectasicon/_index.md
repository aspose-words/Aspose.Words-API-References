---
title: DocumentBuilder.InsertOleObjectAsIcon
linktitle: InsertOleObjectAsIcon
articleTitle: InsertOleObjectAsIcon
second_title: Aspose.Words для .NET
description: Легко вставляйте объекты OLE в виде значков в свои документы с помощью DocumentBuilder. Настраивайте значки и подписи, обеспечивая при этом бесшовную интеграцию.
type: docs
weight: 430
url: /ru/net/aspose.words/documentbuilder/insertoleobjectasicon/
---
## InsertOleObjectAsIcon(*string, bool, string, string*) {#insertoleobjectasicon_1}

Вставляет встроенный или связанный объект OLE как значок в документ. Позволяет указать файл значка и подпись. Определяет тип объекта OLE по расширению файла.

```csharp
public Shape InsertOleObjectAsIcon(string fileName, bool isLinked, string iconFile, 
    string iconCaption)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| fileName | String | Полный путь к файлу. |
| isLinked | Boolean | Если`истинный` затем вставляется связанный объект OLE, в противном случае вставляется встроенный объект OLE. |
| iconFile | String | Полный путь к файлу ICO. Если значение равно`нулевой` , Aspose.Words будет использовать предопределенное изображение. |
| iconCaption | String | Подпись к иконке. Если значение равно`нулевой` , Aspose.Words будет использовать имя файла . |

### Возвращаемое значение

Узел формы, содержащий объект Ole и вставленный в текущую позицию Builder.

## Примеры

Показывает, как вставить объект OLE в документ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Объекты OLE — это ссылки на файлы в нашей локальной файловой системе, которые могут быть открыты другими установленными приложениями.
// Двойной щелчок по этим фигурам запустит приложение, а затем воспользуйтесь им для открытия связанного объекта.
// Существует три способа использования метода InsertOleObject для вставки этих фигур и настройки их внешнего вида.
// 1 - Изображение взято из локальной файловой системы:
using (FileStream imageStream = new FileStream(ImageDir + "Logo.jpg", FileMode.Open))
{
    // Если 'presentation' пропущено и установлено 'asIcon', этот перегруженный метод выбирает
    // значок в соответствии с расширением файла и использует имя файла для подписи значка.
    builder.InsertOleObject(MyDir + "Spreadsheet.xlsx", false, false, imageStream); 
}

// Если 'presentation' пропущено и установлено 'asIcon', этот перегруженный метод выбирает
// значок в соответствии с 'progId' и использует имя файла для подписи значка.
// 2 — Значок на основе приложения, которое откроет объект:
builder.InsertOleObject(MyDir + "Spreadsheet.xlsx", "Excel.Sheet", false, true, null);

// Если 'iconFile' и 'iconCaption' опущены, этот перегруженный метод выбирает
// значок в соответствии с 'progId' и использует предопределенную подпись значка.
// 3 — Значок изображения размером 32 x 32 пикселя или меньше из локальной файловой системы с пользовательской подписью:
builder.InsertOleObjectAsIcon(MyDir + "Presentation.pptx", false, ImageDir + "Logo icon.ico",
    "Double click to view presentation!");

doc.Save(ArtifactsDir + "DocumentBuilder.InsertOleObject.docx");
```

### Смотрите также

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)

---

## InsertOleObjectAsIcon(*string, string, bool, string, string*) {#insertoleobjectasicon_2}

Вставляет встроенный или связанный объект OLE как значок в документ. Позволяет указать файл значка и подпись. Определяет тип объекта OLE с использованием заданного параметра progID.

```csharp
public Shape InsertOleObjectAsIcon(string fileName, string progId, bool isLinked, string iconFile, 
    string iconCaption)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| fileName | String | Полный путь к файлу. |
| progId | String | ProgId объекта OLE. |
| isLinked | Boolean | Если`истинный` затем вставляется связанный объект OLE, в противном случае вставляется встроенный объект OLE. |
| iconFile | String | Полный путь к файлу ICO. Если значение равно`нулевой` , Aspose.Words будет использовать предопределенное изображение. |
| iconCaption | String | Подпись к иконке. Если значение равно`нулевой` , Aspose.Words будет использовать имя файла . |

### Возвращаемое значение

Узел формы, содержащий объект Ole и вставленный в текущую позицию Builder.

## Примеры

Показывает, как вставить встроенный или связанный объект OLE в качестве значка в документ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Если 'iconFile' и 'iconCaption' опущены, этот перегруженный метод выбирает
// значок в соответствии с 'progId' и использует имя файла для подписи значка.
builder.InsertOleObjectAsIcon(MyDir + "Presentation.pptx", "Package", false, ImageDir + "Logo icon.ico", "My embedded file");

builder.InsertBreak(BreakType.LineBreak);

using (FileStream stream = new FileStream(MyDir + "Presentation.pptx", FileMode.Open))
{
    // Если 'iconFile' и 'iconCaption' опущены, этот перегруженный метод выбирает
    // значок в соответствии с расширением файла и использует имя файла для подписи значка.
    Shape shape = builder.InsertOleObjectAsIcon(stream, "PowerPoint.Application", ImageDir + "Logo icon.ico",
        "My embedded file stream");

    OlePackage setOlePackage = shape.OleFormat.OlePackage;
    setOlePackage.FileName = "Presentation.pptx";
    setOlePackage.DisplayName = "Presentation.pptx";
}

doc.Save(ArtifactsDir + "DocumentBuilder.InsertOleObjectAsIcon.docx");
```

### Смотрите также

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)

---

## InsertOleObjectAsIcon(*Stream, string, string, string*) {#insertoleobjectasicon}

Вставляет встроенный объект OLE как значок из потока в документ. Позволяет указать файл значка и подпись. Определяет тип объекта OLE с использованием заданного параметра progID.

```csharp
public Shape InsertOleObjectAsIcon(Stream stream, string progId, string iconFile, 
    string iconCaption)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| stream | Stream | Поток, содержащий данные приложения. |
| progId | String | ProgId объекта OLE. |
| iconFile | String | Полный путь к файлу ICO. Если значение равно`нулевой` , Aspose.Words будет использовать предопределенное изображение. |
| iconCaption | String | Подпись к иконке. Если значение равно`нулевой` , Aspose.Words будет использовать предопределенную подпись значка. |

### Возвращаемое значение

Узел формы, содержащий объект Ole и вставленный в текущую позицию Builder.

## Примеры

Показывает, как вставить встроенный или связанный объект OLE в качестве значка в документ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Если 'iconFile' и 'iconCaption' опущены, этот перегруженный метод выбирает
// значок в соответствии с 'progId' и использует имя файла для подписи значка.
builder.InsertOleObjectAsIcon(MyDir + "Presentation.pptx", "Package", false, ImageDir + "Logo icon.ico", "My embedded file");

builder.InsertBreak(BreakType.LineBreak);

using (FileStream stream = new FileStream(MyDir + "Presentation.pptx", FileMode.Open))
{
    // Если 'iconFile' и 'iconCaption' опущены, этот перегруженный метод выбирает
    // значок в соответствии с расширением файла и использует имя файла для подписи значка.
    Shape shape = builder.InsertOleObjectAsIcon(stream, "PowerPoint.Application", ImageDir + "Logo icon.ico",
        "My embedded file stream");

    OlePackage setOlePackage = shape.OleFormat.OlePackage;
    setOlePackage.FileName = "Presentation.pptx";
    setOlePackage.DisplayName = "Presentation.pptx";
}

doc.Save(ArtifactsDir + "DocumentBuilder.InsertOleObjectAsIcon.docx");
```

### Смотрите также

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
