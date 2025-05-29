---
title: FieldDate Class
linktitle: FieldDate
articleTitle: FieldDate
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.Fields.FieldDate, разработанный для простой реализации полей DATE, улучшая автоматизацию и форматирование документов.
type: docs
weight: 2180
url: /ru/net/aspose.words.fields/fielddate/
---
## FieldDate class

Реализует поле ДАТА.

Чтобы узнать больше, посетите[Работа с полями](https://docs.aspose.com/words/net/working-with-fields/) документальная статья.

```csharp
public class FieldDate : Field
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [FieldDate](fielddate/)() | Конструктор по умолчанию. |

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
| [UseLastFormat](../../aspose.words.fields/fielddate/uselastformat/) { get; set; } | Возвращает или задает, следует ли использовать последний формат, использованный приложением хостинга при вставке нового поля ДАТА. |
| [UseLunarCalendar](../../aspose.words.fields/fielddate/uselunarcalendar/) { get; set; } | Возвращает или задает, использовать ли лунный календарь Хиджры или еврейский лунный календарь. |
| [UseSakaEraCalendar](../../aspose.words.fields/fielddate/usesakaeracalendar/) { get; set; } | Возвращает или задает, использовать ли календарь эпохи Сака. |
| [UseUmAlQuraCalendar](../../aspose.words.fields/fielddate/useumalquracalendar/) { get; set; } | Возвращает или задает, использовать ли календарь Ум-аль-Кура. |

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

Вставляет текущую дату и время. По умолчанию используется григорианский календарь.

## Примеры

Показывает, как использовать поля ДАТА для отображения дат в соответствии с различными видами календарей.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Если мы хотим, чтобы текст в документе всегда отображал правильную дату, мы можем использовать поле ДАТА.
// Ниже приведены три типа культурных календарей, которые поле ДАТА может использовать для отображения даты.
// 1 - Исламский лунный календарь:
FieldDate field = (FieldDate)builder.InsertField(FieldType.FieldDate, true);
field.UseLunarCalendar = true;
Assert.AreEqual(" DATE  \\h", field.GetFieldCode());
builder.Writeln();

// 2 - Календарь Умм аль-Кура:
field = (FieldDate)builder.InsertField(FieldType.FieldDate, true);
field.UseUmAlQuraCalendar = true;
Assert.AreEqual(" DATE  \\u", field.GetFieldCode());
builder.Writeln();

// 3 - Индийский национальный календарь:
field = (FieldDate)builder.InsertField(FieldType.FieldDate, true);
field.UseSakaEraCalendar = true;
Assert.AreEqual(" DATE  \\s", field.GetFieldCode());
builder.Writeln();

// Вставьте поле ДАТА и установите его тип календаря на последний, использовавшийся хост-приложением.
// В Microsoft Word тип будет последним использованным в диалоговом окне Вставка -> Текст -> Дата и время.
field = (FieldDate)builder.InsertField(FieldType.FieldDate, true);
field.UseLastFormat = true;
Assert.AreEqual(" DATE  \\l", field.GetFieldCode());
builder.Writeln();

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.DATE.docx");
```

### Смотрите также

* class [Field](../field/)
* пространство имен [Aspose.Words.Fields](../../aspose.words.fields/)
* сборка [Aspose.Words](../../)
