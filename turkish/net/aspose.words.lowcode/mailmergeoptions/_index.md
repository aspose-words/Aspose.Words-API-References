---
title: MailMergeOptions Class
linktitle: MailMergeOptions
articleTitle: MailMergeOptions
second_title: .NET için Aspose.Words
description: Kusursuz düşük kodlu posta birleştirme çözümleri için Aspose.Words.MailMergeOptions sınıfını keşfedin. Özelleştirilebilir özellikler ile belge otomasyonunuzu geliştirin!
type: docs
weight: 4260
url: /tr/net/aspose.words.lowcode/mailmergeoptions/
---
## MailMergeOptions class

Posta birleştirme işlevselliği için seçenekleri temsil eder.

```csharp
public class MailMergeOptions
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [MailMergeOptions](mailmergeoptions/)() | Default_Constructor |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [CleanupOptions](../../aspose.words.lowcode/mailmergeoptions/cleanupoptions/) { get; set; } | Posta birleştirme sırasında hangi öğelerin kaldırılacağını belirten bir dizi bayrak alır veya ayarlar. |
| [CleanupParagraphsWithPunctuationMarks](../../aspose.words.lowcode/mailmergeoptions/cleanupparagraphswithpunctuationmarks/) { get; set; } | Noktalama işaretli paragrafların boş olarak kabul edilip edilmeyeceğini ve kaldırılıp kaldırılmayacağını belirten bir değer alır veya ayarlar.RemoveEmptyParagraphs seçenek belirtildi. |
| [MergeDuplicateRegions](../../aspose.words.lowcode/mailmergeoptions/mergeduplicateregions/) { get; set; } | Veri kaynağına ait tüm belge birleştirme bölgelerinin, veri kaynağına ait bölgelerle veya yalnızca ilk bölgeyle bir birleştirme işlemi yürütülürken birleştirilip birleştirilmeyeceğini belirten bir değer alır veya ayarlar. |
| [MergeWholeDocument](../../aspose.words.lowcode/mailmergeoptions/mergewholedocument/) { get; set; } | Bölgelerle bir posta birleştirme işlemi yürütülürken tüm belgedeki alanların güncellenip güncellenmeyeceğini belirten bir değer alır veya ayarlar. |
| [PreserveUnusedTags](../../aspose.words.lowcode/mailmergeoptions/preserveunusedtags/) { get; set; } | Kullanılmayan "mustache" etiketlerinin korunup korunmayacağını belirten bir değer alır veya ayarlar. |
| [RegionEndTag](../../aspose.words.lowcode/mailmergeoptions/regionendtag/) { get; set; } | Bir posta birleştirme bölgesi son etiketini alır veya ayarlar. |
| [RegionStartTag](../../aspose.words.lowcode/mailmergeoptions/regionstarttag/) { get; set; } | Bir posta birleştirme bölgesi başlangıç etiketini alır veya ayarlar. |
| [RestartListsAtEachSection](../../aspose.words.lowcode/mailmergeoptions/restartlistsateachsection/) { get; set; } | Bir posta birleştirmenin yürütülmesinden sonra listelerin her bölümde yeniden başlatılıp başlatılmayacağını belirten bir değer alır veya ayarlar. |
| [RetainFirstSectionStart](../../aspose.words.lowcode/mailmergeoptions/retainfirstsectionstart/) { get; set; } | İlk belge bölümünün bölüm başlangıcının ve sonraki veri kaynağı satırları için kopyalarının posta birleştirme sırasında saklanıp saklanmayacağını veya MS Word davranışına göre güncellenip güncellenmeyeceğini belirten bir değer alır veya ayarlar. |
| [TrimWhitespaces](../../aspose.words.lowcode/mailmergeoptions/trimwhitespaces/) { get; set; } | Posta birleştirme değerlerinden son ve öndeki boşlukların kesilip kesilmeyeceğini belirten bir değer alır veya ayarlar. |
| [UnconditionalMergeFieldsAndRegions](../../aspose.words.lowcode/mailmergeoptions/unconditionalmergefieldsandregions/) { get; set; } | Üst IF alanının koşulundan bağımsız olarak birleştirme alanlarının ve birleştirme bölgelerinin birleştirilip birleştirilmeyeceğini belirten bir değer alır veya ayarlar. |
| [UseNonMergeFields](../../aspose.words.lowcode/mailmergeoptions/usenonmergefields/) { get; set; } | Ne zaman`doğru` , MERGEFIELD alanlarına ek olarak, bazı diğer alan türlerinde ve ayrıca "{{fieldName}}" etiketlerinde posta birleştirmenin gerçekleştirildiğini belirtir. |
| [UseWholeParagraphAsRegion](../../aspose.words.lowcode/mailmergeoptions/usewholeparagraphasregion/) { get; set; } | Tüm paragrafın bir değerle gösterilip gösterilmediğini belirten bir değer alır veya ayarlar**TabloBaşlangıcı** veya**Tablo Sonu** field veya belirli aralık**TabloBaşlangıcı** Ve**Tablo Sonu** alanlar posta birleştirme bölgesine dahil edilmelidir. |

## Örnekler

Tek bir kayıt için posta birleştirme işleminin nasıl yapılacağını gösterir.

```csharp
// Posta birleştirme işlemini yapmanın birkaç yolu vardır:
string doc = MyDir + "Mail merge.doc";

string[] fieldNames = new string[] { "FirstName", "Location", "SpecialCharsInName()" };
string[] fieldValues = new string[] { "James Bond", "London", "Classified" };

MailMerger.Execute(doc, ArtifactsDir + "LowCode.MailMerge.1.docx", fieldNames, fieldValues);
MailMerger.Execute(doc, ArtifactsDir + "LowCode.MailMerge.2.docx", SaveFormat.Docx, fieldNames, fieldValues);
MailMergeOptions mailMergeOptions = new MailMergeOptions();
mailMergeOptions.TrimWhitespaces = true;
MailMerger.Execute(doc, ArtifactsDir + "LowCode.MailMerge.3.docx", SaveFormat.Docx, fieldNames, fieldValues, mailMergeOptions);
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.LowCode](../../aspose.words.lowcode/)
* toplantı [Aspose.Words](../../)
