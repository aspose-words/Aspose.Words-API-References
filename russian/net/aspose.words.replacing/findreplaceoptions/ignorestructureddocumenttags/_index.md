---
title: FindReplaceOptions.IgnoreStructuredDocumentTags
linktitle: IgnoreStructuredDocumentTags
articleTitle: IgnoreStructuredDocumentTags
second_title: Aspose.Words для .NET
description: Откройте для себя свойство FindReplaceOptions IgnoreStructuredDocumentTags. Управляйте игнорированием содержимого StructuredDocumentTag с помощью этой простой в использовании логической настройки.
type: docs
weight: 120
url: /ru/net/aspose.words.replacing/findreplaceoptions/ignorestructureddocumenttags/
---
## FindReplaceOptions.IgnoreStructuredDocumentTags property

Возвращает или задает логическое значение, указывающее, следует ли игнорировать содержимое[`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/) . Значение по умолчанию:`ЛОЖЬ` .

```csharp
public bool IgnoreStructuredDocumentTags { get; set; }
```

## Примечания

Когда эта опция установлена на`истинный` , содержание[`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/) будет рассматриваться как простой текст.

В противном случае,[`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/) будет обработан как отдельный Story , а заменяющий шаблон будет искаться отдельно для каждого[`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/) , так что если шаблон пересекает[`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/) , то для такого шаблона замена не будет выполнена.

## Примеры

Показывает, как игнорировать содержимое тегов при замене.

```csharp
Document doc = new Document(MyDir + "Structured document tags.docx");

// Этот абзац содержит SDT.
Paragraph p = (Paragraph)doc.FirstSection.Body.GetChild(NodeType.Paragraph, 2, true);
string textToSearch = p.ToString(SaveFormat.Text).Trim();

FindReplaceOptions options = new FindReplaceOptions() { IgnoreStructuredDocumentTags = true };
doc.Range.Replace(textToSearch, "replacement", options);

doc.Save(ArtifactsDir + "StructuredDocumentTag.IgnoreStructuredDocumentTags.docx");
```

### Смотрите также

* class [FindReplaceOptions](../)
* пространство имен [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* сборка [Aspose.Words](../../../)
