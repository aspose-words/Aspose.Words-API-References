---
title: Font Class
linktitle: Font
articleTitle: Font
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.Font, включающий основные атрибуты шрифта, такие как имя, размер и цвет, для улучшения форматирования и дизайна вашего документа.
type: docs
weight: 3240
url: /ru/net/aspose.words/font/
---
## Font class

Содержит атрибуты шрифта (имя шрифта, размер шрифта, цвет и т. д.) для объекта.

Чтобы узнать больше, посетите[Работа со шрифтами](https://docs.aspose.com/words/net/working-with-fonts/) документальная статья.

```csharp
public class Font
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [AllCaps](../../aspose.words/font/allcaps/) { get; set; } | True, если шрифт отформатирован как все заглавные буквы. |
| [AutoColor](../../aspose.words/font/autocolor/) { get; } | Возвращает текущий вычисленный цвет текста (черный или белый), который будет использоваться для «автоматического цвета». Если цвет не равен «автоматическому», то возвращается[`Color`](./color/) . |
| [Bidi](../../aspose.words/font/bidi/) { get; set; } | Указывает, будет ли содержимое этого прогона иметь характеристики справа налево. |
| [Bold](../../aspose.words/font/bold/) { get; set; } | True, если шрифт отформатирован как жирный. |
| [BoldBi](../../aspose.words/font/boldbi/) { get; set; } | True, если текст, написанный справа налево, отформатирован как полужирный. |
| [Border](../../aspose.words/font/border/) { get; } | Возвращает[`Border`](../border/) объект, задающий границу для шрифта. |
| [Color](../../aspose.words/font/color/) { get; set; } | Получает или задает цвет шрифта. |
| [ComplexScript](../../aspose.words/font/complexscript/) { get; set; } | Указывает, будет ли содержимое этого прогона рассматриваться как сложный текст сценария независимо от их значений символов Unicode при определении форматирования для этого прогона. |
| [DoubleStrikeThrough](../../aspose.words/font/doublestrikethrough/) { get; set; } | True, если шрифт отформатирован как двойной зачеркнутый текст. |
| [Emboss](../../aspose.words/font/emboss/) { get; set; } | True, если шрифт отформатирован как рельефный. |
| [EmphasisMark](../../aspose.words/font/emphasismark/) { get; set; } | Возвращает или задает знак акцента, примененный к данному форматированию. |
| [Engrave](../../aspose.words/font/engrave/) { get; set; } | True, если шрифт отформатирован как гравированный. |
| [Fill](../../aspose.words/font/fill/) { get; } | Получает форматирование заполнения для`Font` . |
| [Hidden](../../aspose.words/font/hidden/) { get; set; } | True, если шрифт отформатирован как скрытый текст. |
| [HighlightColor](../../aspose.words/font/highlightcolor/) { get; set; } | Получает или задает цвет выделения (маркера). |
| [Italic](../../aspose.words/font/italic/) { get; set; } | True, если шрифт отформатирован как курсив. |
| [ItalicBi](../../aspose.words/font/italicbi/) { get; set; } | True, если текст, написанный справа налево, отформатирован курсивом. |
| [Kerning](../../aspose.words/font/kerning/) { get; set; } | Возвращает или задает размер шрифта, при котором начинается кернинг. |
| [LineSpacing](../../aspose.words/font/linespacing/) { get; } | Возвращает межстрочный интервал данного шрифта (в пунктах). |
| [LocaleId](../../aspose.words/font/localeid/) { get; set; } | Возвращает или задает идентификатор локали (язык) форматируемых символов. |
| [LocaleIdBi](../../aspose.words/font/localeidbi/) { get; set; } | Возвращает или задает идентификатор локали (язык) отформатированных символов, написанных справа налево. |
| [LocaleIdFarEast](../../aspose.words/font/localeidfareast/) { get; set; } | Возвращает или задает идентификатор локали (язык) форматированных азиатских символов. |
| [Name](../../aspose.words/font/name/) { get; set; } | Получает или задает имя шрифта. |
| [NameAscii](../../aspose.words/font/nameascii/) { get; set; } | Возвращает или задает шрифт, используемый для латинского текста (символы с кодами символов от 0 (нуля) до 127). |
| [NameBi](../../aspose.words/font/namebi/) { get; set; } | Возвращает или задает имя шрифта в документе с письмом справа налево. |
| [NameFarEast](../../aspose.words/font/namefareast/) { get; set; } | Возвращает или задает имя восточноазиатского шрифта. |
| [NameOther](../../aspose.words/font/nameother/) { get; set; } | Возвращает или задает шрифт, используемый для символов с кодами от 128 до 255. |
| [NoProofing](../../aspose.words/font/noproofing/) { get; set; } | Истинно, когда отформатированные символы не подлежат проверке орфографии. |
| [NumberSpacing](../../aspose.words/font/numberspacing/) { get; set; } | Возвращает или задает тип интервала отображаемой цифры. |
| [Outline](../../aspose.words/font/outline/) { get; set; } | True, если шрифт отформатирован как контурный. |
| [Position](../../aspose.words/font/position/) { get; set; } | Возвращает или задает положение текста (в пунктах) относительно базовой линии. Положительное число поднимает текст, а отрицательное число опускает его. |
| [Scaling](../../aspose.words/font/scaling/) { get; set; } | Возвращает или задает масштабирование ширины символа в процентах. |
| [Shading](../../aspose.words/font/shading/) { get; } | Возвращает[`Shading`](../shading/) объект, который ссылается на форматирование штриховки для шрифта. |
| [Shadow](../../aspose.words/font/shadow/) { get; set; } | True, если шрифт отформатирован как затененный. |
| [Size](../../aspose.words/font/size/) { get; set; } | Получает или задает размер шрифта в пунктах. |
| [SizeBi](../../aspose.words/font/sizebi/) { get; set; } | Возвращает или задает размер шрифта в пунктах, используемый в документе с письмом справа налево. |
| [SmallCaps](../../aspose.words/font/smallcaps/) { get; set; } | True, если шрифт отформатирован как маленькие заглавные буквы. |
| [SnapToGrid](../../aspose.words/font/snaptogrid/) { get; set; } | Указывает, должен ли текущий шрифт использовать настройки сетки документа для символов в строке при компоновке. |
| [Spacing](../../aspose.words/font/spacing/) { get; set; } | Возвращает или задает интервал (в пунктах) между символами . |
| [StrikeThrough](../../aspose.words/font/strikethrough/) { get; set; } | True, если шрифт отформатирован как зачеркнутый текст. |
| [Style](../../aspose.words/font/style/) { get; set; } | Возвращает или задает стиль символов, применяемый к данному форматированию. |
| [StyleIdentifier](../../aspose.words/font/styleidentifier/) { get; set; } | Возвращает или задает независимый от локали идентификатор стиля символа, примененного к данному форматированию. |
| [StyleName](../../aspose.words/font/stylename/) { get; set; } | Возвращает или задает имя стиля символа, примененного к данному форматированию. |
| [Subscript](../../aspose.words/font/subscript/) { get; set; } | True, если шрифт отформатирован как подстрочный. |
| [Superscript](../../aspose.words/font/superscript/) { get; set; } | True, если шрифт отформатирован как верхний индекс. |
| [TextEffect](../../aspose.words/font/texteffect/) { get; set; } | Получает или задает эффект анимации шрифта. |
| [ThemeColor](../../aspose.words/font/themecolor/) { get; set; } | Получает или задает цвет темы в примененной цветовой схеме, которая связана с этим`Font` объект. |
| [ThemeFont](../../aspose.words/font/themefont/) { get; set; } | Возвращает или задает шрифт темы в примененной схеме шрифтов, которая связана с этим`Font` объект. |
| [ThemeFontAscii](../../aspose.words/font/themefontascii/) { get; set; } | Возвращает или задает шрифт темы, используемый для латинского текста (символы с кодами символов от 0 (нуля) до 127) в примененной схеме шрифтов, которая связана с этим`Font` объект. |
| [ThemeFontBi](../../aspose.words/font/themefontbi/) { get; set; } | Возвращает или задает шрифт темы в примененной схеме шрифтов, которая связана с этим`Font` object в документе с письмом справа налево. |
| [ThemeFontFarEast](../../aspose.words/font/themefontfareast/) { get; set; } | Возвращает или задает шрифт восточноазиатской темы в применяемой схеме шрифтов, которая связана с этим`Font` объект. |
| [ThemeFontOther](../../aspose.words/font/themefontother/) { get; set; } | Возвращает или задает шрифт темы, используемый для символов с кодами символов от 128 до 255 в примененной схеме шрифтов, которая связана с этим`Font` объект. |
| [TintAndShade](../../aspose.words/font/tintandshade/) { get; set; } | Возвращает или задает двойное значение, которое осветляет или затемняет цвет. |
| [Underline](../../aspose.words/font/underline/) { get; set; } | Возвращает или задает тип подчеркивания, применяемого к шрифту. |
| [UnderlineColor](../../aspose.words/font/underlinecolor/) { get; set; } | Возвращает или задает цвет подчеркивания, применяемого к шрифту. |

## Методы

| Имя | Описание |
| --- | --- |
| [ClearFormatting](../../aspose.words/font/clearformatting/)() | Сбрасывает форматирование шрифта до значения по умолчанию. |
| [HasDmlEffect](../../aspose.words/font/hasdmleffect/)(*[TextDmlEffect](../textdmleffect/)*) | Проверяет, применен ли определенный текстовый эффект DrawingML. |

## Примечания

Вы не создаете экземпляры`Font` класс напрямую. Вы просто используете `Font` для доступа к свойствам шрифта различных объектов, таких как[`Run`](../run/) , [`Paragraph`](../paragraph/) ,[`Style`](../style/) ,[`DocumentBuilder`](../documentbuilder/).

## Примеры

Показывает, как отформатировать фрагмент текста, используя его свойство шрифта.

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

// Создать пользовательский стиль абзаца.
Style style = doc.Styles.Add(StyleType.Paragraph, "MyStyle1");
style.Font.Size = 24;
style.Font.Name = "Verdana";
style.ParagraphFormat.SpaceAfter = 12;

// Создайте список и убедитесь, что абзацы, использующие этот стиль, будут использовать этот список.
style.ListFormat.List = doc.Lists.Add(ListTemplate.BulletDefault);
style.ListFormat.ListLevelNumber = 0;

// Применяем стиль абзаца к текущему абзацу конструктора документа, а затем добавляем текст.
builder.ParagraphFormat.Style = style;
builder.Writeln("Hello World: MyStyle1, bulleted list.");

// Измените стиль конструктора документов на такой, который не имеет форматирования списка, и напишите еще один абзац.
builder.ParagraphFormat.Style = doc.Styles["Normal"];
builder.Writeln("Hello World: Normal.");

builder.Document.Save(ArtifactsDir + "Styles.ParagraphStyleBulletedList.docx");
```

### Смотрите также

* пространство имен [Aspose.Words](../../aspose.words/)
* сборка [Aspose.Words](../../)
