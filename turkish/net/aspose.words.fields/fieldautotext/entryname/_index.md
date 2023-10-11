---
title: FieldAutoText.EntryName
second_title: Aspose.Words for .NET API Referansı
description: FieldAutoText mülk. Otomatik Metin girişinin adını alır veya ayarlar.
type: docs
weight: 20
url: /tr/net/aspose.words.fields/fieldautotext/entryname/
---
## FieldAutoText.EntryName property

Otomatik Metin girişinin adını alır veya ayarlar.

```csharp
public string EntryName { get; set; }
```

### Örnekler

OTOMETİN ve SÖZLÜK alanlarıyla bir yapı taşının nasıl görüntüleneceğini gösterir.

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

// Bir kaynak oluşturun ve bunu yapı taşımıza metin olarak ekleyin.
Document buildingBlockSource = new Document();
DocumentBuilder buildingBlockSourceBuilder = new DocumentBuilder(buildingBlockSource);
buildingBlockSourceBuilder.Writeln("Hello World!");

Node buildingBlockContent = doc.GlossaryDocument.ImportNode(buildingBlockSource.FirstSection, true);
buildingBlock.AppendChild(buildingBlockContent);

// Belgemizin veya ekli şablonunun içermeyebileceği parçaları içeren bir dosya ayarlayın.
doc.FieldOptions.BuiltInTemplatesPaths = new[] { MyDir + "Busniess brochure.dotx" };

DocumentBuilder builder = new DocumentBuilder(doc);

// Aşağıda yapı taşımızın içeriğini görüntülemek için alanları kullanmanın iki yolu verilmiştir.
// 1 - OTOMETİN alanını kullanma:
FieldAutoText fieldAutoText = (FieldAutoText)builder.InsertField(FieldType.FieldAutoText, true);
fieldAutoText.EntryName = "MyBlock";

Assert.AreEqual(" AUTOTEXT  MyBlock", fieldAutoText.GetFieldCode());

// 2 - SÖZLÜK alanını kullanma:
FieldGlossary fieldGlossary = (FieldGlossary)builder.InsertField(FieldType.FieldGlossary, true);
fieldGlossary.EntryName = "MyBlock";

Assert.AreEqual(" GLOSSARY  MyBlock", fieldGlossary.GetFieldCode());

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.AUTOTEXT.GLOSSARY.dotx");
```

### Ayrıca bakınız

* class [FieldAutoText](../)
* ad alanı [Aspose.Words.Fields](../../fieldautotext/)
* toplantı [Aspose.Words](../../../)


