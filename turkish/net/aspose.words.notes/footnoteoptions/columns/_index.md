---
title: FootnoteOptions.Columns
second_title: Aspose.Words for .NET API Referansı
description: FootnoteOptions mülk. Dipnot alanının formatlanacağı sütun sayısını belirtir.
type: docs
weight: 10
url: /tr/net/aspose.words.notes/footnoteoptions/columns/
---
## FootnoteOptions.Columns property

Dipnot alanının formatlanacağı sütun sayısını belirtir.

```csharp
public int Columns { get; set; }
```

### Notlar

Bu özelliğin değeri 0 ise dipnot alanı, görüntülenen sayfadaki sütun sayısına bağlı olarak bir dizi sütunla biçimlendirilir. Varsayılan değer 0. 'dir

### Örnekler

Dipnot bölümünün belirli sayıda sütuna nasıl bölüneceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Footnotes and endnotes.docx");
doc.FootnoteOptions.Columns = 2;
doc.Save(ArtifactsDir + "Document.FootnoteColumns.docx");
```

### Ayrıca bakınız

* class [FootnoteOptions](../)
* ad alanı [Aspose.Words.Notes](../../footnoteoptions/)
* toplantı [Aspose.Words](../../../)


