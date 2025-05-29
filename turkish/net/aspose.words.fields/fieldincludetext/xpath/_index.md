---
title: FieldIncludeText.XPath
linktitle: XPath
articleTitle: XPath
second_title: .NET için Aspose.Words
description: Belirli XML bölümlerine kolayca erişmek ve bunları değiştirmek için FieldIncludeText XPath özelliğini keşfedin; böylece veri yönetimi verimliliğinizi artırın.
type: docs
weight: 90
url: /tr/net/aspose.words.fields/fieldincludetext/xpath/
---
## FieldIncludeText.XPath property

XML dosyasının istenen kısmı için XPath'yi alır veya ayarlar.

```csharp
public string XPath { get; set; }
```

## Örnekler

INCLUDETEXT alanının nasıl oluşturulacağını ve özelliklerinin nasıl ayarlanacağını gösterir.

```csharp
public void FieldIncludeText()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Aşağıda, yerel dosya sisteminde bir XML dosyasının içeriğini görüntülemek için INCLUDETEXT alanlarını kullanmanın iki yolu bulunmaktadır.
    // 1 - Bir XML belgesinde XSL dönüşümü gerçekleştirin:
    FieldIncludeText fieldIncludeText = CreateFieldIncludeText(builder, MyDir + "CD collection data.xml", false, "text/xml", "XML", "ISO-8859-1");
    fieldIncludeText.XslTransformation = MyDir + "CD collection XSL transformation.xsl";

    builder.Writeln();

    // 2 - Bir XML belgesinden belirli öğeleri almak için bir XPath kullanın:
    fieldIncludeText = CreateFieldIncludeText(builder, MyDir + "CD collection data.xml", false, "text/xml", "XML", "ISO-8859-1");
    fieldIncludeText.NamespaceMappings = "xmlns:n='myNamespace'";
    fieldIncludeText.XPath = "/catalog/cd/title";

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.INCLUDETEXT.docx");
}

/// <summary>
/// Özel özelliklere sahip bir INCLUDETEXT alanı eklemek için bir belge oluşturucu kullanın.
/// </summary>
public FieldIncludeText CreateFieldIncludeText(DocumentBuilder builder, string sourceFullName, bool lockFields, string mimeType, string textConverter, string encoding)
{
    FieldIncludeText fieldIncludeText = (FieldIncludeText)builder.InsertField(FieldType.FieldIncludeText, true);
    fieldIncludeText.SourceFullName = sourceFullName;
    fieldIncludeText.LockFields = lockFields;
    fieldIncludeText.MimeType = mimeType;
    fieldIncludeText.TextConverter = textConverter;
    fieldIncludeText.Encoding = encoding;

    return fieldIncludeText;
}
```

### Ayrıca bakınız

* class [FieldIncludeText](../)
* ad alanı [Aspose.Words.Fields](../../../aspose.words.fields/)
* toplantı [Aspose.Words](../../../)
