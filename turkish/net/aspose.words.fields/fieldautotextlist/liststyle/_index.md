---
title: FieldAutoTextList.ListStyle
linktitle: ListStyle
articleTitle: ListStyle
second_title: Aspose.Words for .NET
description: FieldAutoTextList ListStyle mülk. Girişleri içerecek listenin temel aldığı stilin adını alır veya ayarlar C#'da.
type: docs
weight: 30
url: /tr/net/aspose.words.fields/fieldautotextlist/liststyle/
---
## FieldAutoTextList.ListStyle property

Girişleri içerecek listenin temel aldığı stilin adını alır veya ayarlar.

```csharp
public string ListStyle { get; set; }
```

## Örnekler

Otomatik Metin girişleri listesinden seçim yapmak için AUTOTEXTLIST alanının nasıl kullanılacağını gösterir.

```csharp
public void FieldAutoTextList()
{
    Document doc = new Document();

    // Bir sözlük belgesi oluşturun ve onu otomatik metin girişleriyle doldurun.
    doc.GlossaryDocument = new GlossaryDocument();
    AppendAutoTextEntry(doc.GlossaryDocument, "AutoText 1", "Contents of AutoText 1");
    AppendAutoTextEntry(doc.GlossaryDocument, "AutoText 2", "Contents of AutoText 2");
    AppendAutoTextEntry(doc.GlossaryDocument, "AutoText 3", "Contents of AutoText 3");

    DocumentBuilder builder = new DocumentBuilder(doc);

    // Bir AUTOTEXTLIST alanı oluşturun ve alanın Microsoft Word'de görüntüleyeceği metni ayarlayın.
    // Kullanıcının bir Otomatik Metin yapı taşı seçmesi için bu alanı sağ tıklatmasını isteyecek şekilde metni ayarlayın,
    // alanın kimin içeriğini göstereceği.
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
/// Otomatik Metin tipi bir yapı taşı oluşturun ve bunu bir sözlük belgesine ekleyin.
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

### Ayrıca bakınız

* class [FieldAutoTextList](../)
* ad alanı [Aspose.Words.Fields](../../../aspose.words.fields/)
* toplantı [Aspose.Words](../../../)
