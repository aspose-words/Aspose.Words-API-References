---
title: ImportFormatOptions Class
linktitle: ImportFormatOptions
articleTitle: ImportFormatOptions
second_title: Aspose.Words для .NET
description: Откройте для себя Aspose.Words.ImportFormatOptions для настраиваемого форматирования документов. Улучшите свой вывод с помощью индивидуальных настроек импорта для оптимальных результатов.
type: docs
weight: 3690
url: /ru/net/aspose.words/importformatoptions/
---
## ImportFormatOptions class

Позволяет указать различные параметры импорта для форматирования вывода.

Чтобы узнать больше, посетите[Укажите параметры загрузки](https://docs.aspose.com/words/net/specify-load-options/) документальная статья.

```csharp
public class ImportFormatOptions
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [ImportFormatOptions](importformatoptions/)() | Конструктор по умолчанию. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [AdjustSentenceAndWordSpacing](../../aspose.words/importformatoptions/adjustsentenceandwordspacing/) { get; set; } | Возвращает или задает логическое значение, указывающее, следует ли автоматически корректировать интервалы между предложениями и словами. Значение по умолчанию:`ЛОЖЬ` . |
| [ForceCopyStyles](../../aspose.words/importformatoptions/forcecopystyles/) { get; set; } | Возвращает или задает логическое значение, указывающее, следует ли копировать конфликтующие стили вKeepSourceFormatting mode. Значение по умолчанию:`ЛОЖЬ` . |
| [IgnoreHeaderFooter](../../aspose.words/importformatoptions/ignoreheaderfooter/) { get; set; } | Возвращает или задает логическое значение, указывающее, что исходное форматирование содержимого верхних/нижних колонтитулов игнорируется , еслиKeepSourceFormatting используется режим . Значение по умолчанию:`истинный` . |
| [IgnoreTextBoxes](../../aspose.words/importformatoptions/ignoretextboxes/) { get; set; } | Возвращает или задает логическое значение, указывающее, что исходное форматирование содержимого текстовых полей игнорируется , еслиKeepSourceFormatting используется режим . Значение по умолчанию:`истинный` . |
| [KeepSourceNumbering](../../aspose.words/importformatoptions/keepsourcenumbering/) { get; set; } | Возвращает или задает логическое значение, указывающее, как будет импортироваться нумерация при ее конфликте в исходном и целевом документах. Значение по умолчанию:`ЛОЖЬ` . |
| [MergePastedLists](../../aspose.words/importformatoptions/mergepastedlists/) { get; set; } | Возвращает или задает логическое значение, указывающее, будут ли вставленные списки объединены с окружающими списками. Значение по умолчанию:`ЛОЖЬ` . |
| [SmartStyleBehavior](../../aspose.words/importformatoptions/smartstylebehavior/) { get; set; } | Возвращает или задает логическое значение, указывающее, как будут импортироваться стили , если у них одинаковые имена в исходном и целевом документах. Значение по умолчанию:`ЛОЖЬ` . |

## Примеры

Показывает, как устранить дублирование стилей при вставке документов.

```csharp
Document dstDoc = new Document();
DocumentBuilder builder = new DocumentBuilder(dstDoc);

Style myStyle = builder.Document.Styles.Add(StyleType.Paragraph, "MyStyle");
myStyle.Font.Size = 14;
myStyle.Font.Name = "Courier New";
myStyle.Font.Color = Color.Blue;

builder.ParagraphFormat.StyleName = myStyle.Name;
builder.Writeln("Hello world!");

// Клонируем документ и редактируем стиль клона «MyStyle», чтобы его цвет отличался от цвета оригинала.
// Если мы вставим клон в исходный документ, два стиля с одинаковыми именами вызовут конфликт.
Document srcDoc = dstDoc.Clone();
srcDoc.Styles["MyStyle"].Font.Color = Color.Red;

// Когда мы включаем SmartStyleBehavior и используем режим формата импорта KeepSourceFormatting,
// Aspose.Words разрешит конфликты стилей путем преобразования стилей исходного документа.
// с теми же именами, что и целевые стили в прямые атрибуты абзаца.
ImportFormatOptions options = new ImportFormatOptions();
options.SmartStyleBehavior = true;

builder.InsertDocument(srcDoc, ImportFormatMode.KeepSourceFormatting, options);

dstDoc.Save(ArtifactsDir + "DocumentBuilder.SmartStyleBehavior.docx");
```

### Смотрите также

* пространство имен [Aspose.Words](../../aspose.words/)
* сборка [Aspose.Words](../../)
