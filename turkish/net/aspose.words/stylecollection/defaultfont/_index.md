---
title: StyleCollection.DefaultFont
linktitle: DefaultFont
articleTitle: DefaultFont
second_title: Aspose.Words for .NET
description: StyleCollection DefaultFont mülk. Belgenin varsayılan metin formatını alır C#'da.
type: docs
weight: 20
url: /tr/net/aspose.words/stylecollection/defaultfont/
---
## StyleCollection.DefaultFont property

Belgenin varsayılan metin formatını alır.

```csharp
public Font DefaultFont { get; }
```

## Notlar

Belge genelindeki varsayılanların Microsoft Word 2007'de sunulduğunu ve OOXML formatlarında tam olarak desteklendiğini unutmayın (Docx) yalnızca. Önceki belge biçimlerinin bu özellik için sınırlı desteği vardır ve yalnızca yazı tipi adları saklanabilir.

## Örnekler

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

* class [Font](../../font/)
* class [StyleCollection](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
