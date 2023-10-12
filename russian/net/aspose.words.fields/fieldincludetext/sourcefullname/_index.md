---
title: FieldIncludeText.SourceFullName
second_title: Справочник по API Aspose.Words для .NET
description: FieldIncludeText свойство. Получает или задает расположение документа с помощью IRI.
type: docs
weight: 70
url: /ru/net/aspose.words.fields/fieldincludetext/sourcefullname/
---
## FieldIncludeText.SourceFullName property

Получает или задает расположение документа с помощью IRI.

```csharp
public string SourceFullName { get; set; }
```

### Примеры

Показывает, как создать поле INCLUDETEXT и установить его свойства.

```csharp
public void FieldIncludeText()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Ниже приведены два способа использования полей INCLUDETEXT для отображения содержимого XML-файла в локальной файловой системе.
    // 1 — выполнить XSL-преобразование XML-документа:
    FieldIncludeText fieldIncludeText = CreateFieldIncludeText(builder, MyDir + "CD collection data.xml", false, "text/xml", "XML", "ISO-8859-1");
    fieldIncludeText.XslTransformation = MyDir + "CD collection XSL transformation.xsl";

    builder.Writeln();

    // 2. Используйте XPath для получения определенных элементов из XML-документа:
    fieldIncludeText = CreateFieldIncludeText(builder, MyDir + "CD collection data.xml", false, "text/xml", "XML", "ISO-8859-1");
    fieldIncludeText.NamespaceMappings = "xmlns:n='myNamespace'";
    fieldIncludeText.XPath = "/catalog/cd/title";

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.INCLUDETEXT.docx");
}

/// <summary>
/// Используйте конструктор документов, чтобы вставить поле INCLUDETEXT с настраиваемыми свойствами.
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
* пространство имен [Aspose.Words.Fields](../../fieldincludetext/)
* сборка [Aspose.Words](../../../)


