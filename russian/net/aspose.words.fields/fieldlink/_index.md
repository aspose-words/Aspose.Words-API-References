---
title: Class FieldLink
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.Fields.FieldLink сорт. Реализует поле ССЫЛКА.
type: docs
weight: 1960
url: /ru/net/aspose.words.fields/fieldlink/
---
## FieldLink class

Реализует поле ССЫЛКА.

```csharp
public class FieldLink : Field
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [FieldLink](fieldlink/)() | Конструктор по умолчанию. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [AutoUpdate](../../aspose.words.fields/fieldlink/autoupdate/) { get; set; } | Получает или задает, следует ли обновлять это поле автоматически. |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Получает текст, представляющий результат отображаемого поля. |
| [End](../../aspose.words.fields/field/end/) { get; } | Получает узел, представляющий конец поля. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Получает[`FieldFormat`](../fieldformat/) объект, предоставляющий типизированный доступ к форматированию поля. |
| [FormatUpdateType](../../aspose.words.fields/fieldlink/formatupdatetype/) { get; set; } | Получает или задает способ обновления форматирования связанного объекта. |
| [InsertAsBitmap](../../aspose.words.fields/fieldlink/insertasbitmap/) { get; set; } | Получает или задает, следует ли вставлять связанный объект в виде растрового изображения. |
| [InsertAsHtml](../../aspose.words.fields/fieldlink/insertashtml/) { get; set; } | Получает или задает, следует ли вставлять связанный объект как текст в формате HTML. |
| [InsertAsPicture](../../aspose.words.fields/fieldlink/insertaspicture/) { get; set; } | Получает или задает, следует ли вставлять связанный объект в виде изображения. |
| [InsertAsRtf](../../aspose.words.fields/fieldlink/insertasrtf/) { get; set; } | Получает или задает, следует ли вставлять связанный объект в формате RTF. |
| [InsertAsText](../../aspose.words.fields/fieldlink/insertastext/) { get; set; } | Получает или задает, следует ли вставлять связанный объект в текстовом формате. |
| [InsertAsUnicode](../../aspose.words.fields/fieldlink/insertasunicode/) { get; set; } | Получает или задает, следует ли вставлять связанный объект как текст Unicode. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Получает или устанавливает, является ли текущий результат поля более неверным (устаревшим) из-за других изменений, внесенных в документ. |
| [IsLinked](../../aspose.words.fields/fieldlink/islinked/) { get; set; } | Получает или задает, следует ли уменьшать размер файла, не сохраняя графические данные вместе с документом. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Получает или задает, заблокировано ли поле (не следует пересчитывать его результат). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Получает или задает LCID поля. |
| [ProgId](../../aspose.words.fields/fieldlink/progid/) { get; set; } | Получает или задает тип приложения информации о ссылке. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Получает или задает текст, который находится между разделителем поля и концом поля. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Получает узел, представляющий разделитель полей. Может быть нулевым. |
| [SourceFullName](../../aspose.words.fields/fieldlink/sourcefullname/) { get; set; } | Получает или задает имя и расположение исходного файла. |
| [SourceItem](../../aspose.words.fields/fieldlink/sourceitem/) { get; set; } | Получает или задает связываемую часть исходного файла. |
| [Start](../../aspose.words.fields/field/start/) { get; } | Получает узел, представляющий начало поля. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Получает тип поля Microsoft Word. |

## Методы

| Имя | Описание |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Возвращает текст между началом поля и разделителем поля (или концом поля, если разделителя нет). Включены как код поля, так и результат поля дочерних полей. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(bool) | Возвращает текст между началом поля и разделителем полей (или концом поля, если разделителя нет). |
| [Remove](../../aspose.words.fields/field/remove/)() | Удаляет поле из документа. Возвращает узел сразу после поля. Если конец поля является последним child его родительского узла, возвращает его родительский абзац. Если поле уже удалено, возвращает **нулевой** . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Выполняет развязку поля. |
| [Update](../../aspose.words.fields/field/update/)() | Выполняет обновление поля. Выдает, если поле уже обновляется. |
| [Update](../../aspose.words.fields/field/update/)(bool) | Выполняет обновление поля. Выдает, если поле уже обновляется. |

### Примечания

Для информации, скопированной из другого приложения, это поле связывает эту информацию с исходным файлом исходного .

### Примеры

Показывает, как использовать различные типы полей для связи с другими документами в локальной файловой системе и отображения их содержимого.

```csharp
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Ниже приведены три типа полей, которые мы можем использовать для отображения содержимого связанного документа в виде текста.
    // 1 - Поле ССЫЛКА:
    builder.Writeln("FieldLink:\n");
    InsertFieldLink(builder, insertLinkedObjectAs, "Word.Document.8", MyDir + "Document.docx", null, true);

    // 2 - Поле DDE:
    builder.Writeln("FieldDde:\n");
    InsertFieldDde(builder, insertLinkedObjectAs, "Excel.Sheet", MyDir + "Spreadsheet.xlsx",
        "Sheet1!R1C1", true, true);

    // 3 - Поле DDEAUTO:
    builder.Writeln("FieldDdeAuto:\n");
    InsertFieldDdeAuto(builder, insertLinkedObjectAs, "Excel.Sheet", MyDir + "Spreadsheet.xlsx",
        "Sheet1!R1C1", true);

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.LINK.DDE.DDEAUTO.docx");
}

{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Ниже приведены три типа полей, которые мы можем использовать для отображения содержимого связанного документа в виде изображения.
    // 1 - Поле ССЫЛКА:
    builder.Writeln("FieldLink:\n");
    InsertFieldLink(builder, insertLinkedObjectAs, "Excel.Sheet", MyDir + "MySpreadsheet.xlsx",
        "Sheet1!R2C2", true);

    // 2 - Поле DDE:
    builder.Writeln("FieldDde:\n");
    InsertFieldDde(builder, insertLinkedObjectAs, "Excel.Sheet", MyDir + "Spreadsheet.xlsx",
        "Sheet1!R1C1", true, true);

    // 3 - Поле DDEAUTO:
    builder.Writeln("FieldDdeAuto:\n");
    InsertFieldDdeAuto(builder, insertLinkedObjectAs, "Excel.Sheet", MyDir + "Spreadsheet.xlsx",
        "Sheet1!R1C1", true);

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.LINK.DDE.DDEAUTO.AsImage.docx");
}

/// <summary>
/// Используйте конструктор документов, чтобы вставить поле ССЫЛКА и установить его свойства в соответствии с параметрами.
/// </summary>
private static void InsertFieldLink(DocumentBuilder builder, InsertLinkedObjectAs insertLinkedObjectAs,
    string progId, string sourceFullName, string sourceItem, bool shouldAutoUpdate)
{
    FieldLink field = (FieldLink)builder.InsertField(FieldType.FieldLink, true);

    switch (insertLinkedObjectAs)
    {
        case InsertLinkedObjectAs.Text:
            field.InsertAsText = true;
            break;
        case InsertLinkedObjectAs.Unicode:
            field.InsertAsUnicode = true;
            break;
        case InsertLinkedObjectAs.Html:
            field.InsertAsHtml = true;
            break;
        case InsertLinkedObjectAs.Rtf:
            field.InsertAsRtf = true;
            break;
        case InsertLinkedObjectAs.Picture:
            field.InsertAsPicture = true;
            break;
        case InsertLinkedObjectAs.Bitmap:
            field.InsertAsBitmap = true;
            break;
    }

    field.AutoUpdate = shouldAutoUpdate;
    field.ProgId = progId;
    field.SourceFullName = sourceFullName;
    field.SourceItem = sourceItem;

    builder.Writeln("\n");
}

/// <summary>
/// Используйте конструктор документов, чтобы вставить поле DDE и установить его свойства в соответствии с параметрами.
/// </summary>
private static void InsertFieldDde(DocumentBuilder builder, InsertLinkedObjectAs insertLinkedObjectAs, string progId,
    string sourceFullName, string sourceItem, bool isLinked, bool shouldAutoUpdate)
{
    FieldDde field = (FieldDde)builder.InsertField(FieldType.FieldDDE, true);

    switch (insertLinkedObjectAs)
    {
        case InsertLinkedObjectAs.Text:
            field.InsertAsText = true;
            break;
        case InsertLinkedObjectAs.Unicode:
            field.InsertAsUnicode = true;
            break;
        case InsertLinkedObjectAs.Html:
            field.InsertAsHtml = true;
            break;
        case InsertLinkedObjectAs.Rtf:
            field.InsertAsRtf = true;
            break;
        case InsertLinkedObjectAs.Picture:
            field.InsertAsPicture = true;
            break;
        case InsertLinkedObjectAs.Bitmap:
            field.InsertAsBitmap = true;
            break;
    }

    field.AutoUpdate = shouldAutoUpdate;
    field.ProgId = progId;
    field.SourceFullName = sourceFullName;
    field.SourceItem = sourceItem;
    field.IsLinked = isLinked;

    builder.Writeln("\n");
}

/// <summary>
/// Используйте конструктор документов, чтобы вставить поле DDEAUTO, и установить его свойства в соответствии с параметрами.
/// </summary>
private static void InsertFieldDdeAuto(DocumentBuilder builder, InsertLinkedObjectAs insertLinkedObjectAs,
    string progId, string sourceFullName, string sourceItem, bool isLinked)
{
    FieldDdeAuto field = (FieldDdeAuto)builder.InsertField(FieldType.FieldDDEAuto, true);

    switch (insertLinkedObjectAs)
    {
        case InsertLinkedObjectAs.Text:
            field.InsertAsText = true;
            break;
        case InsertLinkedObjectAs.Unicode:
            field.InsertAsUnicode = true;
            break;
        case InsertLinkedObjectAs.Html:
            field.InsertAsHtml = true;
            break;
        case InsertLinkedObjectAs.Rtf:
            field.InsertAsRtf = true;
            break;
        case InsertLinkedObjectAs.Picture:
            field.InsertAsPicture = true;
            break;
        case InsertLinkedObjectAs.Bitmap:
            field.InsertAsBitmap = true;
            break;
    }

    field.ProgId = progId;
    field.SourceFullName = sourceFullName;
    field.SourceItem = sourceItem;
    field.IsLinked = isLinked;
}

public enum InsertLinkedObjectAs
{
    // СвязанныйОбъектКакТекст
    Text,
    Unicode,
    Html,
    Rtf,
    // СвязанныйОбъектКакИзображение
    Picture,
    Bitmap
}
```

### Смотрите также

* class [Field](../field/)
* пространство имен [Aspose.Words.Fields](../../aspose.words.fields/)
* сборка [Aspose.Words](../../)


