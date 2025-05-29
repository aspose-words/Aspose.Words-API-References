---
title: FieldRD.IsPathRelative
linktitle: IsPathRelative
articleTitle: IsPathRelative
second_title: Aspose.Words для .NET
description: Откройте для себя свойство IsPathRelative FieldRD для простого управления путями документов. Упростите кодирование с помощью гибких настроек пути для повышения эффективности!
type: docs
weight: 30
url: /ru/net/aspose.words.fields/fieldrd/ispathrelative/
---
## FieldRD.IsPathRelative property

Возвращает или задает, является ли путь относительным к текущему документу.

```csharp
public bool IsPathRelative { get; set; }
```

## Примеры

Демонстрирует использование поля RD для создания записей оглавления из заголовков других документов.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Используйте конструктор документов для вставки оглавления,
// а затем добавьте одну запись для оглавления на следующей странице.
builder.InsertField(FieldType.FieldTOC, true);
builder.InsertBreak(BreakType.PageBreak);
builder.CurrentParagraph.ParagraphFormat.StyleName = "Heading 1";
builder.Writeln("TOC entry from within this document");

// Вставьте поле RD, которое ссылается на другой документ локальной файловой системы в своем свойстве FileName.
// TOC теперь также будет принимать все заголовки из указанного документа в качестве записей для своей таблицы.
FieldRD field = (FieldRD)builder.InsertField(FieldType.FieldRefDoc, true);
field.FileName = ArtifactsDir + "ReferencedDocument.docx";

Assert.AreEqual($" RD  {ArtifactsDir.Replace(@"\",@"\\")}ReferencedDocument.docx", field.GetFieldCode());

 // Создаем документ, на который ссылается поле RD, и вставляем заголовок.
// Этот заголовок будет отображаться как запись в поле TOC в нашем первом документе.
Document referencedDoc = new Document();
DocumentBuilder refDocBuilder = new DocumentBuilder(referencedDoc);
refDocBuilder.CurrentParagraph.ParagraphFormat.StyleName = "Heading 1";
refDocBuilder.Writeln("TOC entry from referenced document");
referencedDoc.Save(ArtifactsDir + "ReferencedDocument.docx");

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.RD.docx");
```

### Смотрите также

* class [FieldRD](../)
* пространство имен [Aspose.Words.Fields](../../../aspose.words.fields/)
* сборка [Aspose.Words](../../../)
