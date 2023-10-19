---
title: PageSetup.Bidi
linktitle: Bidi
articleTitle: Bidi
second_title: Aspose.Words for .NET
description: PageSetup Bidi mülk. Bu bölümün çift yönlü karmaşık komut dosyaları metin içerdiğini belirtir C#'da.
type: docs
weight: 10
url: /tr/net/aspose.words/pagesetup/bidi/
---
## PageSetup.Bidi property

Bu bölümün çift yönlü (karmaşık komut dosyaları) metin içerdiğini belirtir.

```csharp
public bool Bidi { get; set; }
```

## Notlar

Ne zaman`doğru`bu bölümdeki sütunlar sağdan sola doğru düzenlenmiştir.

## Örnekler

Bir bölümdeki metin sütunlarının sırasının nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();

PageSetup pageSetup = doc.Sections[0].PageSetup;
pageSetup.TextColumns.SetCount(3);

DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Column 1.");
builder.InsertBreak(BreakType.ColumnBreak);
builder.Write("Column 2.");
builder.InsertBreak(BreakType.ColumnBreak);
builder.Write("Column 3.");

// Sütunların sayfanın sağ tarafından başlayarak düzenlenmesi için "Bidi" özelliğini "true" olarak ayarlayın.
// Sütunların sırası sağdan sola metnin yönüyle eşleşecektir.
// Sütunların sayfanın sol tarafından düzenlenmesi için "Bidi" özelliğini "false" olarak ayarlayın.
// Sütunların sırası soldan sağa metnin yönüyle eşleşecektir.
pageSetup.Bidi = reverseColumns;

doc.Save(ArtifactsDir + "PageSetup.Bidi.docx");
```

### Ayrıca bakınız

* class [PageSetup](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
