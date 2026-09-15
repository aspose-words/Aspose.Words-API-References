---
title: "Aspose::Words::Fields::FieldBuilder class"
linktitle: "FieldBuilder"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Fields::FieldBuilder class. يبني حقلًا من رموز كود الحقل (الوسائط والمفاتيح). لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 20000
url: /ar/cpp/aspose.words.fields/fieldbuilder/
---
## FieldBuilder class


يبني حقلًا من رموز كود الحقل (المعلمات والمفاتيح). لمزيد من المعلومات، زر [العمل مع الحقول](https://docs.aspose.com/words/cpp/working-with-fields/) مقالة الوثائق.

```cpp
class FieldBuilder : public Aspose::Words::Fields::IFieldBuildingBlock
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [AddArgument](./addargument/)(const System::String\&) | يضيف وسيطًا للحقل. |
| [AddArgument](./addargument/)(int32_t) | يضيف وسيطًا للحقل. |
| [AddArgument](./addargument/)(double) | يضيف وسيطًا للحقل. |
| [AddArgument](./addargument/)(const System::SharedPtr\<Aspose::Words::Fields::FieldBuilder\>\&) | يضيف حقلًا فرعيًا ممثلاً بـ [FieldBuilder](./) إلى كود الحقل. |
| [AddArgument](./addargument/)(const System::SharedPtr\<Aspose::Words::Fields::FieldArgumentBuilder\>\&) | يضيف وسيطًا للحقل ممثلاً بـ [FieldArgumentBuilder](../fieldargumentbuilder/) إلى كود الحقل. |
| [AddSwitch](./addswitch/)(const System::String\&) | يضيف مفتاحًا للحقل. |
| [AddSwitch](./addswitch/)(const System::String\&, const System::String\&) | يضيف مفتاحًا للحقل. |
| [AddSwitch](./addswitch/)(const System::String\&, int32_t) | يضيف مفتاحًا للحقل. |
| [AddSwitch](./addswitch/)(const System::String\&, double) | يضيف مفتاحًا للحقل. |
| [BuildAndInsert](./buildandinsert/)(const System::SharedPtr\<Aspose::Words::Inline\>\&) | يبني ويُدرج حقلًا في المستند قبل العقدة المضمنة المحددة. |
| [BuildAndInsert](./buildandinsert/)(const System::SharedPtr\<Aspose::Words::Paragraph\>\&) | يبني ويُدرج حقلًا في المستند إلى نهاية الفقرة المحددة. |
| [FieldBuilder](./fieldbuilder/)(Aspose::Words::Fields::FieldType) | يُهيئ نسخة من الفئة [FieldBuilder](./). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |

## أمثلة



يظهر كيفية إنشاء حقول باستخدام مُنشئ الحقول، ثم إدراجها في المستند.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// فيما يلي ثلاثة أمثلة على إنشاء الحقول باستخدام مُنشئ الحقول.
// 1 -  حقل واحد:
// استخدم منشئ الحقول لإضافة حقل SYMBOL يعرض رمز ƒ (فلورين).
auto builder = System::MakeObject<Aspose::Words::Fields::FieldBuilder>(Aspose::Words::Fields::FieldType::FieldSymbol);
builder->AddArgument(402);
builder->AddSwitch(u"\\f", u"Arial");
builder->AddSwitch(u"\\s", 25);
builder->AddSwitch(u"\\u");
System::SharedPtr<Aspose::Words::Fields::Field> field = builder->BuildAndInsert(doc->get_FirstSection()->get_Body()->get_FirstParagraph());

ASSERT_EQ(u" SYMBOL 402 \\f Arial \\s 25 \\u ", field->GetFieldCode());

// 2 -  حقل متداخل:
// استخدم منشئ الحقول لإنشاء حقل صيغة يُستخدم كحقل داخلي بواسطة منشئ حقول آخر.
auto innerFormulaBuilder = System::MakeObject<Aspose::Words::Fields::FieldBuilder>(Aspose::Words::Fields::FieldType::FieldFormula);
innerFormulaBuilder->AddArgument(100);
innerFormulaBuilder->AddArgument(u"+");
innerFormulaBuilder->AddArgument(74);

// أنشئ منشئًا آخر لحقل SYMBOL آخر، وأدرج حقل الصيغة
// الذي أنشأناه أعلاه داخل حقل SYMBOL كمعامل له.
builder = System::MakeObject<Aspose::Words::Fields::FieldBuilder>(Aspose::Words::Fields::FieldType::FieldSymbol);
builder->AddArgument(innerFormulaBuilder);
field = builder->BuildAndInsert(doc->get_FirstSection()->get_Body()->AppendParagraph(System::String::Empty));

// حقل SYMBOL الخارجي سيستخدم نتيجة حقل الصيغة، 174، كمعامل له،
// مما سيجعل الحقل يعرض رمز ® (علامة التسجيل) لأن رقم حرفه هو 174.
ASSERT_EQ(u" SYMBOL \u0013 = 100 + 74 \u0014\u0015 ", field->GetFieldCode());

// 3 -  حقول متداخلة متعددة ومعاملات:
// الآن، سنستخدم منشئًا لإنشاء حقل IF، الذي يعرض أحد قيمتي نص مخصصتين،
// اعتمادًا على القيمة true/false لتعبيره. للحصول على قيمة true/false
// التي تحدد أي نص يعرضه حقل IF، سيختبر حقل IF تعبيرين رقميين للتساوي.
// سنزود التعبيرين على شكل حقول صيغة، والتي سنضمّنها داخل حقل IF.
auto leftExpression = System::MakeObject<Aspose::Words::Fields::FieldBuilder>(Aspose::Words::Fields::FieldType::FieldFormula);
leftExpression->AddArgument(2);
leftExpression->AddArgument(u"+");
leftExpression->AddArgument(3);

auto rightExpression = System::MakeObject<Aspose::Words::Fields::FieldBuilder>(Aspose::Words::Fields::FieldType::FieldFormula);
rightExpression->AddArgument(2.5);
rightExpression->AddArgument(u"*");
rightExpression->AddArgument(5.2);

// بعد ذلك، سنبني معاملين للحقل، سيعملان كقيم نصية للإخراج true/false لحقل IF.
// ستعيد هذه المعاملات استخدام قيم الإخراج لتعبيراتنا الرقمية.
auto trueOutput = System::MakeObject<Aspose::Words::Fields::FieldArgumentBuilder>();
trueOutput->AddText(u"True, both expressions amount to ");
trueOutput->AddField(leftExpression);

auto falseOutput = System::MakeObject<Aspose::Words::Fields::FieldArgumentBuilder>();
falseOutput->AddNode(System::MakeObject<Aspose::Words::Run>(doc, u"False, "));
falseOutput->AddField(leftExpression);
falseOutput->AddNode(System::MakeObject<Aspose::Words::Run>(doc, u" does not equal "));
falseOutput->AddField(rightExpression);

// أخيرًا، سننشئ منشئ حقل آخر لحقل IF وندمج جميع التعبيرات.
builder = System::MakeObject<Aspose::Words::Fields::FieldBuilder>(Aspose::Words::Fields::FieldType::FieldIf);
builder->AddArgument(leftExpression);
builder->AddArgument(u"=");
builder->AddArgument(rightExpression);
builder->AddArgument(trueOutput);
builder->AddArgument(falseOutput);
field = builder->BuildAndInsert(doc->get_FirstSection()->get_Body()->AppendParagraph(System::String::Empty));

ASSERT_EQ(System::String(u" IF \u0013 = 2 + 3 \u0014\u0015 = \u0013 = 2.5 * 5.2 \u0014\u0015 ") + u"\"True, both expressions amount to \u0013 = 2 + 3 \u0014\u0015\" " + u"\"False, \u0013 = 2 + 3 \u0014\u0015 does not equal \u0013 = 2.5 * 5.2 \u0014\u0015\" ", field->GetFieldCode());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.SYMBOL.docx");
```

## انظر أيضًا

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
