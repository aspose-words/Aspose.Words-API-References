---
title: "Aspose::Words::Fields::FieldOptions sınıfı"
linktitle: "FieldOptions"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fields::FieldOptions sınıfı. Bir belgede alan işleme kontrolü için seçenekleri temsil eder. Daha fazla bilgi edinmek için C++'daki dokümantasyon makalesini ziyaret edin."
type: docs
weight: 77000
url: /tr/cpp/aspose.words.fields/fieldoptions/
---
## FieldOptions class


Bir belgede alan işleme kontrol seçeneklerini temsil eder. Daha fazla bilgi edinmek için [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/) dokümantasyon makalesini ziyaret edin.

```cpp
class FieldOptions : public System::Object
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [get_BarcodeGenerator](./get_barcodegenerator/)() const | Özel barkod oluşturucuyu alır veya ayarlar. |
| [get_BibliographyStylesProvider](./get_bibliographystylesprovider/)() const | [FieldBibliography](../fieldbibliography/) ve [FieldCitation](../fieldcitation/) alanları için bibliyografi stilini döndüren bir sağlayıcı alır. |
| [get_BuiltInTemplatesPaths](./get_builtintemplatespaths/)() const | MS Word yerleşik şablonlarının yollarını alır veya ayarlar. |
| [get_ComparisonExpressionEvaluator](./get_comparisonexpressionevaluator/)() const | Alan karşılaştırma ifadeleri değerlendiricisini alır. |
| [get_CurrentUser](./get_currentuser/)() const | Geçerli kullanıcı bilgilerini alır veya ayarlar. |
| [get_CustomTocStyleSeparator](./get_customtocstyleseparator/)() const | [FieldToc](../fieldtoc/) alanındaki \t anahtarı için özel stil ayırıcıyı alır. |
| [get_DefaultDocumentAuthor](./get_defaultdocumentauthor/)() const | Varsayılan belge yazarının adını alır veya ayarlar. Yazar adı zaten yerleşik belge özelliklerinde belirtilmişse, bu seçenek dikkate alınmaz. |
| [get_FieldDatabaseProvider](./get_fielddatabaseprovider/)() const | [FieldDatabase](../fielddatabase/) alanı için sorgu sonucunu döndüren bir sağlayıcı alır. |
| [get_FieldIndexFormat](./get_fieldindexformat/)() | Belgedeki [FieldIndex](../fieldindex/) alanları için biçimlendirmeyi temsil eden bir [FieldIndexFormat](./get_fieldindexformat/) alır veya ayarlar. |
| [get_FieldUpdateCultureProvider](./get_fieldupdatecultureprovider/)() const | Her belirli alan için özgün bir kültür nesnesi döndüren bir sağlayıcıyı alır veya ayarlar. |
| [get_FieldUpdateCultureSource](./get_fieldupdateculturesource/)() const | Alan sonucunu biçimlendirmek için kullanılacak kültürü belirtir. |
| [get_FieldUpdatingCallback](./get_fieldupdatingcallback/)() const | [IFieldUpdatingCallback](../ifieldupdatingcallback/) uygulamasını alır. |
| [get_FieldUpdatingProgressCallback](./get_fieldupdatingprogresscallback/)() const | [IFieldUpdatingProgressCallback](../ifieldupdatingprogresscallback/) uygulamasını alır. |
| [get_FileName](./get_filename/)() const | Belgenin dosya adını alır veya ayarlar. |
| [get_IsBidiTextSupportedOnUpdate](./get_isbiditextsupportedonupdate/)() const | Alan güncellemesi sırasında çift yönlü metnin tam olarak desteklenip desteklenmediğini gösteren değeri alır veya ayarlar. |
| [get_LegacyNumberFormat](./get_legacynumberformat/)() const | Alanlar için eski (AW 13.10'dan önceki) sayı formatının etkin olup olmadığını gösteren değeri alır veya ayarlar. |
| [get_PreProcessCulture](./get_preprocessculture/)() const | Alan değerlerini ön işlemek için kültürü alır veya ayarlar. |
| [get_ResultFormatter](./get_resultformatter/)() const | Alan sonucunun nasıl biçimlendirileceğini kontrol etmeye izin verir. |
| [get_TemplateName](./get_templatename/)() const | Belge tarafından kullanılan şablonun dosya adını alır veya ayarlar. |
| [get_ToaCategories](./get_toacategories/)() const | Yetkililer kategorileri tablosunu alır veya ayarlar. |
| [get_UseInvariantCultureNumberFormat](./get_useinvariantculturenumberformat/)() const | Sayı formatının değişmez kültür kullanılarak ayrıştırılıp ayrıştırılmadığını gösteren değeri alır veya ayarlar. |
| [get_UserPromptRespondent](./get_userpromptrespondent/)() const | Alan güncellemesi sırasında kullanıcı istemlerine yanıt veren kişiyi alır veya ayarlar. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_BarcodeGenerator](./set_barcodegenerator/)(const System::SharedPtr\<Aspose::Words::Fields::IBarcodeGenerator\>\&) | Özel barkod oluşturucuyu alır veya ayarlar. |
| [set_BibliographyStylesProvider](./set_bibliographystylesprovider/)(const System::SharedPtr\<Aspose::Words::Fields::IBibliographyStylesProvider\>\&) | [FieldBibliography](../fieldbibliography/) ve [FieldCitation](../fieldcitation/) alanları için bibliyografi stilini döndüren bir sağlayıcı ayarlar. |
| [set_BuiltInTemplatesPaths](./set_builtintemplatespaths/)(const System::ArrayPtr\<System::String\>\&) | [Aspose::Words::Fields::FieldOptions::get_BuiltInTemplatesPaths](./get_builtintemplatespaths/) için ayarlayıcı. |
| [set_ComparisonExpressionEvaluator](./set_comparisonexpressionevaluator/)(const System::SharedPtr\<Aspose::Words::Fields::IComparisonExpressionEvaluator\>\&) | Alan karşılaştırma ifadeleri değerlendiricisini ayarlar. |
| [set_CurrentUser](./set_currentuser/)(const System::SharedPtr\<Aspose::Words::Fields::UserInformation\>\&) | Ayarlayıcı [Aspose::Words::Fields::FieldOptions::get_CurrentUser](./get_currentuser/). |
| [set_CustomTocStyleSeparator](./set_customtocstyleseparator/)(const System::String\&) | Ayarlayan özel stil ayırıcıyı \t anahtarı için [FieldToc](../fieldtoc/) alanında. |
| [set_DefaultDocumentAuthor](./set_defaultdocumentauthor/)(const System::String\&) | Ayarlayıcı [Aspose::Words::Fields::FieldOptions::get_DefaultDocumentAuthor](./get_defaultdocumentauthor/). |
| [set_FieldDatabaseProvider](./set_fielddatabaseprovider/)(const System::SharedPtr\<Aspose::Words::Fields::IFieldDatabaseProvider\>\&) | Ayarlayan bir sağlayıcı, [FieldDatabase](../fielddatabase/) alanı için sorgu sonucunu döndürür. |
| [set_FieldIndexFormat](./set_fieldindexformat/)(Aspose::Words::Fields::FieldIndexFormat) | Ayarlayıcı [Aspose::Words::Fields::FieldOptions::get_FieldIndexFormat](./get_fieldindexformat/). |
| [set_FieldUpdateCultureProvider](./set_fieldupdatecultureprovider/)(const System::SharedPtr\<Aspose::Words::Fields::IFieldUpdateCultureProvider\>\&) | Ayarlayıcı [Aspose::Words::Fields::FieldOptions::get_FieldUpdateCultureProvider](./get_fieldupdatecultureprovider/). |
| [set_FieldUpdateCultureSource](./set_fieldupdateculturesource/)(Aspose::Words::Fields::FieldUpdateCultureSource) | Ayarlayıcı [Aspose::Words::Fields::FieldOptions::get_FieldUpdateCultureSource](./get_fieldupdateculturesource/). |
| [set_FieldUpdatingCallback](./set_fieldupdatingcallback/)(const System::SharedPtr\<Aspose::Words::Fields::IFieldUpdatingCallback\>\&) | [IFieldUpdatingCallback](../ifieldupdatingcallback/) uygulamasını ayarlar. |
| [set_FieldUpdatingProgressCallback](./set_fieldupdatingprogresscallback/)(const System::SharedPtr\<Aspose::Words::Fields::IFieldUpdatingProgressCallback\>\&) | [IFieldUpdatingProgressCallback](../ifieldupdatingprogresscallback/) uygulamasını ayarlar. |
| [set_FileName](./set_filename/)(const System::String\&) | Ayarlayıcı [Aspose::Words::Fields::FieldOptions::get_FileName](./get_filename/). |
| [set_IsBidiTextSupportedOnUpdate](./set_isbiditextsupportedonupdate/)(bool) | Ayarlayıcı [Aspose::Words::Fields::FieldOptions::get_IsBidiTextSupportedOnUpdate](./get_isbiditextsupportedonupdate/). |
| [set_LegacyNumberFormat](./set_legacynumberformat/)(bool) | Ayarlayıcı [Aspose::Words::Fields::FieldOptions::get_LegacyNumberFormat](./get_legacynumberformat/). |
| [set_PreProcessCulture](./set_preprocessculture/)(const System::SharedPtr\<System::Globalization::CultureInfo\>\&) | Ayarlayıcı [Aspose::Words::Fields::FieldOptions::get_PreProcessCulture](./get_preprocessculture/). |
| [set_ResultFormatter](./set_resultformatter/)(const System::SharedPtr\<Aspose::Words::Fields::IFieldResultFormatter\>\&) | Alan sonucunun nasıl biçimlendirileceğini kontrol etmeye izin verir. |
| [set_TemplateName](./set_templatename/)(const System::String\&) | Ayarlayıcı [Aspose::Words::Fields::FieldOptions::get_TemplateName](./get_templatename/). |
| [set_ToaCategories](./set_toacategories/)(const System::SharedPtr\<Aspose::Words::Fields::ToaCategories\>\&) | Ayarlayıcı [Aspose::Words::Fields::FieldOptions::get_ToaCategories](./get_toacategories/). |
| [set_UseInvariantCultureNumberFormat](./set_useinvariantculturenumberformat/)(bool) | Ayarlayıcı [Aspose::Words::Fields::FieldOptions::get_UseInvariantCultureNumberFormat](./get_useinvariantculturenumberformat/). |
| [set_UserPromptRespondent](./set_userpromptrespondent/)(const System::SharedPtr\<Aspose::Words::Fields::IFieldUserPromptRespondent\>\&) | Ayarlayıcı [Aspose::Words::Fields::FieldOptions::get_UserPromptRespondent](./get_userpromptrespondent/). |
| static [Type](./type/)() |  |
## Ayrıca Bakınız

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
