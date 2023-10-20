---
title: FieldOptions.BuiltInTemplatesPaths
linktitle: BuiltInTemplatesPaths
articleTitle: BuiltInTemplatesPaths
second_title: Aspose.Words для .NET
description: FieldOptions BuiltInTemplatesPaths свойство. Получает или задает пути к встроенным шаблонам MS Word на С#.
type: docs
weight: 30
url: /ru/net/aspose.words.fields/fieldoptions/builtintemplatespaths/
---
## FieldOptions.BuiltInTemplatesPaths property

Получает или задает пути к встроенным шаблонам MS Word.

```csharp
public string[] BuiltInTemplatesPaths { get; set; }
```

## Примечания

Это свойство используется[`FieldAutoText`](../../fieldautotext/) и[`FieldGlossary`](../../fieldglossary/) поля, если указанная запись автоматического текста не найдена в[`AttachedTemplate`](../../../aspose.words/document/attachedtemplate/) шаблон.

По умолчанию MS Word хранит встроенные шаблоны в папках c:\Users\&lt;имя пользователя&gt;\AppData\Roaming\Microsoft\Document Building Blocks\1033\16\Built-In Building Blocks.dotx и C:\Users\&lt;имя пользователя&gt;\. Файлы AppData\Roaming\Microsoft\Templates\Normal.dotm.

## Примеры

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

* class [FieldOptions](../)
* пространство имен [Aspose.Words.Fields](../../../aspose.words.fields/)
* сборка [Aspose.Words](../../../)
