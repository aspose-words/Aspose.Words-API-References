---
title: "Aspose::Words::Fields::FieldBuilder::AddArgument yöntemi"
linktitle: "AddArgument"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fields::FieldBuilder::AddArgument yöntemi. C++'ta bir alanın koduna FieldArgumentBuilder tarafından temsil edilen bir alan argümanını ekler."
type: docs
weight: 3000
url: /tr/cpp/aspose.words.fields/fieldbuilder/addargument/
---
## FieldBuilder::AddArgument(const System::SharedPtr\<Aspose::Words::Fields::FieldArgumentBuilder\>\&) method


Bir alanın koduna [FieldArgumentBuilder](../../fieldargumentbuilder/) tarafından temsil edilen bir argüman ekler.

```cpp
System::SharedPtr<Aspose::Words::Fields::FieldBuilder> Aspose::Words::Fields::FieldBuilder::AddArgument(const System::SharedPtr<Aspose::Words::Fields::FieldArgumentBuilder> &argument)
```


## Örnekler



Bir alan oluşturucu kullanarak alanların nasıl oluşturulacağını ve ardından belgeye nasıl ekleneceğini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Aşağıda bir alan oluşturucu kullanılarak yapılan alan oluşturma örneklerinden üçü verilmiştir.
// 1 -  Tek alan:
// Bir alan oluşturucu kullanarak ƒ (Florin) simgesini gösteren bir SYMBOL alanı ekleyin.
auto builder = System::MakeObject<Aspose::Words::Fields::FieldBuilder>(Aspose::Words::Fields::FieldType::FieldSymbol);
builder->AddArgument(402);
builder->AddSwitch(u"\\f", u"Arial");
builder->AddSwitch(u"\\s", 25);
builder->AddSwitch(u"\\u");
System::SharedPtr<Aspose::Words::Fields::Field> field = builder->BuildAndInsert(doc->get_FirstSection()->get_Body()->get_FirstParagraph());

ASSERT_EQ(u" SYMBOL 402 \\f Arial \\s 25 \\u ", field->GetFieldCode());

// 2 -  İç içe alan:
// Bir alan oluşturucu kullanarak başka bir alan oluşturucu tarafından iç alan olarak kullanılan bir formül alanı oluşturun.
auto innerFormulaBuilder = System::MakeObject<Aspose::Words::Fields::FieldBuilder>(Aspose::Words::Fields::FieldType::FieldFormula);
innerFormulaBuilder->AddArgument(100);
innerFormulaBuilder->AddArgument(u"+");
innerFormulaBuilder->AddArgument(74);

// Başka bir SYMBOL alanı için başka bir oluşturucu oluşturun ve formül alanını ekleyin
// yukarıda oluşturduğumuz bu alanı SYMBOL alanının argümanı olarak ekleyin.
builder = System::MakeObject<Aspose::Words::Fields::FieldBuilder>(Aspose::Words::Fields::FieldType::FieldSymbol);
builder->AddArgument(innerFormulaBuilder);
field = builder->BuildAndInsert(doc->get_FirstSection()->get_Body()->AppendParagraph(System::String::Empty));

// Dış SYMBOL alanı, formül alanının sonucu olan 174'ü argümanı olarak kullanacak,
// bu da alanın karakter numarası 174 olduğu için ® (Kayıtlı İşaret) simgesini göstermesini sağlayacak.
ASSERT_EQ(u" SYMBOL \u0013 = 100 + 74 \u0014\u0015 ", field->GetFieldCode());

// 3 -  Birden fazla iç içe alan ve argüman:
// Şimdi, iki özel metin değerinden birini gösteren bir IF alanı oluşturmak için bir oluşturucu kullanacağız,
// ifadesinin doğru/yanlış değerine bağlı olarak. Doğru/yanlış bir değer elde etmek için
// IF alanının hangi metni göstereceğini belirleyen, IF alanı iki sayısal ifadeyi eşitlik için test edecektir.
// İki ifadeyi formül alanları şeklinde sağlayacağız ve bu alanları IF alanının içine iç içe yerleştireceğiz.
auto leftExpression = System::MakeObject<Aspose::Words::Fields::FieldBuilder>(Aspose::Words::Fields::FieldType::FieldFormula);
leftExpression->AddArgument(2);
leftExpression->AddArgument(u"+");
leftExpression->AddArgument(3);

auto rightExpression = System::MakeObject<Aspose::Words::Fields::FieldBuilder>(Aspose::Words::Fields::FieldType::FieldFormula);
rightExpression->AddArgument(2.5);
rightExpression->AddArgument(u"*");
rightExpression->AddArgument(5.2);

// Sonra, IF alanı için doğru/yanlış çıktı metinleri olarak hizmet edecek iki alan argümanı oluşturacağız.
// Bu argümanlar sayısal ifadelerimizin çıktı değerlerini yeniden kullanacak.
auto trueOutput = System::MakeObject<Aspose::Words::Fields::FieldArgumentBuilder>();
trueOutput->AddText(u"True, both expressions amount to ");
trueOutput->AddField(leftExpression);

auto falseOutput = System::MakeObject<Aspose::Words::Fields::FieldArgumentBuilder>();
falseOutput->AddNode(System::MakeObject<Aspose::Words::Run>(doc, u"False, "));
falseOutput->AddField(leftExpression);
falseOutput->AddNode(System::MakeObject<Aspose::Words::Run>(doc, u" does not equal "));
falseOutput->AddField(rightExpression);

// Son olarak, IF alanı için bir oluşturucu daha oluşturacak ve tüm ifadeleri birleştireceğiz.
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

## Ayrıca Bakınız

* Class [FieldBuilder](../)
* Class [FieldArgumentBuilder](../../fieldargumentbuilder/)
* Class [FieldBuilder](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
## FieldBuilder::AddArgument(const System::SharedPtr\<Aspose::Words::Fields::FieldBuilder\>\&) method


Bir alanın koduna başka bir [FieldBuilder](../) tarafından temsil edilen bir alt alan ekler.

```cpp
System::SharedPtr<Aspose::Words::Fields::FieldBuilder> Aspose::Words::Fields::FieldBuilder::AddArgument(const System::SharedPtr<Aspose::Words::Fields::FieldBuilder> &argument)
```


## Örnekler



Bir alan oluşturucu kullanarak alanların nasıl oluşturulacağını ve ardından belgeye nasıl ekleneceğini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Aşağıda bir alan oluşturucu kullanılarak yapılan alan oluşturma örneklerinden üçü verilmiştir.
// 1 -  Tek alan:
// Bir alan oluşturucu kullanarak ƒ (Florin) simgesini gösteren bir SYMBOL alanı ekleyin.
auto builder = System::MakeObject<Aspose::Words::Fields::FieldBuilder>(Aspose::Words::Fields::FieldType::FieldSymbol);
builder->AddArgument(402);
builder->AddSwitch(u"\\f", u"Arial");
builder->AddSwitch(u"\\s", 25);
builder->AddSwitch(u"\\u");
System::SharedPtr<Aspose::Words::Fields::Field> field = builder->BuildAndInsert(doc->get_FirstSection()->get_Body()->get_FirstParagraph());

ASSERT_EQ(u" SYMBOL 402 \\f Arial \\s 25 \\u ", field->GetFieldCode());

// 2 -  İç içe alan:
// Bir alan oluşturucu kullanarak başka bir alan oluşturucu tarafından iç alan olarak kullanılan bir formül alanı oluşturun.
auto innerFormulaBuilder = System::MakeObject<Aspose::Words::Fields::FieldBuilder>(Aspose::Words::Fields::FieldType::FieldFormula);
innerFormulaBuilder->AddArgument(100);
innerFormulaBuilder->AddArgument(u"+");
innerFormulaBuilder->AddArgument(74);

// Başka bir SYMBOL alanı için başka bir oluşturucu oluşturun ve formül alanını ekleyin
// yukarıda oluşturduğumuz bu alanı SYMBOL alanının argümanı olarak ekleyin.
builder = System::MakeObject<Aspose::Words::Fields::FieldBuilder>(Aspose::Words::Fields::FieldType::FieldSymbol);
builder->AddArgument(innerFormulaBuilder);
field = builder->BuildAndInsert(doc->get_FirstSection()->get_Body()->AppendParagraph(System::String::Empty));

// Dış SYMBOL alanı, formül alanının sonucu olan 174'ü argümanı olarak kullanacak,
// bu da alanın karakter numarası 174 olduğu için ® (Kayıtlı İşaret) simgesini göstermesini sağlayacak.
ASSERT_EQ(u" SYMBOL \u0013 = 100 + 74 \u0014\u0015 ", field->GetFieldCode());

// 3 -  Birden fazla iç içe alan ve argüman:
// Şimdi, iki özel metin değerinden birini gösteren bir IF alanı oluşturmak için bir oluşturucu kullanacağız,
// ifadesinin doğru/yanlış değerine bağlı olarak. Doğru/yanlış bir değer elde etmek için
// IF alanının hangi metni göstereceğini belirleyen, IF alanı iki sayısal ifadeyi eşitlik için test edecektir.
// İki ifadeyi formül alanları şeklinde sağlayacağız ve bu alanları IF alanının içine iç içe yerleştireceğiz.
auto leftExpression = System::MakeObject<Aspose::Words::Fields::FieldBuilder>(Aspose::Words::Fields::FieldType::FieldFormula);
leftExpression->AddArgument(2);
leftExpression->AddArgument(u"+");
leftExpression->AddArgument(3);

auto rightExpression = System::MakeObject<Aspose::Words::Fields::FieldBuilder>(Aspose::Words::Fields::FieldType::FieldFormula);
rightExpression->AddArgument(2.5);
rightExpression->AddArgument(u"*");
rightExpression->AddArgument(5.2);

// Sonra, IF alanı için doğru/yanlış çıktı metinleri olarak hizmet edecek iki alan argümanı oluşturacağız.
// Bu argümanlar sayısal ifadelerimizin çıktı değerlerini yeniden kullanacak.
auto trueOutput = System::MakeObject<Aspose::Words::Fields::FieldArgumentBuilder>();
trueOutput->AddText(u"True, both expressions amount to ");
trueOutput->AddField(leftExpression);

auto falseOutput = System::MakeObject<Aspose::Words::Fields::FieldArgumentBuilder>();
falseOutput->AddNode(System::MakeObject<Aspose::Words::Run>(doc, u"False, "));
falseOutput->AddField(leftExpression);
falseOutput->AddNode(System::MakeObject<Aspose::Words::Run>(doc, u" does not equal "));
falseOutput->AddField(rightExpression);

// Son olarak, IF alanı için bir oluşturucu daha oluşturacak ve tüm ifadeleri birleştireceğiz.
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

## Ayrıca Bakınız

* Class [FieldBuilder](../)
* Class [FieldBuilder](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
## FieldBuilder::AddArgument(const System::String\&) method


Bir alanın argümanını ekler.

```cpp
System::SharedPtr<Aspose::Words::Fields::FieldBuilder> Aspose::Words::Fields::FieldBuilder::AddArgument(const System::String &argument)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| argument | const System::String\& | Argüman değeri. |

## Örnekler



Bir alan oluşturucu kullanarak alanların nasıl oluşturulacağını ve ardından belgeye nasıl ekleneceğini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Aşağıda bir alan oluşturucu kullanılarak yapılan alan oluşturma örneklerinden üçü verilmiştir.
// 1 -  Tek alan:
// Bir alan oluşturucu kullanarak ƒ (Florin) simgesini gösteren bir SYMBOL alanı ekleyin.
auto builder = System::MakeObject<Aspose::Words::Fields::FieldBuilder>(Aspose::Words::Fields::FieldType::FieldSymbol);
builder->AddArgument(402);
builder->AddSwitch(u"\\f", u"Arial");
builder->AddSwitch(u"\\s", 25);
builder->AddSwitch(u"\\u");
System::SharedPtr<Aspose::Words::Fields::Field> field = builder->BuildAndInsert(doc->get_FirstSection()->get_Body()->get_FirstParagraph());

ASSERT_EQ(u" SYMBOL 402 \\f Arial \\s 25 \\u ", field->GetFieldCode());

// 2 -  İç içe alan:
// Bir alan oluşturucu kullanarak başka bir alan oluşturucu tarafından iç alan olarak kullanılan bir formül alanı oluşturun.
auto innerFormulaBuilder = System::MakeObject<Aspose::Words::Fields::FieldBuilder>(Aspose::Words::Fields::FieldType::FieldFormula);
innerFormulaBuilder->AddArgument(100);
innerFormulaBuilder->AddArgument(u"+");
innerFormulaBuilder->AddArgument(74);

// Başka bir SYMBOL alanı için başka bir oluşturucu oluşturun ve formül alanını ekleyin
// yukarıda oluşturduğumuz bu alanı SYMBOL alanının argümanı olarak ekleyin.
builder = System::MakeObject<Aspose::Words::Fields::FieldBuilder>(Aspose::Words::Fields::FieldType::FieldSymbol);
builder->AddArgument(innerFormulaBuilder);
field = builder->BuildAndInsert(doc->get_FirstSection()->get_Body()->AppendParagraph(System::String::Empty));

// Dış SYMBOL alanı, formül alanının sonucu olan 174'ü argümanı olarak kullanacak,
// bu da alanın karakter numarası 174 olduğu için ® (Kayıtlı İşaret) simgesini göstermesini sağlayacak.
ASSERT_EQ(u" SYMBOL \u0013 = 100 + 74 \u0014\u0015 ", field->GetFieldCode());

// 3 -  Birden fazla iç içe alan ve argüman:
// Şimdi, iki özel metin değerinden birini gösteren bir IF alanı oluşturmak için bir oluşturucu kullanacağız,
// ifadesinin doğru/yanlış değerine bağlı olarak. Doğru/yanlış bir değer elde etmek için
// IF alanının hangi metni göstereceğini belirleyen, IF alanı iki sayısal ifadeyi eşitlik için test edecektir.
// İki ifadeyi formül alanları şeklinde sağlayacağız ve bu alanları IF alanının içine iç içe yerleştireceğiz.
auto leftExpression = System::MakeObject<Aspose::Words::Fields::FieldBuilder>(Aspose::Words::Fields::FieldType::FieldFormula);
leftExpression->AddArgument(2);
leftExpression->AddArgument(u"+");
leftExpression->AddArgument(3);

auto rightExpression = System::MakeObject<Aspose::Words::Fields::FieldBuilder>(Aspose::Words::Fields::FieldType::FieldFormula);
rightExpression->AddArgument(2.5);
rightExpression->AddArgument(u"*");
rightExpression->AddArgument(5.2);

// Sonra, IF alanı için doğru/yanlış çıktı metinleri olarak hizmet edecek iki alan argümanı oluşturacağız.
// Bu argümanlar sayısal ifadelerimizin çıktı değerlerini yeniden kullanacak.
auto trueOutput = System::MakeObject<Aspose::Words::Fields::FieldArgumentBuilder>();
trueOutput->AddText(u"True, both expressions amount to ");
trueOutput->AddField(leftExpression);

auto falseOutput = System::MakeObject<Aspose::Words::Fields::FieldArgumentBuilder>();
falseOutput->AddNode(System::MakeObject<Aspose::Words::Run>(doc, u"False, "));
falseOutput->AddField(leftExpression);
falseOutput->AddNode(System::MakeObject<Aspose::Words::Run>(doc, u" does not equal "));
falseOutput->AddField(rightExpression);

// Son olarak, IF alanı için bir oluşturucu daha oluşturacak ve tüm ifadeleri birleştireceğiz.
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

## Ayrıca Bakınız

* Class [FieldBuilder](../)
* Class [FieldBuilder](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
## FieldBuilder::AddArgument(double) method


Bir alanın argümanını ekler.

```cpp
System::SharedPtr<Aspose::Words::Fields::FieldBuilder> Aspose::Words::Fields::FieldBuilder::AddArgument(double argument)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| argument | double | Argüman değeri. |

## Örnekler



Bir alan oluşturucu kullanarak alanların nasıl oluşturulacağını ve ardından belgeye nasıl ekleneceğini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Aşağıda bir alan oluşturucu kullanılarak yapılan alan oluşturma örneklerinden üçü verilmiştir.
// 1 -  Tek alan:
// Bir alan oluşturucu kullanarak ƒ (Florin) simgesini gösteren bir SYMBOL alanı ekleyin.
auto builder = System::MakeObject<Aspose::Words::Fields::FieldBuilder>(Aspose::Words::Fields::FieldType::FieldSymbol);
builder->AddArgument(402);
builder->AddSwitch(u"\\f", u"Arial");
builder->AddSwitch(u"\\s", 25);
builder->AddSwitch(u"\\u");
System::SharedPtr<Aspose::Words::Fields::Field> field = builder->BuildAndInsert(doc->get_FirstSection()->get_Body()->get_FirstParagraph());

ASSERT_EQ(u" SYMBOL 402 \\f Arial \\s 25 \\u ", field->GetFieldCode());

// 2 -  İç içe alan:
// Bir alan oluşturucu kullanarak başka bir alan oluşturucu tarafından iç alan olarak kullanılan bir formül alanı oluşturun.
auto innerFormulaBuilder = System::MakeObject<Aspose::Words::Fields::FieldBuilder>(Aspose::Words::Fields::FieldType::FieldFormula);
innerFormulaBuilder->AddArgument(100);
innerFormulaBuilder->AddArgument(u"+");
innerFormulaBuilder->AddArgument(74);

// Başka bir SYMBOL alanı için başka bir oluşturucu oluşturun ve formül alanını ekleyin
// yukarıda oluşturduğumuz bu alanı SYMBOL alanının argümanı olarak ekleyin.
builder = System::MakeObject<Aspose::Words::Fields::FieldBuilder>(Aspose::Words::Fields::FieldType::FieldSymbol);
builder->AddArgument(innerFormulaBuilder);
field = builder->BuildAndInsert(doc->get_FirstSection()->get_Body()->AppendParagraph(System::String::Empty));

// Dış SYMBOL alanı, formül alanının sonucu olan 174'ü argümanı olarak kullanacak,
// bu da alanın karakter numarası 174 olduğu için ® (Kayıtlı İşaret) simgesini göstermesini sağlayacak.
ASSERT_EQ(u" SYMBOL \u0013 = 100 + 74 \u0014\u0015 ", field->GetFieldCode());

// 3 -  Birden fazla iç içe alan ve argüman:
// Şimdi, iki özel metin değerinden birini gösteren bir IF alanı oluşturmak için bir oluşturucu kullanacağız,
// ifadesinin doğru/yanlış değerine bağlı olarak. Doğru/yanlış bir değer elde etmek için
// IF alanının hangi metni göstereceğini belirleyen, IF alanı iki sayısal ifadeyi eşitlik için test edecektir.
// İki ifadeyi formül alanları şeklinde sağlayacağız ve bu alanları IF alanının içine iç içe yerleştireceğiz.
auto leftExpression = System::MakeObject<Aspose::Words::Fields::FieldBuilder>(Aspose::Words::Fields::FieldType::FieldFormula);
leftExpression->AddArgument(2);
leftExpression->AddArgument(u"+");
leftExpression->AddArgument(3);

auto rightExpression = System::MakeObject<Aspose::Words::Fields::FieldBuilder>(Aspose::Words::Fields::FieldType::FieldFormula);
rightExpression->AddArgument(2.5);
rightExpression->AddArgument(u"*");
rightExpression->AddArgument(5.2);

// Sonra, IF alanı için doğru/yanlış çıktı metinleri olarak hizmet edecek iki alan argümanı oluşturacağız.
// Bu argümanlar sayısal ifadelerimizin çıktı değerlerini yeniden kullanacak.
auto trueOutput = System::MakeObject<Aspose::Words::Fields::FieldArgumentBuilder>();
trueOutput->AddText(u"True, both expressions amount to ");
trueOutput->AddField(leftExpression);

auto falseOutput = System::MakeObject<Aspose::Words::Fields::FieldArgumentBuilder>();
falseOutput->AddNode(System::MakeObject<Aspose::Words::Run>(doc, u"False, "));
falseOutput->AddField(leftExpression);
falseOutput->AddNode(System::MakeObject<Aspose::Words::Run>(doc, u" does not equal "));
falseOutput->AddField(rightExpression);

// Son olarak, IF alanı için bir oluşturucu daha oluşturacak ve tüm ifadeleri birleştireceğiz.
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

## Ayrıca Bakınız

* Class [FieldBuilder](../)
* Class [FieldBuilder](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
## FieldBuilder::AddArgument(int32_t) method


Bir alanın argümanını ekler.

```cpp
System::SharedPtr<Aspose::Words::Fields::FieldBuilder> Aspose::Words::Fields::FieldBuilder::AddArgument(int32_t argument)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| argument | int32_t | Argüman değeri. |

## Örnekler



Bir alan oluşturucu kullanarak alanların nasıl oluşturulacağını ve ardından belgeye nasıl ekleneceğini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Aşağıda bir alan oluşturucu kullanılarak yapılan alan oluşturma örneklerinden üçü verilmiştir.
// 1 -  Tek alan:
// Bir alan oluşturucu kullanarak ƒ (Florin) simgesini gösteren bir SYMBOL alanı ekleyin.
auto builder = System::MakeObject<Aspose::Words::Fields::FieldBuilder>(Aspose::Words::Fields::FieldType::FieldSymbol);
builder->AddArgument(402);
builder->AddSwitch(u"\\f", u"Arial");
builder->AddSwitch(u"\\s", 25);
builder->AddSwitch(u"\\u");
System::SharedPtr<Aspose::Words::Fields::Field> field = builder->BuildAndInsert(doc->get_FirstSection()->get_Body()->get_FirstParagraph());

ASSERT_EQ(u" SYMBOL 402 \\f Arial \\s 25 \\u ", field->GetFieldCode());

// 2 -  İç içe alan:
// Bir alan oluşturucu kullanarak başka bir alan oluşturucu tarafından iç alan olarak kullanılan bir formül alanı oluşturun.
auto innerFormulaBuilder = System::MakeObject<Aspose::Words::Fields::FieldBuilder>(Aspose::Words::Fields::FieldType::FieldFormula);
innerFormulaBuilder->AddArgument(100);
innerFormulaBuilder->AddArgument(u"+");
innerFormulaBuilder->AddArgument(74);

// Başka bir SYMBOL alanı için başka bir oluşturucu oluşturun ve formül alanını ekleyin
// yukarıda oluşturduğumuz bu alanı SYMBOL alanının argümanı olarak ekleyin.
builder = System::MakeObject<Aspose::Words::Fields::FieldBuilder>(Aspose::Words::Fields::FieldType::FieldSymbol);
builder->AddArgument(innerFormulaBuilder);
field = builder->BuildAndInsert(doc->get_FirstSection()->get_Body()->AppendParagraph(System::String::Empty));

// Dış SYMBOL alanı, formül alanının sonucu olan 174'ü argümanı olarak kullanacak,
// bu da alanın karakter numarası 174 olduğu için ® (Kayıtlı İşaret) simgesini göstermesini sağlayacak.
ASSERT_EQ(u" SYMBOL \u0013 = 100 + 74 \u0014\u0015 ", field->GetFieldCode());

// 3 -  Birden fazla iç içe alan ve argüman:
// Şimdi, iki özel metin değerinden birini gösteren bir IF alanı oluşturmak için bir oluşturucu kullanacağız,
// ifadesinin doğru/yanlış değerine bağlı olarak. Doğru/yanlış bir değer elde etmek için
// IF alanının hangi metni göstereceğini belirleyen, IF alanı iki sayısal ifadeyi eşitlik için test edecektir.
// İki ifadeyi formül alanları şeklinde sağlayacağız ve bu alanları IF alanının içine iç içe yerleştireceğiz.
auto leftExpression = System::MakeObject<Aspose::Words::Fields::FieldBuilder>(Aspose::Words::Fields::FieldType::FieldFormula);
leftExpression->AddArgument(2);
leftExpression->AddArgument(u"+");
leftExpression->AddArgument(3);

auto rightExpression = System::MakeObject<Aspose::Words::Fields::FieldBuilder>(Aspose::Words::Fields::FieldType::FieldFormula);
rightExpression->AddArgument(2.5);
rightExpression->AddArgument(u"*");
rightExpression->AddArgument(5.2);

// Sonra, IF alanı için doğru/yanlış çıktı metinleri olarak hizmet edecek iki alan argümanı oluşturacağız.
// Bu argümanlar sayısal ifadelerimizin çıktı değerlerini yeniden kullanacak.
auto trueOutput = System::MakeObject<Aspose::Words::Fields::FieldArgumentBuilder>();
trueOutput->AddText(u"True, both expressions amount to ");
trueOutput->AddField(leftExpression);

auto falseOutput = System::MakeObject<Aspose::Words::Fields::FieldArgumentBuilder>();
falseOutput->AddNode(System::MakeObject<Aspose::Words::Run>(doc, u"False, "));
falseOutput->AddField(leftExpression);
falseOutput->AddNode(System::MakeObject<Aspose::Words::Run>(doc, u" does not equal "));
falseOutput->AddField(rightExpression);

// Son olarak, IF alanı için bir oluşturucu daha oluşturacak ve tüm ifadeleri birleştireceğiz.
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

## Ayrıca Bakınız

* Class [FieldBuilder](../)
* Class [FieldBuilder](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
