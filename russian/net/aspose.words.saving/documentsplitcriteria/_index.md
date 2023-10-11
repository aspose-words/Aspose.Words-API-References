---
title: Enum DocumentSplitCriteria
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.Saving.DocumentSplitCriteria перечисление. Указывает как документ разбивается на части при сохранении вHtml  Epub илиAzw3 формат.
type: docs
weight: 4960
url: /ru/net/aspose.words.saving/documentsplitcriteria/
---
## DocumentSplitCriteria enumeration

Указывает, как документ разбивается на части при сохранении вHtml , Epub илиAzw3 формат.

```csharp
[Flags]
public enum DocumentSplitCriteria
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| None | `0` | Документ не разделен. |
| PageBreak | `1` | Документ разбивается на части по явным разрывам страниц. Разрыв страницы может быть задан с помощью[`PageBreak`](../../aspose.words/controlchar/pagebreak/) символ, разрыв раздела, определяющий начало нового раздела на новой странице, или абзац, имеющий свой[`PageBreakBefore`](../../aspose.words/paragraphformat/pagebreakbefore/) свойство установлено в`истинный` . |
| ColumnBreak | `2` | Документ разбивается на части по разрывам столбцов. Разрыв столбца можно указать с помощью[`ColumnBreak`](../../aspose.words/controlchar/columnbreak/) символ or разрыв раздела, указывающий начало нового раздела в новом столбце. |
| SectionBreak | `4` | Документ разбивается на части при разрыве раздела любого типа. |
| HeadingParagraph | `8` | Документ разделен на части по абзацу, отформатированному с использованием стиля заголовка. **Заголовок 1** , **Заголовок 2** и т. д. Используйте вместе с[`DocumentSplitHeadingLevel`](../htmlsaveoptions/documentsplitheadinglevel/) чтобы указать уровни заголовков (от 1 до указанного уровня), по которым следует разбить. |

### Примечания

`DocumentSplitCriteria`представляет собой набор флагов, которые можно комбинировать. Например, вы можете разделить document на разрывы страниц и заголовки абзацев в одной операции экспорта.

Различные критерии могут частично перекрываться. Например, **Заголовок 1** стиль часто присваивается [`PageBreakBefore`](../../aspose.words/paragraphformat/pagebreakbefore/) имущество, поэтому оно подпадает под два критерия:PageBreak и HeadingParagraph. Некоторые разрывы разделов могут привести к разрывам страниц и т. д. В типичных случаях наиболее практичным вариантом является указание только одного флага.

### Примеры

Показывает, как использовать определенную кодировку при сохранении документа в формате .epub.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Используйте объект SaveOptions, чтобы указать кодировку документа, который мы сохраним.
HtmlSaveOptions saveOptions = new HtmlSaveOptions();
saveOptions.SaveFormat = SaveFormat.Epub;
saveOptions.Encoding = Encoding.UTF8;

// По умолчанию выходной документ .epub будет содержать все свое содержимое в одной HTML-части.
// Критерий разделения позволяет нам сегментировать документ на несколько частей HTML.
// Мы установим критерии для разделения документа на абзацы заголовков.
// Это полезно для читателей, которые не могут читать HTML-файлы, размер которых превышает определенный размер.
saveOptions.DocumentSplitCriteria = DocumentSplitCriteria.HeadingParagraph;

// Указываем, что хотим экспортировать свойства документа.
saveOptions.ExportDocumentProperties = true;

doc.Save(ArtifactsDir + "HtmlSaveOptions.Doc2EpubSaveOptions.epub", saveOptions);
```

### Смотрите также

* пространство имен [Aspose.Words.Saving](../../aspose.words.saving/)
* сборка [Aspose.Words](../../)


