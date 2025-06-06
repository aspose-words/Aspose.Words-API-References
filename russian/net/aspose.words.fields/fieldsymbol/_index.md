---
title: FieldSymbol Class
linktitle: FieldSymbol
articleTitle: FieldSymbol
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.Fields.FieldSymbol для эффективной реализации поля SYMBOL, расширяющего возможности обработки документов.
type: docs
weight: 2870
url: /ru/net/aspose.words.fields/fieldsymbol/
---
## FieldSymbol class

Реализует поле SYMBOL.

Чтобы узнать больше, посетите[Работа с полями](https://docs.aspose.com/words/net/working-with-fields/) документальная статья.

```csharp
public class FieldSymbol : Field
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [FieldSymbol](fieldsymbol/)() | Конструктор по умолчанию. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [CharacterCode](../../aspose.words.fields/fieldsymbol/charactercode/) { get; set; } | Возвращает или задает значение кодовой точки символа в десятичном или шестнадцатеричном формате. |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Получает текст, представляющий отображаемый результат поля. |
| [DontAffectsLineSpacing](../../aspose.words.fields/fieldsymbol/dontaffectslinespacing/) { get; set; } | Возвращает или задает, влияет ли символ, извлеченный полем, на межстрочный интервал абзаца. |
| [End](../../aspose.words.fields/field/end/) { get; } | Получает узел, представляющий конец поля. |
| [FontName](../../aspose.words.fields/fieldsymbol/fontname/) { get; set; } | Возвращает или задает имя шрифта символа, извлеченного полем. |
| [FontSize](../../aspose.words.fields/fieldsymbol/fontsize/) { get; set; } | Возвращает или задает размер в пунктах шрифта символа, извлеченного полем. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Получает[`FieldFormat`](../fieldformat/)объект, который обеспечивает типизированный доступ к форматированию поля. |
| [IsAnsi](../../aspose.words.fields/fieldsymbol/isansi/) { get; set; } | Возвращает или задает, интерпретируется ли код символа как значение символа ANSI. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Возвращает или задает, является ли текущий результат поля более неверным (устаревшим) из-за других изменений, внесенных в документ. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Возвращает или задает, заблокировано ли поле (не следует пересчитывать его результат). |
| [IsShiftJis](../../aspose.words.fields/fieldsymbol/isshiftjis/) { get; set; } | Возвращает или задает, интерпретируется ли код символа как значение символа SHIFT-JIS. |
| [IsUnicode](../../aspose.words.fields/fieldsymbol/isunicode/) { get; set; } | Возвращает или задает, интерпретируется ли код символа как значение символа Unicode. |
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

Извлекает символ, значение кодовой точки которого указано в десятичном или шестнадцатеричном формате.

## Примеры

Показывает, как использовать поле СИМВОЛ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Ниже приведены три способа использования поля SYMBOL для отображения одного символа.
// 1 - Добавить поле СИМВОЛ, которое отображает символ © (авторское право), заданный кодом символа ANSI:
FieldSymbol field = (FieldSymbol)builder.InsertField(FieldType.FieldSymbol, true);

// Код символа ANSI «U+00A9» или «169» в целочисленной форме зарезервирован для символа авторского права.
field.CharacterCode = 0x00a9.ToString();
field.IsAnsi = true;

Assert.AreEqual(" SYMBOL  169 \\a", field.GetFieldCode());

builder.Writeln(" Line 1");

// 2 - Добавьте поле СИМВОЛ, отображающее символ ∞ (бесконечность), и измените его внешний вид:
field = (FieldSymbol)builder.InsertField(FieldType.FieldSymbol, true);

// В Unicode символ бесконечности занимает код «221E».
field.CharacterCode = 0x221E.ToString();
field.IsUnicode = true;

// Изменим шрифт нашего символа после использования таблицы символов Windows
// чтобы убедиться, что шрифт может представить этот символ.
field.FontName = "Calibri";
field.FontSize = "24";

// Мы можем установить этот флаг для высоких символов, чтобы они не давили на остальной текст в своей строке.
field.DontAffectsLineSpacing = true;

Assert.AreEqual(" SYMBOL  8734 \\u \\f Calibri \\s 24 \\h", field.GetFieldCode());

builder.Writeln("Line 2");

// 3 - Добавить поле СИМВОЛ, которое отображает символ あ,
// со шрифтом, поддерживающим кодовую страницу Shift-JIS (Windows-932):
field = (FieldSymbol)builder.InsertField(FieldType.FieldSymbol, true);
field.FontName = "MS Gothic";
field.CharacterCode = 0x82A0.ToString();
field.IsShiftJis = true;

Assert.AreEqual(" SYMBOL  33440 \\f \"MS Gothic\" \\j", field.GetFieldCode());

builder.Write("Line 3");

doc.Save(ArtifactsDir + "Field.SYMBOL.docx");
```

### Смотрите также

* class [Field](../field/)
* пространство имен [Aspose.Words.Fields](../../aspose.words.fields/)
* сборка [Aspose.Words](../../)
