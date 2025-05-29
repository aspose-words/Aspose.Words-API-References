---
title: FootnoteOptions.Columns
linktitle: Columns
articleTitle: Columns
second_title: .NET için Aspose.Words
description: Gelişmiş okunabilirlik ve sunum için özelleştirilebilir sütun düzenleriyle dipnotlarınızı kolayca biçimlendirmek amacıyla FootnoteOptions Sütunlar özelliğini keşfedin.
type: docs
weight: 10
url: /tr/net/aspose.words.notes/footnoteoptions/columns/
---
## FootnoteOptions.Columns property

Dipnot alanının biçimlendirileceği sütun sayısını belirtir.

```csharp
public int Columns { get; set; }
```

## Notlar

Bu özelliğin değeri 0 ise, dipnot alanı görüntülenen sayfadaki sütun sayısına göre sütun sayısıyla biçimlendirilir. Varsayılan değer 0'dır.

## Örnekler

Dipnot bölümünün belirli sayıda sütuna nasıl bölüneceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Footnotes and endnotes.docx");
doc.FootnoteOptions.Columns = 2;
doc.Save(ArtifactsDir + "Document.FootnoteColumns.docx");
```

### Ayrıca bakınız

* class [FootnoteOptions](../)
* ad alanı [Aspose.Words.Notes](../../../aspose.words.notes/)
* toplantı [Aspose.Words](../../../)
