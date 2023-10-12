---
title: FieldTC.EntryLevel
second_title: Справочник по API Aspose.Words для .NET
description: FieldTC свойство. Получает или задает уровень записи.
type: docs
weight: 20
url: /ru/net/aspose.words.fields/fieldtc/entrylevel/
---
## FieldTC.EntryLevel property

Получает или задает уровень записи.

```csharp
public string EntryLevel { get; set; }
```

### Примеры

Показывает, как вставить поле TOC и отфильтровать поля TC, которые в конечном итоге станут записями.

```csharp
public void FieldTocEntryIdentifier()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Вставьте поле TOC, которое скомпилирует все поля TC в оглавление.
    FieldToc fieldToc = (FieldToc)builder.InsertField(FieldType.FieldTOC, true);

    // Настройте поле только для получения записей TC типа «A» и уровня записи от 1 до 3.
    fieldToc.EntryIdentifier = "A";
    fieldToc.EntryLevelRange = "1-3";

    Assert.AreEqual(" TOC  \\f A \\l 1-3", fieldToc.GetFieldCode());

    // Эти две записи появятся в таблице.
    builder.InsertBreak(BreakType.PageBreak);
    InsertTocEntry(builder, "TC field 1", "A", "1");
    InsertTocEntry(builder, "TC field 2", "A", "2");

    Assert.AreEqual(" TC  \"TC field 1\" \\n \\f A \\l 1", doc.Range.Fields[1].GetFieldCode());

    // Эта запись будет опущена в таблице, поскольку ее тип отличается от «A».
    InsertTocEntry(builder, "TC field 3", "B", "1");

    // Эта запись будет исключена из таблицы, поскольку ее уровень записи находится за пределами диапазона 1-3.
    InsertTocEntry(builder, "TC field 4", "A", "5");

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.TC.docx");
}

/// <summary>
/// Используйте конструктор документов, чтобы вставить поле TC.
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
* пространство имен [Aspose.Words.Fields](../../fieldtc/)
* сборка [Aspose.Words](../../../)


