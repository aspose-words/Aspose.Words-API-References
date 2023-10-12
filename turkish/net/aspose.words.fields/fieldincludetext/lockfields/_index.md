---
title: FieldIncludeText.LockFields
second_title: Aspose.Words for .NET API Referansı
description: FieldIncludeText mülk. Dahil edilen belgedeki alanların güncellenmesinin engellenip engellenmeyeceğini alır veya ayarlar.
type: docs
weight: 40
url: /tr/net/aspose.words.fields/fieldincludetext/lockfields/
---
## FieldIncludeText.LockFields property

Dahil edilen belgedeki alanların güncellenmesinin engellenip engellenmeyeceğini alır veya ayarlar.

```csharp
public bool LockFields { get; set; }
```

### Örnekler

INCLUDETEXT alanının nasıl oluşturulacağını ve özelliklerinin nasıl ayarlanacağını gösterir.

```csharp
public void FieldIncludeText()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Aşağıda yerel dosya sistemindeki bir XML dosyasının içeriğini görüntülemek için INCLUDETEXT alanlarını kullanmanın iki yolu verilmiştir.
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
* ad alanı [Aspose.Words.Fields](../../fieldincludetext/)
* toplantı [Aspose.Words](../../../)


