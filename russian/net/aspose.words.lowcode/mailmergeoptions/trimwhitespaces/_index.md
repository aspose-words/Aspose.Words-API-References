---
title: MailMergeOptions.TrimWhitespaces
linktitle: TrimWhitespaces
articleTitle: TrimWhitespaces
second_title: Aspose.Words для .NET
description: Оптимизируйте слияние почты с помощью свойства TrimWhitespaces. Легко управляйте начальными и конечными пробелами для более чистых и профессиональных документов.
type: docs
weight: 110
url: /ru/net/aspose.words.lowcode/mailmergeoptions/trimwhitespaces/
---
## MailMergeOptions.TrimWhitespaces property

Возвращает или задает значение, указывающее, удаляются ли конечные и начальные пробелы из значений слияния почты.

```csharp
public bool TrimWhitespaces { get; set; }
```

## Примечания

Значение по умолчанию:`истинный` .

## Примеры

Показывает, как выполнить операцию слияния почты для одной записи.

```csharp
// Существует несколько способов выполнить операцию слияния почты:
string doc = MyDir + "Mail merge.doc";

string[] fieldNames = new string[] { "FirstName", "Location", "SpecialCharsInName()" };
string[] fieldValues = new string[] { "James Bond", "London", "Classified" };

MailMerger.Execute(doc, ArtifactsDir + "LowCode.MailMerge.1.docx", fieldNames, fieldValues);
MailMerger.Execute(doc, ArtifactsDir + "LowCode.MailMerge.2.docx", SaveFormat.Docx, fieldNames, fieldValues);
MailMergeOptions mailMergeOptions = new MailMergeOptions();
mailMergeOptions.TrimWhitespaces = true;
MailMerger.Execute(doc, ArtifactsDir + "LowCode.MailMerge.3.docx", SaveFormat.Docx, fieldNames, fieldValues, mailMergeOptions);
```

### Смотрите также

* class [MailMergeOptions](../)
* пространство имен [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* сборка [Aspose.Words](../../../)
