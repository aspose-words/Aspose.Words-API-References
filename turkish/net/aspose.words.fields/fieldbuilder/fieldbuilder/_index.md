---
title: FieldBuilder
linktitle: FieldBuilder
articleTitle: FieldBuilder
second_title: .NET için Aspose.Words
description: Projelerinizdeki alanları zahmetsizce oluşturmak ve yönetmek için güçlü araç olan FieldBuilder'ı keşfedin. İş akışınızı bugün kolaylaştırın!
type: docs
weight: 10
url: /tr/net/aspose.words.fields/fieldbuilder/fieldbuilder/
---
## FieldBuilder constructor

Bir örneğini başlatır[`FieldBuilder`](../) sınıf.

```csharp
public FieldBuilder(FieldType fieldType)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| fieldType | FieldType | İnşa edilecek alanın türü. |

## Örnekler

Alan oluşturucuyu kullanarak bir alanın nasıl oluşturulacağını ve ekleneceğini gösterir.

```csharp
Document doc = new Document();

// Bir belgeye metin içeriği eklemenin kolay bir yolu belge oluşturucuyu kullanmaktır.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write(" Hello world! This text is one Run, which is an inline node.");

// Alanların, alan kodunu parça parça oluşturmak için kullanabileceğimiz kendi oluşturucuları vardır.
// Bu durumda, ABD posta kodunu temsil eden bir BARKOD alanı oluşturacağız.
// ve sonra bunu bir Çalıştır'ın önüne ekleyin.
FieldBuilder fieldBuilder = new FieldBuilder(FieldType.FieldBarcode);
fieldBuilder.AddArgument("90210");
fieldBuilder.AddSwitch("\\f", "A");
fieldBuilder.AddSwitch("\\u");

fieldBuilder.BuildAndInsert(doc.FirstSection.Body.FirstParagraph.Runs[0]);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.CreateWithFieldBuilder.docx");
```

### Ayrıca bakınız

* enum [FieldType](../../fieldtype/)
* class [FieldBuilder](../)
* ad alanı [Aspose.Words.Fields](../../../aspose.words.fields/)
* toplantı [Aspose.Words](../../../)
