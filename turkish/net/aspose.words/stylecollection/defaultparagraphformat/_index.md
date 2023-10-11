---
title: StyleCollection.DefaultParagraphFormat
second_title: Aspose.Words for .NET API Referansı
description: StyleCollection mülk. Belgenin varsayılan paragraf formatını alır.
type: docs
weight: 30
url: /tr/net/aspose.words/stylecollection/defaultparagraphformat/
---
## StyleCollection.DefaultParagraphFormat property

Belgenin varsayılan paragraf formatını alır.

```csharp
public ParagraphFormat DefaultParagraphFormat { get; }
```

### Notlar

Belge genelindeki varsayılanların Microsoft Word 2007'de sunulduğunu ve OOXML formatlarında tam olarak desteklendiğini unutmayın (Docx) yalnızca. Önceki belge formatlarında, belgenin varsayılan paragraf formatı desteği yoktur.

### Örnekler

Bir belgenin stil koleksiyonuna nasıl Stil ekleneceğini gösterir.

```csharp
Document doc = new Document();

StyleCollection styles = doc.Styles;
// Daha sonra bu koleksiyona ekleyebileceğimiz yeni stiller için varsayılan parametreleri ayarlayın.
styles.DefaultFont.Name = "Courier New";
// "StyleType.Paragraph" stilini eklersek koleksiyon şu değerleri uygulayacaktır:
// "DefaultParagraphFormat" özelliğini stilin "ParagraphFormat" özelliğine dönüştürüyoruz.
styles.DefaultParagraphFormat.FirstLineIndent = 15.0;
// Bir stil ekleyin ve ardından bunun varsayılan ayarlara sahip olduğunu doğrulayın.
styles.Add(StyleType.Paragraph, "MyStyle");

Assert.AreEqual("Courier New", styles[4].Font.Name);
Assert.AreEqual(15.0, styles["MyStyle"].ParagraphFormat.FirstLineIndent);
```

### Ayrıca bakınız

* class [ParagraphFormat](../../paragraphformat/)
* class [StyleCollection](../)
* ad alanı [Aspose.Words](../../stylecollection/)
* toplantı [Aspose.Words](../../../)


