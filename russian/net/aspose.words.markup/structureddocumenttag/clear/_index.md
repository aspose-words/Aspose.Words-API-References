---
title: StructuredDocumentTag.Clear
linktitle: Clear
articleTitle: Clear
second_title: Aspose.Words для .NET
description: StructuredDocumentTag Clear метод. Очищает содержимое этого тега структурированного документа и отображает заполнитель если он определен на С#.
type: docs
weight: 340
url: /ru/net/aspose.words.markup/structureddocumenttag/clear/
---
## StructuredDocumentTag.Clear method

Очищает содержимое этого тега структурированного документа и отображает заполнитель, если он определен.

```csharp
public void Clear()
```

## Примечания

Невозможно очистить содержимое тега структурированного документа, если он имеет версии.

Если этот тег структурированного документа сопоставлен с пользовательским XML (с использованием[`XmlMapping`](../xmlmapping/) ), указанный узел XML очищается.

## Примеры

Показывает, как удалить содержимое элементов тега структурированного документа.

```csharp
Document doc = new Document();

// Создайте тег документа со структурой простого текста и затем добавьте его в документ.
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Block);
doc.FirstSection.Body.AppendChild(tag);

// Этот тег структурированного документа, имеющий форму текстового поля, уже отображает текст-заполнитель.
Assert.AreEqual("Click here to enter text.", tag.GetText().Trim());
Assert.True(tag.IsShowingPlaceholderText);

// Создаем строительный блок с текстовым содержимым.
GlossaryDocument glossaryDoc = doc.GlossaryDocument;
BuildingBlock substituteBlock = new BuildingBlock(glossaryDoc);
substituteBlock.Name = "My placeholder";
substituteBlock.AppendChild(new Section(glossaryDoc));
substituteBlock.FirstSection.EnsureMinimum();
substituteBlock.FirstSection.Body.FirstParagraph.AppendChild(new Run(glossaryDoc, "Custom placeholder text."));
glossaryDoc.AppendChild(substituteBlock);

// Установите для свойства PlaceholderName тега структурированного документа имя нашего строительного блока, чтобы получить
// тег структурированного документа для отображения содержимого стандартного блока вместо исходного текста по умолчанию.
tag.PlaceholderName = "My placeholder";

Assert.AreEqual("Custom placeholder text.", tag.GetText().Trim());
Assert.True(tag.IsShowingPlaceholderText);

// Отредактируйте текст тега структурированного документа и скройте текст-заполнитель.
Run run = (Run)tag.GetChild(NodeType.Run, 0, true);
run.Text = "New text.";
tag.IsShowingPlaceholderText = false;

Assert.AreEqual("New text.", tag.GetText().Trim());

// Используйте метод «Очистить», чтобы очистить содержимое тега структурированного документа и снова отобразить заполнитель.
tag.Clear();

Assert.True(tag.IsShowingPlaceholderText);
Assert.AreEqual("Custom placeholder text.", tag.GetText().Trim());
```

### Смотрите также

* class [StructuredDocumentTag](../)
* пространство имен [Aspose.Words.Markup](../../../aspose.words.markup/)
* сборка [Aspose.Words](../../../)
