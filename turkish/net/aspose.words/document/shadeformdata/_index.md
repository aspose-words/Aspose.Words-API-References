---
title: Document.ShadeFormData
second_title: Aspose.Words for .NET API Referansı
description: Document mülk. Form alanlarında gri gölgelemenin açılıp açılmayacağını belirtir.
type: docs
weight: 380
url: /tr/net/aspose.words/document/shadeformdata/
---
## Document.ShadeFormData property

Form alanlarında gri gölgelemenin açılıp açılmayacağını belirtir.

```csharp
public bool ShadeFormData { get; set; }
```

### Örnekler

Form alanlarına gri gölgelemenin nasıl uygulanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Hello world! ");
builder.InsertTextInput("My form field", TextFormFieldType.Regular, "",
    "Text contents of form field, which are shaded in grey by default.", 0);

// Gri gölgelemeyi kapatabiliriz, böylece yer imlerine eklenen metin diğer metinle karışacaktır.
doc.ShadeFormData = useGreyShading;
doc.Save(ArtifactsDir + "Document.ShadeFormData.docx");
```

### Ayrıca bakınız

* class [Document](../)
* ad alanı [Aspose.Words](../../document/)
* toplantı [Aspose.Words](../../../)


