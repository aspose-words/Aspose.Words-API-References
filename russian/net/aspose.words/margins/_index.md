---
title: Margins Enum
linktitle: Margins
articleTitle: Margins
second_title: Aspose.Words для .NET
description: Откройте для себя перечисление Aspose.Words.Margins для настраиваемых полей документа. Улучшите форматирование документа с помощью простых в использовании предустановок!
type: docs
weight: 4580
url: /ru/net/aspose.words/margins/
---
## Margins enumeration

Указывает предустановленные поля.

```csharp
public enum Margins
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| Normal | `0` | Нормальные поля. |
| Narrow | `1` | Узкие поля. |
| Moderate | `2` | Умеренные поля. |
| Wide | `3` | Широкие поля. |
| Mirrored | `4` | Зеркальные поля. |
| Custom | `5` | Пользовательские поля. |

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

* пространство имен [Aspose.Words](../../aspose.words/)
* сборка [Aspose.Words](../../)
