---
title: "Aspose::Words::Fields::FieldBuilder::BuildAndInsert metodu"
linktitle: "BuildAndInsert"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fields::FieldBuilder::BuildAndInsert metodu. C++'ta belirtilen satır içi düğümden önce bir alanı belgeye oluşturur ve ekler."
type: docs
weight: 5000
url: /tr/cpp/aspose.words.fields/fieldbuilder/buildandinsert/
---
## FieldBuilder::BuildAndInsert(const System::SharedPtr\<Aspose::Words::Inline\>\&) method


Belirtilen satır içi düğümün önüne bir alan oluşturur ve belgeye ekler.

```cpp
System::SharedPtr<Aspose::Words::Fields::Field> Aspose::Words::Fields::FieldBuilder::BuildAndInsert(const System::SharedPtr<Aspose::Words::Inline> &refNode)
```


### ReturnValue

Eklelen alanı temsil eden bir [Field](../../field/) nesnesi.

## Örnekler



Bir alan oluşturucu kullanarak bir alanın nasıl oluşturulup ekleneceğini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Bir belgeye metin içeriği eklemenin pratik bir yolu belge oluşturucu kullanmaktır.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Write(u" Hello world! This text is one Run, which is an inline node.");

// Alanların kendi oluşturucuları vardır; bunları alan kodunu parça parça oluşturmak için de kullanabiliriz.
// Bu durumda, ABD posta kodunu temsil eden bir BARCODE alanı oluşturacağız,
// ve ardından bunu bir Run'un önüne ekleyeceğiz.
auto fieldBuilder = System::MakeObject<Aspose::Words::Fields::FieldBuilder>(Aspose::Words::Fields::FieldType::FieldBarcode);
fieldBuilder->AddArgument(u"90210");
fieldBuilder->AddSwitch(u"\\f", u"A");
fieldBuilder->AddSwitch(u"\\u");

fieldBuilder->BuildAndInsert(doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0));

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.CreateWithFieldBuilder.docx");
```

## Ayrıca Bakınız

* Class [Field](../../field/)
* Class [Inline](../../../aspose.words/inline/)
* Class [FieldBuilder](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
## FieldBuilder::BuildAndInsert(const System::SharedPtr\<Aspose::Words::Paragraph\>\&) method


Belirtilen paragrafın sonuna bir alan oluşturur ve belgeye ekler.

```cpp
System::SharedPtr<Aspose::Words::Fields::Field> Aspose::Words::Fields::FieldBuilder::BuildAndInsert(const System::SharedPtr<Aspose::Words::Paragraph> &refNode)
```


### ReturnValue

Eklelen alanı temsil eden bir [Field](../../field/) nesnesi.

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

* Class [Field](../../field/)
* Class [Paragraph](../../../aspose.words/paragraph/)
* Class [FieldBuilder](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
