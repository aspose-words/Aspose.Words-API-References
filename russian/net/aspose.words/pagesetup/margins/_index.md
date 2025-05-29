---
title: PageSetup.Margins
linktitle: Margins
articleTitle: Margins
second_title: Aspose.Words для .NET
description: Легко настройте поля страницы с помощью свойства PageSetup. Настройте параметры для оптимальной компоновки и представления. Улучшите внешний вид вашего документа!
type: docs
weight: 260
url: /ru/net/aspose.words/pagesetup/margins/
---
## PageSetup.Margins property

Возвращает или устанавливает предустановку[`Margins`](../../margins/) страницы.

```csharp
public Margins Margins { get; set; }
```

## Примеры

Показывает, когда следует пересчитывать макет страницы документа.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Сохранение документа в формате PDF, в виде изображения или печать в первый раз автоматически
// кэшируем макет документа на его страницах.
doc.Save(ArtifactsDir + "Document.UpdatePageLayout.1.pdf");

// Измените документ каким-либо образом.
doc.Styles["Normal"].Font.Size = 6;
doc.Sections[0].PageSetup.Orientation = Aspose.Words.Orientation.Landscape;
doc.Sections[0].PageSetup.Margins = Margins.Mirrored;

// В текущей версии Aspose.Words изменение документа не приводит к его автоматической перестройке
// кэшированный макет страницы. Если мы хотим кэшированный макет
// чтобы оставаться в курсе событий, нам придется обновлять его вручную.
doc.UpdatePageLayout();

doc.Save(ArtifactsDir + "Document.UpdatePageLayout.2.pdf");
```

### Смотрите также

* enum [Margins](../../margins/)
* class [PageSetup](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
