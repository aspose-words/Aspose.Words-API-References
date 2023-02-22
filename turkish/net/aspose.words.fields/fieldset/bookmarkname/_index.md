---
title: FieldSet.BookmarkName
second_title: Aspose.Words for .NET API Referansı
description: FieldSet mülk. Yer iminin adını alır veya ayarlar.
type: docs
weight: 20
url: /tr/net/aspose.words.fields/fieldset/bookmarkname/
---
## FieldSet.BookmarkName property

Yer iminin adını alır veya ayarlar.

```csharp
public string BookmarkName { get; set; }
```

### Örnekler

SET alanıyla işaretlenmiş metnin nasıl oluşturulacağını ve ardından bir REF alanı kullanarak belgede nasıl görüntüleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

 // İşaretlenmiş metni bir SET alanıyla adlandırın.
// Bu alan, metin içinde görünen bir yer imi yapısına değil, adlandırılmış bir değişkene "yer imi" anlamına gelir.
FieldSet fieldSet = (FieldSet)builder.InsertField(FieldType.FieldSet, false);
fieldSet.BookmarkName = "MyBookmark";
fieldSet.BookmarkText = "Hello world!";
fieldSet.Update();

Assert.AreEqual(" SET  MyBookmark \"Hello world!\"", fieldSet.GetFieldCode());

// Bir REF alanında yer imine ada göre bakın ve içeriğini görüntüleyin.
FieldRef fieldRef = (FieldRef)builder.InsertField(FieldType.FieldRef, true);
fieldRef.BookmarkName = "MyBookmark";
fieldRef.Update();

Assert.AreEqual(" REF  MyBookmark", fieldRef.GetFieldCode());
Assert.AreEqual("Hello world!", fieldRef.Result);

doc.Save(ArtifactsDir + "Field.SET.REF.docx");
```

### Ayrıca bakınız

* class [FieldSet](../)
* ad alanı [Aspose.Words.Fields](../../fieldset/)
* toplantı [Aspose.Words](../../../)


