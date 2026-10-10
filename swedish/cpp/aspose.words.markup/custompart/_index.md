---
title: "Aspose::Words::Markup::CustomPart klass"
linktitle: "CustomPart"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Markup::CustomPart klass. Representerar en anpassad (godtycklig innehåll) del som inte är definierad av ISO/IEC 29500-standarden. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 1000
url: /sv/cpp/aspose.words.markup/custompart/
---
## CustomPart class


Representerar en anpassad (godtycklig innehålls)del som inte definieras av ISO/IEC 29500-standarden. För att lära dig mer, besök dokumentationsartikeln [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/).

```cpp
class CustomPart : public System::Object
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [Clone](./clone/)() | Skapar en "tillräckligt djup" kopia av objektet. Duplicerar inte byte av [Data](./get_data/) värdet. |
| [CustomPart](./custompart/)() |  |
| [get_ContentType](./get_contenttype/)() const | Anger innehållstypen för denna anpassade del. |
| [get_Data](./get_data/)() const | Innehåller data för denna anpassade del. |
| [get_IsExternal](./get_isexternal/)() const | Falskt om denna anpassade del lagras i OOXML-paketet. Sant om denna anpassade del är ett externt mål. |
| [get_Name](./get_name/)() const | Hämtar eller anger delens absoluta namn inom OOXML-paketet eller mål‑URL:en. |
| [get_RelationshipType](./get_relationshiptype/)() const | Hämtar eller anger relationstypen från förälderdelen till denna anpassade del. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_ContentType](./set_contenttype/)(const System::String\&) | Sättare för [Aspose::Words::Markup::CustomPart::get_ContentType](./get_contenttype/). |
| [set_Data](./set_data/)(const System::ArrayPtr\<uint8_t\>\&) | Sättare för [Aspose::Words::Markup::CustomPart::get_Data](./get_data/). |
| [set_IsExternal](./set_isexternal/)(bool) | Sättare för [Aspose::Words::Markup::CustomPart::get_IsExternal](./get_isexternal/). |
| [set_Name](./set_name/)(const System::String\&) | Sättare för [Aspose::Words::Markup::CustomPart::get_Name](./get_name/). |
| [set_RelationshipType](./set_relationshiptype/)(const System::String\&) | Sättare för [Aspose::Words::Markup::CustomPart::get_RelationshipType](./get_relationshiptype/). |
| static [Type](./type/)() |  |
## Anmärkningar


Denna klass representerar en OOXML-del som är mål för ett "okänt förhållande". Alla förhållanden som inte är definierade i ISO/IEC 29500 betraktas som "okända förhållanden". Okända förhållanden är tillåtna i ett Office Open XML-dokument förutsatt att de följer riktlinjerna för relationsmarkup.

Microsoft Word bevarar anpassade delar under öppna/spara-cykler. Ytterligare information kan hittas här [http://blogs.msdn.com/dmahugh/archive/2006/11/25/arbitrary-content-in-an-opc-package.aspx](http://blogs.msdn.com/dmahugh/archive/2006/11/25/arbitrary-content-in-an-opc-package.aspx)

Aspose.Words roundtripper också anpassade delar och tillåter dessutom att programmässigt komma åt sådana delar via objekten [CustomPart](./) och [CustomPartCollection](../custompartcollection/).

Förväxla inte anpassade delar med Custom XML Data. Använd [CustomXmlPart](../customxmlpart/) om du behöver komma åt Custom XML Data.

## Exempel



Visar hur man får åtkomst till ett dokuments godtyckliga samling av anpassade delar.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Custom parts OOXML package.docx");

ASSERT_EQ(2, doc->get_PackageCustomParts()->get_Count());

// Klona den andra delen och lägg sedan till klonen i samlingen.
System::SharedPtr<Aspose::Words::Markup::CustomPart> clonedPart = doc->get_PackageCustomParts()->idx_get(1)->Clone();
doc->get_PackageCustomParts()->Add(clonedPart);

ASSERT_EQ(3, doc->get_PackageCustomParts()->get_Count());

// Iterera över samlingen och skriv ut varje del.
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::Markup::CustomPart>>> enumerator = doc->get_PackageCustomParts()->GetEnumerator();
    int32_t index = 0;
    while (enumerator->MoveNext())
    {
        std::cout << System::String::Format(u"Part index {0}:", index) << std::endl;
        std::cout << System::String::Format(u"\tName:\t\t\t\t{0}", enumerator->get_Current()->get_Name()) << std::endl;
        std::cout << System::String::Format(u"\tContent type:\t\t{0}", enumerator->get_Current()->get_ContentType()) << std::endl;
        std::cout << System::String::Format(u"\tRelationship type:\t{0}", enumerator->get_Current()->get_RelationshipType()) << std::endl;
        std::cout << (enumerator->get_Current()->get_IsExternal() ? u"\tSourced from outside the document" : System::String::Format(u"\tStored within the document, length: {0} bytes", enumerator->get_Current()->get_Data()->get_Length())) << std::endl;
        index++;
    }
}

// Vi kan ta bort element från den här samlingen individuellt eller alla på en gång.
doc->get_PackageCustomParts()->RemoveAt(2);

ASSERT_EQ(2, doc->get_PackageCustomParts()->get_Count());

doc->get_PackageCustomParts()->Clear();

ASSERT_EQ(0, doc->get_PackageCustomParts()->get_Count());
```

## Se även

* Namespace [Aspose::Words::Markup](../)
* Library [Aspose.Words for C++](../../)
