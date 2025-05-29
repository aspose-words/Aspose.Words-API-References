---
title: StyleCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words для .NET
description: Откройте для себя мощное свойство StyleCollection Item, позволяющее легко извлекать стили по имени или псевдониму, что значительно упростит процесс проектирования!
type: docs
weight: 50
url: /ru/net/aspose.words/stylecollection/item/
---
## StyleCollection indexer (1 of 3)

Получает стиль по имени или псевдониму.

```csharp
public Style this[string name] { get; }
```

## Примечания

Чувствителен к регистру, возвращает`нулевой` если стиль с указанным именем не найден.

Если это английское название встроенного стиля, который еще не существует, он автоматически создается.

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

* class [Style](../../style/)
* class [StyleCollection](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)

---

## StyleCollection indexer (2 of 3)

Получает встроенный стиль по его независимому от локали идентификатору.

```csharp
public Style this[StyleIdentifier sti] { get; }
```

| Параметр | Описание |
| --- | --- |
| sti | А[`StyleIdentifier`](../../styleidentifier/) значение, указывающее встроенный стиль для извлечения. |

## Примечания

При обращении к стилю, который еще не существует, автоматически создает его.

## Примеры

Показывает, как добавить стиль в коллекцию стилей документа.

```csharp
Document doc = new Document();

StyleCollection styles = doc.Styles;
// Устанавливаем параметры по умолчанию для новых стилей, которые мы позже можем добавить в эту коллекцию.
styles.DefaultFont.Name = "Courier New";
// Если мы добавим стиль "StyleType.Paragraph", коллекция применит значения
// его свойство "DefaultParagraphFormat" к свойству "ParagraphFormat" стиля.
styles.DefaultParagraphFormat.FirstLineIndent = 15.0;
// Добавьте стиль, а затем проверьте, что у него настройки по умолчанию.
styles.Add(StyleType.Paragraph, "MyStyle");

Assert.AreEqual("Courier New", styles[4].Font.Name);
Assert.AreEqual(15.0, styles["MyStyle"].ParagraphFormat.FirstLineIndent);
```

### Смотрите также

* class [Style](../../style/)
* enum [StyleIdentifier](../../styleidentifier/)
* class [StyleCollection](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)

---

## StyleCollection indexer (3 of 3)

Получает стиль по индексу.

```csharp
public Style this[int index] { get; }
```

## Примеры

Показывает, как добавить стиль в коллекцию стилей документа.

```csharp
Document doc = new Document();

StyleCollection styles = doc.Styles;
// Устанавливаем параметры по умолчанию для новых стилей, которые мы позже можем добавить в эту коллекцию.
styles.DefaultFont.Name = "Courier New";
// Если мы добавим стиль "StyleType.Paragraph", коллекция применит значения
// его свойство "DefaultParagraphFormat" к свойству "ParagraphFormat" стиля.
styles.DefaultParagraphFormat.FirstLineIndent = 15.0;
// Добавьте стиль, а затем проверьте, что у него настройки по умолчанию.
styles.Add(StyleType.Paragraph, "MyStyle");

Assert.AreEqual("Courier New", styles[4].Font.Name);
Assert.AreEqual(15.0, styles["MyStyle"].ParagraphFormat.FirstLineIndent);
```

### Смотрите также

* class [Style](../../style/)
* class [StyleCollection](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
