---
title: FieldTC.OmitPageNumber
linktitle: OmitPageNumber
articleTitle: OmitPageNumber
second_title: Aspose.Words для .NET
description: Откройте для себя свойство FieldTC OmitPageNumber — управляйте видимостью номеров страниц оглавления для повышения ясности и профессионализма документа.
type: docs
weight: 30
url: /ru/net/aspose.words.fields/fieldtc/omitpagenumber/
---
## FieldTC.OmitPageNumber property

Возвращает или задает, следует ли опускать номер страницы в оглавлении для этого поля.

```csharp
public bool OmitPageNumber { get; set; }
```

## Примеры

Показывает, как вставить поле TOC и отфильтровать, какие поля TC в конечном итоге станут записями.

```csharp
public void FieldTocEntryIdentifier()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Вставьте поле TOC, которое объединит все поля TC в таблицу содержания.
    FieldToc fieldToc = (FieldToc)builder.InsertField(FieldType.FieldTOC, true);

    // Настройте поле только для выбора записей TC типа «A» и уровня записи от 1 до 3.
    fieldToc.EntryIdentifier = "A";
    fieldToc.EntryLevelRange = "1-3";

    Assert.AreEqual(" TOC  \\f A \\l 1-3", fieldToc.GetFieldCode());

    // Эти две записи появятся в таблице.
    builder.InsertBreak(BreakType.PageBreak);
    InsertTocEntry(builder, "TC field 1", "A", "1");
    InsertTocEntry(builder, "TC field 2", "A", "2");

    Assert.AreEqual(" TC  \"TC field 1\" \\n \\f A \\l 1", doc.Range.Fields[1].GetFieldCode());

    // Эта запись будет исключена из таблицы, поскольку ее тип отличается от «A».
    InsertTocEntry(builder, "TC field 3", "B", "1");

    // Эта запись будет исключена из таблицы, поскольку ее уровень входа находится за пределами диапазона 1-3.
    InsertTocEntry(builder, "TC field 4", "A", "5");

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.TC.docx");
}

/// <summary>
/// Используйте конструктор документов для вставки поля TC.
/// </summary>
public void InsertTocEntry(DocumentBuilder builder, string text, string typeIdentifier, string entryLevel)
{
    FieldTC fieldTc = (FieldTC)builder.InsertField(FieldType.FieldTOCEntry, true);
    fieldTc.OmitPageNumber = true;
    fieldTc.Text = text;
    fieldTc.TypeIdentifier = typeIdentifier;
    fieldTc.EntryLevel = entryLevel;
}
```

### Смотрите также

* class [FieldTC](../)
* пространство имен [Aspose.Words.Fields](../../../aspose.words.fields/)
* сборка [Aspose.Words](../../../)
