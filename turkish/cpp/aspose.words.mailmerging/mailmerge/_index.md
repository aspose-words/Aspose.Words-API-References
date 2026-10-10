---
title: "Aspose::Words::MailMerging::MailMerge class"
linktitle: "MailMerge"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::MailMerging::MailMerge class. Posta birleştirme işlevselliğini temsil eder. Daha fazla bilgi için C++'taki belge makalesini ziyaret edin."
type: docs
weight: 4000
url: /tr/cpp/aspose.words.mailmerging/mailmerge/
---
## MailMerge class


Posta birleştirme işlevselliğini temsil eder. Daha fazla bilgi için, [Mail Merge and Reporting](https://docs.aspose.com/words/cpp/mail-merge-and-reporting/) dokümantasyon makalesini ziyaret edin.

```cpp
class MailMerge : public System::Object
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [DeleteFields](./deletefields/)() | Belgeden posta birleştirme ile ilgili alanları kaldırır. |
| [Execute](./execute/)(const System::SharedPtr\<Aspose::Words::MailMerging::IMailMergeDataSource\>\&) | Özel bir veri kaynağından posta birleştirme gerçekleştirir. |
| [Execute](./execute/)(const System::ArrayPtr\<System::String\>\&, const System::ArrayPtr\<System::SharedPtr\<System::Object\>\>\&) | Tek bir kayıt için posta birleştirme işlemi gerçekleştirir. |
| [ExecuteWithRegions](./executewithregions/)(const System::SharedPtr\<Aspose::Words::MailMerging::IMailMergeDataSource\>\&) | Özel bir veri kaynağından posta birleştirme bölgeleriyle posta birleştirme gerçekleştirir. |
| [ExecuteWithRegions](./executewithregions/)(const System::SharedPtr\<Aspose::Words::MailMerging::IMailMergeDataSourceRoot\>\&) | Özel bir veri kaynağından posta birleştirme bölgeleriyle posta birleştirme gerçekleştirir. |
| [get_CleanupOptions](./get_cleanupoptions/)() const | Posta birleştirme sırasında hangi öğelerin kaldırılacağını belirten bayrak kümesini alır. |
| [get_CleanupParagraphsWithPunctuationMarks](./get_cleanupparagraphswithpunctuationmarks/)() const | Paragraf işaretleri içeren paragrafların boş olarak kabul edilip edilmediğini ve [RemoveEmptyParagraphs](../mailmergecleanupoptions/) seçeneği belirtilmişse kaldırılması gerektiğini gösteren bir değeri alır veya ayarlar. |
| [get_FieldMergingCallback](./get_fieldmergingcallback/)() const | Belge içinde bir posta birleştirme alanıyle karşılaşıldığında posta birleştirme sırasında gerçekleşir. |
| [get_MailMergeCallback](./get_mailmergecallback/)() const | Posta birleştirme sırasında belirli olayları ele almayı sağlar. |
| [get_MappedDataFields](./get_mappeddatafields/)() | Posta birleştirme işlemi için eşlenmiş veri alanlarını temsil eden bir koleksiyon döndürür. |
| [get_MergeDuplicateRegions](./get_mergeduplicateregions/)() const | Tüm belge posta birleştirme bölgelerinin, veri kaynağı adıyla eşleşenlerin, veri kaynağına karşı bölgelerle posta birleştirme yürütülürken birleştirilip birleştirilmeyeceğini veya yalnızca ilkinin birleştirileceğini gösteren değeri alır. |
| [get_MergeWholeDocument](./get_mergewholedocument/)() const | Bölgelerle posta birleştirme yürütülürken tüm belgedeki alanların güncellenip güncellenmeyeceğini gösteren değeri alır. |
| [get_PreserveUnusedTags](./get_preserveunusedtags/)() const | Kullanılmayan "mustache" etiketlerinin korunup korunmayacağını gösteren değeri alır. |
| [get_RegionEndTag](./get_regionendtag/)() const | Posta birleştirme bölgesi son etiketi alır. |
| [get_RegionStartTag](./get_regionstarttag/)() const | Posta birleştirme bölgesi başlangıç etiketi alır. |
| [get_RestartListsAtEachSection](./get_restartlistsateachsection/)() const | Posta birleştirme yürütüldükten sonra listelerin her bölümde yeniden başlatılıp başlatılmayacağını gösteren değeri alır. |
| [get_RetainFirstSectionStart](./get_retainfirstsectionstart/)() const | [SectionStart](../../aspose.words/pagesetup/get_sectionstart/) değerini alır; bu değer, ilk belge bölümünün ve sonraki veri kaynağı satırları için kopyalarının posta birleştirme sırasında korunup korunmayacağını veya MS Word davranışına göre güncellenip güncellenmeyeceğini gösterir. |
| [get_TrimWhitespaces](./get_trimwhitespaces/)() const | Posta birleştirme değerlerinden sondaki ve baştaki boşlukların kırpılıp kırpılmadığını gösteren bir değeri alır. |
| [get_UnconditionalMergeFieldsAndRegions](./get_unconditionalmergefieldsandregions/)() const | Üst IF alanının koşulundan bağımsız olarak birleştirme alanlarının ve birleştirme bölgelerinin birleştirilip birleştirilmediğini gösteren bir değeri alır. |
| [get_UseNonMergeFields](./get_usenonmergefields/)() const | **true** olduğunda, MERGEFIELD alanlarına ek olarak posta birleştirmenin bazı diğer alan türlerine ve ayrıca "{{fieldName}}" etiketlerine de uygulandığını belirtir. |
| [get_UseWholeParagraphAsRegion](./get_usewholeparagraphasregion/)() const | Tam bir paragrafın **TableStart** veya **TableEnd** alanı ile ya da **TableStart** ve **TableEnd** alanları arasındaki belirli aralığın posta birleştirme bölgesine dahil edilip edilmemesi gerektiğini gösteren bir değeri alır. |
| [GetFieldNames](./getfieldnames/)() | Belgede mevcut olan posta birleştirme alanı adlarının bir koleksiyonunu döndürür. |
| [GetFieldNamesForRegion](./getfieldnamesforregion/)(const System::String\&) | Bölgede mevcut olan posta birleştirme alanı adlarının bir koleksiyonunu döndürür. |
| [GetFieldNamesForRegion](./getfieldnamesforregion/)(const System::String\&, int32_t) | Bölgede mevcut olan posta birleştirme alanı adlarının bir koleksiyonunu döndürür. |
| [GetRegionsByName](./getregionsbyname/)(const System::String\&) | Belirtilen adla posta birleştirme bölgelerinin bir koleksiyonunu döndürür. |
| [GetRegionsHierarchy](./getregionshierarchy/)() | Belgede mevcut olan bölgelerin (alanlarla birlikte) tam hiyerarşisini döndürür. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_CleanupOptions](./set_cleanupoptions/)(Aspose::Words::MailMerging::MailMergeCleanupOptions) | Posta birleştirme sırasında hangi öğelerin kaldırılması gerektiğini belirten bir dizi bayrağı ayarlar. |
| [set_CleanupParagraphsWithPunctuationMarks](./set_cleanupparagraphswithpunctuationmarks/)(bool) | [Aspose::Words::MailMerging::MailMerge::get_CleanupParagraphsWithPunctuationMarks](./get_cleanupparagraphswithpunctuationmarks/) için ayarlayıcı. |
| [set_FieldMergingCallback](./set_fieldmergingcallback/)(const System::SharedPtr\<Aspose::Words::MailMerging::IFieldMergingCallback\>\&) | Belge içinde bir posta birleştirme alanıyle karşılaşıldığında posta birleştirme sırasında gerçekleşir. |
| [set_MailMergeCallback](./set_mailmergecallback/)(const System::SharedPtr\<Aspose::Words::MailMerging::IMailMergeCallback\>\&) | Posta birleştirme sırasında belirli olayları ele almayı sağlar. |
| [set_MergeDuplicateRegions](./set_mergeduplicateregions/)(bool) | Veri kaynağı adıyla belgede bulunan tüm posta birleştirme bölgelerinin, veri kaynağına karşı bölgelere sahip bir posta birleştirme işlemi yürütülürken birleştirilip birleştirilmeyeceğini (veya yalnızca ilkinin) gösteren bir değeri ayarlar. |
| [set_MergeWholeDocument](./set_mergewholedocument/)(bool) | Bölgelere sahip bir posta birleştirme işlemi yürütülürken belgedeki tüm alanların güncellenip güncellenmeyeceğini gösteren bir değeri ayarlar. |
| [set_PreserveUnusedTags](./set_preserveunusedtags/)(bool) | Kullanılmayan "mustache" etiketlerinin korunup korunmayacağını gösteren bir değeri ayarlar. |
| [set_RegionEndTag](./set_regionendtag/)(const System::String\&) | Posta birleştirme bölgesi son etiketi ayarlar. |
| [set_RegionStartTag](./set_regionstarttag/)(const System::String\&) | Posta birleştirme bölgesi başlangıç etiketi ayarlar. |
| [set_RestartListsAtEachSection](./set_restartlistsateachsection/)(bool) | Posta birleştirme işlemi yürütüldükten sonra listelerin her bölümde yeniden başlatılıp başlatılmayacağını gösteren bir değeri ayarlar. |
| [set_RetainFirstSectionStart](./set_retainfirstsectionstart/)(bool) | [SectionStart](../../aspose.words/pagesetup/get_sectionstart/) değerini ayarlar; bu değer, ilk belge bölümünün ve sonraki veri kaynağı satırları için kopyalarının posta birleştirme sırasında korunup korunmayacağını veya MS Word davranışına göre güncellenip güncellenmeyeceğini gösterir. |
| [set_TrimWhitespaces](./set_trimwhitespaces/)(bool) | Posta birleştirme değerlerinden sondaki ve baştaki boşlukların kırpılıp kırpılmadığını gösteren bir değeri ayarlar. |
| [set_UnconditionalMergeFieldsAndRegions](./set_unconditionalmergefieldsandregions/)(bool) | Üst IF alanının koşulundan bağımsız olarak birleştirme alanlarının ve birleştirme bölgelerinin birleştirilip birleştirilmeyeceğini gösteren bir değeri ayarlar. |
| [set_UseNonMergeFields](./set_usenonmergefields/)(bool) | [Aspose::Words::MailMerging::MailMerge::get_UseNonMergeFields](./get_usenonmergefields/) için ayarlayıcı. |
| [set_UseWholeParagraphAsRegion](./set_usewholeparagraphasregion/)(bool) | Tam bir paragrafın **TableStart** veya **TableEnd** alanı ile ya da **TableStart** ve **TableEnd** alanları arasındaki belirli aralığın posta birleştirme bölgesine dahil edilip edilmemesi gerektiğini gösteren bir değeri ayarlar. |
| static [Type](./type/)() |  |
## Açıklamalar


Posta birleştirme işleminin çalışması için belge, Word MERGEFIELD ve isteğe bağlı olarak NEXT alanlarını içermelidir. Posta birleştirme sırasında, belgedeki birleştirme alanları veri kaynağınızdaki değerlerle değiştirilir.

Posta birleştirmeyi kullanmanın iki ayrı yolu vardır: posta birleştirme bölgeleriyle ve bölgesiz.

En basit posta birleştirme, bölgesizdir ve Word'de posta birleştirmenin nasıl çalıştığına çok benzer. Bilgiyi **Execute** yöntemleriyle **DataTable**, **DataSet** veya nesne dizisi gibi bir veri kaynağından belgenize birleştirin. [MailMerge](./) nesnesi veri kaynağının tüm kayıtlarını işler ve her kayıt için belgenin tüm içeriğini kopyalar ve ekler.

[MailMerge](./) nesnesi bir NEXT alanıyla karşılaştığında, veri kaynağındaki bir sonraki kaydı seçer ve herhangi bir içerik kopyalamadan birleştirmeye devam eder.

Tanımlı posta birleştirme bölgeleriyle bir belgeye bilgi birleştirmek için [ExecuteWithRegions()](../) ve diğer aşırı yüklemeleri kullanın. Bu işlem için veri kaynağı olarak kullanabilirsiniz.

Belge içinde bölümleri dinamik olarak büyütmek istiyorsanız posta birleştirme bölgelerini kullanmanız gerekir. Posta birleştirme bölgeleri olmadan, tüm belge veri kaynağının her kaydı için tekrarlanır.

## Ayrıca Bakınız

* Namespace [Aspose::Words::MailMerging](../)
* Library [Aspose.Words for C++](../../)
