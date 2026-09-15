---
title: "Aspose::Words::Fields::FieldOptions فئة"
linktitle: "FieldOptions"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Fields::FieldOptions فئة. يمثل خيارات للتحكم في معالجة الحقول في مستند. للتعرف على المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 77000
url: /ar/cpp/aspose.words.fields/fieldoptions/
---
## FieldOptions class


يمثل خيارات للتحكم في معالجة الحقول في مستند. لمعرفة المزيد، قم بزيارة مقالة الوثائق [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/).

```cpp
class FieldOptions : public System::Object
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [get_BarcodeGenerator](./get_barcodegenerator/)() const | الحصول على أو تعيين مولد الباركود المخصص. |
| [get_BibliographyStylesProvider](./get_bibliographystylesprovider/)() const | الحصول على موفر يُعيد نمط ببليوغرافيا لحقول [FieldBibliography](../fieldbibliography/) و[FieldCitation](../fieldcitation/). |
| [get_BuiltInTemplatesPaths](./get_builtintemplatespaths/)() const | الحصول على أو تعيين مسارات القوالب المدمجة في MS Word. |
| [get_ComparisonExpressionEvaluator](./get_comparisonexpressionevaluator/)() const | الحصول على مُقَيِّم تعبيرات مقارنة الحقول. |
| [get_CurrentUser](./get_currentuser/)() const | الحصول على أو تعيين معلومات المستخدم الحالي. |
| [get_CustomTocStyleSeparator](./get_customtocstyleseparator/)() const | الحصول على فاصل النمط المخصص للمفتاح \t في حقل [FieldToc](../fieldtoc/). |
| [get_DefaultDocumentAuthor](./get_defaultdocumentauthor/)() const | الحصول على أو تعيين اسم مؤلف المستند الافتراضي. إذا تم تحديد اسم المؤلف مسبقًا في خصائص المستند المدمجة، فلن يُؤخذ هذا الخيار في الاعتبار. |
| [get_FieldDatabaseProvider](./get_fielddatabaseprovider/)() const | الحصول على موفر يُعيد نتيجة استعلام لحقل [FieldDatabase](../fielddatabase/). |
| [get_FieldIndexFormat](./get_fieldindexformat/)() | الحصول على أو تعيين [FieldIndexFormat](./get_fieldindexformat/) الذي يمثل تنسيق حقول [FieldIndex](../fieldindex/) في المستند. |
| [get_FieldUpdateCultureProvider](./get_fieldupdatecultureprovider/)() const | الحصول على أو تعيين موفر يُعيد كائن ثقافة مخصص لكل حقل على حدة. |
| [get_FieldUpdateCultureSource](./get_fieldupdateculturesource/)() const | يحدد الثقافة المستخدمة لتنسيق نتيجة الحقل. |
| [get_FieldUpdatingCallback](./get_fieldupdatingcallback/)() const | الحصول على تنفيذ [IFieldUpdatingCallback](../ifieldupdatingcallback/). |
| [get_FieldUpdatingProgressCallback](./get_fieldupdatingprogresscallback/)() const | الحصول على تنفيذ [IFieldUpdatingProgressCallback](../ifieldupdatingprogresscallback/). |
| [get_FileName](./get_filename/)() const | الحصول على أو تعيين اسم ملف المستند. |
| [get_IsBidiTextSupportedOnUpdate](./get_isbiditextsupportedonupdate/)() const | الحصول على أو تعيين القيمة التي تشير إلى ما إذا كان النص ثنائي الاتجاه مدعومًا بالكامل أثناء تحديث الحقل أم لا. |
| [get_LegacyNumberFormat](./get_legacynumberformat/)() const | الحصول على أو تعيين القيمة التي تشير إلى ما إذا كان تنسيق الأرقام القديم (أقدم من AW 13.10) للحقول مفعلاً أم لا. |
| [get_PreProcessCulture](./get_preprocessculture/)() const | الحصول على أو تعيين الثقافة لمعالجة قيم الحقول مسبقًا. |
| [get_ResultFormatter](./get_resultformatter/)() const | يسمح بالتحكم في طريقة تنسيق نتيجة الحقل. |
| [get_TemplateName](./get_templatename/)() const | الحصول على أو تعيين اسم ملف القالب المستخدم في المستند. |
| [get_ToaCategories](./get_toacategories/)() const | الحصول على أو تعيين جدول فئات السلطات. |
| [get_UseInvariantCultureNumberFormat](./get_useinvariantculturenumberformat/)() const | الحصول على أو تعيين القيمة التي تشير إلى ما إذا كان تنسيق الأرقام يُحلل باستخدام ثقافة ثابتة أم لا. |
| [get_UserPromptRespondent](./get_userpromptrespondent/)() const | الحصول على أو تعيين المستجيب لمطالبات المستخدم أثناء تحديث الحقل. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_BarcodeGenerator](./set_barcodegenerator/)(const System::SharedPtr\<Aspose::Words::Fields::IBarcodeGenerator\>\&) | الحصول على أو تعيين مولد الباركود المخصص. |
| [set_BibliographyStylesProvider](./set_bibliographystylesprovider/)(const System::SharedPtr\<Aspose::Words::Fields::IBibliographyStylesProvider\>\&) | تعيين موفر يُعيد نمط ببليوغرافيا لحقول [FieldBibliography](../fieldbibliography/) و[FieldCitation](../fieldcitation/). |
| [set_BuiltInTemplatesPaths](./set_builtintemplatespaths/)(const System::ArrayPtr\<System::String\>\&) | مُعيّن لـ [Aspose::Words::Fields::FieldOptions::get_BuiltInTemplatesPaths](./get_builtintemplatespaths/). |
| [set_ComparisonExpressionEvaluator](./set_comparisonexpressionevaluator/)(const System::SharedPtr\<Aspose::Words::Fields::IComparisonExpressionEvaluator\>\&) | تعيين مُقَيِّم تعبيرات مقارنة الحقول. |
| [set_CurrentUser](./set_currentuser/)(const System::SharedPtr\<Aspose::Words::Fields::UserInformation\>\&) | محدد لـ [Aspose::Words::Fields::FieldOptions::get_CurrentUser](./get_currentuser/). |
| [set_CustomTocStyleSeparator](./set_customtocstyleseparator/)(const System::String\&) | يضبط فاصل النمط المخصص للمفتاح \t في حقل [FieldToc](../fieldtoc/). |
| [set_DefaultDocumentAuthor](./set_defaultdocumentauthor/)(const System::String\&) | محدد لـ [Aspose::Words::Fields::FieldOptions::get_DefaultDocumentAuthor](./get_defaultdocumentauthor/). |
| [set_FieldDatabaseProvider](./set_fielddatabaseprovider/)(const System::SharedPtr\<Aspose::Words::Fields::IFieldDatabaseProvider\>\&) | يضبط موفرًا يُعيد نتيجة استعلام لحقل [FieldDatabase](../fielddatabase/). |
| [set_FieldIndexFormat](./set_fieldindexformat/)(Aspose::Words::Fields::FieldIndexFormat) | محدد لـ [Aspose::Words::Fields::FieldOptions::get_FieldIndexFormat](./get_fieldindexformat/). |
| [set_FieldUpdateCultureProvider](./set_fieldupdatecultureprovider/)(const System::SharedPtr\<Aspose::Words::Fields::IFieldUpdateCultureProvider\>\&) | محدد لـ [Aspose::Words::Fields::FieldOptions::get_FieldUpdateCultureProvider](./get_fieldupdatecultureprovider/). |
| [set_FieldUpdateCultureSource](./set_fieldupdateculturesource/)(Aspose::Words::Fields::FieldUpdateCultureSource) | محدد لـ [Aspose::Words::Fields::FieldOptions::get_FieldUpdateCultureSource](./get_fieldupdateculturesource/). |
| [set_FieldUpdatingCallback](./set_fieldupdatingcallback/)(const System::SharedPtr\<Aspose::Words::Fields::IFieldUpdatingCallback\>\&) | يضبط تنفيذ [IFieldUpdatingCallback](../ifieldupdatingcallback/). |
| [set_FieldUpdatingProgressCallback](./set_fieldupdatingprogresscallback/)(const System::SharedPtr\<Aspose::Words::Fields::IFieldUpdatingProgressCallback\>\&) | يضبط تنفيذ [IFieldUpdatingProgressCallback](../ifieldupdatingprogresscallback/). |
| [set_FileName](./set_filename/)(const System::String\&) | محدد لـ [Aspose::Words::Fields::FieldOptions::get_FileName](./get_filename/). |
| [set_IsBidiTextSupportedOnUpdate](./set_isbiditextsupportedonupdate/)(bool) | محدد لـ [Aspose::Words::Fields::FieldOptions::get_IsBidiTextSupportedOnUpdate](./get_isbiditextsupportedonupdate/). |
| [set_LegacyNumberFormat](./set_legacynumberformat/)(bool) | محدد لـ [Aspose::Words::Fields::FieldOptions::get_LegacyNumberFormat](./get_legacynumberformat/). |
| [set_PreProcessCulture](./set_preprocessculture/)(const System::SharedPtr\<System::Globalization::CultureInfo\>\&) | محدد لـ [Aspose::Words::Fields::FieldOptions::get_PreProcessCulture](./get_preprocessculture/). |
| [set_ResultFormatter](./set_resultformatter/)(const System::SharedPtr\<Aspose::Words::Fields::IFieldResultFormatter\>\&) | يسمح بالتحكم في طريقة تنسيق نتيجة الحقل. |
| [set_TemplateName](./set_templatename/)(const System::String\&) | محدد لـ [Aspose::Words::Fields::FieldOptions::get_TemplateName](./get_templatename/). |
| [set_ToaCategories](./set_toacategories/)(const System::SharedPtr\<Aspose::Words::Fields::ToaCategories\>\&) | محدد لـ [Aspose::Words::Fields::FieldOptions::get_ToaCategories](./get_toacategories/). |
| [set_UseInvariantCultureNumberFormat](./set_useinvariantculturenumberformat/)(bool) | محدد لـ [Aspose::Words::Fields::FieldOptions::get_UseInvariantCultureNumberFormat](./get_useinvariantculturenumberformat/). |
| [set_UserPromptRespondent](./set_userpromptrespondent/)(const System::SharedPtr\<Aspose::Words::Fields::IFieldUserPromptRespondent\>\&) | محدد لـ [Aspose::Words::Fields::FieldOptions::get_UserPromptRespondent](./get_userpromptrespondent/). |
| static [Type](./type/)() |  |
## انظر أيضًا

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
