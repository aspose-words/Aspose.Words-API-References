---
title: Document.ShadeFormData
linktitle: ShadeFormData
articleTitle: ShadeFormData
second_title: .NET için Aspose.Words
description: Gri gölgelendirmeyle form görünürlüğünü artırmak, kullanıcı deneyimini ve erişilebilirliği iyileştirmek için ShadeFormData özelliğinin nasıl kullanılacağını keşfedin.
type: docs
weight: 400
url: /tr/net/aspose.words/document/shadeformdata/
---
## Document.ShadeFormData property

Form alanlarında gri gölgelendirmenin açılıp açılmayacağını belirtir.

```csharp
public bool ShadeFormData { get; set; }
```

## Örnekler

Form alanlarına gri gölgelendirmenin nasıl uygulanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Hello world! ");
builder.InsertTextInput("My form field", TextFormFieldType.Regular, "",
    "Text contents of form field, which are shaded in grey by default.", 0);

// Gri tonlamayı kapatabiliriz, böylece yer imlerine eklenen metin diğer metinlerle harmanlanır.
doc.ShadeFormData = useGreyShading;
doc.Save(ArtifactsDir + "Document.ShadeFormData.docx");
```

### Ayrıca bakınız

* class [Document](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
