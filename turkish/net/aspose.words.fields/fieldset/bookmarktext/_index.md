---
title: FieldSet.BookmarkText
linktitle: BookmarkText
articleTitle: BookmarkText
second_title: Aspose.Words for .NET
description: FieldSet BookmarkText mülk. Yer iminin yeni metnini alır veya ayarlar C#'da.
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

SET alanıyla yer imli metnin nasıl oluşturulacağını ve ardından REF alanını kullanarak belgede nasıl görüntüleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

 // Yer imlerine eklenen metni SET alanıyla adlandırın.
// Bu alan, metin içinde görünen bir yer imi yapısını değil, adlandırılmış bir değişkeni "yer işareti" anlamına gelir.
FieldSet fieldSet = (FieldSet)builder.InsertField(FieldType.FieldSet, false);
fieldSet.BookmarkName = "MyBookmark";
fieldSet.BookmarkText = "Hello world!";
fieldSet.Update();

Assert.AreEqual(" SET  MyBookmark \"Hello world!\"", fieldSet.GetFieldCode());

// Bir REF alanında yer imine isme göre bakın ve içeriğini görüntüleyin.
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
