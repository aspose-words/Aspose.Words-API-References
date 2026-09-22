---
title: "Aspose::Words::Layout::LayoutEnumerator sınıfı"
linktitle: "LayoutEnumerator"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Layout::LayoutEnumerator sınıfı. Bir belgenin sayfa düzeni varlıklarını listeler. Bu sınıfı sayfa düzeni modelinde dolaşmak için kullanabilirsiniz. Mevcut özellikler, varlığın işlendiği tip, geometri, metin ve sayfa indeksi ile birlikte genel yapı ve ilişkileri içerir. GetEntity() ve Current kombinasyonunu kullanarak belge düğümüne karşılık gelen varlığa geçin. Daha fazla bilgi için C++'daki dokümantasyon makalesini ziyaret edin."
type: docs
weight: 2000
url: /tr/cpp/aspose.words.layout/layoutenumerator/
---
## LayoutEnumerator class


Bir belgenin sayfa düzeni varlıklarını listeler. Bu sınıfı sayfa düzeni modelinde dolaşmak için kullanabilirsiniz. Mevcut özellikler, varlığın işlendiği tip, geometri, metin ve sayfa indeksi ile birlikte genel yapı ve ilişkileri içerir. [GetEntity()](../) ve [Current](./get_current/) kombinasyonunu kullanarak belge düğümüne karşılık gelen varlığa geçin. Daha fazla bilgi için [Converting to Fixed-page Format](https://docs.aspose.com/words/cpp/converting-to-fixed-page-format/) dokümantasyon makalesini ziyaret edin.

```cpp
class LayoutEnumerator : public System::Object,
                         public System::Details::EnumeratorBasedIterator<System::SharedPtr<System::Object>>,
                         private System::Details::IteratorPointerUpdater<System::SharedPtr<System::Object>, false>
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [CloneIterator](./cloneiterator/)() const override |  |
| [get_Current](./get_current/)() const | Sayfa düzeni modelindeki mevcut konumu alır veya ayarlar. Bu özellik, mevcut düzen varlığına karşılık gelen opak bir nesne döndürür. |
| [get_Document](./get_document/)() const | Bu örneğin listelediği belgeyi alır. |
| [get_Kind](./get_kind/)() | Geçerli varlığın türünü alır. Bu boş bir dize olabilir ancak asla **null** olmaz. |
| [get_PageIndex](./get_pageindex/)() | Geçerli varlığı içeren sayfanın 1 tabanlı indeksini alır. |
| [get_Rectangle](./get_rectangle/)() | Geçerli varlığın sayfanın sol üst köşesine (puan cinsinden) göre sınırlayıcı dikdörtgenini döndürür. |
| [get_Text](./get_text/)() | Geçerli span varlığının metnini alır. Diğer varlık türleri için istisna fırlatır. |
| [get_Type](./get_type/)() | Geçerli varlığın tipini alır. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(const System::String\&) | Varlığın adlandırılmış bir özelliğini alır. |
| [IncrementIterator](./incrementiterator/)() override |  |
| [InitializeIterator](./initializeiterator/)() override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [LayoutEnumerator](./layoutenumerator/)(const System::SharedPtr\<Aspose::Words::Document\>\&) | Bu sınıfın yeni bir örneğini başlatır. |
| [MoveFirstChild](./movefirstchild/)() | İlk alt varlığa geçer. |
| [MoveLastChild](./movelastchild/)() | Son alt varlığa geçer. |
| [MoveNext](./movenext/)() | Görsel sırada bir sonraki kardeş varlığa geçer. Sayfalar arasında bölünmüş bir paragrafın satırlarını yinelediğinde bu yöntem bir sonraki sayfaya geçmez, aynı sayfadaki bir sonraki varlığa geçer. |
| [MoveNextLogical](./movenextlogical/)() | Mantıksal sırada bir sonraki kardeş varlığa geçer. Sayfalar arasında bölünmüş bir paragrafın satırlarını yinelediğinde bu yöntem, satır başka bir sayfada olsa bile bir sonraki satıra geçer. |
| [MoveParent](./moveparent/)() | Üst varlığa geçer. |
| [MoveParent](./moveparent/)(Aspose::Words::Layout::LayoutEntityType) | Belirtilen tipteki üst varlığa geçer. |
| [MovePrevious](./moveprevious/)() | Önceki kardeş varlığa geçer. |
| [MovePreviousLogical](./movepreviouslogical/)() | Mantıksal sırada önceki kardeş varlığa geçer. Sayfalar arasında bölünmüş bir paragrafın satırlarını yinelediğinde bu yöntem, satır başka bir sayfada olsa bile önceki satıra geçer. |
| [Reset](./reset/)() | Enumeratörü belgenin ilk sayfasına taşır. |
| [set_Current](./set_current/)(const System::SharedPtr\<System::Object\>\&) | Ayarlayıcı [Aspose::Words::Layout::LayoutEnumerator::get_Current](./get_current/). |
| static [Type](./type/)() |  |
## Ayrıca Bakınız

* Namespace [Aspose::Words::Layout](../)
* Library [Aspose.Words for C++](../../)
