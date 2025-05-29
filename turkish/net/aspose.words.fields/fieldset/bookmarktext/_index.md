---
title: FieldSet.BookmarkText
linktitle: BookmarkText
articleTitle: BookmarkText
second_title: .NET için Aspose.Words
description: Yer imlerinizi daha iyi düzenleme ve erişilebilirlik için özelleştirmek ve geliştirmek amacıyla FieldSet BookmarkText özelliğini nasıl kolayca yöneteceğinizi keşfedin.
type: docs
weight: 30
url: /tr/net/aspose.words.fields/fieldset/bookmarktext/
---
## FieldSet.BookmarkText property

Yer iminin yeni metnini alır veya ayarlar.

```csharp
public string BookmarkText { get; set; }
```

## Örnekler

SET alanıyla yer imli metnin nasıl oluşturulacağını ve ardından REF alanı kullanılarak belgede nasıl görüntüleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

 // SET alanı ile yer imli metni adlandırın.
// Bu alan, metin içerisinde görünen bir yer imi yapısına değil, adlandırılmış bir değişkene atıfta bulunur.
FieldSet fieldSet = (FieldSet)builder.InsertField(FieldType.FieldSet, false);
fieldSet.BookmarkName = "MyBookmark";
fieldSet.BookmarkText = "Hello world!";
fieldSet.Update();

Assert.AreEqual(" SET  MyBookmark \"Hello world!\"", fieldSet.GetFieldCode());

// REF alanında yer imine adıyla başvur ve içeriğini görüntüle.
FieldRef fieldRef = (FieldRef)builder.InsertField(FieldType.FieldRef, true);
fieldRef.BookmarkName = "MyBookmark";
fieldRef.Update();

Assert.AreEqual(" REF  MyBookmark", fieldRef.GetFieldCode());
Assert.AreEqual("Hello world!", fieldRef.Result);

doc.Save(ArtifactsDir + "Field.SET.REF.docx");
```

### Ayrıca bakınız

* class [FieldSet](../)
* ad alanı [Aspose.Words.Fields](../../../aspose.words.fields/)
* toplantı [Aspose.Words](../../../)
