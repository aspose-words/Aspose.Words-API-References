---
title: StyleCollection Class
linktitle: StyleCollection
articleTitle: StyleCollection
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.StyleCollection, содержащий богатый набор встроенных и пользовательских объектов стилей для улучшения форматирования и дизайна вашего документа.
type: docs
weight: 6990
url: /ru/net/aspose.words/stylecollection/
---
## StyleCollection class

Коллекция[`Style`](../style/)объекты, представляющие как встроенные, так и пользовательские стили в документе.

Чтобы узнать больше, посетите[Работа со стилями и темами](https://docs.aspose.com/words/net/working-with-styles-and-themes/) документальная статья.

```csharp
public class StyleCollection : IEnumerable<Style>
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [Count](../../aspose.words/stylecollection/count/) { get; } | Получает количество стилей в коллекции. |
| [DefaultFont](../../aspose.words/stylecollection/defaultfont/) { get; } | Получает форматирование текста документа по умолчанию. |
| [DefaultParagraphFormat](../../aspose.words/stylecollection/defaultparagraphformat/) { get; } | Получает форматирование абзаца документа по умолчанию. |
| [Document](../../aspose.words/stylecollection/document/) { get; } | Получает документ владельца. |
| [Item](../../aspose.words/stylecollection/item/) { get; } | Получает стиль по имени или псевдониму. (3 indexers) |

## Методы

| Имя | Описание |
| --- | --- |
| [Add](../../aspose.words/stylecollection/add/)(*[StyleType](../styletype/), string*) | Создает новый пользовательский стиль и добавляет его в коллекцию. |
| [AddCopy](../../aspose.words/stylecollection/addcopy/)(*[Style](../style/)*) | Копирует стиль в эту коллекцию. |
| [ClearQuickStyleGallery](../../aspose.words/stylecollection/clearquickstylegallery/)() | Удаляет все стили из панели «Галерея быстрых стилей». |
| [GetEnumerator](../../aspose.words/stylecollection/getenumerator/)() | Получает объект перечислителя, который будет перечислять стили в алфавитном порядке их имен. |

## Примеры

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

* class [Style](../style/)
* пространство имен [Aspose.Words](../../aspose.words/)
* сборка [Aspose.Words](../../)
