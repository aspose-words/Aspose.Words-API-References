---
title: "Aspose::Words::CleanupOptions::get_UnusedLists‑metod"
linktitle: "get_UnusedLists"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::CleanupOptions::get_UnusedLists‑metod. Anger om oanvända listor och listdefinitioner ska tas bort från dokumentet. Standardvärdet är true i C++."
type: docs
weight: 5000
url: /sv/cpp/aspose.words/cleanupoptions/get_unusedlists/
---
## CleanupOptions::get_UnusedLists method


Anger om oanvända listor och listdefinitioner ska tas bort från dokumentet. Standardvärdet är **true**.

```cpp
bool Aspose::Words::CleanupOptions::get_UnusedLists() const
```


## Exempel



Visar hur man tar bort alla oanvända anpassade stilar från ett dokument.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

doc->get_Styles()->Add(Aspose::Words::StyleType::List, u"MyListStyle1");
doc->get_Styles()->Add(Aspose::Words::StyleType::List, u"MyListStyle2");
doc->get_Styles()->Add(Aspose::Words::StyleType::Character, u"MyParagraphStyle1");
doc->get_Styles()->Add(Aspose::Words::StyleType::Character, u"MyParagraphStyle2");

// Kombinerat med de inbyggda stilarna har dokumentet nu åtta stilar.
// En anpassad stil markeras som "använd" så länge det finns någon text i dokumentet
// formaterad i den stilen. Detta betyder att de 4 stilar vi lade till för närvarande är oanvända.
ASSERT_EQ(8, doc->get_Styles()->get_Count());

// Applicera en anpassad teckenstil och sedan en anpassad liststil. Att göra så markerar dem som "använd".
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->get_Font()->set_Style(doc->get_Styles()->idx_get(u"MyParagraphStyle1"));
builder->Writeln(u"Hello world!");

System::SharedPtr<Aspose::Words::Lists::List> list = doc->get_Lists()->Add(doc->get_Styles()->idx_get(u"MyListStyle1"));
builder->get_ListFormat()->set_List(list);
builder->Writeln(u"Item 1");
builder->Writeln(u"Item 2");

// Nu finns det en oanvänd teckenstil och en oanvänd liststil.
// Metoden Cleanup() kan, när den är konfigurerad med ett CleanupOptions-objekt, rikta in sig på oanvända stilar och ta bort dem.
auto cleanupOptions = System::MakeObject<Aspose::Words::CleanupOptions>();
cleanupOptions->set_UnusedLists(true);
cleanupOptions->set_UnusedStyles(true);
cleanupOptions->set_UnusedBuiltinStyles(true);

doc->Cleanup(cleanupOptions);

ASSERT_EQ(4, doc->get_Styles()->get_Count());

// Att ta bort varje nod som en anpassad stil tillämpas på markerar den som "oanvänd" igen.
// Kör Cleanup-metoden igen för att ta bort dem.
doc->get_FirstSection()->get_Body()->RemoveAllChildren();
doc->Cleanup(cleanupOptions);

ASSERT_EQ(2, doc->get_Styles()->get_Count());
```

## Se även

* Class [CleanupOptions](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
