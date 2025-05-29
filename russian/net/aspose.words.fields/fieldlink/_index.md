---
title: FieldLink Class
linktitle: FieldLink
articleTitle: FieldLink
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.Fields.FieldLink для бесшовной реализации поля LINK. Улучшите обработку документов с помощью мощных функций уже сегодня!
type: docs
weight: 2520
url: /ru/net/aspose.words.fields/fieldlink/
---
## FieldLink class

Реализует поле LINK.

Чтобы узнать больше, посетите[Работа с полями](https://docs.aspose.com/words/net/working-with-fields/) документальная статья.

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
| [AutoUpdate](../../aspose.words.fields/fieldlink/autoupdate/) { get; set; } | Возвращает или задает, следует ли обновлять это поле автоматически. |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Получает текст, представляющий отображаемый результат поля. |
| [End](../../aspose.words.fields/field/end/) { get; } | Получает узел, представляющий конец поля. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Получает[`FieldFormat`](../fieldformat/)объект, который обеспечивает типизированный доступ к форматированию поля. |
| [FormatUpdateType](../../aspose.words.fields/fieldlink/formatupdatetype/) { get; set; } | Возвращает или задает способ обновления форматирования связанного объекта. |
| [InsertAsBitmap](../../aspose.words.fields/fieldlink/insertasbitmap/) { get; set; } | Возвращает или задает, следует ли вставлять связанный объект как растровое изображение. |
| [InsertAsHtml](../../aspose.words.fields/fieldlink/insertashtml/) { get; set; } | Возвращает или задает, следует ли вставлять связанный объект как текст в формате HTML. |
| [InsertAsPicture](../../aspose.words.fields/fieldlink/insertaspicture/) { get; set; } | Возвращает или задает, следует ли вставлять связанный объект как изображение. |
| [InsertAsRtf](../../aspose.words.fields/fieldlink/insertasrtf/) { get; set; } | Возвращает или задает, следует ли вставлять связанный объект в формате RTF. |
| [InsertAsText](../../aspose.words.fields/fieldlink/insertastext/) { get; set; } | Возвращает или задает, следует ли вставлять связанный объект в текстовом формате. |
| [InsertAsUnicode](../../aspose.words.fields/fieldlink/insertasunicode/) { get; set; } | Возвращает или задает, следует ли вставлять связанный объект как текст Unicode. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Возвращает или задает, является ли текущий результат поля более неверным (устаревшим) из-за других изменений, внесенных в документ. |
| [IsLinked](../../aspose.words.fields/fieldlink/islinked/) { get; set; } | Возвращает или задает, следует ли уменьшить размер файла, не сохраняя графические данные вместе с документом. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Возвращает или задает, заблокировано ли поле (не следует пересчитывать его результат). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Получает или задает LCID поля. |
| [ProgId](../../aspose.words.fields/fieldlink/progid/) { get; set; } | Возвращает или задает тип приложения для информации о ссылке. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Возвращает или задает текст, который находится между разделителем полей и концом поля. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Получает узел, представляющий разделитель полей. Может быть`нулевой` . |
| [SourceFullName](../../aspose.words.fields/fieldlink/sourcefullname/) { get; set; } | Возвращает или задает имя и местоположение исходного файла. |
| [SourceItem](../../aspose.words.fields/fieldlink/sourceitem/) { get; set; } | Возвращает или задает часть исходного файла, которая связана. |
| [Start](../../aspose.words.fields/field/start/) { get; } | Получает узел, представляющий начало поля. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Получает тип поля Microsoft Word. |

## Методы

| Имя | Описание |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Возвращает текст между началом поля и разделителем полей (или концом поля, если разделитель отсутствует). Включаются как код поля, так и результат поля дочерних полей. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(*bool*) | Возвращает текст между началом поля и разделителем полей (или концом поля, если разделитель отсутствует). |
| [Remove](../../aspose.words.fields/field/remove/)() | Удаляет поле из документа. Возвращает узел сразу после поля. Если конец поля — последний child его родительского узла, возвращает его родительский абзац. Если поле уже удалено, возвращает`нулевой` . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Выполняет отмену связи поля. |
| [Update](../../aspose.words.fields/field/update/)() | Выполняет обновление поля. Выдает исключение, если поле уже обновляется. |
| [Update](../../aspose.words.fields/field/update/)(*bool*) | Выполняет обновление поля. Выдает исключение, если поле уже обновляется. |

## Примечания

Для информации, скопированной из другого приложения, это поле связывает эту информацию с исходным файлом .

## Примеры

Показывает, как использовать различные типы полей для ссылки на другие документы в локальной файловой системе и отображения их содержимого.

```csharp
public void FieldLinkedObjectsAsText(InsertLinkedObjectAs insertLinkedObjectAs)
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Ниже приведены три типа полей, которые мы можем использовать для отображения содержимого связанного документа в виде текста.
    // 1 - Поле ССЫЛКИ:
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

public void FieldLinkedObjectsAsImage(InsertLinkedObjectAs insertLinkedObjectAs)
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Ниже приведены три типа полей, которые мы можем использовать для отображения содержимого связанного документа в виде изображения.
    // 1 - Поле ССЫЛКИ:
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
/// Используйте конструктор документов, чтобы вставить поле LINK и задать его свойства в соответствии с параметрами.
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
/// Используйте конструктор документов для вставки поля DDE и установки его свойств в соответствии с параметрами.
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
/// Используйте конструктор документов для вставки поля DDEAUTO и установки его свойств в соответствии с параметрами.
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
