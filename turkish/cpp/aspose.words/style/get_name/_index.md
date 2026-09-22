---
title: "Aspose::Words::Style::get_Name yöntemi"
linktitle: "get_Name"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Style::get_Name yöntemi. C++'ta stilin adını alır veya ayarlar."
type: docs
weight: 14000
url: /tr/cpp/aspose.words/style/get_name/
---
## Style::get_Name method


Stilin adını alır veya ayarlar.

```cpp
System::String Aspose::Words::Style::get_Name() const
```

## Açıklamalar


Boş dize olamaz.

Koleksiyonda zaten bu isimde bir stil varsa, bu stil onu geçersiz kılar. Tüm etkilenen düğümler yeni stile referans verir.

## Örnekler



Bir belgenin stil koleksiyonuna nasıl erişileceğini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

ASSERT_EQ(4, doc->get_Styles()->get_Count());

// Aspose.Words kullanılarak oluşturulan bir belgenin varsayılan olarak içerdiği tüm stilleri numaralandırın ve listeleyin.
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::Style>>> stylesEnum = doc->get_Styles()->GetEnumerator();
    while (stylesEnum->MoveNext())
    {
        System::SharedPtr<Aspose::Words::Style> curStyle = stylesEnum->get_Current();
        std::cout << System::String::Format(u"Style name:\t\"{0}\", of type \"{1}\"", curStyle->get_Name(), curStyle->get_Type()) << std::endl;
        std::cout << System::String::Format(u"\tSubsequent style:\t{0}", curStyle->get_NextParagraphStyleName()) << std::endl;
        std::cout << System::String::Format(u"\tIs heading:\t\t\t{0}", curStyle->get_IsHeading()) << std::endl;
        std::cout << System::String::Format(u"\tIs QuickStyle:\t\t{0}", curStyle->get_IsQuickStyle()) << std::endl;

        ASPOSE_ASSERT_EQ(doc, curStyle->get_Document());
    }
}
```


Bir belgenin stilinin nasıl klonlanacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// AddCopy yöntemi belirtilen stilin bir kopyasını oluşturur ve
// stil için otomatik olarak yeni bir ad oluşturur, örneğin "Heading 1_0".
System::SharedPtr<Aspose::Words::Style> newStyle = doc->get_Styles()->AddCopy(doc->get_Styles()->idx_get(u"Heading 1"));

// Stilin tanımlayıcı adını değiştirmek için stilin "Name" özelliğini kullanın.
newStyle->set_Name(u"My Heading 1");

// Belgemizde artık farklı adlara sahip iki aynı görünümlü stil var.
// Stillerden birinin ayarlarını değiştirmek diğerini etkilemez.
newStyle->get_Font()->set_Color(System::Drawing::Color::get_Red());

ASSERT_EQ(u"My Heading 1", newStyle->get_Name());
ASSERT_EQ(u"Heading 1", doc->get_Styles()->idx_get(u"Heading 1")->get_Name());

ASSERT_EQ(doc->get_Styles()->idx_get(u"Heading 1")->get_Type(), newStyle->get_Type());
ASSERT_EQ(doc->get_Styles()->idx_get(u"Heading 1")->get_Font()->get_Name(), newStyle->get_Font()->get_Name());
ASPOSE_ASSERT_EQ(doc->get_Styles()->idx_get(u"Heading 1")->get_Font()->get_Size(), newStyle->get_Font()->get_Size());
ASPOSE_ASSERT_NE(doc->get_Styles()->idx_get(u"Heading 1")->get_Font()->get_Color(), newStyle->get_Font()->get_Color());
```

## Ayrıca Bakınız

* Class [Style](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
