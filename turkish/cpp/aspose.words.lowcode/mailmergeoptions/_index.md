---
title: "Aspose::Words::LowCode::MailMergeOptions sınıfı"
linktitle: "MailMergeOptions"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::LowCode::MailMergeOptions sınıfı. C++'ta posta birleştirme işlevi için seçenekleri temsil eder."
type: docs
weight: 750
url: /tr/cpp/aspose.words.lowcode/mailmergeoptions/
---
## MailMergeOptions class


Posta birleştirme işlevi için seçenekleri temsil eder.

```cpp
class MailMergeOptions : public System::Object
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [get_CleanupOptions](./get_cleanupoptions/)() const | Posta birleştirme sırasında hangi öğelerin kaldırılacağını belirten bayrak kümesini alır. |
| [get_CleanupParagraphsWithPunctuationMarks](./get_cleanupparagraphswithpunctuationmarks/)() const | Paragraf işaretleri içeren paragrafların boş olarak kabul edilip edilmediğini ve [RemoveEmptyParagraphs](../../aspose.words.mailmerging/mailmergecleanupoptions/) seçeneği belirtilmişse kaldırılıp kaldırılmayacağını gösteren değeri alır veya ayarlar. |
| [get_MergeDuplicateRegions](./get_mergeduplicateregions/)() const | Tüm belge posta birleştirme bölgelerinin, veri kaynağı adıyla eşleşenlerin, veri kaynağına karşı bölgelerle posta birleştirme yürütülürken birleştirilip birleştirilmeyeceğini veya yalnızca ilkinin birleştirileceğini gösteren değeri alır. |
| [get_MergeWholeDocument](./get_mergewholedocument/)() const | Bölgelerle posta birleştirme yürütülürken tüm belgedeki alanların güncellenip güncellenmeyeceğini gösteren değeri alır. |
| [get_PreserveUnusedTags](./get_preserveunusedtags/)() const | Kullanılmayan "mustache" etiketlerinin korunup korunmayacağını gösteren değeri alır. |
| [get_RegionEndTag](./get_regionendtag/)() const | Posta birleştirme bölgesi son etiketi alır. |
| [get_RegionStartTag](./get_regionstarttag/)() const | Posta birleştirme bölgesi başlangıç etiketi alır. |
| [get_RestartListsAtEachSection](./get_restartlistsateachsection/)() const | Posta birleştirme yürütüldükten sonra listelerin her bölümde yeniden başlatılıp başlatılmayacağını gösteren değeri alır. |
| [get_RetainFirstSectionStart](./get_retainfirstsectionstart/)() const | Posta birleştirme sırasında ilk belge bölümünün bölüm başlangıcı ve sonraki veri kaynağı satırları için kopyalarının korunup korunmayacağını veya MS Word davranışına göre güncellenip güncellenmeyeceğini gösteren değeri alır. |
| [get_TrimWhitespaces](./get_trimwhitespaces/)() const | Posta birleştirme değerlerinden sondaki ve baştaki boşlukların kırpılıp kırpılmadığını gösteren bir değeri alır. |
| [get_UnconditionalMergeFieldsAndRegions](./get_unconditionalmergefieldsandregions/)() const | Üst IF alanının koşulundan bağımsız olarak birleştirme alanlarının ve birleştirme bölgelerinin birleştirilip birleştirilmediğini gösteren bir değeri alır. |
| [get_UseNonMergeFields](./get_usenonmergefields/)() const | **true** olduğunda, MERGEFIELD alanlarına ek olarak posta birleştirmenin bazı diğer alan türlerine ve ayrıca "{{fieldName}}" etiketlerine de uygulandığını belirtir. |
| [get_UseWholeParagraphAsRegion](./get_usewholeparagraphasregion/)() const | Tam bir paragrafın **TableStart** veya **TableEnd** alanı ile ya da **TableStart** ve **TableEnd** alanları arasındaki belirli aralığın posta birleştirme bölgesine dahil edilip edilmemesi gerektiğini gösteren bir değeri alır. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [MailMergeOptions](./mailmergeoptions/)() |  |
| [set_CleanupOptions](./set_cleanupoptions/)(Aspose::Words::MailMerging::MailMergeCleanupOptions) | Posta birleştirme sırasında hangi öğelerin kaldırılması gerektiğini belirten bir dizi bayrağı ayarlar. |
| [set_CleanupParagraphsWithPunctuationMarks](./set_cleanupparagraphswithpunctuationmarks/)(bool) | Şunun ayarlayıcısı: [Aspose::Words::LowCode::MailMergeOptions::get_CleanupParagraphsWithPunctuationMarks](./get_cleanupparagraphswithpunctuationmarks/). |
| [set_MergeDuplicateRegions](./set_mergeduplicateregions/)(bool) | Veri kaynağı adıyla belgede bulunan tüm posta birleştirme bölgelerinin, veri kaynağına karşı bölgelere sahip bir posta birleştirme işlemi yürütülürken birleştirilip birleştirilmeyeceğini (veya yalnızca ilkinin) gösteren bir değeri ayarlar. |
| [set_MergeWholeDocument](./set_mergewholedocument/)(bool) | Bölgelere sahip bir posta birleştirme işlemi yürütülürken belgedeki tüm alanların güncellenip güncellenmeyeceğini gösteren bir değeri ayarlar. |
| [set_PreserveUnusedTags](./set_preserveunusedtags/)(bool) | Kullanılmayan "mustache" etiketlerinin korunup korunmayacağını gösteren bir değeri ayarlar. |
| [set_RegionEndTag](./set_regionendtag/)(const System::String\&) | Posta birleştirme bölgesi son etiketi ayarlar. |
| [set_RegionStartTag](./set_regionstarttag/)(const System::String\&) | Posta birleştirme bölgesi başlangıç etiketi ayarlar. |
| [set_RestartListsAtEachSection](./set_restartlistsateachsection/)(bool) | Posta birleştirme işlemi yürütüldükten sonra listelerin her bölümde yeniden başlatılıp başlatılmayacağını gösteren bir değeri ayarlar. |
| [set_RetainFirstSectionStart](./set_retainfirstsectionstart/)(bool) | Posta birleştirme sırasında ilk belge bölümünün bölüm başlangıcı ve sonraki veri kaynağı satırları için kopyalarının MS Word davranışına göre korunup korunmayacağını veya güncellenip güncellenmeyeceğini gösteren bir değeri ayarlar. |
| [set_TrimWhitespaces](./set_trimwhitespaces/)(bool) | Posta birleştirme değerlerinden sondaki ve baştaki boşlukların kırpılıp kırpılmadığını gösteren bir değeri ayarlar. |
| [set_UnconditionalMergeFieldsAndRegions](./set_unconditionalmergefieldsandregions/)(bool) | Üst IF alanının koşulundan bağımsız olarak birleştirme alanlarının ve birleştirme bölgelerinin birleştirilip birleştirilmeyeceğini gösteren bir değeri ayarlar. |
| [set_UseNonMergeFields](./set_usenonmergefields/)(bool) | Şunun ayarlayıcısı: [Aspose::Words::LowCode::MailMergeOptions::get_UseNonMergeFields](./get_usenonmergefields/). |
| [set_UseWholeParagraphAsRegion](./set_usewholeparagraphasregion/)(bool) | Tam bir paragrafın **TableStart** veya **TableEnd** alanı ile ya da **TableStart** ve **TableEnd** alanları arasındaki belirli aralığın posta birleştirme bölgesine dahil edilip edilmemesi gerektiğini gösteren bir değeri ayarlar. |
| static [Type](./type/)() |  |
## Ayrıca Bakınız

* Namespace [Aspose::Words::LowCode](../)
* Library [Aspose.Words for C++](../../)
