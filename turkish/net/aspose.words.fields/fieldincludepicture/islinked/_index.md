---
title: FieldIncludePicture.IsLinked
linktitle: IsLinked
articleTitle: IsLinked
second_title: .NET için Aspose.Words
description: Belgelerinizi FieldIncludePicture IsLinked özelliğiyle optimize edin; dosya boyutunu küçültmek ve performansı artırmak için grafik depolama alanını kontrol edin.
type: docs
weight: 30
url: /tr/net/aspose.words.fields/fieldincludepicture/islinked/
---
## FieldIncludePicture.IsLinked property

Grafik verilerinin belgeyle birlikte depolanmaması yoluyla dosya boyutunun azaltılıp azaltılmayacağını alır veya ayarlar.

```csharp
public bool IsLinked { get; set; }
```

## Örnekler

IMPORT ve INCLUDEPICTURE alanlarını kullanarak resim eklemenin nasıl yapılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Aşağıda yerel dosya sisteminden bağlantılı görselleri görüntülemek için kullanabileceğimiz iki benzer alan türü bulunmaktadır.
// 1 - INCLUDEPICTURE alanı:
FieldIncludePicture fieldIncludePicture = (FieldIncludePicture)builder.InsertField(FieldType.FieldIncludePicture, true);
fieldIncludePicture.SourceFullName = ImageDir + "Transparent background logo.png";

Assert.True(Regex.Match(fieldIncludePicture.GetFieldCode(), " INCLUDEPICTURE  .*").Success);

// PNG32.FLT filtresini uygulayın.
fieldIncludePicture.GraphicFilter = "PNG32";
fieldIncludePicture.IsLinked = true;
fieldIncludePicture.ResizeHorizontally = true;
fieldIncludePicture.ResizeVertically = true;

// 2 - IMPORT alanı:
FieldImport fieldImport = (FieldImport)builder.InsertField(FieldType.FieldImport, true);
fieldImport.SourceFullName = ImageDir + "Transparent background logo.png";
fieldImport.GraphicFilter = "PNG32";
fieldImport.IsLinked = true;

Assert.True(Regex.Match(fieldImport.GetFieldCode(), " IMPORT  .* \\\\c PNG32 \\\\d").Success);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.IMPORT.INCLUDEPICTURE.docx");
```

### Ayrıca bakınız

* class [FieldIncludePicture](../)
* ad alanı [Aspose.Words.Fields](../../../aspose.words.fields/)
* toplantı [Aspose.Words](../../../)
