---
title: FieldIncludeText.NamespaceMappings
linktitle: NamespaceMappings
articleTitle: NamespaceMappings
second_title: Aspose.Words для .NET
description: Откройте для себя свойство FieldIncludeText NamespaceMappings, которое позволяет легко управлять сопоставлениями пространств имен для запросов XPath, повышая эффективность обработки данных.
type: docs
weight: 60
url: /ru/net/aspose.words.fields/fieldincludetext/namespacemappings/
---
## FieldIncludeText.NamespaceMappings property

Получает или задает сопоставления пространств имен для запросов XPath.

```csharp
public string NamespaceMappings { get; set; }
```

## Примеры

Показывает, как создать поле INCLUDETEXT и задать его свойства.

```csharp
public void FieldIncludeText()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Ниже приведены два способа использования полей INCLUDETEXT для отображения содержимого XML-файла в локальной файловой системе.
    // 1 — Выполнить XSL-преобразование XML-документа:
    FieldIncludeText fieldIncludeText = CreateFieldIncludeText(builder, MyDir + "CD collection data.xml", false, "text/xml", "XML", "ISO-8859-1");
    fieldIncludeText.XslTransformation = MyDir + "CD collection XSL transformation.xsl";

    builder.Writeln();

    // 2 — Используйте XPath для извлечения определенных элементов из XML-документа:
    fieldIncludeText = CreateFieldIncludeText(builder, MyDir + "CD collection data.xml", false, "text/xml", "XML", "ISO-8859-1");
    fieldIncludeText.NamespaceMappings = "xmlns:n='myNamespace'";
    fieldIncludeText.XPath = "/catalog/cd/title";

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.INCLUDETEXT.docx");
}

/// <summary>
/// Используйте конструктор документов для вставки поля INCLUDETEXT с пользовательскими свойствами.
/// </summary>
public FieldIncludeText CreateFieldIncludeText(DocumentBuilder builder, string sourceFullName, bool lockFields, string mimeType, string textConverter, string encoding)
{
    FieldIncludeText fieldIncludeText = (FieldIncludeText)builder.InsertField(FieldType.FieldIncludeText, true);
    fieldIncludeText.SourceFullName = sourceFullName;
    fieldIncludeText.LockFields = lockFields;
    fieldIncludeText.MimeType = mimeType;
    fieldIncludeText.TextConverter = textConverter;
    fieldIncludeText.Encoding = encoding;

    return fieldIncludeText;
}
```

### Смотрите также

* class [FieldIncludeText](../)
* пространство имен [Aspose.Words.Fields](../../../aspose.words.fields/)
* сборка [Aspose.Words](../../../)
