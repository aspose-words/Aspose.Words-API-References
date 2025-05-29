---
title: LoadOptions.PreserveIncludePictureField
linktitle: PreserveIncludePictureField
articleTitle: PreserveIncludePictureField
second_title: .NET için Aspose.Words
description: Microsoft Word biçimlerinde INCLUDEPICTURE alanını LoadOptions PreserveIncludePictureField ile kontrol edin. En iyi sonuçlar için belge biçimlendirmesini kolayca yönetin.
type: docs
weight: 120
url: /tr/net/aspose.words.loading/loadoptions/preserveincludepicturefield/
---
## LoadOptions.PreserveIncludePictureField property

Microsoft Word biçimlerini okurken INCLUDEPICTURE alanının korunup korunmayacağını alır veya ayarlar. Varsayılan değer`YANLIŞ` .

```csharp
public bool PreserveIncludePictureField { get; set; }
```

## Notlar

Varsayılan olarak, INCLUDEPICTURE alanı bir şekil nesnesine dönüştürülür. Alanın korunmasını istiyorsanız, örneğin programatik olarak güncellemek istiyorsanız, bunu geçersiz kılabilirsiniz. Ancak, this yaklaşımının Aspose.Words için yaygın olmadığını unutmayın. Bunu kendi riskinizle kullanın.

Olası kullanım durumlarından biri, resmin kaynak path 'sini dinamik olarak değiştirmek için bir alt alan olarak MERGEFIELD kullanmak olabilir. Bu durumda INCLUDEPICTURE'ın modelde korunması gerekir.

## Örnekler

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

    // Tüm INCLUDEPICTURE alanlarını dönüştürüp dönüştürmemeye karar vermek için bir LoadOptions nesnesinde bir bayrak ayarlayabiliriz
    // bunları içeren bir belge yüklenirken görüntü şekillerine dönüşür.
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
* ad alanı [Aspose.Words.Loading](../../../aspose.words.loading/)
* toplantı [Aspose.Words](../../../)
