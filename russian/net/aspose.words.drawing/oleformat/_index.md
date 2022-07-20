---
title: OleFormat
second_title: Справочник по API Aspose.Words для .NET
description: Предоставляет доступ к данным объекта OLE или элемента управления ActiveX.
type: docs
weight: 1020
url: /ru/net/aspose.words.drawing/oleformat/
---
## OleFormat class

Предоставляет доступ к данным объекта OLE или элемента управления ActiveX.

```csharp
public class OleFormat
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [AutoUpdate](../../aspose.words.drawing/oleformat/autoupdate) { get; set; } | Указывает, будет ли автоматически обновляться ссылка на объект OLE в Microsoft Word. |
| [Clsid](../../aspose.words.drawing/oleformat/clsid) { get; } | Получает CLSID объекта OLE. |
| [IconCaption](../../aspose.words.drawing/oleformat/iconcaption) { get; } | Получает заголовок значка объекта OLE. |
| [IsLink](../../aspose.words.drawing/oleformat/islink) { get; } | Возвращает значение true, если объект OLE связан (когда[`SourceFullName`](./sourcefullname) указано). |
| [IsLocked](../../aspose.words.drawing/oleformat/islocked) { get; set; } | Указывает, заблокирована ли ссылка на объект OLE от обновлений. |
| [OleControl](../../aspose.words.drawing/oleformat/olecontrol) { get; } | получает[`OleControl`](./olecontrol) объекты, если этот объект OLE является элементом управления ActiveX. В противном случае это свойство равно null. |
| [OleIcon](../../aspose.words.drawing/oleformat/oleicon) { get; } | Получает аспект отрисовки объекта OLE. Когда **истинный** , объект OLE отображается в виде значка. Когда **ЛОЖЬ** , объект OLE отображается как содержимое. |
| [OlePackage](../../aspose.words.drawing/oleformat/olepackage) { get; } | Предоставить доступ к[`OlePackage`](../olepackage) если объект OLE является пакетом OLE. В противном случае возвращает null. |
| [ProgId](../../aspose.words.drawing/oleformat/progid) { get; set; } | Получает или задает ProgID объекта OLE. |
| [SourceFullName](../../aspose.words.drawing/oleformat/sourcefullname) { get; set; } | Получает или задает путь и имя исходного файла для связанного объекта OLE. |
| [SourceItem](../../aspose.words.drawing/oleformat/sourceitem) { get; set; } | Получает или задает строку, которая используется для идентификации части исходного файла, на которую делается ссылка. |
| [SuggestedExtension](../../aspose.words.drawing/oleformat/suggestedextension) { get; } | Получает расширение файла, предложенное для текущего внедренного объекта, если вы хотите сохранить его в файл. |
| [SuggestedFileName](../../aspose.words.drawing/oleformat/suggestedfilename) { get; } | Получает имя файла, предложенное для текущего встроенного объекта, если вы хотите сохранить его в файл. |

## Методы

| Имя | Описание |
| --- | --- |
| [GetOleEntry](../../aspose.words.drawing/oleformat/getoleentry)(string) | Получает запись данных объекта OLE. |
| [GetRawData](../../aspose.words.drawing/oleformat/getrawdata)() | Получает необработанные данные объекта OLE. |
| [Save](../../aspose.words.drawing/oleformat/save#save)(Stream) | Сохраняет данные встроенного объекта в указанный поток. |
| [Save](../../aspose.words.drawing/oleformat/save#save_1)(string) | Сохраняет данные внедренного объекта в файл с указанным именем. |

### Примечания

Использовать[`OleFormat`](../shape/oleformat) свойство для доступа к данным объекта OLE. Вы не создаете экземпляры[`OleFormat`](../oleformat) класс напрямую.

### Примеры

Показывает, как извлекать встроенные объекты OLE в файлы.

```csharp
Document doc = new Document(MyDir + "OLE spreadsheet.docm");
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

// Объект OLE в первой фигуре — это электронная таблица Microsoft Excel.
OleFormat oleFormat = shape.OleFormat;

Assert.AreEqual("Excel.Sheet.12", oleFormat.ProgId);

// Наш объект не обновляется автоматически и не заблокирован от обновлений.
Assert.False(oleFormat.AutoUpdate);
Assert.AreEqual(false, oleFormat.IsLocked);

// Если мы планируем сохранить объект OLE в файл в локальной файловой системе,
// мы можем использовать свойство "SuggestedExtension", чтобы определить, какое расширение файла применить к файлу.
Assert.AreEqual(".xlsx", oleFormat.SuggestedExtension);

// Ниже приведены два способа сохранения объекта OLE в файл в локальной файловой системе.
// 1 - Сохраняем через поток:
using (FileStream fs = new FileStream(ArtifactsDir + "OLE spreadsheet extracted via stream" + oleFormat.SuggestedExtension, FileMode.Create))
{
    oleFormat.Save(fs);
}

// 2 - Сохраните его прямо в имя файла:
oleFormat.Save(ArtifactsDir + "OLE spreadsheet saved directly" + oleFormat.SuggestedExtension);
```

### Смотрите также

* пространство имен [Aspose.Words.Drawing](../../aspose.words.drawing)
* сборка [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->