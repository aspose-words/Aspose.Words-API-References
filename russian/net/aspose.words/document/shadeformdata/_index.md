---
title: Document.ShadeFormData
second_title: Справочник по API Aspose.Words для .NET
description: Document свойство. Указывает включать ли затенение серым в полях формы.
type: docs
weight: 380
url: /ru/net/aspose.words/document/shadeformdata/
---
## Document.ShadeFormData property

Указывает, включать ли затенение серым в полях формы.

```csharp
public bool ShadeFormData { get; set; }
```

### Примеры

Показывает, как применить заливку серым к полям формы.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Hello world! ");
builder.InsertTextInput("My form field", TextFormFieldType.Regular, "",
    "Text contents of form field, which are shaded in grey by default.", 0);

// Мы можем отключить затенение серого, чтобы текст с закладкой сливался с другим текстом.
doc.ShadeFormData = useGreyShading;
doc.Save(ArtifactsDir + "Document.ShadeFormData.docx");
```

### Смотрите также

* class [Document](../)
* пространство имен [Aspose.Words](../../document/)
* сборка [Aspose.Words](../../../)


