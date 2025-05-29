---
title: FieldBibliography Class
linktitle: FieldBibliography
articleTitle: FieldBibliography
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.Fields.FieldBibliography, чтобы без усилий управлять полями библиографии в ваших документах. Улучшайте свои тексты с легкостью!
type: docs
weight: 2050
url: /ru/net/aspose.words.fields/fieldbibliography/
---
## FieldBibliography class

Реализует поле БИБЛИОГРАФИЯ.

Чтобы узнать больше, посетите[Работа с полями](https://docs.aspose.com/words/net/working-with-fields/) документальная статья.

```csharp
public class FieldBibliography : Field
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [FieldBibliography](fieldbibliography/)() | Конструктор по умолчанию. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Получает текст, представляющий отображаемый результат поля. |
| [End](../../aspose.words.fields/field/end/) { get; } | Получает узел, представляющий конец поля. |
| [FilterLanguageId](../../aspose.words.fields/fieldbibliography/filterlanguageid/) { get; set; } | Возвращает или задает идентификатор языка, который используется для фильтрации библиографических данных только для тех источников в документе, которые используют этот язык. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Получает[`FieldFormat`](../fieldformat/)объект, который обеспечивает типизированный доступ к форматированию поля. |
| [FormatLanguageId](../../aspose.words.fields/fieldbibliography/formatlanguageid/) { get; set; } | Возвращает или задает идентификатор языка, который используется для форматирования библиографических источников в документе. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Возвращает или задает, является ли текущий результат поля более неверным (устаревшим) из-за других изменений, внесенных в документ. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Возвращает или задает, заблокировано ли поле (не следует пересчитывать его результат). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Получает или задает LCID поля. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Возвращает или задает текст, который находится между разделителем полей и концом поля. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Получает узел, представляющий разделитель полей. Может быть`нулевой` . |
| [SourceTag](../../aspose.words.fields/fieldbibliography/sourcetag/) { get; set; } | Возвращает или задает значение, чтобы в библиографии отображались только источники с соответствующим значением элемента тега. |
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

Вставляет содержимое раздела «Библиография» документа в библиографическом стиле.

## Примеры

Показывает, как работать с полями ЦИТАТА и БИБЛИОГРАФИЯ.

```csharp
// Открываем документ, содержащий библиографические источники, которые мы можем найти в
// Microsoft Word через Ссылки -> Цитаты и библиография -> Управление источниками.
Document doc = new Document(MyDir + "Bibliography.docx");
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Text to be cited with one source.");

// Создайте ссылку, указав только номер страницы и автора указанной книги.
FieldCitation fieldCitation = (FieldCitation)builder.InsertField(FieldType.FieldCitation, true);

// Мы ссылаемся на источники, используя их имена тегов.
fieldCitation.SourceTag = "Book1";
fieldCitation.PageNumber = "85";
fieldCitation.SuppressAuthor = false;
fieldCitation.SuppressTitle = true;
fieldCitation.SuppressYear = true;

Assert.AreEqual(" CITATION  Book1 \\p 85 \\t \\y", fieldCitation.GetFieldCode());

// Создайте более подробную цитату, ссылающуюся на два источника.
builder.InsertParagraph();
builder.Write("Text to be cited with two sources.");
fieldCitation = (FieldCitation)builder.InsertField(FieldType.FieldCitation, true);
fieldCitation.SourceTag = "Book1";
fieldCitation.AnotherSourceTag = "Book2";
fieldCitation.FormatLanguageId = "en-US";
fieldCitation.PageNumber = "19";
fieldCitation.Prefix = "Prefix ";
fieldCitation.Suffix = " Suffix";
fieldCitation.SuppressAuthor = false;
fieldCitation.SuppressTitle = false;
fieldCitation.SuppressYear = false;
fieldCitation.VolumeNumber = "VII";

Assert.AreEqual(" CITATION  Book1 \\m Book2 \\l en-US \\p 19 \\f \"Prefix \" \\s \" Suffix\" \\v VII", fieldCitation.GetFieldCode());

// Мы можем использовать поле БИБЛИОГРАФИЯ для отображения всех источников в документе.
builder.InsertBreak(BreakType.PageBreak);
FieldBibliography fieldBibliography = (FieldBibliography)builder.InsertField(FieldType.FieldBibliography, true);
fieldBibliography.FormatLanguageId = "5129";
fieldBibliography.FilterLanguageId = "5129";
fieldBibliography.SourceTag = "Book2";

Assert.AreEqual(" BIBLIOGRAPHY  \\l 5129 \\f 5129 \\m Book2", fieldBibliography.GetFieldCode());

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.CITATION.docx");
```

### Смотрите также

* class [Field](../field/)
* пространство имен [Aspose.Words.Fields](../../aspose.words.fields/)
* сборка [Aspose.Words](../../)
