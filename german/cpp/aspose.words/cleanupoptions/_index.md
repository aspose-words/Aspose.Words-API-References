---
title: "Aspose::Words::CleanupOptions Klasse"
linktitle: "CleanupOptions"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::CleanupOptions Klasse. Ermöglicht das Festlegen von Optionen für die Dokumentenbereinigung. Weitere Informationen finden Sie im Dokumentationsartikel in C++."
type: docs
weight: 10000
url: /de/cpp/aspose.words/cleanupoptions/
---
## CleanupOptions class


Ermöglicht das Festlegen von Optionen für die Dokumentenbereinigung. Weitere Informationen finden Sie im Dokumentationsartikel [Clean Up a Document](https://docs.aspose.com/words/cpp/clean-up-a-document/).

```cpp
class CleanupOptions : public System::Object
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [CleanupOptions](./cleanupoptions/)() |  |
| [get_DuplicateStyle](./get_duplicatestyle/)() const | Liest/legt ein Flag fest, das angibt, ob doppelte Formatvorlagen aus dem Dokument entfernt werden sollen. Standardwert ist **false**. |
| [get_UnusedBuiltinStyles](./get_unusedbuiltinstyles/)() const | Gibt an, dass ungenutzte [BuiltIn](../style/get_builtin/) Formatvorlagen aus dem Dokument entfernt werden sollen. |
| [get_UnusedLists](./get_unusedlists/)() const | Gibt an, ob ungenutzte Listen und Listendefinitionen aus dem Dokument entfernt werden sollen. Standardwert ist **true**. |
| [get_UnusedStyles](./get_unusedstyles/)() const | Gibt an, ob ungenutzte Formatvorlagen aus dem Dokument entfernt werden sollen. Standardwert ist **true**. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_DuplicateStyle](./set_duplicatestyle/)(bool) | Setter für [Aspose::Words::CleanupOptions::get_DuplicateStyle](./get_duplicatestyle/). |
| [set_UnusedBuiltinStyles](./set_unusedbuiltinstyles/)(bool) | Setter für [Aspose::Words::CleanupOptions::get_UnusedBuiltinStyles](./get_unusedbuiltinstyles/). |
| [set_UnusedLists](./set_unusedlists/)(bool) | Setter für [Aspose::Words::CleanupOptions::get_UnusedLists](./get_unusedlists/). |
| [set_UnusedStyles](./set_unusedstyles/)(bool) | Setter für [Aspose::Words::CleanupOptions::get_UnusedStyles](./get_unusedstyles/). |
| static [Type](./type/)() |  |

## Beispiele



Zeigt, wie alle nicht verwendeten benutzerdefinierten Stile aus einem Dokument entfernt werden können.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

doc->get_Styles()->Add(Aspose::Words::StyleType::List, u"MyListStyle1");
doc->get_Styles()->Add(Aspose::Words::StyleType::List, u"MyListStyle2");
doc->get_Styles()->Add(Aspose::Words::StyleType::Character, u"MyParagraphStyle1");
doc->get_Styles()->Add(Aspose::Words::StyleType::Character, u"MyParagraphStyle2");

// In Kombination mit den integrierten Stilen hat das Dokument jetzt acht Stile.
// Ein benutzerdefinierter Stil wird als "verwendet" markiert, solange im Dokument irgendein Text vorhanden ist
// der in diesem Stil formatiert ist. Das bedeutet, dass die 4 von uns hinzugefügten Stile derzeit nicht verwendet werden.
ASSERT_EQ(8, doc->get_Styles()->get_Count());

// Wenden Sie einen benutzerdefinierten Zeichenstil an und anschließend einen benutzerdefinierten Listenstil an. Dadurch werden sie als "verwendet" markiert.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->get_Font()->set_Style(doc->get_Styles()->idx_get(u"MyParagraphStyle1"));
builder->Writeln(u"Hello world!");

System::SharedPtr<Aspose::Words::Lists::List> list = doc->get_Lists()->Add(doc->get_Styles()->idx_get(u"MyListStyle1"));
builder->get_ListFormat()->set_List(list);
builder->Writeln(u"Item 1");
builder->Writeln(u"Item 2");

// Jetzt gibt es einen nicht verwendeten Zeichenstil und einen nicht verwendeten Listenstil.
// Die Methode Cleanup(), wenn sie mit einem CleanupOptions-Objekt konfiguriert ist, kann nicht verwendete Stile anvisieren und entfernen.
auto cleanupOptions = System::MakeObject<Aspose::Words::CleanupOptions>();
cleanupOptions->set_UnusedLists(true);
cleanupOptions->set_UnusedStyles(true);
cleanupOptions->set_UnusedBuiltinStyles(true);

doc->Cleanup(cleanupOptions);

ASSERT_EQ(4, doc->get_Styles()->get_Count());

// Das Entfernen jedes Knotens, auf den ein benutzerdefinierter Stil angewendet wird, markiert ihn erneut als "nicht verwendet".
// Führen Sie die Cleanup-Methode erneut aus, um sie zu entfernen.
doc->get_FirstSection()->get_Body()->RemoveAllChildren();
doc->Cleanup(cleanupOptions);

ASSERT_EQ(2, doc->get_Styles()->get_Count());
```

## Siehe auch

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
