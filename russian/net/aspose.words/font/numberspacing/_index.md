---
title: Font.NumberSpacing
linktitle: NumberSpacing
articleTitle: NumberSpacing
second_title: Aspose.Words для .NET
description: Откройте для себя свойство Font NumberSpacing для настройки интервала между цифрами для улучшения читаемости и дизайна. Оптимизируйте свою типографику сегодня!
type: docs
weight: 290
url: /ru/net/aspose.words/font/numberspacing/
---
## Font.NumberSpacing property

Возвращает или задает тип интервала отображаемой цифры.

```csharp
public NumSpacing NumberSpacing { get; set; }
```

## Примеры

Показывает, как задать тип интервала между цифрами.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Этот эффект поддерживается только в новых версиях MS Word.
doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2019);

builder.Write("1 ");
builder.Write("This is an example");

Run run = doc.FirstSection.Body.FirstParagraph.Runs[0];
if (run.Font.NumberSpacing == NumSpacing.Default)
    run.Font.NumberSpacing = NumSpacing.Proportional;

doc.Save(ArtifactsDir + "Fonts.NumberSpacing.docx");
```

### Смотрите также

* enum [NumSpacing](../../numspacing/)
* class [Font](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
