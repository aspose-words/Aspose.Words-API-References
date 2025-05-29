---
title: FieldFormText Class
linktitle: FieldFormText
articleTitle: FieldFormText
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.Fields.FieldFormText для бесшовной реализации поля FORMTEXT. Улучшите автоматизацию документов с помощью мощных функций уже сегодня!
type: docs
weight: 2340
url: /ru/net/aspose.words.fields/fieldformtext/
---
## FieldFormText class

Реализует поле FORMTEXT.

Чтобы узнать больше, посетите[Работа с полями](https://docs.aspose.com/words/net/working-with-fields/) документальная статья.

```csharp
public class FieldFormText : Field
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [FieldFormText](fieldformtext/)() | Конструктор по умолчанию. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Получает текст, представляющий отображаемый результат поля. |
| [End](../../aspose.words.fields/field/end/) { get; } | Получает узел, представляющий конец поля. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Получает[`FieldFormat`](../fieldformat/)объект, который обеспечивает типизированный доступ к форматированию поля. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Возвращает или задает, является ли текущий результат поля более неверным (устаревшим) из-за других изменений, внесенных в документ. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Возвращает или задает, заблокировано ли поле (не следует пересчитывать его результат). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Получает или задает LCID поля. |
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

Вставляет поле формы в стиле текстового поля.

## Примеры

Показывает, как обрабатывать поля FORMCHECKBOX, FORMDROPDOWN и FORMTEXT.

```csharp
// Эти поля являются устаревшими эквивалентами FormField. Мы можем читать, но не создавать эти поля с помощью Aspose.Words.
// В Microsoft Word мы можем вставить эти поля через меню «Инструменты прежних версий» на вкладке «Разработчик».
Document doc = new Document(MyDir + "Form fields.docx");

FieldFormCheckBox fieldFormCheckBox = (FieldFormCheckBox)doc.Range.Fields[1];
Assert.AreEqual(" FORMCHECKBOX \u0001", fieldFormCheckBox.GetFieldCode());

FieldFormDropDown fieldFormDropDown = (FieldFormDropDown)doc.Range.Fields[2];
Assert.AreEqual(" FORMDROPDOWN \u0001", fieldFormDropDown.GetFieldCode());

FieldFormText fieldFormText = (FieldFormText)doc.Range.Fields[0];
Assert.AreEqual(" FORMTEXT \u0001", fieldFormText.GetFieldCode());
```

### Смотрите также

* class [Field](../field/)
* пространство имен [Aspose.Words.Fields](../../aspose.words.fields/)
* сборка [Aspose.Words](../../)
