---
title: "Aspose::Words::CleanupOptions‑klass"
linktitle: "CleanupOptions"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::CleanupOptions‑klass. Tillåter att ange alternativ för dokumentrengöring. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 10000
url: /sv/cpp/aspose.words/cleanupoptions/
---
## CleanupOptions class


Tillåter att ange alternativ för dokumentrengöring. För att läsa mer, besök dokumentationsartikeln [Rensa ett dokument](https://docs.aspose.com/words/cpp/clean-up-a-document/).

```cpp
class CleanupOptions : public System::Object
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [CleanupOptions](./cleanupoptions/)() |  |
| [get_DuplicateStyle](./get_duplicatestyle/)() const | Hämtar/sätter en flagga som indikerar om dubblettstilar ska tas bort från dokumentet. Standardvärdet är **false**. |
| [get_UnusedBuiltinStyles](./get_unusedbuiltinstyles/)() const | Anger att oanvända [BuiltIn](../style/get_builtin/) stilar ska tas bort från dokumentet. |
| [get_UnusedLists](./get_unusedlists/)() const | Anger om oanvända listor och listdefinitioner ska tas bort från dokumentet. Standardvärdet är **true**. |
| [get_UnusedStyles](./get_unusedstyles/)() const | Anger om oanvända stilar ska tas bort från dokumentet. Standardvärdet är **true**. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_DuplicateStyle](./set_duplicatestyle/)(bool) | Sättare för [Aspose::Words::CleanupOptions::get_DuplicateStyle](./get_duplicatestyle/). |
| [set_UnusedBuiltinStyles](./set_unusedbuiltinstyles/)(bool) | Sättare för [Aspose::Words::CleanupOptions::get_UnusedBuiltinStyles](./get_unusedbuiltinstyles/). |
| [set_UnusedLists](./set_unusedlists/)(bool) | Sättare för [Aspose::Words::CleanupOptions::get_UnusedLists](./get_unusedlists/). |
| [set_UnusedStyles](./set_unusedstyles/)(bool) | Inställare för [Aspose::Words::CleanupOptions::get_UnusedStyles](./get_unusedstyles/). |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
