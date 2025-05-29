---
title: FieldOptions.BuiltInTemplatesPaths
linktitle: BuiltInTemplatesPaths
articleTitle: BuiltInTemplatesPaths
second_title: .NET için Aspose.Words
description: Sorunsuz belge oluşturma için FieldOptions BuiltInTemplatesPaths özelliğiyle MS Word'ün yerleşik şablon yollarının nasıl yönetileceğini keşfedin.
type: docs
weight: 30
url: /tr/net/aspose.words.fields/fieldoptions/builtintemplatespaths/
---
## FieldOptions.BuiltInTemplatesPaths property

MS Word yerleşik şablonlarının yollarını alır veya ayarlar.

```csharp
public string[] BuiltInTemplatesPaths { get; set; }
```

## Notlar

Bu özellik tarafından kullanılıyor[`FieldAutoText`](../../fieldautotext/) Ve[`FieldGlossary`](../../fieldglossary/) alanlar, başvurulan otomatik metin girişi bulunmazsa[`AttachedTemplate`](../../../aspose.words/document/attachedtemplate/) şablon.

Varsayılan olarak MS Word yerleşik şablonları c:\Users\&lt;kullanıcı adı&gt;\AppData\Roaming\Microsoft\Document Building Blocks\1033\16\Built-In Building Blocks.dotx ve C:\Users\&lt;kullanıcı adı&gt;\AppData\Roaming\Microsoft\Templates\Normal.dotm dosyalarında depolar.

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

* class [FieldOptions](../)
* ad alanı [Aspose.Words.Fields](../../../aspose.words.fields/)
* toplantı [Aspose.Words](../../../)
