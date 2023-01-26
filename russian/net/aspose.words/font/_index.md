---
title: Font
second_title: Справочник по API Aspose.Words для .NET
description: Содержит атрибуты шрифта имя шрифта размер шрифта цвет и т. д. для объекта.
type: docs
weight: 2650
url: /ru/net/aspose.words/font/
---
## Font class

Содержит атрибуты шрифта (имя шрифта, размер шрифта, цвет и т. д.) для объекта.

```csharp
public class Font
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [AllCaps](../../aspose.words/font/allcaps/) { get; set; } | Истинно, если шрифт отформатирован так, чтобы все буквы были заглавными. |
| [AutoColor](../../aspose.words/font/autocolor/) { get; } | Возвращает текущий рассчитанный цвет текста (черный или белый), который будет использоваться для «автоцвета». Если цвет не «авто», то возвращает[`Color`](./color/) . |
| [Bidi](../../aspose.words/font/bidi/) { get; set; } | Указывает, должно ли содержимое этого цикла иметь характеристики письма справа налево. |
| [Bold](../../aspose.words/font/bold/) { get; set; } | Истинно, если шрифт отформатирован как полужирный. |
| [BoldBi](../../aspose.words/font/boldbi/) { get; set; } | Истинно, если текст справа налево выделен полужирным шрифтом. |
| [Border](../../aspose.words/font/border/) { get; } | Возвращает объект Border, указывающий границу для шрифта. |
| [Color](../../aspose.words/font/color/) { get; set; } | Получает или задает цвет шрифта. |
| [ComplexScript](../../aspose.words/font/complexscript/) { get; set; } | Указывает, должно ли содержимое этого запуска рассматриваться как сложный текст сценария независимо от их значений символов Unicode при определении форматирования для этого запуска. |
| [DoubleStrikeThrough](../../aspose.words/font/doublestrikethrough/) { get; set; } | Истинно, если шрифт отформатирован как двойной зачеркнутый текст. |
| [Emboss](../../aspose.words/font/emboss/) { get; set; } | Истинно, если шрифт отформатирован как рельефный. |
| [EmphasisMark](../../aspose.words/font/emphasismark/) { get; set; } | Получает или задает знак выделения, применяемый к этому форматированию. |
| [Engrave](../../aspose.words/font/engrave/) { get; set; } | Истинно, если шрифт отформатирован как выгравированный. |
| [Fill](../../aspose.words/font/fill/) { get; } | Получает форматирование заливки для шрифта. |
| [Hidden](../../aspose.words/font/hidden/) { get; set; } | Истинно, если шрифт отформатирован как скрытый текст. |
| [HighlightColor](../../aspose.words/font/highlightcolor/) { get; set; } | Получает или задает цвет выделения (маркера). |
| [Italic](../../aspose.words/font/italic/) { get; set; } | Истинно, если шрифт отформатирован как курсив. |
| [ItalicBi](../../aspose.words/font/italicbi/) { get; set; } | Истинно, если текст с написанием справа налево отформатирован курсивом. |
| [Kerning](../../aspose.words/font/kerning/) { get; set; } | Получает или задает размер шрифта, с которого начинается кернинг. |
| [LineSpacing](../../aspose.words/font/linespacing/) { get; } | Возвращает межстрочный интервал этого шрифта (в пунктах). |
| [LocaleId](../../aspose.words/font/localeid/) { get; set; } | Получает или задает идентификатор локали (язык) отформатированных символов. |
| [LocaleIdBi](../../aspose.words/font/localeidbi/) { get; set; } | Получает или задает идентификатор локали (язык) отформатированных символов с письмом справа налево. |
| [LocaleIdFarEast](../../aspose.words/font/localeidfareast/) { get; set; } | Получает или задает идентификатор локали (язык) отформатированных азиатских символов. |
| [Name](../../aspose.words/font/name/) { get; set; } | Получает или задает имя шрифта. |
| [NameAscii](../../aspose.words/font/nameascii/) { get; set; } | Возвращает или задает шрифт, используемый для латинского текста (символы с кодами от 0 (ноль) до 127). |
| [NameBi](../../aspose.words/font/namebi/) { get; set; } | Возвращает или задает имя шрифта в документе на языке с письмом справа налево. |
| [NameFarEast](../../aspose.words/font/namefareast/) { get; set; } | Возвращает или задает имя восточноазиатского шрифта. |
| [NameOther](../../aspose.words/font/nameother/) { get; set; } | Возвращает или задает шрифт, используемый для символов с кодами символов от 128 до 255. |
| [NoProofing](../../aspose.words/font/noproofing/) { get; set; } | Истина, если отформатированные символы не должны проверяться на орфографию. |
| [Outline](../../aspose.words/font/outline/) { get; set; } | Истинно, если шрифт отформатирован как контурный. |
| [Position](../../aspose.words/font/position/) { get; set; } | Получает или задает положение текста (в пунктах) относительно базовой линии. Положительное число поднимает текст, а отрицательное число опускает его. |
| [Scaling](../../aspose.words/font/scaling/) { get; set; } | Получает или задает масштабирование ширины символов в процентах. |
| [Shading](../../aspose.words/font/shading/) { get; } | Возвращает объект Shading, который ссылается на форматирование заливки для шрифта. |
| [Shadow](../../aspose.words/font/shadow/) { get; set; } | Истинно, если шрифт отформатирован как затененный. |
| [Size](../../aspose.words/font/size/) { get; set; } | Получает или задает размер шрифта в пунктах. |
| [SizeBi](../../aspose.words/font/sizebi/) { get; set; } | Получает или задает размер шрифта в пунктах, используемый в документе с письмом справа налево. |
| [SmallCaps](../../aspose.words/font/smallcaps/) { get; set; } | Истинно, если шрифт отформатирован как маленькие заглавные буквы. |
| [SnapToGrid](../../aspose.words/font/snaptogrid/) { get; set; } | Указывает, должен ли текущий шрифт использовать символы сетки документа на строку settings при макетировании. |
| [Spacing](../../aspose.words/font/spacing/) { get; set; } | Возвращает или задает интервал (в пунктах) между символами . |
| [StrikeThrough](../../aspose.words/font/strikethrough/) { get; set; } | Истинно, если шрифт отформатирован как зачеркнутый текст. |
| [Style](../../aspose.words/font/style/) { get; set; } | Получает или задает стиль символов, применяемый к этому форматированию. |
| [StyleIdentifier](../../aspose.words/font/styleidentifier/) { get; set; } | Получает или задает независимый от языкового стандарта идентификатор стиля символа, примененного к данному форматированию. |
| [StyleName](../../aspose.words/font/stylename/) { get; set; } | Получает или задает имя стиля символов, примененного к этому форматированию. |
| [Subscript](../../aspose.words/font/subscript/) { get; set; } | Истинно, если шрифт отформатирован как нижний индекс. |
| [Superscript](../../aspose.words/font/superscript/) { get; set; } | Истинно, если шрифт отформатирован как надстрочный. |
| [TextEffect](../../aspose.words/font/texteffect/) { get; set; } | Получает или задает эффект анимации шрифта. |
| [ThemeColor](../../aspose.words/font/themecolor/) { get; set; } | Получает или задает цвет темы в применяемой цветовой схеме, связанной с этим объектом Font. |
| [ThemeFont](../../aspose.words/font/themefont/) { get; set; } | Получает или задает шрифт темы в применяемой схеме шрифтов, связанной с этим объектом Font. |
| [ThemeFontAscii](../../aspose.words/font/themefontascii/) { get; set; } | Получает или задает шрифт темы, используемый для латинского текста (символы с кодами символов от 0 (ноль) до 127) в применяемой схеме шрифтов, связанной с этим объектом Font. |
| [ThemeFontBi](../../aspose.words/font/themefontbi/) { get; set; } | Получает или задает шрифт темы в применяемой схеме шрифтов, связанной с этим объектом Font в документе с письмом справа налево. |
| [ThemeFontFarEast](../../aspose.words/font/themefontfareast/) { get; set; } | Получает или задает шрифт восточноазиатской темы в применяемой схеме шрифтов, связанной с этим объектом Font. |
| [ThemeFontOther](../../aspose.words/font/themefontother/) { get; set; } | Получает или задает шрифт темы, используемый для символов с кодами символов от 128 до 255 в применяемой схеме шрифтов, связанной с этим объектом Font. |
| [TintAndShade](../../aspose.words/font/tintandshade/) { get; set; } | Получает или задает двойное значение, которое делает цвет светлее или темнее. |
| [Underline](../../aspose.words/font/underline/) { get; set; } | Получает или задает тип подчеркивания шрифта. |
| [UnderlineColor](../../aspose.words/font/underlinecolor/) { get; set; } | Получает или задает цвет подчеркивания шрифта. |

## Методы

| Имя | Описание |
| --- | --- |
| [ClearFormatting](../../aspose.words/font/clearformatting/)() | Восстанавливает форматирование шрифта по умолчанию. |
| [HasDmlEffect](../../aspose.words/font/hasdmleffect/)(TextDmlEffect) | Проверяет, применяется ли конкретный текстовый эффект DrawingML. |

### Примечания

Вы не создаете экземпляры`Font` класс напрямую. Вы просто используете `Font` для доступа к свойствам шрифта различных объектов, таких как[`Run`](../run/) , [`Paragraph`](../paragraph/) ,[`Style`](../style/) ,[`DocumentBuilder`](../documentbuilder/).

### Примеры

Показывает, как отформатировать набор текста, используя его свойство шрифта.

```csharp
Document doc = new Document();
Run run = new Run(doc, "Hello world!");

Aspose.Words.Font font = run.Font;
font.Name = "Courier New";
font.Size = 36;
font.HighlightColor = Color.Yellow;

doc.FirstSection.Body.FirstParagraph.AppendChild(run);
doc.Save(ArtifactsDir + "Font.CreateFormattedRun.docx");
```

Показывает, как вставить в документ строку, окруженную рамкой.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Border.Color = Color.Green;
builder.Font.Border.LineWidth = 2.5d;
builder.Font.Border.LineStyle = LineStyle.DashDotStroker;

builder.Write("Text surrounded by green border.");

doc.Save(ArtifactsDir + "Border.FontBorder.docx");
```

Показывает, как создать и использовать стиль абзаца с форматированием списка.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Создать собственный стиль абзаца.
Style style = doc.Styles.Add(StyleType.Paragraph, "MyStyle1");
style.Font.Size = 24;
style.Font.Name = "Verdana";
style.ParagraphFormat.SpaceAfter = 12;

// Создайте список и убедитесь, что абзацы, использующие этот стиль, будут использовать этот список.
style.ListFormat.List = doc.Lists.Add(ListTemplate.BulletDefault);
style.ListFormat.ListLevelNumber = 0;

// Применяем стиль абзаца к текущему абзацу конструктора документов, а затем добавляем текст.
builder.ParagraphFormat.Style = style;
builder.Writeln("Hello World: MyStyle1, bulleted list.");

// Измените стиль построителя документа на стиль без форматирования списка и напишите еще один абзац.
builder.ParagraphFormat.Style = doc.Styles["Normal"];
builder.Writeln("Hello World: Normal.");

builder.Document.Save(ArtifactsDir + "Styles.ParagraphStyleBulletedList.docx");
```

### Смотрите также

* пространство имен [Aspose.Words](../../aspose.words/)
* сборка [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
