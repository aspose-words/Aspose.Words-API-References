---
title: Class ImportFormatOptions
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.ImportFormatOptions сорт. Позволяет указать различные параметры импорта для форматирования вывода.
type: docs
weight: 3240
url: /ru/net/aspose.words/importformatoptions/
---
## ImportFormatOptions class

Позволяет указать различные параметры импорта для форматирования вывода.

Чтобы узнать больше, посетите[Укажите параметры загрузки](https://docs.aspose.com/words/net/specify-load-options/) статья документации.

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
| [AdjustSentenceAndWordSpacing](../../aspose.words/importformatoptions/adjustsentenceandwordspacing/) { get; set; } | Получает или задает логическое значение, указывающее, следует ли автоматически регулировать интервал между предложениями и словами. Значение по умолчанию:`ЛОЖЬ` . |
| [ForceCopyStyles](../../aspose.words/importformatoptions/forcecopystyles/) { get; set; } | Получает или задает логическое значение, указывающее, следует ли копировать конфликтующие стили вKeepSourceFormatting mode. Значение по умолчанию:`ЛОЖЬ` . |
| [IgnoreHeaderFooter](../../aspose.words/importformatoptions/ignoreheaderfooter/) { get; set; } | Получает или задает логическое значение, указывающее, что исходное форматирование содержимого верхних и нижних колонтитулов игнорируется , еслиKeepSourceFormatting используется режим. Значение по умолчанию:`истинный` . |
| [IgnoreTextBoxes](../../aspose.words/importformatoptions/ignoretextboxes/) { get; set; } | Получает или задает логическое значение, указывающее, что исходное форматирование содержимого текстовых полей игнорируется , еслиKeepSourceFormatting используется режим. Значение по умолчанию:`истинный` . |
| [KeepSourceNumbering](../../aspose.words/importformatoptions/keepsourcenumbering/) { get; set; } | Получает или задает логическое значение, определяющее, как будет импортироваться нумерация, если она конфликтует в исходном и целевом документах. Значение по умолчанию:`ЛОЖЬ` . |
| [MergePastedLists](../../aspose.words/importformatoptions/mergepastedlists/) { get; set; } | Получает или задает логическое значение, определяющее, будут ли вставленные списки объединяться с окружающими списками. Значение по умолчанию:`ЛОЖЬ` . |
| [SmartStyleBehavior](../../aspose.words/importformatoptions/smartstylebehavior/) { get; set; } | Получает или задает логическое значение, определяющее, как будут импортироваться стили , если они имеют одинаковые имена в исходном и целевом документах. Значение по умолчанию:`ЛОЖЬ` . |

### Примеры

Показывает, как устранить повторяющиеся стили при вставке документов.

```csharp
Document dstDoc = new Document();
DocumentBuilder builder = new DocumentBuilder(dstDoc);

Style myStyle = builder.Document.Styles.Add(StyleType.Paragraph, "MyStyle");
myStyle.Font.Size = 14;
myStyle.Font.Name = "Courier New";
myStyle.Font.Color = Color.Blue;

builder.ParagraphFormat.StyleName = myStyle.Name;
builder.Writeln("Hello world!");

// Клонируем документ и редактируем стиль «MyStyle» клона, чтобы его цвет отличался от цвета оригинала.
// Если мы вставим клон в исходный документ, два стиля с одинаковым именем вызовут конфликт.
Document srcDoc = dstDoc.Clone();
srcDoc.Styles["MyStyle"].Font.Color = Color.Red;

// Когда мы включаем SmartStyleBehavior и используем режим формата импорта KeepSourceFormatting,
// Aspose.Words разрешит конфликты стилей путем преобразования стилей исходного документа.
// с теми же именами, что и стили назначения, в прямые атрибуты абзаца.
ImportFormatOptions options = new ImportFormatOptions();
options.SmartStyleBehavior = true;

builder.InsertDocument(srcDoc, ImportFormatMode.KeepSourceFormatting, options);

dstDoc.Save(ArtifactsDir + "DocumentBuilder.SmartStyleBehavior.docx");
```

### Смотрите также

* пространство имен [Aspose.Words](../../aspose.words/)
* сборка [Aspose.Words](../../)


