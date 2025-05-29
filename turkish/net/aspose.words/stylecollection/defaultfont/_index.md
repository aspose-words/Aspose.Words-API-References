---
title: StyleCollection.DefaultFont
linktitle: DefaultFont
articleTitle: DefaultFont
second_title: .NET için Aspose.Words
description: Kusursuz belge metin biçimlendirmesi için StyleCollection DefaultFont özelliğini keşfedin. Belgelerinizi tutarlı, profesyonel bir stille geliştirin.
type: docs
weight: 20
url: /tr/net/aspose.words/stylecollection/defaultfont/
---
## StyleCollection.DefaultFont property

Belgenin varsayılan metin biçimlendirmesini alır.

```csharp
public Font DefaultFont { get; }
```

## Notlar

Belge genelindeki varsayılanların Microsoft Word 2007'de tanıtıldığını ve OOXML biçimlerinde tam olarak desteklendiğini unutmayın (Docx) yalnızca. Daha önceki belge biçimleri bu özellik için sınırlı desteğe sahipti ve yalnızca yazı tipi adları saklanabilirdi.

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

* class [Font](../../font/)
* class [StyleCollection](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
