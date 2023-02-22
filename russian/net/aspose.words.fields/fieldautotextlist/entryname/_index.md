---
title: FieldAutoTextList.EntryName
second_title: Справочник по API Aspose.Words для .NET
description: FieldAutoTextList свойство. Получает или задает имя записи автотекста.
type: docs
weight: 20
url: /ru/net/aspose.words.fields/fieldautotextlist/entryname/
---
## FieldAutoTextList.EntryName property

Получает или задает имя записи автотекста.

```csharp
public string EntryName { get; set; }
```

### Примеры

Показывает, как использовать поле AUTOTEXTLIST для выбора из списка записей автотекста.

```csharp
{
    Document doc = new Document();

    // Создайте глоссарий и заполните его автотекстовыми записями.
    doc.GlossaryDocument = new GlossaryDocument();
    AppendAutoTextEntry(doc.GlossaryDocument, "AutoText 1", "Contents of AutoText 1");
    AppendAutoTextEntry(doc.GlossaryDocument, "AutoText 2", "Contents of AutoText 2");
    AppendAutoTextEntry(doc.GlossaryDocument, "AutoText 3", "Contents of AutoText 3");

    DocumentBuilder builder = new DocumentBuilder(doc);

    // Создайте поле АВТОТЕКСТ и задайте текст, который поле будет отображать в Microsoft Word.
    // Установите текст, чтобы предложить пользователю щелкнуть правой кнопкой мыши это поле, чтобы выбрать стандартный блок автотекста,
    // чье содержимое будет отображаться в поле.
    FieldAutoTextList field = (FieldAutoTextList)builder.InsertField(FieldType.FieldAutoTextList, true);
    field.EntryName = "Right click here to select an AutoText block";
    field.ListStyle = "Heading 1";
    field.ScreenTip = "Hover tip text for AutoTextList goes here";

    Assert.AreEqual(" AUTOTEXTLIST  \"Right click here to select an AutoText block\" " +
                    "\\s \"Heading 1\" " +
                    "\\t \"Hover tip text for AutoTextList goes here\"", field.GetFieldCode());

    doc.Save(ArtifactsDir + "Field.AUTOTEXTLIST.dotx");

/// <summary>
/// Создайте строительный блок типа AutoText и добавьте его в глоссарий.
/// </summary>
private static void AppendAutoTextEntry(GlossaryDocument glossaryDoc, string name, string contents)
{
    BuildingBlock buildingBlock = new BuildingBlock(glossaryDoc);
    buildingBlock.Name = name;
    buildingBlock.Gallery = BuildingBlockGallery.AutoText;
    buildingBlock.Category = "General";
    buildingBlock.Behavior = BuildingBlockBehavior.Paragraph;

    Section section = new Section(glossaryDoc);
    section.AppendChild(new Body(glossaryDoc));
    section.Body.AppendParagraph(contents);
    buildingBlock.AppendChild(section);

    glossaryDoc.AppendChild(buildingBlock);
}
```

### Смотрите также

* class [FieldAutoTextList](../)
* пространство имен [Aspose.Words.Fields](../../fieldautotextlist/)
* сборка [Aspose.Words](../../../)


