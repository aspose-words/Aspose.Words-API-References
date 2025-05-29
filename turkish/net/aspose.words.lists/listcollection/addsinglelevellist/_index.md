---
title: ListCollection.AddSingleLevelList
linktitle: AddSingleLevelList
articleTitle: AddSingleLevelList
second_title: .NET için Aspose.Words
description: ListCollection AddSingleLevelList yöntemi ile belgenize tek düzeyli bir listeyi zahmetsizce oluşturun ve ekleyin, böylece organizasyonu ve netliği artırın.
type: docs
weight: 60
url: /tr/net/aspose.words.lists/listcollection/addsinglelevellist/
---
## ListCollection.AddSingleLevelList method

Önceden tanımlanmış şablona dayalı yeni bir tek düzeyli liste oluşturur ve bunu belgedeki liste koleksiyonuna ekler.

```csharp
public List AddSingleLevelList(ListTemplate listTemplate)
```

## Örnekler

Önceden tanımlanmış şablona dayalı yeni bir tek düzeyli listenin nasıl oluşturulacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
ListCollection listCollection = doc.Lists;

// BulletCircle şablonundan madde işaretli liste oluşturur.
List bulletedList = listCollection.AddSingleLevelList(ListTemplate.BulletCircle);

// Madde işaretli listeyi sonuç belgeye yazar.
builder.Writeln("Bulleted list starts below:");
builder.ListFormat.List = bulletedList;
builder.Writeln("Item 1");
builder.Writeln("Item 2");
builder.ListFormat.RemoveNumbers();

// NumberUppercaseLetterDot şablonundan numaralı listeyi oluşturur.
List numberedList = listCollection.AddSingleLevelList(ListTemplate.NumberUppercaseLetterDot);

// Numaralandırılmış listeyi sonuç belgeye yazar.
builder.Writeln("Numbered list starts below:");
builder.ListFormat.List = numberedList;
builder.Writeln("Item 1");
builder.Writeln("Item 2");

doc.Save(ArtifactsDir + "Lists.AddSingleLevelList.docx");
```

### Ayrıca bakınız

* class [List](../../list/)
* enum [ListTemplate](../../listtemplate/)
* class [ListCollection](../)
* ad alanı [Aspose.Words.Lists](../../../aspose.words.lists/)
* toplantı [Aspose.Words](../../../)
