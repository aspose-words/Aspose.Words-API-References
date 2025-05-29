---
title: FieldAddressBlock Class
linktitle: FieldAddressBlock
articleTitle: FieldAddressBlock
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.Fields.FieldAddressBlock для бесшовной интеграции полей ADDRESSBLOCK в ваши документы. Улучшите автоматизацию документов сегодня!
type: docs
weight: 1940
url: /ru/net/aspose.words.fields/fieldaddressblock/
---
## FieldAddressBlock class

Реализует поле ADDRESSBLOCK.

Чтобы узнать больше, посетите[Работа с полями](https://docs.aspose.com/words/net/working-with-fields/) документальная статья.

```csharp
public class FieldAddressBlock : Field
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [FieldAddressBlock](fieldaddressblock/)() | Конструктор по умолчанию. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Получает текст, представляющий отображаемый результат поля. |
| [End](../../aspose.words.fields/field/end/) { get; } | Получает узел, представляющий конец поля. |
| [ExcludedCountryOrRegionName](../../aspose.words.fields/fieldaddressblock/excludedcountryorregionname/) { get; set; } | Получает или задает имя исключенной страны/региона. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Получает[`FieldFormat`](../fieldformat/)объект, который обеспечивает типизированный доступ к форматированию поля. |
| [FormatAddressOnCountryOrRegion](../../aspose.words.fields/fieldaddressblock/formataddressoncountryorregion/) { get; set; } | Возвращает или задает форматирование адреса в соответствии со страной/регионом получателя , как определено POST*CODE (Всемирный почтовый союз 2006). |
| [IncludeCountryOrRegionName](../../aspose.words.fields/fieldaddressblock/includecountryorregionname/) { get; set; } | Возвращает или задает, следует ли включать название страны/региона. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Возвращает или задает, является ли текущий результат поля более неверным (устаревшим) из-за других изменений, внесенных в документ. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Возвращает или задает, заблокировано ли поле (не следует пересчитывать его результат). |
| [LanguageId](../../aspose.words.fields/fieldaddressblock/languageid/) { get; set; } | Возвращает или задает идентификатор языка, используемый для форматирования адреса. |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Получает или задает LCID поля. |
| [NameAndAddressFormat](../../aspose.words.fields/fieldaddressblock/nameandaddressformat/) { get; set; } | Получает или задает формат имени и адреса. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Возвращает или задает текст, который находится между разделителем полей и концом поля. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Получает узел, представляющий разделитель полей. Может быть`нулевой` . |
| [Start](../../aspose.words.fields/field/start/) { get; } | Получает узел, представляющий начало поля. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Получает тип поля Microsoft Word. |

## Методы

| Имя | Описание |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Возвращает текст между началом поля и разделителем полей (или концом поля, если разделитель отсутствует). Включаются как код поля, так и результат поля дочерних полей. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(*bool*) | Возвращает текст между началом поля и разделителем полей (или концом поля, если разделитель отсутствует). |
| [GetFieldNames](../../aspose.words.fields/fieldaddressblock/getfieldnames/)() | Возвращает коллекцию имен полей слияния, используемых полем. |
| [Remove](../../aspose.words.fields/field/remove/)() | Удаляет поле из документа. Возвращает узел сразу после поля. Если конец поля — последний child его родительского узла, возвращает его родительский абзац. Если поле уже удалено, возвращает`нулевой` . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Выполняет отмену связи поля. |
| [Update](../../aspose.words.fields/field/update/)() | Выполняет обновление поля. Выдает исключение, если поле уже обновляется. |
| [Update](../../aspose.words.fields/field/update/)(*bool*) | Выполняет обновление поля. Выдает исключение, если поле уже обновляется. |

## Примечания

Представляет блок адреса.блок адреса представляет собой блок текста, указывающий информацию , соответствующую почтовому адресу, в порядке, требуемом страной назначения.

## Примеры

Показывает, как получить имена полей слияния, используемые полем.

```csharp
Document doc = new Document(MyDir + "Field sample - ADDRESSBLOCK.docx");

string[] addressFieldsExpect =
{
    "Company", "First Name", "Middle Name", "Last Name", "Suffix", "Address 1", "City", "State",
    "Country or Region", "Postal Code"
};

FieldAddressBlock addressBlockField = (FieldAddressBlock) doc.Range.Fields[0];
string[] addressBlockFieldNames = addressBlockField.GetFieldNames();
```

### Смотрите также

* class [Field](../field/)
* пространство имен [Aspose.Words.Fields](../../aspose.words.fields/)
* сборка [Aspose.Words](../../)
