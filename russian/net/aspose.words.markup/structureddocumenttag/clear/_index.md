---
title: StructuredDocumentTag.Clear
linktitle: Clear
articleTitle: Clear
second_title: Aspose.Words для .NET
description: С легкостью очищайте содержимое структурированного тега документа с помощью метода Clear и отображайте определенный заполнитель для улучшенного управления документами.
type: docs
weight: 360
url: /ru/net/aspose.words.markup/structureddocumenttag/clear/
---
## StructuredDocumentTag.Clear method

Очищает содержимое этого структурированного тега документа и отображает заполнитель, если он определен.

```csharp
public void Clear()
```

## Примечания

Невозможно очистить содержимое структурированного тега документа, если в нем есть изменения.

Если этот структурированный тег документа сопоставлен с пользовательским XML (с использованием[`XmlMapping`](../xmlmapping/) ), указанный узел XML очищается.

## Примеры

Показывает, как удалить содержимое элементов тега структурированного документа.

```csharp
Document doc = new Document();

// Создайте структурированный тег документа с простым текстом, а затем добавьте его к документу.
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Block);
doc.FirstSection.Body.AppendChild(tag);

// Этот структурированный тег документа, имеющий форму текстового поля, уже отображает текст-заполнитель.
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

// Установите свойство "PlaceholderName" тега структурированного документа на имя нашего строительного блока, чтобы получить
// структурированный тег документа для отображения содержимого строительного блока вместо исходного текста по умолчанию.
tag.PlaceholderName = "My placeholder";

Assert.AreEqual("Custom placeholder text.", tag.GetText().Trim());
Assert.True(tag.IsShowingPlaceholderText);

// Отредактируйте текст структурированного тега документа и скройте текст-заполнитель.
Run run = (Run)tag.GetChild(NodeType.Run, 0, true);
run.Text = "New text.";
tag.IsShowingPlaceholderText = false;

Assert.AreEqual("New text.", tag.GetText().Trim());

// Используйте метод «Очистить», чтобы очистить содержимое этого структурированного тега документа и снова отобразить заполнитель.
tag.Clear();

Assert.True(tag.IsShowingPlaceholderText);
Assert.AreEqual("Custom placeholder text.", tag.GetText().Trim());
```

### Смотрите также

* class [StructuredDocumentTag](../)
* пространство имен [Aspose.Words.Markup](../../../aspose.words.markup/)
* сборка [Aspose.Words](../../../)
