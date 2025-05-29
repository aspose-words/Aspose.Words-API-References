---
title: ViewOptions Class
linktitle: ViewOptions
articleTitle: ViewOptions
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.Settings.ViewOptions для настройки отображения документов в Microsoft Word, что улучшит ваши возможности редактирования и производительность.
type: docs
weight: 6780
url: /ru/net/aspose.words.settings/viewoptions/
---
## ViewOptions class

Предоставляет различные параметры, которые управляют тем, как документ отображается в Microsoft Word.

Чтобы узнать больше, посетите[Работа с параметрами и внешним видом документов Word](https://docs.aspose.com/words/net/work-with-word-document-options-and-appearance/) документальная статья.

```csharp
public class ViewOptions
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [DisplayBackgroundShape](../../aspose.words.settings/viewoptions/displaybackgroundshape/) { get; set; } | Управляет отображением фоновой формы в режиме макета печати. |
| [DoNotDisplayPageBoundaries](../../aspose.words.settings/viewoptions/donotdisplaypageboundaries/) { get; set; } | Отключает отображение пространства между верхом текста и верхним краем страницы. |
| [FormsDesign](../../aspose.words.settings/viewoptions/formsdesign/) { get; set; } | Указывает, находится ли документ в режиме разработки форм. |
| [ViewType](../../aspose.words.settings/viewoptions/viewtype/) { get; set; } | Управляет режимом просмотра в Microsoft Word. |
| [ZoomPercent](../../aspose.words.settings/viewoptions/zoompercent/) { get; set; } | Возвращает или задает процент, с которым вы хотите просматривать документ. |
| [ZoomType](../../aspose.words.settings/viewoptions/zoomtype/) { get; set; } | Получает или задает значение масштабирования на основе размера окна. |

## Примеры

Показывает, как задать пользовательский коэффициент масштабирования, который старые версии Microsoft Word будут применять к документу при загрузке.

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

Показывает, как задать пользовательский тип масштабирования, который старые версии Microsoft Word будут применять к документу при загрузке.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Установите свойство "ZoomType" на "ZoomType.PageWidth", чтобы получить Microsoft Word
// для автоматического масштабирования документа по ширине страницы.
// Установите свойство "ZoomType" на "ZoomType.FullPage", чтобы получить Microsoft Word
// для автоматического масштабирования документа, чтобы сделать видимой всю первую страницу.
// Установите свойство "ZoomType" на "ZoomType.TextFit", чтобы получить Microsoft Word
// для автоматического масштабирования документа в соответствии с внутренними текстовыми полями первой страницы.
doc.ViewOptions.ZoomType = zoomType;

doc.Save(ArtifactsDir + "ViewOptions.SetZoomType.doc");
```

### Смотрите также

* class [Document](../../aspose.words/document/)
* property [ViewOptions](../../aspose.words/document/viewoptions/)
* пространство имен [Aspose.Words.Settings](../../aspose.words.settings/)
* сборка [Aspose.Words](../../)
