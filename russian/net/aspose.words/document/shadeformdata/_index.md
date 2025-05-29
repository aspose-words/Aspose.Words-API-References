---
title: Document.ShadeFormData
linktitle: ShadeFormData
articleTitle: ShadeFormData
second_title: Aspose.Words для .NET
description: Узнайте, как использовать свойство ShadeFormData для улучшения видимости формы с помощью серой заливки, что улучшает пользовательский опыт и доступность.
type: docs
weight: 400
url: /ru/net/aspose.words/document/shadeformdata/
---
## Document.ShadeFormData property

Указывает, следует ли включать серую заливку полей формы.

```csharp
public bool ShadeFormData { get; set; }
```

## Примеры

Показывает, как применять серую заливку к полям формы.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Hello world! ");
builder.InsertTextInput("My form field", TextFormFieldType.Regular, "",
    "Text contents of form field, which are shaded in grey by default.", 0);

// Мы можем отключить серую заливку, чтобы текст закладки сливался с другим текстом.
doc.ShadeFormData = useGreyShading;
doc.Save(ArtifactsDir + "Document.ShadeFormData.docx");
```

### Смотрите также

* class [Document](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
