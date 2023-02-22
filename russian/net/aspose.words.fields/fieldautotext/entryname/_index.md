---
title: FieldAutoText.EntryName
second_title: Справочник по API Aspose.Words для .NET
description: FieldAutoText свойство. Получает или задает имя записи автотекста.
type: docs
weight: 20
url: /ru/net/aspose.words.fields/fieldautotext/entryname/
---
## FieldAutoText.EntryName property

Получает или задает имя записи автотекста.

```csharp
public string EntryName { get; set; }
```

### Примеры

Показывает, как отобразить стандартный блок с полями АВТОТЕКСТ и ГЛОССАРИЙ.

```csharp
Document doc = new Document();

// Создайте глоссарий и добавьте в него стандартный блок автотекста.
doc.GlossaryDocument = new GlossaryDocument();
BuildingBlock buildingBlock = new BuildingBlock(doc.GlossaryDocument);
buildingBlock.Name = "MyBlock";
buildingBlock.Gallery = BuildingBlockGallery.AutoText;
buildingBlock.Category = "General";
buildingBlock.Description = "MyBlock description";
buildingBlock.Behavior = BuildingBlockBehavior.Paragraph;
doc.GlossaryDocument.AppendChild(buildingBlock);

// Создадим источник и добавим его как текст в наш строительный блок.
Document buildingBlockSource = new Document();
DocumentBuilder buildingBlockSourceBuilder = new DocumentBuilder(buildingBlockSource);
buildingBlockSourceBuilder.Writeln("Hello World!");

Node buildingBlockContent = doc.GlossaryDocument.ImportNode(buildingBlockSource.FirstSection, true);
buildingBlock.AppendChild(buildingBlockContent);

// Установить файл, который содержит части, которые наш документ или прикрепленный к нему шаблон могут не содержать.
doc.FieldOptions.BuiltInTemplatesPaths = new[] { MyDir + "Busniess brochure.dotx" };

DocumentBuilder builder = new DocumentBuilder(doc);

// Ниже приведены два способа использования полей для отображения содержимого нашего стандартного блока.
// 1 - Использование поля АВТОТЕКСТ:
FieldAutoText fieldAutoText = (FieldAutoText)builder.InsertField(FieldType.FieldAutoText, true);
fieldAutoText.EntryName = "MyBlock";

Assert.AreEqual(" AUTOTEXT  MyBlock", fieldAutoText.GetFieldCode());

// 2 - Использование поля ГЛОССАРИЙ:
FieldGlossary fieldGlossary = (FieldGlossary)builder.InsertField(FieldType.FieldGlossary, true);
fieldGlossary.EntryName = "MyBlock";

Assert.AreEqual(" GLOSSARY  MyBlock", fieldGlossary.GetFieldCode());

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.AUTOTEXT.GLOSSARY.dotx");
```

### Смотрите также

* class [FieldAutoText](../)
* пространство имен [Aspose.Words.Fields](../../fieldautotext/)
* сборка [Aspose.Words](../../../)


