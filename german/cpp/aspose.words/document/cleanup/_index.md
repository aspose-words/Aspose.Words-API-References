---
title: "Aspose::Words::Document::Cleanup-Methode"
linktitle: "Cleanup"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Document::Cleanup-Methode. Bereinigt ungenutzte Formatvorlagen und Listen aus dem Dokument in C++."
type: docs
weight: 6000
url: /de/cpp/aspose.words/document/cleanup/
---
## Document::Cleanup() method


Bereinigt ungenutzte Formatvorlagen und Listen aus dem Dokument.

```cpp
void Aspose::Words::Document::Cleanup()
```


## Beispiele



Zeigt, wie ungenutzte benutzerdefinierte Formatvorlagen aus einem Dokument entfernt werden.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

doc->get_Styles()->Add(Aspose::Words::StyleType::List, u"MyListStyle1");
doc->get_Styles()->Add(Aspose::Words::StyleType::List, u"MyListStyle2");
doc->get_Styles()->Add(Aspose::Words::StyleType::Character, u"MyParagraphStyle1");
doc->get_Styles()->Add(Aspose::Words::StyleType::Character, u"MyParagraphStyle2");

// In Kombination mit den integrierten Stilen hat das Dokument jetzt acht Stile.
// Eine benutzerdefinierte Formatvorlage gilt als "verwendet", wenn sie auf einen Teil des Dokuments angewendet wird,
// was bedeutet, dass die vier von uns hinzugefügten Formatvorlagen derzeit ungenutzt sind.
ASSERT_EQ(8, doc->get_Styles()->get_Count());

// Wenden Sie eine benutzerdefinierte Zeichenformatvorlage und anschließend eine benutzerdefinierte Listenvorlage an. Dadurch werden die Formatvorlagen als "verwendet" markiert.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->get_Font()->set_Style(doc->get_Styles()->idx_get(u"MyParagraphStyle1"));
builder->Writeln(u"Hello world!");

System::SharedPtr<Aspose::Words::Lists::List> list = doc->get_Lists()->Add(doc->get_Styles()->idx_get(u"MyListStyle1"));
builder->get_ListFormat()->set_List(list);
builder->Writeln(u"Item 1");
builder->Writeln(u"Item 2");

doc->Cleanup();

ASSERT_EQ(6, doc->get_Styles()->get_Count());

// Das Entfernen jedes Knotens, auf den ein benutzerdefinierter Stil angewendet wird, markiert ihn erneut als "nicht verwendet".
// Führen Sie die Cleanup-Methode erneut aus, um sie zu entfernen.
doc->get_FirstSection()->get_Body()->RemoveAllChildren();
doc->Cleanup();

ASSERT_EQ(4, doc->get_Styles()->get_Count());
```

## Siehe auch

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::Cleanup(const System::SharedPtr\<Aspose::Words::CleanupOptions\>\&) method


Bereinigt ungenutzte Formatvorlagen und Listen aus dem Dokument basierend auf den angegebenen [CleanupOptions](../../cleanupoptions/).

```cpp
void Aspose::Words::Document::Cleanup(const System::SharedPtr<Aspose::Words::CleanupOptions> &options)
```


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

* Class [CleanupOptions](../../cleanupoptions/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
