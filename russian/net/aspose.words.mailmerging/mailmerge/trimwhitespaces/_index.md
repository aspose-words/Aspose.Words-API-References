---
title: MailMerge.TrimWhitespaces
linktitle: TrimWhitespaces
articleTitle: TrimWhitespaces
second_title: Aspose.Words для .NET
description: Оптимизируйте процесс слияния почты с помощью свойства TrimWhitespaces, гарантируя чистоту данных за счет удаления начальных и конечных пробелов для получения точных результатов.
type: docs
weight: 130
url: /ru/net/aspose.words.mailmerging/mailmerge/trimwhitespaces/
---
## MailMerge.TrimWhitespaces property

Возвращает или задает значение, указывающее, удаляются ли конечные и начальные пробелы из значений слияния почты.

```csharp
public bool TrimWhitespaces { get; set; }
```

## Примечания

Значение по умолчанию:`истинный` .

## Примеры

Показывает, как обрезать пробелы из значений источника данных при выполнении слияния почты.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertField("MERGEFIELD myMergeField", null);

doc.MailMerge.TrimWhitespaces = trimWhitespaces;
doc.MailMerge.Execute(new[] { "myMergeField" }, new object[] { "\t hello world! " });

Assert.AreEqual(trimWhitespaces ? "hello world!\f" : "\t hello world! \f", doc.GetText());
```

### Смотрите также

* class [MailMerge](../)
* пространство имен [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* сборка [Aspose.Words](../../../)
