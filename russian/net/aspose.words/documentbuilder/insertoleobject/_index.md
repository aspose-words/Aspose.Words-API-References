---
title: InsertOleObject
second_title: Справочник по API Aspose.Words для .NET
description: Вставляет встроенный объект OLE из потока в документ.
type: docs
weight: 370
url: /ru/net/aspose.words/documentbuilder/insertoleobject/
---
## InsertOleObject(Stream, string, bool, Stream) {#insertoleobject}

Вставляет встроенный объект OLE из потока в документ.

```csharp
public Shape InsertOleObject(Stream stream, string progId, bool asIcon, Stream presentation)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| stream | Stream | Поток, содержащий данные приложения. |
| progId | String | Программный идентификатор объекта OLE. |
| asIcon | Boolean | Указывает пиктографический или обычный режим вставляемого объекта OLE. |
| presentation | Stream | Представление изображения объекта OLE. Если значение равно null, Aspose.Words будет использовать одно из предопределенных изображений. |

### Возвращаемое значение

Узел формы, содержащий объект Ole и вставленный в текущую позицию Builder.

### Примеры

Показывает, как использовать конструктор документов для встраивания объектов OLE в документ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставляем электронную таблицу Microsoft Excel из локальной файловой системы
// в документ, сохраняя его внешний вид по умолчанию.
using (Stream spreadsheetStream = File.Open(MyDir + "Spreadsheet.xlsx", FileMode.Open))
{
    builder.Writeln("Spreadsheet Ole object:");
    // Если 'presentation' опущено и установлено 'asIcon', этот перегруженный метод выбирает
    // значок в соответствии с 'progId' и использует предопределенный заголовок значка.
    builder.InsertOleObject(spreadsheetStream, "OleObject.xlsx", false, null);
}

// Вставьте презентацию Microsoft Powerpoint как объект OLE.
// На этот раз для значка будет загружено изображение из Интернета.
using (Stream powerpointStream = File.Open(MyDir + "Presentation.pptx", FileMode.Open))
{
    using (WebClient webClient = new WebClient())
    {
        byte[] imgBytes = File.ReadAllBytes(ImageDir + "Logo.jpg");

        using (MemoryStream imageStream = new MemoryStream(imgBytes))
        {
            builder.InsertParagraph();
            builder.Writeln("Powerpoint Ole object:");
            builder.InsertOleObject(powerpointStream, "OleObject.pptx", true, imageStream);
        }
    }
}

// Дважды щелкните эти объекты в Microsoft Word, чтобы открыть
// связанные файлы с помощью соответствующих приложений.
doc.Save(ArtifactsDir + "DocumentBuilder.InsertOleObjects.docx");
```

### Смотрите также

* class [Shape](../../../aspose.words.drawing/shape)
* class [DocumentBuilder](../../documentbuilder)
* пространство имен [Aspose.Words](../../documentbuilder)
* сборка [Aspose.Words](../../../)

---

## InsertOleObject(string, bool, bool, Stream) {#insertoleobject_1}

Вставляет встроенный или связанный объект OLE из файла в документ. Определяет тип объекта OLE, используя расширение файла.

```csharp
public Shape InsertOleObject(string fileName, bool isLinked, bool asIcon, Stream presentation)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| fileName | String | Полный путь к файлу. |
| isLinked | Boolean | Если true, то вставляется связанный объект OLE, в противном случае вставляется встроенный объект OLE. |
| asIcon | Boolean | Указывает пиктографический или обычный режим вставляемого объекта OLE. |
| presentation | Stream | Представление изображения объекта OLE. Если значение равно null, Aspose.Words будет использовать одно из предопределенных изображений. |

### Возвращаемое значение

Узел формы, содержащий объект Ole и вставленный в текущую позицию Builder.

### Примеры

Показывает, как вставить объект OLE в документ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// OLE-объекты — это ссылки на файлы в нашей локальной файловой системе, которые могут быть открыты другими установленными приложениями.
// Двойной щелчок по этим фигурам запустит приложение, а затем использует его для открытия связанного объекта.
// Существует три способа использования метода InsertOleObject для вставки этих фигур и настройки их внешнего вида.
// 1 - Изображение взято из локальной файловой системы:
using (FileStream imageStream = new FileStream(ImageDir + "Logo.jpg", FileMode.Open))
{
    // Если 'presentation' опущено и установлено 'asIcon', этот перегруженный метод выбирает
    // значок в соответствии с расширением файла и использует имя файла для заголовка значка.
    builder.InsertOleObject(MyDir + "Spreadsheet.xlsx", false, false, imageStream); 
}

// Если 'presentation' опущено и установлено 'asIcon', этот перегруженный метод выбирает
// значок в соответствии с 'progId' и использует имя файла для заголовка значка.
// 2 - Иконка на основе приложения, которое будет открывать объект:
builder.InsertOleObject(MyDir + "Spreadsheet.xlsx", "Excel.Sheet", false, true, null);

// Если 'iconFile' и 'iconCaption' опущены, этот перегруженный метод выбирает
// значок в соответствии с 'progId' и использует предопределенный заголовок значка.
// 3 — значок изображения размером 32 x 32 пикселя или меньше из локальной файловой системы с пользовательской подписью:
builder.InsertOleObjectAsIcon(MyDir + "Presentation.pptx", false, ImageDir + "Logo icon.ico",
    "Double click to view presentation!");

doc.Save(ArtifactsDir + "DocumentBuilder.InsertOleObject.docx");
```

### Смотрите также

* class [Shape](../../../aspose.words.drawing/shape)
* class [DocumentBuilder](../../documentbuilder)
* пространство имен [Aspose.Words](../../documentbuilder)
* сборка [Aspose.Words](../../../)

---

## InsertOleObject(string, string, bool, bool, Stream) {#insertoleobject_2}

Вставляет встроенный или связанный объект OLE из файла в документ. Определяет тип объекта OLE, используя заданный параметр progID.

```csharp
public Shape InsertOleObject(string fileName, string progId, bool isLinked, bool asIcon, 
    Stream presentation)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| fileName | String | Полный путь к файлу. |
| progId | String | ProgId объекта OLE. |
| isLinked | Boolean | Если true, то вставляется связанный объект OLE, в противном случае вставляется встроенный объект OLE. |
| asIcon | Boolean | Указывает пиктографический или обычный режим вставляемого объекта OLE. |
| presentation | Stream | Представление изображения объекта OLE. Если значение равно null, Aspose.Words будет использовать одно из предопределенных изображений. |

### Возвращаемое значение

Узел формы, содержащий объект Ole и вставленный в текущую позицию Builder.

### Примеры

Показывает, как вставить объект OLE в документ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// OLE-объекты — это ссылки на файлы в нашей локальной файловой системе, которые могут быть открыты другими установленными приложениями.
// Двойной щелчок по этим фигурам запустит приложение, а затем использует его для открытия связанного объекта.
// Существует три способа использования метода InsertOleObject для вставки этих фигур и настройки их внешнего вида.
// 1 - Изображение взято из локальной файловой системы:
using (FileStream imageStream = new FileStream(ImageDir + "Logo.jpg", FileMode.Open))
{
    // Если 'presentation' опущено и установлено 'asIcon', этот перегруженный метод выбирает
    // значок в соответствии с расширением файла и использует имя файла для заголовка значка.
    builder.InsertOleObject(MyDir + "Spreadsheet.xlsx", false, false, imageStream); 
}

// Если 'presentation' опущено и установлено 'asIcon', этот перегруженный метод выбирает
// значок в соответствии с 'progId' и использует имя файла для заголовка значка.
// 2 - Иконка на основе приложения, которое будет открывать объект:
builder.InsertOleObject(MyDir + "Spreadsheet.xlsx", "Excel.Sheet", false, true, null);

// Если 'iconFile' и 'iconCaption' опущены, этот перегруженный метод выбирает
// значок в соответствии с 'progId' и использует предопределенный заголовок значка.
// 3 — значок изображения размером 32 x 32 пикселя или меньше из локальной файловой системы с пользовательской подписью:
builder.InsertOleObjectAsIcon(MyDir + "Presentation.pptx", false, ImageDir + "Logo icon.ico",
    "Double click to view presentation!");

doc.Save(ArtifactsDir + "DocumentBuilder.InsertOleObject.docx");
```

### Смотрите также

* class [Shape](../../../aspose.words.drawing/shape)
* class [DocumentBuilder](../../documentbuilder)
* пространство имен [Aspose.Words](../../documentbuilder)
* сборка [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
