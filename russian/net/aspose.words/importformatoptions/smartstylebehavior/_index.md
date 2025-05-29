---
title: ImportFormatOptions.SmartStyleBehavior
linktitle: SmartStyleBehavior
articleTitle: SmartStyleBehavior
second_title: Aspose.Words для .NET
description: Узнайте, как свойство ImportFormatOptions SmartStyleBehavior оптимизирует импорт стилей с одинаковыми именами в документах. Настройте свой процесс импорта без усилий!
type: docs
weight: 80
url: /ru/net/aspose.words/importformatoptions/smartstylebehavior/
---
## ImportFormatOptions.SmartStyleBehavior property

Возвращает или задает логическое значение, указывающее, как будут импортироваться стили , если у них одинаковые имена в исходном и целевом документах. Значение по умолчанию:`ЛОЖЬ` .

```csharp
public bool SmartStyleBehavior { get; set; }
```

## Примечания

Когда эта опция есть**включено** , исходный стиль будет расширен до прямых атрибутов внутри целевого документа a , еслиKeepSourceFormatting используется режим импорта.

Когда эта опция есть**неполноценный**, исходный стиль будет расширен только если он пронумерован. Существующие атрибуты назначения не будут переопределены, включая списки.

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

* class [ImportFormatOptions](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
