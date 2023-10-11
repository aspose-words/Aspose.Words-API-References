---
title: FieldGlossary.EntryName
second_title: Справочник по API Aspose.Words для .NET
description: FieldGlossary свойство. Получает или задает имя вставляемой записи глоссария.
type: docs
weight: 20
url: /ru/net/aspose.words.fields/fieldglossary/entryname/
---
## FieldGlossary.EntryName property

Получает или задает имя вставляемой записи глоссария.

```csharp
public string EntryName { get; set; }
```

### Примеры

Показывает, как отобразить стандартный блок с полями АВТОТЕКСТ и ГЛОССАРИЙ.

```csharp
Document doc = new Document();

// Создаем документ глоссария и добавляем в него стандартный блок автотекста.
doc.GlossaryDocument = new GlossaryDocument();
BuildingBlock buildingBlock = new BuildingBlock(doc.GlossaryDocument);
buildingBlock.Name = "MyBlock";
buildingBlock.Gallery = BuildingBlockGallery.AutoText;
buildingBlock.Category = "General";
buildingBlock.Description = "MyBlock description";
buildingBlock.Behavior = BuildingBlockBehavior.Paragraph;
doc.GlossaryDocument.AppendChild(buildingBlock);

// Создаем источник и добавляем его в виде текста в наш строительный блок.
Document buildingBlockSource = new Document();
DocumentBuilder buildingBlockSourceBuilder = new DocumentBuilder(buildingBlockSource);
buildingBlockSourceBuilder.Writeln("Hello World!");

Node buildingBlockContent = doc.GlossaryDocument.ImportNode(buildingBlockSource.FirstSection, true);
buildingBlock.AppendChild(buildingBlockContent);

// Устанавливаем файл, содержащий части, которые не могут содержаться в нашем документе или прикрепленном к нему шаблоне.
doc.FieldOptions.BuiltInTemplatesPaths = new[] { MyDir + "Busniess brochure.dotx" };

DocumentBuilder builder = new DocumentBuilder(doc);

// Ниже приведены два способа использования полей для отображения содержимого нашего строительного блока.
// 1 - Использование поля АВТОТЕКСТ:
FieldAutoText fieldAutoText = (FieldAutoText)builder.InsertField(FieldType.FieldAutoText, true);
fieldAutoText.EntryName = "MyBlock";

Assert.AreEqual(" AUTOTEXT  MyBlock", fieldAutoText.GetFieldCode());

// 2 – Использование поля ГЛОССАРИЙ:
FieldGlossary fieldGlossary = (FieldGlossary)builder.InsertField(FieldType.FieldGlossary, true);
fieldGlossary.EntryName = "MyBlock";

Assert.AreEqual(" GLOSSARY  MyBlock", fieldGlossary.GetFieldCode());

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.AUTOTEXT.GLOSSARY.dotx");
```

### Смотрите также

* class [FieldGlossary](../)
* пространство имен [Aspose.Words.Fields](../../fieldglossary/)
* сборка [Aspose.Words](../../../)


