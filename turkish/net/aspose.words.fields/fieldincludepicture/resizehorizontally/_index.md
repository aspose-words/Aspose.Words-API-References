---
title: FieldIncludePicture.ResizeHorizontally
linktitle: ResizeHorizontally
articleTitle: ResizeHorizontally
second_title: Aspose.Words for .NET
description: FieldIncludePicture ResizeHorizontally mülk. Resmin kaynaktan yatay olarak yeniden boyutlandırılıp yeniden boyutlandırılmayacağını alır veya ayarlar C#'da.
type: docs
weight: 40
url: /tr/net/aspose.words.fields/fieldincludepicture/resizehorizontally/
---
## FieldIncludePicture.ResizeHorizontally property

Resmin kaynaktan yatay olarak yeniden boyutlandırılıp yeniden boyutlandırılmayacağını alır veya ayarlar.

```csharp
public bool ResizeHorizontally { get; set; }
```

## Örnekler

IMPORT ve INCLUDEPICTURE alanlarını kullanarak görüntülerin nasıl ekleneceğini gösterir.

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

// 2 - İTHALAT alanı:
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
