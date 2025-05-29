---
title: PageSetup.Bidi
linktitle: Bidi
articleTitle: Bidi
second_title: .NET için Aspose.Words
description: Sorunsuz çift yönlü metin biçimlendirme için PageSetup Bidi özelliğini keşfedin. Daha iyi okunabilirlik için karmaşık betik desteğiyle belgelerinizi geliştirin!
type: docs
weight: 10
url: /tr/net/aspose.words/pagesetup/bidi/
---
## PageSetup.Bidi property

Bu bölümün çift yönlü (karmaşık betikler) metin içerdiğini belirtir.

```csharp
public bool Bidi { get; set; }
```

## Notlar

Ne zaman`doğru`Bu bölümdeki sütunlar sağdan sola doğru düzenlenmiştir.

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

// Sütunları sayfanın sağ tarafından başlayarak düzenlemek için "Bidi" özelliğini "true" olarak ayarlayın.
// Sütunların sıralaması sağdan sola doğru yazılan metnin yönüne göre olacaktır.
// Sütunları sayfanın sol tarafından başlayarak düzenlemek için "Bidi" özelliğini "false" olarak ayarlayın.
// Sütunların sıralaması soldan sağa doğru yazılan metnin yönüne göre olacaktır.
pageSetup.Bidi = reverseColumns;

doc.Save(ArtifactsDir + "PageSetup.Bidi.docx");
```

### Ayrıca bakınız

* class [PageSetup](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
