---
title: PageSetup.Bidi
linktitle: Bidi
articleTitle: Bidi
second_title: Aspose.Words для .NET
description: Откройте для себя свойство PageSetup Bidi для бесшовного двунаправленного форматирования текста. Улучшите свои документы с помощью поддержки сложных скриптов для лучшей читаемости!
type: docs
weight: 10
url: /ru/net/aspose.words/pagesetup/bidi/
---
## PageSetup.Bidi property

Указывает, что этот раздел содержит двунаправленный (сложные скрипты) текст.

```csharp
public bool Bidi { get; set; }
```

## Примечания

Когда`истинный`столбцы в этом разделе располагаются справа налево.

## Примеры

Показывает, как задать порядок текстовых столбцов в разделе.

```csharp
Document doc = new Document();

PageSetup pageSetup = doc.Sections[0].PageSetup;
pageSetup.TextColumns.SetCount(3);

DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Column 1.");
builder.InsertBreak(BreakType.ColumnBreak);
builder.Write("Column 2.");
builder.InsertBreak(BreakType.ColumnBreak);
builder.Write("Column 3.");

// Установите свойство «Bidi» в значение «true», чтобы расположить столбцы, начиная с правой стороны страницы.
// Порядок столбцов будет соответствовать направлению текста справа налево.
// Установите свойство «Bidi» в значение «false», чтобы расположить столбцы, начиная с левой стороны страницы.
// Порядок столбцов будет соответствовать направлению текста слева направо.
pageSetup.Bidi = reverseColumns;

doc.Save(ArtifactsDir + "PageSetup.Bidi.docx");
```

### Смотрите также

* class [PageSetup](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
