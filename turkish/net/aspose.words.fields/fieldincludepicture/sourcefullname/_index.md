---
title: FieldIncludePicture.SourceFullName
linktitle: SourceFullName
articleTitle: SourceFullName
second_title: .NET için Aspose.Words
description: FieldIncludePicture SourceFullName özelliğini keşfedin. Gelişmiş medya entegrasyonu ve sorunsuz kullanıcı deneyimi için resim konumlarını IRI ile kolayca yönetin.
type: docs
weight: 60
url: /tr/net/aspose.words.fields/fieldincludepicture/sourcefullname/
---
## FieldIncludePicture.SourceFullName property

IRI kullanarak resmin konumunu alır veya ayarlar.

```csharp
public string SourceFullName { get; set; }
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
