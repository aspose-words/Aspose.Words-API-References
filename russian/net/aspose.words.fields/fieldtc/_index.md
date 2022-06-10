---
title: FieldTC
second_title: Справочник по API Aspose.Words для .NET
description: Реализует поле TC.
type: docs
weight: 2290
url: /ru/net/aspose.words.fields/fieldtc/
---
## FieldTC class

Реализует поле TC.

```csharp
public sealed class FieldTC : Field
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [FieldTC](fieldtc)() | Конструктор по умолчанию. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult) { get; } | Получает текст, представляющий результат отображаемого поля. |
| [End](../../aspose.words.fields/field/end) { get; } | Получает узел, представляющий конец поля. |
| [EntryLevel](../../aspose.words.fields/fieldtc/entrylevel) { get; set; } | Получает или устанавливает уровень записи. |
| [Format](../../aspose.words.fields/field/format) { get; } | Получает объект[`FieldFormat`](../fieldformat), предоставляющий типизированный доступ к форматированию поля. |
| [IsDirty](../../aspose.words.fields/field/isdirty) { get; set; } | Получает или устанавливает, является ли текущий результат поля более неправильным (устаревшим) из-за других изменений, внесенных в документ. |
| [IsLocked](../../aspose.words.fields/field/islocked) { get; set; } | Получает или устанавливает, заблокировано ли поле (не должно пересчитывать его результат). |
| [LocaleId](../../aspose.words.fields/field/localeid) { get; set; } | Получает или задает LCID поля. |
| [OmitPageNumber](../../aspose.words.fields/fieldtc/omitpagenumber) { get; set; } | Получает или задает, следует ли опускать номер страницы в оглавлении для этого поля. |
| [Result](../../aspose.words.fields/field/result) { get; set; } | Получает или задает текст, который находится между разделителем полей и концом поля. |
| [Separator](../../aspose.words.fields/field/separator) { get; } | Получает узел, представляющий разделитель полей. Может быть нулевым. |
| [Start](../../aspose.words.fields/field/start) { get; } | Получает узел, представляющий начало поля. |
| [Text](../../aspose.words.fields/fieldtc/text) { get; set; } | Получает или задает текст записи. |
| virtual [Type](../../aspose.words.fields/field/type) { get; } | Получает тип поля Microsoft Word. |
| [TypeIdentifier](../../aspose.words.fields/fieldtc/typeidentifier) { get; set; } | Получает или задает идентификатор типа для этого поля (обычно это буква). |

## Методы

| Имя | Описание |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode)() | Возвращает текст между началом поля и разделителем полей (или концом поля, если разделителя нет). Включены как код поля, так и результат дочерних полей. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode)(bool) | Возвращает текст между началом поля и разделителем полей (или концом поля, если разделителя нет). |
| [Remove](../../aspose.words.fields/field/remove)() | Удаляет поле из документа. Возвращает узел сразу после поля. Если конец поля является последним дочерним элементом его родительского узла, возвращает его родительский абзац. Если поле уже удалено, возвращает **null** . |
| [Unlink](../../aspose.words.fields/field/unlink)() | Выполняет развязку поля. |
| [Update](../../aspose.words.fields/field/update)() | Выполняет обновление поля. Выдает, если поле уже обновляется. |
| [Update](../../aspose.words.fields/field/update)(bool) | Выполняет обновление поля. Выдает, если поле уже обновляется. |

### Примечания

Определяет текст и номер страницы для записи оглавления (включая таблицу рисунков), который используется полем TOC.

### Примеры

Показывает, как вставить поле TOC и отфильтровать, какие поля TC становятся записями.

```csharp
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Вставьте поле TOC, которое скомпилирует все поля TC в оглавление.
    FieldToc fieldToc = (FieldToc)builder.InsertField(FieldType.FieldTOC, true);

    // Настройте поле только для получения записей TC типа "A" и начального уровня от 1 до 3.
    fieldToc.EntryIdentifier = "A";
    fieldToc.EntryLevelRange = "1-3";

    Assert.AreEqual(" TOC  \\f A \\l 1-3", fieldToc.GetFieldCode());

    // Эти две записи появятся в таблице.
    builder.InsertBreak(BreakType.PageBreak);
    InsertTocEntry(builder, "TC field 1", "A", "1");
    InsertTocEntry(builder, "TC field 2", "A", "2");

    Assert.AreEqual(" TC  \"TC field 1\" \\n \\f A \\l 1", doc.Range.Fields[1].GetFieldCode());

    // Эта запись будет исключена из таблицы, потому что она имеет тип, отличный от "A".
    InsertTocEntry(builder, "TC field 3", "B", "1");

    // Эта запись будет исключена из таблицы, поскольку ее начальный уровень выходит за пределы диапазона 1-3.
    InsertTocEntry(builder, "TC field 4", "A", "5");

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.TC.docx");

/// <summary>
/// Используйте конструктор документов, чтобы вставить поле TC.
/// </summary>
public void InsertTocEntry(DocumentBuilder builder, string text, string typeIdentifier, string entryLevel)
{
    FieldTC fieldTc = (FieldTC)builder.InsertField(FieldType.FieldTOCEntry, true);
    fieldTc.OmitPageNumber = true;
    fieldTc.Text = text;
    fieldTc.TypeIdentifier = typeIdentifier;
    fieldTc.EntryLevel = entryLevel;
}
```

### Смотрите также

* class [Field](../field)
* пространство имен [Aspose.Words.Fields](../../aspose.words.fields)
* сборка [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
