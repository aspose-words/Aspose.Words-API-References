---
title: Class FieldAddressBlock
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.Fields.FieldAddressBlock сорт. Реализует поле ADDRESSBLOCK.
type: docs
weight: 1530
url: /ru/net/aspose.words.fields/fieldaddressblock/
---
## FieldAddressBlock class

Реализует поле ADDRESSBLOCK.

Чтобы узнать больше, посетите[Работа с полями](https://docs.aspose.com/words/net/working-with-fields/) статья документации.

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
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Получает текст, представляющий результат отображаемого поля. |
| [End](../../aspose.words.fields/field/end/) { get; } | Получает узел, представляющий конец поля. |
| [ExcludedCountryOrRegionName](../../aspose.words.fields/fieldaddressblock/excludedcountryorregionname/) { get; set; } | Получает или задает имя исключенной страны или региона. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Получает[`FieldFormat`](../fieldformat/) объект, обеспечивающий типизированный доступ к форматированию поля. |
| [FormatAddressOnCountryOrRegion](../../aspose.words.fields/fieldaddressblock/formataddressoncountryorregion/) { get; set; } | Получает или задает необходимость форматирования адреса в соответствии со страной/регионом получателя , как определено POST*CODE (Universal Postal Union 2006). |
| [IncludeCountryOrRegionName](../../aspose.words.fields/fieldaddressblock/includecountryorregionname/) { get; set; } | Получает или задает, следует ли включать название страны/региона. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Получает или устанавливает, является ли текущий результат поля более неправильным (устаревшим) из-за других изменений, внесенных в документ. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Получает или задает, заблокировано ли поле (не следует пересчитывать результат). |
| [LanguageId](../../aspose.words.fields/fieldaddressblock/languageid/) { get; set; } | Получает или задает идентификатор языка, используемый для форматирования адреса. |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Получает или задает LCID поля. |
| [NameAndAddressFormat](../../aspose.words.fields/fieldaddressblock/nameandaddressformat/) { get; set; } | Получает или задает формат имени и адреса. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Получает или задает текст, расположенный между разделителем полей и концом поля. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Получает узел, представляющий разделитель полей. Возможно`нулевой` . |
| [Start](../../aspose.words.fields/field/start/) { get; } | Получает узел, представляющий начало поля. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Получает тип поля Microsoft Word. |

## Методы

| Имя | Описание |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Возвращает текст между началом поля и разделителем поля (или концом поля, если разделителя нет). Включены как код поля, так и результат поля дочерних полей. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(bool) | Возвращает текст между началом поля и разделителем полей (или концом поля, если разделителя нет). |
| [GetFieldNames](../../aspose.words.fields/fieldaddressblock/getfieldnames/)() | Возвращает коллекцию имен полей слияния почты, используемых этим полем. |
| [Remove](../../aspose.words.fields/field/remove/)() | Удаляет поле из документа. Возвращает узел сразу после поля. Если конец поля является последним дочерним его родительского узла, возвращает его родительский абзац. Если поле уже удалено, возвращается`нулевой` . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Выполняет отсоединение поля. |
| [Update](../../aspose.words.fields/field/update/)() | Выполняет обновление поля. Выдает, если поле уже обновляется. |
| [Update](../../aspose.words.fields/field/update/)(bool) | Выполняет обновление поля. Выдает, если поле уже обновляется. |

### Примечания

Представляет блок адреса. Анадресный блокпредставляет собой блок текста, определяющий information , соответствующий почтовому адресу, в порядке, требуемом страной назначения.

### Примеры

Показывает, как получить имена полей слияния почты, используемые полем.

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


