---
title: FieldBarcode Class
linktitle: FieldBarcode
articleTitle: FieldBarcode
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.Fields.FieldBarcode для легкой генерации штрихкодов в документах. Улучшите свой рабочий процесс с помощью бесшовной интеграции и мощных функций.
type: docs
weight: 2040
url: /ru/net/aspose.words.fields/fieldbarcode/
---
## FieldBarcode class

Реализует поле BARCODE.

Чтобы узнать больше, посетите[Работа с полями](https://docs.aspose.com/words/net/working-with-fields/) документальная статья.

```csharp
public class FieldBarcode : Field
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [FieldBarcode](fieldbarcode/)() | Конструктор по умолчанию. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Получает текст, представляющий отображаемый результат поля. |
| [End](../../aspose.words.fields/field/end/) { get; } | Получает узел, представляющий конец поля. |
| [FacingIdentificationMark](../../aspose.words.fields/fieldbarcode/facingidentificationmark/) { get; set; } | Возвращает или задает тип лицевой идентификационной метки (FIM) для вставки. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Получает[`FieldFormat`](../fieldformat/)объект, который обеспечивает типизированный доступ к форматированию поля. |
| [IsBookmark](../../aspose.words.fields/fieldbarcode/isbookmark/) { get; set; } | Возвращает или задает,[`PostalAddress`](./postaladdress/) это имя закладки. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Возвращает или задает, является ли текущий результат поля более неверным (устаревшим) из-за других изменений, внесенных в документ. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Возвращает или задает, заблокировано ли поле (не следует пересчитывать его результат). |
| [IsUSPostalAddress](../../aspose.words.fields/fieldbarcode/isuspostaladdress/) { get; set; } | Возвращает или задает,[`PostalAddress`](./postaladdress/) почтовый адрес в США. |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Получает или задает LCID поля. |
| [PostalAddress](../../aspose.words.fields/fieldbarcode/postaladdress/) { get; set; } | Возвращает или задает почтовый адрес, используемый для генерации штрих-кода, или имя закладки, которая ссылается на него. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Возвращает или задает текст, который находится между разделителем полей и концом поля. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Получает узел, представляющий разделитель полей. Может быть`нулевой` . |
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

Вставляет почтовый штрих-код в машиночитаемую форму адреса, используемую Почтовой службой США.

## Примеры

Показывает, как использовать поле ШТРИХ-КОД для отображения почтовых индексов США в виде штрих-кода.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln();

// Ниже приведены два способа использования полей BARCODE для отображения пользовательских значений в виде штрихкодов.
// 1 — Сохраните значение, которое будет отображаться в штрих-коде, в свойстве PostalAddress:
FieldBarcode field = (FieldBarcode)builder.InsertField(FieldType.FieldBarcode, true);

// Это значение должно быть действительным почтовым индексом.
field.PostalAddress = "96801";
field.IsUSPostalAddress = true;
field.FacingIdentificationMark = "C";

Assert.AreEqual(" BARCODE  96801 \\u \\f C", field.GetFieldCode());

builder.InsertBreak(BreakType.LineBreak);

// 2 — Ссылка на закладку, в которой хранится значение, которое будет отображать этот штрих-код:
field = (FieldBarcode)builder.InsertField(FieldType.FieldBarcode, true);
field.PostalAddress = "BarcodeBookmark";
field.IsBookmark = true;

Assert.AreEqual(" BARCODE  BarcodeBookmark \\b", field.GetFieldCode());

// Закладка, на которую ссылается поле BARCODE в своем свойстве PostalAddress
// не должны содержать ничего, кроме действительного почтового индекса.
builder.InsertBreak(BreakType.PageBreak);
builder.StartBookmark("BarcodeBookmark");
builder.Writeln("968877");
builder.EndBookmark("BarcodeBookmark");

doc.Save(ArtifactsDir + "Field.BARCODE.docx");
```

### Смотрите также

* class [Field](../field/)
* пространство имен [Aspose.Words.Fields](../../aspose.words.fields/)
* сборка [Aspose.Words](../../)
