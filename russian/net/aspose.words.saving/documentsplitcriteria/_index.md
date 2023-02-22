---
title: Enum DocumentSplitCriteria
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.Saving.DocumentSplitCriteria перечисление. Указывает как документ разбивается на части при сохранении вHtml илиEpub формат.
type: docs
weight: 4700
url: /ru/net/aspose.words.saving/documentsplitcriteria/
---
## DocumentSplitCriteria enumeration

Указывает, как документ разбивается на части при сохранении вHtml илиEpub формат.

```csharp
[Flags]
public enum DocumentSplitCriteria
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| None | `0` | Документ не разделен. |
| PageBreak | `1` | Документ разбит на части по явным разрывам страниц. Разрыв страницы может быть задан[`PageBreak`](../../aspose.words/controlchar/pagebreak/) символ, разрыв раздела, указывающий начало нового раздела на новой странице, или абзац, который имеет свой[`PageBreakBefore`](../../aspose.words/paragraphformat/pagebreakbefore/) свойство установлено на`истинный` . |
| ColumnBreak | `2` | Документ разбит на части по разрывам столбцов. Разрыв столбца может быть указан с помощью[`ColumnBreak`](../../aspose.words/controlchar/columnbreak/) символ or разрыв раздела, указывающий начало нового раздела в новом столбце. |
| SectionBreak | `4` | Документ разбивается на части при разрыве раздела любого типа. |
| HeadingParagraph | `8` | Документ разбит на части по абзацу, отформатированному с использованием стиля заголовка **Заголовок 1** , **Заголовок 2** и т.д. Использовать вместе с[`DocumentSplitHeadingLevel`](../htmlsaveoptions/documentsplitheadinglevel/) указать уровни заголовков (от 1 до указанного уровня), на которых следует разделить. |

### Примечания

`DocumentSplitCriteria`представляет собой набор флагов, которые можно комбинировать. Например, вы можете разделить document на разрывы страниц и абзацы заголовков в одной и той же операции экспорта.

Различные критерии могут частично совпадать. Например, **Заголовок 1** стиль часто дается [`PageBreakBefore`](../../aspose.words/paragraphformat/pagebreakbefore/) свойство, поэтому оно подпадает под два критерия:PageBreak и HeadingParagraph. Некоторые разрывы разделов могут привести к разрывам страниц и так далее. В типичных случаях наиболее практичным вариантом является указание только одного флага.

### Примеры

Показывает, как использовать определенную кодировку при сохранении документа в формате .epub.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Используйте объект SaveOptions для указания кодировки сохраняемого документа.
HtmlSaveOptions saveOptions = new HtmlSaveOptions();
saveOptions.SaveFormat = SaveFormat.Epub;
saveOptions.Encoding = Encoding.UTF8;

// По умолчанию выходной документ .epub будет иметь все свое содержимое в одной HTML-части.
// Критерий разделения позволяет нам разделить документ на несколько частей HTML.
// Мы установим критерии для разделения документа на абзацы заголовков.
// Это полезно для читателей, которые не могут читать файлы HTML, размер которых превышает определенный.
saveOptions.DocumentSplitCriteria = DocumentSplitCriteria.HeadingParagraph;

// Указываем, что хотим экспортировать свойства документа.
saveOptions.ExportDocumentProperties = true;

doc.Save(ArtifactsDir + "HtmlSaveOptions.Doc2EpubSaveOptions.epub", saveOptions);
```

### Смотрите также

* пространство имен [Aspose.Words.Saving](../../aspose.words.saving/)
* сборка [Aspose.Words](../../)


