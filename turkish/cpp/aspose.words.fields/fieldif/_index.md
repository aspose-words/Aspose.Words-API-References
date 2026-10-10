---
title: "Aspose::Words::Fields::FieldIf sınıfı"
linktitle: "FieldIf"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fields::FieldIf sınıfı. IF alanını uygular. Daha fazla bilgi edinmek için C++'daki belge makalesini ziyaret edin."
type: docs
weight: 54000
url: /tr/cpp/aspose.words.fields/fieldif/
---
## FieldIf class


IF alanını uygular. Daha fazla bilgi edinmek için, [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/) dokümantasyon makalesini ziyaret edin.

```cpp
class FieldIf : public Aspose::Words::Fields::Field,
                public Aspose::Words::Fields::IMergeFieldSurrogate
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [EvaluateCondition](./evaluatecondition/)() | Koşulu değerlendirir. |
| [get_ComparisonOperator](./get_comparisonoperator/)() | Karşılaştırma operatörünü alır veya ayarlar. |
| [get_DisplayResult](../field/get_displayresult/)() | Görüntülenen alan sonucunu temsil eden metni alır. |
| [get_End](./get_end/)() override | Alan sonunu temsil eden düğümü alır. |
| [get_End](../field/get_end/)() const | Alan sonunu temsil eden düğümü alır. |
| [get_FalseText](./get_falsetext/)() | Karşılaştırma ifadesi **false** olduğunda görüntülenen metni alır veya ayarlar. |
| [get_FieldEnd](../field/get_fieldend/)() const | Alan sonunu temsil eden düğümü alır. |
| [get_FieldStart](../field/get_fieldstart/)() const | Alan başlangıcını temsil eden düğümü alır. |
| [get_Format](../field/get_format/)() | Alan biçimlendirmesine tipli erişim sağlayan bir [FieldFormat](../fieldformat/) nesnesi alır. |
| [get_IsDirty](../field/get_isdirty/)() | Alan'ın mevcut sonucunun, belgeye yapılan diğer değişiklikler nedeniyle artık doğru (eski) olup olmadığını alır veya ayarlar. |
| [get_IsLocked](../field/get_islocked/)() | Alan'ın kilitli olup olmadığını (sonucunu yeniden hesaplamamalı) alır veya ayarlar. |
| [get_LeftExpression](./get_leftexpression/)() | Karşılaştırma ifadesinin sol kısmını alır veya ayarlar. |
| [get_LocaleId](../field/get_localeid/)() | Alan'ın LCID'sini alır veya ayarlar. |
| [get_Result](../field/get_result/)() | Alan ayırıcı ile alan sonu arasındaki metni alır veya ayarlar. |
| [get_RightExpression](./get_rightexpression/)() | Karşılaştırma ifadesinin sağ kısmını alır veya ayarlar. |
| [get_Separator](./get_separator/)() override | Alan ayırıcıyı temsil eden düğümü alır. **null** olabilir. |
| [get_Start](./get_start/)() override | Alan başlangıcını temsil eden düğümü alır. |
| [get_Start](../field/get_start/)() const | Alan başlangıcını temsil eden düğümü alır. |
| [get_TrueText](./get_truetext/)() | Karşılaştırma ifadesi true olduğunda görüntülenen metni alır veya ayarlar. |
| virtual [get_Type](../field/get_type/)() const | Microsoft Word alan türünü alır. |
| [GetFieldCode](../field/getfieldcode/)() | Alan başlangıcı ile alan ayırıcı (veya ayırıcı yoksa alan sonu) arasındaki metni döndürür. Hem alan kodu hem de alt alanların alan sonucu dahil edilir. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Alan başlangıcı ile alan ayırıcı (veya ayırıcı yoksa alan sonu) arasındaki metni döndürür. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | Alanı belgeden kaldırır. Alanın hemen sonrasındaki bir düğüm döndürür. Alanın sonu, üst düğümünün son çocuğuysa, üst paragrafını döndürür. Alan zaten kaldırılmışsa, **null** döndürür. |
| [set_ComparisonOperator](./set_comparisonoperator/)(const System::String\&) | [Aspose::Words::Fields::FieldIf::get_ComparisonOperator](./get_comparisonoperator/) için ayarlayıcı. |
| [set_FalseText](./set_falsetext/)(const System::String\&) | Ayarlayıcı [Aspose::Words::Fields::FieldIf::get_FalseText](./get_falsetext/). |
| [set_IsDirty](../field/set_isdirty/)(bool) | [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/) için ayarlayıcı. |
| [set_IsLocked](../field/set_islocked/)(bool) | [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/) için ayarlayıcı. |
| [set_LeftExpression](./set_leftexpression/)(const System::String\&) | Ayarlayıcı [Aspose::Words::Fields::FieldIf::get_LeftExpression](./get_leftexpression/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/) için ayarlayıcı. |
| [set_Result](../field/set_result/)(const System::String\&) | [Aspose::Words::Fields::Field::get_Result](../field/get_result/) için ayarlayıcı. |
| [set_RightExpression](./set_rightexpression/)(const System::String\&) | Ayarlayıcı [Aspose::Words::Fields::FieldIf::get_RightExpression](./get_rightexpression/). |
| [set_TrueText](./set_truetext/)(const System::String\&) | Ayarlayıcı [Aspose::Words::Fields::FieldIf::get_TrueText](./get_truetext/). |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Alan bağlantısını kaldırır. |
| [Update](../field/update/)() | Alan güncellemesini gerçekleştirir. Alan zaten güncelleniyorsa bir istisna fırlatır. |
| [Update](../field/update/)(bool) | Bir alan güncellemesi gerçekleştirir. Alan zaten güncelleniyorsa bir istisna fırlatır. |
## Açıklamalar


İfadeler [LeftExpression](./get_leftexpression/) ve [RightExpression](./get_rightexpression/) tarafından belirlenen değerleri, [ComparisonOperator](./get_comparisonoperator/) tarafından belirlenen operatörü kullanarak karşılaştırır.

Aşağıdaki formatta bir alan, posta birleştirme kaynağı olarak kullanılacaktır: { IF 0 = 0 "{PatientsNameFML}" "" \* MERGEFORMAT }

## Örnekler



IF alanının nasıl ekleneceğini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Statement 1: ");
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldIf>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIf, true));
field->set_LeftExpression(u"0");
field->set_ComparisonOperator(u"=");
field->set_RightExpression(u"1");

// IF alanı, \"TrueText\" özelliğinden bir dize gösterecektir,
// veya \"FalseText\" özelliğinden, oluşturduğumuz ifadenin doğruluğuna bağlı olarak.
field->set_TrueText(u"True");
field->set_FalseText(u"False");
field->Update();

// Bu durumda, \"0 = 1\" yanlıştır, bu yüzden gösterilen sonuç \"False\" olacaktır.
ASSERT_EQ(u" IF  0 = 1 True False", field->GetFieldCode());
ASSERT_EQ(Aspose::Words::Fields::FieldIfComparisonResult::False, field->EvaluateCondition());
ASSERT_EQ(u"False", field->get_Result());

builder->Write(u"\nStatement 2: ");
field = System::ExplicitCast<Aspose::Words::Fields::FieldIf>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIf, true));
field->set_LeftExpression(u"5");
field->set_ComparisonOperator(u"=");
field->set_RightExpression(u"2 + 3");
field->set_TrueText(u"True");
field->set_FalseText(u"False");
field->Update();

// Bu sefer ifade doğrudur, bu yüzden gösterilen sonuç \"True\" olacaktır.
ASSERT_EQ(u" IF  5 = \"2 + 3\" True False", field->GetFieldCode());
ASSERT_EQ(Aspose::Words::Fields::FieldIfComparisonResult::True, field->EvaluateCondition());
ASSERT_EQ(u"True", field->get_Result());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.IF.docx");
```

## Ayrıca Bakınız

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
