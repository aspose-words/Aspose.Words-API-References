---
title: "Aspose::Words::Layout::RevisionOptions sınıfı"
linktitle: "RevisionOptions"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Layout::RevisionOptions sınıfı. Belge revizyonlarının yerleşim sürecinde nasıl işlendiğini kontrol etmeyi sağlar. Daha fazla bilgi için C++'daki dokümantasyon makalesini ziyaret edin."
type: docs
weight: 5000
url: /tr/cpp/aspose.words.layout/revisionoptions/
---
## RevisionOptions class


Düzen sürecinde belge revizyonlarının nasıl ele alındığını kontrol etmeyi sağlar. Daha fazla bilgi için, [Converting to Fixed-page Format](https://docs.aspose.com/words/cpp/converting-to-fixed-page-format/) dokümantasyon makalesini ziyaret edin.

```cpp
class RevisionOptions : public System::Object
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [get_CommentColor](./get_commentcolor/)() const | Yorumlar için kullanılacak rengi belirtmenizi sağlar. Varsayılan değer [Red](../revisioncolor/). |
| [get_DeleteCellColor](./get_deletecellcolor/)() | Silinen hücreler için kullanılacak rengi belirtmenizi sağlar [Deletion](../../aspose.words/revisiontype/). Varsayılan değer [Pink](../revisioncolor/). |
| [get_DeletedTextColor](./get_deletedtextcolor/)() | Silinen içerik için kullanılacak rengi belirtmenizi sağlar [Deletion](../../aspose.words/revisiontype/). Varsayılan değer [ByAuthor](../revisioncolor/). |
| [get_DeletedTextEffect](./get_deletedtexteffect/)() | Silinen içeriğe uygulanacak efekti belirtmenizi sağlar [Deletion](../../aspose.words/revisiontype/). Varsayılan değer [StrikeThrough](../revisiontexteffect/) |
| [get_InsertCellColor](./get_insertcellcolor/)() | Eklenecek hücreler için kullanılacak rengi belirtmenizi sağlar [Insertion](../../aspose.words/revisiontype/). Varsayılan değer [Blue](../revisioncolor/). |
| [get_InsertedTextColor](./get_insertedtextcolor/)() | Eklenecek içerik için kullanılacak rengi belirtmenizi sağlar [Insertion](../../aspose.words/revisiontype/). Varsayılan değer [ByAuthor](../revisioncolor/). |
| [get_InsertedTextEffect](./get_insertedtexteffect/)() | Eklenecek içeriğe uygulanacak efekti belirtmenizi sağlar [Insertion](../../aspose.words/revisiontype/). Varsayılan değer [Underline](../revisiontexteffect/). |
| [get_MeasurementUnit](./get_measurementunit/)() const | Revizyon yorumları için ölçü birimlerini belirtmenizi sağlar. Varsayılan değer [Centimeters](../../aspose.words/measurementunits/) |
| [get_MovedFromTextColor](./get_movedfromtextcolor/)() | İçeriğin taşındığı alanlar için kullanılacak rengi belirtmenizi sağlar [Moving](../../aspose.words/revisiontype/). Varsayılan değer [ByAuthor](../revisioncolor/). |
| [get_MovedFromTextEffect](./get_movedfromtexteffect/)() | İçeriğin taşındığı alanlara uygulanacak efekti belirtmenizi sağlar [Moving](../../aspose.words/revisiontype/). Varsayılan değer [DoubleStrikeThrough](../revisiontexteffect/) |
| [get_MovedToTextColor](./get_movedtotextcolor/)() | İçeriğin taşındığı hedef alanlar için kullanılacak rengi belirtmenizi sağlar [Moving](../../aspose.words/revisiontype/). Varsayılan değer [ByAuthor](../revisioncolor/). |
| [get_MovedToTextEffect](./get_movedtotexteffect/)() | İçeriğin taşındığı hedef alanlara uygulanacak efekti belirtmenizi sağlar [Moving](../../aspose.words/revisiontype/). Varsayılan değer [DoubleUnderline](../revisiontexteffect/) |
| [get_RevisedPropertiesColor](./get_revisedpropertiescolor/)() | Biçimlendirme özelliklerinde değişiklik olan içerik için kullanılacak rengi belirtmenizi sağlar [FormatChange](../../aspose.words/revisiontype/) Varsayılan değer [NoHighlight](../revisioncolor/). |
| [get_RevisedPropertiesEffect](./get_revisedpropertieseffect/)() | Biçimlendirme özelliklerinde değişiklik olan içerik alanları için efekti belirtmenizi sağlar [FormatChange](../../aspose.words/revisiontype/) Varsayılan değer [None](../revisiontexteffect/) |
| [get_RevisionBarsColor](./get_revisionbarscolor/)() const | Revize bilgi içeren belge satırlarını belirten kenar çubukları için kullanılacak rengi belirtmenizi sağlar. Varsayılan değer [Red](../revisioncolor/). |
| [get_RevisionBarsPosition](./get_revisionbarsposition/)() const | Revizyon çubuklarının renderleme konumunu alır veya ayarlar. Varsayılan değer [Outside](../../aspose.words.drawing/horizontalalignment/). |
| [get_RevisionBarsWidth](./get_revisionbarswidth/)() const | Revizyon çubuklarının genişliğini alır veya ayarlar, puan. |
| [get_ShowInBalloons](./get_showinballoons/)() const | Revizyonların balonlarda renderlenip renderlenmeyeceğini belirtmenizi sağlar. Varsayılan değer [None](../showinballoons/). |
| [get_ShowOriginalRevision](./get_showoriginalrevision/)() const | Orijinal metnin revize edilmişin yerine gösterilip gösterilmeyeceğini belirtmenizi sağlar. Varsayılan değer **false**. |
| [get_ShowRevisionBars](./get_showrevisionbars/)() const | Revizyon çubuklarının revize içerik içeren satırların yakınında renderlenip renderlenmeyeceğini belirtmenizi sağlar. Varsayılan değer **true**. |
| [get_ShowRevisionMarks](./get_showrevisionmarks/)() const | Revizyon metninin özel biçimlendirme işaretlemesiyle işaretlenip işaretlenmeyeceğini belirtmenizi sağlar. Varsayılan değer **true**. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_CommentColor](./set_commentcolor/)(Aspose::Words::Layout::RevisionColor) | [Aspose::Words::Layout::RevisionOptions::get_CommentColor](./get_commentcolor/) için ayarlayıcı. |
| [set_DeleteCellColor](./set_deletecellcolor/)(Aspose::Words::Layout::RevisionColor) | Ayarlayıcı [Aspose::Words::Layout::RevisionOptions::get_DeleteCellColor](./get_deletecellcolor/). |
| [set_DeletedTextColor](./set_deletedtextcolor/)(Aspose::Words::Layout::RevisionColor) | Ayarlayıcı [Aspose::Words::Layout::RevisionOptions::get_DeletedTextColor](./get_deletedtextcolor/). |
| [set_DeletedTextEffect](./set_deletedtexteffect/)(Aspose::Words::Layout::RevisionTextEffect) | Ayarlayıcı [Aspose::Words::Layout::RevisionOptions::get_DeletedTextEffect](./get_deletedtexteffect/). |
| [set_InsertCellColor](./set_insertcellcolor/)(Aspose::Words::Layout::RevisionColor) | Ayarlayıcı [Aspose::Words::Layout::RevisionOptions::get_InsertCellColor](./get_insertcellcolor/). |
| [set_InsertedTextColor](./set_insertedtextcolor/)(Aspose::Words::Layout::RevisionColor) | Ayarlayıcı [Aspose::Words::Layout::RevisionOptions::get_InsertedTextColor](./get_insertedtextcolor/). |
| [set_InsertedTextEffect](./set_insertedtexteffect/)(Aspose::Words::Layout::RevisionTextEffect) | Ayarlayıcı [Aspose::Words::Layout::RevisionOptions::get_InsertedTextEffect](./get_insertedtexteffect/). |
| [set_MeasurementUnit](./set_measurementunit/)(Aspose::Words::MeasurementUnits) | Revizyon yorumları için ölçü birimlerini belirtmenizi sağlar. Varsayılan değer [Centimeters](../../aspose.words/measurementunits/) |
| [set_MovedFromTextColor](./set_movedfromtextcolor/)(Aspose::Words::Layout::RevisionColor) | Ayarlayıcı [Aspose::Words::Layout::RevisionOptions::get_MovedFromTextColor](./get_movedfromtextcolor/). |
| [set_MovedFromTextEffect](./set_movedfromtexteffect/)(Aspose::Words::Layout::RevisionTextEffect) | Ayarlayıcı [Aspose::Words::Layout::RevisionOptions::get_MovedFromTextEffect](./get_movedfromtexteffect/). |
| [set_MovedToTextColor](./set_movedtotextcolor/)(Aspose::Words::Layout::RevisionColor) | Ayarlayıcı [Aspose::Words::Layout::RevisionOptions::get_MovedToTextColor](./get_movedtotextcolor/). |
| [set_MovedToTextEffect](./set_movedtotexteffect/)(Aspose::Words::Layout::RevisionTextEffect) | Ayarlayıcı [Aspose::Words::Layout::RevisionOptions::get_MovedToTextEffect](./get_movedtotexteffect/). |
| [set_RevisedPropertiesColor](./set_revisedpropertiescolor/)(Aspose::Words::Layout::RevisionColor) | Ayarlayıcı [Aspose::Words::Layout::RevisionOptions::get_RevisedPropertiesColor](./get_revisedpropertiescolor/). |
| [set_RevisedPropertiesEffect](./set_revisedpropertieseffect/)(Aspose::Words::Layout::RevisionTextEffect) | Ayarlayıcı [Aspose::Words::Layout::RevisionOptions::get_RevisedPropertiesEffect](./get_revisedpropertieseffect/). |
| [set_RevisionBarsColor](./set_revisionbarscolor/)(Aspose::Words::Layout::RevisionColor) | Ayarlayıcı [Aspose::Words::Layout::RevisionOptions::get_RevisionBarsColor](./get_revisionbarscolor/). |
| [set_RevisionBarsPosition](./set_revisionbarsposition/)(Aspose::Words::Drawing::HorizontalAlignment) | Ayarlayıcı [Aspose::Words::Layout::RevisionOptions::get_RevisionBarsPosition](./get_revisionbarsposition/). |
| [set_RevisionBarsWidth](./set_revisionbarswidth/)(float) | Ayarlayıcı [Aspose::Words::Layout::RevisionOptions::get_RevisionBarsWidth](./get_revisionbarswidth/). |
| [set_ShowInBalloons](./set_showinballoons/)(Aspose::Words::Layout::ShowInBalloons) | Ayarlayıcı [Aspose::Words::Layout::RevisionOptions::get_ShowInBalloons](./get_showinballoons/). |
| [set_ShowOriginalRevision](./set_showoriginalrevision/)(bool) | Ayarlayıcı [Aspose::Words::Layout::RevisionOptions::get_ShowOriginalRevision](./get_showoriginalrevision/). |
| [set_ShowRevisionBars](./set_showrevisionbars/)(bool) | Ayarlayıcı [Aspose::Words::Layout::RevisionOptions::get_ShowRevisionBars](./get_showrevisionbars/). |
| [set_ShowRevisionMarks](./set_showrevisionmarks/)(bool) | Ayarlayıcı [Aspose::Words::Layout::RevisionOptions::get_ShowRevisionMarks](./get_showrevisionmarks/). |
| static [Type](./type/)() |  |

## Örnekler



Bir oluşturulmuş çıktı belgesinde revizyonların görünümünün nasıl değiştirileceğini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Bir revizyon ekleyin, ardından tüm revizyonların rengini yeşile değiştirin.
builder->Writeln(u"This is not a revision.");
doc->StartTrackRevisions(u"John Doe", System::DateTime::get_Now());
builder->Writeln(u"This is a revision.");
doc->StopTrackRevisions();
builder->Writeln(u"This is not a revision.");

// Her revize edilmiş satırın solunda görünen çubuğu kaldırın.
doc->get_LayoutOptions()->get_RevisionOptions()->set_InsertedTextColor(Aspose::Words::Layout::RevisionColor::BrightGreen);
doc->get_LayoutOptions()->get_RevisionOptions()->set_ShowRevisionBars(false);
doc->get_LayoutOptions()->get_RevisionOptions()->set_RevisionBarsPosition(Aspose::Words::Drawing::HorizontalAlignment::Right);

doc->Save(get_ArtifactsDir() + u"Revision.LayoutOptionsRevisions.pdf");
```

## Ayrıca Bakınız

* Namespace [Aspose::Words::Layout](../)
* Library [Aspose.Words for C++](../../)
