---
title: FieldAutoTextList.ScreenTip
linktitle: ScreenTip
articleTitle: ScreenTip
second_title: Aspose.Words для .NET
description: Откройте для себя свойство FieldAutoTextList ScreenTip, легко настройте текст всплывающей подсказки для улучшения пользовательского опыта и ясности вашего приложения.
type: docs
weight: 40
url: /ru/net/aspose.words.fields/fieldautotextlist/screentip/
---
## FieldAutoTextList.ScreenTip property

Возвращает или задает текст всплывающей подсказки для отображения.

```csharp
public string ScreenTip { get; set; }
```

## Примеры

Показывает, как использовать поле AUTOTEXTLIST для выбора из списка записей автотекста.

```csharp
public void FieldAutoTextList()
{
    Document doc = new Document();

    // Создайте документ глоссария и заполните его автоматическими текстовыми записями.
    doc.GlossaryDocument = new GlossaryDocument();
    AppendAutoTextEntry(doc.GlossaryDocument, "AutoText 1", "Contents of AutoText 1");
    AppendAutoTextEntry(doc.GlossaryDocument, "AutoText 2", "Contents of AutoText 2");
    AppendAutoTextEntry(doc.GlossaryDocument, "AutoText 3", "Contents of AutoText 3");

    DocumentBuilder builder = new DocumentBuilder(doc);

    // Создайте поле AUTOTEXTLIST и задайте текст, который будет отображаться в поле в Microsoft Word.
    // Задайте текст, который предложит пользователю щелкнуть правой кнопкой мыши по этому полю, чтобы выбрать блок AutoText,
    // содержимое которого будет отображаться в поле.
    FieldAutoTextList field = (FieldAutoTextList)builder.InsertField(FieldType.FieldAutoTextList, true);
    field.EntryName = "Right click here to select an AutoText block";
    field.ListStyle = "Heading 1";
    field.ScreenTip = "Hover tip text for AutoTextList goes here";

    Assert.AreEqual(" AUTOTEXTLIST  \"Right click here to select an AutoText block\" " +
                    "\\s \"Heading 1\" " +
                    "\\t \"Hover tip text for AutoTextList goes here\"", field.GetFieldCode());

    doc.Save(ArtifactsDir + "Field.AUTOTEXTLIST.dotx");
}

/// <summary>
/// Создайте строительный блок типа AutoText и добавьте его в документ глоссария.
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
* пространство имен [Aspose.Words.Fields](../../../aspose.words.fields/)
* сборка [Aspose.Words](../../../)
