---
title: StyleCollection.DefaultParagraphFormat
linktitle: DefaultParagraphFormat
articleTitle: DefaultParagraphFormat
second_title: .NET için Aspose.Words
description: Belgenizin varsayılan paragraf biçimlendirmesine kolayca erişmek ve onu özelleştirmek için StyleCollection DefaultParagraphFormat özelliğini keşfedin ve okunabilirliği artırın.
type: docs
weight: 30
url: /tr/net/aspose.words/stylecollection/defaultparagraphformat/
---
## StyleCollection.DefaultParagraphFormat property

Belgenin varsayılan paragraf biçimlendirmesini alır.

```csharp
public ParagraphFormat DefaultParagraphFormat { get; }
```

## Notlar

Belge genelindeki varsayılanların Microsoft Word 2007'de tanıtıldığını ve OOXML biçimlerinde tam olarak desteklendiğini unutmayın (Docx) yalnızca. Daha önceki belge biçimleri, belgenin varsayılan paragraf biçimlendirmesini desteklemez.

## Örnekler

Bir belgenin stiller koleksiyonuna Stil eklemenin nasıl yapılacağını gösterir.

```csharp
Document doc = new Document();

StyleCollection styles = doc.Styles;
// Daha sonra bu koleksiyona ekleyebileceğimiz yeni stiller için varsayılan parametreleri ayarlayın.
styles.DefaultFont.Name = "Courier New";
// "StyleType.Paragraph" stilini eklersek, koleksiyon şu değerleri uygulayacaktır:
// "DefaultParagraphFormat" özelliğini stilin "ParagraphFormat" özelliğine.
styles.DefaultParagraphFormat.FirstLineIndent = 15.0;
// Bir stil ekleyin ve ardından varsayılan ayarlara sahip olduğunu doğrulayın.
styles.Add(StyleType.Paragraph, "MyStyle");

Assert.AreEqual("Courier New", styles[4].Font.Name);
Assert.AreEqual(15.0, styles["MyStyle"].ParagraphFormat.FirstLineIndent);
```

### Ayrıca bakınız

* class [ParagraphFormat](../../paragraphformat/)
* class [StyleCollection](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
