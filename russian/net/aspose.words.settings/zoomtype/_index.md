---
title: ZoomType Enum
linktitle: ZoomType
articleTitle: ZoomType
second_title: Aspose.Words для .NET
description: Откройте для себя перечисление Aspose.Words.Settings.ZoomType для настройки размеров отображения документов в Microsoft Word для оптимального просмотра и производительности.
type: docs
weight: 6810
url: /ru/net/aspose.words.settings/zoomtype/
---
## ZoomType enumeration

Возможные значения размера документа, отображаемого на экране в Microsoft Word.

```csharp
public enum ZoomType
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| Custom | `0` | Процент масштабирования задается явно. Он не пересчитывается автоматически при изменении размера элемента управления. |
| None | `0` | Указывает на использование явного процента масштабирования. То же, что иCustom . |
| FullPage | `1` | Процент масштабирования автоматически пересчитывается для размещения на одной полной странице. |
| PageWidth | `2` | Процент масштабирования автоматически пересчитывается в соответствии с шириной страницы. |
| TextFit | `3` | Процент масштабирования автоматически пересчитывается для вписывания текста. |

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

### Смотрите также

* class [ViewOptions](../viewoptions/)
* property [ZoomType](../viewoptions/zoomtype/)
* пространство имен [Aspose.Words.Settings](../../aspose.words.settings/)
* сборка [Aspose.Words](../../)
