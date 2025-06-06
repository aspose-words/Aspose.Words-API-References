---
title: FieldGlossary.EntryName
linktitle: EntryName
articleTitle: EntryName
second_title: .NET için Aspose.Words
description: Sözlük girişlerini kolayca yönetmek için FieldGlossary EntryName özelliğini keşfedin; sorunsuz içerik entegrasyonu için adlar alın veya ayarlayın.
type: docs
weight: 20
url: /tr/net/aspose.words.fields/fieldglossary/entryname/
---
## FieldGlossary.EntryName property

Eklenecek sözlük girişinin adını alır veya ayarlar.

```csharp
public string EntryName { get; set; }
```

## Örnekler

Bir yapı bloğunun AUTOTEXT ve GLOSSARY alanlarıyla nasıl görüntüleneceğini gösterir.

```csharp
Document doc = new Document();

// Bir sözlük belgesi oluşturun ve buna bir Otomatik Metin yapı taşı ekleyin.
doc.GlossaryDocument = new GlossaryDocument();
BuildingBlock buildingBlock = new BuildingBlock(doc.GlossaryDocument);
buildingBlock.Name = "MyBlock";
buildingBlock.Gallery = BuildingBlockGallery.AutoText;
buildingBlock.Category = "General";
buildingBlock.Description = "MyBlock description";
buildingBlock.Behavior = BuildingBlockBehavior.Paragraph;
doc.GlossaryDocument.AppendChild(buildingBlock);

// Bir kaynak oluşturup bunu yapı taşımıza metin olarak ekleyelim.
Document buildingBlockSource = new Document();
DocumentBuilder buildingBlockSourceBuilder = new DocumentBuilder(buildingBlockSource);
buildingBlockSourceBuilder.Writeln("Hello World!");

Node buildingBlockContent = doc.GlossaryDocument.ImportNode(buildingBlockSource.FirstSection, true);
buildingBlock.AppendChild(buildingBlockContent);

// Belgemizin veya ekli şablonunun içermeyebileceği parçaları içeren bir dosya ayarlayın.
doc.FieldOptions.BuiltInTemplatesPaths = new[] { MyDir + "Busniess brochure.dotx" };

DocumentBuilder builder = new DocumentBuilder(doc);

// Aşağıda yapı taşımızın içeriğini görüntülemek için alanları kullanmanın iki yolu bulunmaktadır.
// 1 - AUTOTEXT alanının kullanılması:
FieldAutoText fieldAutoText = (FieldAutoText)builder.InsertField(FieldType.FieldAutoText, true);
fieldAutoText.EntryName = "MyBlock";

Assert.AreEqual(" AUTOTEXT  MyBlock", fieldAutoText.GetFieldCode());

// 2 - GLOSSARY alanının kullanılması:
FieldGlossary fieldGlossary = (FieldGlossary)builder.InsertField(FieldType.FieldGlossary, true);
fieldGlossary.EntryName = "MyBlock";

Assert.AreEqual(" GLOSSARY  MyBlock", fieldGlossary.GetFieldCode());

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.AUTOTEXT.GLOSSARY.dotx");
```

### Ayrıca bakınız

* class [FieldGlossary](../)
* ad alanı [Aspose.Words.Fields](../../../aspose.words.fields/)
* toplantı [Aspose.Words](../../../)
