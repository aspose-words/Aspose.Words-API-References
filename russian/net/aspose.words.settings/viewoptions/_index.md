---
title: ViewOptions Class
linktitle: ViewOptions
articleTitle: ViewOptions
second_title: Aspose.Words для .NET
description: Aspose.Words.Settings.ViewOptions сорт. Предоставляет различные параметры управляющие отображением документа в Microsoft Word на С#.
type: docs
weight: 5950
url: /ru/net/aspose.words.settings/viewoptions/
---
## ViewOptions class

Предоставляет различные параметры, управляющие отображением документа в Microsoft Word.

Чтобы узнать больше, посетите[Работа с параметрами и внешним видом документов Word](https://docs.aspose.com/words/net/work-with-word-document-options-and-appearance/) статья документации.

```csharp
public class ViewOptions
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [DisplayBackgroundShape](../../aspose.words.settings/viewoptions/displaybackgroundshape/) { get; set; } | Управляет отображением формы фона в виде макета печати. |
| [DoNotDisplayPageBoundaries](../../aspose.words.settings/viewoptions/donotdisplaypageboundaries/) { get; set; } | Отключает отображение пространства между верхней частью текста и верхним краем страницы. |
| [FormsDesign](../../aspose.words.settings/viewoptions/formsdesign/) { get; set; } | Указывает, находится ли документ в режиме разработки форм. |
| [ViewType](../../aspose.words.settings/viewoptions/viewtype/) { get; set; } | Управляет режимом просмотра в Microsoft Word. |
| [ZoomPercent](../../aspose.words.settings/viewoptions/zoompercent/) { get; set; } | Получает или задает процент (от 10 до 500), с которым вы хотите просмотреть документ. |
| [ZoomType](../../aspose.words.settings/viewoptions/zoomtype/) { get; set; } | Получает или задает значение масштабирования в зависимости от размера окна. |

## Примеры

Показывает, как установить пользовательский коэффициент масштабирования, который старые версии Microsoft Word будут применять к документу при загрузке.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

doc.ViewOptions.ViewType = ViewType.PageLayout;
doc.ViewOptions.ZoomPercent = 50;

Assert.AreEqual(ZoomType.Custom, doc.ViewOptions.ZoomType);
Assert.AreEqual(ZoomType.None, doc.ViewOptions.ZoomType);

doc.Save(ArtifactsDir + "ViewOptions.SetZoomPercentage.doc");
```

Показывает, как установить пользовательский тип масштабирования, который старые версии Microsoft Word будут применять к документу при загрузке.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Установите для свойства «ZoomType» значение «ZoomType.PageWidth», чтобы получить Microsoft Word
// для автоматического масштабирования документа по ширине страницы.
// Установите для свойства «ZoomType» значение «ZoomType.FullPage», чтобы получить Microsoft Word
// для автоматического масштабирования документа, чтобы сделать видимой всю первую страницу.
// Установите для свойства «ZoomType» значение «ZoomType.TextFit», чтобы получить Microsoft Word
// для автоматического масштабирования документа по размеру внутренних полей текста первой страницы.
doc.ViewOptions.ZoomType = zoomType;

doc.Save(ArtifactsDir + "ViewOptions.SetZoomType.doc");
```

### Смотрите также

* class [Document](../../aspose.words/document/)
* property [ViewOptions](../../aspose.words/document/viewoptions/)
* пространство имен [Aspose.Words.Settings](../../aspose.words.settings/)
* сборка [Aspose.Words](../../)
