---
title: FieldSymbol.IsShiftJis
linktitle: IsShiftJis
articleTitle: IsShiftJis
second_title: Aspose.Words для .NET
description: Откройте для себя свойство FieldSymbol IsShiftJis — легко управляйте кодами символов SHIFTJIS для улучшенной обработки данных и бесшовной интерпретации символов.
type: docs
weight: 70
url: /ru/net/aspose.words.fields/fieldsymbol/isshiftjis/
---
## FieldSymbol.IsShiftJis property

Возвращает или задает, интерпретируется ли код символа как значение символа SHIFT-JIS.

```csharp
public bool IsShiftJis { get; set; }
```

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

* class [FieldSymbol](../)
* пространство имен [Aspose.Words.Fields](../../../aspose.words.fields/)
* сборка [Aspose.Words](../../../)
