---
title: PlainTextDocument.Text
second_title: Справочник по API Aspose.Words для .NET
description: PlainTextDocument свойство. Получает текстовое содержимое документа объединенное в строку.
type: docs
weight: 40
url: /ru/net/aspose.words/plaintextdocument/text/
---
## PlainTextDocument.Text property

Получает текстовое содержимое документа, объединенное в строку.

```csharp
public string Text { get; }
```

### Примеры

Показывает, как загрузить содержимое документа Microsoft Word в виде открытого текста.

```csharp
Document doc = new Document(); 
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

doc.Save(ArtifactsDir + "PlainTextDocument.Load.docx");

PlainTextDocument plaintext = new PlainTextDocument(ArtifactsDir + "PlainTextDocument.Load.docx");

Assert.AreEqual("Hello world!", plaintext.Text.Trim());
```

### Смотрите также

* class [PlainTextDocument](../)
* пространство имен [Aspose.Words](../../plaintextdocument/)
* сборка [Aspose.Words](../../../)


