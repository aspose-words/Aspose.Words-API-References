---
title: DocumentBuilder.InsertDocument
second_title: Справочник по API Aspose.Words для .NET
description: DocumentBuilder метод. Вставляет документ в позицию курсора.
type: docs
weight: 310
url: /ru/net/aspose.words/documentbuilder/insertdocument/
---
## InsertDocument(Document, ImportFormatMode) {#insertdocument}

Вставляет документ в позицию курсора.

```csharp
public Node InsertDocument(Document srcDoc, ImportFormatMode importFormatMode)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| srcDoc | Document | Исходный документ для вставки. |
| importFormatMode | ImportFormatMode | Указывает, как объединить конфликтующее форматирование стилей. |

### Возвращаемое значение

Первый узел вставленного контента.

### Примечания

Этот метод имитирует поведение MS Word, как если бы было нажато CTRL+'A' (выделить все содержимое), затем CTRL+'C' (копировать выбранное в буфер) внутри одного документа , а затем CTRL+'V' (вставить содержимое из буфер) внутри другого документа.

### Примеры

Показывает, как вставить документ в другой документ.

```csharp
Document doc = new Document(MyDir + "Document.docx");

DocumentBuilder builder = new DocumentBuilder(doc);
builder.MoveToDocumentEnd();
builder.InsertBreak(BreakType.PageBreak);

Document docToInsert = new Document(MyDir + "Formatted elements.docx");

builder.InsertDocument(docToInsert, ImportFormatMode.KeepSourceFormatting);
builder.Document.Save(ArtifactsDir + "DocumentBuilder.InsertDocument.docx");
```

### Смотрите также

* class [Node](../../node/)
* class [Document](../../document/)
* enum [ImportFormatMode](../../importformatmode/)
* class [DocumentBuilder](../)
* пространство имен [Aspose.Words](../../documentbuilder/)
* сборка [Aspose.Words](../../../)

---

## InsertDocument(Document, ImportFormatMode, ImportFormatOptions) {#insertdocument_1}

Вставляет документ в позицию курсора.

```csharp
public Node InsertDocument(Document srcDoc, ImportFormatMode importFormatMode, 
    ImportFormatOptions importFormatOptions)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| srcDoc | Document | Исходный документ для вставки. |
| importFormatMode | ImportFormatMode | Указывает, как объединить конфликтующее форматирование стилей. |
| importFormatOptions | ImportFormatOptions | Позволяет указать параметры, влияющие на форматирование результирующего документа. |

### Возвращаемое значение

Первый узел вставленного контента.

### Примечания

Этот метод имитирует поведение MS Word, как если бы было нажато CTRL+'A' (выделить все содержимое), затем CTRL+'C' (копировать выбранное в буфер) внутри одного документа , а затем CTRL+'V' (вставить содержимое из буфер) внутри другого документа.

### Примеры

Показывает, как устранить повторяющиеся стили при вставке документов.

```csharp
Document dstDoc = new Document();
DocumentBuilder builder = new DocumentBuilder(dstDoc);

Style myStyle = builder.Document.Styles.Add(StyleType.Paragraph, "MyStyle");
myStyle.Font.Size = 14;
myStyle.Font.Name = "Courier New";
myStyle.Font.Color = Color.Blue;

builder.ParagraphFormat.StyleName = myStyle.Name;
builder.Writeln("Hello world!");

// Клонируем документ и редактируем стиль «MyStyle» клона, чтобы его цвет отличался от цвета оригинала.
// Если мы вставим клон в исходный документ, два стиля с одинаковым именем вызовут конфликт.
Document srcDoc = dstDoc.Clone();
srcDoc.Styles["MyStyle"].Font.Color = Color.Red;

// Когда мы включаем SmartStyleBehavior и используем режим формата импорта KeepSourceFormatting,
// Aspose.Words разрешит конфликты стилей путем преобразования стилей исходного документа.
// с теми же именами, что и стили назначения, в прямые атрибуты абзаца.
ImportFormatOptions options = new ImportFormatOptions();
options.SmartStyleBehavior = true;

builder.InsertDocument(srcDoc, ImportFormatMode.KeepSourceFormatting, options);

dstDoc.Save(ArtifactsDir + "DocumentBuilder.SmartStyleBehavior.docx");
```

### Смотрите также

* class [Node](../../node/)
* class [Document](../../document/)
* enum [ImportFormatMode](../../importformatmode/)
* class [ImportFormatOptions](../../importformatoptions/)
* class [DocumentBuilder](../)
* пространство имен [Aspose.Words](../../documentbuilder/)
* сборка [Aspose.Words](../../../)


