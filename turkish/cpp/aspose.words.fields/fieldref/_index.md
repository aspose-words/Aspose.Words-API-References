---
title: "Aspose::Words::Fields::FieldRef sınıfı"
linktitle: "FieldRef"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fields::FieldRef sınıfı. REF alanını uygular. Daha fazla bilgi için C++'daki belge makalesini ziyaret edin."
type: docs
weight: 85000
url: /tr/cpp/aspose.words.fields/fieldref/
---
## FieldRef class


REF alanını uygular. Daha fazla bilgi edinmek için [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/) dokümantasyon makalesini ziyaret edin.

```cpp
class FieldRef : public Aspose::Words::Fields::Field,
                 public Aspose::Words::Fields::IFieldCodeTokenInfoProvider,
                 public Aspose::Words::Fields::IMergeFieldSurrogate
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [get_BookmarkName](./get_bookmarkname/)() | Referans alınan yer işaretinin adını alır veya ayarlar. |
| [get_DisplayResult](../field/get_displayresult/)() | Görüntülenen alan sonucunu temsil eden metni alır. |
| [get_End](./get_end/)() override | Alan sonunu temsil eden düğümü alır. |
| [get_End](../field/get_end/)() const | Alan sonunu temsil eden düğümü alır. |
| [get_FieldEnd](../field/get_fieldend/)() const | Alan sonunu temsil eden düğümü alır. |
| [get_FieldStart](../field/get_fieldstart/)() const | Alan başlangıcını temsil eden düğümü alır. |
| [get_Format](../field/get_format/)() | Alan biçimlendirmesine tipli erişim sağlayan bir [FieldFormat](../fieldformat/) nesnesi alır. |
| [get_IncludeNoteOrComment](./get_includenoteorcomment/)() | Yer işaretiyle işaretlenen dipnot, sonnot ve ek açıklama numaralarının artırılıp artırılmayacağını alır ve ilgili dipnot, sonnot ve yorum metnini ekler. |
| [get_InsertHyperlink](./get_inserthyperlink/)() | Yer işaretli paragraf için bir köprü oluşturulup oluşturulmayacağını alır. |
| [get_InsertParagraphNumber](./get_insertparagraphnumber/)() | Referans alınan paragrafın paragraf numarasının belgede göründüğü şekilde tam olarak eklenip eklenmeyeceğini alır. |
| [get_InsertParagraphNumberInFullContext](./get_insertparagraphnumberinfullcontext/)() | Referans alınan paragrafın paragraf numarasının tam bağlamda eklenip eklenmeyeceğini alır. |
| [get_InsertParagraphNumberInRelativeContext](./get_insertparagraphnumberinrelativecontext/)() | Referans alınan paragrafın paragraf numarasının göreceli bağlamda eklenip eklenmeyeceğini alır. |
| [get_InsertRelativePosition](./get_insertrelativeposition/)() | Referans alınan paragrafın göreceli konumunun eklenip eklenmeyeceğini alır. |
| [get_IsDirty](../field/get_isdirty/)() | Alan'ın mevcut sonucunun, belgeye yapılan diğer değişiklikler nedeniyle artık doğru (eski) olup olmadığını alır veya ayarlar. |
| [get_IsLocked](../field/get_islocked/)() | Alan'ın kilitli olup olmadığını (sonucunu yeniden hesaplamamalı) alır veya ayarlar. |
| [get_LocaleId](../field/get_localeid/)() | Alan'ın LCID'sini alır veya ayarlar. |
| [get_NumberSeparator](./get_numberseparator/)() | Dizi numaralarını ve sayfa numaralarını ayırmak için kullanılan karakter dizisini alır. |
| [get_Result](../field/get_result/)() | Alan ayırıcı ile alan sonu arasındaki metni alır veya ayarlar. |
| [get_Separator](./get_separator/)() override | Alan ayırıcıyı temsil eden düğümü alır. **null** olabilir. |
| [get_Start](./get_start/)() override | Alan başlangıcını temsil eden düğümü alır. |
| [get_Start](../field/get_start/)() const | Alan başlangıcını temsil eden düğümü alır. |
| [get_SuppressNonDelimiters](./get_suppressnondelimiters/)() | Ayırıcı olmayan karakterlerin bastırılıp bastırılmayacağını alır. |
| virtual [get_Type](../field/get_type/)() const | Microsoft Word alan türünü alır. |
| [GetFieldCode](../field/getfieldcode/)() | Alan başlangıcı ile alan ayırıcı (veya ayırıcı yoksa alan sonu) arasındaki metni döndürür. Hem alan kodu hem de alt alanların alan sonucu dahil edilir. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Alan başlangıcı ile alan ayırıcı (veya ayırıcı yoksa alan sonu) arasındaki metni döndürür. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | Alanı belgeden kaldırır. Alanın hemen sonrasındaki bir düğüm döndürür. Alanın sonu, üst düğümünün son çocuğuysa, üst paragrafını döndürür. Alan zaten kaldırılmışsa, **null** döndürür. |
| [set_BookmarkName](./set_bookmarkname/)(const System::String\&) | Ayarlayıcı [Aspose::Words::Fields::FieldRef::get_BookmarkName](./get_bookmarkname/). |
| [set_IncludeNoteOrComment](./set_includenoteorcomment/)(bool) | Yer işaretiyle işaretlenen dipnot, sonnot ve ek açıklama numaralarının artırılıp artırılmayacağını ayarlar ve ilgili dipnot, sonnot ve yorum metnini ekler. |
| [set_InsertHyperlink](./set_inserthyperlink/)(bool) | Yer işaretli paragraf için bir köprü oluşturulup oluşturulmayacağını ayarlar. |
| [set_InsertParagraphNumber](./set_insertparagraphnumber/)(bool) | Referans alınan paragrafın paragraf numarasının belgede göründüğü şekilde tam olarak eklenip eklenmeyeceğini ayarlar. |
| [set_InsertParagraphNumberInFullContext](./set_insertparagraphnumberinfullcontext/)(bool) | Referans alınan paragrafın paragraf numarasının tam bağlamda eklenip eklenmeyeceğini ayarlar. |
| [set_InsertParagraphNumberInRelativeContext](./set_insertparagraphnumberinrelativecontext/)(bool) | İlgili bağlamda başvurulan paragrafın paragraf numarasının eklenip eklenmeyeceğini ayarlar. |
| [set_InsertRelativePosition](./set_insertrelativeposition/)(bool) | Başvurulan paragrafın göreli konumunun eklenip eklenmeyeceğini ayarlar. |
| [set_IsDirty](../field/set_isdirty/)(bool) | [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/) için ayarlayıcı. |
| [set_IsLocked](../field/set_islocked/)(bool) | [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/) için ayarlayıcı. |
| [set_LocaleId](../field/set_localeid/)(int32_t) | [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/) için ayarlayıcı. |
| [set_NumberSeparator](./set_numberseparator/)(const System::String\&) | Dizi numaralarını ve sayfa numaralarını ayırmak için kullanılan karakter dizisini ayarlar. |
| [set_Result](../field/set_result/)(const System::String\&) | [Aspose::Words::Fields::Field::get_Result](../field/get_result/) için ayarlayıcı. |
| [set_SuppressNonDelimiters](./set_suppressnondelimiters/)(bool) | Ayırıcı olmayan karakterlerin bastırılıp bastırılmayacağını ayarlar. |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Alan bağlantısını kaldırır. |
| [Update](../field/update/)() | Alan güncellemesini gerçekleştirir. Alan zaten güncelleniyorsa bir istisna fırlatır. |
| [Update](../field/update/)(bool) | Bir alan güncellemesi gerçekleştirir. Alan zaten güncelleniyorsa bir istisna fırlatır. |

## Örnekler



SET alanı ile yer işaretli metin oluşturmayı ve ardından REF alanı kullanarak belge içinde görüntülemeyi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Yer işaretli metni bir SET alanı ile adlandırın.
// Bu alan, metin içinde görünen bir yer işareti yapısı değil, adlandırılmış bir değişken olan "bookmark"a referans verir.
auto fieldSet = System::ExplicitCast<Aspose::Words::Fields::FieldSet>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSet, false));
fieldSet->set_BookmarkName(u"MyBookmark");
fieldSet->set_BookmarkText(u"Hello world!");
fieldSet->Update();

ASSERT_EQ(u" SET  MyBookmark \"Hello world!\"", fieldSet->GetFieldCode());

// REF alanında yer işaretine adını kullanarak referans verin ve içeriğini gösterin.
auto fieldRef = System::ExplicitCast<Aspose::Words::Fields::FieldRef>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldRef, true));
fieldRef->set_BookmarkName(u"MyBookmark");
fieldRef->Update();

ASSERT_EQ(u" REF  MyBookmark", fieldRef->GetFieldCode());
ASSERT_EQ(u"Hello world!", fieldRef->get_Result());

doc->Save(get_ArtifactsDir() + u"Field.SET.REF.docx");
```

## Ayrıca Bakınız

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
