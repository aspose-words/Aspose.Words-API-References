---
title: DocumentSplitCriteria Enum
linktitle: DocumentSplitCriteria
articleTitle: DocumentSplitCriteria
second_title: Aspose.Words для .NET
description: Узнайте, как Aspose.Words.Saving.DocumentSplitCriteria улучшает разделение документов для оптимальных форматов Html, Epub и Azw3. Оптимизируйте процесс сохранения!
type: docs
weight: 5710
url: /ru/net/aspose.words.saving/documentsplitcriteria/
---
## DocumentSplitCriteria enumeration

Указывает, как документ будет разделен на части при сохранении вHtml , Epub илиAzw3 формат.

```csharp
[Flags]
public enum DocumentSplitCriteria
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| None | `0` | Документ не разделен. |
| PageBreak | `1` | Документ разделен на части по явным разрывам страниц. Разрыв страницы может быть указан с помощью[`PageBreak`](../../aspose.words/controlchar/pagebreak/) символ, разрыв раздела, указывающий начало нового раздела на новой странице, или абзац, имеющий свой[`PageBreakBefore`](../../aspose.words/paragraphformat/pagebreakbefore/) свойство установлено в`истинный` . |
| ColumnBreak | `2` | Документ разделен на части по разрывам столбцов. Разрыв столбца может быть указан с помощью[`ColumnBreak`](../../aspose.words/controlchar/columnbreak/) символ или разрыв раздела, указывающий начало нового раздела в новом столбце. |
| SectionBreak | `4` | Документ разделен на части по разрыву раздела любого типа. |
| HeadingParagraph | `8` | Документ разделен на части по абзацу, отформатированные с использованием стиля заголовка**Заголовок 1** ,**Заголовок 2** и т.д. Использовать вместе с[`DocumentSplitHeadingLevel`](../htmlsaveoptions/documentsplitheadinglevel/) для указания уровней заголовков (от 1 до указанного уровня), по которым будет выполняться разделение. |

## Примечания

`DocumentSplitCriteria`это набор флагов, которые можно комбинировать. Например, вы можете разделить document на разрывах страниц и заголовках абзацев в одной и той же операции экспорта.

Различные критерии могут частично перекрываться. Например,**Заголовок 1** стиль часто обозначается как [`PageBreakBefore`](../../aspose.words/paragraphformat/pagebreakbefore/) имущество, поэтому оно подпадает под два критерия:PageBreak и HeadingParagraph. Некоторые разрывы разделов могут приводить к разрывам страниц и т. д. В типичных случаях указание только одного флага является наиболее практичным вариантом.

## Примеры

Показывает, как использовать определенную кодировку при сохранении документа в формате .epub.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Используйте объект SaveOptions, чтобы указать кодировку документа, который мы будем сохранять.
HtmlSaveOptions saveOptions = new HtmlSaveOptions();
saveOptions.SaveFormat = SaveFormat.Epub;
saveOptions.Encoding = Encoding.UTF8;

// По умолчанию выходной документ .epub будет иметь все свое содержимое в одной части HTML.
// Критерий разделения позволяет нам сегментировать документ на несколько частей HTML.
// Мы установим критерии для разделения документа на заголовочные абзацы.
// Это полезно для читателей, которые не могут читать HTML-файлы, размер которых больше определенного значения.
saveOptions.DocumentSplitCriteria = DocumentSplitCriteria.HeadingParagraph;

// Указываем, что мы хотим экспортировать свойства документа.
saveOptions.ExportDocumentProperties = true;

doc.Save(ArtifactsDir + "HtmlSaveOptions.Doc2EpubSaveOptions.epub", saveOptions);
```

### Смотрите также

* пространство имен [Aspose.Words.Saving](../../aspose.words.saving/)
* сборка [Aspose.Words](../../)
