---
title: FieldOptions.BuiltInTemplatesPaths
second_title: Aspose.Words for .NET API Referansı
description: FieldOptions mülk. MS Word yerleşik şablonlarının yollarını alır veya ayarlar.
type: docs
weight: 20
url: /tr/net/aspose.words.fields/fieldoptions/builtintemplatespaths/
---
## FieldOptions.BuiltInTemplatesPaths property

MS Word yerleşik şablonlarının yollarını alır veya ayarlar.

```csharp
public string[] BuiltInTemplatesPaths { get; set; }
```

### Notlar

Bu özellik tarafından kullanılır[`FieldAutoText`](../../fieldautotext/) ve[`FieldGlossary`](../../fieldglossary/) alanlarda, başvurulan otomatik metin girişi[`AttachedTemplate`](../../../aspose.words/document/attachedtemplate/) şablon.

Varsayılan olarak MS Word, yerleşik şablonları c:\Users\&lt;username&gt;\AppData\Roaming\Microsoft\Document Building Blocks\1033\16\Built-In Building Blocks.dotx ve C:\Users\&lt;username&gt;\ dizininde saklar. AppData\Roaming\Microsoft\Templates\Normal.dotm dosyaları.

### Örnekler

AUTOTEXT ve SÖZLÜK alanlarıyla bir yapı taşının nasıl görüntüleneceğini gösterir.

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

// Belgemizin veya ekli şablonunun içermeyebileceği bölümleri içeren bir dosya ayarlayın.
doc.FieldOptions.BuiltInTemplatesPaths = new[] { MyDir + "Busniess brochure.dotx" };

DocumentBuilder builder = new DocumentBuilder(doc);

// Aşağıda, yapı taşımızın içeriğini görüntülemek için alanları kullanmanın iki yolu bulunmaktadır.
// 1 - Bir AUTOTEXT alanı kullanma:
FieldAutoText fieldAutoText = (FieldAutoText)builder.InsertField(FieldType.FieldAutoText, true);
fieldAutoText.EntryName = "MyBlock";

Assert.AreEqual(" AUTOTEXT  MyBlock", fieldAutoText.GetFieldCode());

// 2 - SÖZLÜK alanı kullanma:
FieldGlossary fieldGlossary = (FieldGlossary)builder.InsertField(FieldType.FieldGlossary, true);
fieldGlossary.EntryName = "MyBlock";

Assert.AreEqual(" GLOSSARY  MyBlock", fieldGlossary.GetFieldCode());

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.AUTOTEXT.GLOSSARY.dotx");
```

### Ayrıca bakınız

* class [FieldOptions](../)
* ad alanı [Aspose.Words.Fields](../../fieldoptions/)
* toplantı [Aspose.Words](../../../)


