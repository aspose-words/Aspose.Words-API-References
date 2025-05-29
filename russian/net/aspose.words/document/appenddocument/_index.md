---
title: Document.AppendDocument
linktitle: AppendDocument
articleTitle: AppendDocument
second_title: Aspose.Words для .NET
description: Легко добавляйте документы с помощью нашего метода добавления документов. Улучшите свой рабочий процесс, легко интегрируя контент в существующие файлы.
type: docs
weight: 570
url: /ru/net/aspose.words/document/appenddocument/
---
## AppendDocument(*[Document](../), [ImportFormatMode](../../importformatmode/)*) {#appenddocument}

Добавляет указанный документ в конец данного документа.

```csharp
public void AppendDocument(Document srcDoc, ImportFormatMode importFormatMode)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| srcDoc | Document | Документ для присоединения. |
| importFormatMode | ImportFormatMode | Указывает, как объединить конфликтующие стили форматирования. |

## Примеры

Показывает, как добавить документ в конец другого документа.

```csharp
Document srcDoc = new Document();
srcDoc.FirstSection.Body.AppendParagraph("Source document text. ");

Document dstDoc = new Document();
dstDoc.FirstSection.Body.AppendParagraph("Destination document text. ");

// Добавить исходный документ к целевому документу, сохраняя его форматирование,
// затем сохраните исходный документ в локальной файловой системе.
dstDoc.AppendDocument(srcDoc, ImportFormatMode.KeepSourceFormatting);
dstDoc.Save(ArtifactsDir + "Document.AppendDocument.docx");
```

Показывает, как добавить все документы в папке в конец шаблона документа.

```csharp
Document dstDoc = new Document();

DocumentBuilder builder = new DocumentBuilder(dstDoc);
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;
builder.Writeln("Template Document");
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Normal;
builder.Writeln("Some content here");
// Добавить все незашифрованные документы с расширением .doc
// из каталога нашей локальной файловой системы в базовый документ.
List<string> docFiles = Directory.GetFiles(MyDir, "*.doc").Where(item => item.EndsWith(".doc")).ToList();
foreach (string fileName in docFiles)
{
    FileFormatInfo info = FileFormatUtil.DetectFileFormat(fileName);
    if (info.IsEncrypted)
        continue;

    Document srcDoc = new Document(fileName);
    dstDoc.AppendDocument(srcDoc, ImportFormatMode.UseDestinationStyles);
}

dstDoc.Save(ArtifactsDir + "Document.AppendAllDocumentsInFolder.doc");
```

### Смотрите также

* enum [ImportFormatMode](../../importformatmode/)
* class [Document](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)

---

## AppendDocument(*[Document](../), [ImportFormatMode](../../importformatmode/), [ImportFormatOptions](../../importformatoptions/)*) {#appenddocument_1}

Добавляет указанный документ в конец данного документа.

```csharp
public void AppendDocument(Document srcDoc, ImportFormatMode importFormatMode, 
    ImportFormatOptions importFormatOptions)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| srcDoc | Document | Документ для присоединения. |
| importFormatMode | ImportFormatMode | Указывает, как объединить конфликтующие стили форматирования. |
| importFormatOptions | ImportFormatOptions | Позволяет указать параметры, влияющие на форматирование результирующего документа. |

## Примеры

Показывает, как управлять конфликтами стилей списков при добавлении клона документа к самому себе.

```csharp
Document srcDoc = new Document(MyDir + "List item.docx");
Document dstDoc = new Document(MyDir + "List item.docx");

// Если есть конфликт стилей списка, применяем формат списка исходного документа.
// Установите свойство «KeepSourceNumbering» в значение «false», чтобы не импортировать какие-либо номера списков в целевой документ.
// Установите свойство "KeepSourceNumbering" в значение "true", импортируйте все конфликтующие
// нумерация в стиле списка с тем же внешним видом, что и в исходном документе.
DocumentBuilder builder = new DocumentBuilder(dstDoc);
builder.MoveToDocumentEnd();
builder.InsertBreak(BreakType.SectionBreakNewPage);

ImportFormatOptions options = new ImportFormatOptions();
options.KeepSourceNumbering = keepSourceNumbering;
builder.InsertDocument(srcDoc, ImportFormatMode.KeepSourceFormatting, options);

dstDoc.UpdateListLabels();
```

Показывает, как управлять конфликтами стилей списков при вставке документа.

```csharp
Document dstDoc = new Document();
DocumentBuilder builder = new DocumentBuilder(dstDoc);
builder.InsertBreak(BreakType.ParagraphBreak);

dstDoc.Lists.Add(ListTemplate.NumberDefault);
Aspose.Words.Lists.List list = dstDoc.Lists[0];

builder.ListFormat.List = list;

for (int i = 1; i <= 15; i++)
    builder.Write($"List Item {i}\n");

Document attachDoc = (Document)dstDoc.Clone(true);

// Если есть конфликт стилей списка, применяем формат списка исходного документа.
// Установите свойство «KeepSourceNumbering» в значение «false», чтобы не импортировать какие-либо номера списков в целевой документ.
// Установите свойство "KeepSourceNumbering" в значение "true", импортируйте все конфликтующие
// нумерация в стиле списка с тем же внешним видом, что и в исходном документе.
ImportFormatOptions importOptions = new ImportFormatOptions();
importOptions.KeepSourceNumbering = keepSourceNumbering;

builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.InsertDocument(attachDoc, ImportFormatMode.KeepSourceFormatting, importOptions);

dstDoc.Save(ArtifactsDir + "DocumentBuilder.InsertDocumentAndResolveStyles.docx");
```

Показывает, как управлять конфликтами стилей списков при добавлении документа.

```csharp
// Загружаем документ с текстом в пользовательском стиле и клонируем его.
Document srcDoc = new Document(MyDir + "Custom list numbering.docx");
Document dstDoc = srcDoc.Clone();

// Теперь у нас есть два документа, каждый с идентичным стилем под названием «CustomStyle».
// Измените цвет текста для одного из стилей, чтобы выделить его среди других.
dstDoc.Styles["CustomStyle"].Font.Color = Color.DarkRed;

// Если есть конфликт стилей списка, применяем формат списка исходного документа.
// Установите свойство «KeepSourceNumbering» в значение «false», чтобы не импортировать какие-либо номера списков в целевой документ.
// Установите свойство "KeepSourceNumbering" в значение "true", импортируйте все конфликтующие
// нумерация в стиле списка с тем же внешним видом, что и в исходном документе.
ImportFormatOptions options = new ImportFormatOptions();
options.KeepSourceNumbering = keepSourceNumbering;

// Объединение двух документов с разными стилями и одинаковыми именами приводит к конфликту стилей.
// Мы можем указать режим формата импорта при добавлении документов, чтобы разрешить этот конфликт.
dstDoc.AppendDocument(srcDoc, ImportFormatMode.KeepDifferentStyles, options);
dstDoc.UpdateListLabels();

dstDoc.Save(ArtifactsDir + "DocumentBuilder.AppendDocumentAndResolveStyles.docx");
```

### Смотрите также

* enum [ImportFormatMode](../../importformatmode/)
* class [ImportFormatOptions](../../importformatoptions/)
* class [Document](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
