---
title: FieldChar Class
linktitle: FieldChar
articleTitle: FieldChar
second_title: .NET için Aspose.Words
description: Belge alanı karakterleri için temel bir temel olan Aspose.Words.Fields.FieldChar sınıfını keşfedin, belge işleme ve özelleştirmenizi geliştirin.
type: docs
weight: 2080
url: /tr/net/aspose.words.fields/fieldchar/
---
## FieldChar class

Bir belgedeki alan karakterlerini temsil eden düğümler için temel sınıf.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Alanlarla Çalışma](https://docs.aspose.com/words/net/working-with-fields/) belgeleme makalesi.

```csharp
public abstract class FieldChar : SpecialChar
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Özel düğüm tanımlayıcısını belirtir. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Bu düğümün ait olduğu belgeyi alır. |
| [FieldType](../../aspose.words.fields/fieldchar/fieldtype/) { get; } | Alanın türünü döndürür. |
| [Font](../../aspose.words/inline/font/) { get; } | Bu nesnenin yazı tipi biçimlendirmesine erişim sağlar. |
| virtual [IsComposite](../../aspose.words/node/iscomposite/) { get; } | Geri Döndürür`doğru` eğer bu düğüm diğer düğümleri içerebiliyorsa. |
| [IsDeleteRevision](../../aspose.words/inline/isdeleterevision/) { get; } | Değişiklik izleme etkinleştirilmişken bu nesnenin Microsoft Word'de silinmesi durumunda doğru değerini döndürür. |
| [IsDirty](../../aspose.words.fields/fieldchar/isdirty/) { get; set; } | Belgede yapılan diğer değişiklikler nedeniyle alanın geçerli sonucunun artık doğru (eski) olup olmadığını alır veya ayarlar. |
| [IsFormatRevision](../../aspose.words/inline/isformatrevision/) { get; } | Değişiklik izleme etkinleştirilmişken Microsoft Word'de nesnenin biçimlendirmesinin değiştirilmesi durumunda doğru değerini döndürür. |
| [IsInsertRevision](../../aspose.words/inline/isinsertrevision/) { get; } | Bu nesnenin Microsoft Word'e değişiklik izleme etkinleştirilmişken eklenip eklenmediğini döndürür. |
| [IsLocked](../../aspose.words.fields/fieldchar/islocked/) { get; set; } | Üst alanın kilitli olup olmadığını alır veya ayarlar (sonucunu yeniden hesaplamamalıdır). |
| [IsMoveFromRevision](../../aspose.words/inline/ismovefromrevision/) { get; } | Geri Döndürür`doğru` bu nesne Microsoft Word'de değişiklik izleme etkinleştirilmişken taşınırsa (silinirse). |
| [IsMoveToRevision](../../aspose.words/inline/ismovetorevision/) { get; } | Geri Döndürür`doğru` bu nesne Microsoft Word'de değişiklik izleme etkinleştirilmişken taşınırsa (eklenirse). |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Bu düğümü hemen takip eden düğümü alır. |
| override [NodeType](../../aspose.words/specialchar/nodetype/) { get; } | Geri DöndürürSpecialChar . |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Bu düğümün en yakın üst düğümünü alır. |
| [ParentParagraph](../../aspose.words/inline/parentparagraph/) { get; } | Üst öğeyi alır[`Paragraph`](../../aspose.words/paragraph/) bu düğümün. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Bu düğümden hemen önceki düğümü alır. |
| [Range](../../aspose.words/node/range/) { get; } | Bir[`Range`](../../aspose.words/range/)bu düğümde bulunan bir belgenin bölümünü temsil eden nesne. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| override [Accept](../../aspose.words/specialchar/accept/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | Bir ziyaretçiyi kabul eder. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | Düğümün bir kopyasını oluşturur. |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../../aspose.words/nodetype/)*) | Belirtilenin ilk atasını alır[`NodeType`](../../aspose.words/nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | Belirtilen nesne türünün ilk atasını alır. |
| [GetField](../../aspose.words.fields/fieldchar/getfield/)() | char. alanı için bir alan döndürür |
| override [GetText](../../aspose.words/specialchar/gettext/)() | Bu düğümün temsil ettiği özel karakteri alır. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../../aspose.words/node/)*) | Ön sipariş ağacı geçiş algoritmasına göre bir sonraki düğümü alır. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../../aspose.words/node/)*) | Ön sipariş ağacı geçiş algoritmasına göre önceki düğümü alır. |
| [Remove](../../aspose.words/node/remove/)() | Kendini ana öğeden kaldırır. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../../aspose.words/saveformat/)*) | Düğümün içeriğini belirtilen biçimde bir dizeye aktarır. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | Belirtilen kaydetme seçeneklerini kullanarak düğümün içeriğini bir dizeye aktarır. |

## Notlar

Microsoft Word belgesindeki tam bir alan, bir alan başlangıç karakteri, alan kodu, alan ayırıcı karakteri, alan sonucu ve alan bitiş karakterinden oluşan karmaşık bir yapıdır. Bazı alanlarda yalnızca alan başlangıcı, alan kodu ve alan bitişi bulunur.

Bir belgeye kolayca yeni bir alan eklemek için şunu kullanın:[`InsertField`](../../aspose.words/documentbuilder/insertfield/) yöntemi.

## Örnekler

FieldStart düğümüyle nasıl çalışılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

FieldDate field = (FieldDate)builder.InsertField(FieldType.FieldDate, true);
field.Format.DateTimeFormat = "dddd, MMMM dd, yyyy";
field.Update();

FieldChar fieldStart = field.Start;

Assert.AreEqual(FieldType.FieldDate, fieldStart.FieldType);
Assert.AreEqual(false, fieldStart.IsDirty);
Assert.AreEqual(false, fieldStart.IsLocked);

// Belgedeki alanı temsil eden cephe nesnesini al.
field = (FieldDate)fieldStart.GetField();

Assert.AreEqual(false, field.IsLocked);
Assert.AreEqual(" DATE  \\@ \"dddd, MMMM dd, yyyy\"", field.GetFieldCode());

// Alanı güncel tarihi gösterecek şekilde güncelleyin.
field.Update();
```

### Ayrıca bakınız

* class [FieldStart](../fieldstart/)
* class [FieldSeparator](../fieldseparator/)
* class [FieldEnd](../fieldend/)
* class [SpecialChar](../../aspose.words/specialchar/)
* ad alanı [Aspose.Words.Fields](../../aspose.words.fields/)
* toplantı [Aspose.Words](../../)
