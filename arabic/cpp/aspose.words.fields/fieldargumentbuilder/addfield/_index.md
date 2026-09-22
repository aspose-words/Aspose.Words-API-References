---
title: "طريقة Aspose::Words::Fields::FieldArgumentBuilder::AddField"
linktitle: "AddField"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Fields::FieldArgumentBuilder::AddField. تُضيف حقلًا ممثلاً بـ FieldBuilder إلى الوسيط في C++."
type: docs
weight: 3000
url: /ar/cpp/aspose.words.fields/fieldargumentbuilder/addfield/
---
## FieldArgumentBuilder::AddField method


يضيف حقلًا ممثلاً بـ [FieldBuilder](../../fieldbuilder/) إلى الوسيط.

```cpp
System::SharedPtr<Aspose::Words::Fields::FieldArgumentBuilder> Aspose::Words::Fields::FieldArgumentBuilder::AddField(const System::SharedPtr<Aspose::Words::Fields::FieldBuilder> &fieldBuilder)
```


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

* Class [FieldArgumentBuilder](../)
* Class [FieldBuilder](../../fieldbuilder/)
* Class [FieldArgumentBuilder](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
