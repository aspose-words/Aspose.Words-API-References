---
title: LoadOptions.PreserveIncludePictureField
second_title: Aspose.Words for .NET API Referansı
description: LoadOptions mülk. Microsoft Word formatlarını okurken INCLUDEPICTURE alanının korunup korunmayacağını alır veya ayarlar. Varsayılan değerYANLIŞ .
type: docs
weight: 120
url: /tr/net/aspose.words.loading/loadoptions/preserveincludepicturefield/
---
## LoadOptions.PreserveIncludePictureField property

Microsoft Word formatlarını okurken INCLUDEPICTURE alanının korunup korunmayacağını alır veya ayarlar. Varsayılan değer:`YANLIŞ` .

```csharp
public bool PreserveIncludePictureField { get; set; }
```

### Notlar

Varsayılan olarak INCLUDEPICTURE alanı bir şekil nesnesine dönüştürülür. Korunacak alana ihtiyacınız varsa, örneğin alanı programlı olarak güncellemek istiyorsanız bunu geçersiz kılabilirsiniz. Ancak this yaklaşımının Aspose.Words için yaygın olmadığını unutmayın. Riski size ait olmak üzere kullanın.

Olası kullanım durumlarından biri, resmin kaynak path yolunu dinamik olarak değiştirmek için MERGEFIELD'ı alt alan olarak kullanmak olabilir. Bu durumda modelde korunacak INCLUDEPICTURE'a ihtiyacınız var.

### Örnekler

Bir belge yüklenirken INCLUDEPICTURE alanlarının nasıl korunacağını veya atılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

FieldIncludePicture includePicture = (FieldIncludePicture)builder.InsertField(FieldType.FieldIncludePicture, true);
includePicture.SourceFullName = ImageDir + "Transparent background logo.png";
includePicture.Update(true);

using (MemoryStream docStream = new MemoryStream())
{
    doc.Save(docStream, new OoxmlSaveOptions(SaveFormat.Docx));

    // Tüm INCLUDEPICTURE alanlarının dönüştürülüp dönüştürülmeyeceğine karar vermek için LoadOptions nesnesine bir bayrak ayarlayabiliriz
    // bunları içeren bir belge yüklenirken görüntü şekillerine.
    LoadOptions loadOptions = new LoadOptions
    {
        PreserveIncludePictureField = preserveIncludePictureField
    };

    doc = new Document(docStream, loadOptions);

    if (preserveIncludePictureField)
    {
        Assert.True(doc.Range.Fields.Any(f => f.Type == FieldType.FieldIncludePicture));

        doc.UpdateFields();
        doc.Save(ArtifactsDir + "Field.PreserveIncludePicture.docx");
    }
    else
    {
        Assert.False(doc.Range.Fields.Any(f => f.Type == FieldType.FieldIncludePicture));
    }
}
```

### Ayrıca bakınız

* class [LoadOptions](../)
* ad alanı [Aspose.Words.Loading](../../loadoptions/)
* toplantı [Aspose.Words](../../../)


